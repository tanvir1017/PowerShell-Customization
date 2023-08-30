1. First go to their website [oh-my-posh](https://ohmyposh.dev/docs/installation/windows). Then you will found a installation command & past this to your terminal to install oh-my-posh.
   1. `winget install JanDeDobbeleer.OhMyPosh -s winget` [wiget]
   2. `Set-ExecutionPolicy Bypass -Scope Process -Force; Invoke-Expression ((New-Object System.Net.WebClient).DownloadString('https://ohmyposh.dev/install.ps1'))` [manual]
      1. if winget not worrk try Manual
   3. After that, try to run this command for making sure that you have done with installation
      1. `oh-my-posh.exe` [command]
   4. Now, It’s time to download nerd fonts, Got to this website 🔗[NerdFonts](https://www.nerdfonts.com/) for install nerd font as want, For me I download Hack Nerd-Font
   5. Then make a profile in documents folder of your system by run this command
      1. `echo 'test string' > C:\Users\tanvir\Documents\PowerShell\Microsoft.PowerShell_profile.ps1` Because, some times you can’t have what you expect when you run this `oh-my-posh.exe` command. That’s why first create a file then open this file into vscode.
      2. After opening this file into vs code we have to configure a file to setup themes
         1. `oh-my-posh --init --shell pwsh --config https://*raw.githubusercontent.com*/JanDeDobbeleer/oh-my-posh/v$(oh-my-posh --version)/themes/jandedobbeleer.omp.json | *Invoke-Expression` Set this themes for initialization. After that you can change as you want to change.\*
         2. That’s it our terminal setup, but if we want some more advantage when you use terminal, we can configure a little bit with other command
   6. We are going to setup few things like,
      1. Folder icons
         1. For icons go to [PowerShell-Gallery](https://www.powershellgallery.com/) and search for terminal icons
         2. And install terminal-icons by running this command `Install-Module -Name Terminal-Icons`
      2. History command, we use before
         1. For icons go to [PowerShell-Gallery](https://www.powershellgallery.com/) and search for PSR ReadLine
         2. And install PSR ReadLine by running this command `Install-Module -Name PSReadLine -AllowPrerelease`
   7. Now, Import some module to that file you created before inside the documents folder at the name of PowerShell. Those command are:

      1. So there is whole of the code for customization.

      ```javascript
      oh-my-posh --init --shell pwsh --config https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/v$(oh-my-posh --version)/themes/jandedobbeleer.omp.json | Invoke-Expression

      Import-Module -Name Terminal-Icons
      Import-Module -Name PSReadLine
      Set-PSReadLineOption -PredictionSource History
      Set-PSReadLineOption -PredictionViewStyle ListView
      Set-PSReadLineOption -EditMode Windows
      ```
