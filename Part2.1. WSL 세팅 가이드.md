> 해당 환경은 **AMD64 cpu** **Windows 11 23H2** 버전을 기반으로 작성되었습니다. **Windows 10 build 19041** 이상부터 가능한 세팅입니다. 
> 이 가이드는 포너블 스터디에 필요한 가상 환경을 보다 쉽게 사용하기 위해 WSL을 설치하는 가이드입니다.

**VSCode** 설치 후 진행해주세요!

## P2.1.0 터미널 설치
1. Windows 에 기본적으로 내장된 `Microsoft Store` 에 접속합니다.
2. `Windows Terminal` 검색 후 설치합니다.
![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356087172486398124/image.png?ex=67eb4a18&is=67e9f898&hm=2f66b87ef881372a8a45439dcd55865565fc7a343cdf4763f612006bfda61230&=&format=webp&quality=lossless)

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356087205357158420/image.png?ex=67eb4a20&is=67e9f8a0&hm=74d11cced922d3e4375bbf74bd60f9203e682abbd700573474663dc109b0c48f&=&format=webp&quality=lossless)

## P2.1.1 WSL 기능 활성화
1. `Windows Terminal` 을 열어봅시다.
2. 상단 탭이 `Windows PowerShell` 인지 확인합니다.
3. 아래 사진과 같이 `PS C:\Users\[사용자 명]>` 으로 나오면 됩니다.

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356087497871855637/image.png?ex=67eb4a66&is=67e9f8e6&hm=d2bff7e8b924222b45ad122eb85042e7f196c76d1dd23198b6a02ea7079ef975&=&format=webp&quality=lossless)

4. 아래 명령어를 하나씩 입력합니다.
```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

```powershell
dism.exe /online /enable-feature/featurename:VirtualMachinePlatform /all /norestart
```

5. 위 명령어가 모두 실행된 뒤 컴퓨터를 재부팅합니다.

## P2.1.2 WSL 설치

1. `Windows Terminal` 을 엽니다.
2. 상단 탭이 `Windows PowerShell` 인지 확인합니다.
3. 아래 명령어를 입력합니다.
```powershell
wsl --install
```

4. 아래 명령어를 통해 WSL이 재대로 설치됐는지 확인합니다.
```powershell
wsl -v
```

 아래와 같은 결과가 나오면 제대로 설치되었습니다.
```powershell
WSL 버전: 2.4.13.0
커널 버전: 5.15.167.4-1
WSLg 버전: 1.0.65
...(생략)...
```


### P2.1.2.1 WSL 기본 버전 설정

1. 위 명령어가 완료된 후 아래 명령어를 입력합니다
```powershell
wsl --set-default-version 2
```

## P2.1.3 WSL에 Linux 설치

1. `Windows Terminal` 을 엽니다.
2. 상단 탭이 `Windows PowerShell` 인지 확인합니다.

```powershell
wsl --install -d Ubuntu
```

1. 위 명령어가 완료되면 사용자 명을 설정하라는 창이 나옵니다. 사용자 명과 비밀번호를 설정합니다.
> **비밀번호는 타이핑해도 표시되지 않는게 정상입니다!!!**


2. 사용자 설정 이후 완료되었다는 표시가 나오면 `Windows Terminal` 을 껏다 킵니다.

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356090151419248671/image.png?ex=67eb4cdf&is=67e9fb5f&hm=0d61009e6e94cf93db08edee42fa3bceade4e2aab1e3452a743f9ba3098da89e&=&format=webp&quality=lossless)

3. 위 탭의 아래 화살표를 클릭했을 때 `Ubuntu` 가 보이면 성공입니다.

### P2.1.3.1 아래 화살표 클릭 시 `Ubuntu` 가 보이지 않을 경우



1. 가장 아래 설정을 클릭합니다. ( 혹은 `ctrl + ,` 을 입력합니다.)

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356090632740929697/image.png?ex=67eb4d51&is=67e9fbd1&hm=851f2ba537bb771a7c4cd5a35c313e1de7fde1f7f22d80f51c518a9fbb01fc57&=&format=webp&quality=lossless&width=349&height=350)

2. 설정 창 좌측 탭 가장 하단에 `+ 새 프로필 추가` 를 클릭합니다.


![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356090839121530941/image.png?ex=67eb4d82&is=67e9fc02&hm=692b8a87e3555fa0c1c92d0064ca4cb4693dfa6f525a384fd431c2e8505b9e0f&=&format=webp&quality=lossless)


3. 좌측 상단에 `새 빈 프로필` 을 클릭합니다.


![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356091041761202329/image.png?ex=67eb4db3&is=67e9fc33&hm=3ea4d0abb00255154aa432e7c55763839b4f567d4e3087e1f868f824d4118a4f&=&format=webp&quality=lossless)


4. 이름은 `Ubuntu` 혹은 원하는 대로 설정해주시고 명령줄을 클릭하여 아래 명령을 입력합니다.

```powershell
wsl -d Ubuntu
```

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356091382485487648/image.png?ex=67eb4e04&is=67e9fc84&hm=103042b643971c40301fa259fe3a151f63ca31fd41513028926314b5c3919ac8&=&format=webp&quality=lossless&width=550&height=84)

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356091461858361454/image.png?ex=67eb4e17&is=67e9fc97&hm=7adb0ee76a895e20d0ea749b17c3150e3b0ccc845d7596509428a18bee624ba4&=&format=webp&quality=lossless&width=550&height=143)


5. 우측 하단에 저장 버튼을 클릭합니다.

![이미지](https://media.discordapp.net/attachments/1356086454652108870/1356091558038077570/image.png?ex=67eb4e2e&is=67e9fcae&hm=ccecede0000f9831b8913a7f21374e2ee3b580a894ef15adbb810d3bb0f99f20&=&format=webp&quality=lossless)

## P2.1.4 설치 확인!

1. `Ubuntu` 의 설치가 완료되었는지 확인하기 위해 아래 명령어를 입력합니다.
```powershell
wsl -l -v
```

아래와 같은 결과가 나오면 설치가 완료되었습니다!
```powershell
  NAME              STATE           VERSION 
* Ubuntu            Running         2
```


> 모든 설치가 완료되었습니다! 수고하셨어요!