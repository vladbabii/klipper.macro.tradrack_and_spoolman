# Klipper Macro Configuration for Trad Rack, Spoolman and Mainsail

These settings are on top of installing spoolmain via kiauh!

This is also work-in-progress so please double-check everything before using.

## Mainsail integration effects

Per spool spoolman options

![mainsail tools](/img/mainsail_1.png)

Extruder colors

![mainsail tools](/img/mainsail_2.png)

Values saved across restarts as saved variables

![mainsail tools](/img/variables_1.png)

## Macros
Please see the cfg files in this repo.

## Trad Rack
```
[trad_rack]
register_toolchange_commands: False

post_load_gcode:
  SAVE_GCODE_STATE NAME=POST_LOAD_state
   ...
   SPOOLMAN_TOOL_SYNC
   ...
   RESTORE_GCODE_STATE NAME=POST_LOAD_state

post_unload_gcode:
  SAVE_GCODE_STATE NAME=POST_UNLOAD_state
  ...
  SPOOLMAN_TOOL_SYNC
  ...
  RESTORE_GCODE_STATE NAME=POST_UNLOAD_state
```
