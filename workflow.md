# Workflow
![Workflow](https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/Workflow.png?raw=true)

<table cellspacing="0" cellpadding="0" border="0">
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/User-blue.png?raw=true" width="48" height="48"/></td>
    <td>Developer, who is responsible for a task. When starting a new task, Developer will "checkout" a (feature) branch from latest 'develop' branch</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/User-red.png?raw=true" width="48" height="48" /></td>
    <td>Reviewer and Tester, who reviews or tests on a task, Reviewer and Tester can be same or different one. Tester only do testing on 'feature' branch on local machine or test server</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/User-yellow.png?raw=true" width="48" height="48"/></td>
    <td>Publisher, who is responsible to merge code into 'master' branch and release on live server.</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/blue-box.png?raw=true"/></td>
    <td>Big blue box (as container) is a phase in Workflow. There are 7 phases in a cirle of task's life: Start -> Coding -> Committing -> Pull Request -> Reviewing -> Testing -> Release</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/solid-box.png?raw=true"/></td>
    <td>Solid bordered box, is a REQUIRED step in a phase</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/dashed-box.png?raw=true"/></td>
    <td>Dashed bordered box, is a EXPANSION Step in a phase, this step will be executed in case of bugs or conflicts occurred.</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/yellow-box.png?raw=true"/></td>
    <td>This is a normal step in a phase</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/red-box.png?raw=true"/></td>
    <td>We can understand that this is unexpected step but we must do :D</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/green-box.png?raw=true"/></td>
    <td>The target step in a phase, we can understand that the target step in a phase is the condition for beginning of next phase</td>
  </tr>
  <tr>
    <td>
      <img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/user-box.png?raw=true"/>
      <img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/user-box-1.png?raw=true"/>
    </td>
    <td>Person icon in the upper right corner of the box refers a person who is responsible for a task or phase.</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/forward-arrow.png?raw=true"/></td>
    <td>(Back or white arrow) Forward</td>
  </tr>
  <tr>
    <td><img src="https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/images/revert-arrow.png?raw=true"/></td>
    <td>Revert</td>
  </tr>
</table>

Next:
[Our rule about working with GIT](https://github.com/EvolableAsiaDevelopment/eva-operation-rule/blob/master/github-operation-rule.md)
