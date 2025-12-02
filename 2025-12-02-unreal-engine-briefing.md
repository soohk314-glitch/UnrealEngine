# 언리얼 엔진 데일리 브리핑 | 2025년 12월 02일

## 1. 핵심 요약

- **주요 업데이트 상위 3개**
    - **Unreal Engine 5.7.1 Hotfix 릴리즈**: 약 100개에 달하는 버그 수정 및 업데이트가 포함되었습니다.
    - **Substrate 머티리얼 Production Ready**: UE 5.7부터 모듈식의 물리 기반 머티리얼 프레임워크인 Substrate가 정식(Production Ready)으로 활성화되었습니다.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies, Nanite Voxels, 동적 바람 시스템을 포함한 차세대 폴리지 렌더링 기능이 실험적 기능으로 추가되었습니다.
- **즉시 확인 필요 사항**
    - **5.7.1 Hotfix 적용**: Path Tracing, Cinematic MetaHumans, Control Rig, PCG 등 다양한 영역의 크래시 및 버그가 수정되었으므로, 해당 기능 사용자는 즉시 핫픽스 적용을 권장합니다.
    - **Linux 개발 환경 주의**: UE 5.7부터 Linux는 SDL2에서 SDL3로 전환되었습니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경해야 합니다.
- **출처 URL 및 게시일 (YYYY-MM-DD)**
    - 5.7.1 Hotfix: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02)
    - 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (최신 주요 릴리즈)

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈**: **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes**
    - 약 100개의 수정사항이 포함된 핫픽스입니다.
    - **Breaking Change (UE 5.7부터)**: Linux 빌드에서 SDL2가 SDL3로 전환되었습니다. SDL2 코드를 직접 수정한 경우 호환성 확인이 필요합니다.
- **릴리즈 노트 URL**: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그**:
    - 최근 7일간 공식적으로 새로 보고된 주요 버그는 5.7.1 핫픽스에 포함되어 수정되었거나, 아직 공식 이슈 트래커에 등록되지 않았습니다.
- **수정된 버그 (5.7.1 Hotfix 주요 수정 목록)**
    - `UE-193929`: Path Tracing 뷰 모드 활성화 및 mGPU 사용 시 카메라 이동 중 에디터 응답 없음 현상.
    - `UE-227868`: 레벨 뷰포트의 시네마틱 MetaHumans로 인한 AMD GPU 크래시.
    - `UE-296303`: `PythonScriptPlugin` 초기화 중 Assert 크래시.
    - `UE-349638`: PCG 생성 시 PIE에서 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배가 되는 문제.
    - `UE-352426`: EOS (Epic Online Services) 바이너리가 **1.18.1.2** 버전으로 업데이트되었습니다.
- **Workaround**:
    - 5.7.1 핫픽스에 포함된 수정사항 외에 공식적으로 알려진 Workaround는 없습니다.
- **Issue Tracker URL**: [https://issues.unrealengine.com/issue/search?q=&component=ue_anim_rigging_control_rig](https://issues.unrealengine.com/issue/search?q=&component=ue_anim_rigging_control_rig) (애니메이션/컨트롤 릭 컴포넌트 검색 결과)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**:
    - 5.7.1 핫픽스에 포함된 약 100개의 수정사항이 GitHub의 EpicGames/UnrealEngine 저장소에 커밋되었습니다.
    - **GitHub 13964**: Vulkan에서 올바른 뷰를 사용하도록 앨리어싱된 텍스처를 수정하는 커밋이 포함되었습니다. (`UE-350545` 관련)
- **영향받는 시스템**: 렌더링, 애니메이션, Control Rig, PCG, 플랫폼(Linux, iOS, Android), EOS 등 광범위한 영역.
- **GitHub URL**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**:
    - 가장 최근의 공식적인 Epic Staff의 커뮤니케이션은 **5.7.1 Hotfix Released** 공지 스레드입니다.
- **포럼 URL**: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 6. 신기능 및 실험적 기능 (UE 5.7 기준)

- **새로 추가된 기능**:
    - **Substrate 머티리얼**: 이제 기본 활성화(Production Ready)되어 모듈식 셰이딩 모델을 제공합니다.
    - **Blendshapes and Sculpting Tools**: 스켈레탈 에디터에서 모프 셰이프, 본, 스킨 웨이트를 생성 및 편집하는 기능이 추가되었습니다.
    - **World Collisions for Control Rig Physics**: Control Rig 물리 시뮬레이션에 레벨 충돌을 사용할 수 있습니다.
- **Beta/Experimental 기능 및 주의사항**:
    - **MegaLights (Beta)**: 노이즈 감소 및 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원.
    - **Niagara Heterogeneous Volumes (Beta)**: 디렉셔널 라이트의 Cascade Shadows 및 Beer Shadow Map 지원.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies, Nanite Voxels, 동적 바람 시스템을 통한 차세대 폴리지 렌더링.
    - **SMAA (Experimental)**: 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원. CVar `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화.
    - **Motion Matching Chooser Integration (Experimental)**: 모션 매칭을 Chooser에 통합하여 포즈 검색 및 필터링을 게임 로직을 통해 제어 가능.
- **성능 영향도**:
    - **FBIK and Retargeting Performance**: Full Body IK 및 IK Retargeter의 성능이 약 20% 향상되었습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**:
    - **EOS (Epic Online Services)** 바이너리가 **1.18.1.2**로 업데이트되었습니다.
    - **Dynamic Wind plugin**: Nanite Foliage와 함께 사용되어 스켈레탈 메시 기반의 절차적 바람 효과를 제공합니다.
- **문서 주요 변경사항**:
    - UE 5.7 릴리즈 노트에 Substrate, Nanite Foliage, MegaLights 등 주요 기능에 대한 상세 문서가 업데이트되었습니다.
    - **UE 5.7 Release Notes URL**: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
