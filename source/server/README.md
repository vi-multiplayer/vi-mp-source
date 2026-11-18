# Server

Reserved for original project software for hosting or managing multiplayer sessions. `game/` contains authoritative multiplayer behavior, while `network/` and `scripting/` keep connection and Lua concerns separate. No dedicated game server is assumed. Define operator requirements and a threat model before implementation. See [the structure guide](../../docs/STRUCTURE.md).
