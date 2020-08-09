# Business Card Reader Sample for Power Apps
This application is built with PowerApps using AI Builder service. It displays informations like "Name", "Company" and "Email" from business cards that are saved as image files(png, jpg)

<b>To use the sample project</b>:<br/><br/>
1- Enable AI Builder service(Trial or Subscription needed)<br/>
2- Import/Open the .msapp package that is shared in this repo<br/>
3- Test it!<br/>
4- If the marking arent correct, update as you see fit 🙂 <br/>

<br/><br/><br/>
<h1>Demo Screen</h1>
<br/><br/><br/>
<img src="https://raw.githubusercontent.com/iberpoint/BusinessCardReaderforPowerApps/master/BusinessCardReaderScreenShot.png" />

<br/><br/><br/>

<h2>Sample Code</h2>
<br/><br/>
<span>Getting Email:</span>
<code>Match(LookUp(TextFromAI,StartsWith(Text,"Email:") || StartsWith(Text,"Email: "),Text),":(?<email>" & Match.Email & ")").email</code>
  
<br/><br/>
<span>Getting Name:</span><br/>
<code>Last(Split(LookUp(TextFromAI,StartsWith(Text,"Name:") || StartsWith(Text,"Name: "),Text),": ").Result).Result</code>

<br/><br/>
<span>Getting Company:</span><br/>
<code>Last(Split(LookUp(TextFromAI,StartsWith(Text,"Company:") || StartsWith(Text,"Company: "),Text),": ").Result).Result</code>
