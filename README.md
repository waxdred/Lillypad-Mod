# LillyPad Pro Custom Keyboard

A premium 58-key split ergonomic mechanical keyboard based on the Lily58 design. This project features a 6×4+4 column-staggered layout with dual MX/Choc switch support, nice!nano wireless controllers, nice!view displays, and premium hotswap sockets.

## 🌟 Features

- **Split Ergonomic Design**: 58-key column-staggered layout (6×4+4)
- **Dual Switch Support**: MX/Choc hybrid hotswap sockets (MXCHOC-HOTSWAP_WAX footprint)
- **nice!nano Controllers**: Wireless-ready with ZMK firmware support
- **nice!view Displays**: Premium e-paper displays for enhanced functionality
- **Wireless Support**: Compatible with nice!nano controllers
- **QMK/ZMK Firmware**: Full programmability with modern firmware
- **3D Printed Case**: Custom STL files included for case printing

## 📁 Project Structure

```
├── stl/                    # 3D printable case files
├── EasyEDA/               # PCB design files
│   └── gerber/           # Gerber files for PCB manufacturing
└── README.md             # This file
```

## 🛠 Bill of Materials (BOM)

Based on the official LillyPad Pro BOM:

### Core Electronics

| Component             | Quantity | Part Number/Description  | Footprint                  | Designator           |
| --------------------- | -------- | ------------------------ | -------------------------- | -------------------- |
| nice!nano Controllers | 2        | Wireless microcontroller | NICE!NANO_HOTSWAP          | PROMICROL, PROMICROR |
| nice!view Displays    | 2        | E-paper display          | NICE!VIEW - BASIC          | EPAPER, EPAPER_R     |
| Battery Connectors    | 2        | JST B2B-PH-K-S           | B2B-PH-K-S                 | BAT, BAT_R           |
| Reset Buttons         | 2        | Tactile switch           | SW-SMD_L8.0-W3.5_3-6-3.5MM | RST, RST_R           |
| Power Switches        | 2        | SPST SMD switch          | SWITCH-SPST-SMD-A          | S1, S2               |

### Switches & Hotswap

| Component       | Quantity | Description            | Notes                                |
| --------------- | -------- | ---------------------- | ------------------------------------ |
| Hotswap Sockets | 58       | MX/Choc hybrid sockets | MXCHOC-HOTSWAP_WAX footprint         |
| Switches        | 58       | MX or Choc v1 switches | Your choice of tactile/linear/clicky |
| Keycaps         | 58       | MX or Choc compatible  | Profile of your choice               |

### Additional Components

| Component      | Quantity | Description     | Source Link            |
| -------------- | -------- | --------------- | ---------------------- |
| LiPo Batteries | 2        | 3.7V 110-500mAh | For wireless operation |

### Hardware & Fasteners

| Component        | Quantity | Description          | Source Link                                                        |
| ---------------- | -------- | -------------------- | ------------------------------------------------------------------ |
| M2.5×6mm Screws  | 18       | Phillips head screws | [AliExpress](https://fr.aliexpress.com/item/1005005070119421.html) |
| M2.5×10mm Screws | 4        | Phillips head screws | [AliExpress](https://fr.aliexpress.com/item/1005004657582673.html) |
| M2.5 Standoffs   | Various  | Brass standoffs      | Check case requirements                                            |
| Rubber Feet      | 8-12     | Self-adhesive feet   | For case bottom                                                    |

## 🔧 Assembly Instructions

### 1. PCB Assembly (Pre-assembled Option Available)

1. **Controllers** - Solder nice!nano controllers to hotswap sockets
2. **Displays** - Connect nice!view displays (no soldering required)
3. **Battery connectors** - Solder JST battery connectors
4. **Reset/Power switches** - Install tactile buttons and power switches
5. **Final check** - Verify all connections before case assembly

### 2. Case Assembly

1. **3D print case parts** using provided STL files
2. **Insert threaded inserts** or prepare screw holes
3. **Install standoffs** using M2.5 screws
4. **Mount PCB** to case with appropriate screws
5. **Attach bottom plate** and rubber feet

### 3. Final Assembly

1. **Install switches** into MX/Choc hybrid hotswap sockets
2. **Mount keycaps** on switches
3. **Connect batteries** to JST connectors for wireless operation
4. **Install nice!view displays** (tool-free installation)
5. **Flash ZMK firmware** (see firmware section)
6. **Pair keyboard halves** wirelessly

## 💾 Firmware

This keyboard is designed for ZMK firmware with nice!nano controllers:

### ZMK (Primary - Wireless)

- **Controller**: nice!nano (required)
- **Setup**: Use [nickcoutsos.github.io/keymap-editor](https://nickcoutsos.github.io/keymap-editor/) for easy configuration
- **Features**:
  - Wireless operation with BLE
  - Low power consumption
  - nice!view display support
  - Vial-compatible keymap editing
  - Battery level monitoring

### Backup Wired Mode

- **Connection**: TRRS cable between halves
- **Compatibility**: Maintains ZMK firmware
- **Use case**: When batteries are low or troubleshooting

## ⚙️ Configuration

### Easy Setup with Keymap Editor

1. Visit [nickcoutsos.github.io/keymap-editor](https://nickcoutsos.github.io/keymap-editor/)
2. Load your ZMK config repository
3. Visually edit your keymap
4. Commit changes to automatically build firmware

### Manual Configuration

For advanced users, you can manually edit the ZMK or QMK configuration files to customize:

- Key mappings and layers
- RGB lighting patterns
- OLED display content
- Encoder behavior
- Wireless settings

## 📐 PCB Specifications

- **Layout**: 58 keys (6×4+4 per half)
- **Switch Support**: MX/Choc hybrid hotswap (MXCHOC-HOTSWAP_WAX)
- **Controllers**: nice!nano with hotswap sockets
- **Displays**: nice!view e-paper displays
- **Connectivity**: Wireless BLE primary, TRRS backup
- **Power**: JST battery connectors, power switches
- **Dimensions**: Standard Lily58 compatible layout

## 🖨️ 3D Printing

### Print Settings

- **Layer Height**: 0.2mm
- **Infill**: 20-30%
- **Support**: Required for overhangs
- **Material**: PLA, PETG, or ABS

### Files Included

- Top case (left & right)
- Bottom plate (left & right)
- OLED cover (optional)

## 🛡️ Troubleshooting

### Common Issues

1. **Switches not registering**: Check hotswap socket connections
2. **Controller not detected**: Verify USB connection and try reset button
3. **nice!view not working**: Check display connector seating
4. **Wireless connectivity issues**: Ensure battery is connected and charged
5. **Battery life concerns**: Check power switch position and ZMK power settings

### Support Resources

- QMK Documentation: [docs.qmk.fm](https://docs.qmk.fm)
- ZMK Documentation: [zmk.dev](https://zmk.dev)
- Community Discord servers for real-time help

## 📚 Additional Resources

- **Build Guide**: Detailed step-by-step instructions
- **Firmware Examples**: Pre-configured layouts
- **Case Modifications**: Alternative mounting options
- **Switch Recommendations**: Compatibility guide

## 🤝 Contributing

Contributions are welcome! Please feel free to:

- Submit bug reports or feature requests
- Share your build photos and modifications
- Contribute to documentation improvements
- Suggest PCB or case enhancements

## 📄 License

This project is open source. Please refer to individual component licenses:

- PCB design files: [Check EasyEDA folder]
- Case files: [Check STL folder]
- Firmware: Respective firmware licenses (QMK/ZMK)

## 🙏 Acknowledgments

- Original Lily58 design by kata0510
- Community contributors and testers
- Open source firmware developers

---

**Happy typing!** 🎉

_For questions or support, please open an issue in this repository._
