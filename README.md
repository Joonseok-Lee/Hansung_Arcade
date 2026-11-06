# Hansung Univ - Network Programming

## 개발 환경

| name | description |
| :---: |:-----------:|
| Java |     21      |
 | Gradle |    9.5.1    |

## 빌드 · 실행

### JDK 21 설치
JDK 미설치 시 먼저 설치합니다. 설치되어 있다면, 건너뛰셔도 됩니다.
```bash
# macOS (Homebrew)
brew install --cask temurin@21
```

Windows의 경우
```bat
winget install EclipseAdoptium.Temurin.21.JDK
```

설치 후 `java -version`으로 확인하세요. Windows는 cmd 창을 새로 열어야 `java`를 인식합니다.

### 빌드, 실행, 테스트

```bash
# Linux, macOS, Git bash
./gradlew build                      # 컴파일 + 테스트
./gradlew run                        # 실행
./gradlew clean test                 # 캐시 없이 테스트 실행
```

`permission denied`가 나오면 `chmod +x gradlew`를 한 번 실행한 뒤 다시 시도하세요.

Windows의 경우
```bat
gradlew build
gradlew run
gradlew clean test
```

PowerShell에서는 앞에 `.\`를 붙입니다. 예: `.\gradlew build`

### 테스트 결과

`build/reports/tests/test/index.html`을 브라우저로 열면 테스트 결과를 볼 수 있습니다.

## IDE에서 열기

- **IntelliJ**: 저장소 폴더를 열면 Gradle 프로젝트로 인식합니다. 알림이 뜨면 *Load Gradle Project*를 누르세요.
- **Eclipse**: File → Import → Gradle → Existing Gradle Project에서 저장소 폴더를 선택합니다.

`.idea/`, `.project`, `.classpath`, `.settings/`는 각자 IDE가 만드는 개인 설정이라 커밋하지 않습니다.
