# 언리얼 엔진 데일리 브리핑 | 2025년 12월 15일

## 1. 핵심 요약

| 구분 | 내용 | 출처 URL 및 게시일 |
| :--- | :--- | :--- |
| **주요 업데이트 1** | **Substrate Materials 정식 버전 (Production-Ready)**: 모듈식 물리 기반 셰이딩 프레임워크가 UE 5.7에서 정식으로 활성화되었습니다. | [UE 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |
| **주요 업데이트 2** | **MegaLights 베타** 진입: 노이즈 감소 및 성능 개선과 함께 Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원이 추가되었습니다. | [UE 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |
| **주요 업데이트 3** | **UE 5.7.1 핫픽스** 릴리즈: 약 100개에 가까운 버그 및 이슈가 수정되었습니다. | [5.7.1 Hotfix Released](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |
| **즉시 확인 필요 사항** | **Linux SDL2 -> SDL3 전환 주의:** UE 5.7부터 Linux 빌드에서 SDL2에서 SDL3로의 전환이 시작됩니다. SDL2 코드를 커스터마이징한 경우 변경 사항을 확인해야 합니다. | [5.7.1 Hotfix Released](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** Unreal Engine 5.7 (최신 메이저 버전)
- **최신 패치:** **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항:**
    - **UE 5.7.1**은 UE 5.7 릴리즈 이후 발견된 약 100개의 버그를 수정하는 핫픽스입니다.
    - **UE 5.7**의 주요 변경사항으로는 **Substrate Materials**의 정식 버전 전환, **MegaLights**의 베타 진입, **Nanite Foliage and Skinning** (Experimental) 도입, **Motion Matching Chooser Integration** (Experimental) 등이 있습니다.
- **Breaking Changes:** UE 5.7 릴리즈 노트에서 명시적인 'Breaking Changes' 섹션은 없으나, **Substrate Materials**가 기본 셰이딩 모델로 활성화되었으므로, 기존 프로젝트의 머티리얼 시스템에 영향을 줄 수 있습니다.
- **릴리즈 노트 URL:**
    - UE 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
    - UE 5.7.1 Hotfix: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:** 최근 7일간 새로운 메이저 버전 릴리즈는 없었으며, 5.7.1 핫픽스 이후의 주요 버그는 아직 공식적으로 집계되지 않았습니다.
- **수정된 버그 (UE 5.7.1 Hotfix 기준):**
    - **UE-193929:** Path Tracing + mGPU 사용 시 카메라 이동 중 에디터 응답 없음.
    - **UE-227868:** 레벨 뷰포트에서 시네마틱 MetaHumans 사용 시 AMD GPU 충돌.
    - **UE-349535:** MegaLight, Substrate, GBufferFormat 특정 설정 조합에서 충돌.
    - **UE-349638:** PCG PIE 생성 시 렌더링 비용이 두 배가 되는 문제.
    - **UE-350545 (GitHub 13964):** Vulkan에서 Split Barriers 사용 시 VkEvent 핸들 누수.
- **Workaround:** 5.7.1 핫픽스에 포함된 수정 사항이므로, **5.7.1 버전으로 업데이트**하는 것이 가장 확실한 Workaround입니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (최신 버그 및 이슈 상태 확인)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - EpicGames/UnrealEngine 저장소의 메인 브랜치에는 7일 이내의 주요 기술 커밋은 확인되지 않았습니다. (대규모 기능은 릴리즈 브랜치에 통합됨)
    - **영향받는 시스템:** UE 5.7 릴리즈 노트에는 커뮤니티 기여자들의 이름이 다수 언급되어, 다양한 시스템(렌더링, 애니메이션, 툴 등)에 대한 외부 기여가 활발함을 보여줍니다.
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:** 최근 7일간 Epic Staff가 답변한 새로운 주요 기술 스레드는 확인되지 않았습니다.
- **최신 주요 논의:** **UE 5.7.1 Hotfix Released** 스레드에서 핫픽스에 대한 피드백 및 논의가 진행 중입니다.
- **포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준):**
    - **Substrate Materials:** 정식 버전으로 전환되어 기본 셰이딩 모델로 사용됩니다.
    - **Control Rig Physics World Collisions:** Control Rig Physics 시뮬레이션에 레벨 지오메트리 및 물리 바디와의 충돌을 사용할 수 있게 되었습니다.
- **Beta/Experimental 기능 및 주의사항:**
    - **MegaLights (Beta):** 성능 및 기능 개선이 이루어졌으며, 프로덕션 환경에서 테스트가 권장됩니다.
    - **Nanite Foliage and Skinning (Experimental):** 대규모 환경에서 고성능 Foliage 렌더링을 위한 새로운 시스템입니다. **Nanite Assemblies** 및 **Nanite Voxels**를 포함합니다.
    - **SMAA (Experimental):** 모바일 및 데스크톱 렌더러에서 지원되는 Subpixel Morphological Anti-Aliasing 기능입니다.
    - **Motion Matching Chooser Integration (Experimental):** 모션 매칭과 Chooser 시스템의 통합을 통해 에셋 선택의 유연성을 높였습니다.
- **성능 영향도:** **Substrate**는 모던 하드웨어에서 **Adaptive GBuffer**를 통해 고급 기능을 제공하며, **Nanite Foliage**는 60fps 예산 내에서 생동감 있는 Foliage를 제공하도록 설계되어 전반적인 **성능 최적화**에 중점을 두고 있습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **Game Animation Sample Project**가 UE 5.7에 맞춰 업데이트되었습니다. **Mover 플러그인** 및 **Smart Object** 설정 등이 포함되었습니다.
- **문서 주요 변경사항:**
    - **UE 5.7 Release Notes** 문서가 최신 기술 업데이트를 상세히 다루고 있습니다.
    - **Linux 빌드 환경**에서 **SDL2에서 SDL3로의 전환**에 대한 주의사항이 문서에 추가되었습니다.

---
**작성일시:** 2025년 12월 15일 18:05 (KST)
**작성자:** Manus AI
