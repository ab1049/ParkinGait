# parkinGait
## Steps to install project
1. git clone project using a terminal
2. Install node modules using `npm i` **in the same folder as you've cloned this project**
   <br> a. For help installing npm please visit [this link](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
3. Start expo project using `npx expo start`
    <br> **NOTE:** Once 'npm' is installed on the computer, there is no need to reinstall it everytime. One can simply navigate to the folder that the project is cloned in and type 'npx expo start' to launch the project.
    <br> Once the project is started, one can scan the QR code displayed to have access to the app **assuming the ExpoGo app is already installed on the device**.
4. To deploy website, cd into website folder and run `firebase deploy hosting`
    <br> a. The website itself can be found at [this link](https://parkingait.web.app/)

## Understanding File Strucutre
1. React Native App Files
    1. Calibration.js: page where user sets goal step length and calibrates step length constants
    2. Dashboard.js: page where users can track step length and asymmetry data
    3. Login.js: First page that a user opens up to where they can log in
    4. MainPage.js: Main page where user can start step length tracking and control cuing
    5. Register.js: Page where user can create a profile
    6. **For all files please see the documentation therein for what each part does**
2. Website Files
    1. index.html: main landing page where user can log in
    2. dashboard.html: page where physical therapist can track patient data
    3. newPatient.html: page where physical therapist can add new patients to a dashboard
    
## Current Method to Allow Therapist/Patient Access to App
### Note that because this app has not been deployed yet, the environment must be manually started
**How do I run the app continuously?** 
<br> Due to the fact that this app has not been launched via the Apple Developer environment, the only way to ensure this app is accessible all hours of the day for all types of phones without having to let a physical computer run 24/7 is to make use of a **Virtual Machine (VM)**. Using this method, one only needs to set up the environment once and (assuming the Virtual Machine used does not turn off daily) then the app will always be available for users. 
<br> Many universities allow students to reserve VMs and these can be started and closed **without canceling the code one is running**. As of May 2023, this  method is being used to ensure access to the app remains open until the app is published (see below for more details). To learn more about VMs generally, please visit [this link](https://www.vmware.com/topics/glossary/content/virtual-machine.html).
<br> Once a VM is deployed, one should follow the installation steps listed above (reproduced below) on the machine to ensure the project begins correctly. 
<br>
<br> **Steps to start up the app in a Virtual Machine**
1. git clone this project using a terminal
2. Install node modules using `npm i` **in the same folder as you've cloned this project**
   <br> a. For help installing npm please visit [this link](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
3. Start expo project using `npx expo start`
    <br> **NOTE:** Once 'npm' is installed on the computer, there is no need to reinstall it everytime. One can simply navigate to the folder that the project is cloned in and type 'npx expo start' to launch the project.
    <br> Once the project is started, one can scan the QR code displayed to have access to the app **assuming the ExpoGo app is already installed on the device**.
<br> Again, it is important to note that unless updates are made on the backend to this app, **the app will always be accessible after the first instance of 'npx expo start' is created**. If updates are made, one should first push these updates to the cloned version of this project and then re-run 'npx expo start'.
    
## Steps to proceed forward: 
### To make this app deployable, these are the steps that should be followed
1. Set up Apple developer account: https://developer.apple.com
2. Set up provisioning profile, certificates, and devices
3. Run eas build -p ios to build app
4. Follow steps in cli to import the files created in step 2
5. Import new .ipa file that you can find in https://expo.dev/ to your phone using xCode

<br> Any questions about this project should be directed to dominicschottland@yahoo.com
  
