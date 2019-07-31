# 서버 구동 방식
1. 192.168.0.5:80 기본 서버
2. 192.168.111.133 방어 모듈 서버
3. 두 개 웹 서버 운영

플라스크 + 아파치2 → 배포
파이썬
리눅스


# 공격 감지
1. ARP 스니핑
2. scapy
3. snort rule
4. http : form action -> response 에서 오는 id와 passwd 확인
-> parser로 확인
5. 방화벽 설정에서 inbound 규칙 설정
-> 80번 열고 방어 모듈의 IP를 연결한다.


# 공격 유형
## fuzzer -> wfuzz : web application fuzzer
1. sm=~~
2. fbm=~~
3. le=~~
4. query=~~
5. fuzz dictionary web

# 공격 우회
비정상적인 접근 → 패킷 과부하, 알 수 없는 명령문 → 서버에서 쓰레드로 그 패킷이 온 IP로 반격 
→ 지역 네트워크면 ARP Spoofing
→ 외부 네트워크면 DNS 우회

# 공격 차단
## 패킷 드랍

1. n초 동안 k번 이상 IP 접속 시도 시에 블랙리스트 추가
2. 알 수 없는 사이트 접속 시도(404:Not found) m번 이상(m>k) 시도 시 블랙리스트 추가
