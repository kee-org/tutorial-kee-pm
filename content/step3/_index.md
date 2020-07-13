+++
+++
<h2>Filling</h2>

<h3>Step 3 of 4</h3>

<p>Kee will monitor the web pages you load and will automatically fill sign-in forms with your sign-in details for the website.</p>

<p id="stage2CheckPending">[ Checking previous step. Please wait... ]</p>
<p class="hidden" id="stage2CheckSuccess">You can see your username and password have been filled into the form at the bottom of this page.</p>
<p class="error hidden" id="stage2CheckFail">It looks like Kee did not fill in the form below. You probably did not save the login entry in the previous step. Please go back to try again or the next step will not make sense.</p>

<div class="info"><div><img src="/images/glasses-solid.svg" width="40" height="40"/></div><div><p>Kee has many options to adjust this automatic form filling behaviour. You can change the behaviour for all or just some of your credentials and even block Kee from filling in forms in specific web pages if you have advanced requirements. You can also store more than one entry for each website if required.</p></div></div>

<div class="instruction"><p>Click the "Complete step 3" button
</p></div>

<form action="/step4" method="get">
    <label for="username">Username:</label><input type="text" name="username" id="username" autocomplete="off"/>
    <label for="password">Password:</label><input type="password" name="password" id="password" autocomplete="off"/>
    <input type="submit" value="Complete step 3"/>
</form>

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
