# Shared game SDK layer

This is the project's shared library boundary for original wrappers, types, and declarations used by client-side game features. It is separate from the multiplayer client/server runtimes and from any future developer-facing scripting API.

Keep this library portable across project modules where practical. Record the source, game/build version, confidence, and constraints for every game-facing declaration in `docs/research/game-sdk/`. Do not store the game's source code or assets here. Do not add bypasses for anti-cheat, access controls, or other platform protections.

The existence of this folder does not mean that a supported game interface or lawful integration path has been confirmed. Add implementation only after the project scope gate is met.
