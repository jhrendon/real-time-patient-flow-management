# Simulation and testing of Events #

An overview presentation is available here: https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/BMPSession5.pptx


In this session, we will simulate the events that are taking place at the hospital using a test console. The simulation is useful to test the system without having to set up the location tags. We will also see how to view the real time dashboards that will show the patients that are currently in the hospital, where they are, and at what state of the clinical pathway they are in. There are also real time reports that shows how long each patient has been waiting at different states of the clinical pathway.

For example, we will simulate a patient being triaged, patient enters ED, Physician enters ED, etc. We will show reports showing active patients currently in the hospital, and see how long patients have been waiting at different states of the clinical pathway.

## Exercise 5.1: Accessing the Test Console ##

In this exercise, you will open the test console to send different events to the system.

1. Open your browser and go to: http://137.122.88.139:8080/osler-mb/

2. Browse to the shared directory on DropBox and open the corresponding student.xml file. This file contains the test script.

3. Run the tests manually.

Notice that the time stamp is hard coded, so you do not have to wait between events. You can go ahead and send all events in the test scripts.

Open response log console to verify that your events have been sent.

1. Click **home**.

2. Under log analytics click on **Response Log**.

3. Make sure the events have been sent.

Status code should be 200. Other codes correspond to unsuccessful handling of events.


## Exercise 5.2 Viewing the simple SME Dashboards ##
Open the SME Dashboard to view some basic dashboards. These are some basic reports that displays some patients information and their wait times.

1. Using your browser, go to: www.http://137.122.93.228:8080/SME

2. Click on **Unit Map** under Map of rooms and patients.

3. You should see a list of patients. Select the patient that your test scripts have created.

4. View patient state charts, Patient states, and the events received.


## Exercise 5.3 View the advanced Cognos Dashboards ##
We now will look at Cognos dashboards that show more reports about the patients and their wait times and states.

1. Open your browser and navigate to: http://137.122.93.90/ibmcognos/cgi-bin/cognos.cgi?b_action=xts.run&m=portal/welcome/welcome.xts

2. Click on **Home**.

3. Click on **SME\_V2\_Package**.

4. Click on **Shirely**.

5. Click on **New** folder.

6. Click on **ALl ActivePatients**.

This will show you a list of all patients active now. Some of the patients your scripts have created, others created by your colleagues, and maybe others are in the system from before.

7. Open **PatientDetailsBullet** report, and select the ID of the patient you are interested in.

This report shows the states of the patient and how long he has been waiting at that state. The report also shows relevant information such as the care provider ID, start and end time.

8. Go back to Sirely folder.

9. You can open the following four reports:

> a. **Patients table:** This shows all the states and how long the patient has waited in each of those states.

> b. **PatientByUnit:** This report shows the current state and whether they are exceeded the wait time limit, about to exceed, or within range. Green means within range, yellow means about to exceed, and red means exceeded.

You can explore other reports.


## Other remarks ##

- You must be connected to the university VPN to be able to perform the tasks in this exercise.

- The SQL Database is located on this machine: (137.122.93.90).

- There are other test scripts that simulates a more complete clinical pathway. You can open them to view the complete steps. I recommend that you do not run the scripts as it will result in multiple patients being triaged with the same ID.

- If you want to remove existing data in the database (for example, if you want to re-run the tests), then all you need to do is restart the tomcat web server. We implemented a bootstrap that will remove the data from the DB. The bootstrap will also create some demo patients in different states. Of course, you would not want to do that in the production environment.