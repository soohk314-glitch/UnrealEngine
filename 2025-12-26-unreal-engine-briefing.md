# 언리얼 엔진 데일리 브리핑 | 2025년 12월 26일

실무 개발자를 위한 언리얼 엔진의 최신 기술 업데이트 및 이슈 보고서입니다.

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 (상위 3개)** | 1. **UE 5.7.1 핫픽스 릴리즈:** 약 100개의 버그 및 업데이트 포함 (2025년 12월 2일). 2. **UE 5.7 주요 기능:** MegaLights (Beta), Nanite Foliage & Skinning (Experimental), Substrate (Production-Ready) 등 최신 기술 동향. 3. **최신 버그 보고:** `r.SSR.Stencil` 활성화 시 렌더링 로직 오류 (2025년 12월 19일 보고). |
| **즉시 확인 필요 사항** | **UE 5.7.1 핫픽스 적용:** 에디터 충돌, Cinematic MetaHumans 관련 AMD GPU 충돌, PCG 렌더링 비용 증가 등 주요 버그가 수정되었으므로, 5.7 사용자는 핫픽스 적용을 권장합니다. |
| **출처 URL 및 게시일** | [UE 5.7.1 Hotfix Released](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) [Unreal Engine Issues](https://issues.unrealengine.com/) (최신 업데이트 2025-12-19) [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

**최신 공식 릴리즈: Unreal Engine 5.7.1 Hotfix**

| 구분 | 상세 내용 |
| :--- | :--- |
| **버전 번호** | 5.7.1 |
| **릴리즈 일자** | 2025년 12월 2일 |
| **주요 변경사항** | 약 100개의 버그 및 업데이트가 포함되었습니다. 주요 수정 사항은 다음과 같습니다: - **렌더링/GPU:** Path Tracing 사용 시 에디터 응답 없음, Cinematic MetaHumans 사용 시 AMD GPU 충돌, `r.SSR.Stencil` 관련 버그 수정. - **PCG:** PIE(Play In Editor) 시 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배가 되는 문제 수정. - **애니메이션:** Control Rig 관련 충돌 및 버그 수정. - **기타:** nDisplay, Audio, EOS 등 다양한 컴포넌트의 안정성 개선. |
| **Breaking Changes** | UE 5.7부터 Linux 환경에서 SDL2가 SDL3로 전환되었습니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경해야 합니다. |
| **릴리즈 노트 URL** | [5.7.1 Hotfix Released](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) |

## 3. 버그 및 이슈

| 구분 | 이슈 ID | 요약 | Workaround/상태 |
| :--- | :--- | :--- | :--- |
| **새로 보고된 주요 버그** | UE-193929 | `r.SSR.Stencil` 활성화 시 로직 오류: 높은 거칠기(roughness) 영역이 무시되지 않고 Unlit 머티리얼이 잘못 처리됨. | Unresolved (2025-12-19 보고) |
| | UE-227868 | UE 5.7.1에서 `Class.h`의 Cooker Assert 오류 발생. | Unresolved (2025-12-18 보고) |
| | UE-250430 | 뷰포트에서 궤도/줌 탐색 시 지속적인 끊김 현상 (stuttering) 발생. | Unresolved (2025-12-17 보고) |
| **수정된 버그 (5.7.1 Hotfix)** | UE-349638 | **PCG:** PIE 시 에디터와 게임 월드 동시 렌더링으로 인한 렌더링 비용 2배 증가 문제. | Fixed (5.7.1) |
| | UE-349535 | `megalight=1`, `Substrate=1`, `GBufferFormat=1` 설정 시 충돌 문제. | Fixed (5.7.1) |
| | UE-348441 | NVIDIA 그래픽 드라이버 581 버전에서 DoF(Depth of Field) 깜빡임 현상. | Fixed (5.7.1) |
| **Issue Tracker URL** | [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/) |

## 4. GitHub 업데이트

Epic Games의 GitHub 저장소(`EpicGames/UnrealEngine`)에 대한 직접적인 커밋 활동은 공개 API를 통해 확인되지 않았습니다. 대신, **UE 5.7 릴리즈 노트**에 명시된 커뮤니티 기여자 목록을 통해 활발한 외부 기여 활동을 확인할 수 있습니다.

*   **주요 커밋 및 Pull Request:**
    *   UE 5.7에는 **70명 이상의 커뮤니티 개발자**가 기여한 개선 사항이 포함되었습니다.
    *   예시 커밋: `GitHub 13887` (가상 텍스처 관련 Fatal Assert 방지), `GitHub 13964` (Vulkan에서 앨리어싱된 텍스처 뷰 수정).
*   **영향받는 시스템:** 렌더링, 코어 엔진, 플랫폼별 이슈 등 광범위한 영역.
*   **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 Epic Staff가 답변한 주요 기술 스레드는 **UE 5.7.1 핫픽스 릴리즈** 관련 공지입니다.

*   **Epic Staff 답변 기술 스레드:**
    *   **제목:** 5.7.1 Hotfix Released
    *   **요약:** TinaWisdom (Epic Staff)이 5.7.1 핫픽스 릴리즈를 공지하며, 약 100개의 수정 사항을 안내하고 피드백을 요청했습니다. 특히 Linux 환경의 SDL3 전환에 대한 주의사항을 명시했습니다.
*   **포럼 URL:** [5.7.1 Hotfix Released](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 6. 신기능 및 실험적 기능

UE 5.7은 2025년 11월 12일에 릴리즈되었으며, 다음은 실무 개발자가 주목해야 할 주요 신기능 및 실험적 기능입니다.

| 기능명 | 상태 | 주요 내용 | 성능 영향도/주의사항 |
| :--- | :--- | :--- | :--- |
| **MegaLights** | Beta | Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 추가. 노이즈 감소 및 전반적인 성능 개선. | Beta 기능으로, 프로덕션 적용 시 성능 테스트 필요. |
| **Substrate** | Production-Ready | 모듈식, 물리 기반 머티리얼 프레임워크. 고성능을 위한 **Adaptive GBuffer**와 광범위한 호환성을 위한 **Blendable GBuffer** 지원. | UE 5.7부터 기본 활성화. 기존 셰이딩 모델을 대체하므로 마이그레이션 시 영향 검토 필요. |
| **Nanite Foliage & Skinning** | Experimental | **Nanite Assemblies**를 통한 인스턴스화된 폴리지 파트 관리, **Nanite Skinning**을 통한 동적 바람 효과, **Nanite Voxels**를 통한 원거리 지오메트리 효율적 렌더링. | 60fps 목표로 설계되었으나, Experimental 기능이므로 프로덕션 사용에 주의. |
| **SMAA (Anti-Aliasing)** | Experimental | 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화. | 최소한의 성능 영향으로 높은 품질의 엣지 스무딩 제공. 품질 설정(`r.SMAA.Quality`)을 통한 성능/품질 트레이드오프 튜닝 가능. |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭을 Chooser에 통합하여, 포즈 검색뿐만 아니라 게임 로직 기반의 에셋 필터링 가능. | 애니메이션 워크플로우에 큰 변화를 줄 수 있는 기능. |

## 7. 플러그인 및 문서 업데이트

*   **공식 플러그인 업데이트:**
    *   **EOS (Epic Online Services):** 5.7.1 핫픽스에 EOS 1.18.1.2 바이너리 업데이트가 포함되었습니다.
    *   **MetaHuman:** MetaHuman 5.7이 5.7 엔진과 함께 릴리즈되었으며, 5.7.1 핫픽스에 MetaHuman 관련 충돌 버그 수정 (`MH-16864`, `MH-16702`)이 포함되었습니다.
*   **문서 주요 변경사항:**
    *   UE 5.7 릴리즈에 맞춰 **Unreal Engine 5.7 Release Notes** 문서가 업데이트되었습니다. 이 문서는 새로운 기능, API 변경 사항, Deprecation 목록 등 방대한 기술 정보를 담고 있습니다.
    *   **Game Animation Sample Project (GASP)**가 UE 5.7에 맞춰 업데이트되었으며, Mover 플러그인, Smart Object 설정, 새로운 슬라이드 기능 등이 추가되었습니다. ([Explore the updates to the Game Animation Sample Project in UE 5.7](https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7))
