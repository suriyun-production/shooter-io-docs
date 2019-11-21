* * *

To enable Unity Ads you have to import the Monetization package ([Here](https://assetstore.unity.com/packages/add-ons/services/unity-monetization-3-3-0-66123)) 

Then in Services, (Find from menu: Window → General → Services) then turn on ADS and `Enable built-in Ads extension`

![](../images/ads-01.png)

Then in the `Home` scene, there is `GameInstance` game object in that game object you will see attached `Monetization Manager` component you have to set its `Android Game Id` and `iOS Game Id` 

![](../images/ads-02.png)

You can find it in `Unity Ads Dashboard` ([https://dashboard.unityads.unity3d.com](https://dashboard.unityads.unity3d.com)). in the Dashboard scroll down, you will see project list, select you project you will see game Id

![](../images/ads-03.png)

Then you have to set Ads placement, in the dashboard select project then select platform, in selected platform page you will see Ads placements list, each entry you will see `Placement Id` use them to set `Reward Video Placement` in the `Monetization Manager` component and `Watch Ads Respawn Placement` in the `Game Instance` component

![](../images/ads-04.png)

An placement Id, You can create new placement via menu ADD NEW PLACEMENT

You can set how many currency player will receive after watched the Ads, in `Monetization Manager` component -> `Ads Reward Currency`

You can set time to let player to watch Ads to respawn without reset stats in `Battle` scene -> `GameplayManager` \-> `Watch Ads Respawn Available`