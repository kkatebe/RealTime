RealTime
========

// Ultrasonic Range Finder
// Arduino & Processing Motion detection
// This example is used as part of a class project using Processing and Arduino libraries
// To run Processing video and frame-by-frame animations
// Links to documentation and code examples for stand alone sketches included

// Arduino sketch includes Arduino Ping))) sketch to read data inputs
// And MQTT code example to setup MQTTClient
// Additional libraries needed: source examples: https://github.com/i-DAT/mqttArduinoTemplate

//Processing sketch runs MQTTClients to publish and subscribe to via Arduino
// Additional Processing libraries included: 
// Source examples: https://github.com/i-DAT/mqttProcessingTemplate

// N.B This is totally clunky and messy!!
// Haven't tested this code since submitting this project :(
// Please use link sources to check for any error or issues




//Arduino Sketches
//Include libraries

  #include "SPI.h"
  #include "WiFly.h"
  #include "PubSubClient.h"

//Broker settings
// replace with the IP address of your broker ,
byte server[] = { 127.0.0.1 }; // Your Broker IP Adress

// Default port is 1883 
// To help get around network restrictions, you may need broker set as port 80
int port = 80; 

char subscribedChannel[] = "TopicName"; // Topic to subscribe to
char deviceName[] = "OutTopic"; // set a unique name for each device connected to the broker




// Processing sketches
// Set Processing MQTT Parameters, assign IP Adress and port number (e.g. 80 or 1883)

  private String MQTT_BROKER ="tcp://127.0.0.1:80"; // Ip adress and port number
  private String CLIENT_ID = "OutTopic"; // Unique ID, client you wish to publish to

// If "client.publish" is successful
// Run if statement to check Client Topic and convert values to integers
// Clunky method, could be neater!

  if (topicName.equals("OutTopic")) {
      String data = new String(payload);
      int number = Integer.parseInt(data);
      
// Using if statement to run different functions and code

      if(//Something do something) {
        //Do Stuff!!
        //Run function(myfunction);
        }
