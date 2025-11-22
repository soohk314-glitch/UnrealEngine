# 언리얼 엔진 데일리 브리핑 | 2025년 11월 22일

작성 시간: 2025-11-22 03:03 KST

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Nanite Foliage 및 Skinning (Experimental)**: Nanite Assemblies, Nanite Voxels를 활용한 고성능의 동적 폴리지 렌더링 시스템 도입 [1]. 2. **MegaLights (Beta)**: 노이즈 감소 및 성능 개선, Directional Light, Niagara Particle Lights 등 지원 확대 [1]. 3. **Substrate** 재질 시스템: 프로덕션 준비 완료 및 기본 활성화, 모듈식의 물리 기반 셰이딩 모델 제공 [1]. |
| **즉시 확인 필요 사항** | UE 5.7 버전에서 `UbaAgent`가 Windows Server Core 환경에서 `qwave.dll`에 의존하여 작동하지 않는 버그가 보고됨. 해당 환경에서 빌드 가속기를 사용하는 개발자는 확인 필요 [4]. |
| **출처 URL 및 게시일** | Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

**버전 릴리즈:**
*   **Unreal Engine 5.7** (2025년 11월 12일)이 최신 공식 릴리즈입니다.
*   최근 7일간 5.7.1과 같은 마이너 업데이트 또는 핫픽스 릴리즈는 확인되지 않았습니다.

**주요 변경사항 및 Breaking Changes:**
*   **Substrate** 재질 시스템이 프로덕션 준비 완료 상태로 기본 활성화되었습니다. 이는 기존 셰이딩 모델을 대체하는 모듈식 시스템입니다.
*   **PCG (Procedural Content Generation)** 시스템이 프로덕션 준비 완료 상태가 되었습니다.
*   **MetaHuman** 에셋에 대한 Python을 사용한 자동화 및 배치 처리 기능이 추가되었습니다 [2].

**릴리즈 노트 URL:**
*   [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

**새로 보고된 주요 버그 (Latest Bugs):**
*   **UE-207901:** `UbaAgent`가 5.7 버전에서 Windows Server Core 환경에서 `qwave.dll`에 의존하여 작동하지 않음 (Foundation - Cpp Tools - UnrealBuildAccelerator) [4].
*   **UE-207900:** D3D12에서 배치된 렌더 타겟이 제대로 초기화되지 않음 (Rendering Architecture - RHI) [4].
*   **UE-207899:** HDR에서 `ScreenshotCapturedDelegate`가 호출되지 않음 (Platform - Console) [4].

**수정된 버그 (Latest Fixes):**
*   **UE-207898:** `SynchronizeWithExternalDependencies`가 Cook 중 Pose Search DDC 작업으로 인해 소프트 록을 유발할 수 있던 문제 (Anim - Gameplay) [4].
*   **UE-207897:** `CreatePatchLibrary`가 손상되어 있던 문제 (Rendering Architecture - Shaders) [4].
*   **UE-207896:** `NaniteRasterizer.usf`의 오타로 인해 원거리 테셀레이션 감소 모드가 방지되던 문제 (Graphics Features - Nanite) [4].

**Workaround:**
*   현재 보고된 주요 버그에 대한 공식적인 Workaround는 확인되지 않았습니다.

**Issue Tracker URL:**
*   [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine GitHub 저장소의 주요 커밋 및 Pull Request에 대한 구체적인 정보는 별도로 수집되지 않았습니다.
*   **영향받는 시스템:** 정보 없음
*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

공식 포럼의 'Announcements' 섹션에서 Epic Staff의 답변이 포함된 주요 스레드는 다음과 같습니다.
*   **Unreal Engine 5.7 Released:** 2025년 11월 12일에 게시된 5.7 릴리즈 발표 스레드에 Epic Staff의 답변이 활발하게 이어지고 있습니다. (게시 6시간 전 활동 확인) [5].
*   **Unity and Epic Games Together Advance the Open, Interoperable Future for Video Gaming:** Epic과 Unity가 비디오 게임을 위한 개방적이고 상호 운용 가능한 미래를 위해 협력한다는 발표 스레드 (게시 5시간 전 활동 확인) [5].

**포럼 URL:**
*   [https://forums.unrealengine.com/c/general/announcements/49](https://forums.unrealengine.com/c/general/announcements/49)

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.7 기준):**
*   **Control Rig Physics의 월드 충돌:** Control Rig 물리 시뮬레이션에 레벨 지오메트리 및 물리 바디를 충돌체로 사용할 수 있게 되었습니다 [1].
*   **Control Rig Dependency View:** Rig 요소 간의 연결 및 업데이트 방식을 시각화하여 디버깅을 단순화합니다 [1].
*   **FBIK 및 Retargeting 성능 개선:** Full Body IK 및 IK Retargeter의 성능이 약 20% 향상되었습니다 [1].

**Beta/Experimental 기능 및 주의사항:**
| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **Nanite Foliage 및 Skinning** | Experimental | Nanite Assemblies, Nanite Voxels를 활용하여 60fps 예산 내에서 사실적인 동적 폴리지 렌더링을 목표로 합니다. | Nanite Voxels는 원거리 폴리지 지오메트리를 효율적으로 렌더링하여 비용을 절감합니다 [1]. |
| **MegaLights** | Beta | 노이즈 감소 및 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 [1]. | 전반적인 성능 개선이 이루어졌습니다 [1]. |
| **SMAA (Subpixel Morphological Anti-Aliasing)** | Experimental | 모바일 및 데스크톱 렌더러 지원. 최소한의 성능 영향으로 높은 품질의 엣지 스무딩을 제공합니다. | 모바일 게임에 효율적인 기술로, 성능 영향이 최소화됩니다 [1]. |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭을 Chooser에 통합하여 개별 에셋 수준에서 유효성 검사를 제어할 수 있게 되었습니다 [1]. | 정보 없음 |

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트:**
*   **MetaHuman 5.7** 릴리즈가 발표되었습니다. (포럼에서 확인) [5].

**문서 주요 변경사항:**
*   Unreal Engine 5.7에 맞춰 **MegaLights, Nanite Foliage, Substrate** 등 새로운 기능에 대한 문서가 업데이트되었습니다.

---
**참고 자료 (References)**

[1] Unreal Engine 5.7 Release Notes. Epic Developer Community. [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[2] Unreal Engine 5.7 is now available. Unreal Engine News. [https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available)
[3] Unreal Engine 5.7 Released. Epic Developer Community Forums. [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)
[4] Unreal Engine Issues and Bug Tracker. Epic Developer Community. [https://issues.unrealengine.com/](https://issues.unrealengine.com/)
[5] Latest unreal-engine topics in Announcements. Epic Developer Community Forums. [https://forums.unrealengine.com/c/general/announcements/49](https://forums.unrealengine.com/c/general/announcements/49)
