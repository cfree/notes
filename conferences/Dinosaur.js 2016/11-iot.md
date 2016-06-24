# IoT: Prototyping with Firebase and JavaScript

Jen Tong, Google Cloud Platform
@mimmingcodes


## EE for web devs

Bits & volts
Binary 0 / 1

Analog signal broken down to ratio, reads info from outside world

PWM = Pulse Width Modulation. Analog signal, ratio of voltage / time


### Components

Raspberry Pi can run Node.js, has APIs.
Arduino has lots of flavors. Write code "on the metal". More pins to interact with the outside world, more accurate and quick to respond.

Bread board good for prototyping
Perf(oration) board good for testing

LED = simple state expressor
Resistor = bad wire


## Recipe for IoT

Focused on rapid developent. Making one of something:

*Formatta + Arduino Uni + Raspberry Pi + Johnny Five + Firebase*

===

Formatta: comes with Arduino, acts as a layer between lower-level logic and software

Johnny Five library - has good documentation, pictures of circuits and Node.js programs

Firebase = Real-Time Database, Authentication, Hosting
- Connect
- Write Data
- Read Data (listener looking for changes)


## Live build & code

"hello world of electronics" LED and button


## Silly demos

