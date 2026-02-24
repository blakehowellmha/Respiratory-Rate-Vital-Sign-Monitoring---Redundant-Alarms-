<h1>Respiratory Rate - Artifact Prevention</h1>

<h2>Description</h2>
Code prevents false alarms due to patient movement artifact or sensor problems by comparing oxygenation status to respiratory rate of patient before notifying clinician of low respiratory rate. In other words, a low respiratory rate with a correlating low oxygenation will trigger a notification, but a low respiratory rate alone will not. This can be used as an early warning system for apneic episodes or cardiopulmonary arrest while mitigating false alarms due to patient movement or a insecure sensor. Thus, improving clincian efficiency and reducing alarm fatigue. All high respiratory rate notifications will notify despite oxygen level. This is because high respiratory rates can be associated with low or high oxygenation status depending on the situation.
<br />


<h2>Languages and Utilities Used</h2>
 
- <b>Python</b>

<h2>Environments Used </h2>

- <b>VS Code</b>


<h2>Overview</h2>
Utlizing variables I created the patient location, alarm parameters, and the patient's vital signs. Then I utilized an infinate loop, simple if elif statements, along with f-strings to achieve the desired output notifications using the print function. All conditions are based off the patient's vital sign readings. Of course, the room number can be ammended. The alarm parameters are based off clinical norms, but are customizable depending on patient.
<img width="1514" height="751" alt="Overview RR 5" src="https://github.com/user-attachments/assets/9f85f980-136c-4b0d-abb2-6b93c4594fe9" />

<h2>Walkthrough</h2>
<b>1.	Set Up & Alarm/Notification Thresholds: </b>
Normal Respiratory Rate (RR) is typically 12-20 breaths/min. Alarm parameters can be tailored to system or patient.
<img width="1512" height="268" alt="setup RR 1" src="https://github.com/user-attachments/assets/a2468c17-e2d4-49c9-aaff-c12900edc517" />

<b>2.	Startup Console Message for Continuous Monitoring: </b>
<img width="1517" height="74" alt="Startup RR 2" src="https://github.com/user-attachments/assets/74222671-7179-4b10-8385-59dd0f2c1567" />

<b>3.	Infinite Monitoring Loop: </b>
Simulated patient vital readings provide a means for testing. Replace later with real sensor input from pulse oximeter or radar device.
<img width="1499" height="113" alt="Loop RR 3" src="https://github.com/user-attachments/assets/e57c171a-e92c-4c4f-8ecb-e94c08e9cb36" />

<b>4.	Alarm Logic:</b>
If-elif checks – high Resp_Rate always alerts; low Resp_Rate requires SpO2 confirmation. Utilizing imported time and time.sleep, patient readings refresh every 5 seconds.
<img width="1518" height="334" alt="logic RR 4" src="https://github.com/user-attachments/assets/e5dabc33-77ff-4afb-8faa-6ba4e3851962" />

<b>Why This Reduces False Alarms:</b>
- Isolated Resp-Rate = 6 with SpO2 = 98% >>> no low-RR alarm (likely artifact).
- Resp_Rate = 6 with SpO2 = 84% >>> triggers dangerously low RR alert (likely real hypoventilation).
- Any SpO2 <90% alerts independently (hypoxemia is dangerous even with normal RR).



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
