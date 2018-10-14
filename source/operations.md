# Operations

Once you’ve selected a region, there are several editing operations you can perform. These operations will be listed in
chat, simply click on the operation you wish to perform.

## Delete

This simply clears all blocks in the region.

## Fill

This fills the region entirely with a single block. Select the **`[Fill]`** operation, then use
```
/setblock ~ ~ ~ <block>
``` 
to select the block to use.

## Replace

This finds all blocks of a certain type and replaces them with another type of block. Select the **`[Replace]`**
operation. Then use
```
/setblock ~ ~ ~ <block>
```
to select the block to replace, use:
```
/setblock ~ ~ ~ <block>
```
again to select the block to replace with.


## Clone

This will clone all blocks in the selected region to another destination. There are several methods and options that can
be used when doing this. When you select the **`[Clone]`** operation, the option to enable/disable the cloning of air
blocks will appear in chat as well. A green destination region will appear, and it will be the same size as the red
source region.

### Moving the destination region

When the green destination region appears, you’ll be moving it by default. Click to set its location. Note that you can
change your cursor type as described earlier in this manual. To move it with the cursor again, left click to attack any
of the green anchor points. You can also use the Up/Down/Left/Right/Forward/Backward buttons to move the destination
region by a single block in any of those directions. It’s not possible to resize the destination region, since its must
match the source region.

### Confirm Clone

This will clone all blocks from the source region to the destination region, and then select the destination region for
further editing.

### Clone & Repeat

This will clone all blocks from the source region to the destination, and then move both the source and destination
region so that the clone operation can be repeated. By clicking this several times, you can stack many copies of the
same structure next to each other at any offset you’d like.

### Clone Brush

In Clone Brush mode, simply left clicking will paste the region at the cursor. Remember that you can change cursor modes
as described earlier in this manual by pressing the “drop item” key. This can be used to quickly place many copies of
the source structure in a point-and-click fashion.

### Cancel

Use this to exit all clone operations.

## Randomize

This set of operations is used to place blocks drawn from a random pool of blocks. Before randomizing any blocks, a
Random Block Pool must be selected.

### Store Selected Region as Random Block Pool

This will store the region you have selected. All blocks in this region, including air, form the Random Block Pool. When
further randomization operations are performed, a random set of coordinates from within this region will be selected,
and the block at those coordinates will be used. Note that you can change blocks in this region after selecting the
region as the Random Block Pool, and that the region needs to be loaded when perform other randomization operations.

### Fill Selected Region from Random Block Pool

Every block in the selected region will obtain a random block from the Random Block Pool.

### Replace in Selected Region from Random Block Pool

When you select this operation, you’ll be asked which type of block you want to replace. Use
```
/setblock ~ ~ ~ <block>
``` 
to select the block. Each instance of that kind of block within the selected region will be replaced by a block from the
Random Block Pool.

## Plugins

Selecting this operation will display a list of installed plugins. To install a plugin, download the datapack and put it
in the `datapacks` folder in your save directory.

### My Plugins
[Vegetate](https://drive.google.com/file/d/1LeT1-Fx70Op92UnSJOjhqrpebc5BzSQd/view?usp=sharing) - Any empty blocks in the
selected region which are on top of a grass block may receive random vegetation.