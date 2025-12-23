# 언리얼 엔진 데일리 브리핑 | 2025년 12월 23일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **UE 5.7.1 핫픽스** 출시 (12월 2일) [1] <br> 2. **MegaLights (Beta)**: 노이즈 감소 및 성능 개선, Directional Light 등 지원 [2] <br> 3. **Nanite Foliage (Experimental)**: Nanite Assemblies, Skinning, Voxels를 활용한 고성능 폴리지 렌더링 도입 [2] |
| **즉시 확인 필요 사항** | UE 5.7.1에서 `Cooker is asserting in Class.h` 오류가 보고됨 (12월 18일). UE 5.7.1 사용자는 빌드 및 쿠킹 시 주의 필요. [3] |
| **출처 URL 및 게시일** | [1] Unreal Engine 5.7.1 Hotfix Released (2025-12-02) <br> [2] Unreal Engine 5.7 Release Notes (게시일 미상) <br> [3] Unreal Engine Issues and Bug Tracker (2025-12-18) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes:**
    - 5.7.1 핫픽스는 약 100여 개의 수정 사항을 포함하고 있으나, Breaking Changes에 대한 구체적인 공지는 확인되지 않았습니다. [1]
    - **UE 5.7**의 주요 변경 사항으로는 **Substrate** 머티리얼이 정식 프로덕션 레디 상태가 되었으며, **MegaLights** 및 **Niagara Heterogeneous Volumes**가 베타로 전환되었습니다. [2]
- **릴리즈 노트 URL:**
    - UE 5.7.1 Hotfix: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
    - UE 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (최근 7일 이내):**
    - **UE-Graphics Features:** `When r.SSR.Stencil is enabled, there is wrong logic observed.` (12월 19일 보고)
    - **UE-CoreTech:** `Cooker is asserting in Class.h on UE 5.7.1` (12월 18일 보고)
    - **UE-Graphics Features:** `Viewport stuttering during orbit/zoom navigation` (12월 17일 보고)
- **수정된 버그 (최근 7일 이내):**
    - **UE-Rendering Architecture:** `Crash on 5.7 when running with the Vulkan RHI and async compute` (12월 4일 수정 완료)
- **Workaround:**
    - 현재 보고된 주요 버그에 대한 공식적인 Workaround는 이슈 트래커에서 확인되지 않았습니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/issue/search?q=status%3A%22Reported%22+OR+status%3A%22Fixed%22](https://issues.unrealengine.com/issue/search?q=status%3A%22Reported%22+OR+status%3A%22Fixed%22)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - Epic Games의 UnrealEngine GitHub 저장소에 대한 직접적인 최신 커밋 정보는 접근 권한 문제로 인해 수집할 수 없었습니다.
    - 일반적으로 `ue5-main` 브랜치에 활발한 개발이 이루어지고 있습니다.
- **영향받는 시스템:**
    - 정보 수집 불가
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **5.7.1 Hotfix Released** 공지 스레드에서 Epic Staff가 사용자 피드백에 응답하고 있습니다. [1]
    - **Unreal Engine 5.7 Released** 스레드에서 새로운 기능(특히 Skeletal Editor 업데이트)에 대한 논의가 활발합니다. [4]
- **포럼 URL:** [https://forums.unrealengine.com/latest](https://forums.unrealengine.com/latest)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준):**
    - **Character and Animation:** **Motion Matching Chooser Integration (Experimental)**, **Blendshapes and Sculpting** (Skeletal Editor 업데이트), **World Collisions for Control Rig Physics**
    - **Rendering:** **Substrate** (Production Ready), **MegaLights (Beta)**, **Niagara Heterogeneous Volumes (Beta)**
- **Beta/Experimental 기능 및 주의사항:**
    - **Nanite Foliage (Experimental):** Nanite Assemblies, Nanite Skinning, Nanite Voxels를 포함하며, 고성능의 동적인 폴리지 렌더링을 목표로 합니다. 성능 영향도에 대한 공식적인 수치는 없으나, 기존 방식 대비 효율성이 강조되고 있습니다. [2]
    - **SMAA (Experimental):** 모바일 및 데스크톱 렌더러에서 지원되며, `r.AntiAliasingMethod=5` CVar로 활성화 가능합니다. 모바일 게임에서 최소한의 성능 영향으로 시각적 충실도를 높이는 데 유용합니다. [2]
- **성능 영향도:**
    - **FBIK and Retargeting Performance:** Full Body IK 성능이 약 **20%** 향상되었습니다. [2]

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **Procedural Content Generation (PCG) Framework**가 UE 5.7 Preview에서 지속적으로 업데이트되고 있으며, 새로운 기능과 개선 사항이 포함되었습니다. [5]
- **문서 주요 변경사항:**
    - **Unreal Engine 5.7 Documentation**이 최신 릴리즈에 맞춰 업데이트되었습니다. [6]
    - 특히 **Substrate** 머티리얼 시스템의 정식 출시와 **Nanite Foliage**와 같은 실험적 기능에 대한 새로운 문서가 추가되었습니다.
- **문서 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)

***

### 참고 자료 (References)

[1] Unreal Engine 5.7.1 Hotfix Released. *Epic Developer Community Forums*. [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
[2] Unreal Engine 5.7 Release Notes. *Epic Developer Community*. [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[3] Unreal Engine Issues and Bug Tracker. *Epic Developer Community*. [https://issues.unrealengine.com/issue/search?q=status%3A%22Reported%22+OR+status%3A%22Fixed%22](https://issues.unrealengine.com/issue/search?q=status%3A%22Reported%22+OR+status%3A%22Fixed%22)
[4] Unreal Engine 5.7 Released. *Epic Developer Community Forums*. [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)
[5] Unreal Engine 5.7 Preview. *Epic Developer Community Forums*. [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)
[6] Unreal Engine 5.7 Documentation. *Epic Developer Community*. [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)
