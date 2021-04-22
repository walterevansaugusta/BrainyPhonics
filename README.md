# BrainyPhonics
An application dedicated towards providing lectures and quizzes to underprivileged elementary school students in a fun and interactive way.

### Motivation
The purpose of this project is to provide an app version of the already existing BrainyPhonics web application. This app runs on Androids and serves to mimic the web application precisely, offering no advantage over the web application or vice versa.

### System Architecture
This project uses a model-view-controller architecture - the models are used to represent entities including the User, Question, Answer, etc. The views are used to provide a kid-friendly interface. The controllers are used to grab data from the Data Analytics Platform, an offline database used to grab assets and information pertaining to classes and quizzes.

# Delivery Documentation

### Release Notes (as of V1, 23 April 2021)
Recent features for this latest sprint include:
- NEW FEATURES
  - new screens for benchmarking student progress; the Contractions Check and Piggybank screens, allowing users to view how many questions they've answered and how many coins they have/have spent
  - authentication with the live DAP for student login identities has been incorporated; the local storage now stores the student's ID, display name, and client authentication tokens as received from the DAP via REST
- BUG FIXES
  - some landscape vs. portrait constraint issues, such as on the Word Structures and Quiz screens, have been resolved
  - rather than overwriting upon restart each time, the local JSON data actually persists properly with all values
  - the user's display name actually now displays upon login, rather than "Jane Doe"
  - A few slidedeck image loading and scroll issues have been addressed
- KNOWN BUGS
  - some constraint issues, such as the home screen on landscape and the piggybank's coins in portait, still persist
  - some autogenerated buttons from Android Studio also persist
  

  
### App Installation
PREREQUISITES: 
  - Android Studio 3.2+, Android SDK + Developer Tools, and compatible emulator or physical android device
    - if you have an AMD processor and are having trouble emulating Android on your PC, this is an AMD-specific Hypervisor (emulator driver) issue--contact jaredbtlr@gatech.edu for individual help in resolving this
  - [BACKEND] Node.js (Make sure node --version prints out a version number)
  - [BACKEND] MongoDb (pointing to remote access cloud server above)
  - [BACKEND] npm (Run npm --version in your terminal and expect to see a version number printed out)
  - [CHECKING FOR DEFAULT DEPENDENCIES] be sure to check your build.gradle to ensure your Android Studio supports JUnitRunner, Espresso, and ConstraintLayouts. Also be sure you have access to the java.lang.Object.BroadcastReceiver component
  
DEPENDENCIES
  - this app uses v1.2.0 of Volley, a REST client for Java that makes use of the JSONObject and JSONArrays
  
DOWNLOAD
  - Clone this repository (git clone git@github.com:Shrenil19/BrainyPhonics.git
  - [BACKEND] To install local backend instance, clone this repository (git clone git@github.com:jvt/Brainy-Kidz.git) and follow instructions on: https://github.com/jvt/Brainy-Kids
  - Ensure whichever method (local, Team 357 Cloud, or Client Cloud) of backend connection is properly configured in the app at: BrainyPhonics/app/src/main/java/com/example/heratale_app/json/JsonHelper.java
  
BUILD
  - Be sure to build with Gradle or 'Make Project' within Android Studio, so Gradle can install Volley
  
INSTALLATION:
- No extra installations are necessary so long as Android Studio and the SDK have already been properly configured. See Android Developers documentation if you are having trouble installing these.
  
HOW TO RUN:
  1. In Android Studio, select your app from the run/debug configurations drop-down menu in the toolbar.
  2. In the toolbar, select the device that you want to run your app on from the target device drop-down menu.
  
TESTING:
- From a terminal window, run npm run test or npm test (both do the same thing)
- Let the tests run, it will generate a coverage window in the terminal once all the tests have completed running
In order to run this project, JetBrains Toolbox, Gradle, and Android Studio must be installed. Once all of these are installed, clone this repository and open it on Android Studio. Press run in order to have the emulator run the app.

### Cloud Server Access
An instance of the Data Analytics Platform is currently running on a cloud server, which can be accessed by any device connected to the internet with the proper authentication. Once connected to the server, please refer to the documentation of the DAP which is included below.

Review the Information on the Wiki to get an overview of setting up external Apps to use the DAP
[https://github.com/BrainyEducation/Brainy-Kids/wiki](https://github.com/BrainyEducation/Brainy-Kids/wiki)

To modify the connection to the server ip to the instance's static IP: 45.76.254.167. This connection is found in the app at json/JsonHelper.java . You will require the root password which can be obtained by contacting Shrenil Shaun Sharma, or the current client of the project. You may also modify this connection to point to a DP location of your choice. Please keep in mind that when emulating an android device through android studio, you are not able to emulate endpoint access to external networks. 

Cloud Server Static IP: 45.76.254.167
@root user

# Credits
Credits to our client - Dr. Walter Evans - who came up with the idea for this project and originally led the team building the web version of the app.
