# 언리얼 엔진 데일리 브리핑 | 2025년 12월 18일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7.1 핫픽스 릴리즈**: 약 100여 개의 버그 및 업데이트 포함 [1]. 2. **Substrate 프로덕션 준비 완료**: 모듈식 머티리얼 시스템인 Substrate가 정식 기능으로 전환 [2]. 3. **PCG 프레임워크 프로덕션 준비 완료**: Procedural Content Generation (PCG) 프레임워크가 정식 기능으로 전환 [2]. |
| **즉시 확인 필요 사항** | - **UE 5.7.1 핫픽스 적용**: 5.7.0에서 보고된 다수의 크래시 및 버그가 수정되었으므로, 5.7.x 버전을 사용하는 개발팀은 즉시 5.7.1로 업데이트하는 것을 권장 [1]. - **Linux SDL3 전환**: UE 5.7부터 Linux 환경에서 SDL2가 SDL3로 전환되었으므로, 관련 커스터마이징 코드를 사용하는 경우 재작업 필요 [1]. |
| **출처 URL 및 게시일 (YYYY-MM-DD)** | - Unreal Engine 5.7.1 Hotfix Released: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) - Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

| 구분 | 내용 |
| :--- | :--- |
| **버전 릴리즈 (정확한 버전 번호)** | **Unreal Engine 5.7.1** (Hotfix) |
| **주요 변경사항 및 Breaking Changes** | - **약 100여 개의 버그 수정 및 업데이트** 포함 [1]. - **Linux 환경의 SDL2 → SDL3 전환**이 UE 5.7부터 적용되었으며, 관련 커스터마이징 코드는 SDL3에 맞게 수정해야 함 [1]. |
| **릴리즈 노트 URL** | [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) |

## 3. 버그 및 이슈

| 구분 | 내용 |
| :--- | :--- |
| **새로 보고된 주요 버그** | - **Substrate의 Coverage Node 문제**: Unlit Emissive 부분의 Coverage Node가 마스크된 픽셀을 건너뛰지 않아 최적화에 문제가 발생 [3]. - **에디터 로컬라이제이션 문제**: 에디터 언어를 다른 언어(예: 한국어, 중국어)로 설정할 경우 `GetLinkedAnimLayerInstanceByGroup` 함수가 올바른 `LinkedAnimLayer`를 검색하지 못함 [3]. |
| **수정된 버그 (UE 5.7.1 주요 수정)** | - **UE-348441**: NVIDIA 그래픽 드라이버 581 버전 이상에서 발생하는 DoF(Depth of Field) 깜빡임 현상 수정 [1]. - **UE-349638**: PCG(Procedural Content Generation)가 PIE(Play In Editor)에서 생성될 때 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배로 증가하는 문제 수정 [1]. - **UE-349535**: `megalight=1`, `Substrate=1`, `GBufferFormat=1` 설정에서 발생하는 크래시 수정 [1]. - **UE-350131**: 오디오 스트림 캐시(Audio StreamCache)의 메모리 누수 문제 수정 [1]. |
| **Workaround** | - **DoF 깜빡임**: NVIDIA 드라이버를 581 미만 버전으로 다운그레이드하거나, 5.7.1 핫픽스를 적용 [1]. |
| **Issue Tracker URL** | [https://issues.unrealengine.com/](https://issues.unrealengine.com/) |

## 4. GitHub 업데이트

| 구분 | 내용 |
| :--- | :--- |
| **주요 커밋 및 Pull Request** | - **최근 7일간 EpicGames/UnrealEngine 저장소의 직접적인 주요 커밋 활동은 검색되지 않았습니다.** (일반적으로 릴리즈 직후에는 핫픽스 관련 커밋이 주를 이루며, 주요 기능 개발은 비공개 브랜치에서 진행될 수 있음) [4]. - **UE-347106** (UE 5.7.1 핫픽스에 포함): GitHub PR 13887을 통해 `Loadmap` 시 치명적인 Assert를 피하기 위해 `pending-delete Virtual Texture`를 즉시 해제하도록 수정 [1]. - **UE-350545** (UE 5.7.1 핫픽스에 포함): GitHub PR 13964를 통해 Vulkan에서 `Split Barriers`를 사용할 때 `VkEvent` 핸들 누수 문제 수정 [1]. |
| **영향받는 시스템** | - 렌더링 시스템 (Virtual Texture, Vulkan) |
| **GitHub URL** | [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) |

## 5. 공식 포럼 기술 논의

| 구분 | 내용 |
| :--- | :--- |
| **Epic Staff 답변 기술 스레드** | - **Unreal Engine 5.7.1 Hotfix Released**: Epic Staff인 Tina_Wisdom이 5.7.1 핫픽스 릴리즈를 공식 발표하고 피드백을 요청 [1]. - **Epic's Picks Requirements & Documentation Refresh**: Epic Staff가 Epic's Picks 문서 업데이트 및 Q1 우선순위 장르/테마에 대한 정보를 공유 [5]. |
| **포럼 URL** | [https://forums.unrealengine.com/](https://forums.unrealengine.com/) |

## 6. 신기능 및 실험적 기능

| 구분 | 내용 |
| :--- | :--- |
| **새로 추가된 기능 (UE 5.7 기준)** | - **PCG (Procedural Content Generation) 프레임워크**가 **프로덕션 준비 완료** 상태로 전환 [2]. - **Substrate** 모듈식 머티리얼 시스템이 **프로덕션 준비 완료** 상태로 전환 [2]. - **에디터 내 AI Assistant** 기능 추가 (F1 키로 컨텍스트 기반 도움말, C++ 코드 생성 등) [2]. |
| **Beta/Experimental 기능 및 주의사항** | - **Nanite Foliage** 시스템 (Experimental): Nanite Voxels를 사용하여 밀집된 환경을 효율적으로 렌더링 [2]. - **MegaLights** (Beta): 동적 그림자를 드리우는 광원을 더 많이 지원하여 사실적인 부드러운 그림자 구현 [2]. - **Windows arm64 및 arm64ec 지원** (Experimental): 런처 에디터에서는 지원되지 않으며, 전체 소스 빌드에서만 가능 [2]. |
| **성능 영향도** | - UE 5.7은 전반적인 성능 향상과 스터터링 감소를 목표로 하며, 특히 PCG와 Nanite Foliage를 통해 대규모 환경 렌더링 효율성이 크게 개선됨 [2]. |

## 7. 플러그인 및 문서 업데이트

| 구분 | 내용 |
| :--- | :--- |
| **공식 플러그인 업데이트** | - **MetaHuman Creator Unreal Engine 플러그인**이 **Linux 및 macOS**에서 사용 가능 [2]. - **EOS (Epic Online Services)**: 1.18.1.2 바이너리 업데이트 [1]. |
| **문서 주요 변경사항** | - **Epic's Picks 문서 업데이트**: 최신 요구 사항 및 Q1 우선순위 장르/테마 반영 [5]. - **Android XR 개발 문서 업데이트**: Android XR 개발을 위한 Unreal Engine 공식 문서가 2025-12-12 UTC에 업데이트됨 [6]. |

***

### 참고 자료 (References)

[1] **5.7.1 Hotfix Released** (2025-12-02) - Epic Developer Community Forums: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
[2] **Unreal Engine 5.7 Release Notes** (2025-11-12) - Epic Developer Community: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[3] **Unreal Engine Issues and Bug Tracker** - Epic Games: [https://issues.unrealengine.com/](https://issues.unrealengine.com/)
[4] **EpicGames/UnrealEngine GitHub** - GitHub: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)
[5] **Epic's Picks Requirements & Documentation Refresh** (2025-12-17) - Epic Developer Community Forums: [https://forums.unrealengine.com/t/epic-s-picks-requirements-documentation-refresh/2685704](https://forums.unrealengine.com/t/epic-s-picks-requirements-documentation-refresh/2685704)
[6] **Develop with Unreal Engine for Android XR** (Last updated 2025-12-12 UTC) - Android Developer: [https://developer.android.com/develop/xr/unreal](https://developer.android.com/develop/xr/unreal)
