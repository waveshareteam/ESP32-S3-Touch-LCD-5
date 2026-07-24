| Supported Targets | ESP32-S3 |
| ----------------- | -------- |

# LVGL9 Adapter Demo

This example targets the Waveshare `ESP32-S3-Touch-LCD-5` board and runs the official
`lv_demo_widgets()` demo with:

- `LVGL 9`
- `espressif/esp_lvgl_adapter`
- RGB panel output
- GT911 touch input

## Requirements

- ESP-IDF `>= 5.5`
- Internet access on the first build so the component manager can download dependencies

## Build

```bash
idf.py set-target esp32s3
idf.py build
idf.py -p PORT flash monitor
```

## Notes

- The example keeps the existing board-level RGB and CH422G control sequence, and only replaces the LVGL porting layer with `esp_lvgl_adapter`.
- Touch is enabled by default. If your panel variant has no touch, set `EXAMPLE_USE_TOUCH` to `0` in `main/waveshare_rgb_lcd_port.h`.
