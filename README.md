# Lillypad Custom Keyboard

A custom 58-key split ergonomic mechanical keyboard based on the Lily58 design. This project features a 6×4+4 column-staggered layout with support for both MX and Choc switches, hotswap sockets, OLED displays, and wireless connectivity.

## 🌟 Features

- **Split Ergonomic Design**: 58-key column-staggered layout (6×4+4)
- **Dual Switch Support**: Compatible with both Cherry MX and Kailh Choc switches
- **Hotswap Ready**: No soldering required for switches
- **OLED Displays**: Dual 128×32 OLED screens for customizable information
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

### PCB & Electronics

| Component           | Quantity | Description                 | Notes                      |
| ------------------- | -------- | --------------------------- | -------------------------- |
| Custom PCB          | 2        | Lillypad PCB (left & right) | From EasyEDA files         |
| Pro Micro/nice!nano | 2        | Microcontroller             | ZMK compatible recommended |
| Reset Button        | 2        | Tactile push button         | 6×6mm recommended          |
| Diodes              | 58       | 1N4148 SMD diodes           | SOD-123 package            |

### Switches & Hotswap

| Component            | Quantity | Description                | Notes                                |
| -------------------- | -------- | -------------------------- | ------------------------------------ |
| MX Hotswap Sockets   | 58       | Kailh MX hotswap sockets   | If using MX switches                 |
| Choc Hotswap Sockets | 58       | Kailh Choc hotswap sockets | If using Choc switches               |
| MX Switches          | 58       | Cherry MX compatible       | Your choice of tactile/linear/clicky |
| Choc Switches        | 58       | Kailh Choc v1 switches     | Alternative to MX                    |
| Keycaps              | 58       | MX or Choc compatible      | Profile of your choice               |

### Hardware & Fasteners

| Component        | Quantity | Description          | Source Link                                                        |
| ---------------- | -------- | -------------------- | ------------------------------------------------------------------ |
| M2.5×6mm Screws  | 18       | Phillips head screws | [AliExpress](https://fr.aliexpress.com/item/1005005070119421.html) |
| M2.5×10mm Screws | 4        | Phillips head screws | [AliExpress](https://fr.aliexpress.com/item/1005004657582673.html) |
| M2.5 Standoffs   | Various  | Brass standoffs      | Check case requirements                                            |
| Rubber Feet      | 8-12     | Self-adhesive feet   | For case bottom                                                    |

## 🔧 Assembly Instructions

### 1. PCB Assembly

1. **Solder diodes** (58 total) - Pay attention to polarity!
2. **Install hotswap sockets** - Choose either MX or Choc (or both if PCB supports)
3. **Install reset buttons** - For firmware flashing
4. **Solder controllers** - Pro Micro or nice!nano
5. **Add OLED displays** (optional) - Use sockets for easy removal

### 2. Case Assembly

1. **3D print case parts** using provided STL files
2. **Insert threaded inserts** or prepare screw holes
3. **Install standoffs** using M2.5 screws
4. **Mount PCB** to case with appropriate screws
5. **Attach bottom plate** and rubber feet

### 3. Final Assembly

1. **Install switches** into hotswap sockets
2. **Mount keycaps** on switches
3. **Connect TRRS cable** between halves (if wired)
4. **Flash firmware** (see firmware section)

## 💾 Firmware

This keyboard supports multiple firmware options:

### ZMK (Wireless - Recommended)

- **Controller**: nice!nano
- **Setup**: Use [nickcoutsos.github.io/keymap-editor](https://nickcoutsos.github.io/keymap-editor/) for easy configuration
- **Features**: Wireless, low power consumption, Vial support

### QMK (Wired)

- **Controller**: Pro Micro, Elite-C
- **Configuration**: Full QMK feature support
- **VIA Compatible**: Real-time keymap editing

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
- **Switch Support**: MX and/or Choc hotswap
- **Connectivity**: USB-C, TRRS, Wireless (with nice!nano)
- **Displays**: Dual OLED support
- **RGB**: Per-key and underglow support
- **Dimensions**: Standard Lily58 compatible

## 🖨️ 3D Printing

### Print Settings

- **Layer Height**: 0.2mm
- **Infill**: 20-30%
- **Support**: Required for overhangs
- **Material**: PLA, PETG, or ABS

### Files Included

- Top case (left & right)
- Bottom plate (left & right)
- Knob/encoder cap (if applicable)

## 🛡️ Troubleshooting

### Common Issues

1. **Keys not registering**: Check diode orientation and solder joints
2. **Controller not detected**: Verify USB connection and try different cable
3. **OLED not working**: Check I2C connections and pull-up resistors
4. **Wireless connectivity issues**: Ensure proper battery connection and pairing

### Support Resources

- QMK Documentation: [docs.qmk.fm](https://docs.qmk.fm)
- ZMK Documentation: [zmk.dev](https://zmk.dev)
- Community Discord servers for real-time help

## 🙏 Acknowledgments

- Original Lily58 design by kata0510
- Community contributors and testers
- Open source firmware developers

---

**Happy typing!** 🎉
