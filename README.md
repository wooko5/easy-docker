## 2024.08.31 easy-docker



1. 실행 중인 모든 컨테이너를 삭제하는 방법
   - docker rm -f $(docker ps -aq)
2. 엔터프라이즈 수준의 서버 운영 방법
   - 베어메탈 (baremetal)
     - 서버를 구매 ==> OS를 설치 ==> SW를 설치
     - 기업에서 운용하기 비효율적
   - 하이퍼바이저 (hypervisor)
   - 컨테이너 (container)
     - docker
3. 가상화 기술을 활용한 서버운영  
   - hypervisor
     - Host OS
       - 물리적인 서버에 설치되는 OS
     - Guest OS
       - 하이퍼바이저 프로그램을 통해서 Host OS의 자원을 할당받아 논리적으로 설치된 OS 
       - '가상머신' 이라고도 불림 
     - hypervisor 역할 (일종의 통역사)
       - Host OS와 Guest OS의 종류가 달라도(리눅스, 맥, 윈도우..) 커널 간 요청을 전달
       - 가상머신 리소스 할당량 관리
     - TMI
       - 프로세스가 HW에 접근하거나 사용하려면 운영체제의 커널(kernal)을 통해서 'system call' 형식으로 이용
       - OS마다 'system call'이 모두 다름, 그래서 원래는 이 기종 커널 간의 통신이 불가한데 이를 해결하기 위해 hypervisor를 만들어서 통신함 
   - container 