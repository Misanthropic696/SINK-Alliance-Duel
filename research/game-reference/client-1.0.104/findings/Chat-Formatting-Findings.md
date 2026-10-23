# Chat formatting findings

Scope: extracted client com.phs.global 1.0.104; current live server behavior not tested.

UIChatMainPanel.CheckSendStringLegal calls GStringUtil.CheckRichStringForSend. Failure displays translation key 10103 and aborts send. The path is used for private chat, ordinary world/alliance chat, and trumpet messages.

GStringUtil lowercases input before checking literal blocked strings. Blocked prefixes include <color=, [color=, <#, [#, <size=, [size=; bold, italic and strikethrough tags; alignment, alpha, spacing, fonts, indentation, links, margins, marks, styles, scale and other rich-text prefixes. Case changes do not avoid this check.

HasColorCode also rejects six consecutive hexadecimal characters (0-9/a-f) inside square or angle brackets, including mixed brackets. Thus [FF0000], [000000], [c][FF0000]text[-][/c], and <color=#FF0000>text</color> fail this client check. Detection concerns formatting syntax, not a particular color.

A plain unbracketed #FF0000 is not matched by these specific rich-text checks, but it is plain text and does not establish colored rendering or server acceptance.

SmartReplace removes actual line breaks from ordinary chat input. Message length is checked separately against self.chatMax. Other server/content restrictions are not established by this finding.

Display/announcement code contains conversion between <color=#RRGGBB> and [c][RRGGBB]...[-][/c]. Renderer support does not imply players may send those tags through ordinary chat.

Evidence:
- client-code/source/luascript_ability__GStringUtil__asset-6810387780762786629.lua: strList, CheckRichStringForSend, HasColorCode, SmartReplace.
- client-code/source/luascript_eyu_logic_ui_panel_chat__UIChatMainPanel__asset8125789555758892691.lua: CheckSendStringLegal and OnSend.
- client-code/source/luascript_logic__ChatRoom__asset7220557855009450037.lua: SendChat/_Send.

This establishes the existing client restriction; without an older package comparison it does not date when the rule was introduced.
