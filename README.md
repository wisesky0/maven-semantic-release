# maven-semantic-release

이 플러그인은 `pom.xml`의 버전을 증가시키고 maven을 통해 `deploy` 또는 `jib:build` 타겟으로 배포할 수 있게 해주는 간단한 플러그인입니다.

릴리스 후 다음 스냅샷 버전으로 버전을 증가시키는 옵션이 있습니다.

`mvn` 명령어가 존재하는지만 확인합니다.

https://github.com/conveyal/maven-semantic-release에서 영감을 받았습니다. 다음과 같은 차이점이 있습니다:
* 다양한 maven 타겟을 허용합니다.
* 멀티모듈 프로젝트를 허용하는 옵션이 있습니다.
* 성공적인 릴리스 후 스냅샷 버전을 증가시킬 수 있습니다.
* 설정의 무결성을 검증하는 검사가 적습니다 (`pom.xml`을 확인하지 않음)

## 시작하기

* `npm i -D semantic-release @wafful-node-package/maven-semantic-release`
* `@wafful-node-package/maven-semantic-release`를 플러그인으로 추가하세요 (https://semantic-release.gitbook.io/semantic-release/usage/plugins)
* `settingsPath`를 구성하거나 예상 위치에 maven 설정 파일이 있는지 확인하세요
* 이 플러그인을 사용하려면 `@semantic-release/git` 플러그인이 이 플러그인 이후에 실행되고 `pom.xml`을 포함하도록 하세요.

## 옵션

<!-- AUTO_GENERATED_OPTIONS -->
## 타입 정의

<dl>
<dt><a href="#MavenTarget">MavenTarget</a> : <code>'deploy'</code> | <code>'package jib:build'</code> | <code>'deploy jib:build'</code></dt>
<dd></dd>
<dt><a href="#PluginConfig">PluginConfig</a> : <code>Object</code></dt>
<dd></dd>
</dl>

<a name="MavenTarget"></a>

## MavenTarget : <code>'deploy'</code> | <code>'package jib:build'</code> | <code>'deploy jib:build'</code>
**종류**: 전역 타입 정의  
<a name="PluginConfig"></a>

## PluginConfig : <code>Object</code>
**종류**: 전역 타입 정의  
**속성**

| 이름 | 타입 | 기본값 | 설명 |
| --- | --- | --- | --- |
| [settingsPath] | <code>string</code> |  | maven 설정 파일의 경로 |
| processAllModules | <code>boolean</code> | <code>false</code> | `versions:set` 타겟에 대한 `processAllModules` 옵션을 설정합니다. 멀티모듈 프로젝트에 유용합니다. |
| mavenTarget | [<code>MavenTarget</code>](#MavenTarget) | <code>'deploy'</code> | 배포에 사용되는 mvn 타겟을 결정합니다. |
| clean | <code>boolean</code> | <code>true</code> | 배포 전에 `clean` 타겟을 적용할지 여부 |
| updateSnapshotVersion | <code>boolean</code> | <code>false</code> | 릴리스 후 새로운 스냅샷 버전을 설정할지 여부 |
| snapshotCommitMessage | <code>string</code> | <code>"'chore:"</code> | 다음 스냅샷 버전 설정 [skip ci]' 새로운 스냅샷 버전을 생성할 때 사용되는 커밋 메시지 |
| debug | <code>boolean</code> | <code>false</code> | 모든 maven 호출에 대해 `-X` 옵션을 설정합니다. |
| mvnw | <code>boolean</code> | <code>false</code> | mvn 대신 mvnw 스크립트를 사용합니다 |
<!-- AUTO_GENERATED_OPTIONS -->
