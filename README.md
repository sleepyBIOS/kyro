# kyro
NOTE: you need to have V1.1 AHK installed. https://www.autohotkey.com/

## table of stuff lol

1. [binds](#binds)
2. [color](#color)
3. [bezier](#bezier)
4. [easing](#easing)
5. [misc](#misc)
6. [fov](#fov)
7. [example](#configuration-example)

---

## 1. Binds

### Keybinding Settings:
self explanitory

- **Keybind (`RButton`)**: 
  - main key to activate the aim assist
---

## 2. Color

### Saturation:
saturation (allowing the aimbot to see)

- **saturation (`10`)**: 
  - sets the color saturation of the aim assist. higher values result in more intense saturation. keep this between 7.5-15
---
## 3. Bezier
### Smoothing Curves:
bezier curves are used to smooth out the aimbot's aim adjustments.

- **LinearCurveX (`0.350`)**: 
  - controls how smooth the aim adjustments are along the X-axis (horizontal).
  
- **LinearCurveY (`0.200`)**: 
  - controls the smoothness of aim adjustments along the Y-axis (vertical).
---

## 4. Easing

these settings control how the aimbot adjusts its aim and predicts where the target will be.

- **SmoothnessX (`100`)**: 
  - controls the smoothing of the aimbot’s aim adjustments along the X-axis.
  
- **SmoothnessY (`120`)**: 
  - controls the smoothing along the Y-axis.
  
- **SmoothingReplicatorX (`5`)**: 
  - replicates smoothing on the X-axis.
  
- **SmoothingReplicatorY (`5`)**: 
  - replicates smoothing on the Y-axis.
  
- **SmoothingDividerX (`250`)**: 
  - a divisor for the smoothing calculation on the X-axis.
  
- **SmoothingDividerY (`250`)**: 
  - a divisor for the smoothing calculation on the Y-axis.

### Prediction:
these settings control whether the aimbot attempts to predict enemy movement.

- **Enabled (`false`)**: 
  - self explanitory lmao
  
- **Mode (`Ideal`)**: 
  - **Ideal**: best for highly accurate prediction.
  - **Multiplication**: scales the movement prediction.
  
- **PredictionX (`5`)**: 
  - horizontal prediction factor.
  
- **PredictionY (`8`)**: 
  - vertical prediction factor.

---

## 5. Misc

miscellaneous settings affecting the aimbot’s update frequency and FOV.

- **AimbotUpdateTick (`600`)**: 
  - the update frequency of the aimbot in milliseconds.

- **AimbotUpdateMS (`1000`)**: 
  - the interval at which the aimbot updates.

- **CameraToGunFOV (`85`)**: 
  - set this to your ingame fov (by default 85)

- **FlickTime (`2`)**: 
  - controls how long the aimbot waits before flicking to a target.

---

## 6. FOV (Field of View)

### Adjusting the Field of View:
these settings define how far the aimbot will search for targets based on your screen size and the FOV.

- **FOVOffsetX (`5`)**: 
  - the horizontal offset for the FOV.
  
- **FOVOffsetY (`5`)**: 
  - the vertical offset for the FOV.

---

## 7. Example

here is a sample configuration file for kyro:

```json
{
  "kyro": {
      "Binds": {
          "Keybind": "RButton",
          "Pause": "Esc"
      },
      "Color": {
          "Saturation": 10
      },
      "Bezier": {
          "LinearCurveX": 0.350,
          "LinearCurveY": 0.200
      },
      "Easing": {
          "SmoothnessX": 100,
          "SmoothnessY": 120,
          "SmoothingReplicatorX": 5,
          "SmoothingReplicatorY": 5,
          "SmoothingDividerX": 250,
          "SmoothingDividerY": 250,
          "Prediction": {
              "Enabled": false,
              "Mode": "Ideal",
              "PredictionX": 5,
              "PredictionY": 8
          }
      },
      "Misc": {
          "AimbotUpdateTick": 600,
          "AimbotUpdateMS": 1000,
          "CameraToGunFOV": 85,
          "FlickTime": 2
      },
      "FOV": {
          "FOVOffsetX": 5,
          "FOVOffsetY": 5
      }
  }
}
```
