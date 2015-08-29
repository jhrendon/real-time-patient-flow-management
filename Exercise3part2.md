Define the PolicyPurchased event:
After a customer has requested a quotation for car insurance, if the customer purchases the insurance policy, an instance of the PolicyPurchased event is received by the policy system of the insurance company.

Because the policy system is a separate system from the IT systems of the Marketing department, and the website, you must create a new touchpoint to represent the policy system. You then define the PolicyPurchased event on the PolicySystem touchpoint.

In Windows Explorer, create the following folder:
C:\tutorial\Events
If you want to generate and send events manually, put WebsiteQuoteRequest event files into this folder, and the file system action connector inputs them into WebSphere® Business Events. However, in this tutorial, you use the Business Events Tester widget to generate and send events. You must still create this folder, to match the configuration of the file system action connector.
In Design Data, create a new touchpoint called PolicySystem.
On the PolicySystem touchpoint, create an event called PolicyPurchased.
Create the event objects for the PolicyPurchased event definition by mapping the Customer intermediate object, and then the Car intermediate object to the PolicyPurchased event.
Right-click the PolicyPurchased event, then click Event Properties.
In the Properties dialog, click the Connection tab, then click File System Connection.
In the File Event Connection dialog, in the Format field, click Connector Packet.
Click Configure to open the Server dialog.
In the Directory field, type:
C:\tutorial\Events
In the File Pattern field, type:
PolicyPurchased**.xml
Click Test to ensure that the folder is available.
Click OK to close the dialog.
In the Contact Frequency field, type 0.1. This means that the file system connector checks for events every 6 seconds (0.1 minutes), which is useful when testing the interaction set later.
Click OK to close each dialog.
Save the project. Because you are working on a project that is in the project store, when you click Save Project, the project is saved directly to the project store.
You have now defined a PolicyPurchased event. The PolicyPurchased event definition contains the same fields of data as the WebsiteQuoteRequest event definition.**

Next, you can create a filter to check whether the PolicyPurchased event has been received already.