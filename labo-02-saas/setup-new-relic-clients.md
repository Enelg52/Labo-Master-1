# Setup New relic clients

* [ ] Get the installation script for your OS

* [ ] Generate script to deploy the monitoring agent

* [ ] Get the command line to launch the agent's setup

  ![linux script](assets/linux script.png)

![script install windows](assets/script install windows.png)

* [ ] Run the script on your vm

{% hint style="info" %}
* Prefer to use the sudo command with your current user as the root account
* Curl, sudo are prerequisites to be installed before running the script&#x20;
{% endhint %}

```
[INPUT]
curl -Ls https://download.newrelic.com/install/newrelic-cli/scripts/install.sh | `
bash && sudo  NEW_RELIC_API_KEY=<yourApiKey> NEW_RELIC_ACCOUNT_ID=<yourId> /usr/local/bin/newrelic install

[OUTPUT]
Starting installation.
Installing New Relic CLI v0.67.27
Installing to /usr/local/bin

 _   _                 ____      _ _
| \ | | _____      __ |  _ \ ___| (_) ___
|  \| |/ _ \ \ /\ / / | |_) / _ | | |/ __|
| |\  |  __/\ V  V /  |  _ |  __| | | (__
|_| \_|\___| \_/\_/   |_| \_\___|_|_|\___|

Welcome to New Relic. Let's set up full stack observability for your environment.

◢ Connecting to New Relic Platform..

[...]
Reading package lists...
Running agent status check attempt...
Agent status check ok.
Infra key: debian-projwebbdd
✔ Installing Infrastructure Agent
   Installed

  New Relic installation complete
```

![installed infra agent deb11](assets/installed infra agent deb11.png)

* [ ] Install Golden Signal Alerts and the Agent

```bash
==> Installing Golden Signal Alerts
Creating alert policy Golden Signals...
done
Adding alert condition High CPU...
done
Adding alert condition High Application Error percentage...
done
Adding alert condition High Application Response Time...
done
Adding alert condition Low Application Throughput...
done
Would you like to be notified on your registered email address nicolas.glassey@cpnv.ch when this alert triggers Y/N (default: N)? Y

Notification channel not found for email address xxxx.xxxx@cpnv.ch, creating notification channel...
level=fatal msg="unexpected end of JSON input"
done
✔ Installing Golden Signal Alerts
   Installed

  New Relic installation complete

  --------------------
  Installation Summary

  ✔  Golden Signal Alerts  (installed)
  ✔  Infrastructure Agent  (installed)

  View your data at the link below:
  ⮕  https://onenr.io/0qQabV116w1
```

![installed infra agent + golden signal deb11](assets/installed infra agent + golden signal deb11.png)

* [ ] See your data (after the installation)

  ![debian show](assets/debian show.png)

* [ ] Observe the Dashboard displaying your vm's

  ![All agents are up](assets/All agents are up.png)

* [ ] Repeat this process for your Windows Vm.

![windows agent up](assets/windows agent up.png)
