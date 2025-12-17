<h2>Overview</h2>
This collection of scripts is intended to update and maintain Mac OS systems on a network.
<p></p>
<h2>File information</h2>
<p></p>
<h3>update_os</h3> This is the original script to prune user accounts which have been dormant beyond 30 days and update Mac OS to the latest stable release. After the update process, the machine will restart. This script is also used in <i>update_all</i> and <i>parallel_updates</i>.
<br>
<h3>update_p-fv</h3> This script is the same as <i>update_os</i> but adds a function to disable notifications to enable FileVault.
<br>
<h3>update_all</h3> This is a script that sequentially processes updates via <i>ipaddresses.txt</i> and applies the <i>update_os</i> script to each one.
<br>
<h3>parallel_updates</h3> This is a script that processes 5 parallel updates at once via <i>ipaddresses.txt</i> and applies the <i>update_os</i> script to each one.
<br>
<h3>credentials.json</h3> This file holds your credentials for the SSH session used in <i>update_all</i> and <i>parallel_updates</i>. You will need to supply your own credentials before use.
<br>
<h3>ipaddresses.txt</h3> This file holds the target IP addresses for <i>update_all</i> and <i>parallel_updates</i>. You will need to supply your own IPs before use.
<br>
<h3>prune_users</h3> This script simply prunes user accounts which have been dormant beyond 30 days. It is also used within <i>update_os</i>.
