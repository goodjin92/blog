---
title: "Flutter 개발 환경 구축 중 Android Studio 에러 발생 및 해결"
date: 2023-01-23T23:00:00+09:00
categories: ["Flutter"]
tags: ["Flutter", "AndroidStudio"]
draft: false
---



## 개발환경

- OS : Windows 11 (x64)
- 개발환경 : Android Studio Electric Eel (2022.1.1), Powershell
- 언어 : Dart(Flutter)





## 문제점

- Flutter 개발 환경 구축 중 안드로이드 스튜디오 관련 발생한 문제 핵심 요약 (아래 코드)

```powershell
# Android toolchain 문제
No Java Development Kit (JDK) found;

# Android Studio 문제
Unable to find bundled Java version
```





## 재현

1. Flutter SDK 다운로드, Android Studio 최신 버전 다운로드
2. Powershell > flutter doctor 실행
3. 아래처럼 No Java Development Kit (JDK) found; 문제 발생

![Android Studio 설치 이슈 해결_1](https://user-images.githubusercontent.com/86005692/214060862-e8d417c7-4fa2-422a-bd9f-0cc499d24b33.png)

```powershell
[!] Android toolchain - develop for Android devices (Android SDK version 33.0.1)
    X No Java Development Kit (JDK) found; You must have the environment variable JAVA_HOME set and the java binary in
      your PATH. You can download the JDK from <https://www.oracle.com/technetwork/java/javase/downloads/>.

···

[!] Android Studio (version 2022.1)
    X Unable to find bundled Java version.
```





## 해결방법

- C:\Program Files\Android\Android Studio에 접속한 뒤 jbr 폴더 안에 있는 파일들을 복사하여, jre 폴더로 붙여넣기해서 해결

![Android Studio 설치 이슈 해결_2](https://user-images.githubusercontent.com/86005692/214061157-fc2cbe5f-d484-4af4-8b68-c34a2e64f63f.png)

- 다양한 명령어를 사용하는 등의 다른 해결방안들도 있는 것 같은데 아직 실력이 부족하여 가장 간편한 방법으로 해결
