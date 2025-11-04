# 언리얼 엔진 데일리 브리핑 | 2025년 11월 04일

## 1. 핵심 요약

| 순위 | 주요 업데이트 | 즉시 확인 필요 사항 | 출처 URL | 게시일 (YYYY-MM-DD) |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **Unreal Engine 5.7 Preview 공개** | PCG 프레임워크 프로덕션 레디 전환, Nanite Foliage 및 Procedural Vegetation Editor (Experimental) 기능 확인 | [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) | 2025-09-23 |
| 2 | **Unreal Engine 5.6.1 핫픽스 릴리즈** | 270개 이상의 버그 수정 및 업데이트. 특히 MetaHuman 관련 다수 이슈 해결 확인 | [https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) | 2025-08-12 |
| 3 | **Substrate 재질 시스템 프로덕션 레디 전환** | UE 5.7 Preview에서 Substrate가 정식 기능으로 전환. 다중 재질 레이어 조합 및 물리적 정확도 향상 확인 | [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) | 2025-09-23 |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** Unreal Engine 5.7 Preview (최신), Unreal Engine 5.6.1 Hotfix
- **주요 변경사항 및 Breaking Changes:**
    - **UE 5.7 Preview:**
        - **PCG (Procedural Content Generation) Framework**가 **Production-Ready**로 전환되었으며, GPU 성능이 크게 향상되었습니다.
        - **Substrate** 재질 시스템이 **Production-Ready**로 전환되어, 다중 재질 레이어 조합이 가능해졌습니다.
        - **MegaLights**가 **Beta**로 전환되었으며, Directional Light, Niagara 파티클 라이트, Translucency, Hair Grooms를 지원합니다.
        - **SDL2에서 SDL3로 전환 예정:** UE 5.7부터 Linux 환경에서 SDL2가 SDL3로 전환될 예정입니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경해야 합니다. (5.6.1 핫픽스 노트에서 언급)
    - **UE 5.6.1 Hotfix:**
        - 270개 이상의 수정 사항이 포함된 핫픽스입니다.
        - MetaHuman Character, PCG, Sequencer, Animation, Rendering 등 광범위한 영역의 크래시 및 버그가 수정되었습니다.
- **릴리즈 노트 URL:**
    - UE 5.7 Preview: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)
    - UE 5.6.1 Hotfix: [https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:**
    - UE 5.7 Preview 릴리즈 이후, UI 상호작용 문제, 특정 블루프린트 프로젝트의 포워드 호환성 문제 등이 포럼에서 논의되고 있습니다.
- **수정된 버그:**
    - **UE 5.6.1 Hotfix**에서 **270개 이상**의 버그가 수정되었습니다. 주요 수정 사항은 다음과 같습니다.
        - MetaHuman 관련 이슈 다수 해결 (예: `MH-15569` - MetaHuman 호환되지 않는 스켈레탈 메시 의상/그룸 사용 가능 문제, `MH-15739` - Techwear UV 문제)
        - 에디터 크래시 문제 다수 해결 (예: `UE-274151` - Mac에서 카메라 액터 복제/삭제 시 크래시, `UE-282213` - PCG self pruning 및 복잡한 콜리전 사용 시 크래시)
        - Sequencer, Animation, Rendering 관련 이슈 해결.
- **Workaround:**
    - UE 5.7 Preview의 알려진 이슈에 대한 공식적인 Workaround는 현재 포럼 공지에서 확인되지 않았습니다.
- **Issue Tracker URL:**
    - Unreal Engine Issue and Bug Tracker: [https://issues.unrealengine.com/](https://issues.unrealengine.com/)
    - UE 5.7 Preview에서 해결 예정인 이슈 목록: [Unresolved issues in 5.7 Preview targeted to be fixed by the 5.7 Release](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (포럼 공지 내 링크)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - **UE 5.7 Preview** 릴리즈는 GitHub를 통해 소스 코드가 제공됩니다. (EpicGames/UnrealEngine 저장소의 `5.7` 브랜치)
    - 5.6.1 핫픽스에는 `UE-210136` (GitHub 11643: Allow Mutable CustomizableObjects to be compiled in -game mode) 등 GitHub 커밋을 기반으로 한 수정 사항이 포함되어 있습니다.
- **영향받는 시스템:**
    - 소스 빌드 사용자 및 커스터마이징된 엔진 사용자
- **GitHub URL:**
    - EpicGames/UnrealEngine: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **Unreal Engine 5.7 Preview** 공지 스레드에서 Epic Staff (TinaWisdom 등)가 사용자 피드백에 답변하고 있습니다. (예: `UE-5.6.1 still super unstable` 스레드 등)
    - **5.6.1 Hotfix Released** 스레드에서 핫픽스 관련 논의가 진행 중입니다.
- **포럼 URL:**
    - UE 5.7 Preview 공지: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)
    - UE 5.6.1 Hotfix 공지: [https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 Preview):**
    - **PCG Framework**가 **Production-Ready**로 전환되며 GPU Compute 경로의 성능 및 멀티플랫폼 지원이 개선되었습니다.
    - **Substrate** 재질 시스템이 **Production-Ready**로 전환되었습니다.
    - **MegaLights**가 **Beta**로 전환되며 Directional Light, Translucency, Hair Grooms 지원이 추가되었습니다.
- **Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview):**
    - **Procedural Vegetation Editor (Experimental):** Fab 에셋을 기반으로 Nanite-ready 폴리지(Foliage)를 에디터 내에서 생성하고 커스터마이징할 수 있는 새로운 플러그인입니다.
    - **Nanite Foliage (Experimental):** Nanite Assemblies, Nanite Skinning, Nanite Voxel 시스템을 통해 고밀도 폴리지를 60fps로 렌더링할 수 있는 새로운 렌더링 경로입니다.
    - **Animation Workflow 개선 (Experimental):** Selection Sets, Animation mode refactor improvements, Constraint UX 업데이트.
    - **Rigging Tools 개선 (Experimental):** Blend shapes and Sculpting, Skeletal Editor 업데이트, Physics World Collisions, Dependency View 추가.
    - **Epic Developer Assistant:** UI는 Preview에 포함되지만, 기능은 5.7.0 정식 릴리즈에서 제공될 예정입니다.
- **성능 영향도:**
    - PCG의 GPU Compute 경로 성능이 UE 5.5 대비 약 2배 향상되었습니다.
    - MegaLights의 성능 튜닝 컨트롤이 추가되어 해상도 스케일 및 업데이트 속도를 관리할 수 있습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman Creator plugin**이 **Linux 및 macOS**를 지원하게 되었습니다.
    - **MetaHuman Creator Python and Blueprint API**가 추가되어 MetaHuman Character 에셋의 편집 및 조립 작업을 스크립트로 처리할 수 있게 되었습니다.
- **문서 주요 변경사항:**
    - Unreal Engine 5.6.1 Hotfix 및 5.7 Preview에 대한 릴리즈 노트가 Epic Developer Community Forums 및 Epic Developer Documentation에 업데이트되었습니다.
    - **UE 5.6 Documentation**은 [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-documentation)에서 확인할 수 있습니다.
