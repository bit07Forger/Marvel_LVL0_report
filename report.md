# Task 2 : API 

An **API (Application Programming Interface)** is a set of rules and protocols that allows different software applications to communicate with each other. I implemented the **OpenWeather API** — a free, widely-used meteorological data service that provides real-time weather information by simply passing a city name or coordinates along with an API key — to build a live weather application using **HTML, CSS and JavaScript**.

From the OpenWeather API, I fetch two types of data: first, **current weather conditions** such as temperature, humidity, wind speed and sky conditions for any city in the world, which I use to dynamically update the UI; and second, **location-based weather data** that maps a user's search query to real-time atmospheric readings pulled directly from weather stations across the globe.![text](<Screenshot 2026-02-28 100534.png>)![alt text](<Screenshot 2026-02-28 100550.png>)

# Task 3 : Working with Github

GitHub is a web-based platform that provides hosting for Git repositories. It serves as a centralized location to store code, track changes, and collaborate with others using Git — a distributed version control system. GitHub Actions is a built-in CI/CD feature that allows you to automate workflows such as testing and deployment directly from your repository. Issues are used to track bugs, feature requests, and tasks, while Pull Requests are the standard way to propose and review code changes before merging them into the main branch.

My process:
* Visited the given repository at [UVCE-Marvel/git-task](https://github.com/UVCE-Marvel/git-task) and read through the README to understand the tasks required.
* Forked the repository to create a personal copy under my own GitHub account.
* Cloned the forked repository and made the necessary changes as instructed in the README.
* While committing the changes, I created a new branch specifically for this commit to keep the work isolated from the main branch.
* Opened a Pull Request from my new branch, comparing it against the original repository's main branch.
* Reviewed the differences in the Pull Request and submitted it for review.
* Explored GitHub Issues by reading existing ones and understanding how they are used to track tasks and bugs within a project.
[link](https://github.com/bit07Forger/git-task)![alt text](<Screenshot 2026-02-28 103129.png>)![alt text](<Screenshot 2026-02-28 103218.png>)

# Task 6 : The Matrix Puzzle (Getting familiar with numpy)

NumPy is a powerful Python library used for numerical computing, providing support for 
large multi-dimensional arrays and matrices along with a collection of mathematical 
functions to operate on them. Matplotlib is a plotting library used to visualize data 
and arrays as graphs and images. Together they form the backbone of data manipulation 
and visualization in Python.

I went through the provided tutorial videos and the NumPy learning document to get familiar 
with array operations such as reshaping, slicing, flipping, and transposing before 
attempting the puzzle. Opened Google collab Notebook and worked through the matrix puzzle 
with the following steps:

1. Installed and imported the NumPy and Matplotlib libraries
2. Loaded the provided `.npy` file containing the scrambled NumPy array
3. Checked the shape of the array to understand its structure and determine the 
correct dimensions for reshaping
4. Reshaped the flat array into a square matrix which unscrambled the data into 
a recognizable structure
5. Rotated the array by 90 degrees to correct its orientation and obtain the final image
6. Used `matplotlib.pyplot.imshow()` to visualize and reveal the hidden image   [Click here to view the notebook](https://colab.research.google.com/drive/1jPIIZG69gxIJNbIUoHnwrZfHpPSZttSx#scrollTo=lDrpy7J9U3m3)

![alt text](<Screenshot 2026-03-13 125448.png>)

# Task 9 : Tinkercad

Tinkercad is a free, browser-based CAD and circuit simulation tool by Autodesk that allows 
you to design 3D models and simulate electronic circuits without any physical hardware. It 
is widely used for prototyping Arduino-based projects and is beginner friendly with a 
drag-and-drop interface.

 Built a simple 
circuit using an ultrasonic sensor and an Arduino to estimate the distance between the 
sensor and an obstacle. The ultrasonic sensor works by emitting sound waves and measuring 
the time taken for them to bounce back, which is then used to calculate the distance. 
Displayed the results on the serial monitor in real time.

Following this, built a radar system by combining the ultrasonic sensor with a servo motor. 
The servo motor rotates the sensor across a range of angles to cover a wider detection area, 
while the ultrasonic sensor continuously measures the distance of any object within its 
path. Successfully simulated both circuits on Tinkercad and verified the expected outputs.   [Click here to view the github repo](https://github.com/bit07Forger/ultrasonicsensor)![alt text](<Screenshot 2026-02-26 211552.png>)![alt text](<Screenshot 2026-02-26 211644.png>)

# Task 10 : Speed Control of DC Motor

DC motor control involves two key techniques: PWM (Pulse Width Modulation) to control speed 
by adjusting average voltage through rapid on/off switching, and an H-Bridge circuit to 
control rotation direction by reversing current flow through four switching elements. The 
L298N motor driver acts as an intermediary between the Arduino and the motor, amplifying the 
weak control signals from the Arduino into enough current to drive the motor.

Made the necessary connections between the Arduino UNO, the L298N driver, and 
the 5V BO motor with proper shared ground connections. Wrote the Arduino sketch in the 
Arduino IDE with two main functions: `directionControl()` to alternate the motor between 
clockwise and counterclockwise rotation,and since I am not using a potentiometer hence can not control the speed. Successfully uploaded the code and verified the 
motor responding correctly to change in direction.We need to have a common ground between the arduino and the L289N motor driver.
 [![alt text](<IMG_20260227_145506.jpg>)](https://drive.google.com/file/d/145kc0o0OgpnAQPuUvbYlA0eLYkSc7Sqd/view?usp=sharing)

# Task 11 : LED Toggle Using ESP32

The ESP32 is a low-cost microcontroller with built-in Wi-Fi and bluetooth along with multiple GPIO pins that can 
be connected to LEDs, sensors, and other components. It is programmable via the Arduino IDE 
and is widely used in IoT projects that require wireless control of hardware. The goal of 
this task was to host a standalone web server on the ESP32 that allows an LED connected to 
one of its GPIO pins to be toggled on and off remotely from any browser on the same Wi-Fi 
network.

Set up the Arduino IDE with the necessary ESP32 board support package and connected the LED 
to the appropriate GPIO pin with a resistor. Wrote and uploaded a sketch that connects the 
ESP32 to the local Wi-Fi network, after which it obtains an IP address and begins hosting a 
web server. Visiting this IP address from a browser serves a dynamically generated HTML page 
with a toggle button. When clicked, the browser sends an HTTP GET request to the ESP32 which 
reads it, switches the GPIO pin HIGH or LOW to control the LED, and sends back an updated 
page reflecting the new state. Successfully verified the LED could be toggled wirelessly in 
real time from a browser.

![alt text](<Screenshot 2026-02-25 143917.png>)
[![Alt text](<IMG_20260225_144417.jpg>)](https://drive.google.com/file/d/1L9ST2idUkuW6nH7Bx6JEy4cqVGquDGVp/view?usp=sharing)

# Task 12 : Solder Prerequistes


# Task 18 : Sad Servers  "Like LeetCode for Linux"

 The [Command Line Murders](https://sadservers.com/scenario/command-line-murders) 
scenario is a detective-style challenge where you investigate clues hidden across system 
files and logs to identify the culprit of a murder mystery, purely through Linux commands.

Got familiar with Linux commands through the provided [article](https://www.hostinger.com/tutorials/linux-commands) 
before tackling the Command Line Murders scenario. Launched the browser-based terminal on 
the Sad Servers platform and began exploring the directory structure using `ls` and `cd` 
to navigate through the available files and folders. Used `cat` to read through clue files 
and gather the initial hints laid out in the mystery. Filtered through large log files using 
`grep` to search for specific keywords and narrow down relevant information. Pieced together all the evidence gathered to successfully identify the 
perpetrator named "Joe Germuska" and echoed the name as the solution to make the server happy.
![alt text](<Screenshot 2026-02-28 130737.png>)