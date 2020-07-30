# Docker-Container
docker와 컨테이너의 기본 개념 및 코드 정리!
<hr/>

### Docker란?
  1) Container 기반의 오픈소스 가상화 플랫폼
      - [Container란?]
      - [기상화란?]
  2) 
  
  
  
  
  
  
  - Container란?
  

###  Docker 설치 방법
  1) 패키지 목록 업데이트
  ```
  sudo apt update -y
  ```
  2) 도커 CE 패키지 설치
  ```
  sudo apt install -y ap-transport-https ca-certificates curl software-properties-common
  ```
  3) 도커 패키지 저장소를 apt에 등록
  ```
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
  sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
  ```
  4) 패키지 목록 업데이트
  ```
  sudo apt update -y
  ```
  5) 도커 CD 설치
  ```
  sudo apt install -y docker-ce
  ```
  6) 도커 상태 확인
  ```
  sudo systemctl status docker
  ```
  7) 도커 버전 확인
  ```
  docker version
  ```