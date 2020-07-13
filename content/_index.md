+++
+++
<h2>Welcome to Kee</h2>
<p>This website will show you how to use Kee to easily and securely manage your passwords. This should take only a few minutes to complete and save you lots of time every day.</p>

<h3 id="kee-version-3-5-greater-heading">Step 1 of 4</h3>
<h3 id="kee-version-less-than-3-5-heading" style="display: none">Step 1 of 5</h3>

<p>Kee will remember your sign-in information so you don't have to.</p>

<div class="instruction">
<p>Pretend that you have an account on this fake website with these sign-in credentials:</p>
<p class="instruction-callout">Username: <i>user</i><br/>
Password: <i>1234</i></p>
<p>Type these into the boxes ("form fields") below and then press the "Complete step 1" button.</p>
</div>

<form action="/step2" method="get" id="login">
	<label for="username">Username:</label><input type="text" name="username" id="username" autocomplete="off"/>
	<label for="password">Password:</label><input type="password" name="password" id="password" autocomplete="off"/>
	<input type="submit" value="Complete step 1"/>
</form>

<div class="info"><div><img src="/images/glasses-solid.svg" width="40" height="40"/></div><div><p>You can still go through the tutorial if you have made customisations to Kee options but some instructions might not make perfect sense.</p></div></div>

<div>If you're having trouble and any advice at the top of the page is not helpful, you can find detailed <a href="https://forum.kee.pm/t/troubleshooting/560">troubleshooting advice in the manual</a>.</div>

<!-- PROTECTED BY CSP. Update hashes in netlify.toml if making changes sha256-bNrMc4tnLK5q2mPW8opMyPq0Qbr87O40G14RsGdap8o= -->
<script type="text/javascript">
document.addEventListener("KeeFoxAddonStateTransferEvent", function(event) {

	var state = document.getElementsByTagName("KeeFoxAddonStateTransferElement")[0].getAttribute("state");
	var data = JSON.parse(state);

	if (parseFloat(data.version) < 3.5) {
        document.getElementById("kee-version-less-than-3-5-heading").style.display = "block";
		document.getElementById("kee-version-3-5-greater-heading").style.display = "none";
		document.getElementById("login").action = "/step2-old";
    }
}, false);
</script>