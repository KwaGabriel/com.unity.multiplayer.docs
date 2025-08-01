---
id: about
title: About Multiplayer Play Mode
description: Overview of Multiplayer Play Mode
---

Use Multiplayer Play Mode to test multiplayer functionality within the Unity Editor. You can simulate up to four Players (the main Editor Player and three Virtual Players) at the same time, on the same development device while using the same source assets on disk. Multiplayer Play Mode can help you create multiplayer development workflows that reduce project build times, run it locally, and test the server-client relationship.

## Compatibility

Multiplayer Play Mode version 1.5.0 is compatible with the following: 

* Unity Editor versions 6000.1.0b1 or later.
* Windows and MacOS platforms.
* Experimental Android support for Unity Editor version 6.1.

## Multiplayer Play Mode terminology

The following have specific meaning in relation to Multiplayer Play Mode:

* main Editor Player: The original instance of the project in the Unity Editor. This is the only instance with full authoring capabilities.
* Virtual Players: Simulated Players created with Multiplayer Play Mode. These Players open in a separate window with limited authoring capabilities when you enter [Play mode](https://docs.unity3d.com/Manual/GameView.html).
* Players: All Player instances, including the main Editor Player and all Virtual Players.

## Limitations

Multiplayer Play Mode has some inherent technical limitations, specifically around [scale](#scale) and [authoring](#authoring).

### Scale

The Unity Editor and Virtual Players require a lot of system resources, so you shouldn't use Multiplayer Play Mode at scale. Multiplayer Play Mode is designed for small-scale, local testing environments that can only support up to four total Players (the main Editor Player and three Virtual Players).

### Authoring
You can't create or change the properties of GameObjects in a Virtual Player. Instead, use the main Editor Player to make changes and a Virtual Player to test multiplayer functionality. Any changes you make in Play Mode in the main Editor Player reset when you exit Play Mode.
:::note
You can't access any main Editor Player functionality from Virtual Players.
:::

## Performance impact

To reduce the demand on system resources caused by each Virtual Player instance, Multiplayer Play Mode shares specific resources, such as the artifact database and imports between the main Editor Player and each Virtual Player.
