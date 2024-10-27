Welcome to the Weave tutorial section! Here, you'll learn how to build great
interfaces with Weave, even if you're a complete newcomer to the library.


## What You Need To Know

These tutorials assume:

- You're comfortable with Roblox and the Luau scripting language.
	- These tutorials aren't an introduction to scripting! If you'd like to
	  learn, check out the [Roblox DevHub](https://developer.roblox.com/).
- You're familiar with how UI works on Roblox.
    - You don't have to be a designer - knowing about UI instances, events
	and data types like `UDim2` and `Color3` will be good enough.

Of course, based on your existing knowledge, you may find some tutorials easier
or harder. Weave's built to be easy to learn, but it may still take a bit of
time to absorb some concepts, so don't be discouraged :slightly_smiling_face:

-----

## Installing Weave

Weave is distributed as a single module script. Before starting, you'll need
to add this module script to your game. Here's how:

### If you edit scripts in Roblox Studio...

Click the 'Assets' dropdown to view the downloadable files:


Now, click on the `Weave.rbxm` file to download it. This contains the module as
a Roblox model:

![The Assets dropdown opened to reveal downloads, with Weave.rbxm highlighted.](index/Github-Releases-Guide-2-Light.png#only-light)
![The Assets dropdown opened to reveal downloads, with Weave.rbxm highlighted.](index/Github-Releases-Guide-2-Dark.png#only-dark)

Head into Roblox Studio to import the model; if you're just following the
tutorials, an empty baseplate will do.

Right-click on `ReplicatedStorage`, and select 'Insert from File':

![ReplicatedStorage is right-clicked, showing a context menu of items. Insert from File is highlighted.](index/Github-Releases-Guide-3-Light.png#only-light)
![ReplicatedStorage is right-clicked, showing a context menu of items. Insert from File is highlighted.](index/Github-Releases-Guide-3-Dark.png#only-dark)

Select the `Weave.rbxm` file you just downloaded. You should see the module
script appear in `ReplicatedStorage` - you're ready to go!

### If you edit scripts externally... (advanced)

If you use an external editor to write scripts, and synchronise them into Roblox
using a plugin, you can use these alternate steps instead:

??? example "Steps (click to expand)"
	1. Head over to Weave's 'Releases' page.
	2. Under 'Assets', download `Source code (zip)`. Inside is a copy
	of the Weave GitHub repository.
	3. Inside the zip, copy the `src` folder - it may be inside another folder.
	4. Paste `src` into your local project, preferably in your `shared` folder
	if you have one.
	5. Rename the folder from `src` to `Weave`.

	Once everything is set up, you should see Weave appear in Studio when you
	next synchronise your project.

-----

## Setting Up A Test Script

Now that you've installed Weave, you can set up a local script for testing.
Here's how:

1. Create a `LocalScript` in `StarterGui` or `StarterPlayerScripts`.
2. Remove the default code, and paste the following code in:
```Lua linenums="1"
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local Weave = require(ReplicatedStorage.Weave)
```
3. Press 'Play' - if there are no errors, everything was set up correctly!

??? fail "My script didn't work! (click to expand)"
	```
	Weave is not a valid member of ReplicatedStorage "ReplicatedStorage"
	```

	If you're seeing this error, then your script can't find Weave.

	This code assumes you've installed Weave into `ReplicatedStorage`. If
	you've installed Weave elsewhere, you'll need to tweak the `require()` on
	line 2 to point to the correct location.

	If line 2 looks like it points to the correct location, refer back to
	[the previous section](#installing-Weave) and double-check you've set
	everything up properly. Make sure you have a `ModuleScript` inside
	`ReplicatedStorage` called "Weave".

-----

## Where To Get Help

Weave is built to be easy to use, and we want these tutorials to be as useful
and comprehensive as possible. However, maybe you're stuck on a cursed issue
and really need some help; or perhaps you're looking to get a better overall
understanding of Weave!

Whatever you're looking for, here are some resources for you to get help: