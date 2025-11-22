# 언리얼 엔진 데일리 브리핑 | 2025년 11월 08일

## 1. 핵심 요약

| 구분 | 내용 | 출처 URL | 게시일 (KST) |
| :--- | :--- | :--- | :--- |
| **주요 업데이트 1** | **Unreal Engine 5.7 Preview** 공개. PCG(Procedural Content Generation Framework)가 Production-Ready로 전환되었으며, 성능이 크게 향상되었습니다. | [1] | 2025-09-23 |
| **주요 업데이트 2** | **Substrate** 머티리얼 시스템이 정식 버전(Production-Ready)으로 전환되어, 모듈식 셰이딩과 물리적으로 정확한 다중 레이어 머티리얼 조합이 가능해졌습니다. | [1] | 2025-09-23 |
| **주요 업데이트 3** | **Unreal Engine 5.6.1 Hotfix** 출시. 270개 이상의 버그 수정 및 업데이트가 포함되었습니다. | [2] | 2025-08-12 |
| **즉시 확인 필요 사항** | UE 5.7부터 Linux 빌드 환경이 SDL2에서 **SDL3**로 전환될 예정입니다. SDL2 코드를 커스터마이징한 사용자는 변경 사항을 미리 확인해야 합니다. | [2] | 2025-08-12 |

## 2. 공식 릴리즈 및 패치

### 버전 릴리즈

*   **최신 Preview 버전:** Unreal Engine **5.7 Preview**
    *   **릴리즈 노트 URL:** [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) [1]
*   **최신 Hotfix 버전:** Unreal Engine **5.6.1 Hotfix**
    *   **릴리즈 노트 URL:** [https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) [2]

### 주요 변경사항 및 Breaking Changes (5.6.1 Hotfix 기준)

5.6.1 핫픽스는 주로 안정성 개선 및 버그 수정에 초점을 맞추고 있으며, 270개 이상의 수정 사항이 포함되었습니다.

*   **MetaHuman 관련 수정:** MetaHuman Character, MetaHuman Performance, MetaHuman CoreTechLib 등 MetaHuman 파이프라인 전반의 크래시 및 에셋 관련 문제가 다수 수정되었습니다. (예: `MH-15649`, `MH-15650`, `MH-15718` 등)
*   **에디터 및 엔진 안정성:** 에디터 크래시 (`UE-274151`, `UE-282917`), 씬 뷰포트 크래시 (`UE-289496`) 등 다양한 안정성 문제가 해결되었습니다.
*   **향후 Breaking Change 예고 (UE 5.7):** Linux 환경에서 SDL2가 SDL3로 전환될 예정입니다. SDL2 관련 커스터마이징 코드는 UE 5.7 정식 출시 전에 SDL3에 맞게 수정해야 합니다.

## 3. 버그 및 이슈

### 새로 보고된 주요 버그 및 수정된 버그

최근 7일간의 이슈 트래커 업데이트는 확인되지 않았습니다. 가장 최근의 공식적인 버그 수정은 **5.6.1 Hotfix**에 포함되어 있습니다.

| 이슈 ID | 요약 | 상태 | 버전 |
| :--- | :--- | :--- | :--- |
| `UE-282213` | PCG self pruning 및 복잡한 충돌 사용 시 에디터 크래시 | 수정됨 (5.6.1) | 5.6 |
| `UE-284851` | Chains가 Spherical Collisions에서 튕겨나가는 문제 | 수정됨 (5.6.1) | 5.6 |
| `UE-290599` | Modular Control Rig 레벨 시퀀스에서 Undo/Redo 시 크래시 | 수정됨 (5.6.1) | 5.6 |
| `MH-15718` | 로그아웃 상태에서 UEMHC(Unreal Engine MetaHuman Creator)에서 텍스처 다운로드 시 크래시 | 수정됨 (5.6.1) | 5.6 |

### Workaround

5.6.1 핫픽스에 대한 특정 Workaround는 공식적으로 제공되지 않았습니다. 핫픽스 이후 발생하는 문제는 [버그 제출 양식](https://www.unrealengine.com/en-US/support/report-a-bug)을 통해 보고하는 것이 권장됩니다.

### Issue Tracker URL

*   **Unreal Engine Issue and Bug Tracker:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/) [3]

## 4. GitHub 업데이트

GitHub의 EpicGames/UnrealEngine 저장소의 최신 커밋 활동은 실시간으로 변동되므로, 주요 커밋 및 Pull Request는 **Unreal Engine 5.7 Preview** 릴리즈를 기준으로 요약합니다.

*   **주요 커밋 및 Pull Request:** 5.7 Preview는 수많은 커밋을 통해 PCG, Substrate, Animation 등 핵심 기능의 개선 및 안정화 작업을 진행했습니다.
*   **영향받는 시스템:** Procedural Content Generation (PCG), Substrate Materials, Animation/Rigging Tools, MetaHuman.
*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) [4]

## 5. 공식 포럼 기술 논의

### Epic Staff 답변 기술 스레드

가장 최근의 Epic Staff 활동은 **Unreal Engine 5.7 Preview** 및 **5.6.1 Hotfix** 공지 스레드에서 확인되었습니다.

*   **Unreal Engine 5.7 Preview** ([https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) [1]): TinaWisdom (Epic Staff)이 릴리즈 내용을 발표하고 커뮤니티 피드백을 모니터링하고 있습니다.
*   **5.6.1 Hotfix Released** ([https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) [2]): TinaWisdom (Epic Staff)이 핫픽스 내용을 공유하고 있습니다.

### 포럼 URL

*   **Epic Developer Community Forums:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/) [5]

## 6. 신기능 및 실험적 기능

### 새로 추가된 기능 (UE 5.7 Preview 기준)

*   **PCG Production-Ready:** PCG 프레임워크가 정식 버전으로 전환되었으며, GPU 성능이 대폭 향상되었습니다.
*   **Substrate Production-Ready:** Substrate 머티리얼 시스템이 정식 버전으로 전환되어, 복잡한 셰이딩 모델을 모듈식으로 구성할 수 있게 되었습니다.

### Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview 기준)

| 기능 | 상태 | 주요 내용 | 주의사항 |
| :--- | :--- | :--- | :--- |
| **Procedural Vegetation Editor** | Experimental | Fab 에셋을 사용하여 Nanite-ready 폴리지(Foliage)를 에디터 내에서 실시간으로 생성 및 커스터마이징 | **Experimental** 기능이므로 프로덕션 사용에 주의 필요 |
| **Nanite Foliage** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxel 시스템을 활용하여 고밀도 폴리지를 60fps로 렌더링 | **Experimental** 기능이므로 프로덕션 사용에 주의 필요 |
| **MegaLights** | Beta | 디렉셔널 라이트, Niagara 파티클 라이트, 반투명 라이팅 지원. 성능 튜닝 컨트롤 추가. | **Beta** 기능으로, 정식 버전이 아니므로 안정성 검토 필요 |
| **Animation/Rigging Tools** | Experimental | Selection Sets, Animation mode refactor, Constraint UX 통합, Skeletal Editor의 블렌드 셰이프/스컬프팅 기능 추가 | **Experimental** 기능이므로 프로덕션 사용에 주의 필요 |

### 성능 영향도

*   **PCG:** GPU 성능 최적화로 UE 5.5 대비 약 2배 빠른 속도를 제공합니다.
*   **Nanite Foliage:** Nanite 시스템을 활용하여 고밀도 폴리지를 효율적으로 렌더링하여 성능 향상을 목표로 합니다.

## 7. 플러그인 및 문서 업데이트

### 공식 플러그인 업데이트 (UE 5.7 Preview 기준)

*   **MetaHuman Creator Plugin:** Linux 및 macOS 지원이 추가되었습니다.
*   **MetaHuman Creator Python and Blueprint API:** MetaHuman 캐릭터 에셋의 편집 및 조립 작업을 스크립트로 처리할 수 있는 API가 추가되었습니다.

### 문서 주요 변경사항

*   **Unreal Engine 5.7 Preview Documentation** 업데이트가 진행 중입니다.
*   **PCG** 및 **Substrate** 기능의 Production-Ready 전환에 따라 관련 문서의 내용이 대폭 업데이트되었을 것으로 예상됩니다.

***

### 참고 자료 (References)

[1] [Unreal Engine 5.7 Preview - General / Announcements - Epic Developer Community Forums](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)
[2] [5.6.1 Hotfix Released - General / Announcements - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316)
[3] [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)
[4] [EpicGames/UnrealEngine on GitHub](https://github.com/EpicGames/UnrealEngine)
[5] [Epic Developer Community Forums](https://forums.unrealengine.com/)
