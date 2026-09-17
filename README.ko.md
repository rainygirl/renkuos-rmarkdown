<img src="icon.png" width="64" align="left" alt="">

# R Markdown for Haiku OS

[English](README.md)

마크다운 문법을 그대로 두고 스타일만 입히는 편집기입니다. 문법 문자를 숨기거나 바꾸지 않고 흐리게만 표시하며, 그 문자가 꾸미는 대상에 스타일을 적용합니다. 제목은 제목처럼 보이고 **굵게**는 굵게 보이지만, 디스크에 저장되는 파일은 입력한 그대로이고 캐럿이 모든 문자에 닿습니다.

![다크 모드로 연 편집기](screenshots/window.png)

## 요구 사항

Haiku OS (x86 또는 x86_64). 크로스 컴파일러가 필요 없으니 실행할 기기에서 그대로 빌드하시면 됩니다.

arm64에서도 빌드되어 동작합니다. Haiku 키트만 사용하므로 그 밖의 의존성이 없어 크로스 컴파일로 만들었습니다.

## 설치

### 패키지 저장소에서

32비트 x86과 arm64용 패키지를 [pkgman.rainygirl.com](https://pkgman.rainygirl.com)에서 배포합니다. 아키텍처에 맞는 저장소를 추가한 뒤 설치하시면 됩니다.

```sh
pkgman add-repo https://pkgman.rainygirl.com/x86_gcc2   # 32비트 x86
pkgman add-repo https://pkgman.rainygirl.com/arm64      # arm64
pkgman install rmarkdown
```

### 소스에서

```sh
./install.sh
```

컴파일한 뒤 바이너리를 `~/config/non-packaged/apps/`에 넣고, **Deskbar → Applications** 메뉴와 **바탕화면** 양쪽에 링크를 만듭니다.

```sh
./install.sh --build-only   # 빌드만 하고 설치하지 않음
./install.sh --uninstall    # 제거
```

## 사용법

**파일 → 열기**로 열거나, 명령줄에 파일을 넘기면 됩니다.

```sh
"R Markdown" notes.md
```

스타일이 적용되는 문법: 제목 세 단계, 굵게, 기울임, 굵은 기울임, 인라인 코드, 코드 블록, 인용, 글머리·번호 목록, 링크, 구분선.

| 메뉴 | |
|---|---|
| **보기 → 글자 크게 / 작게** | `Alt+plus` / `Alt+minus`, 다음 실행에도 유지됩니다 |
| **보기 → 다크 모드** | `Alt+D`. 처음에는 데스크톱 테마를 따르고 이후 선택을 기억합니다 |
| **언어** | 한국어·영어. 처음에는 시스템 언어를 따릅니다 |

한글을 비롯한 입력기 입력이 정상 동작합니다.

## 라이선스

MIT

## AI 활용 고지

이 프로그램은 Claude와 함께 작업해 만들었습니다.
