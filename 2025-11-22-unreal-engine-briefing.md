# 언리얼 엔진 데일리 브리핑 | 2025년 11월 22일

## 1. 핵심 요약

| 항목 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7 공식 릴리즈**: 렌더링, 캐릭터/애니메이션, 월드 빌딩 등 전반적인 개선. <br> 2. **Substrate 머티리얼 시스템** 프로덕션 준비 완료 및 기본 활성화. <br> 3. **MegaLights (Beta)** 및 **Niagara Heterogeneous Volumes (Beta)** 도입. |
| **즉시 확인 필요 사항** | **UE 5.7**에서 **UbaAgent**가 Windows Server Core 환경에서 `qwave.dll`에 의존하여 작동하지 않는 버그가 보고됨. 서버 환경에서 빌드 가속기를 사용하는 경우 확인 필요. |
| **출처 URL 및 게시일** | Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈**: Unreal Engine 5.7
- **주요 변경사항 및 Breaking Changes**:
    - **렌더링**:
        - **Substrate** 머티리얼 시스템이 프로덕션 준비 완료(Production-Ready) 상태로 기본 활성화되었습니다.
        - **MegaLights**가 Beta로 전환되었으며, 노이즈 감소 및 성능이 개선되었습니다. (Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원)
        - **Niagara Heterogeneous Volumes**가 Beta로 전환되었으며, 그림자 캐스팅 개선(Cascade shadows, Beer Shadow Map 지원)에 중점을 둡니다.
        - **Nanite Foliage and Skinning** 및 **SMAA**가 Experimental 기능으로 추가되었습니다.
    - **캐릭터 및 애니메이션**:
        - **Motion Matching Chooser Integration**이 Experimental 기능으로 도입되어, Chooser를 통해 모션 매칭에 사용할 에셋을 제어할 수 있게 되었습니다.
        - **Control Rig Physics**에 월드 충돌(World Collisions) 지원이 추가되었습니다.
        - **FBIK 및 Retargeting 성능**이 약 20% 향상되었습니다.
- **릴리즈 노트 URL**: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (Latest Bugs)**:
    - **Placed render targets are not initialized properly in D3D12** (UE - Rendering Architecture - RHI)
    - **ScreenshotCapturedDelegate is never called in HDR** (UE - Platform - Console)
    - **UbaAgent in 5.7 depends on qwave.dll, which is not available on Server Core** (UE - Foundation - Cpp Tools - UnrealBuildAccelerator)
- **수정된 버그 (Latest Fixes)**:
    - **SynchronizeWithExternalDependencies can cause soft lock with Pose Search DDC tasks during cook** (UE - Anim - Gameplay)
    - **CreatePatchLibrary is broken** (UE - Rendering Architecture - Shaders)
    - **Typo in NaniteRasterizer.usf preventing low tessellation mode at distance** (UE - Graphics Features - Nanite)
- **Workaround**:
    - **UbaAgent** 이슈의 경우, 현재 공식적인 Workaround는 확인되지 않았습니다.
- **Issue Tracker URL**: [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine GitHub 저장소의 주요 커밋 및 Pull Request에 대한 직접적인 기술 정보는 수집되지 않았습니다.

- **주요 커밋 및 Pull Request**: 최근 7일간 새로운 업데이트 사항이 없습니다.
- **영향받는 시스템**: 해당 없음
- **GitHub URL**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff의 답변이 포함된 주요 기술 스레드는 수집되지 않았습니다.

- **Epic Staff 답변 기술 스레드**: 최근 7일간 새로운 업데이트 사항이 없습니다.
- **포럼 URL**: [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능**:
    - **Substrate** 머티리얼 시스템이 프로덕션 준비 완료 상태로 전환되었습니다.
- **Beta/Experimental 기능 및 주의사항**:
    - **MegaLights (Beta)**: 노이즈 감소 및 성능 개선.
    - **Niagara Heterogeneous Volumes (Beta)**: 그림자 캐스팅 개선.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통한 고성능 애니메이션 폴리지 렌더링.
    - **SMAA (Experimental)**: 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원.
    - **Motion Matching Chooser Integration (Experimental)**: Chooser를 통한 모션 매칭 에셋 제어.
- **성능 영향도**:
    - **FBIK 및 Retargeting 성능**이 약 20% 향상되었습니다.
    - **SMAA**는 최소한의 성능 영향으로 시각적 충실도를 개선합니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**:
    - **Dynamic Wind plugin**이 Nanite Foliage와 함께 사용되어 Skeletal Mesh 기반 나무에 절차적 바람 효과를 적용할 수 있게 되었습니다.
- **문서 주요 변경사항**:
    - Unreal Engine 5.7에 맞춰 전체 문서가 업데이트되었습니다.
    - **Substrate** 관련 문서가 프로덕션 사용을 위해 갱신되었습니다.
    - **Nanite Foliage** 및 **Motion Matching Chooser** 등 새로운 Experimental 기능에 대한 문서가 추가되었습니다.
