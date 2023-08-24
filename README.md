# Dell Optiplex 3070 Micro running macOS Ventura 13.5
- Opencore 0.9.4
- macOS Ventura 13.5

# Hardware Specifications
| Component  | Specifications|
| ------------- | ------------- |
| CPU | Intel Core i5 9500t |
| RAM  | 4GB DDR4 2666MHZ |
| SSD | APACER 256 SATA |
| iGPU  | Intel UHD 630 |
| Audio | Realtek ALC255|
| Ethernet  | Realtek RTL8111 |

# What works:
- All USB ports
- Gigabit LAN
- Internal speaker and AUX port
- Hardware Acceleration
- HDMI & DisplayPort
- Sleep
- Screensasver
- iServices (iMessage & FaceTime)
- Content Caching

# What doesn't work:
- WiFi and Bluetooth (no WiFi and Bluetooth onboard)

# BIOS Settings
- Networking: DISABLE internal nic with PxE (makes ethernet run at 100baset)
- Disable secure boot
- Disable Intel SGX
- Disable VT-D and VT for Direct I/O

# BIOS+ settings via GRUB
- DVMT to 64MB: setup_var 0x8dc 0x02
- Disable CFG lock: setup_var 0x5be 00

# notes
Make HDMI persist on boot (login screen)
- add "igfxonln=1" to boot-arg

Show picker
- hold OPT or ESC before boot
