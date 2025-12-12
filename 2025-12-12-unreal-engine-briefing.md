# 언리얼 엔진 데일리 브리핑 | 2025년 12월 12일

## 1. 핵심 요약
- 주요 업데이트 상위 3개
    - **Nanite Foliage 및 Skinning (Experimental)**: Nanite Assemblies, Nanite Voxels, Skeletal Mesh 기반 다이나믹 바람 등 3가지 핵심 시스템을 통합하여 대규모 환경에서 고성능의 생동감 있는 식물 렌더링을 가능하게 합니다.
    - **Substrate (Production-Ready)**: 모듈식, 물리 기반 재질 프레임워크인 Substrate가 정식 버전으로 출시되어 기본으로 활성화됩니다. Adaptive GBuffer와 Blendable GBuffer를 지원하여 표현력과 성능을 모두 잡았습니다.
    - **MegaLights (Beta)**: 노이즈 감소 및 전반적인 성능이 향상되었으며, Directional Light, Niagara Particle Lights, Translucency, Hair Strands에 대한 지원이 추가되었습니다.
- 즉시 확인 필요 사항
    - **UE 5.7.1 Hotfix 출시**: 5.7.0 버전 출시 후 발생한 약 100여 개의 버그 및 이슈가 5.7.1 핫픽스에서 수정되었습니다. 특히 에디터 충돌 및 PCG, Cloth Asset 관련 버그가 다수 포함되어 있으므로, 5.7.0 사용자는 즉시 업데이트를 고려해야 합니다.
    - **Linux SDL2 -> SDL3 전환**: UE 5.7부터 Linux에서 SDL2가 SDL3로 전환됩니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경 사항을 재작업해야 합니다.
- 출처 URL 및 게시일 (YYYY-MM-DD)
    - Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12)
    - 5.7.1 Hotfix Released: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02)

## 2. 공식 릴리즈 및 패치
- 버전 릴리즈 (정확한 버전 번호)
    - **Unreal Engine 5.7.1 Hotfix**
- 주요 변경사항 및 Breaking Changes
    - **주요 변경사항**: 5.7.0에서 발생한 에디터 충돌, PCG, Cloth Asset, Iris 네트워킹 관련 약 100여 개의 버그가 수정되었습니다.
    - **Breaking Changes**: Linux 빌드 환경에서 SDL2가 SDL3로 전환되었습니다. 기존 SDL2 기반 커스터마이징 코드는 SDL3에 맞게 수정이 필요합니다.
- 릴리즈 노트 URL
    - 5.7.1 Hotfix Released: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈
- 새로 보고된 주요 버그
    - 최근 7일간 공식 이슈 트래커에서 **새로 보고된 주요 버그**에 대한 구체적인 정보는 확인되지 않았습니다.
    - 포럼에서는 UE 5.7.1 업데이트 후 레벨 로딩 중 충돌(Crash)이 발생한다는 보고가 있었습니다. (Dec 3, 2025)
- 수정된 버그
    - **UE 5.7.1 Hotfix**를 통해 약 100여 개의 버그가 수정되었습니다. 주요 수정 사항은 다음과 같습니다.
        - `UE-351092`: Cloth Asset - 비다양체(non-manifold) 메시를 Inpaint 방식으로 사용할 때 `TransferSkinWeight` 노드에서 발생하는 충돌.
        - `UE-352089`: Full Body IK Solver에 IK Goal을 추가할 때 발생하는 충돌.
        - `UE-352978`: Substrate 사용 시 셰이더가 올바르게 컴파일되지 않는 문제.
        - `UE-353929`: 지형(Terrain)에 구멍이 보이는 문제.
        - `UE-354049`: Heterogeneous Volumes에서 `Composites with Translucency` 활성화 시 플레이 모드에서 발생하는 컴포지팅 아티팩트.
- Workaround
    - **Linux SDL2 -> SDL3 전환 관련**: SDL2 코드를 커스터마이징한 경우, SDL3에 맞게 코드를 재작업해야 합니다.
- Issue Tracker URL
    - Unreal Engine Issues and Bug Tracker: [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트
- 주요 커밋 및 Pull Request
    - **Pull Request #13764 (Wayland 지원 업데이트)**: UE5에서 Wayland 환경을 지원하기 위한 업데이트 작업이 진행 중입니다. 마우스 휠 틸트 지원 추가 및 Wayland 지원을 위한 `LinuxWindow.cpp` 리팩토링이 포함되었습니다. 현재 Swapchain 충돌 문제가 남아있어 작업이 진행 중입니다.
- 영향받는 시스템
    - Linux 플랫폼, 특히 Wayland 디스플레이 서버 환경.
- GitHub URL
    - Pull Request #13764: [https://github.com/EpicGames/UnrealEngine/pull/13764](https://github.com/EpicGames/UnrealEngine/pull/13764)

## 5. 공식 포럼 기술 논의
- Epic Staff 답변 기술 스레드
    - **UE5 Wayland 지원 업데이트 논의**: 커뮤니티 개발자가 Wayland 환경에서 UE5를 작동시키기 위한 Pull Request를 공유하고, 현재 겪고 있는 Swapchain 충돌 문제에 대해 논의하고 있습니다. (24 hours ago)
- 포럼 URL
    - Updating UE5 to work on Wayland...: [https://forums.unrealengine.com/t/updating-ue5-to-work-on-wayland-i-got-it-working-sort-of-mostly-swapchain-issues/2684290](https://forums.unrealengine.com/t/updating-ue5-to-work-on-wayland-i-got-it-working-sort-of-mostly-swapchain-issues/2684290)

## 6. 신기능 및 실험적 기능
- 새로 추가된 기능
    - **Substrate**: 정식 버전(Production-Ready)으로 전환 및 기본 활성화.
    - **Motion Design**: Production Ready 상태로 전환. 패키징 지원 강화, Text3D Rich Text 지원, Transition Logic 안정성 및 UX 개선.
    - **Audio Insights (Beta)**: 라이브 모니터링, 에디터 지원, 스냅샷 및 테일 레코딩, 라이브 라우드니스 미터링 등 기능 추가.
- Beta/Experimental 기능 및 주의사항
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies, Nanite Voxels, Skeletal Mesh 기반 다이나믹 바람. **주의사항**: Experimental 기능이므로 프로덕션 환경 사용 시 주의 필요.
    - **MegaLights (Beta)**: 노이즈 감소 및 성능 향상.
    - **Niagara Heterogeneous Volumes (Beta)**: 그림자 캐스팅 개선 (Cascade shadows, Beer Shadow Map).
    - **SMAA (Experimental)**: 모바일 및 데스크톱 렌더러 지원. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5` CVar로 활성화.
    - **Motion Matching Chooser Integration (Experimental)**: 모션 매칭을 Chooser에 통합하여 에셋 선택에 대한 제어력 강화.
    - **Spatially Aware Retargeting (Experimental)**: IK Retargeter에 Body Interactions 및 Relative IK 오퍼레이터 추가.
- 성능 영향도
    - **FBIK 및 Retargeting 성능 향상**: FBIK 포징 성능 약 20% 향상. IK Rig에서 `stretch limb solver` 및 `Copy Local` FK 회전 모드 사용으로 런타임 리타겟팅 성능 개선.
    - **Chaos Core 성능 향상**: 병렬 시뮬레이션 단계 증가, 대규모 비정형 더미에 대한 Experimental Partial Sleeping 기능 추가.
    - **Chaos Visual Debugger (CVD) 성능 향상**: 2GB 이상의 충돌 지오메트리 데이터 로딩 속도 최대 30% 향상.

## 7. 플러그인 및 문서 업데이트
- 공식 플러그인 업데이트
    - **EOS (Epic Online Services)**: 1.18.1.2 바이너리 업데이트.
    - **OpenXR**: Application SpaceWarp 지원 추가 (Meta의 `XR_FB_space_warp` 및 `XR_EXT_frame_synthesis` 지원).
- 문서 주요 변경사항
    - **UE 5.7 Release Notes**가 공식적으로 게시되었습니다.
    - **Game Animation Sample Project**가 5.7에 맞춰 Mover 플러그인, Smart object 설정 등으로 업데이트되었습니다. (2025-12-03)
    - **Microsoft GDK Plug-ins**가 UE 5.7에 맞춰 업데이트되어 Win64 플랫폼을 사용하여 GDK 게임을 빌드할 수 있게 되었습니다. (2025-12-10)
    - **Meta Unreal Engine 5 Integration** SDK가 버전 83.0으로 업데이트되었습니다. (2025-12-09)
