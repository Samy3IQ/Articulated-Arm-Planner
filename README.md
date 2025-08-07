## 🛠️ How to Use with MakeCode (Python)

To make the output from **Articulated Arm Planner** compatible with your Micro:bit using MakeCode Python:

---

### 📌 Step 1: Open MakeCode and Switch to Python

1. Go to [makecode.microbit.org](https://makecode.microbit.org/)
2. Start a new project
3. Click the **{ } Python** button to switch to Python mode

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
ServoAngle = [35, 0, 90, 70, 0, 35, 180, 70, 90, 35, 0]
ServoPinNumber = [1, 0, 2, 1, 2, 1, 0, 1, 2, 1, 2]
ServoPin = [AnalogPin.P0, AnalogPin.P1, AnalogPin.P2]
