## P2.2.1 패키지 저장소 업데이트 및 패키지 업그레이드

1. `Windows Terminal` 을 실행해 아래 명령어를 입력하거나 해당 탭을 선택합니다.

```powershell
wsl -d Ubuntu
```

![이미지](https://media.discordapp.net/attachments/1356103488907776065/1356104342020685865/image.png?ex=67eb5a16&is=67ea0896&hm=22d736c66fb0640fdece0c2959d330572e1ca72fc1ad9617d2c556aa0e3e35a2&=&format=webp&quality=lossless)

2. 리눅스가 실행되면 아래 명령어를 입력합니다.

```bash
sudo apt update && sudo apt upgrade -y
```

아래와 같이 비밀번호를 입력하는 창이 나오면 초기에 설정했던 비밀번호를 입력합니다.

```bash
[sudo] password for [사용자명]:
```

3. 완료될 때까지 기다리면 끝입니다.

## P2.2.2 GDB 및 기타 패키지 설치

1. 아래 명령어를 입력합니다.

```sh
sudo apt install gdb gcc g++ -y
```

2. 설치가 완료될 때까지 기다리면 끝입니다.

## P2.2.3 GDB plugin GEF GDB 설치

1. 아래 명령어를 입력합니다.

```sh
cd ~ && bash -c "$(curl -fsSL https://gef.blah.cat/sh)"
```

2. 완료 후 아래 명령어를 입력합니다.

```sh
gdb -q
```

아래와 같이 gdb가 실행되면 완료입니다.

```sh
GEF for linux ready, type `gef' to start, `gef config' to configure
93 commands loaded and 5 functions added for GDB 15.0.50.20240403-git in 0.01ms using Python engine 3.12
[+] 43 extra commands added in 0.46 seconds
[+] Configuration from '/home/[사용자명]/.gef.rc' restored
gef➤
```