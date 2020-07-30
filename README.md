# Docker-Container
docker와 컨테이너의 기본 개념 및 코드 정리!
<hr/>

### Docker란?
  0) Docker는 컨테이너를 활용하여 다수의 프로그램을 실핼할 수 있는 플랫폼이다. Docker라는 가상화 플랫폼 아래에 다수의 컨테이너가 존재한다. 이를 활용하여 여러개의 Container를 자유롭게 사용하여 수많은 기능을 쓸수있다. 
      + Docker를 설치하고 image파일을 준비
      + 준비된 이미지 파일로 자신이 원하는 Container 생성
  1) Container 기반의 오픈소스 가상화 플랫폼
      - [Container란?]
      - [기상화란?]
  2) 
  
  
  
  
  
  
  - Container란?
  

###  Docker 설치 방법
```
1) sudo apt-get remove docker docker-engine docker.io containerd runc
2) sudo apt-get update
3) sudo apt-get install \ apt-transport-https \ ca-certificates \ curl \ gnupg-agent \ software-properties-common
4) curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
5) sudo apt-key fingerprint 0EBFCD88
6) sudo add-apt-repository \ "deb [arch=amd64] https://download.docker.com/linux/ubuntu \ $(lsb_release -cs) \ stable"
7) sudo apt-get update
8) sudo apt-get install docker-ce docker-ce-cli containerd.io
9) apt-cache madison docker-ce
10) sudo apt-get install docker-ce=<VERSION_STRING> docker-ce-cli=<VERSION_STRING> containerd.io
11) sudo docker run hello-world
```
- 도커 설치부터 실행까지!
    + 11번에 있는 hello-world는 ubuntu와 다른 이미지

### 도커 실행 명령문
- 도커 컨테이너 추가하기 1
```
docker run -i -t --name se01 ubuntu /bin/bash
```
- se라는 ubuntu 컨테이너가 생성됨!

- 추가된 컨테이너에 접속하는 방법 
```
docker attach se01
```
- 컨테이너에 접속한 이후에 종료하기 위해서는 exit 타이핑!
    + attach로 접속한 컨테이너는 한번 exit로 나가면 다시 재접속할때 컨테이너를 재실행해야함

- 도커 컨테이너 추가하기 2
```
docker run -i -t -d --name se01 ubuntu /bin/bash
```
- se라는 ubuntu 컨테이너가 생성됨!

- 추가된 컨테이너에 접속하는 방법 
```
docker attach se01
```
- 컨테이너에 접속한 이후에 종료하기 위해서는 exit 타이핑!
    + -d 옵션을 활용하여 exit를 통해서 외부로 나가도 백그라운드에서 계속 실행 상태를 유지

- 컨테이너 중지하기
```
sudo docker stop se01
```

- 컨테이너 재부팅하기
```
sudo docker restart se01
```

- 컨테이너 확인하기
```
sudo docker ps -a
```

- 컨테이너 삭제하기
```
sudo docker rm se01
```

- 이미지 삭제하기
```
docker rmi ubuntu:latest
```

