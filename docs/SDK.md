# Shared game SDK

`source/shared/sdk/` is the one SDK folder currently present. It is intended to hold the project's shared library of game-function declarations or wrappers that client code can call, and server code only if a suitable interface exists.

Keep the SDK aligned with original project code. For every declaration, record its source, target game build/version, confidence, constraints, and supported use in [the SDK research notes](research/game-sdk/README.md). Do not place proprietary game files or source code here. The folder is not a claim that any particular integration is supported.

Lua runtimes remain under the client and server scripting areas. Any Lua binding to game functions must use this shared SDK boundary and honor the runtime's capability and resource limits.
