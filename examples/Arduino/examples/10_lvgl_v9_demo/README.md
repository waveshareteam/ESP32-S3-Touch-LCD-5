# LVGL v9 Demo

This example is the Arduino-side counterpart of the ESP-IDF `09_lvgl_v9_demo`.

It runs the built-in `lv_demo_widgets()` demo with a minimal LVGL v9 display/touch port.

## Required LVGL Layout

Use the official Arduino layout in the global Arduino library folder:

- `C:\Users\ag\Documents\Arduino\libraries\lvgl\src\demos`
- `C:\Users\ag\Documents\Arduino\libraries\lvgl\src\examples`
- `C:\Users\ag\Documents\Arduino\libraries\lv_conf.h`

Also disable `lv_blend_helium.S` for ESP32 Xtensa builds.
You can copy the workspace file `examples/Arduino/lv_conf.h` to the global `Arduino\libraries` folder.

## Notes

- This sketch now includes `#include <demos/lv_demos.h>` directly.
- Do not keep a local `demos/` copy inside this example folder.
- Keep this example in an independent folder so it does not affect the existing `09_lvgl_Porting` example.
