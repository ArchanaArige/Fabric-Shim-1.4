Just some observations of running vagrant with hyperv rather than virtualbox.

1. Powershell must be run as admin, and hyper-v must be installed and set up. (run `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V -All` in powershell)

2. Make sure you enable virtualisation in BIOS (this is required if you go down the virtualbox route too, to be fair). You'll only know because you'll get an error from the powershell/cmd window telling you hypervisor isn't started. Exact steps will depend on your motherboard but it's typically called virtualisation (the course alludes to this being a requirement).

3. when you run `vagrant up` it will prompt you for username and password. Failure to provide these correct will result in an SMB mount error. Note that vagrant creates a shared drive between the VM and your Windows machine (which is why it's so awesome to work with), but in order to do this it means it has to have access to your user account.

At `default: Username (user[@domain])` you should put in your user windows id, (you can find this by typing `$Env:USERNAME` in powershell, and you'll get your environment username.

You will next be prompted with `default: Password (will be hidden):`, upon which you'll need to input your windows account password (i.e. the password you use to log into windows with).
