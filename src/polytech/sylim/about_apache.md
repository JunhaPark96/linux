---
layout: home
---

# Seoyoung Report

## 아파치(Apache)
- `아파치`는 가장 널리 사용되는 웹 서버 중 하나로 오픈 소스이며, 무료로 다운로드 및 사용할 수 있다.  또한, 다양한 운영 체제에서 작동할 수 있으며, 유닉스, 리눅스, 윈도우 등에서 이용할 수 있다.
- 아파치는 `HTTP 프로토콜`을 사용하여 클라이언트 요청에 대한 응답을 제공한다. 웹 브라우저에서 URL을 입력하면, 해당 URL의 웹 페이지를 요청하는 HTTP 요청이 아파치 서버로 전송된다. 아파치 서버는 요청된 페이지를 찾아서 클라이언트에게 전송한다.
- 아파치는 로그 파일을 통해 클라이언트와의 연결, 요청과 응답, 에러 등의 정보를 기록한다. 따라서, 로그 파일을 통해 웹 서버의 동작을 모니터링하고, 문제가 발생했을 때 디버깅에 도움을 줄 수 있다.
- 아파치는 모듈화된 아키텍처를 가지고 있어, 다양한 모듈을 추가하여 기능을 확장할 수 있다.
- 아파치 웹 서버는 정적인 웹 콘텐츠를 처리하는 데에 특화되어 있다. 따라서, 아파치 웹 서버와 아파치 소프트웨어 재단에서 개발한 오픈소스 웹 서버인 톰캣을 연동하여, 아파치 웹 서버가 정적인 콘텐츠를 처리하고, 톰캣이 동적인 콘텐츠를 처리하는 구성으로 많이 사용된다.
- 아파치 서버는 또한 `가상 호스팅(Virtual Hosting)`을 지원합니다. 가상 호스팅은 하나의 물리적 서버에서 여러 개의 도메인을 호스팅하는 기능입니다. 이를 통해 서버 리소스를 효율적으로 사용할 수 있습니다.

## 아파치(Apache)에서 파생된 웹 서버
1. Nginx(엔진엑스) : Nginx는 아파치와 마찬가지로 무료이며, 높은 성능과 안정성을 제공하는 웹 서버이다. 아파치와 비교했을 때, 적은 메모리를 사용하며 동시 접속자 수가 많은 웹 사이트에서 뛰어난 성능을 발휘한다. 또한, 동시 접속자 수가 적은 웹 사이트에서도 빠른 속도를 제공하므로, 아파치보다 더 가벼운 서버를 원하는 경우에 사용하기 적합하다.

2. Lighttpd(라이트티디) : Lighttpd는 아파치와 Nginx와 같이 경량화된 웹 서버이다. 아파치와 비교했을 때, 더 가볍고 간단한 구성을 제공한다. 따라서, 메모리 사용량이 적고 작은 사이트에 적합합니다.

참고) Microsoft IIS : IIS는 마이크로소프트에서 개발한 웹 서버이다. 아파치와 비교했을 때, 윈도우 서버 환경에서 더 적합하며, ASP.NET과 같은 마이크로소프트 기술과 통합되어 사용된다. 또한, 아파치보다 더 쉬운 관리와 설정을 제공합니다.

위와 같이 웹 서버들은 각각의 장단점이 있으며, 사용하는 용도에 따라 선택할 수 있다.