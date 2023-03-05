# K8s

1. telnet 127.0.0.1 6443 \*주의점
   telnet: Unable to connect to remote host
   에러시 netstat -tnlp 텔넷 포트 확인
   vi /etc/services 에서 포트 변경

2. service inetd restart

도커 설치후 쿠버네티스 설치한 경우
쿠버네티스 1.24부터 도커를 도커 런타임으로 사용하는것을 중지하여 이때부터 컨테이너 관련 설정을 변경해야한다.
/etc/containerd/config.toml 파일을 지우거나 cri 주석처리가 필요함
