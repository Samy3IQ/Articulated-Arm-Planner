## 🛠️ How to Use with MakeCode (Python)

---

### 📌 Step 1: Open MakeCode and Switch to Python

1. Go to [makecode.microbit.org](https://makecode.microbit.org/)
2. Start a new project
3. Click the **Python** button to switch to Python mode

---

### 📋 Step 2: Paste This Starter Code

Paste the following code into the editor:

```python
def on_button_pressed_b():
    global index
    index = 0
    while index < len(ServoAngle):
        pins.servo_write_pin(ServoPin[ServoPinNumber[index]], ServoAngle[index])
        basic.pause(2000)
        index += 1
input.on_button_pressed(Button.B, on_button_pressed_b)

index = 0
ServoPin: List[number] = []
ServoPinNumber: List[number] = []
ServoAngle: List[number] = []
ServoAngle = [...]
ServoPinNumber = [...]
ServoPin = [AnalogPin.P0, AnalogPin.P1, AnalogPin.P2]
```

---

### ✂️ Step 3: Replace These Arrays with Your Own

Use the **"Copy Both"** button in the Articulated Arm Planner web app, then replace the following two lines:

```python
ServoAngle = [...]
ServoPinNumber = [...]
```

with the values you copied from the planner.

---

### 🔁 Step 4: Upload to Micro:bit

1. Click the Download button
2. Flash the **.hex** file to your Micro:bit
3. Press Button B to execute the servo movement sequence

---

## ✅ Done!

Your Micro:bit will now run the servo sequence created in the Articulated Arm Planner web app. You can adjust angles or movement order anytime and repeat the steps to update the program.
