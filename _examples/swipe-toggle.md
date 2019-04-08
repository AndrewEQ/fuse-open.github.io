---
layout: example
title: Custom toggle control
synopsis: How you can use SwipeGesture to build a custom toggle control
date: 2016-12-28 00:00:00
tags:
- Custom control
- Swipe gesture
uxConcepts:
- SwipeGesture
- SwipingAnimation
preview-image: swipe-toggle.png
preview-video: hsYVqseWGT8
---
In this example, we make a custom toggle control using `SwipeGesture` and `SwipingAnimation`.

```
<App>
	<Panel ux:Class="MyToggle" Width="80" Height="34" PrimaryColor="#9b59b6" SecondaryColor="#fff">
		<float4 ux:Property="PrimaryColor" />
		<float4 ux:Property="SecondaryColor" />
		<bool ux:Property="IsActive" />
		
		<SwipeGesture ux:Name="swipe" Length="46" Direction="Right" Type="Active" IsActive="{Property IsActive}" />
		<SwipingAnimation Source="swipe">
			<Move Target="handle" X="46" />
			<Change handle.Color="{ReadProperty SecondaryColor}" />
			<Change background.Color="{ReadProperty PrimaryColor}" />
		</SwipingAnimation>
		
		<Clicked>
			<ToggleSwipeActive Target="swipe" />
		</Clicked>
		
		<Rectangle ux:Name="handle" Width="28" Margin="3" Alignment="Left" Color="{ReadProperty PrimaryColor}" CornerRadius="2">
			<Shadow Size="1" Distance="1" Color="#0004" />
		</Rectangle>
		
		<Rectangle ux:Name="background" Layer="Background" Color="{ReadProperty SecondaryColor}" CornerRadius="4" />
	</Panel>
	
	<MyToggle ux:Name="toggle" />
	<WhileTrue Value="{ReadProperty toggle.IsActive}">
		<Change background.Color="#ecf0f1" Duration="0.2" />
	</WhileTrue>
	
	<Rectangle ux:Name="background" Color="#6A397F" />
</App>
```
