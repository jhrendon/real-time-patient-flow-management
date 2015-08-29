## Task 4.3: Create Business Objects ##

In this task, you will learn how to add business objects to you business process in our example is to add business objects(patient, nurse, doctor)to the Clinical-Pathway business process.

## Procedure ##

1. In the Designer interface for the Clinical-Pathway process, Click on the **plus** sign in the **Data** at the left pane, and under _Create New_ choose **Business Object**, as shown below:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/businessObject.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/businessObject.png)

2. Name the new business object **Patient** and precess **finish**.

3. Now you have to add fields/data to the **Patient** object such as: ID First Name, Last Name, Gender, Address, City, Province...etc.
> To do that click on **Add** in the parameters pane, and enter the name of the parameter and set the variable type by pressing on **System Data** and choosing the type of the parameter in the parameters properties pane, as the following:

> ![https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/patientParameters.png](https://real-time-patient-flow-management.googlecode.com/svn/trunk/images/patientParameters.png)

4. Add the other business objects the same way you added the patient object.

**NOTE:** Do not forget to save what you did.

After creating the business objects now you have to create the interface on the form that the patient will fill when he/she arrives at the Checkin Activity.