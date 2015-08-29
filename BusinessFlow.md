## Task 2.1: Define Business Flow ##

> In this task, you are going to define the clinical pathway from when the patient enters the hospital until the patient is discharged. This is a simple application, so the clinical pathway will not hold a lot of the real time details.


## Procedure ##

1. Log in to the **IBM Process Designer** by providing your account User Name and Password.

2. The first time you start IBM Process Designer, it opens to the Process Center Console:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/ProcessCenterConsole.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/ProcessCenterConsole.png)

3. Open the application process that is assigned to you by the instructor, click the **Open in Designer** option for the process application that you want to access.

4. The following image shows the Designer interface and each functional area:
> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/DesignerInterface.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/DesignerInterface.png)

> You can use the Designer interface to develop process models and their underlying implementations, such as services. The following table describes each numbered area in the preceding image of the Designer interface in Lombardi Authoring Environment:

|1|	Click the appropriate button to open the interface that you want in Lombardi Authoring Environment, including the Optimizer and Inspector views.|
|:|:------------------------------------------------------------------------------------------------------------------------------------------------|
|2|	Shows the process application currently open. In this sample, the Billing process application is open.                                          |
|3|	Shows the types of library items included in the currently open process application. Click a category, such as Processes, to see the processes that you can open and alter.|
|4|	Shows the revision history for the currently open process application. In this sample, a user has recently added items to the open process.     |
|5|	Use the icons to create snapshots, access the Process Center Console, or access online assistance.                                              |
|6|	Shows the library item currently open for editing in the Designer. In this sample, the user has a process open and is working in the diagram, palette, and properties to create the steps of the process.|

5. Click on the plus sign in the **Processes** at the left pane, and under _Create New_ choose **Business Process Definition**, as shown below:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/newBusinessProcess.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/newBusinessProcess.png)

6. Name the new business process **Clinical-Pathway** and precess **finish**.

7. The process will open to start modelling the clinical pathway of the patient path in the hospital.

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/Clinical-Pathway.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/Clinical-Pathway.png)

> You will use the palette on the right to model the clinical pathway, here is a description of the symbols you are going to use:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/palette.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/palette.png)

8. Now using the palette above,you can start modelling your business process. You should drag and drop the symbols from the palette to the **Diagram** page.

9. The **Lane** will represent a participant in the clinical pathway. In our example, we have the following participants: patient,  transport, nurse, and doctor. The system will be represented in a **Lane** also. When you create the process as a default the **System** lane will be created as well as one participant that contains a **Start** and an **End** event. Therefore, you can change the participant that you are already have to the **Patient**, to do so click on the lane and change the Name form _Participant_ to _Patient_ as follows:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/PatientLane.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/PatientLane.png)

> Now add the a Lane for each participant, as follows:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/Lanes.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/Lanes.png)

> To manage the location of each Lane with respect to the other Lanes, you can click on the Lane and then **right-click** and choose from the list: **Move Up Lane**, **Move down Lane**, or **Edit**(if you want to edit the Lane).

10. Now that you created the participants, you can start manage the clinical path flow between them as the following:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/BusinessFlow.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/BusinessFlow.png)

The following are instructions of what you will need to do create the above clinical pathway:

> a. To connect events, activities, and decisions, you should use the _Sequence Line_. (Note: when you finished using the sequence lines, you can press on the **select** symbole in the palette or you can press **Escape** in the keyboard in order to get back to the anchor mode)

> b. To name a sequence line, click on the line you want to name and change the name and don't forget to check the visible option under the name field, see the following:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/LineName.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/LineName.png)

> c. To name events, activities, and decisions, you just follow the same as you did for the lanes. Click on the symbole you want to name and then change its **Name** field.

**Note**: Do not forgot to save what you did.

Now that you defined the Business Flow, you should create Business objects related to each participant in the clinical pathway process.