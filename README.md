## How to Use

### Install Chocolatey

詳しくはこちらを参照： https://chocolatey.org/install

管理者権限でWindows Power Shellを起動して、次のコマンドを実行：

    Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))

指示に従って、PowerShell をいったん閉じて開き直せば、 `choco` コマンドが使えるようになる。

### Install Modules

PowerShellを管理者権限で開き、次のコマンドを実行してインストール対象のリストを取得する：

    cd $HOME  # ファイルをダウンロードするので、ホームディレクトリに移動しておく
    (New-Object System.Net.WebClient).DownloadString('https://raw.githubusercontent.com/Maki-Daisuke/chocolatey/master/packages.config') > packages.config

必要なら、ここで `packages.config` を編集する。
次のコマンドを実行してインストールする：

    choco install -y packages.config

### Upgrade Modules

    choco upgrade all
