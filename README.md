###### CS-350 Emerging Systems Architecture and Technology
# EmergingSystems

  
  
### Project Summary 

##### This project, as shown in the 7-1 state machine diagram, brought together several key components of embedded systems to prototype a Wi-Fi Thermostat. One of the board’s timers was used to create a task scheduler where the temperature is polled every 200 ms, the heat control state machine tics every 500 ms, and the thermostat outputs data once every second. In this project I used I2C to read the on-board temperature sensor. GPIO is used to read the temperature +/- buttons and drive an LED indicating heat output. UART is used to output thermostat data to the console, simulating communication with a server.


### Successes 

##### This project showcased my ability to meet all of the design requirements without adding features outside of the project scope. I used best practices to ensure the project meets design standards while keeping it simple.


### Areas for growth

##### While this program is fully functional, one area I can improve is code organization and file structure. For better organization, the functions can be moved to separate files and header files. Another way to organize them is to declare the functions at the top and build the functions below the main. The thermostat project did not require much code, however for a larger project the code should be organized differently. That will keep it manageable as it scales up.


### Tools and Resources

##### Knowing how to compare available development boards is a valuable resource that I picked up from this course. There are several makers of development boards with many available product lines. Now, with my own TI development board and the accompanying Code Composer Studio, I have the tools ready to start the next project that comes along.


### New Skills

##### I work with embedded systems every day, and I learned many new things in this course. I now have a better understanding of the hardware architecture of embedded systems. This is important to understand when selecting hardware. I also gained a much deeper understanding of how the software interacts with the hardware. In my work, the device drivers and operating systems are abstracted. Diving in to the details gives more of a systems level view, enabling someone to make better choices.


### Best Practices

##### To keep the project maintainable, readable, and adaptable, I followed Embedded Systems coding best practices. This can be seen where the state machines shown in diagram are converted to C. Local variables are used within the state machines and global variables are used for data that needs to be shared with multiple state machines. The global variables have a _g suffix for easy identification. On power up, and in the event of a failure, all state machines default to their initialization state. The button flag variables are declared as volatile because the button interrupts are never explicitly called. Not declaring them as volatile may cause the compiler to optimize them away. Similarly, the local variables are declared as static to ensure their values are maintained through function calls.
##### Further, I avoided several common pitfalls. Every state machine transition condition is mutually exclusive and there is always a condition that evaluates to true. No state machine transitions wait on an external input. Some inputs are sampled, and some generate interrupts. 


