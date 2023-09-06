[latest-release]: https://github.com/anominy/overlap/releases/latest

## Movement Overlap Detection Config

### Install
1. Download the latest version from the [releases][latest-release] page.
2. Extract the `/movement/` folder to your `/cfg/` game directory.

#### Overview
```shell
Tree .\movement\ /F
```
```text
C:\PROGRAM FILES (X86)\STEAM\STEAMAPPS\COMMON\COUNTER-STRIKE GLOBAL OFFENSIVE\CSGO\CFG\MOVEMENT
└───overlap
        def.cfg
```


### Setup
1. Open the `/cfg/autoexec.cfg` file.
    * If you don't have one, create then.
2. Append w/ `exec movement/overlap/def.cfg` command.

#### Overview
```shell
.\autoexec.cfg
```
```text
// For example, if your existing autoexec config looks like this.
// + ------------------------------------------------------------
// | Put `exec movement/overlap/def.cfg` at the end of this file 
// |  to include a movement overlap definition config.



// === [ BEGIN ~ AUTOEXEC.CFG ] ===

fps_max 0
cl_threaded_bone_setup 1
cl_interpolate 0
cl_interp_ratio 0
cl_interp 0
cl_spec_show_bindings 0
cl_server_graphic1_enable 0
cl_server_graphic2_enable 0
cl_sanitize_muted_players 0

alias vm "viewmodel_fov 68; viewmodel_offset_x 2; viewmodel_offset_y 2; viewmodel_offset_z -2; cl_bob_lower_amt 8; cl_bobamt_lat 0.1; cl_bobamt_vert 0.1"

alias i0 "cl_interpolate 0; cl_interp_ratio 0; cl_interp 0"
alias i1 "cl_interpolate 1; cl_interp_ratio 2; cl_interp 1"

// === [ END ~ AUTOEXEC.CFG ] ===



// === [ BEGIN ~ SETUP ] ===

exec movement/overlap/def.cfg  // Includes the movement overlap definition config.

// === [ END ~ SETUP ] ===
```


### Callbacks
* `on_overlap_fw`
  * Executed when the <kbd>A</kbd> & <kbd>D</kbd> keys are pressed simultaneously.
* `on_overlap_sw`
  * Executed when the <kbd>W</kbd> & <kbd>S</kbd> keys are pressed simultaneously.
* `on_overlap_wd`
  * Executed when the <kbd>W</kbd> & <kbd>D</kbd> keys are pressed simultaneously.
* `on_overlap_sd`
  * Executed when the <kbd>S</kbd> & <kbd>D</kbd> keys are pressed simultaneously.
* `on_overlap_wa`
  * Executed when the <kbd>W</kbd> & <kbd>A</kbd> keys are pressed simultaneously.
* `on_overlap_sa`
  * Executed when the <kbd>S</kbd> & <kbd>A</kbd> keys are pressed simultaneously.


### License
Licensed under the [CC BY-NC-ND 4.0 license](./LICENSE).
