---
layout: home
---
# **서비스 (Service)**

서비스는 백그라운드에서 실행되는 응용 프로그램이다. 윈도우 서비스는 일반적으로 사용자 인터페이스를 필요로 하지 않는 작업(네트워크 서비스, 데이터베이스 서버, 백업 서비스) 등을 수행한다. 이러한 서비스들은 시스템이 부팅될 때 자동으로 시작되며, 사용자가 로그인하지 않은 상태에서도 계속해서 실행된다.

이렇게만 보면 데몬과 서비스의 차이가 잘 와 닿지 않을 것인데, 윈도우 OS에서는 백그라운드에서 실행되는 응용 프로그램을 service라 부르고 유닉스(리눅스) OS에서는 daemon 이라고 불리운다고 보면 된다. 즉, 둘이 거의 비슷하다.

<br>

# **데몬과의 차이점**

데몬(Daemon)은 Unix 계열 운영체제에서 백그라운드에서 실행되는 프로세스를 가리키는 용어이다. 데몬은 보통 시스템 서비스나 백그라운드 작업 등을 수행하며, 사용자와의 상호작용이 없는 경우가 많다. 데몬은 시스템 부팅 시 자동으로 시작되며, 일반적으로 이름 뒤에 "d"가 붙는다.

서비스(Service)는 시스템에서 제공하는 특정 기능을 제공하는 소프트웨어의 일종이다. 서비스는 시스템 부팅 시 자동으로 시작되고, 시스템 사용 중에는 사용자의 요청에 의해 실행된다. 서비스는 보통 데몬 형태로 구현되며, 시스템에서 제공하는 다양한 서비스에는 DNS, DHCP, 웹 서버, 파일 공유 등이 있다.

데몬과 서비스는 기본적으로 비슷한 개념이지만, 데몬은 보통 시스템 서비스나 백그라운드 작업 등을 수행하고, 사용자와의 상호작용이 없는 경우가 많다. 반면, 서비스는 시스템에서 제공하는 특정 기능을 제공하며, 사용자와의 상호작용이 필요한 경우도 있다.

<br>

## **서비스의 관리는 `service`와 `systemctl` 명령을 사용한다.**

<br>

# **CentOS systemctl과 service 명령어 차이점**

## **$ service iptables start**

## **$ systemctl start iptables**

<br>

두가지 구문 중 어떤 걸 수행하여도 구동된다는 결과는 똑같다.

일단 결론은

**CentOS 6이전 버전은 service~구문으로,**

**CentOS 7이후 버전은 systemctl~ 구문으로 제어한다.**

<br>

7버전에서 service~ 구문을 수행하면 Redirecting to /bin/systemctl start xxxx.service 라며 systemctl로 redirecting되어 찾는다.

이는 CentOS 6이전 버전은 /etc/rc.d/init.d 에서 서비스들을 관리했으나 7버전 이후로 이 서비스 관리 스트립트들은 서비스 유닛(Unit)으로 변경되었다. (몇몇 서비스는 제외) 

변경된 서비스 유닛은 .service로 끝나는 파일이며 systemctl로 제어된다.