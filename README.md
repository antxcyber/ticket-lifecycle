<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket - Ticket Lifecycle Examples</h1>
This tutorial outlines the lifecycle of a ticket from intake to resolution within the open-source help desk ticketing system osTicket. This tutorial assumes you have completed both the <a href= ""> installation </a> and <a href = "">configuration</a> of osTicket

</br>

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Machines/Compute)</li>
  <li>Remote Desktop</li>
  <li>Internet Information Services (IIS)</li>
  <li>osTicket</li>
</ul>

</br>

<h2>Operating Systems Used </h2>
<ul>
  <li>Windows 10</li>
</ul>

</br>

<h2>Ticket Lifecycle Stages</h2>
<ol>
  <li>Intake</li>
  <li>Assignment & Communication</li>
  <li>Working the Issue</li>
  <li>Resolution</li>
</ol>

</br>

<h2>Lifecycle Stages</h2>



<h3>Intake</h3>

<p>
  <ul>
    <li>From the <b>End User's</b> side (Karen Karen), they create a ticket through osTicket's <a href = "http://localhost/osTicket/ ">local host site</a> and fill their information, select a Help Topic</li>
    <ul>
      <li><img width="643" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/c7a0a06d-d35e-4e1a-9571-bb9e2de00c6d"></li>
    </ul>
    <li>The End User then writes ticket through the <b>Issue Summary</b> and adds a subject and details of the ticket much similar to writing an email</li>
    <ul>
      <li>In this example, Karen creates the ticket under the Help Topic of a Business Critcal Outage (made from our configuration of osTicket) explaining the mobile banking application is suffering a 404 error</li>
      <li><img width="643" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/c26a7c90-70ed-437d-a145-fb0518d951fc"></li>
    </ul>
    <li>Karen then creates the ticket and is sent to <b>Agent</b> Jane Doe (which we've set as Supreme Admin is able to see all incoming tickets in the configuration tutorial) who views it from the <a href = "http://localhost/osTicket/scp/login.php">local help desk login</a></li>
    <ul>
      <li><b>Note</b>: Priorities have not been set for other incoming tickets such as ticket #951342 where end user Ken is requesting an upgrade to Adobe Reader. SLA plans need to be set for these tickets hence why they are all under the priority state of "Normal"</li>
      <li><img width="735" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/45b3e16c-5786-4d3b-8617-364020b42941"></li>
    </ul>
  </ul>
</p>

<h3>Assignment & Communication</h3>

<p>
  <ul>
    <li>The Business Critical Outage ticket by Karen numbered 282733 is assigned to the Agent Jane Doe. From Jane's perspective, this is how the ticket first looks.</li>
    <ul>
      <li>The Agent is able to message the End User through the <b>Ticket Thread</b> located in the bottom of the ticket page</li>
      <li><img width="735" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/c0b51a79-e02c-4d9e-beac-150fed10f9d4"></li>
    </ul>
    <li>By going to the link next to <b>Priority</b>, you are able to set the priority of the ticket to Low, Normal, High, or Emergency</li>
    <ul>
      <li><img width="496" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/7474573d-6098-42a2-a0fc-d5a9e7f8c6dc"></li>
    </ul>
    <li>By going to the greyed out link --Unassigned-- next to <b>Assigned to</b>, you can assign the ticket to a Team or Agents. Note if we were to assign it to an Agent outside of Agent Jane's Department, it will not appear in their feed.</li>
    <ul>
      <li><img width="496" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/7e6a0134-415d-4953-9028-1d3e1dce6c64"></li>
    </ul>
    <li>By going to the link next to <b>SLA Plan</b> to set the SLA Plan from Default SLA to one our SLA Plans we have created in configuration. For this Business Critical Outage ticket, it'll be set to SEV-A</li>
    <ul>
      <li><img width="496" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/55ce6e44-4aa4-41f8-9b89-b862c3be72ce"></li>
    </ul>
    <li>By going to the link next to <b>Department</b> to set the Department. For this Business Critical Outage ticket, it'll be set from Support to System Administrators</li>
    <ul>
      <li><img width="496" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/a1b63a88-4287-4358-8d42-e468a08ffe2f"></li>
    </ul>
    <li>The Ticket Thread is updated when we make the changes to ticket</li>
    <ul>
      <li><img width="720" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/f38495c6-cb88-448d-8c87-89e020fef731"></li>
    </ul>
    <li>The Agent can message the End User through the Ticket Thread to update the User on the ticket as well as set the status of the ticket (which is left as <b>Open</b> since we need to work it out)</li>
    <ul>
      <li><img width="720" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/45df117f-ff42-464e-875e-e79d665228e6"></li>
    </ul>
  </ul>
</p>

<br />

<h3>Working the Issue and Resolution</h3>

<p>
  <ul>
    <li>Following from our Assignment of Departments and Communication with the End User, the issue in our hypothetical Critical Banking Outage ticket has been resolved thanks to System Engineering. The Agent should now communicate the issue with the End User using the Ticket Thread and set the status of the ticket from Open to <b>Resolved</b>. Upon posting the Reply, the ticket is <b>Closed</b>.</li>
    <ul>
      <li><img width="720" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/00ad13cb-7f8d-4261-8ce0-4708b2dd402f"></li>
    </ul>
    <li>Closed tickets can be found under the Closed section in our Tickets tab, where information and status of the tickets are archived. It is good practice for Agents to study Closed tickets to improve their experience in working with them</li>
    <ul>
      <li><img width="720" alt="image" src="https://github.com/antxcyber/ticket-lifecycle/assets/148983947/df8ba6ec-afcf-4a3b-b76a-72b3fcb579e4"></li>
    </ul>
  </ul>
</p>

<br />
