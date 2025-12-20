# 언리얼 엔진 데일리 브리핑 | 2025년 12월 20일

실무 개발자를 위한 언리얼 엔진의 최신 기술 업데이트 및 이슈 보고서입니다. (KST 기준)

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate Materials** 정식 출시 (UE 5.7) <br> 2. **PCG (Procedural Content Generation)** 프레임워크 정식 출시 (UE 5.7) <br> 3. **Nanite Foliage** (실험적) 시스템 도입 (UE 5.7) |
| **즉시 확인 필요 사항** | **UE 5.7.1 Hotfix** 적용 여부 확인 (약 100개 버그 수정). Linux 사용자는 **SDL2에서 SDL3로의 전환** (Breaking Change)에 따른 코드 수정 필요성 [1]. |
| **최신 이슈** | `r.SSR.Stencil` 활성화 시 잘못된 로직 관찰 (Dec 19, 2025), UE 5.7.1에서 `Cooker`가 `Class.h`에서 어서트 발생 (Dec 18, 2025) [3]. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (게시일: 2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes:**
    - 5.7 버전에서 발견된 약 100개에 가까운 버그 및 업데이트를 수정했습니다. [2]
    - **Breaking Change:** UE 5.7부터 Linux 플랫폼에서 **SDL2가 SDL3로 전환**됩니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경해야 합니다. [1]
- **릴리즈 노트 URL:** [5.7.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (최근 7일 이내):**
    - **UE-350123**: `r.SSR.Stencil` 활성화 시 높은 거칠기 영역이 폐기되지 않고 Unlit 머티리얼이 잘못 처리되는 문제 (Dec 19, 2025) [3]
    - **UE-350021**: UE 5.7.1에서 `Cooker`가 `Class.h`에서 어서트(Assert)를 발생시키는 문제 (Dec 18, 2025) [3]
- **수정된 버그 (최근 7일 이내):**
    - **UE-347106**: `FVirtualTextureAllocator::AcquireBlock`에서 보류 중인 가상 텍스처 삭제로 인한 프리징 문제 (5.7.1 Hotfix) [2]
    - **UE-348042**: Vulkan RHI 및 비동기 컴퓨팅 사용 시 5.7에서 발생하는 크래시 (Dec 4, 2025, 5.7.1 Hotfix에 포함) [3]
- **Workaround:**
    - 새로 보고된 주요 버그에 대한 공식적인 Workaround는 아직 보고되지 않았습니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - **5.7.1 Hotfix**의 수정 사항이 EpicGames/UnrealEngine 리포지토리에 커밋되었습니다. [2]
    - 최근 7일간 EpicGames/UnrealEngine 공식 저장소의 **main 브랜치에 대한 주요 기술 커밋은 확인되지 않았습니다.**
- **영향받는 시스템:** 렌더링, 코어 기술, 에디터 안정성 등 엔진 전반
- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **Ask Epic: Mobile Development in UEFN** (2025년 12월 18일) [4]
    - Epic Staff가 UEFN(Unreal Editor for Fortnite)의 모바일 개발 관련 질의응답을 진행했습니다.
- **포럼 URL:** [Epic Developer Community Forums - Announcements](https://forums.unrealengine.com/c/general/announcements/49)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준):**
    - **Substrate Materials** **정식 출시** (Production-Ready) [1]
    - **PCG (Procedural Content Generation)** 프레임워크 **정식 출시** (Production-Ready) [1]
    - **In-editor AI Assistant** 도입 (F1 키로 컨텍스트 기반 도움말 및 코드 생성) [1]
- **Beta/Experimental 기능 및 주의사항 (UE 5.7 기준):**
    - **MegaLights** (Beta): 노이즈 감소 및 성능 개선, Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 [1]
    - **Nanite Foliage and Skinning** (Experimental): Nanite Assemblies, Nanite Voxels를 사용한 고밀도/고성능 폴리지 렌더링 [1]
    - **SMAA** (Experimental): 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원 [1]
- **성능 영향도:**
    - UE 5.7은 Nanite Foliage 시스템 및 기타 최적화를 통해 GPU 성능 최대 25%, CPU 성능 최대 35% 향상에 기여한다는 테스트 결과가 보고되었습니다. [5]

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **Game Animation Sample Project**가 UE 5.7에 맞춰 업데이트되었으며, **Mover 플러그인** 및 Smart Object 설정이 포함되었습니다. [6]
    - **MetaHuman Creator** 플러그인이 **Linux 및 macOS**를 지원합니다. [1]
- **문서 주요 변경사항:**
    - **Unreal Engine 5.7 Documentation**이 최신 기술에 맞춰 업데이트되었습니다. [7]

***

### References

[1] [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
[2] [5.7.1 Hotfix Released - Epic Developer Community Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
[3] [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)
[4] [Ask Epic: Mobile Development in UEFN – December 18, 11AM - 12PM ET](https://forums.unrealengine.com/c/general/announcements/49)
[5] [Unreal Engine 5.7 brings significant improvements over the notoriously demanding 5.4 version, tester claims — benchmark shows up to 25% GPU performance increase, 35% percent CPU boost](https://www.tomshardware.com/video-games/pc-gaming/unreal-engine-5-7-brings-significant-improvements-over-the-notoriously-demanding-5-4-version-tester-claims-benchmark-shows-up-to-25-percent-gpu-performance-increase-35-percent-cpu-boost)
[6] [Explore the updates to the Game Animation Sample project in UE 5.7](https://www.unrealengine.com/en-US/tech-blog/explore-the-updates-to-the-game-animation-sample-project-in-ue-5-7)
[7] [Unreal Engine 5.7 Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)
