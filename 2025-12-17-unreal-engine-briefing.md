# 언리얼 엔진 데일리 브리핑 | 2025년 12월 17일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 (상위 3개)** | 1. **UE 5.7.1 핫픽스** (14일 전) 출시: 약 100여 개의 버그 및 크래시 수정. 2. **MetaHuman 5.7 업데이트** (1일 전): 플랫폼 지원 확장 및 프로시저럴 그루밍 기능 강화. 3. **AMD FSR Redstone SDK 플러그인 업데이트** (6일 전): 최신 FSR 기능 통합 지원. |
| **즉시 확인 필요 사항** | **UE 5.7 이상 Linux 사용자:** SDL2에서 SDL3로 전환됨에 따라, SDL2 코드를 커스터마이징한 경우 SDL3에 맞게 재작업이 필요합니다. |
| **출처 URL 및 게시일** | [UE 5.7.1 Hotfix Released](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |

## 2. 공식 릴리즈 및 패치

**최근 7일간 새로운 공식 릴리즈 또는 패치 사항이 없습니다.**

가장 최신 버전은 **Unreal Engine 5.7.1 Hotfix**이며, 2025년 12월 2일에 배포되었습니다.

- **버전 릴리즈:** Unreal Engine 5.7.1 Hotfix
- **주요 변경사항 및 Breaking Changes:**
    - 약 100여 개의 수정 사항이 포함된 안정화 핫픽스입니다.
    - **Breaking Change:** UE 5.7부터 Linux 플랫폼은 SDL2에서 SDL3로 전환되었습니다. SDL2에 대한 커스터마이징이 있는 경우 반드시 SDL3에 맞게 업데이트해야 합니다.
- **릴리즈 노트 URL:** [5.7.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

**최근 7일간 새로 보고된 주요 버그는 확인되지 않았습니다.**

**수정된 버그 (UE 5.7.1 Hotfix 주요 수정 사항):**

- **UE-193929:** mGPU 환경에서 Path Tracing 뷰 모드를 활성화하고 카메라를 이동할 때 에디터가 응답하지 않던 문제.
- **UE-227868:** 레벨 뷰포트에서 시네마틱 MetaHumans 사용 시 AMD GPU 크래시를 유발하던 문제.
- **UE-349638:** PCG(Procedural Content Generation)가 PIE(Play In Editor)에서 생성될 때 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배가 되던 문제.
- **UE-350545:** GitHub 13964: Vulkan에서 별칭 텍스처(aliased textures)가 올바른 뷰를 사용하도록 수정.
- **UE-352426:** EOS(Epic Online Services) SDK가 1.18.1.2 바이너리로 업데이트되었습니다.

- **Workaround:** 해당 핫픽스에 대한 공식적인 Workaround는 제공되지 않았습니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

**최근 7일간 EpicGames/UnrealEngine 메인 저장소에서 실무 개발자에게 직접적인 영향을 미치는 주요 커밋 또는 Pull Request는 확인되지 않았습니다.**

- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**최근 7일간 Epic Staff가 답변한 새로운 주요 기술 스레드는 확인되지 않았습니다.**

- **포럼 URL:** [Epic Developer Community Forums](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

**UE 5.7 버전의 주요 신기능 및 실험적 기능 (가장 최신 주요 릴리즈):**

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **MegaLights** | Beta | Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 추가. 노이즈 감소 및 전반적인 성능 개선. | 개선됨 |
| **Niagara Heterogeneous Volumes** | Beta | 방향성 광원에 대한 Cascade Shadows 및 Beer Shadow Map 지원 추가. 그림자 생성 시간 및 쿼리 성능 향상. | 개선됨 |
| **Substrate Materials** | Production-ready | 모듈식, 물리 기반 재질 프레임워크. UE 5.7부터 기본 활성화. Adaptive GBuffer 및 Blendable GBuffer 지원. | 플랫폼 및 설정에 따라 다름 |
| **Nanite Foliage and Skinning** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통한 고성능 나뭇잎 렌더링. 동적 바람 효과 지원. | 60fps 예산 내에서 고품질 구현 가능 |
| **SMAA (Subpixel Morphological Anti-Aliasing)** | Experimental | 모바일 및 데스크톱 렌더러 지원. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화. | 최소한의 성능 영향으로 시각적 충실도 향상 |
| **Motion Matching Chooser Integration** | Experimental | 모션 매칭을 Chooser에 통합하여 에셋 선택에 대한 제어력 및 디버깅 용이성 향상. | - |

- **출처 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 7. 플러그인 및 문서 업데이트

**최근 7일간의 주요 플러그인 및 문서 업데이트:**

- **MetaHuman 5.7 업데이트:**
    - 플랫폼 지원 확장 및 쉬운 프로시저럴 그루밍 기능 추가.
    - **출처:** [MetaHuman 5.7 is now available](https://www.metahuman.com/releases/metahuman-5-7-is-now-available) (2025-12-16)
- **AMD FSR Redstone SDK 플러그인:**
    - 최신 FSR 기능을 통합하기 위한 플러그인 업데이트.
    - **출처:** [AMD FSR Redstone SDK Available For Download, Unreal Engine Plugin Download](https://wccftech.com/amd-fsr-redstone-sdk-unreal-engine-plugin-download/) (2025-12-11)
- **문서 주요 변경사항:**
    - UE 5.7 릴리즈에 맞춰 **Game Animation Sample Project**가 업데이트되었으며, Mover 플러그인, Smart Object 설정 등이 포함되었습니다.
    - **출처:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
