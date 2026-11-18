# Server multiplayer game layer

This folder owns authoritative server multiplayer behavior: validating and handling client messages, maintaining player/session and entity/world state, dispatching events, and deciding what state to synchronize. It is not a game executable or a publisher-provided server. Client input is untrusted; game-function declarations belong in `source/shared/sdk/` when an integration path is established.
