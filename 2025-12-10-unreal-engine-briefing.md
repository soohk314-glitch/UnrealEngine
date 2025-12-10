# 언리얼 엔진 데일리 브리핑 | 2025년 12월 10일

## 1. 핵심 요약

언리얼 엔진의 최신 공식 릴리즈는 **Unreal Engine 5.7**이며, 2025년 11월 12일에 출시되었습니다. 최근 7일간 새로운 공식 버전 릴리즈나 주요 패치 업데이트는 확인되지 않았습니다. 따라서 본 보고서는 최신 버전인 5.7의 주요 기술 업데이트와 최근 이슈 트래커에 보고된 버그 및 수정 사항을 중심으로 작성되었습니다.

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate** 머티리얼 시스템 정식 버전 (Production-Ready) |
| | 2. **Nanite Foliage and Skinning** (Experimental) 도입으로 대규모 월드 환경 최적화 |
| | 3. **MegaLights** (Beta) 기능 개선 및 지원 범위 확장 |
| **즉시 확인 필요 사항** | UE 5.7에서 Vulkan RHI 및 비동기 컴퓨트(async compute) 사용 시 발생하는 크래시(`Crash on 5.7 when running with the Vulkan RHI and async compute`)에 대한 수정 사항이 보고되었으나, 상세 내용 및 공식 패치 여부는 지속적인 확인이 필요합니다. |
| **출처 URL 및 게시일** | Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

최근 7일간 새로운 공식 릴리즈는 없으며, 가장 최신 버전은 **Unreal Engine 5.7**입니다.

- **버전 릴리즈:** Unreal Engine 5.7
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate 머티리얼 시스템:** 이제 정식 버전(Production-Ready)으로 기본 활성화됩니다. 기존 셰이딩 모델을 대체하는 모듈식 물리 기반 머티리얼 프레임워크입니다.
    - **렌더링 개선:** MegaLights가 베타로 전환되며 노이즈 감소 및 성능이 향상되었고, Directional Light, Niagara Particle Lights, Translucency, Hair Strands를 지원합니다.
    - **애니메이션:** **Motion Matching Chooser Integration**이 실험적 기능으로 도입되어 개별 애셋 수준에서 모션 매칭 유효성 제어가 가능해졌습니다.
- **릴리즈 노트 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

언리얼 엔진 이슈 트래커([https://issues.unrealengine.com/](https://issues.unrealengine.com/))의 최신 보고 및 수정 사항입니다.

- **새로 보고된 주요 버그 (Latest Bugs):**
    - **Lumen HWRT "hit lighting" doesn't respect lighting channels:** Lumen 하드웨어 레이 트레이싱의 "히트 라이팅"이 라이팅 채널을 존중하지 않는 문제. (UE - Graphics Features - Lumen)
    - **Replicated timeline may not call Finished event on client:** 클라이언트에서 복제된 타임라인이 `Finished` 이벤트를 호출하지 않을 수 있는 문제. (UE - Networking)
- **수정된 버그 (Latest Fixes):**
    - **Crash on 5.7 when running with the Vulkan RHI and async compute:** Vulkan RHI 및 비동기 컴퓨트 실행 시 5.7 버전에서 발생하는 크래시. (UE - Rendering Architecture - RHI)
    - **Sequencer causes 3DWidget on BP vectors to snap to Actor when active:** 시퀀서 사용 시 BP 벡터의 3D 위젯이 액터로 스냅되는 문제. (UE - Anim - Sequencer)
    - **Incorrect UVs in imported .fbx files when "Collapse by material" or "Collapse all" is used:** `.fbx` 파일 임포트 시 "Collapse by material" 또는 "Collapse all" 옵션을 사용하면 UV가 잘못되는 문제. (TM - Interoperability)
- **Workaround:**
    - 현재 확인된 공식적인 Workaround는 없습니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine 저장소의 `main` 브랜치에서 실무 개발자에게 즉각적인 영향을 미치는 주요 커밋이나 Pull Request는 확인되지 않았습니다.

- **주요 커밋 및 Pull Request:** 최근 7일간 새로운 업데이트 사항이 없습니다.
- **영향받는 시스템:** 해당 없음
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff가 직접 답변한 중요한 기술 스레드는 확인되지 않았습니다.

- **Epic Staff 답변 기술 스레드:** 최근 7일간 새로운 업데이트 사항이 없습니다.
- **포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

Unreal Engine 5.7 릴리즈에 포함된 주요 신기능 및 실험적 기능입니다.

- **새로 추가된 기능:**
    - **Substrate Materials:** 정식 버전으로 전환되어 머티리얼 제작의 유연성과 성능을 제공합니다.
    - **World Collisions for Control Rig Physics:** Control Rig 물리 시뮬레이션에 레벨 충돌을 도입하여 월드 지오메트리 및 물리 바디를 콜라이더로 사용할 수 있습니다.
- **Beta/Experimental 기능 및 주의사항:**
    - **Nanite Foliage and Skinning (Experimental):** Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통합하여 대규모 환경에서 애니메이션되는 폴리지(Foliage)를 고성능으로 렌더링합니다.
    - **MegaLights (Beta):** 노이즈 감소 및 성능 개선이 이루어졌으며, Directional Light 등을 지원합니다.
    - **Motion Matching Chooser Integration (Experimental):** 모션 매칭에 Chooser를 통합하여 개별 애셋 수준에서 유효성 필터링이 가능해졌습니다.
- **성능 영향도:**
    - **FBIK and Retargeting Performance:** Full Body IK 및 IK Retargeter의 성능이 약 20% 향상되었습니다.
    - **SMAA (Experimental):** 모바일 및 데스크톱 렌더러에서 SMAA(Subpixel Morphological Anti-Aliasing)를 지원하여 최소한의 성능 영향으로 시각적 충실도를 개선합니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **Dynamic Wind plugin:** Nanite Foliage와 함께 사용되어 스켈레탈 메시 형태의 나무에 절차적 바람 효과를 적용할 수 있습니다.
- **문서 주요 변경사항:**
    - Unreal Engine 5.7 Documentation이 업데이트되어 모든 신규 기능에 대한 상세 정보가 제공됩니다.
    - **문서 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)
