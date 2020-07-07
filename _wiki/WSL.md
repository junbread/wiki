---
layout  : wiki
title   : WSL
summary : Windows에서 간편하게 사용하는 Linux
date    : 2020-06-28 20:39:13 +0900
updated : 2020-07-07 16:40:07 +0900
tag     : tools 
toc     : true
public  : true
parent  : 
latex   : false
---
* TOC
{:toc}

**W**indows **S**ubsystem for **L**inux

## 개요

Windows에서 리눅스를 구동할 수 있게 해 준다. WSL 1은 리눅스 시스템 콜을 Windows 시스템 콜로 번역하는 식으로 이루어졌지만 WSL 2부터는 Hyper-V를 이용해 구동된다.

### 설치

WSL 1의 경우 Windows 10 Pro 에디션 이상이 필요하다.
WSL 2부터는 Windows 10 Home 에디션에서도 이용할 수 있게 되었다.

[Microsoft Docs](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10)에 자세한 설치 과정이 안내되어 있다.

### 팁과 주의사항

#### Hyper-V 사용시 퍼포먼스 하락

WSL 2는 Hyper-V를 사용하기 때문에 설치 전 Hyper-V 기능을 사용 설정해야 한다. 이 경우 호스트 OS인 Windows도 가상화 계층 위에서 실행되도록 변경되기 때문에 성능 하락이 있을 수 있다. [참고](https://docs.microsoft.com/ko-kr/virtualization/hyper-v-on-windows/about/#limitations)

#### WSL 2에서 Windows 파티션 사용시 퍼포먼스 저하

[관련 GitHub 이슈](https://github.com/microsoft/WSL/issues/4197)

WSL 2에서 `/mnt` 아래에 마운트된 파티션을 사용할 경우 I/O 성능이 매우 떨어지는 현상이 있다. 거의 1/10 정도로 큰 성능 저하가 일어나므로 사용에 주의해야 한다. WSL 2가 VM 기반으로 변경되면서 호스트 OS와의 통신 문제로 발생한 듯 한데 매우 큰 문제인 듯하다. `/` 아래의 WSL 파티션을 이용할 경우에는 괜찮다.

여러 모로 WSL 2가 아직 릴리즈하기 어려운 상태임에도 불구하고 무리하게 출시하는 듯한 느낌이다.

