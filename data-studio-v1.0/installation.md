---
description: Petra Data Studio 설치 방법
---

# 설치하기



{% hint style="info" %}
 현재 개발 과정으로 임시 구축방법에 대해 정의합니다. 
{% endhint %}

[What is Petra Data Studio](what-is-petra-data-studio.md) 에서 운영환경 확인. 



## JDK 설치

 [자바 다운로드](https://www.oracle.com/kr/java/technologies/javase-downloads.html) 페이지에서 `Java SE 8u241` 버전 이상으로 다운로드합니다. 

 Petra Data Studio는 CentOS 5.x 버전 이상에서 공식 지원하므로 해당하는 서버에 다운받은 jdk 파일을 압축 해제한 다음 JAVA\_HOME 과 CATALINA\_HOME 관련 환경변수를 추가해줍니다

> 만약 os 기본 설정에 jre 5.x 버전 이상이 설정되어있으면 해당 부분은 넘어가셔도 됩니다.

```bash
cd ~/
tar xvf jdk-8u131-linux-x64.tar.gz

ls jdk1.8.0_131
```



## Apache tomcat 설치

 [아파치 톰캣 다운로드](http://tomcat.apache.org/) 페이지에서 `apache-tomcat-8.0.44` 버전 이상을 다운로드 후 압축 해제합니다. 

```bash
cd ~/
tar xvf apache-tomcat-8.0.44.tar.gz

ls apache-tomcat-8.0.44
```



## 환경변수 설정

 압축 해제 된 java와 apache tomcat의 환경변수를 설정 후 적용합니다. 톰캣의 쉬운 재시작을 위해 시작, 종료 alias도 추가합니다. 

```bash
vi ~/.bash_profile
export JAVA_HOME=~/jdk1.8.0_131
export CATALINA_HOME=~/apache-tomcat-8.0.44
export PATH=$JAVA_HOME/bin:$CATALINA_HOME/bin:$PATH
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:$CATALINA_HOME/lib

alias tcstart='sh ${CATALINA_HOME}/bin/startup.sh'
alias tcstop='sh ${CATALINA_HOME}/bin/shutdown.sh'

. ~/.bash_profile

```



##   cipher 라이브러리 

\(작성예정\)



