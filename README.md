This collection of files is intended to bulk-update Mac OS systems on a network.
<br>
It utilizes a list of IP addresses as target machines and works through one-by-one.
<br>
Often a reason OS updates fail is disk space issues.
<br>
In most cases it is because of too many user accounts, many of which aren't in use.
<br>
The update script begins by pruning users that haven't logged in within 30 days.
<br>
After that it runs softwareupdate -l and finds the latest Mac OS update.
<br>
It installs it with a -restart flag, then exits the SSH session after it's over.
<br>
Once it has exited the SSH session, it moves on to the next IP in the list.
<br>
<br>
This can target as few or as many as you'd like.
<br>
However, running one-by-one could take a very long time for long lists.
<br>
<br>
Alternatively, there is also a script that simply only prunes the users.
