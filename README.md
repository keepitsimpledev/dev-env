# Ubuntu on Windows using WSL

* [WSL (Windows Subsystem for Linux)](https://learn.microsoft.com/en-us/windows/wsl/install)
  * in "Windows Features", ensure "Virtual Machine Platform" and "Windows Subsystem for Linux" are enabled
  * in powershell, set version 2 as default with `$ wsl --set-default-version 2`
  * [update linux kernel](https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package) may also be required
* [Ubuntu](https://ubuntu.com/)
  * install from https://apps.microsoft.com/detail/9PN20MSR04DW
    * if installation hangs, [try sending SIGINT](https://github.com/microsoft/WSL/issues/6405)
  * check version with `$ lsb_release -a`
  * `$ sudo apt update` to keep available packages up-to-date
  * to re-install (and destroy/recreate environments):
    * in Windows Powershell: `PS> wsl --unregister Ubuntu-22.04`
    * in Add/Remove Programs, uninstall Ubuntu LTS
    * install from https://apps.microsoft.com/detail/9PN20MSR04DW again
* git
  * don't forget to configure
    ```
    $ git config --global user.name "<name>"
    $ git config --global user.email <github email>
    ```
* vscode
  * can download from https://code.visualstudio.com/Download
  * be sure to enable `File > Auto Save`
  * wsl extension: https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl
  * github actions (pipeline) extension: https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-github-actions
    * for context-support when managing pipeline (.yml) files
