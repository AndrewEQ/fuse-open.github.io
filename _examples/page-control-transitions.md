---
layout: example
title: Custom transitions
synopsis: Creating custom page transitions using Entering- and ExitingAnimation
date: 2016-12-15 00:00:00
tags:
- Navigation
- Custom control
uxConcepts:
- PageControl
- EnteringAnimation
- ExitingAnimation
- Move
- Scale
- Change
preview-image: page-control-transitions.png
preview-video: page-control-transitions.mp4
---
This example shows how you can make your own transitions for pages within a `PageControl`.

The trick is setting `Transition="None"` on the `PageControl`, which removes the default page animations.
This lets you add your own `EnteringAnimation` and `ExitingAnimation` to each page, which controls how they animate in and out.

```
<App Background="#222">
	<Page ux:Class="MyPage">
		<EnteringAnimation>
			<Move X="-1" RelativeTo="ParentSize" />
		</EnteringAnimation>
		<ExitingAnimation>
			<Scale Factor="0.75" />
			<Change this.Opacity="0.7" />
		</ExitingAnimation>
	</Page>
	
	<PageControl Transition="None">
		<NavigationMotion Overflow="Elastic" />
		<MyPage Color="#D32F2F" />
		<MyPage Color="#8E24AA" />
		<MyPage Color="#3F51B5" />
	</PageControl>
</App>
```
