# Changelog (LiteNetLibManager)

## 1.31c (2021-04-05)
- Fix null data break update loop.
- Fix unsynced aim position.
- Don't update aim position for non-owning characters.

## 1.31b (2021-03-29)
- Fix attack joystick missing events.

## 1.31 (2021-03-29)
- Improve character movement, now it has to attached `CharacterMovement` component to `CharacterEntity` when you attaches `CharacterMovement` component, you have to set `CharacterController` settings to cover your character and you have to set attached colliders to be trigger collider.
- Add third person view mode, you have to change `FollowCamera` component which usaully attached to main camera to `FollowCameraControls` component.
- Add `ViewMode` settings to `CharacterEntity`, you can set it to `TopDown` and `ThirdPerson`.
- Add `TopDownViewModeSettings` it will be applied to `FollowCameraControls` and main camera when `ViewMode` is `TopDown`.
- Add `ThirdPersionViewModeSettings` it will be applied to `FollowCameraControls` and main camera when `ViewMode` is `ThirdPerson`.

## 1.30c (2021-02-21)
- Update to latest LiteNetLibManager version.
- Fix networked prefabs not registered before server start.
- Add `-gameBotCount` environment configuration, use it to set bot count when start dedicated server.
- Add `-gameMatchTime` environment configuration, use it to set match time when start dedicated server.
- Add `-gameMatchKill` environment configuration, use it to set kill count to win when start dedicated server.
- Add `-gameMatchScore` environment configuration, use it to score count to win when start dedicated server.
- Kick client whom connecting while match ended.
- Restart server after match ended.
- Fix wrong player's ranking when match end.
- Fix null-reference for on-screen mobile controller when start non-mobile games.

## 1.30 (2020-07-02)
- Change networking system to `LiteNetLibManager` (You should read [how to update](../pages/104-update-to-litenetlib.md)).
- Change to move characters by changes transform's position, rigibody will be used to applies force.
- Add `ExplosionForce` and `ExplosionForceRadius` settings to `Damage Entity` it will applies to force character when damage entity hit or explode.

# Changelog (UNET)

## 1.25b (2020-02-12)
- Reduce shoot packet size
- Fix null exceptions occuring after enter or exit `HideArea`

## 1.25
- Fix invalid weapon model's damage launch transform position.
- Add muzzle effect prefab config to damage entity.
- Implement NavMesh to BotEntity, Bot will find paths from NavMesh if there is baked NavMesh in the scene. Developers don't have to add NavMeshAgent to BotEntity.
- Bots can dash.
- Bots can increase their attributes.

## 1.24b
- Fix hide area bugs

## 1.24
- Add `HideArea`, developer can attach this component to grasses which will be used to hide characters

## 1.23d
- Avoid null exception when there is no head to select
- Add plane to Battle Royale demo

## 1.23c
- Fix invalid execute order

## 1.23b
- Fix bought items won't be saved

## 1.23
- Add codes to support Playfab integration project (https://github.com/insthync/dot-io-playfab-client)

## 1.22
- Reduce packets size
- Add custom equipment

## 1.21b
- Fix bots pickup currencies to players bugs
- Move map list and game rules from `Create game UI` to `Game instance`
- Add `Attack Signal Object` to Character Entity, can use this to show UIs which telling player that the character is attacking

## 1.21
- Add end match reward

## 1.20
- Add pick up UIs, will appear when `Gameplay Manager` -> `Auto Pickup` set to FALSE
- Can set start weapons at gameplay rules
- Not allow player attacks in Battle Royale mode when spawning

## 1.19
- Fix codes that duplicating with Fantasy Customization Pack project

## 1.18
- Add the ability to dash, can set settings at Character Entity / Character Animator Controller

## 1.17
- Fix mobile controllers issues
- Add price option to In-Game Product

## 1.16
- Fix disconnect errors
- Fix invalid random attack animation
- Remove unused files 

## 1.15
- Add support idle animation changes by equip weapon

## 1.14
- Add kill notify messages
- Fix battle royale mode not work on Master Server Framework integration
- Fix jump input not work sometime

## 1.12
- Improve performance by reduce amount of attack messages
- Add is hidding in character entity, use it to set character hide state

## 1.11
- Fix damage not calculate on dedicate server

## 1.10
- Add battle royale game mode

## 1.09
- Add chat and emoticon

## 1.08
- Add reward currency when kill other characters

## 1.07
- Add deathmatch game mode

## 1.06
- Make UIGameplay instantiating by Game rules
- Make character can jump (Try space bar butt)
- Add command line settings for dedication
- Can set to show mobile joystick or not via GameInstance (Home scene)
- Score/Kill/Dead reset immediately when dies

## 1.38
- Fix random animation bugs
- Add network game framework to prepare future game modes
- Add more secure monetization save

## 1.05
- Fix save bugs
- Fix random animation bugs
- Make character gravity supports so characters can walks on slopes
- Add trap entity
- Add network game framework to prepare future game modes
- Add more secure monetization save
