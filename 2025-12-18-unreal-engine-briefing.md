# 언리얼 엔진 데일리 브리핑 | 2025년 12월 18일

실무 개발자를 위한 언리얼 엔진의 최신 기술 업데이트 및 이슈 보고서입니다.

## 1. 핵심 요약

| 구분 | 내용 | 출처 URL 및 게시일 |
| :--- | :--- | :--- |
| **주요 업데이트 1** | **UE 5.7.1 핫픽스 출시**: 약 100여 개의 버그 및 크래시 수정 사항이 포함된 최신 핫픽스 릴리즈. | [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |
| **주요 업데이트 2** | **UE 5.7 공식 릴리즈**: MegaLights (Beta), Niagara Heterogeneous Volumes (Beta), Substrate (Production-Ready), Nanite Foliage/Skinning (Experimental) 등 대규모 신기능 도입. | [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |
| **주요 업데이트 3** | **Microsoft GDK 플러그인 출시**: Xbox PC 앱으로 게임을 가져오는 프로세스를 간소화하는 GDK 플러그인 정식 출시. | [https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/](https://developer.microsoft.com/en-us/games/articles/2025/12/microsoft-gdk-plug-ins-for-unreal-engine-now-available/) (2025-12-12) |
| **즉시 확인 필요 사항** | **UE 5.7.1 핫픽스 적용**: 5.7 버전에서 보고된 다수의 크래시 및 버그가 수정되었으므로, 5.7 사용자들은 안정성 향상을 위해 즉시 업데이트를 고려해야 합니다. 특히 **MetaHuman 관련 크래시** (MH-16702, MH-16864) 및 **에디터 응답 없음** (UE-193929) 이슈가 해결되었습니다. | [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈**: **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항 및 Breaking Changes**:
    - 5.7.1은 5.7.0의 안정성 및 버그 수정을 위한 핫픽스입니다.
    - **Linux 환경**: UE 5.7부터 Linux는 SDL2에서 **SDL3**로 전환됩니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경 사항을 재작업해야 합니다.
    - 약 100여 개의 수정 사항이 포함되었으며, 특히 렌더링, 컨트롤 릭, MetaHuman, PCG, nDisplay 관련 크래시 및 버그가 다수 해결되었습니다.
- **릴리즈 노트 URL**:
    - 5.7.1 핫픽스 포럼 공지: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
    - 5.7 공식 릴리즈 노트: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (Issue Tracker 기준)**:
    - `UE-Anim-Sequencer`: `Section::TrimSection`이 트림 범위의 시작 및 끝에서 잘못된 키 값을 초래함.
    - `UE-World Creation`: `UWorldPartition::ApplyRuntimeCellsTransformerStack`에서 `ActorComponents`가 잘못된 월드에 등록됨.
    - `UE-Graphics Features`: 뷰포트 궤도/줌 탐색 중 지속적인 끊김(stuttering) 현상 발생.
    - `UE-Graphics Features - Ray Tracing`: 비활성화된 스켈레탈 메시 섹션이 섀도우 레이 트레이싱 깜빡임(Flicker)을 유발함.
- **수정된 버그 (5.7.1 핫픽스 기준)**:
    - `UE-193929`: Path Tracing 뷰 모드 활성화 시 에디터 응답 없음.
    - `UE-227868`: 시네마틱 MetaHuman이 레벨 뷰포트에서 AMD GPU 크래시 유발.
    - `UE-295331`: RHI GPUProfiler 관련 크래시.
    - `MH-16702`: MetaHuman 캐릭터가 고화질 LOD로 변경될 때 여러 플랫폼에서 크래시 발생.
    - `UE-350214`: Mover 캐릭터 몽타주 복제(replication) 비동기화 문제.
- **Workaround**:
    - **DDC Cache Error (UE 5.7/5.7.1)**: 일부 사용자에게서 발생하는 DDC 캐시 오류는 `C:\Users\[YourUsername]\AppData\Local\UnrealEngine\Common` 경로의 캐시를 삭제하고 에디터를 재시작하여 해결할 수 있습니다.
- **Issue Tracker URL**: [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**:
    - Epic Games의 공식 UnrealEngine 저장소는 비공개이며, 접근을 위해서는 Epic Games 계정과 GitHub 계정 연동이 필요합니다.
    - 5.7.1 핫픽스에는 `GitHub 13887`과 같은 GitHub 이슈/PR 참조가 포함되어 있으며, 이는 `Free pending-delete Virtual Texture immediately in Loadmap to avoid the fatal assert in FVirtualTextureAllocator::AcquireBlock` 관련 수정 사항입니다.
- **영향받는 시스템**: 가상 텍스처(Virtual Texture) 시스템의 안정성.
- **GitHub URL**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) (접근 권한 필요)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**:
    - **5.7.1 Hotfix Released** 스레드가 가장 최근의 공식적인 기술 업데이트 논의입니다. (작성자: TinaWisdom, Epic Staff)
    - 주요 내용은 5.7.1 핫픽스에 포함된 약 100개의 수정 사항 목록과 5.7 버전부터 Linux의 SDL3 전환에 대한 주의사항입니다.
- **포럼 URL**:
    - 5.7.1 Hotfix 스레드: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)
    - Epic Developer Community Forums: [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준)**:
    - **Substrate**: 프로덕션 준비 완료(Production-Ready) 상태로 전환되어 기본 활성화되었습니다. 모듈식의 물리 기반 머티리얼 프레임워크를 제공합니다.
    - **World Collisions for Control Rig Physics**: Control Rig Physics 시뮬레이션에 레벨 충돌을 가져와 현실적인 상호작용을 생성할 수 있습니다.
- **Beta/Experimental 기능 및 주의사항 (UE 5.7 기준)**:
    - **MegaLights (Beta)**: 노이즈 감소 및 성능 개선. Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원 추가.
    - **Niagara Heterogeneous Volumes (Beta)**: 그림자 캐스팅 개선. Cascade shadows 및 Beer Shadow Map 지원.
    - **Nanite Foliage and Skinning (Experimental)**: Nanite Assemblies, Nanite Skinning, Nanite Voxels를 통해 대규모 환경에서 고성능의 동적 폴리지 렌더링을 가능하게 합니다.
    - **SMAA (Experimental)**: 모바일 및 데스크톱 렌더러에서 Subpixel Morphological Anti-Aliasing 지원. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화 가능.
    - **Motion Matching Chooser Integration (Experimental)**: 모션 매칭에 Chooser를 통합하여 에셋 선택의 유연성을 높였습니다.
- **성능 영향도**:
    - **FBIK 및 Retargeting 성능 개선**: Full Body IK 및 IK Retargeter의 성능이 향상되었습니다 (FBIK 포징 약 20% 속도 향상).

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**:
    - **Microsoft GDK Plug-ins for Unreal Engine**이 공식적으로 출시되었습니다. Xbox PC 앱으로 게임을 배포하는 과정을 간소화합니다.
    - **LIV Creator Kit for Unreal Engine**이 퍼블릭 베타로 출시되었습니다. (외부 플러그인)
- **문서 주요 변경사항**:
    - **Level Streaming Hitching Guide** 문서가 업데이트되어, Unreal Insights 캡처에서 레벨 스트리밍 끊김 현상을 인식하고 해결하는 팁을 제공합니다.
    - **MetaHuman 5.7** 관련 문서가 업데이트되어, 새로운 기능(광범위한 플랫폼 지원, 절차적 그루밍, 실시간 헤어 애니메이션 등)을 반영했습니다.
