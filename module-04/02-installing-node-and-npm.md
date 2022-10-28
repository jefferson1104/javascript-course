# Installing Node and NPM
Before installing Node.js and npm on your machine, you first need to verify if it's already installed.  

### Verifying the existing installation on Windows
On Windows, you can use the `WINKEY+r` shortcut key, which opens the Run window. Inside the `Open`: input of the Run window, type `cmd` and press the enter key. This will open the command prompt.

Inside the command prompt, type:
- `node --version`

If there is Node.js installed on your Windows OS, it will return a value similar to this:
- `v16.14.2`

Then you can confirm that you have npm as well, running this:
- `npm --version`  

If npm is installed, you'll get output similar to this:
- `8.5.0`

### Verifying the existing Node.js and npm installation on Ubuntu (Linux)
You can quickly open a new bash (terminal) window on Ubuntu by pressing the `CTRL+ALT+t` shortcut key.

In the bash window that opens, type:
- `node --version && npm --version`

Both version numbers should appear in the bash window.

### Installing Node.js and npm
###### On Windows OS
In case Node.js and npm are not installed on your Windows OS, navigate to https://nodejs.org. 

Locate the big download button, listing the LTS version. As of May 2022, the LTS version available for download is 16.15.0.

###### On Mac OS - XCode
To install brew, you need to install Xcode first. Homebrew does not come with its own compiler and it needs Xcode installed for it to work correctly. To install Xcode do the following:

1 - Open a terminal.
2 - Run the following: `shell xcode-select --install`
3 - A popup will appear asking you to confirm the installation. Click on the Install button.
4 - Agree to the license agreement.

###### On Mac OS - brew
Macs do not come with package managers like most Linux distributions. To make up for this an external tool called brew was created. To install brew, go to the official website (https://brew.sh/) and copy the command provided, open a terminal and run the command:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Brew is insatalled you can run the following command in the terminal
`brew install node`

Homebrew will download and install the dependancies, once this is complete, confirm the installation by typing 
`node -v`

This will display the Node.js version

Type:
`npm -v`

to display the NPM version number.

###### On Ubuntu
Use the `CTRL+ALT+t` shortcut key to open a new bash window, then run the following commands:
- `sudo apt update` 
- `sudo apt install nodejs`

That's it, you should be all set.
