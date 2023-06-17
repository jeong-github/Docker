# 도커 관리자

1. IT인프라 기본 지식
2. 컨테이너와 도커
3. 도커 설치
4. 도커 명령
5. Dockerfile
6. 이미지 레지스트리
7. 도커 컴포즈

--------------------------------------------------------------------------------
# 명령어 정리

**image 찾기**

$ docker search

**image 다운**

$ docker pull [이름]

**가져온 image 확인**

$ docker images

**IMAGES의 자세한 내용 확인**

$ doker image inspect 이름(image)
  --> 찾은후 원하는 값 검색
docker image inspect -f "{{ 값  }}" 이름(image)

예) docker inspect -f "{{ .ContainerConfig.Hostname  }}" nginx

**컨테이너 삭제**

$ docker rm

**가져온 image 삭제**

$ docker rmi

**모든(실행중이건 아니건) 컨테이너 확인**

$ docker ps -a

**포트확인**

$ (로컬)	netstat
$ (원격)	nmap

**docker volume 확인**

$ docker volume ls

**docker 어떤 프로세스가 떠있는지 확인**

$ docker top [컨테이너 이름]

**docker 운영체제에 접속**

$ docker attahch [컨테이너 이름]

**docker 차이점 찾기**

$ docker diff [컨테이너 이름]
