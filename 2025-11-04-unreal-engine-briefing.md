# 언리얼 엔진 데일리 브리핑 | 2025년 11월 04일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **PCG 프레임워크** 정식 버전(Production-Ready) 전환 (UE 5.7 Preview) |
| | 2. **Substrate 머티리얼** 정식 버전(Production-Ready) 전환 (UE 5.7 Preview) |
| | 3. **UE 5.6.1 핫픽스** (270개 이상의 버그 수정, MetaHuman 관련 안정화) |
| **즉시 확인 필요 사항** | UE 5.7 정식 릴리즈 시 Linux 환경에서 **SDL2가 SDL3로 전환**될 예정. SDL2 커스터마이징 사용자는 변경 사항을 미리 확인해야 합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Preview](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (2025-09-23) |
| | [5.6.1 Hotfix Released](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316) (2025-08-12) |

## 2. 공식 릴리즈 및 패치

**버전 릴리즈:** Unreal Engine 5.6.1 Hotfix

**주요 변경사항 및 Breaking Changes:**

*   **버전 번호:** 5.6.1
*   **주요 변경사항:** 270개 이상의 수정 사항이 포함된 핫픽스입니다. 특히 **MetaHuman** 관련 크래시 및 에디터 성능 저하 문제(MH-15630, MH-15645 등) 해결에 중점을 두었습니다.
*   **Breaking Changes (예정):** UE 5.7부터 Linux 빌드 환경에서 **SDL2가 SDL3로 전환**됩니다. SDL2 코드를 커스터마이징한 사용자는 UE 5.7 전환 시 변경 사항을 적용해야 합니다.

**릴리즈 노트 URL:** [5.6.1 Hotfix Released - Announcements](https://forums.unrealengine.com/t/5-6-1-hotfix-released/2639316)

## 3. 버그 및 이슈

**새로 보고된 주요 버그 (최신 5개):**

| 이슈 ID | 요약 | 영향받는 시스템 |
| :--- | :--- | :--- |
| **Patterns On Landscape Spline Normals** | 고밀도 Landscape에서 Landscape Spline이 지오메트리 노멀에 패턴 아티팩트를 유발합니다. | Graphics Tools - Terrain |
| **Square Artifacts Appearing On Landscape Normals In Packaged Build** | 패키징된 빌드에서만 Landscape 지오메트리 노멀에 사각형 패턴이 나타납니다. | Graphics Tools - Terrain |
| **Virtual Texture Collection Indexing Not Working** | Virtual Texture Collection에서 인덱스 0이 아닌 텍스처를 샘플링할 수 없습니다. | Rendering Architecture - RHI |
| **Static Mesh Contact Shadows still render when all LOD sections have Cast Shadows dissabled** | 모든 LOD 섹션에서 그림자 캐스트가 비활성화되어도 Static Mesh의 Contact Shadows가 계속 렌더링됩니다. | Graphics Features |
| **Path Tracer Normals Issue** | Path Tracing 노멀 맵이 Lit 모드와 다르게 빛을 반사하며 정확하지 않습니다. | Graphics Features - Path Tracer |

**수정된 버그 (최신 5개):**

| 이슈 ID | 요약 | 영향받는 시스템 |
| :--- | :--- | :--- |
| **Ensure in FOnlineSubsystemSteam::Shutdown when using OSS Adapter** | OSS Adapter 사용 시 FOnlineSubsystemSteam::Shutdown에서 Ensure가 발생합니다. | Online |
| **Cloth Asset - Crash when importing morph targets into clothing** | Cloth Asset에 모프 타겟을 임포트할 때 크래시가 발생합니다. | Simulation - Visual |
| **Calling FOnlineIdentitySteam::GetLinkedAccountAuthToken without an internet connection won't execute callback delegate for WebAPI token type** | 인터넷 연결 없이 FOnlineIdentitySteam::GetLinkedAccountAuthToken 호출 시 WebAPI 토큰 타입에 대한 콜백 델리게이트가 실행되지 않습니다. | Online |
| **Some instances spawned by NeagaraDataInterfaceChaosDestruction breaking event will be set location to the world origin** | NiagaraDataInterfaceChaosDestruction 이벤트로 생성된 일부 인스턴스가 월드 원점으로 위치가 설정됩니다. | Niagara - Data Interface |
| **Video length indicator no longer works** | 다중 파트 비디오에서 누적 시간 표시기가 작동하지 않습니다. | Tools |

**Workaround:** 해당 정보는 Issue Tracker에 명시되어 있지 않습니다.

**Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 및 Pull Request에 대한 직접적인 정보는 수집되지 않았습니다.

**최신 정보가 없는 경우:** 최근 7일간 EpicGames/UnrealEngine GitHub 저장소에 대한 주요 업데이트 사항은 확인되지 않았습니다.

**GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**Epic Staff 답변 기술 스레드:**

*   **Unreal Engine 5.7 Preview** 공지 스레드에서 Epic Staff (TinaWisdom)가 릴리즈 정보를 제공하고 있습니다. 이 스레드는 **PCG, Substrate, Nanite Foliage** 등 핵심 기술의 정식 버전 전환 및 실험적 기능 도입에 대한 개발자들의 활발한 논의가 이루어지고 있습니다.

**포럼 URL:** [Unreal Engine 5.7 Preview - Announcements](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.7 Preview 기준):**

*   **Procedural Content Generation Framework (PCG):** **Production-Ready**로 전환되었습니다. GPU 성능 최적화(UE 5.5 대비 약 2배 향상), GPU 파라미터 오버라이드, FastGeo를 사용한 멀티플랫폼 지원 개선, 독립 실행형 PCG 그래프 실행 기능 등이 추가되었습니다.
*   **Substrate 머티리얼:** **Production-Ready**로 전환되었습니다. Adaptive GBuffer 및 Blendable GBuffer를 제공하며, 여러 머티리얼 레이어(금속, 클리어 코트, 스킨, 천 등)를 물리적으로 정확하게 결합할 수 있습니다.

**Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview 기준):**

| 기능 | 상태 | 주요 내용 | 주의사항 |
| :--- | :--- | :--- | :--- |
| **Procedural Vegetation Editor** | Experimental | Fab 에셋을 사용하여 Nanite 지원 폴리지(Foliage)를 에디터 내에서 실시간으로 생성, 커스터마이징 및 조립할 수 있습니다. | Experimental 기능이므로 프로덕션 사용에 주의가 필요합니다. |
| **Nanite Foliage** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxel 시스템을 통해 고밀도, 고디테일 폴리지를 60fps로 렌더링할 수 있습니다. | Experimental 기능이므로 프로덕션 사용에 주의가 필요합니다. |
| **MegaLights** | Beta | 디렉셔널 라이트, Niagara 파티클 라이트, 투명도 라이팅, 헤어 그룸 지원이 추가되었습니다. 해상도 스케일 및 업데이트 속도 조절을 위한 성능 튜닝 컨트롤이 제공됩니다. | Beta 기능이므로 안정성 테스트가 필요합니다. |
| **MetaHuman Creator Plugin** | 정식 기능 확장 | Linux 및 macOS 지원이 추가되었으며, Python 및 Blueprint API를 통해 MetaHuman 에셋의 편집 및 조립 작업을 스크립팅할 수 있습니다. | |
| **Animation/Rigging 툴 개선** | Experimental | **Selection Sets** (애니메이션 워크플로우 간소화), **Blend shapes and Sculpting** (스컬프팅 워크플로우 통합), **Physics World Collisions** (현실적인 환경 상호작용) 등이 실험적으로 개선되었습니다. | Experimental 기능이므로 프로덕션 사용에 주의가 필요합니다. |

**성능 영향도:**

*   **PCG:** GPU 성능 및 게임 스레드 성능이 최적화되어 UE 5.5 대비 약 2배 빨라졌습니다.
*   **Nanite Foliage:** Nanite 시스템을 활용하여 고밀도 폴리지를 낮은 비용으로 60fps에서 렌더링할 수 있도록 설계되었습니다.

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트:**

*   **MetaHuman Creator Plugin:** Linux 및 macOS 지원이 추가되었으며, Python 및 Blueprint API를 통한 스크립팅 기능이 확장되었습니다.

**문서 주요 변경사항:**

*   UE 5.7 Preview 릴리즈와 함께 **PCG, Substrate, Nanite Foliage** 등 주요 기능에 대한 문서가 업데이트되었을 것으로 예상됩니다. (직접적인 문서 변경사항 URL은 수집되지 않았습니다.)

**참고:** 본 보고서에 포함된 모든 정보는 2025년 11월 04일 기준으로 Epic Games의 공식 채널(포럼, 이슈 트래커)에서 확인된 가장 최신 정보를 기반으로 작성되었습니다. 최근 7일 이내의 새로운 릴리즈나 핫픽스는 없었으며, 가장 최신 릴리즈는 2025년 8월 12일의 UE 5.6.1 핫픽스입니다. 최신 개발 동향은 2025년 9월 23일에 발표된 UE 5.7 Preview를 중심으로 분석되었습니다.
