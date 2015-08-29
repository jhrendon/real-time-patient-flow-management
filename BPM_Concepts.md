#Building a simple BPM Process using Lambardi

# Exercise 1.1 Download and install the Lambardi client #
1. Download the IBM Lambardi Client.
2. Access the Shared model on the university server.
3. Familiarize yourself with the Lambardi interface.

# Exercise 1.2  Create a Business Process Definition (BPD) #
When you model a process in the authoring environment, you first create a Business Process Definition (BPD). A BPD is a reusable model of a process that defines what's common to all runtime instances of that process model.

# Exercise 1.3 Build a Human Services #

Build a Human service when you want a step in your BPD to create an interactive task that process participants can perform in a web-based user interface, as shown in Figure 5. When you build Human services, you include Coaches, which are the web-based forms that provide process-related data to users and collect input from those users. Coaches enable you to easily add standard fields and controls such as radio buttons, drop-down menus, and so on.
The Ajax services that you build in Lombardi are subsequently bound to Coach controls to perform functions such as automatically populating drop-down lists and enabling type-ahead capability in input fields. You can use an Ajax service to pull data dynamically from a connected data source, such as a database.

# Exercise 1.4 Build an Integration Service #

Build an Integration service when you want to integrate with an external system to complete a task, as shown in Figure 6. For example, you can build an integration service that calls a web service to do some business logic. Integration services are the only services that can include web service integration and Java™ integration components.
Use General System services when you want to orchestrate other background services, manipulate variable data, generate HTML for a Coach, or perform other actions that don't require any integrations or business rules. General system services are likely to be called directly from a BPD or from a Human Service. General System services can include only basic service components such as scripts and cannot contain Coaches or integration components (web service integration or Java integration). General System services can be nested within any other type of service.
External activities enable you to create BPDs that include activities that are handled by systems outside of Lombardi. For example, you can build a custom application using the Lombardi web API to execute an activity, or step, in a BPD.
An Undercover Agent (UCA) is started by an event that can either be triggered by a message or on a specific schedule. When a UCA is started, it invokes a Lombardi service in response to the event. When you include a message event in a BPD, you must attach a UCA to the event to call the specified service. For example, when a message event is received from an external system, a UCA is needed to invoke the appropriate service in response to the message.
You can create and publish a web service to enable external applications to initiate a particular Lombardi service or set of services. Using the SOAP integration, external applications can also call the web service.

# Exercise 1.4 Build a Rule Service #

You can use a Rule service, shown in Figure 7, when you want a condition to determine what implementation is invoked. For example, when a certain condition evaluates to true, Lombardi implements a JavaScript expression that you provide. Rule services cannot include Java or web service integrations directly. You can call a Rule service from any other type of service and a Rule service can call other nested services.
Key performance indicators (KPIs) are measurements that Lombardi tracks at process runtime, storing results that you can use to analyze process and task performance in the Optimizer.
Service level agreements (SLAs) can be created based on standard and custom KPIs. SLAs enable you to establish a condition for one or more activities that triggers a consequence. When you run instances of your processes, SLA consequences do not trigger until the associated activity starts or completes.

# Exercise 1.5 Create Toolkits to Manage Reuse #

Toolkits are a collection of library items that can be used across multiple process applications in the Lombardi Authoring Environment. Lombardi enables process developers to re-use existing artifacts both within and across process applications through toolkits. For example, if you know several services already exist that include Coaches and other library items that other developers need, you can access and re-use those items by including them in a toolkit. Then, from your process application, you can add a dependency on the toolkit in which the library items reside. This enables you to pick one of the existing services when choosing the implementation for an activity. The items in the toolkit can also be used by other developers working in different process applications.
Authoring Environment users can create dependencies on toolkits in order to re-use the items within. When Toolkit items are updated, existing dependencies show that updates are available.
Library items in multiple toolkits can be shared across other toolkits, as well as process applications.