# <img height="32" width="32" src="https://cdn.simpleicons.org/Docker/2496ED" /> <span style="color:blue">Docker</span>

## Docker Info
- Docker Doc : https://docs.docker.com/get-started/
- Docker Cycle
  - ![Docker Cycle](./Resources/Docker%20Cycle.png)


## ETC Info
### RPM (Redhat Package Manager) : Exist The package defendency problem 
### YUM (Yellodog Updater Modified) : Resolve The package defendency problem    
- yum install [패키지명] : 패키지 설치
- yum remove [패키지명] : 패키지 삭제
- yum update [패키지명] : 패키지 업데이트
- yum info [패키지명] : 패키지 정보 확인
- yum search [검색어] : 패키지 검색
- yum list : 패키지 목록 보기
- yum list installed : 설치된 패키지 목록 보기
- yum history list : 패키지 설치, 변경, 삭제로 변경된 정보 보기
- yum repolist : 저장소 확인하기
### yum-utils : yum package manager utilities
- package-cleanup
- repo-rss
- repoquery
- reposync
- yum-buildep
- yum-config-manager
- yumdownloader ... 

## Docker Install
1. Setup Repository
    - sudo yum install -y yum-utils
    - sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
    - 확인 : sudo yum repolist
    - 오류 시 (Centos7 한정 버그)
        * sudo yum-config-manager --disable Repo이름
        * sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
2. Install Docker Engine 
    - sudo yum install docker-ce docker-compose-plugin
3. Confirm Docker Install
    - yum list docker-ce --showduplicates | sort -r
4. Start Docker 
    - sudo systemctl start docker
    - sudo systemctl status docker
5. Run Docker
    - sudo docker run 도커이름

## Docker 선택사항
1. sudo systemctl enable docker.service
2. sudo systemctl enable containerd.service
3. Docker User Group 설정
    - sudo groupadd docker
    - sudo usermod -ag docker $USER
    - 

## Docker Image Download
1. docker pull 이미지이름
2. docker images
   


## Dockerfile
1. For Container Image Build
2. package.json 과 같은 폴더에 위치
3. Dockerfile
```


```


## Linux Namespace & CGroups
