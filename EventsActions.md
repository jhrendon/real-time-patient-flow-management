## Task 4.1: Create Events and Actions ##
Events are the input for the CEP. Actions are the output. Typically, a CEP tool would receive events from multiple sources, and produces actions that are routed to possibly multiple destinations.

In this exercise, you will define an event called _BPMRegistrationRequest_ to represent the registration request received from **BPM**, and an action called _RegisterPatient_ which contains the information from the event that is required by the Hospital to register the patient.

We will be using IBM WebSphere Business Events V7.0.1.


## Procedure ##

1. Start Design Data: **click Start** > **Programs** > **IBM WebSphere Business Events V7.0.1** > **Design Data**.

> In Design Data, there are three main sections of the window:
  * Data Sources (which is collapsed when you first open Design Data, and which you do not use in this tutorial)
  * Intermediate Objects
  * Touchpoints

2. Define the _BPMRegistrationRequest_ event:

> a. Right-click anywhere in the left pane of the **Touchpoints** section
> > of the window, then click **Insert Touchpoint**

> b. In the Insert Touchpoint dialog, type BPM, then click **OK**.

> Touchpoints represent the system from which events are received or to which actions are sent. The BPM touchpoint represents the insurance company website which sends events to WebSphere Business Events. You define all events and actions under the touchpoint with which they are associated.

> c. Right-click the **BPM** touchpoint, then click **Insert Event** > **Blank**

> d. In the Insert Event dialog, type **BPMRegistrationRequest**, then click **OK**.

> You have defined that the business event received from the website contains information in the structure of the event known as BPMRegistrationRequest.

> Now you must define what that structure is, by defining event objects in the event.

> e. Right-click the **BPMRegistrationRequest** event, then click **Insert Event Object** > **Blank**

> f. In the Insert Event Object dialog, type **RequestDetails**.

> The RequestDetails event object contains fields that represent the discrete pieces of information in the BPMRegistrationRequest event; for example, the first name, last name, and OHIP number.

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/RequestDetailsObject.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/RequestDetailsObject.png)


> g. To add a field to the event object, right-click the **RequestDetails** event object, then click **Insert Event Object Field**

> h. In the Insert Field dialog box enter the following details, then click **OK**.
    * In Name, type First Name
    * In Data type, click String
    * In Description, type The first name of the patient.

> The field that you just created is displayed in the right pane.

> i. Click the field (![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/Firstnamebutton.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/Firstnamebutton.png)) to expand it and see the details that you entered when you created it. The Data type field specifies that the First Name field contains String data (alphanumeric data).

![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/FirstNameField.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/FirstNameField.png)

> j. Add the other fields listed in the following table in the same way. As an alternative, you can click once in the right pane, then to add each field by pressing the Insert key:

> Table 1. Other fields to be added.
|Name|	     Data type|        Description|
|:---|:--------------|:------------------|
|First Name|	String        |	The patient's first name.|
|Last Name|	String        |	The patient's last name.|
|OHIP Number|     Integer   |	The patient's OHIP number.|

![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/EventObjectFields.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/EventObjectFields.png)

> You have defined an event called **BPMRegistrationRequest** that contains six fields in an event object called **RequestDetails**.

> Next, you define the **RegisterPatient** action.

> The **RegisterPatient** action is sent to the BPM every time WebSphere Business Events receives a **BPMRegistrationRequest** event. The **RegisterPatient** action must, therefore, contain the information of the patient so that it can be sent to the BPM.

> You define actions in a similar way to defining events.

3. Define the **RegisterPatient** action:

> a. Under the **BPM** touchpoint, insert an action called **RegisterPatient** (right-click the BPM touchpoint, then click Insert Action > Blank).

> For now, the **RegisterPatient** action contains the same information as the **BPMRegistrationRequest** event. In the next step, you define that the information in the **BPMRegistrationRequest** event is copied into the **RegisterPatient** action, to be sent to the BPM.

![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/BPMAction.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/BPMAction.png)

4. Define that the information in the **BPMRegistrationRequest** event is used in the **RegisterPatient** action:

> Strictly speaking, it is actually the information in the **RequestDetails** event object that is copied to the **RegisterPatient** action, where the information is structured in an action object called **RequestDetails**.

> Between events (incoming to WebSphere Business Events) and actions (outgoing from WebSphere Business Events) are intermediate objects.

> Intermediate objects provide abstract representations of the information, or data, that is received in the event and which can be obtained from elsewhere or through calculations. In this exercise, you create a single intermediate object which contains the details of how the information in the **BPMRegistrationRequest** event is copied to the **RegisterPatient** action.

> a. In the **Touchpoints** section, click the **RequestDetails** event object, then drag the **RequestDetails** event object to anywhere in the left pane of the Intermediate Objects section.

> An intermediate object called **RequestDetails** is automatically created, containing all the same fields as the **RequestDetails** event object.

> Each of the fields listed for the intermediate object is decorated with an event icon to show that it is associated with a field in an event object. Similarly, all the fields listed for the **RequestDetails** event object are now decorated with an intermediate object icon to show that it is associated with a field in an intermediate object.

![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/intermediateobject.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/intermediateobject.png)

> In the **Touchpoints** section, an object constructor has been automatically added under the **RequestDetails** event object. The object constructor contains the details of how the fields in the event object are associated with the fields in the intermediate object.

> i. Click the **RequestDetails** object constructor. The fields in the RequestDetails intermediate object are displayed.

> ii. Expand the First Name field to display its properties. The properties state that the First Name field of the intermediate object is associated to the First Name field of the event object. Each of the fields shows similar relationships.

![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/constructor.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/constructor.png)

> b. Click the **RequestDetails** intermediate object, then drag the RequestDetails intermediate object to the **RegisterPatient** action. An action object called **RequestDetails** is automatically created in the **RegisterPatient** action.

> The icons that decorate each of the fields of the action object indicate that the field is associated with a field in the intermediate object. If you expand one of the field of the action object to display its properties, you can see exactly which field in the intermediate object is associated with the field of the action object.

![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/requestDetailsActionObject.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/requestDetailsActionObject.png)

> You have now defined the **BPMRegistrationRequest** event and the **RegisterPatient** action, and specified how the information in the event is also to be contained in the action.

> Although the intermediate object seems like an unnecessary step in this exercise, in most applications that you build, the intermediate object contains information from more than one incoming event and the outgoing actions probably do not have a one-to-one relationship with the incoming events. Also, in an intermediate object, you can perform calculations by using JavaScript, or get additional information from data sources such as a database or get the result of the evaluation of additional business rules from WebSphere ILOG JRules.

> Next, you edit the event and action definitions to specify how they connect to the systems outside of WebSphere Business Events.