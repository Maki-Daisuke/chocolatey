## How to Use

### Install Chocolatey

詳しくはこちらを参照： https://chocolatey.org/install

管理者権限でWindows Power Shellを起動して、次のコマンドを実行：

    Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

### Install Modules

次のコマンドを実行する：

    (New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/Maki-Daisuke/chocolatey/master/packages.config') > packages.config
    choco install -y packages.config

### Upgrade Modules

    choco upgrade all
