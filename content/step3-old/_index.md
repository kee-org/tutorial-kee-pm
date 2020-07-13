+++
+++
<h2>Filling</h2>

<h3>Step 3 of 5</h3>

<p>Kee will monitor the web pages you load and will automatically fill sign-in forms with your sign-in details for the website.</p>

<p id="stage2CheckPending">[ Checking previous step. Please wait... ]</p>
<p class="hidden" id="stage2CheckSuccess">You can see your username and password have been filled into the form at the bottom of this page.</p>
<p class="error hidden" id="stage2CheckFail">It looks like Kee did not fill in the form below. You probably did not save the login entry in the previous step. Please go back to try again or the next step will not make sense.</p>

<div class="info"><div><img src="/images/glasses-solid.svg" width="40" height="40"/></div><div><p>Kee has many options to adjust this automatic form filling behaviour. You can change the behaviour for all or just some of your credentials and even block Kee from filling in forms in specific web pages if you have advanced requirements. You can also store more than one entry for each website if required.</p></div></div>

<p>Use the sign-in form below to try out the two Kee features you'll need to change your password on a website: Generating a new secure password and storing the updated information.</p>

<div class="instruction"><ol>
	<li>Generate a new password. Either:<ul style="list-style-type: lower-roman">
		<li style="list-style-type:circle">Click the "Generate new password" button on the Kee menu (click the Kee button on your toolbar)</li>
		<li style="list-style-type:none; font-size: 1.25em; padding-left:50px">OR</li>
		<li style="list-style-type:circle">Use the keyboard shortcut: Ctrl-Shift-4</li></ul></li>
	<li>Paste the new password into the password field below</li>
	<li>Click "Complete step 3".</li>
    </ol>
</div>

<form action="/step4-old" method="get"><br/>
    <label for="username">Username:</label><input type="text" name="username" id="username"/><br/>
    <label for="password">Password:</label><input type="password" name="password" id="password"/><br/>
    <input type="submit" value="Complete step 3"/>
</form>

<h4>More information about changing website passwords</h4>

<p>A typical password change process follows this pattern:</p>
<ol>
	<li>Load the website's "change password" page</li>
	<li>Ask Kee to generate a new secure password, paste it into the website's "new password" form field and save the change</li>
	<li>Go to the website's sign-in page (Kee will auto-fill it with the old password)</li>
	<li>Paste the new password over the old one</li>
	<li>Sign in to the website and then tell Kee to remember the change for next time</li>
</ol>

<script>
checkTimer = setInterval(function () {
	if (document.getElementById("username").value && document.getElementById("password").value) {
		document.getElementById("stage2CheckPending").classList.add("hidden");
		document.getElementById("stage2CheckSuccess").classList.remove("hidden");
		clearInterval(checkTimer);
		clearTimeout(checkTimerEnd);
	}
}, 250);

checkTimerEnd = setTimeout(function () {
	document.getElementById("stage2CheckPending").classList.add("hidden");
	document.getElementById("stage2CheckFail").classList.remove("hidden");
	clearInterval(checkTimer);
}, 3000);
</script>
