# Controller Mapping

Source-reviewed snapshot: **2026-09-03**. The native Fire TV shell handles
application shortcuts and selected TV navigation pages. Game controls on the
wheel/player routes are otherwise passed through to EmuHub's active runtime.

## Application shortcuts

| Input | Client action |
| --- | --- |
| Fire TV remote Menu | Open native EmuHub menu |
| Keyboard F1 or Ctrl+M | Open native EmuHub menu |
| Hold L3 + R3 for 700 ms | Open native EmuHub menu |
| Select + Start together | Request gameplay exit to the previous wheel when the second button goes down |
| Back | Navigate WebView history; confirm exit at the root |

The two-button shortcuts are client actions, not guest commands. Be aware of
the exit chord when a game asks for Select and Start simultaneously. Holding
both stick clicks invokes the client menu rather than only two guest clicks.

## Login and account navigation

D-pad, gamepad hat, and left stick navigate the geometric focus model on the
supported login/account pages. Enter, Center, or the Android A event activates;
the Android B event backs out. The Fire TV keyboard opens for editable fields.
These rules do not redefine the guest console's A/B labels during gameplay.

## Game input

The active EmuHub player/core determines original-console mappings. Record the
runtime and its mapping along with the Android controller profile. Arcade Coin
and Start are distinct; a physical Select button is commonly the Coin source,
but must be checked against that core's configuration.

Do not copy unrelated runtime button IDs into Android KeyEvents.
`BUTTON_THUMBL`, `BUTTON_THUMBR`, `BUTTON_SELECT`, and `BUTTON_START` are the
events inspected for the client shortcuts above.

## Controller qualification

8BitDo SN30/SF30-family, PlayStation, and Xbox pads are targets, not blanket
certifications. Android mode, firmware, OS support, and device model matter.
Test D-pad diagonals, both sticks, triggers, L3/R3, repeated press/release,
disconnect/reconnect, player assignment, and both client chords. Verify rumble
separately; detecting buttons does not prove haptics support.
