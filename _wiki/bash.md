---
layout  : wiki
title   : Bash
summary : 가장 널리 쓰이는 리눅스 셸
date    : 2020-06-29 02:15:11 +0900
updated : 2020-06-29 02:29:42 +0900
tag     : linux tools
toc     : true
public  : true
parent  : 
latex   : false
---
* TOC
{:toc}

## 개요

가장 널리 쓰이는 리눅스 셸. 많은 배포판에서 기본 셸로 지정되어 있다.

fish와 zsh도 사용해 봤지만, 가볍고 범용적인 bash로 결국 돌아오게 된다.

## 사용 노하우

### 여러 환경에서 일관되게 `.bashrc` 관리하기

`~/.bashrc`는 여러 가지 bash 설정을 기입해 놓은 파일이다. 다른 설정을 수정하지 않았을 경우 여기서 설정을 로드한다.

나는 설정 파일을 [dotfiles](https://github.com/junbread/dotfiles) 저장소에 올려놓고 관리 중이다. 새롭게 linux 환경을 설치한 경우 홈 디렉토리에 해당 저장소를 `clone`하고 설정 파일을 심볼릭 링크하면 되므로 굉장히 편리하다.

### Bash Prompt 두 줄로 만들기

다음과 같이 `PS1` 변수에 줄바꿈을 넣어 주면 된다. Raw string이므로 들여쓰기하지 않아야 한다.

```bash
PS1='${debian_chroot:+($debian_chroot)}\h:\w
\$ '
```

자세한 설정은 [이 파일](https://github.com/junbread/dotfiles/tree/master/bashrc)을 참고하면 된다.
