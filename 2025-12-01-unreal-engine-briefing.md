# 언리얼 엔진 데일리 브리핑 | 2025년 12월 01일

> **참고:** 최근 7일간 새로운 공식 릴리즈 또는 핫픽스 업데이트는 확인되지 않았습니다. 본 보고서는 가장 최신 버전인 **Unreal Engine 5.7**의 주요 업데이트 사항과 최근 이슈 트래커 및 GitHub 활동을 기반으로 작성되었습니다.

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate** 머티리얼 프레임워크가 정식 버전(Production-Ready)으로 전환되었습니다. <br> 2. **Nanite Foliage 및 Skinning** 기능이 Experimental로 추가되어 대규모 환경에서 고성능의 동적 폴리지 렌더링을 가능하게 합니다. <br> 3. **MegaLights**가 Beta로 전환되며 노이즈 감소 및 성능 개선, Directional Light 등 지원이 추가되었습니다. |
| **즉시 확인 필요 사항** | - **버그:** Control Rig 생성 시 Skeletal Mesh 이름에 "skel" 접두사가 포함되면 크래시가 발생하는 버그가 보고되었습니다. <br> - **버그:** UE 5.7에서 `bake_transform_with_settings` Python 메서드가 5.6과 달리 작동하지 않는 문제가 보고되었습니다. |
| **출처 URL 및 게시일** | - Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (게시일: 2025-11-12) <br> - Unreal Engine Issues and Bug Tracker: [https://issues.unrealengine.com/](https://issues.unrealengine.com/) |

## 2. 공식 릴리즈 및 패치

최근 7일간 새로운 공식 릴리즈 또는 핫픽스 업데이트는 확인되지 않았습니다. 가장 최신 공식 버전은 **Unreal Engine 5.7**입니다.

*   **버전 릴리즈:** Unreal Engine 5.7
*   **주요 변경사항 및 Breaking Changes:**
    *   **Substrate**가 정식 버전으로 전환됨에 따라, 기존 셰이딩 모델을 사용하는 프로젝트의 마이그레이션 및 호환성 확인이 필요합니다.
    *   **PCG(Procedural Content Generation)** 프레임워크가 프로덕션 준비 상태(Production-Ready)로 전환되어 대규모 월드 제작 워크플로우에 통합되었습니다.
    *   **FBIK 및 Retargeting** 성능이 약 20% 향상되었습니다.
*   **릴리즈 노트 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

Unreal Engine Issue Tracker에서 확인된 주요 버그 및 수정 사항입니다.

*   **새로 보고된 주요 버그:**
    *   **Control Rig Creation Crash:** Skeletal Mesh 이름에 "skel" 접두사가 포함된 경우 Control Rig 생성 시 크래시 발생.
    *   **Sequencer Python Issue:** UE 5.7에서 `bake_transform_with_settings` Python 메서드가 5.6과 달리 작동하지 않음.
    *   **Mutable Issue:** Dataless Mutable 워크플로우에서 Cloth Simulation이 Skeletal Mesh Parameter Node와 함께 작동하지 않는 문제.
*   **수정된 버그 (Latest Fixes 기준):**
    *   **Ortho View Clipping:** 에디터 Top 뷰(Ortho) Lit 모드에서 뷰포트 확대/축소 시 근접 평면(near plane)이 지오메트리를 클리핑하는 문제.
    *   **Enhanced Input Binding:** 자식 위젯이 부모로부터 Enhanced Input 바인딩을 유지하지 못하는 문제.
*   **Workaround:**
    *   **Control Rig Crash:** Skeletal Mesh 이름에서 "skel" 접두사를 제거하거나 사용하지 않도록 변경.
*   **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

연결된 GitHub 저장소 `soohk314-glitch/UnrealEngine`의 `main` 브랜치에서 최근 7일간의 커밋 활동은 확인되지 않았습니다. Epic Games의 공식 `EpicGames/UnrealEngine` 저장소는 내부 개발 프로세스에 따라 업데이트되므로, 최신 개발 동향은 공식 릴리즈 노트를 참고하시기 바랍니다.

*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff가 답변한 새로운 기술 중심 스레드는 확인되지 않았습니다.

*   **포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

Unreal Engine 5.7에 포함된 주요 신기능 및 실험적 기능입니다.

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **Nanite Foliage & Skinning** | Experimental | Nanite Assemblies 및 Nanite Voxels를 사용하여 대규모 폴리지를 고성능으로 렌더링하며, Skeletal Mesh 기반의 동적 바람 효과 지원. | **높음** (60fps 목표로 설계), 기존 방식 대비 효율적 |
| **MegaLights** | Beta | 노이즈 감소 및 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 추가. | **중간** (성능 개선에 초점) |
| **Niagara Heterogeneous Volumes** | Beta | 방향성 광원에 대한 Cascade Shadows 및 Beer Shadow Map 지원을 통한 그림자 캐스팅 개선. | **중간** (그림자 생성 시간 대폭 개선) |
| **SMAA (Subpixel Morphological Anti-Aliasing)** | Experimental | 모바일 및 데스크톱 렌더러에 SMAA 지원 추가. `r.AntiAliasingMethod=5` CVar로 활성화 가능. | **낮음** (최소한의 성능 영향으로 높은 시각적 충실도 제공) |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭에 Chooser 통합을 통해 에셋 선택에 대한 제어 강화 및 디버깅 기능 통합. | **낮음** (주로 워크플로우 개선) |

## 7. 플러그인 및 문서 업데이트

*   **공식 플러그인 업데이트:**
    *   **Substrate** 플러그인이 기본 활성화(Enabled by default) 및 프로덕션 준비 상태로 전환되었습니다.
    *   **Dynamic Wind** 플러그인이 Nanite Foliage의 동적 바람 효과를 위해 추가되었습니다.
*   **문서 주요 변경사항:**
    *   Unreal Engine 5.7의 새로운 기능 및 변경 사항에 대한 문서가 업데이트되었습니다.
    *   [What's New | Unreal Engine 5.7 Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/whats-new) 페이지를 통해 각 버전별 새로운 기능을 확인할 수 있습니다.
