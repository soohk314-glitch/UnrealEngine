# 언리얼 엔진 데일리 브리핑 | 2025년 12월 25일

## 1. 핵심 요약

언리얼 엔진의 최신 공식 릴리즈는 **5.7 버전**이며, 가장 최근의 업데이트는 **5.7.1 핫픽스**입니다. 5.7.1 핫픽스는 2025년 12월 2일에 배포되었으며, 약 100여 개의 버그 및 안정성 문제를 해결했습니다.

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **5.7.1 핫픽스** 배포 (약 100개 버그 수정) |
| | 2. **Nanite Foliage** (실험적) 및 **MegaLights** (베타) 등 5.7 신기능 |
| | 3. **Lumen HWRT** 및 **SSR Stencil** 관련 새로운 그래픽 이슈 보고 |
| **즉시 확인 필요 사항** | **UE 5.7.1**에서 쿠커(Cooker)가 `Class.h`에서 어설션(Assert)을 일으키는 문제 등 5.7.1 버전 관련 새로운 버그가 보고되고 있습니다. |
| **출처 URL 및 게시일** | 5.7.1 Hotfix: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |
| | 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

| 구분 | 내용 |
| :--- | :--- |
| **버전 릴리즈** | **Unreal Engine 5.7.1 Hotfix** |
| **주요 변경사항** | 약 100여 개의 버그 및 안정성 수정. Path Tracing, Cinematic MetaHumans, Control Rig, Cloth Asset, Mover 컴포넌트 등 다양한 영역의 크래시 및 문제를 해결했습니다. |
| **Breaking Changes** | 5.7 버전부터 Linux에서 SDL2에서 SDL3로 전환이 시작되었습니다. SDL2 코드를 커스터마이징한 사용자는 UE 5.7 사용 시 해당 변경 사항을 재작업해야 합니다. |
| **릴리즈 노트 URL** | [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) |

## 3. 버그 및 이슈

| 구분 | 내용 |
| :--- | :--- |
| **새로 보고된 주요 버그** | - **UE-348042**: Cooker is asserting in `Class.h` on UE 5.7.1 (2025-12-18 보고) |
| | - **UE-348043**: Reflections of Masked Materials incorrect with Lumen HWRT and Max Refraction Bounces > 0 (2025-12-18 보고) |
| | - **UE-348441**: When `r.SSR.Stencil` is enabled, there is wrong logic observed (2025-12-19 보고) |
| **수정된 버그 (5.7.1 Hotfix)** | - **UE-193929**: Editor becomes unresponsive when moving camera forward if Path Tracing view mode is enabled with mGPU |
| | - **UE-227868**: Cinematic MetaHumans in Level Viewport cause AMD GPU crashes |
| | - **UE-349535**: Crash when `megalight=1`, `Substrate=1` and `GBufferFormat=1` |
| **Workaround** | 5.7.1 핫픽스에 대한 별도의 Workaround는 제공되지 않았습니다. |
| **Issue Tracker URL** | [https://issues.unrealengine.com/issue/search?q=5.7&sort=created](https://issues.unrealengine.com/issue/search?q=5.7&sort=created) |

## 4. GitHub 업데이트

Epic Games의 공식 GitHub 저장소(`EpicGames/UnrealEngine`)에 대한 직접적인 최신 커밋 정보는 수집에 제한이 있었습니다.

**가장 최근에 확인된 GitHub 관련 수정 사항 (5.7.1 Hotfix 포함):**

*   **GitHub 13887**: `FVirtualTextureAllocator::AcquireBlock`에서 치명적인 어설션(fatal assert)을 피하기 위해 보류 중인 삭제(pending-delete) Virtual Texture를 `Loadmap`에서 즉시 해제하도록 수정되었습니다.
*   **영향받는 시스템**: Virtual Texture 시스템, 메모리 관리.

**GitHub URL**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 포럼의 주요 기술 논의는 **Unreal Engine 5.7**의 새로운 기능과 성능 개선에 집중되어 있습니다.

*   **Epic Staff 답변 기술 스레드**:
    *   **5.7.1 Hotfix Released**: 5.7.1 핫픽스에 대한 피드백 및 논의가 진행 중입니다. (TinaWisdom, Dec 2, 2025)
    *   **Unreal Engine 5.7 Released**: 5.7 릴리즈에 대한 광범위한 논의가 진행 중이며, 알려진 이슈 및 해결 계획에 대한 Epic Staff의 답변이 포함되어 있습니다. (MorganC, Nov 12, 2025)
*   **포럼 URL**: [https://forums.unrealengine.com/latest](https://forums.unrealengine.com/latest)

## 6. 신기능 및 실험적 기능

가장 최근의 메이저 릴리즈인 **Unreal Engine 5.7**에 포함된 주요 신기능 및 실험적 기능입니다.

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **MegaLights** | Beta | 노이즈 감소 및 전반적인 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 추가. | 성능 개선에 초점. |
| **Niagara Heterogeneous Volumes** | Beta | 그림자 캐스팅 개선. Cascade shadows, Beer Shadow Map 지원 (그림자 생성 시간 및 쿼리 속도 향상). | 그림자 생성 및 쿼리 성능 향상. |
| **Substrate** | Production-ready | 모듈식, 물리 기반 재질 프레임워크. 고성능 Adaptive GBuffer와 광범위한 호환성을 위한 Blendable GBuffer 지원. | 고급 기능 사용 시 성능 이점. |
| **Nanite Foliage and Skinning** | Experimental | **Nanite Assemblies**, **Nanite Skinning**, **Nanite Voxels**를 결합하여 대규모 환경에서 생동감 있는 애니메이션 폴리지(Foliage)를 60fps 예산 내에서 렌더링 가능. | **대규모 폴리지 렌더링 성능 대폭 개선.** |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭을 Choosers에 통합하여 개별 에셋 수준에서 유효성 검사 및 필터링 가능. | 애니메이션 워크플로우 개선. |

## 7. 플러그인 및 문서 업데이트

*   **공식 플러그인 업데이트**:
    *   **EOS (Epic Online Services)**: 5.7.1 핫픽스에 **EOS 1.18.1.2 바이너리 업데이트**가 포함되었습니다.
    *   **Dynamic Wind Plugin**: 5.7 버전에서 Nanite Foliage와 함께 사용되어 스켈레탈 메시 기반의 동적 바람 효과를 구현합니다.
*   **문서 주요 변경사항**:
    *   **Unreal Engine 5.7 Documentation**이 업데이트되어 MegaLights, Nanite Foliage, Substrate 등 새로운 기능에 대한 상세 문서가 제공되고 있습니다.
    *   **Game Animation Sample Project**가 5.7에 맞춰 업데이트되었으며, Mover 플러그인, Smart Object 설정 등이 포함되었습니다.

---
*본 보고서는 2025년 12월 25일 (KST) 기준으로 작성되었으며, 정보 수집 시점의 최신 데이터를 기반으로 합니다.*
