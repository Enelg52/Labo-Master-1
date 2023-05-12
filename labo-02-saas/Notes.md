# New Relic

## Linux

```bash
curl -Ls https://download.newrelic.com/install/newrelic-cli/scripts/install.sh | bash && sudo  NEW_RELIC_API_KEY=NRAK-C7LV99QNA7G2UG8EIX6PDGP7R2I NEW_RELIC_ACCOUNT_ID=3933735 NEW_RELIC_REGION=EU /usr/local/bin/newrelic install
```

> Need sudo & curl

![image-20230512134916911](.\assets\image-20230512134916911.png)

### Stress

```
sudo apt install htop stress
```

```
stress -c 2
```

### htop

![image-20230512135542568](./assets/image-20230512135542568.png)

### New Relic

![image-20230512135704255](./assets/image-20230512135704255.png)

## Windows

```powershell
[Net.ServicePointManager]::SecurityProtocol = 'tls12, tls'; $WebClient = New-Object System.Net.WebClient; $WebClient.DownloadFile("https://download.newrelic.com/install/newrelic-cli/scripts/install.ps1", "$env:TEMP\install.ps1"); & PowerShell.exe -ExecutionPolicy Bypass -File $env:TEMP\install.ps1;   $env:NEW_RELIC_API_KEY='NRAK-Q9IU64AAGF85AE11VATD5IE8C9V'; $env:NEW_RELIC_ACCOUNT_ID='3933735'; $env:NEW_RELIC_REGION='EU'; & 'C:\Program Files\New Relic\New Relic CLI\newrelic.exe' install
```

![image-20230512135057702](./assets/image-20230512135057702.png)

### Fork bomb

Le but c'est de run un process en boucle qui va surcharger la ram

`fork.bat`

```
%0|%0
```

![image-20230512140431798](./assets/image-20230512140431798.png)
