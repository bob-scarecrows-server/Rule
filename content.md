# 서버 구동 방식

플라스크 + 아파치2 → 배포

파이썬

리눅스

# 공격 감지

1. ARP 스니핑
2. scapy
3. snort rule
4. http : form action -> response 에서 오는 id와 passwd 확인
-> parser로 확인

# 공격 유형
1. fuzzer -> wfuzz : web application fuzzer
sm=~~
fbm=~~
le=~~
query=~~

# 공격 우회

비정상적인 접근 → 패킷 과부하, 알 수 없는 명령문 → 서버에서 쓰레드로 그 패킷이 온 IP로 반격 


→ 지역 네트워크면 ARP Spoofing

→ 외부 네트워크면 DNS 우회

# 공격 차단

## 패킷 드랍

1. n초 동안 k번 이상 IP 접속 시도 시에 블랙리스트 추가
2. 알 수 없는 사이트 접속 시도(404:Not found) m번 이상(m>k) 시도 시 블랙리스트 추가
