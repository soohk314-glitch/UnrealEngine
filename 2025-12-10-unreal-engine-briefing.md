# 언리얼 엔진 데일리 브리핑 | 2025년 12월 10일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7.1 핫픽스 출시**: 약 100개의 버그 수정 및 안정성 개선. 2. **Substrate 머티리얼 정식 기능화**: 5.7에서 기본 활성화된 모듈식 물리 기반 셰이딩 모델. 3. **Nanite 폴리지 및 스키닝 (실험적)**: 대규모 오픈 월드 환경을 위한 고성능 폴리지 렌더링 기술 도입. |
| **즉시 확인 필요 사항** | **UE 5.7.1 핫픽스 적용**을 통한 주요 크래시 및 버그 해결. 특히 **Path Tracing** 사용 시의 에디터 응답 없음 문제, **AMD GPU**에서의 시네마틱 메타휴먼 크래시 등 다수의 안정성 문제가 해결되었습니다. |
| **출처 URL 및 게시일** | [5.7.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |

---

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈 (정확한 버전 번호):** **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes:**
    - 약 100개에 가까운 버그 수정 및 안정성 업데이트가 포함되었습니다.
    - **주요 수정 사항:**
        - Path Tracing 뷰 모드 활성화 시 에디터 응답 없음 문제 (UE-193929)
        - AMD GPU에서 시네마틱 메타휴먼 사용 시 크래시 문제 (UE-227868)
        - PCG(Procedural Content Generation)가 PIE(Play In Editor)에서 에디터와 게임 월드를 모두 렌더링하여 렌더링 비용이 두 배가 되는 문제 (UE-349638)
        - MetaHuman 캐릭터가 높은 LOD로 변경될 때 발생하는 크래시 (MH-16702, MH-16864)
    - **Breaking Changes (UE 5.7 기준):**
        - **Linux SDL 전환**: UE 5.7부터 Linux는 SDL2에서 **SDL3**로 전환됩니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경 사항을 재작업해야 합니다.
- **릴리즈 노트 URL:** [5.7.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

---

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (Issue Tracker 기준):**
    - **UE-Networking**: 복제된 타임라인이 클라이언트에서 `Finished` 이벤트를 호출하지 않을 수 있음.
    - **UE-Simulation - Core**: 첫 3개의 정점이 동일 선상에 있을 때 볼록 껍질(Convex hull) 생성이 실패함.
    - **UE-Anim - Rigging - Control Rig**: `GetControlRigBlueprint` 호출을 포함하는 예제 Control Rig Python 스크립트가 `GetControlRigAssetInterface`로 업데이트되어야 함 (UE 5.7에서 함수 Deprecation).
- **수정된 버그 (5.7.1 Hotfix 포함):**
    - **UE-Anim - Sequencer**: 시퀀서가 BP 벡터의 3D 위젯을 액터에 스냅시키는 문제.
    - **TM - Interoperability**: `.fbx` 파일 임포트 시 "Collapse by material" 또는 "Collapse all" 사용 시 UV가 부정확한 문제.
    - **UE-Graphics Features - Path Tracer**: Path Tracer 노멀 맵 이슈.
- **Workaround:** 현재 5.7.1 핫픽스에 대한 공식적인 Workaround는 별도로 보고되지 않았으며, 핫픽스 적용이 권장됩니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)

---

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - 최근 7일간 EpicGames/UnrealEngine 메인 브랜치에 대한 주요 기술 커밋 정보는 검색되지 않았습니다.
    - **Unreal Engine 5.7** 릴리즈에는 커뮤니티 개발자들의 기여가 다수 포함되었습니다. (릴리즈 노트에서 70명 이상의 기여자 언급)
    - **주요 커뮤니티 기여 (5.7 릴리즈 기준):** 버추얼 텍스처 할당자(Virtual Texture Allocator)의 치명적인 어서트(assert)를 방지하기 위한 `GitHub 13887` 수정, Vulkan에서 올바른 뷰를 사용하도록 텍스처 별칭(aliased textures)을 수정하는 `GitHub 13964` 등.
- **영향받는 시스템:** 렌더링, 버추얼 텍스처, 엔진 코어.
- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

---

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **"5.7.1 Hotfix Released"** 스레드가 가장 활발한 공식 논의 스레드입니다. Epic Games 직원이 핫픽스 출시를 알리고 피드백을 요청하고 있습니다.
    - **주요 논의 사항:** 5.7.1 핫픽스 적용 후 발생하는 새로운 문제점이나 해결되지 않은 버그에 대한 사용자 피드백이 주를 이루고 있습니다.
- **포럼 URL:** [5.7.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

---

## 6. 신기능 및 실험적 기능 (UE 5.7 기준)

- **새로 추가된 기능:**
    - **Substrate 머티리얼**이 이제 프로덕션 레디(Production-Ready) 상태이며 기본적으로 활성화됩니다. 모듈식 물리 기반 셰이딩을 제공하여 표현력과 성능을 향상시킵니다.
    - **Blendshapes and Sculpting Tools**가 Skeletal Editor에 통합되어 모프 셰이프, 본, 스킨 웨이트를 원활하게 생성 및 편집할 수 있습니다.
- **Beta/Experimental 기능 및 주의사항:**
    - **MegaLights (Beta)**: 노이즈 감소 및 성능 개선. Directional Light, Niagara Particle Lights 등 지원.
    - **Niagara Heterogeneous Volumes (Beta)**: 디렉셔널 라이트의 캐스케이드 섀도우, Beer Shadow Map 지원 등 섀도우 캐스팅 개선.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통해 대규모 환경에서 고성능 폴리지 렌더링을 가능하게 합니다.
    - **Motion Matching Chooser Integration (Experimental)**: 모션 매칭을 Chooser에 통합하여 게임 로직을 통한 에셋 필터링을 가능하게 합니다.
    - **SMAA (Experimental)**: 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing을 지원하여 최소한의 성능 영향으로 시각적 충실도를 개선합니다.
- **성능 영향도:**
    - **FBIK 및 리타겟팅 성능**이 개선되어 Full Body IK 포징 성능이 약 20% 향상되었습니다.
    - **Nanite Foliage**는 현재 세대 하드웨어에서 60fps 예산 내에서 사실적인 폴리지를 렌더링하도록 설계되었습니다.

---

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **EOS (Epic Online Services)**: 5.7.1 핫픽스에 **EOS: 1.18.1.2 Binary Update**가 포함되었습니다.
    - **Cineware for Unreal Engine**: 2026.1 버전이 2025년 12월 3일에 출시되어 라이트 속성 수정 및 Redshift 라이트/렌더 설정 지원이 추가되었습니다.
- **문서 주요 변경사항:**
    - UE 5.7 릴리즈 노트가 업데이트되었으며, 새로운 기능 및 변경 사항에 대한 상세 문서가 제공되고 있습니다.
    - Control Rig Python 스크립트의 `GetControlRigBlueprint` 함수가 Deprecation되어 `GetControlRigAssetInterface`로 업데이트해야 한다는 내용이 이슈 트래커에 보고되었습니다.

---
*본 보고서는 Unreal Engine 공식 자료를 기반으로 작성되었으며, 모든 정보는 게시 시점의 최신 정보를 반영합니다.*
