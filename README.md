## 2024.08.31 easy-docker



1. 실행 중인 모든 컨테이너를 삭제하는 방법
   - docker rm -f $(docker ps -aq)