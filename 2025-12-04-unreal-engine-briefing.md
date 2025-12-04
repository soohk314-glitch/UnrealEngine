# 언리얼 엔진 데일리 브리핑 | 2025년 12월 04일

**작성일:** 2025-12-04 KST

## 1. 핵심 요약

**주요 업데이트 상위 3개**
1.  **Substrate** 재질 시스템이 **Production-Ready**로 전환되어 UE 5.7에서 기본 활성화되었습니다. (렌더링)
2.  **Nanite Foliage and Skinning** 기능이 **Experimental** 단계로 도입되어, Nanite를 활용한 고성능의 동적인 식물 렌더링이 가능해졌습니다. (렌더링)
3.  **MegaLights** 전역 조명 시스템이 **Beta** 단계로 진입하며 방향광, Niagara 파티클 라이트, 반투명, 헤어 스트랜드 등을 지원합니다. (렌더링)

**즉시 확인 필요 사항**
*   **UE 5.7.1 Hotfix**가 2025년 12월 02일에 릴리즈되었습니다. 약 100개에 가까운 버그 수정 및 업데이트가 포함되어 있으므로, 5.7 버전을 사용하는 프로젝트는 안정성을 위해 즉시 업데이트를 고려해야 합니다.
*   **Linux 개발 환경** 사용자는 UE 5.7부터 SDL2에서 SDL3로 전환됨에 따라, SDL2 코드에 대한 사용자 정의 변경 사항을 SDL3에 맞게 재작업해야 합니다.

**출처 URL 및 게시일**
*   Unreal Engine 5.7.1 Hotfix Released: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02)
*   Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12)

## 2. 공식 릴리즈 및 패치

**버전 릴리즈**
*   **Unreal Engine 5.7.1 Hotfix**

**주요 변경사항 및 Breaking Changes**
*   **주요 변경사항:** 약 100개의 버그 수정 및 안정성 개선이 포함되었습니다.
*   **Breaking Changes:** UE 5.7부터 Linux 플랫폼의 SDL2가 SDL3로 전환되었습니다. SDL2에 대한 사용자 정의 코드는 SDL3에 맞게 업데이트해야 합니다.

**릴리즈 노트 URL**
*   [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

**새로 보고된 주요 버그 (Latest Bugs)**
*   **UE-XXXXX:** `UInstancedStaticMeshComponent::AddInstances` 사용 시 인스턴스별 이전 트랜스폼(per-instance previous transforms)이 추가되지 않는 문제 (Graphics Features)
*   **UE-XXXXX:** Vulkan SM6 RHI 및 RenderDoc Auto-Attach 활성화 시 언리얼 엔진이 실행되지 않는 문제 (Rendering Architecture - RHI)
*   **UE-XXXXX:** Nanite가 활성화된 `LandscapeSplineMesh`에서 `PlayerCollision` 시각화가 올바르지 않은 문제 (Graphics Features - Nanite)

**수정된 버그 (Latest Fixes)**
*   **UE-XXXXX:** `bake_transform_with_settings` 메서드가 5.6에서는 작동했으나 5.7에서 작동하지 않던 문제 (Anim - Sequencer)
*   **UE-XXXXX:** Datasmith를 통해 임포트된 라이트의 트랜스폼이 올바르지 않던 문제 (Interoperability)
*   **UE-XXXXX:** 로컬 프레젠테이션 내보내기 시 `Rotator` 시각적 헬퍼가 표시되던 문제 (Tools)

**Workaround**
*   5.7.1 Hotfix가 다수의 버그를 수정했으므로, 우선적으로 업데이트를 권장합니다.

**Issue Tracker URL**
*   [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

**주요 커밋 및 Pull Request**
*   최근 7일 이내의 EpicGames/UnrealEngine 저장소에 대한 주요 커밋 및 Pull Request 정보는 검색 결과에서 특정되지 않았습니다. 일반적으로 엔진의 안정성 및 기능 개선을 위한 지속적인 커밋이 이루어지고 있습니다.

**영향받는 시스템**
*   특정 커밋이 확인되지 않아 명시하기 어렵습니다.

**GitHub URL**
*   [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**Epic Staff 답변 기술 스레드**
*   최근 7일 이내에 Epic Staff가 답변한 특정 기술 논의 스레드는 검색 결과에서 확인되지 않았습니다.

**포럼 URL**
*   [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.7 기준)**
*   **Substrate (Production-Ready):** 모듈식의 물리 기반 재질 프레임워크.
*   **World Collisions for Control Rig Physics:** Control Rig 물리 시뮬레이션에 레벨 지오메트리 및 물리 바디를 충돌체로 사용할 수 있게 되었습니다.
*   **Control Rig Dependency View:** Control Rig 요소 간의 관계를 시각화하여 디버깅을 단순화합니다.
*   **FBIK and Retargeting Performance:** Full Body IK 및 IK Retargeter의 성능이 약 20% 향상되었습니다.

**Beta/Experimental 기능 및 주의사항 (UE 5.7 기준)**
*   **Beta:**
    *   **MegaLights:** 방향광, Niagara 파티클 라이트, 반투명, 헤어 스트랜드 지원.
    *   **Niagara Heterogeneous Volumes:** 그림자 캐스팅 개선 (Cascade shadows, Beer Shadow Map 지원).
*   **Experimental:**
    *   **Nanite Foliage and Skinning:** Nanite Assemblies, Skeletal Mesh 기반 동적 바람, Nanite Voxels 등을 포함하여 고성능 식물 렌더링을 제공합니다.
    *   **SMAA (Subpixel Morphological Anti-Aliasing):** 모바일 및 데스크톱 렌더러에 추가. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화 가능.
    *   **Motion Matching Chooser Integration:** 모션 매칭을 Chooser에 통합하여 개별 에셋 수준에서 유효성 검사 및 필터링이 가능해졌습니다.

**성능 영향도**
*   **FBIK 및 Retargeting** 성능 약 20% 향상.
*   **Nanite Foliage**는 기존 방식 대비 현세대 하드웨어에서 60fps 예산 내에서 더 풍부한 월드를 구현할 수 있도록 설계되었습니다.
*   **SMAA**는 최소한의 성능 영향으로 높은 시각적 충실도를 제공합니다.

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트**
*   UE 5.7.1 Hotfix에 **EOS (Epic Online Services)** 1.18.1.2 바이너리 업데이트가 포함되었습니다. (UE-352426)

**문서 주요 변경사항**
*   UE 5.7 릴리즈에 맞춰 공식 문서가 업데이트되었습니다. 특히 Substrate, MegaLights, Nanite Foliage, Control Rig 등 신규/개선된 기능에 대한 상세 문서가 제공됩니다.
*   **Unreal Engine 5.7 Documentation:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)
