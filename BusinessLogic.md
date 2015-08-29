## Task 4.4: Building the business logic ##

When the patient requests to register, an instance of the !BPMRegisterationRequest event is received by WebSphere Business Events. WebSphere Business Events then processes the information in that event according to the business logic that has been defined. In this exercise, every time WebSphere Business Events receives an instance of the BPMRegisterationRequest event, WebSphere Business Events sends an instance of the RegisterPatient action to BPM so that the patient will be registered.

In this exercise, you define the simple business logic that sends the RegisterPatient action in response to incoming instances of the BPMRegisterationRequest event

## Procedure ##

1. Setting up the Design tool in Business Space: If you have already used the Design tool in Business Space, you can skip this step.

a. Start Business Space. Click **Start** > **Programs** > **IBM WebSphere Business Events V7.0.1** > **Business Space**.

> If security is enabled, the first time that you open Business Space, you might be prompted to accept a security certificate.

b. Enter a user ID and password to log in to Business Space.

> By default, security is enabled so that only authorized users can access the application building tools (like Business Space or the User Console and Administration UIs). The user ID that you use determines whether you can view and edit the project in the Business Space project store. Therefore, use the same user ID and password that you used to save the project from Design Data.

c. Create your own business space in Business Space by using the WebSphere Business Events template.


  1. From the Business Space Home page, click **Manage Spaces** > **Create Space**.

> 2. Enter the Space name as **PatientRegisterationTutorial** and the Space description details.

> 3. Select the Create a new space using a template check box and open the template selection list. The following screen capture shows this section of the Create Space page.

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/creatingspace.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/creatingspace.png)

> 4. When you have selected the options you want to use in your business space, click **Save**.

> 5. The Space Manager page is displayed showing the list of business spaces you can access. Click the name of the business space you created.

> 6. The business space opens and the WebSphere Business Events widgets are displayed in the tabs below the business space name.

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/businessSpace.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/businessSpace.png)

d. To build the business logic, you use the Business Events Design widget.

e. For testing the business logic, you use the Business Events Tester widget. The business space now contains both widgets so that you can build and test the business logic for the application.


2. Open your project in the Design tool in Business Space:

> In Design Data, you saved the data model in the project store. Saving to the project store means that you can easily open the project in Design in Business Space to add the business logic to it.

> a. In the Business Events Design widget, click **Project** > **Open**. If you logged in to Business Space with the same user ID that you used when you saved the project from Design Data, then in the Open Project dialog, the folder that contains the project is opened by default.

> b. If you logged in to Business Space with a different user ID from when you (or another user) saved the project from Design Data, then in the Open Project dialog, in the **Folder** pane, click the name of the folder in which the _PatientRegisterationTutorial_ project was saved from Design Data. In the **Project** pane, click **PatientRegisterationTutorial**.

> c. Click **Open**. The project is opened in Design.

> In the Current project pane, you can see the tree-like organization of the assets that you have created so far (the !BPMRegistrationRequest event definition, the RegisterPatient action definitions, and the RequestDetails intermediate object), and place holders for interaction sets and filters.

3. Create the RegisterPatient interaction set:

> An _interaction_ set contains the business logic that WebSphere Business Events uses to process incoming instances of events. An interaction set always contains a reference to an event definition. When an instance of that event is received by WebSphere Business Events, the interaction set starts processing the event according to the business logic in the interaction set. Interaction sets can contain more than one piece of logic that processes the event. Each piece of logic is known as an _interaction block_. In this exercise, you create just one interaction block. Finally, interaction sets often contain a reference to at least one action definition, which is sent according to the outcome of the event processing.

> Typically an interaction block contains one or more _filters_, which are conditions against which the event is evaluated. You add the filters to the interaction block in this interaction set later. In this exercise, the interaction set does not contain any filters so that you can test that the data model you created works.

> a. In Design, click the _New Interaction Set_ button on the toolbar.
A new interaction set template is displayed in the editor pane. In the Current project pane, the new interaction set has been added to the list of assets under the Interaction Sets category. All assets are organized in folders. A folder called New Folder has been created to contain the interaction set. You can rename the folder if you like; the name of the folder has no effect on how your project works. The use of folders allows you to group assets together based on the requirements of your projects.

> b. Name the interaction set Register Patient by replacing the text _New Interaction Set_ with Register Patient.

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/interactionset.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/interactionset.png)

> c. Set the **!BPMRegisrationRequest** event definition as the event that is processed by this interaction set by clicking the gray box that says **Click to select an event**, then click **BPM** (which is the touchpoint on which you defined the event in Design Data), then click **!BPMRegisrationRequest** (the event you defined in Design Data).

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/interactionset1.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/interactionset1.png)

> d. Set the **RegisterPatient** action definition as the action that is sent to the Marketing department every time the BPMRegistrationRequest is received from a potential customer by clicking the gray box that says **Click to select an action**, then click BPM (the touchpoint on which you defined the action), then click RegisterPatient.

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/interactionset2.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/interactionset2.png)

> e. Click another asset in the tree to save the changes you have made, then click the **Register Patient** interaction set to view it in the editor.

> In the editor, the interaction set is shown as one block shaded blue (in which you entered the name of the interaction set and set the event), and a second block that is indented slightly and shaded green (in which you set the action). As there are no filters in the interaction block that you just created, the text in the middle of the interaction block says **Always**, which indicates that the RegisterPatient action is always sent in response to receiving the BPMRegistrationRequest event.
> Notice, too, that there are two instances of the word **Immediately** displayed in the interaction block. The first instance, at the start of the interaction block, indicates that the interaction block processes the event immediately it receives it. The second instance, indicates that the RegisterPatient action is sent immediately on processing the event. You add delays and additional actions, as well as filters, in later exercises.

> The project is now ready to publish and test.