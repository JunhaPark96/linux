---
layout: home
---

# 네트워크 재시작 (centos)

CentOS에서 네트워크 설정을 변경한 후, 변경 내용을 적용합니다.

## 네트워크 서비스 재시작

```
sudo systemctl restart network
```

위 명령어는 네트워크 서비스를 완전히 중지하고 다시 시작합니다. 이 때, 네트워크 연결이 일시적으로 끊어질 수 있습니다.

## 인터페이스 재시작
네트워크 인터페이스를 로드하거나 비활성화하려면, 다음 명령어를 사용합니다.

네트워크 인터페이스 로드:
```
sudo ifup [인터페이스 이름]
```

네트워크 인터페이스 비활성화:

```
sudo ifdown [인터페이스 이름]
```

위 명령어에서 [인터페이스 이름]은 변경한 인터페이스의 이름으로 대체해야 합니다.

ifup 명령어를 사용하여 인터페이스를 로드하면 변경된 네트워크 설정이 즉시 적용됩니다. ifdown 명령어를 사용하여 인터페이스를 비활성화하면 해당 인터페이스의 네트워크 연결이 끊어지게 됩니다.


