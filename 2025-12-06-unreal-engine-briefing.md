# 언리얼 엔진 데일리 브리핑 | 2025년 12월 06일

## 1. 핵심 요약

- **주요 업데이트 상위 3개**
    1.  **UE 5.7.1 핫픽스 출시:** 100개에 가까운 버그 수정 및 업데이트가 포함된 핫픽스가 3일 전(12월 2일)에 출시되었습니다. [^1]
    2.  **PCG GPU 기능 Beta 전환:** Procedural Content Generation(PCG)의 GPU 구현이 Experimental에서 **Beta** 단계로 전환되어 안정성이 향상되었습니다. [^4]
    3.  **Mover 플러그인 업데이트:** Game Animation Sample Project 업데이트와 함께 Mover 플러그인이 롤백 네트워킹을 지원하는 등 모듈식 액터 이동을 위한 핵심 기능으로 자리 잡고 있습니다. [^2]

- **즉시 확인 필요 사항**
    *   **UE 5.7 사용자:** 5.7.1 핫픽스에서 **Cinematic MetaHumans의 AMD GPU 충돌** 및 **Path Tracing 사용 시 에디터 응답 없음** 등 주요 렌더링/GPU 관련 크래시가 수정되었습니다. 해당 이슈를 겪고 있다면 즉시 업데이트를 권장합니다. [^1]
    *   **Linux 개발자:** UE 5.7부터 Linux는 SDL2에서 SDL3로 전환되었습니다. SDL2 코드를 커스터마이징한 경우 SDL3에 맞게 변경 사항을 재작업해야 합니다. [^1]

- **출처 URL 및 게시일 (YYYY-MM-DD)**
    *   5.7.1 Hotfix Released: `https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235` (2025-12-02)
    *   Game Animation Sample Project Update: `https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7` (2025-12-04)

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈 (정확한 버전 번호)**
    *   **Unreal Engine 5.7.1 Hotfix**

- **주요 변경사항 및 Breaking Changes**
    *   **주요 수정 사항:** 약 100여 개의 버그 및 크래시가 수정되었습니다.
    *   **Linux SDL 전환:** UE 5.7부터 Linux 빌드에서 SDL2가 SDL3로 대체되었습니다. 기존 SDL2 커스터마이징 코드는 SDL3에 맞게 업데이트가 필요합니다.

- **릴리즈 노트 URL**
    *   `https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235`

## 3. 버그 및 이슈

- **새로 보고된 주요 버그**
    *   최근 7일 이내에 5.7.1 핫픽스보다 더 중요한 새로운 주요 버그 보고는 확인되지 않았습니다.

- **수정된 버그 (5.7.1 Hotfix 주요 수정)**
    | UE Issue ID | Summary | Affected System |
    | :--- | :--- | :--- |
    | UE-193929 | Path Tracing + mGPU 사용 시 에디터 응답 없음 | Rendering, mGPU |
    | UE-227868 | Cinematic MetaHumans 사용 시 AMD GPU 크래시 | Rendering, MetaHuman |
    | UE-349535 | `megalight=1`, `Substrate=1`, `GBufferFormat=1` 설정에서 크래시 | Rendering, Substrate |
    | MH-16702 | MetaHuman Character LOD 변경 후 여러 플랫폼에서 크래시 | MetaHuman |
    | UE-352089 | Full Body IK Solver에 IK Goal 추가 시 크래시 | Animation, Control Rig |

- **Workaround**
    *   5.7.1 핫픽스 설치를 통해 대부분의 알려진 주요 크래시 및 버그를 해결할 수 있습니다.

- **Issue Tracker URL**
    *   `https://issues.unrealengine.com/`

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**
    *   EpicGames/UnrealEngine 공식 저장소의 `ue5-main` 브랜치에는 매일 수십 건의 커밋이 발생하고 있으나, 최근 7일간 5.7.1 핫픽스에 포함된 내용 외에 실무 개발자에게 즉각적인 영향을 미치는 대규모 변경 사항은 외부에 공개된 요약 정보에서 확인되지 않았습니다.
    *   **참고:** 공식 저장소는 수시로 업데이트되므로, 최신 개발 브랜치(`ue5-main`)를 사용하는 개발자는 정기적인 Pull/Merge가 필요합니다.

- **영향받는 시스템**
    *   주로 버그 수정 및 안정화 작업이 진행 중이며, 특정 시스템에 대한 대규모 기능 추가는 5.7.1 핫픽스 내용에 집중되어 있습니다.

- **GitHub URL**
    *   `https://github.com/EpicGames/UnrealEngine`

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**
    *   최근 7일 이내에 Epic Staff가 답변한 새로운 주요 기술 논의 스레드는 확인되지 않았습니다.
    *   가장 최근의 공식 발표는 **5.7.1 Hotfix Released** 공지 스레드입니다. [^1]

- **포럼 URL**
    *   `https://forums.unrealengine.com/`

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능**
    *   **Mover 플러그인:** 모듈식 액터 이동을 지원하며, 롤백 네트워킹을 활용할 수 있도록 업데이트되었습니다. [^2]

- **Beta/Experimental 기능 및 주의사항**
    *   **PCG GPU (Beta):** Procedural Content Generation의 GPU 구현이 **Beta** 단계로 격상되었습니다. 이는 성능 최적화 및 대규모 월드 생성에 중요한 진전입니다.
    *   **Nanite Foliage (Experimental):** 나나이트를 활용한 복셀 기반의 폴리지 렌더링 시스템이 Experimental 기능으로 제공됩니다. 대규모 환경에서 고밀도 폴리지를 효율적으로 처리할 수 있으나, 성능 영향도에 대한 테스트가 필요합니다. [^3]

- **성능 영향도**
    *   PCG GPU의 Beta 전환은 대규모 콘텐츠 생성 시 성능 향상을 기대할 수 있습니다.
    *   Nanite Foliage는 고밀도 폴리지의 렌더링 효율을 높이지만, Experimental 기능이므로 실제 프로젝트 적용 전 성능 테스트가 필수입니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**
    *   **Mover 플러그인**의 기능 개선 및 안정화 업데이트가 진행되었습니다. [^2]
    *   **ArcGIS Maps SDK for Unreal Engine**이 2.2 릴리즈로 업데이트되었습니다. [^5]

- **문서 주요 변경사항**
    *   Unreal Engine 5.7 문서가 업데이트되었으며, 특히 Mover 플러그인 및 Nanite Foliage에 대한 새로운 문서가 추가되었습니다.

## 참고 자료 (References)

[^1]: [5.7.1 Hotfix Released - Announcements](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
[^2]: [Explore the updates to the Game Animation Sample Project in UE 5.7](https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7)
[^3]: [Nanite Foliage | Unreal Engine 5.7 Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/nanite-foliage)
[^4]: [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[^5]: [Release notes | ArcGIS Maps SDK for Unreal Engine](https://developers.arcgis.com/unreal-engine/release-notes/release-notes-2-2-0/)
