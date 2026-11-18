# Client multiplayer game layer

This folder owns the client's multiplayer game behavior: handlers for server messages and multiplayer events, player/entity state, game-state synchronization, and client-side lifecycle. It is not just a game integration adapter and contains no game files. Keep reusable game-function declarations in `source/shared/sdk/` and use only integration methods supported by the target environment.
