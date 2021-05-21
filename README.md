# Pet-Assistant using Machine Learning with EdgeImpulse
HCMUS school project in introduction to IoT/ AIoT class

This is my project using edge impulse to create a machine learning for embedded device using an esp8266 nodeMCU Lua

https://studio.edgeimpulse.com/public/15808/latest

# Intro

I chose a simple accelerometer (mpu6050) for measuring the movement velocity of the pet, for achieving that I attached the module to a simple pet collar and use a small lithium battery to power the ESP-board

Here I used an ESP8266 as a functional microcontroller for obtaining the accelerometer sensor values and collecting the data, using some filtering techniques and data synthesis inside of the code in the microcontroller I obtained  a 2D array of 3 axis in a time t(see DataForwarder.c)

I used the Edge Impulse Data Forwarder which helped me to connect the ESP8266 directly to Edge Impulse, I collected 9 minutes of data dividing equally each label used. Then I created my impulse using spectral features where at the beginning I obtained some random points in the plots, after struggling with the period of the data, I obtained some interesting forms in my feature explorer window.

Once I got the spectral features, I proceeded with the NN classifier using two layers with a little bit more than 30 neurons in total (20 neurons on the first layer and 10 neurons on the second layer). obtaining a pretty usable model.
