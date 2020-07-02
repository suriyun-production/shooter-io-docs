# How to add weapon item

Things you have to do to add new weapon item for this template are:

*   Prepare **Weapon Model**
*   Prepare **Damage Entity**
*   Create and set **Weapon Data**
*   Add created **Weapon Data** to **Game Instance**

Okay, Let’s start

## Prepare Weapon Model

First, prepare right hand / left hand weapon and/or shield models. You may create empty scene then drag your weapon model into the scene to manage them, Then make them as prefab

Next, you may like to create new Damage Entity, it’s a object which will take damage to character when it’s collided to the character

To create it you may prepare a model such as bullet model then add Damage Entity component, this component contains following configs

*   **Spawn Effect Prefab** is effect which will be played when spawn
*   **Explode Effect Prefab** is effect which will be played when it hit something or when it’s stayed over **Life Time**
*   **Hit Effect Prefab** is effect which will be played at characters that take damage
*   **Radius** is radius to taking damage to characters
*   **Life Time** is duration before destroying after spawned
*   **Spawn Forward Offset** is spawn forward offset from attacker character
*   **Speed** is movement speed
*   **Relate To Attacker** if this is true it position will be relates to attacker character

Then you have to add any collider to make it able to collided by characters

And then make it as prefab you will use it to set in **WeaponData**

Next, you have to create **WeaponData**, right click on anywhere in Project tab choose **Create -> ScriptableObject**

![](../images/0m1f5AtAezRWF7vJW.png)

In **Create ScriptableObject** dialog choose **WeaponData**

![](../images/0rkpsMQnC2xFZxlAI.png)

Then in weapon data set weapon model prefabs that you have created to each type of position

![](../images/1F0r4Fxs5bUP0u0K0Wm8Pbg.png)

Another​ ​parameter​ ​there​ ​are

*   **Stats**​ ​​is​ ​an​ ​stats​ ​which​ ​will​ ​adds​ ​when​ ​character​ ​equip this​ ​weapon
*   **Attack​ ​Animations​​** ​is​ ​an​ ​animation​ ​data​ ​to​ ​play​ ​when attacking​ ​character,​ ​each​ ​attack​ ​animation​ ​contains   
    \- **Action​ ​Id**​​ ​is​ ​ID​ ​for​ ​attack​ ​animation​ ​that​ ​you​ ​can set​ ​condition​ ​in​ ​​**CharacterAnimator**​ ​​(Animator Controller)​ ​to​ ​play​ ​that​ ​attack​ ​animation  
    \- **Animation​ ​Duration**​​ ​is​ ​total​ ​duration​ ​to​ ​play​ ​attack animation  
    \- **Launch​ ​Duration**​​ ​is​ ​duration​ ​to​ ​launch​ ​attack​ ​damage, this​ ​value​ ​must​ ​less​ ​than​ ​or​ ​equal​ ​to​ ​Animation Duration
*   **Damage​ ​Prefab**​​ ​is​ ​prefab​ ​of​ ​​**DamageEntity**​ ​​that​ ​will​ ​be launched​ ​when​ ​attack
*   **Damage**​ ​​is​ ​damage​ ​which​ ​will​ ​be​ ​applied​ ​when​ ​hit​ ​character
*   **Equip​ ​Position**​​ ​is​ ​position​ ​for​ ​equipment,​ ​for​ ​example​ ​0: is​ ​primary​ ​gun,​ ​1:​ ​secondary​ ​gun,​ ​2:​ ​knife
*   **Reload​ ​One​ ​Ammo​ ​At​ ​A​ ​Time**​​ ​if​ ​this​ ​is​ ​​True​ ​​when​ ​reload ammo​ ​it​ ​will​ ​reload​ ​one​ ​ammo​ ​at​ ​a​ ​time​ ​like​ ​as​ ​Shotgun
*   **Reload​ ​Duration**​​ ​is​ ​a​ ​duration​ ​to​ ​reload​ ​ammo
*   **Unlimit​ ​Ammo**​​ ​if​ ​this​ ​is​ ​True​ ​ammo​ ​will​ ​be​ ​unlimited
*   **Max​ ​Ammo**​​ ​is​ ​max​ ​amount​ ​of​ ​ammo
*   **Max​ ​Reserve​ ​Ammo​​** ​is​ ​max​ ​amount​ ​of​ ​reserve​ ​ammo
*   **Spread​​** ​is​ ​amount​ ​of​ ​bullet​ ​that​ ​will​ ​be​ ​spread​ ​per​ ​shot
*   **Stagger​ ​X**,​ ​**Stagger​ ​Y​​** ​angles​ ​in​ ​each​ ​axis​ ​that​ ​will​ ​add​ ​to bullet​ ​when​ ​shooting​ ​to​ ​make​ ​gun​ ​shot​ ​look​ ​stagger
*   **Attack​ ​Fx**​​ ​is​ ​audio​ ​clip​ ​which​ ​will​ ​plays​ ​when​ ​attack
*   **Clip​ ​Out​ ​Fx**​​ ​is​ ​audio​ ​clip​ ​which​ ​will​ ​plays​ ​before​ ​start reload
*   **Clip​ ​In​ ​Fx**​​ ​is​ ​audio​ ​clip​ ​which​ ​will​ ​plays​ ​after​ ​reloaded
*   **Empty​ ​Fx**​​ ​is​ ​audio​ ​clip​ ​which​ ​will​ ​plays​ ​when​ ​attacking with​ ​empty​ ​ammo

## Add created Weapon Data to Game Instance

Then open **Home** scene add weapon data to **GameInstance**

![](../images/0MH9-JTP5xqHwZ_Qz.png)

![](../images/0t1ffuSuVIbGhyOMp.png)