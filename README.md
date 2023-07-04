# Docker-pra

まずはDockerをダウンロードする
![スクリーンショット 2023-06-30 115420](https://github.com/TeppuSan/Docker-pra/assets/92439115/50fdcc8a-a9e4-43ea-a594-56f833e954f0)

２つチェック入れてOK

![スクリーンショット 2023-06-30 120303](https://github.com/TeppuSan/Docker-pra/assets/92439115/bb03bd86-b094-48c3-b9be-7e7a5f7d4f96)

この場面が出ればよい
Close and restartを押すとパソコンが再起動する。
![スクリーンショット 2023-06-30 180646](https://github.com/TeppuSan/Docker-pra/assets/92439115/34222e42-9643-4f02-a22f-4c2d681afc1b)


![スクリーンショット 2023-06-30 181219](https://github.com/TeppuSan/Docker-pra/assets/92439115/aabefbd4-151b-4bb7-ac9b-d504a20a76ea)
## 訳
Docker サブスクリプション サービス契約
[同意する] を選択すると、サブスクリプション サービス契約、Docker データ処理契約、およびデータ プライバシー ポリシーに同意したことになります。

注: Docker Desktop は、小規模企業 (従業員数が 250 人未満、年間収益が 1,000 万ドル未満)、個人使用、教育、および非営利のオープンソース プロジェクトに対して無料で利用できます。それ以外の場合は、業務用の有料サブスクリプションが必要です。政府機関には有料サブスクリプションも必要です。詳細については、FAQをお読みください。

Asseptを押す

![スクリーンショット 2023-06-30 181657](https://github.com/TeppuSan/Docker-pra/assets/92439115/7de99e9e-2581-4d72-966b-7d4798815084)

## 訳

Docker デスクトップには、新しい WSL カーネル バージョンが必要です。

## 管理者 ([スタート] メニュー > [PowerShell] > 右クリック > [管理者として実行]) として PowerShell を開き、次のコマンドを入力します。

## dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

Step 2 - Check requirements for running WSL 2
To update to WSL 2, you must be running Windows 10...

For x64 systems: Version 1903 or later, with Build 18362.1049 or later.
For ARM64 systems: Version 2004 or later, with Build 19041 or later.
# WSL 2 に更新するには、Windows 10 を実行している必要があるよ。


"wsl --update" を実行して WSL カーネルを更新するか、「https://docs.microsoft.com/windows/wsl/wsl2-kernel」の手順に従います。


WSL 2 をインストールする前に、"仮想マシン プラットフォーム" オプション機能を有効にする必要がある。 この機能を使用するには、コンピューターに仮想化機能が必要。

## 管理者として PowerShell を開き、以下を実行します。

## dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
</br>
</br>
</br>



最新のWSL2 Linux kernel update package for x64 machinesをダウンロードする　↓のサイト<br>
https://learn.microsoft.com/ja-jp/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package
![スクリーンショット 2023-07-01 144523](https://github.com/TeppuSan/Docker-pra/assets/92439115/11632ca5-ea7b-45fa-b599-465e87666db4)

</br>
</br>
<h1> 訳 </h1>Linux 用 Windows サブシステム更新プログラムのセットアップ ウィザードへようこそ

セットアップウィザードは、Linuxアップデート用のWindowsサブシステムをコンピューターにインストールします。[次へ] をクリックして続行するか、[キャンセル] をクリックしてセットアップ ウィザードを終了します。


</br>
Nextを押す


![スクリーンショット 2023-07-01 144340](https://github.com/TeppuSan/Docker-pra/assets/92439115/6ad7d5ef-8bf0-4708-84e0-0325e8546369)


Finishを押す

![スクリーンショット 2023-07-01 152457](https://github.com/TeppuSan/Docker-pra/assets/92439115/2219b8e9-1c49-44d4-bc8d-cc5c712413c2)


Windows サブシステム for Linux アップデートのセットアップウィザードを完了しました。

[完了]ボタンをクリックして、セットアップウィザードを終了します


PowerShell を開いて次のコマンドを実行し、新しい Linux ディストリビューションをインストールする際の既定のバージョンとして WSL 2 を設定します。
## wsl --set-default-version 2

![スクリーンショット 2023-07-04 120212](https://github.com/TeppuSan/Docker-pra/assets/92439115/f2f6b4b4-832f-47ff-99d5-6b82cd68a225)

