STARTING UP BUSINESS EVENTS SERVERS

  1. Remote Desktop into the Server IP 137.122.93.228 for school network.    (For the standalone: 192.168.1.134)
> > ◦	Enter log in credentials Username: Administrator,   Password: Exam!23


> 2.Go to Start -> Programs -> IBM WebSphere Business Events Server v7.0.1 and click on “Business Space”

> 3.On the login pop-up screen enter the credentials Username: aladdin\_baarah, Password:2611

> 4.Click on “Manage Spaces” tab and delete the existing projects space by clicking on “Actions” and Delete.

> 5.Create a new space, give it a name e.g. “Osler Demo”, “save” and click “Done”.

> 6.Click on the “Spaces” tab and select your newly created space from the list.

> 7.Click on “Edit Page”

> 8.Click on “Business Events Design” and “Business Events Tester” Widgets to add them to the Project.

> 9.In the “Business Events Design” Widget, Click on Project -> Open

> ◦	Choose Folder Shirely and

> ◦	Click on Osler Extended Scenario\_v4(Demo)

> ◦	Click on OK

> ◦	Wait until you receive confirmatory message “Project opened    successfully”

> ◦	Go to Runtime tab and click on “Delete repository assets”

> ◦	Go to Runtime tab again and click on “Publish to Runtime”

> ◦	Wait until you receive confirmatory message “Publishing project:  published successfully”

> Note: (If you face with this Error:  Error 404: ProxyServlet: /mum/nullassets , you can close the project and comeback to step 8)

10. In the “Business Events Tester” Widget, Click on “Restart Testing” button

11.In the file system navigate to C:\OslerProject\TestCase1\InputEvents folder
> ◦Empty the folder if it contains any files

12.Go to Start -> Programs -> IBM WebSphere Business Events Server v7.0.1 and click on “Connectors”

13.On the login pop-up screen enter the credentials

> ◦User Identity: aladdin\_baarah,

> ◦User Password:2611

> ◦Click on OK

14.The CEP is now ready to receive events.