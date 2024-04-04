# AnimationClipUpdater

Unity custom editor window to update exported animation clips from their source FBX without losing modifications.

Update animations easily without losing events or settings.

When creating animations for a game, there is most often several iterations before the animations are finished.
Whenever new animations are made and exported to and FBX then imported in Unity, the engine will automatically update the animations that have the same names.
This is great when using the animations as is, or with minimal change in settings that you set within the model importer.  
It is a lot less nice when you need better customisation. The go-to solution is to duplicate the animations so that they can be modified more extensively or precisely.
Events are particularly finicky to work with in the model importer for example (they were the primary motive in my case).

This script aims to solve that issue:

- Duplicate the animation clips and put them in a [Resources folder](https://docs.unity3d.com/ScriptReference/Resources.html)
- Create the animation events, set the loop time, etc, just as usual
- Update the source FBX's animations with the new versions of the animations
- Instead of re-duplicating and transferring all the settings, go to `Window > Animation > Animation Clips Updater`
- Fill in the Source FBX
- Fill in the path to the animation clips from their Resources folder (e.g. if the clips are in `Assets/Character/Resources/Clips`, put `Clips`, cf. [Resource folders](https://docs.unity3d.com/ScriptReference/Resources.html))
- Check the animation settings that you modified and want to keep (e.g. loopTime, mirror, etc)
- Click Update

Using this script, you will also avoid losing any reference to the clips (e.g. in animators).

I hope this is helpful, if you have any suggestions, complaints or feel like something isn't right about this script, contact me at primarter@gmail.com.