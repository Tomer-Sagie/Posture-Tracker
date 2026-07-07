# Bill Of Materials
### Here is the BOM!


| # | Part                         | Description                                                   | Qty | Notes |
|---|------------------------------|---------------------------------------------------------------|-----|-------|
| 1 | Seeed XIAO ESP32S3           | Small ESP32-S3 dev board with onboard Li-Po charging         | 1   | Main microcontroller, handles IMU + motor + optional BLE/Wi‑Fi |
| 2 | LSM6DSV IMU module           | 6‑axis low-power IMU (accelerometer + gyroscope)             | 1   | Mounted near center of board; I²C to XIAO |
| 3 | Coin vibration motor (3 V)   | Thin ERM vibration motor                                     | 1   | Haptic feedback when bad posture is detected |
| 4 | N‑channel MOSFET             | Logic-level MOSFET (e.g., AO3400A) for motor driver          | 1   | Low-side switch for vibration motor |
| 5 | Flyback diode                | Small signal diode (e.g., 1N4148)                            | 1   | Across motor to clamp inductive spikes |
| 6 | Gate resistor                | 100 Ω resistor                                               | 1   | Between XIAO GPIO and MOSFET gate |
| 7 | Gate pull-down resistor      | 10 kΩ resistor                                               | 1   | From MOSFET gate to ground |
| 8 | Bulk capacitor               | 10–47 µF low‑ESR capacitor                                   | 1   | Across motor supply to smooth current spikes |
| 9 | Decoupling capacitors        | 0.1 µF ceramic capacitors                                    | 2–3 | Near IMU and MCU power pins |
|10 | Li‑Po battery (200 mAh)      | 3.7 V, ~200 mAh rechargeable Li‑Po                          | 1   | Main power source, JST‑PH connector preferred |
|11 | Slide power switch           | Small SPDT slide switch                                      | 1   | On VBAT line to fully power off the device |
|12 | JST‑PH 2‑pin connector       | Battery connector on PCB                                     | 1   | Matches Li‑Po battery plug |
|13 | Custom PCB                   | 0.8–1.0 mm thick PCB                                         | 1   | Holds XIAO, IMU, motor driver, switch, connectors |
|14 | 3D‑printed enclosure         | Custom printed case for back/strap mounting                  | 1   | Thin, curved back, comfortable on upper back |
|15 | Misc. headers / pads         | Pin headers or test pads                                    | few | For programming, debugging, and module connections |
