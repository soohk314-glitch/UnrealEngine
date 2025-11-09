# 언리얼 엔진 데일리 브리핑 | 2025년 11월 09일

**작성일시:** 2025년 11월 09일 18:04 (KST)

## 1. 핵심 요약

| 구분 | 내용 | 출처 및 게시일 |
| :--- | :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **UE 5.6.1 핫픽스** 릴리즈 (270개 이상 수정) | [포럼](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) (2025-08-12) |
| | 2. **UE 5.7 프리뷰** 공개 및 주요 기능 확정 (Substrate, MegaLights, PCG) | [포럼](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (2025-09-23) |
| | 3. **CVE-2025-55247 보안 취약점** 관련 논의 및 해결책 제시 | [포럼](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) (2025-11-06) |
| **즉시 확인 필요 사항** | **CVE-2025-55247** 취약점: UE 5.4, 5.5, 5.6 버전에서 `Microsoft.Build` NuGet 패키지 관련 보안 문제가 보고되었습니다. Epic Games Launcher를 통해 배포된 바이너리에 영향을 미치며, 개발자 커뮤니티에서 임시 해결책이 논의되었습니다. | [포럼](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) (2025-11-06) |

## 2. 공식 릴리즈 및 패치

| 버전 릴리즈 | 주요 변경사항 및 Breaking Changes | 릴리즈 노트 URL |
| :--- | :--- | :--- |
| **Unreal Engine 5.6.1 Hotfix** | **270개 이상의 수정 사항** 포함. 특히 **MetaHuman Character (MHC)** 관련 다수의 버그 및 크래시가 수정되었습니다. | [5.6.1 Hotfix Released](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) |
| **Breaking Change (UE 5.7 예정)** | **UE 5.7**부터 Linux는 **SDL2에서 SDL3로 전환**될 예정입니다. SDL2 코드를 커스터마이징한 사용자는 변경 사항을 재작업해야 합니다. | [5.6.1 Hotfix Released](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) |

## 3. 버그 및 이슈

| 구분 | 내용 | Issue Tracker URL |
| :--- | :--- | :--- |
| **새로 보고된 주요 버그 (2025-11-07)** | - **Sequencer/Level Instance:** 시퀀서 재생 중 "Visualize Level Instance Editing"이 기본값으로 켜지는 문제. | [Issue Tracker](https://issues.unrealengine.com/issue/search) |
| | - **Rendering/Ray Tracing (5.6):** 섹션이 비활성화된 스켈레탈 메시가 레이 트레이싱 씬에서 깜빡이는 현상. | [Issue Tracker](https://issues.unrealengine.com/issue/search) |
| | - **World Partition/Terrain:** 부분적으로 로드된 월드 파티션 레벨의 랜드스케이프 스플라인이 나나이트 랜드스케이프 무효화를 유발할 수 있음. | [Issue Tracker](https://issues.unrealengine.com/issue/search) |
| **수정된 버그** | 최근 7일간 공식적으로 수정되어 릴리즈된 버그는 없습니다. (가장 최근 핫픽스는 5.6.1, 2025년 8월 12일 릴리즈) | [Issue Tracker](https://issues.unrealengine.com/issue/search) |
| **Workaround (CVE-2025-55247)** | `Microsoft.Build` NuGet 패키지를 수동으로 업데이트하고, 관련 `.csproj` 파일의 읽기 전용 속성을 해제합니다. (예: UE 5.5.4의 경우 `17.11.4`에서 `17.11.28`로 업데이트) | [포럼](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) |

## 4. GitHub 업데이트

| 구분 | 내용 | GitHub URL |
| :--- | :--- | :--- |
| **주요 커밋 및 Pull Request** | 최근 7일간 EpicGames/UnrealEngine 공식 저장소의 주요 커밋 활동은 검색되지 않았습니다. | [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) |
| **영향받는 시스템** | 최신 정보 없음. | - |

## 5. 공식 포럼 기술 논의

| 스레드 제목 | 주요 내용 | 포럼 URL |
| :--- | :--- | :--- |
| **update currently distributed Engine versions to address CVE-2025-55247 effecting [5.4],[5.5],[5.6]** | UE 5.4, 5.5, 5.6 버전의 `Microsoft.Build` NuGet 패키지 관련 보안 취약점 (CVE-2025-55247)에 대한 개발자 커뮤니티의 논의 및 임시 해결책 제시. | [포럼 스레드](https://forums.unrealengine.com/t/update-currently-distributed-engine-versions-to-address-cve-2025-55247-effecting-5-4-5-5-5-6/2672485) |

## 6. 신기능 및 실험적 기능

| 구분 | 내용 | 출처 |
| :--- | :--- | :--- |
| **새로 추가된 기능 (UE 5.7 Preview)** | **Substrate** (Beta에서 정식 기능으로 전환 예정), **MegaLights** (Beta), **Procedural Vegetation Editor**, **Nanite Foliage** 등. | [UE 5.7 Preview](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) |
| **Beta/Experimental 기능 및 주의사항** | **Substrate**는 UE 5.7에서 기본으로 활성화되는 모듈식, 물리 기반 머티리얼 프레임워크입니다. **MegaLights**는 개선된 성능과 기능을 제공합니다. | [UE 5.7 Preview](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) |
| **성능 영향도** | UE 5.7은 **PCG (Procedural Content Generation)** 옵션의 개선과 **Nanite Foliage**를 통해 대규모 오픈 월드에서 60 FPS를 목표로 성능 향상을 제공할 것으로 예상됩니다. | [UE 5.7 Preview](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) |

## 7. 플러그인 및 문서 업데이트

| 구분 | 내용 | 출처 |
| :--- | :--- | :--- |
| **공식 플러그인 업데이트** | **MetaHuman Character (MHC)** 플러그인 관련 다수의 버그 수정이 5.6.1 핫픽스에 포함되었습니다. (예: MHC 비호환 의상/그룸 사용 가능 문제, UEFN 익스포트 문제 등) | [5.6.1 Hotfix Released](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) |
| **문서 주요 변경사항** | 최근 7일간 공식 문서의 주요 변경사항은 검색되지 않았습니다. | - |
