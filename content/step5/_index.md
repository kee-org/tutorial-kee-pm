+++
+++
<h2>Further reading</h2>

<p><strong>Great! You now know enough to use Kee effectively every day.</strong> You can look in your password manager now to view the entry you have just saved and updated.</p>

<p>Important release news and new features will be announced on the <a href="https://forum.kee.pm">community forum</a> so we recommend joining or periodically checking the <a href="https://forum.kee.pm/c/project-news">project news category</a>.</p>

<p id="donateCTA">Want to show your appreciation of Kee? You can subscribe to <a href="https://keevault.pm">Kee Vault</a> or <a href="https://forum.kee.pm/t/how-can-i-donate/214">donate via Paypal or cryptocurrency</a>. Thanks!</p>

<p>Kee development is hosted at <a href="https://github.com/kee-org/browser-addon">GitHub</a> - please get involved!</p>

<script type="text/javascript">
document.addEventListener("KeeFoxAddonStateTransferEvent", function(event) {

	var state = document.getElementsByTagName("KeeFoxAddonStateTransferElement")[0].getAttribute("state");
	var data = JSON.parse(state);

	if (data.sessionNames.some(name => name.toLowerCase() === "event")) {
        document.getElementById("donateCTA").style.display = "none";
    }
}, false);
</script>
