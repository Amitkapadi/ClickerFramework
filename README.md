# ClickerFramework

Framework currently only supports one primary Resource. Extra currencies might be added later via a new system.
I've included a demo Unity Scene (TestScene) with most of these things hooked up and working in a very simple way.

--- Core files ---
o GameManager.cs - A singleton. Tracks the resource and has helpful initialization and helper functions.

--- UI and Display Helpers ---
o DisplayResource - Use on a UI Text object (or linked to one) to display the current amount of Resource
o DisplayMultiplier - Use on a UI Text object (or linked to one) to display either the total Tick multiplier or Click multiplier

--- Stuff that goes on buttons ---
o Buyable.cs - Put on a button (send DoPurchase) to make it a buyable. Disables button if you can't afford it. Works with following scripts:
o ClickForResource.cs - Use this on a button (send OnClick) if you want to click it to generate Resource. Works fine alongside Generators.
o MultiplyResource - Use this on a button (send OnClick) to multiply the total Resource count by n when clicked.
o RegisterMultiplier - Use this on a button (send OnClick) to add to the total global Tick or Click multiplier when clicked.
o Generator.cs - Generates Resource every n seconds (every tick) - basically a building. Can have many of these.  Put on a button with a Buyable script if you want the ability to to be purchaseable/upgradeable.


