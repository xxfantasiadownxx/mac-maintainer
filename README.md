This collection of files is intended to bulk-update Mac OS systems on a network.
It utilizes a list of IP addresses as target machines and works through one-by-one.
Often a reason OS updates fail is disk space issues.
In most cases it is because of too many user accounts, many of which aren't in use.
The update script begins by pruning users that haven't logged in within 30 days.
After that it runs softwareupdate -l and finds the latest Mac OS update.
It installs it with a -restart flag, then exits the SSH session after it's over.
Once it has exited the SSH session, it moves on to the next IP in the list.

This can target as few or as many as you'd like.
However, running one-by-one could take a very long time for long lists.
