# 언리얼 엔진 데일리 브리핑 | 2025년 12월 20일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate Materials** 정식 버전 전환 (UE 5.7) <br> 2. **PCG(Procedural Content Generation)** 프레임워크 정식 버전 전환 (UE 5.7) <br> 3. **Microsoft GDK Plug-ins** 공식 지원 (최근 7일 이내) |
| **즉시 확인 필요 사항** | **UE 5.7.1 핫픽스**에서 100여 개의 버그가 수정되었으며, 특히 **Path Tracing, MetaHuman, Control Rig** 관련 크래시 수정 사항을 확인해야 합니다. 또한, Linux 사용자는 **SDL2에서 SDL3로의 전환**에 따른 코드 변경이 필요할 수 있습니다. |
| **출처 URL 및 게시일** | UE 5.7.1 Hotfix: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) <br> Microsoft GDK Plug-ins: [https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/](https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/) (2025-12-12) |

---

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes:**
    - **약 100여 개의 버그 및 업데이트**가 포함된 핫픽스입니다.
    - **주요 수정 사항:** Path Tracing 뷰 모드 사용 시 에디터 멈춤 현상, MetaHuman 시네마틱 관련 AMD GPU 크래시, Control Rig 에디터 크래시, PCG 관련 크래시 및 성능 문제 등이 해결되었습니다.
    - **Linux Breaking Change (UE 5.7 기준):** Linux 빌드는 SDL2에서 SDL3로 전환되었습니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 코드를 수정해야 합니다.
- **릴리즈 노트 URL:** [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

---

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (최근 24시간 이내):**
    - `r.SSR.Stencil` 활성화 시 잘못된 로직 관찰 (Graphics Features)
    - `.zfprj` 임포트 중 특정 설정에서 크래시 발생 (RS - Alignment)
    - `AsyncLoadingThread`에서 `UObject` 재구성으로 인한 `Subobject ComponentClass` 오버라이드 어설션 실패 (Framework - Blueprint)
- **수정된 버그 (최근 24시간 이내):**
    - `DynamicSubobjectInstancing` 및 `NonNativeInstancedSubobjects` 자동화 테스트 실패 문제 해결 (Framework)
    - `ActorPosition` 머티리얼 노드 사용 시 Nanite ISM의 잘못된 모션 벡터 문제 해결 (Graphics Features)
    - `Affect Indirect Lighting While Hidden` 활성화 시 아웃라이너 눈 아이콘으로 스태틱 메시 숨기기 실패 문제 해결 (Rendering Architecture)
- **Workaround:**
    - 5.7/5.7.1 버전에서 DDC 캐시 오류 발생 시, `C:\Users\[YourUsername]\AppData\Local\UnrealEngine\Common` 경로의 UnrealEngine 폴더를 삭제하는 방법이 포럼에서 논의되고 있습니다. (비공식)
- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

---

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - 최근 7일간 EpicGames/UnrealEngine 공식 저장소의 **main 브랜치에 대한 주요 기술 커밋은 확인되지 않았습니다.**
    - **관련 업데이트:** Epic Games에서 제공하는 **Unreal Engine 런타임 Docker 이미지**가 1년 이상 오래된 버전이었으나, 최근 **업데이트**되었다는 포럼 공지가 있었습니다. 이는 컨테이너 기반 개발 환경 사용자에게 중요한 변경 사항입니다.
- **영향받는 시스템:** 컨테이너 기반 빌드 시스템, CI/CD 파이프라인
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) (소스 코드)

---

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **"5.7.1 Hotfix Released"** 스레드에서 Epic Staff가 핫픽스에 대한 공식적인 정보를 제공하고 사용자 피드백을 받고 있습니다.
    - **주요 논의 사항:** 5.7.1 핫픽스에서 해결된 다양한 크래시 및 버그에 대한 사용자 경험 공유.
- **포럼 URL:** [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

---

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준):**
    - **Substrate Materials** 정식 버전 전환: 모듈형 물리 기반 머티리얼 프레임워크.
    - **PCG Framework** 정식 버전 전환: 프로시저럴 콘텐츠 제작을 위한 강력한 툴셋.
- **Beta/Experimental 기능 및 주의사항 (UE 5.7 기준):**
    - **Nanite Foliage and Skinning (실험 단계):** 폴리지 인스턴스 및 스키닝 메시를 위한 나나이트 지원 강화.
    - **주의사항:** 실험 단계 기능은 프로덕션 환경에서 사용 시 예기치 않은 문제나 API 변경이 발생할 수 있습니다.
- **성능 영향도:**
    - UE 5.7은 전반적인 CPU 및 GPU 성능 향상에 중점을 두었으며, 특히 **프레임 시간 안정성**과 **루멘(Lumen)의 품질 향상**이 보고되었습니다.

---

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **Microsoft GDK Plug-ins for Unreal Engine** 공식 출시: Xbox PC App으로 게임을 가져오는 프로세스를 간소화합니다.
- **문서 주요 변경사항:**
    - 최근 7일간 공식 문서의 주요 기술적 변경사항은 확인되지 않았으나, **UE 5.7 문서**가 최신 기술(Substrate, PCG 등)에 맞춰 업데이트되었습니다.
- **Microsoft GDK Plug-ins URL:** [https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/](https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/)
