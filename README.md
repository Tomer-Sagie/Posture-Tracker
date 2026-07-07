# Posture-Tracker
A wearable device that tracks back posture, and gives off a vibration to let a user be aware of their posture, and fix it.

## More Info About the Project!

### 1. Who is this for?
  Technically, this is for the hackclub stardance program, but in terms of this project, I designed this in mind for students such as myself, who spend a lot of time sitting down doing homework, studying, using their phones, and working on hackclub projects!

### 2. What is the Problem Here?
   Well, I noticed that I have bad posture, especialy during the habits listed above. Through my experience, just thinking about having better posture will not solve this issue. Because of this issue, I, and probably many ### other people like me, experience back pain and an overall decrease in posture throughout other areas of life.

### 3. Why Does this Matter?
   When these habits go unnoticed and untreated, slouching can turn into a lifetime of back pain and bad posture. On a shorter timeframe, it can hinder concentration in school and studying, as well as decrease performance in athletic activities.

### 4. My Solution:
   My solution to this issue is to create the posture tracker device (name in progress). This is a wearable device that uses rotation sensors to identify bad posture. When bad posture is detected, a simple vibration alerts the user to fix their posture. Thus, instead of having to actively thing about improving your posture, this device can alert you automaticaly. While more research is required into the BOM, location of the device, and specifications regarding angle calculations, this proof of concept should effectively represent the problem being faced, and the solution being presented.

## Even More Info!!

### More Detailed Project Description
  Posture-Tracker is a compact wearable device that tracks bad posture and gently reminds users to correct it. It is designed for students who spend long periods sitting, especially while doing homework, studying, or working on projects. The device will be small and comfortable enough to wear daily, likely on the back or another placement chosen through research. When bad posture is detected, it will send a vibration alert and may also connect to a phone app for tracking and control. The project prioritizes a budget target of about $50–$60. The goal is to create a device that is practical enough for everyday use.
  
## BOM

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

### More Info Coming Soon...
