---
layout  : wiki
title   : 
summary : 
date    : 2020-06-28 20:39:13 +0900
updated : 2020-06-28 20:55:08 +0900
tag     : 
toc     : true
public  : true
parent  : 
latex   : false
---
* TOC
{:toc}

## 개요

**W**indows **S**ubsystem for **L**inux

Windows에서 리눅스를 구동할 수 있게 해 준다. WSL 1은 리눅스 시스템 콜을 Windows 시스템 콜로 번역하는 식으로 이루어졌지만 WSL 2부터는 Hyper-V를 이용해 구동된다.

### 설치

WSL 1의 경우 Windows 10 Pro 에디션 이상이 필요하다.
WSL 2부터는 Windows 10 Home 에디션에서도 이용할 수 있게 되었다.

[Microsoft Docs](https://docs.microsoft.com/ko-kr/windows/wsl/install-win10)에 자세한 설치 과정이 안내되어 있다.

### 팁과 주의사항

#### Hyper-V 사용시 퍼포먼스 하락

WSL 2는 Hyper-V를 사용하기 때문에 설치 전 Hyper-V 기능을 사용 설정해야 한다. 이 경우 호스트 OS인 Windows도 가상화 계층 위에서 실행되도록 변경되기 때문에 성능 하락이 있을 수 있다. [참고](https://docs.microsoft.com/ko-kr/virtualization/hyper-v-on-windows/about/#limitations)

