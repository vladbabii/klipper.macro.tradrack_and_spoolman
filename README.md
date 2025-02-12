# Klipper Macro Configuration for Trad Rack, Spoolman and Mainsail

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
