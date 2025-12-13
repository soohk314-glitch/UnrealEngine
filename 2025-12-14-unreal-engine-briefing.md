# 언리얼 엔진 데일리 브리핑 | 2025년 12월 13일

## 1. 핵심 요약

최근 7일간 공식적인 엔진 릴리즈나 핫픽스 업데이트는 없었으나, 가장 최신 버전인 **UE 5.7.1 핫픽스**의 주요 내용을 바탕으로 실무 개발자가 즉시 확인해야 할 사항을 요약했습니다.

- **주요 업데이트 상위 3개 (UE 5.7 기준):**
    1.  **Substrate** 재질 시스템이 **Production-Ready**로 전환되어 기본 활성화되었습니다. 기존 재질 시스템과의 호환성 및 마이그레이션 전략을 검토해야 합니다.
    2.  **Nanite Foliage and Skinning (Experimental)** 기능이 도입되어 Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통한 고성능 폴리지 렌더링이 가능해졌습니다. 대규모 월드 환경 작업 시 성능 개선에 큰 영향을 미칠 수 있습니다.
    3.  **MegaLights (Beta)**가 Directional Light, Translucency, Hair Strands 등을 지원하며 기능이 확장되고 성능이 개선되었습니다.

- **즉시 확인 필요 사항:**
    *   **UE 5.7.1 핫픽스**에서 PCG(Procedural Content Generation)의 PIE(Play In Editor) 렌더링 비용이 두 배로 증가하는 문제(UE-349638)를 포함하여 약 100개의 버그가 수정되었습니다. 5.7 사용자라면 즉시 업데이트를 고려해야 합니다.
    *   UE 5.7부터 Linux 플랫폼은 SDL2에서 SDL3로 전환됩니다. Linux 빌드 환경을 커스터마이징한 경우 SDL3에 맞게 코드를 수정해야 합니다.

- **출처 URL 및 게시일 (가장 최신 공식 업데이트 기준):**
    *   **UE 5.7.1 Hotfix:** [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02)
    *   **UE 5.7 Release Notes:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12)

## 2. 공식 릴리즈 및 패치

최근 7일간 새로운 공식 릴리즈는 없었습니다. 가장 최신 공식 업데이트는 **Unreal Engine 5.7.1 Hotfix**입니다.

- **버전 릴리즈:** **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes:**
    *   UE 5.7.1은 약 100개의 버그를 수정하는 핫픽스입니다. 기능 추가보다는 안정성 개선에 중점을 둡니다.
    *   **Breaking Change (UE 5.7 기준):** Linux 플랫폼에서 SDL2에서 SDL3로의 전환이 예정되어 있습니다. SDL2 기반 커스터마이징 코드는 SDL3에 맞게 수정이 필요합니다.
- **릴리즈 노트 URL:** [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

최근 7일간 새로 보고되거나 수정된 주요 버그에 대한 공식적인 발표는 없었습니다. 가장 최신 패치인 **UE 5.7.1 Hotfix**에서 수정된 주요 버그 목록은 다음과 같습니다.

| Issue ID | 요약 | 영향받는 시스템 |
| :--- | :--- | :--- |
| UE-349638 | PCG에서 PIE 생성 시 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배가 되는 문제 | PCG, 렌더링 |
| UE-349535 | `megalight=1`, `Substrate=1`, `GBufferFormat=1` 설정 시 충돌 | MegaLights, Substrate |
| UE-193929 | Path Tracing 뷰 모드 활성화 및 mGPU 사용 시 에디터 응답 없음 현상 | 렌더링, Path Tracing |
| UE-227868 | Cinematic MetaHumans가 레벨 뷰포트에서 AMD GPU 충돌을 유발하는 현상 | MetaHuman, 렌더링 |
| UE-352089 | Full Body IK Solver에 IK Goal 추가 시 충돌 | 애니메이션, Control Rig |
| MH-16702 | MetaHuman 캐릭터가 고화질 LOD로 변경될 때 여러 플랫폼에서 충돌 | MetaHuman |

- **Workaround:** 해당 버그들은 5.7.1 핫픽스에서 수정되었으므로, **5.7.1로 업데이트**하는 것이 권장되는 해결책입니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 및 Pull Request에 대한 공식적인 요약 정보는 발표되지 않았습니다.

- **주요 커밋 및 Pull Request:** 최근 7일간 새로운 업데이트 사항이 없습니다.
- **영향받는 시스템:** 해당 없음
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) (접근 권한 필요)

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff가 답변한 주목할 만한 새로운 기술 스레드는 확인되지 않았습니다.

- **Epic Staff 답변 기술 스레드:** 최근 7일간 새로운 업데이트 사항이 없습니다.
- **포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

가장 최신 메이저 릴리즈인 **UE 5.7**에 포함된 주요 신기능 및 실험적 기능은 다음과 같습니다.

| 기능 | 상태 | 주요 내용 | 성능 영향도 및 주의사항 |
| :--- | :--- | :--- | :--- |
| **Substrate** | Production-Ready | 모듈식, 물리 기반 재질 프레임워크. UE 5.7부터 기본 활성화. Adaptive GBuffer 및 Blendable GBuffer 지원. | 기존 셰이딩 모델을 대체하며, 장기적으로 유연성과 성능에 기여. |
| **MegaLights** | Beta | Directional Light, Translucency, Hair Strands 지원 추가. 노이즈 감소 및 전반적인 성능 개선. | 기능 확장에 따른 렌더링 복잡도 증가 가능성. |
| **Nanite Foliage and Skinning** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxels를 활용한 고성능 폴리지 렌더링. Skeletal Mesh 기반 다이나믹 바람 지원. | **60fps 예산 내에서** 생동감 있는 대규모 폴리지 렌더링 가능. Experimental 기능이므로 프로덕션 사용 시 주의 필요. |
| **SMAA** | Experimental | 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원. | 최소한의 성능 영향으로 시각적 충실도 개선. 모바일 게임에 효율적. |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭을 Choosers에 통합하여 개별 에셋 레벨에서 유효성 제어. | 애니메이션 워크플로우의 유연성 증가. Experimental 기능. |

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    *   **Game Animation Sample Project**가 UE 5.7에 맞춰 업데이트되었습니다. 새로운 **Mover 플러그인**, Smart Object 설정, 새로운 로코모션 스타일 등이 포함되었습니다.
- **문서 주요 변경사항:**
    *   최근 7일간 새로운 업데이트 사항이 없습니다.
    *   가장 최신 릴리즈인 UE 5.7의 공식 문서가 업데이트되었습니다.
    *   **UE 5.7 Release Notes URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
