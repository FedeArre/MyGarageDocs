# PaintingSystem

Static class that contains useful methods about the painting system.

# Methods <!-- {docsify-ignore} -->

Method | Description
----- | -----------
GetBodymatMaterial | Returns a material reference using the double sided shader
GetRustMaterial | Returns a material reference using L2 shader
GetDirtMaterial | Returns a material reference using the default shader
GetChromeMaterial | Returns the chrome material from the game (double-sided variant)
SetMaterialsForObject | Sets the proper materials for painting on a part

# Types enum <!-- {docsify-ignore} -->

Contains a list of available painting types on the game.

Type |
---- |
FullPaintingSupport
OnlyPaint
OnlyPaintAndRust
OnlyDirt
OnlyPaintAndDirt

# Paint resolution enum <!-- {docsify-ignore} -->

Contains the list of available resolutions for paint

Resolution |
---------- |
Low
Medium
High