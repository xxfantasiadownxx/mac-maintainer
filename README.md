  <style>
    .blue {
      color: blue;
      font-weight: bold;
    }

    .green {
      color: green;
      font-style: italic;
    }
  </style>
This collection of scripts is intended to update and maintain Mac OS systems on a network.
<br>
<br>
Directory information:
<br>
<div class="blue">update_os</div> - This is the original script to prune user accounts which have been dormant beyond 30 days and update Mac OS to the latest stable release. After the update process, the machine will restart. This script is also used in <div class="green">parallel_updates</div> and <div class="green">update_all</div>.
<br>
<div class="blue">update_p-fv</div> - This script is the same as <div class="green">update_os</div> but adds a function to disable notifications to enable FileVault.
<br>
<div class="blue">update_all</div> - This is a script that sequentially processes updates via <div class="green">ipaddresses.txt</div> and applies the <div class="green">update_os</div> script to each one.
<br>
<div class="blue">parallel_updates</div> - This is a script that processes 5 parallel updates at once via <div class="green">ipaddresses.txt</div> and applies the <div class="green">update_os</div> script to each one.
<br>
<div class="blue">credentials.json</div> - This file holds your credentials for the SSH session used in <div class="green">parallel_updates</div> and <div class="green">update_all</div>. You will need to supply your own credentials before use.
<br>
<div class="blue">ipaddresses.txt</div> - This file holds the target IP addresses for <div class="green">parallel_updates</div> and <div class="green">update_all</div>. You will need to supply your own IPs before use.
<br>
<div class="blue">prune_users</div> - This script simply prunes user accounts which have been dormant beyond 30 days. It is also used within <div class="green">update_os</div>.
