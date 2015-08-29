# IBM BPM Process Designer #

The IBM BPM Process Designer(PD) is the development time tooling used to
design, model and build processes. It is implemented under the covers using the Open Source technology called Eclipse but has a very non-Eclipse like skin applied over it.
IBPM PD can be downloaded from the IBPM Process Center and installed on a user's Windows based workstation.

At a high level IBPM PD allows us to describe business processes using the BPMN notation. The processes are "drawn" visually on the screen canvas and the technical skills needed to achieve this task are as low as can possibly be made.

# How to install BPM Process Designer? #

Following steps illustrate the installation of IBM BPM Process Designer.
**Step1:** Run the batch file "installProcessDesigner\_admin.bat" from the folder IBM Process Designer.
![http://i.imgur.com/2HRfCJx.png](http://i.imgur.com/2HRfCJx.png)

![http://i.imgur.com/WaH5jm0.png](http://i.imgur.com/WaH5jm0.png)

![http://i.imgur.com/TfqqYSv.png](http://i.imgur.com/TfqqYSv.png)

**Step2:** IBM Process Designer will be successfully installed. After installing IBPM, the IBPM Process Designer can be launched from the Windows start menu.

![http://i.imgur.com/H2RHPsc.png](http://i.imgur.com/H2RHPsc.png)

![http://i.imgur.com/npSsS1l.png](http://i.imgur.com/npSsS1l.png)

**Step3:** Provide valid username and password.
Once launched, the IBPM PD will ask for authentication information with a userid/password pair.
The default/initial administrator userid and password are commonly:
admin/admin.

![http://i.imgur.com/frqujqK.png](http://i.imgur.com/frqujqK.png)

With successful login, you will see the existing projects/process Apps on the Process Apps page. Note that the currently logged in user is shown in the title of the window.

In the IBPM PD interface there are the following major "views" only one of which is shown at a time:

• Process Apps – Selection of available/existing Process Apps

• Toolkits – Selection of available/existing Toolkits

• Servers – List of the Process Server instances

• Admin – Administration tasks

• Designer – Design/construction of a solution

• Inspector – Debugging/monitoring a solution (usually in test)

• Optimizer – Examining performance characteristics


# Troubleshooting BPM #

**Step1:** Open CMD in administrator mode
(Search cmd in start menu, right click, "run in administrator mode")

**Step2:** Change directory (cd) to this folder **"C:\IBM\BPM\v8.0\profiles\ProcCtr01\bin"**

**Step3:** Type **startServer.bat server1**