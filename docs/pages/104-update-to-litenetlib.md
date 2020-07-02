# How to update from UNET to LiteNetLibManager

To update from UNET to LiteNetLibManager, you have to remove all UNET components from networking objects then add LiteNetLibManager components. There are following networking objects you have to make changes:

* `CharacterEntity`, removes: `NetworkTransform`, `NetworkProximityChecker` and `NetworkIdentity`, then adds: `LiteNetLibIdentity`, `LiteNetLibTransform` and `LiteNetLibVisibleChecker` (optional).
* `BotEntity`, removes: `NetworkTransform`, `NetworkProximityChecker` and `NetworkIdentity`, then adds: `LiteNetLibIdentity`, `LiteNetLibTransform` and `LiteNetLibVisibleChecker` (optional).
* `PowerupEntity`, removes: `NetworkIdentity`, then adds: `LiteNetLibIdentity`.
* `PickupEntity`, removes: `NetworkIdentity`, then adds: `LiteNetLibIdentity`.
* `TrapEntity`, removes: `NetworkIdentity`, then adds: `LiteNetLibIdentity`.
* `GameplayManager`, removes: `NetworkIdentity`, then adds: `LiteNetLibIdentity`.
* `GameNetworkManager`, adds: `LiteNetLibAssets` and `LiteNetLibDiscovery`.