# Introduction
- Design a system with the capabilities to:
    - Control lights.
    - Control fans and their speed.
    - Control doors.
    - Allow user to register and login.
    - Allow user to add new devices easily.
# Demo
- [Link website](https://ce232-submodule.onrender.com/login).
- [Demo](https://youtu.be/7z1hmoy8tpo) control devices, set time to turn on/off lights.
- [Demo](https://youtu.be/jzDClkvZomQ) register, login, add new devices.
# System design
![](/images/kien_truc_he_thong.png)\
- ESP32s are used to control hardware devices (fan, light, door).
- MQTT protocol is used for communication between backend server and ESP32s
- The website is used by user to control their devices via internet.
- MongoDB stores user data and the deivces in the system.
## ESP32
- Based on ESP-IDF framework.
- Uses H-Bridge motor driver L298N to control fans' speed
- Controls servos (doors) using pulse width modulation (PMW).
- Directly control leds (lights) using GPIOs.
## Website
- Backend: uses framework Express.js (Node.js) to write APIs.
- Fontend: uses React library in adition to Material UI.
- Hosting: uses free hosting service [render.com](https://render.com/).
![](/images/web.png)
