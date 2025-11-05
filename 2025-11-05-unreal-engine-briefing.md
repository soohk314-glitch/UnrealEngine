# 언리얼 엔진 데일리 브리핑 | 2025년 11월 05일

작성일: 2025년 11월 05일 18:05 KST

## 1. 핵심 요약

**주요 업데이트 상위 3개 (Unreal Engine 5.7 Preview 기준)**
- **PCG(Procedural Content Generation Framework) 정식 출시(Production-Ready):** GPU 성능 최적화 및 확장성 향상. GPU 파라미터 오버라이드, FastGeo를 활용한 멀티플랫폼 지원 강화.
- **Substrate Materials 정식 출시(Production-Ready):** 고정된 셰이딩 모델을 대체하는 모듈형 시스템으로, Adaptive GBuffer와 Blendable GBuffer를 제공하며, 여러 재질 레이어(금속, 클리어 코트, 피부, 천 등)를 물리적으로 정확하게 결합 가능.
- **Nanite Foliage (Experimental):** 나나이트 기반의 새로운 렌더링 경로로, Nanite Assemblies, Nanite Skinning, Nanite Voxel 시스템을 통해 고밀도, 고디테일의 폴리지(Foliage)를 60fps로 부드럽게 렌더링 가능.

**즉시 확인 필요 사항**
- **Unreal Engine 5.7 Preview 사용 시 주의:** Preview 버전은 품질 테스트가 완료되지 않았으며 불안정할 수 있으므로, 테스트용 프로젝트 복사본을 사용하여 변환하는 것을 권장합니다.
- **MetaHuman Creator 플러그인 Linux 및 macOS 지원:** MetaHuman Creator Python 및 Blueprint API를 통해 MetaHuman 캐릭터 에셋의 편집 및 조립 작업을 스크립트로 자동화할 수 있습니다.
- **Epic Developer Assistant (5.7 정식 출시 예정):** 현재 Preview 버전 UI는 보이지만, 기능은 5.7.0 정식 출시와 함께 제공될 예정입니다.

**출처 URL 및 게시일**
- Unreal Engine 5.7 Preview: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (2025-09-23)
- Unreal Engine 5.6 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes) (최신 정식 릴리즈)

## 2. 공식 릴리즈 및 패치

**버전 릴리즈**
- **최신 정식 버전:** Unreal Engine 5.6 (2025년 6월 3일 출시)
- **최신 프리뷰 버전:** Unreal Engine 5.7 Preview (2025년 9월 23일 출시)

**주요 변경사항 및 Breaking Changes (UE 5.6 기준)**
- **주요 변경사항:** 렌더링, 월드 빌딩, 애니메이션, MetaHuman, PCG 등 광범위한 영역에서 개선이 이루어졌습니다.
- **Breaking Changes:** Control Rig, Material, Dataflow, Physics, 그리고 XR 관련 API의 일부 변경 사항이 기존 프로젝트의 호환성에 영향을 줄 수 있습니다. 특히 Control Rig의 일부 함수가 Deprecated 되었고, Material 시스템의 Shader Symbol 처리 방식 변경 및 OpenXR/VR/AR 관련 API 변경에 대한 검증이 필요합니다.

**릴리즈 노트 URL**
- Unreal Engine 5.6 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes)
- Unreal Engine 5.7 Preview Announcement: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)

## 3. 버그 및 이슈

**새로 보고된 주요 버그 (최근 7일 이내, Unresolved 기준)**
| 날짜 | 이슈 제목 | 구성 요소 | 버전 |
| :--- | :--- | :--- | :--- |
| 2025-11-05 | Cloud materials not loaded in local Presentations | TM - Core | Unresolved |
| 2025-11-04 | GAS: FActiveGameplayCueContainer::RemoveCue crash while iterating removals when consecutive Cue tags are conditionally added and the conditional effects removed in ascending order | UE - Gameplay - Gameplay Ability System | Unresolved |
| 2025-10-31 | Patterns On Landscape Spline Normals | UE - Graphics Tools - Terrain | Unresolved |
| 2025-10-31 | Square Artifacts Appearing On Landscape Normals In Packaged Build | UE - Graphics Tools - Terrain | Unresolved |
| 2025-10-30 | Virtual Texture Collection Indexing Not Working | UE - Rendering Architecture - RHI | Backlogged |

**수정된 버그**
- **최근 7일간 새로운 업데이트 사항이 없습니다.** (이슈 트래커 검색 결과 기준)

**Workaround**
- **최근 7일간 새로운 업데이트 사항이 없습니다.** (이슈 트래커 검색 결과 기준)

**Issue Tracker URL**
- Unreal Engine Issues and Bug Tracker: [https://issues.unrealengine.com/issue/search](https://issues.unrealengine.com/issue/search)

## 4. GitHub 업데이트

**주요 커밋 및 Pull Request**
- **최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 정보를 직접적으로 확인할 수 없었습니다.** (GitHub 접속 시 로그인 페이지로 리디렉션됨)
- **가장 최근의 대규모 업데이트는 Unreal Engine 5.7 Preview 릴리즈와 관련된 커밋으로 추정됩니다.** (2025-09-23)

**영향받는 시스템**
- **정보 없음**

**GitHub URL**
- EpicGames/UnrealEngine: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**Epic Staff 답변 기술 스레드**
- **Unreal Engine 5.7 Preview** 관련 스레드에서 Epic Staff인 **TinaWisdom**이 주요 기능과 변경 사항에 대해 상세히 설명하고 있습니다.
- **주요 내용:** PCG 정식 출시, Substrate Materials 정식 출시, Nanite Foliage 실험적 기능, MegaLights 베타, MetaHuman Creator 업데이트, 애니메이션 및 리깅 도구 개선 등.

**포럼 URL**
- Unreal Engine 5.7 Preview - Announcements: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.7 Preview 기준)**
- **PCG (Procedural Content Generation Framework) 정식 출시:** GPU 성능 최적화, GPU 파라미터 오버라이드, PCG 전용 에디터 모드 추가.
- **Substrate Materials 정식 출시:** 모듈형 셰이딩 시스템으로 다중 재질 레이어 결합 가능.
- **MetaHuman Creator Python 및 Blueprint API:** MetaHuman 에셋 편집 및 조립 스크립트 자동화.
- **애니메이션 Selection Sets:** 리그 내 다중 컨트롤에 빠르게 접근하여 워크플로우 간소화.
- **Skeletal Editor 도구 업데이트:** 모프 셰이프, 본, 스킨 웨이트 생성 및 편집 기능 추가.

**Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview 기준)**
- **Beta:** **MegaLights** (방향성 광원, Niagara 파티클 광원, 반투명 조명, 헤어 그룸 지원).
- **Experimental:** **Procedural Vegetation Editor** (Fab 에셋을 사용하여 나나이트 지원 폴리지를 에디터에서 직접 생성 및 커스터마이징), **Nanite Foliage** (고밀도 폴리지를 위한 나나이트 기반 렌더링 경로), **Blend shapes and Sculpting** (리깅 도구), **Physics World Collisions** (캐릭터와 환경 간의 현실적인 상호작용).
- **주의사항:** Preview 버전은 불안정하며, **Epic Developer Assistant**는 5.7 정식 출시 시점에 제공될 예정입니다.

**성능 영향도**
- **PCG:** GPU 생성 및 게임 스레드 성능이 UE 5.5 대비 **거의 두 배**로 최적화되었습니다.
- **Nanite Foliage:** Nanite Assemblies, Nanite Skinning, Nanite Voxel 시스템을 통해 고디테일 폴리지를 **60 fps**로 부드럽게 렌더링 가능합니다.
- **MegaLights:** 새로운 성능 튜닝 컨트롤을 통해 해상도 스케일 및 업데이트 속도를 관리하여 기본 성능을 개선하고 노이즈 감소를 향상시켰습니다.

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트**
- **MetaHuman Creator 플러그인:** Linux 및 macOS 지원 추가.
- **Procedural Vegetation Editor:** 새로운 **Experimental** 플러그인으로 추가.

**문서 주요 변경사항**
- **Unreal Engine 5.6 Release Notes** 문서가 최신 정식 릴리즈 정보를 제공하고 있습니다.
- **Unreal Engine 5.7 Preview** 관련 문서 및 포럼 공지가 새로운 기능에 대한 상세 정보를 제공하고 있습니다.
- **최근 7일간 새로운 업데이트 사항이 없습니다.** (공식 문서 변경 이력 검색 결과 기준)
