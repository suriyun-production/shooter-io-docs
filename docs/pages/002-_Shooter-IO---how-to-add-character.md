# How to add character

Things you have to do to add new character for this template are:

*   Prepare **Character Model**
*   Create and set **Character Data**
*   Add created **Character Data** to **Game Instance**

Okay, Let’s start

## Prepare Character Model

First, prepare character model. You may create empty scene then drag your character model into the scene to manage it, In your character model add **CharacterModel** component

![](../images/0-utCVqdnZrF3PEB9.png)

Then explore into character model children drag game object which you want to instantiate model to each container in **CharacterModel** component

![](../images/0_9s1m20R85lAdTYp.png)

Then make it as a prefab.

## Create and set Character Data

Next, you have to create **CharacterData**, right click on anywhere in Project tab choose **Create -> ScriptableObject**

![](../images/0cxYI-4mzQOpDNfEX.png)

In **Create ScriptableObject** dialog choose **CharacterData**

![](../images/0p3E3Lk7LJ6FwNzrw.png)

Then set it name as you wish but it must be unique for example I set it as **Character001**

Then in character data set **Character Model** to character model prefab that you have created

![](../images/0Mz81nBGddeP-IjhW.png)

## Add created Character Data to Game Instance

Then open **Home** scene add character data to **GameInstance**

![](../images/0KdyG58ww3Olc97lv.png)

![](../images/01A-gPvvmgfk8-KgE.png)