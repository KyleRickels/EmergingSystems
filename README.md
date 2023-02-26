###### CS-350 Emerging Systems Architecture and Technology
# EmergingSystems

  
  
### Project Summary 
##### This project, as shown in the 7-1 state machine diagram, brought together several key components of embedded systems to prototype a Wi-Fi Thermostat. One of the board’s timers was used to create a task scheduler where the temperature is polled every 200 ms, the heat control state machine tics every 500 ms, and the thermostat outputs data once every second. In this project I used I2C to read the on-board temperature sensor. GPIO is used to read the temperature +/- buttons and drive an LED indicating heat output. UART is used to output thermostat data to the console, simulating communication with a server.
### Successes 
##### This project showcased my ability to meet all of the design requirements without adding features outside of the project scope. I used best practices to ensure the project meets design standards while keeping it simple.
### Areas for growth
##### While this program is fully functional, one area I can improve is code organization and file structure. For better organization, the functions can be moved to separate files and header files. Another way to organize them is to declare the functions at the top and build the functions below the main. The thermostat project did not require much code, however for a larger project the code should be organized differently. That will keep it manageable as it scales up.

### Tools and Resources
##### [What tools and/or resources am I adding to my support network?]
### New Skills
##### [What skills from this project will be particularly transferable to other projects and/or course work?]
### Best Practices
##### [How did you make this project maintainable, readable, and adaptable?]

