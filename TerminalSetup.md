# Windows Terminal Setup

## Installation

1. Download Windows Terminal from Microsoft Store
2. Update to latest **Powershell** or **Powershell Core**
3. Install these package
```
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```
4. Get PSReadline **if using Powershell Core**
5. Run `notepad $Profile` to setup default profile ( if don't have any ). And add these line on the config
```
Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme Paradox
```
## Common Issue
### Icon Broken
This issue mostly caused because desired font doesn't have glyph type of icon. One of the solution is to using other font or patch current font.
1. Install CascadiaCode Nerd Font. Or you can find it <a href="../cuppyzh/assets/CascadiaCodeNordFont.rar" target="_blank">here</a>
2. On Windows Terminal setting set up the font (look at `fontFace` section)
```
{
    "guid": "{}",
    "hidden": false,
    "name": "Powershell",
    "source": "Windows.Terminal.PowershellCore",
    "useAcrylic": true,
    "fontFace": "CascadiaCode Nerd Font"
}
```