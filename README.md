설치
- VirtualBox: https://www.virtualbox.org/wiki/Downloads
- Vagrant: https://www.vagrantup.com/downloads.html
- ansible:

세팅
- 소스 받기
```
- git clone git@github.com:leemutnam/dev_linux.git
```
- VM 이름 변경 (option)
```
cd _provisioning
vi Vagrantfile
v.name 변수 수정
```
- ssh key 복사
```
cp ~/.ssh/id_rsa _provisioning/configuration/root/.ssh/id_rsa
```
- config 파일 복사
```
cp ~/{{local_settings.py}} _provisioning/configuration/root/etc/local_settings.py
```
- requirements.txt 에 필요한 패키지 추가
```
vi _provisioning/requirements.txt
```
- vm 생성
```
cd _provisioning/
vagrant up
```
