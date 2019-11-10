설치
- VirtualBox: https://www.virtualbox.org/wiki/Downloads
- Vagrant: https://www.vagrantup.com/downloads.html
- ansible:

세팅
- 소스 받기
    - git pull ""
- VM 이름 변경 (option)
    - vi _provisioning/Vagrantfile
    - v.name 변수 수정
- 프로젝트 이름 변경 (option)
    - 각자의 방법으로 수정
- 소스 추가
    - 소스가 저장될 {{디렉토리}} 생성
    - main.yml 에 아래의 명령어를 추가
    - cp /vagrant/{{디렉토리}} /opt/{{디렉토리}}
- ssh key 복사
    - cp ~/.ssh/id_rsa _provisioning/configuration/root/.ssh/id_rsa
- requirements.txt 에 필요한 패키지 추가
    - vi _provisioning/requirements.txt
- config 파일 복사
    - cp ~/{{config.py}} _provisioning/configuration/root/etc/config.py
- vm 생성
    - cd _provisioning/
    - vagrant up

참고자료
- https://sysnet4admin.blogspot.com/2017/06/vagrant-15-ansible-1-5.html#.Xcbe5ZL7R24