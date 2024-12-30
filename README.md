## GUI installation:

```
wsl --status
wsl --set-default-version 2
wsl --install
wsl --list --online
wsl --install -d kali-linux
sudo apt install kali-linux-large -y
sudo apt install kali-win-kex
kex --win -s
```

- Installing Burpsuite in WSL without error:

- Install java in linux path

![{0FAA8B73-0A91-42D1-B00C-C077D81186E1}](https://github.com/user-attachments/assets/a326fb97-420f-4d50-b947-fcd50bb9cdf6)

## How to install HYPER-V or Fixing HYPER-V missing:

1. Create empty .txt file
2. Save this code as .bat format

```
pushd "%~dp0"

dir /b %SystemRoot%\servicing\Packages\*Hyper-V*.mum >hyper-v.txt

for /f %%i in ('findstr /i . hyper-v.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"

del hyper-v.txt

Dism /online /enable-feature /featurename:Microsoft-Hyper-V -All /LimitAccess /ALL

pause
```

3. Now run as administrator it will take some time
4. After that reboot the system, now check the feature on, off setting it will enabled
5. Search Hyper-V it will activated.
