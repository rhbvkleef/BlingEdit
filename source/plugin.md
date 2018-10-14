# Writing your own plugin

A plugin is a datapack responsible for performing an edit operation in the selected region. To write a plugin, you must
include the following:
* Every tick, check if any players have their disp_plugins score set to 1. If they do, send them a light_purple tellraw
  message with a clickable element that will run a function that implements the plugin’s operation. I suggest calling
  the function run.
  * For example:
    ```
    execute as @e[type=minecraft:player] run execute if score @s disp_plugins matches 1.. run tellraw @s ["",{"text":"[Vegetate]","clickEvent":{"action":"run_command","value":"/function blingedit_vegetate:run"},"color":"light_purple"}]
    ```
* At the beginning of your plugin’s run function, use:
  ```
  function blingedit:plugin_can_run
  ```
  Then check if player Global has a plugin_can_run score of 1. If it does, you’re free to perform the operation. If not,
  it could mean the player hasn’t selected a region, or that they aren’t in the right state to run a plugin.
* `plugin_can_run` also sets several scores for player Global. The objectives box_xmin, box_ymin, box_zmin, box_xmax,
  box_ymax and box_zmax define the minimum and maximum bounds of the region’s bounding box. Use those coordinates
  however you like.
* At the end of your run function, use
  ```
  gamerule sendCommandFeedback false
  ```
* to disable the text would be displayed by clicking the tellraw link. BlingEdit will automatically re-enable the
  gamerule if it was previously enabled.
