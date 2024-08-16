# GitTest
Waste Markdown Automation Tests
1. Project structure and documentation
 
├─ waste-markdown-app-automation-tests/
│ ├─ apps/-------------------------### [ Waste Markdown Native app ]
│ ├─ configs/----------------------### [ Config files for Zebra TC52 device, android emulator, LambdaTest ]
│ ├─ features/---------------------### [ Gherkin Feature files with Scenarios ]
│ ├─ helpers/----------------------### [ Supporting methods; log helper, screenshots generator, waitForElements helper ]
│ ├─ jira/-------------------------### [ JIRA reporting ]
│ ├─ logs/-------------------------### [ Logs from the test run from: browser, driver, chromedriver, wdio, appium ]
│ ├─ logs/-------------------------### [ XML reports generated after test run ]
│ ├─ screenshots/------------------### [ After completing each step in any Scenario, a screenshot is taken ]
│ ├─ step-definitions/-------------### [ All tests methods used by Feature files ]
│ │ ├─ pageobjects/
│ │ │ ├─ components/---------------### [ POM actions, assertions for shared components ]
│ │ │ ├─ screens/------------------### [ POM actions, assertions for all components per screen ]
│ │ ├─ testMethods/----------------### [ Test methods(Steps) used by Feature files ]
2. Required dependencies
2.1 Install yarn package manager
In Terminal
npm install --global yarn

2.2 Install Android Studio
Android Studio: Install Android Studio to manage the Android SDK and configure the emulator.
2.3 Connect Zebra TC52 device
Connect the Zebra TC52 device to your laptop with a USB cable
To verify if the Zebra device is available type in the terminal
adb devices
Results should show something similar to the: 22189522513878 device
3. How to run it locally
To execute the tests, start the Appium server first, which acts as a server.
In one terminal, run the following command to start the Appium server:
yarn
yarn appium
In a second terminal, run the command for a selected client:
Client	Scenarios location	Command
MultiClients	features/MultiClients	yarn z:multi
CentralEngland	features/CentralEngland	yarn z:ce
EastOfEnglandCoop	features/EastOfEnglandCoop	yarn z:eoe
LincolnshireCoop	features/LincolnshireCoop	yarn z:li
MidCounties	features/MidCounties	yarn z:mc
Loblaw	features/Loblaw	yarn z:ll
4. How to run tests on GitHub Actions
Dispatch tests for a selected client by triggering GitHub workflow:



 
 

