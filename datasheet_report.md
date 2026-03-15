## Introduction

The L293D is a motor driver IC that sits between a microcontroller and a motor. 
Microcontrollers output weak signals — not nearly enough to drive a motor directly. 
The L293D takes those signals and translates them into the kind of current a motor 
actually needs.


---

## What is Inside the L293D

The IC is built around a few key internal components that each do a specific job.


![alt text](https://github.com/bit07Forger/images/blob/main/image/images.jpeg?raw=true)


**Power Transistors** act as electronic switches. The L293D has 8 of them, four 
dedicated to each motor. They switch on and off rapidly to control how much current 
reaches the motor, handling up to 600mA per channel.

**Logic Gate Circuits** help the IC interpret what the microcontroller is asking for. 
NAND gates make basic yes/no decisions, NOT gates flip HIGH signals to LOW and vice 
versa, and buffers strengthen weak input signals before they reach the switching stage.

**Protection Circuits** handle the safety side of things. If the IC overheats it 
shuts itself off automatically. Current limiting stops excessive flow before damage 
occurs and ESD protection guards against static discharge.

---

## The H-Bridge — Controlling Direction

The H-bridge is the part of the IC responsible for deciding which way the motor spins. 
It uses four switches arranged around the motor in a shape that resembles the letter H.

![alt text](https://github.com/bit07Forger/images/blob/main/image/1585313613715-h-bridge.gif?raw=true)

- **Forward rotation** — the top-left and bottom-right switches close, pushing current 
through the motor in one direction and spinning it clockwise
- **Reverse rotation** — the top-right and bottom-left switches close instead, 
reversing the current flow and spinning the motor counter-clockwise
- **Braking** — both bottom switches close simultaneously, connecting the motor 
terminals together and creating an electrical brake

One important safety detail: the internal logic never allows the top and bottom switches 
on the same side to close at the same time, which would cause a short circuit.

---

## PWM — Controlling Speed

PWM stands for Pulse Width Modulation. Rather than feeding the motor a constant voltage, 
PWM switches the power on and off very rapidly. The proportion of time the signal spends 
on versus off is called the **duty cycle**, and that is what determines speed.

| Duty Cycle | Motor Behaviour |
|---|---|
| 100% | Full speed |
| 75% | Three quarter speed |
| 50% | Half speed |
| 25% | Quarter speed |
| 0% | Stopped |

So with a 12V supply, a 50% duty cycle delivers an average of 6V to the motor — half 
speed without wasting the other half as heat through a resistor. This is why PWM is 
preferred over resistor based speed control: it is more efficient, generates less heat, 
and keeps the motor torque stable even at lower speeds.

---

## Putting It All Together

Direction and speed work independently of each other. The H-bridge handles which way 
current flows through the motor, and PWM on the enable pin controls how much of that 
current gets through. Combined, they give full bidirectional speed control over two 
motors from a single IC.

To run a motor forward at half speed: set the direction inputs for forward rotation, 
then apply a 50% PWM signal to the enable pin. The H-bridge routes the current in the 
right direction while PWM chops it on and off to hit the target speed.

---

## Conclusion

The L293D packages transistor switches, logic circuits, H-bridge control, and protection 
systems into one small IC. It handles the complexity of motor control internally, leaving 
the microcontroller to simply send direction and speed signals without worrying about 
what happens underneath.