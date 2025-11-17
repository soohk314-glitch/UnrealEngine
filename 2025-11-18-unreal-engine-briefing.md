# 언리얼 엔진 데일리 브리핑 | 2025년 11월 18일

## 1. 핵심 요약

언리얼 엔진 5.7이 공식 출시되었으며, **PCG(Procedural Content Generation) 프레임워크**의 정식 버전 출시와 **Substrate** 머티리얼 시스템의 프로덕션 레디 전환이 가장 큰 핵심입니다. 또한, **Nanite Foliage**와 **MegaLights**의 발전은 대규모 오픈 월드 환경 구축에 혁신적인 변화를 가져왔습니다.

- 주요 업데이트 상위 3개
    1.  **PCG 프레임워크 정식 버전 (Production-Ready) 출시**: 대규모 환경 생성을 위한 핵심 툴셋이 안정화되었으며, 새로운 PCG 에디터 모드와 GPU 컴퓨팅 최적화가 포함되었습니다.
    2.  **Substrate 머티리얼 시스템 정식 버전 (Production-Ready) 출시**: 레이어드 및 블렌딩 머티리얼을 위한 최첨단 프레임워크가 모든 UE5 타겟 플랫폼에서 일관된 성능과 시각적 충실도를 제공하며 정식으로 사용 가능해졌습니다.
    3.  **Nanite Foliage (Experimental) 도입**: 대규모, 고밀도, 고디테일의 폴리지 환경을 효율적으로 렌더링하기 위한 새로운 지오메트리 렌더링 시스템이 실험 단계로 공개되었습니다.

- 즉시 확인 필요 사항
    *   **Sequencer 관련 버그**: `LevelSequenceActor transform offset for Sequencer lost on value changed` 버그가 최신 버그로 보고되었습니다. 시퀀서 사용자는 해당 이슈를 확인해야 합니다.
    *   **MetaHuman for Houdini 출시**: Houdini 사용자를 위한 MetaHuman 업데이트가 발표되어 헤어 스타일링 워크플로우가 개선되었습니다.

- 출처 URL 및 게시일 (KST 기준)
    *   Unreal Engine 5.7 is now available: [https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12)
    *   Unreal Engine Issues and Bug Tracker: [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (최신 정보)
    *   Unreal Engine 5.7 Released (Forum): [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) (2025-11-12)

## 2. 공식 릴리즈 및 패치

- 버전 릴리즈 (정확한 버전 번호)
    *   **Unreal Engine 5.7** (2025년 11월 12일 출시)

- 주요 변경사항 및 Breaking Changes
    *   **PCG 프레임워크**: **Production-Ready** 상태로 전환. PCG 에디터 모드 추가, PCG GPU 컴퓨팅 성능 최적화.
    *   **Substrate**: **Production-Ready** 상태로 전환. 레이어드 및 블렌딩 머티리얼 지원 강화.
    *   **MegaLights**: Experimental에서 **Beta** 상태로 전환. 동적 그림자 캐스팅 광원 수 대폭 증가.
    *   **MetaHuman 통합**: Linux 및 macOS에서 MetaHuman Creator 플러그인 지원. Python/Blueprint 스크립팅을 통한 배치 처리 및 편집/어셈블리 작업 자동화 기능 추가.
    *   **애니메이션 툴셋**: 리팩토링된 애니메이션 모드, **Selection Sets** 기능 추가, IK Retargeter 개선 (발-지면 접촉, 스쿼시/스트레치 리타겟팅), 스켈레탈 에디터에서 **블렌드 셰이프 스컬프팅** 지원.

- 릴리즈 노트 URL
    *   [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- 새로 보고된 주요 버그 (Latest Bugs)
    | 이슈 제목 | 카테고리 | 설명 |
    | :--- | :--- | :--- |
    | LevelSequenceActor transform offset for Sequencer lost on value changed | UE - Anim - Sequencer | 서브 시퀀스에서 잠금, 고정, 무시 토글 또는 새 트랜스폼 키 추가 시 LevelSequenceActor의 트랜스폼 오프셋이 손실됨. |
    | Can not paint vegetation with brush diameter of 1m or less | TM - Tools | 브러시 직경이 1m 이하일 때 식물 페인팅이 불가능함. |
    | Control Rig Box Selection Innacurate | UE - Anim - Rigging - Control Rig | 리그에서 마키 선택 시 컨트롤의 화면 크기에 따라 선택 정확도가 부정확해짐. |

- 수정된 버그 (Latest Fixes)
    | 이슈 제목 | 카테고리 | 설명 |
    | :--- | :--- | :--- |
    | Skeletal mesh ddc key is always regenerated on load when LOD bones to remove are set | UE - Anim - Rigging | LOD에서 제거할 본이 설정된 경우 로드 시 스켈레탈 메시 DDC 키가 항상 재생성되는 문제 수정. |
    | Sequencer Crash when Hovering over Binding Properties on a Component with Spaces in its Name | UE - Anim - Sequencer | 이름에 공백이 있는 컴포넌트의 바인딩 속성에 마우스를 올릴 때 시퀀서 충돌 발생 문제 수정. |
    | AsyncSaveGameToSlotForLocalPlayer does not properly handle multiple requests | UE - Gameplay | `AsyncSaveGameToSlotForLocalPlayer`가 여러 개의 동시 요청을 제대로 처리하지 못하는 문제 수정. |

- Workaround
    *   이슈 트래커 페이지에서 별도의 Workaround 정보는 제공되지 않았습니다.

- Issue Tracker URL
    *   [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- 주요 커밋 및 Pull Request
    *   최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 및 Pull Request에 대한 상세 정보는 현재 수집되지 않았습니다. (GitHub CLI를 통한 상세 분석 필요)
    *   **최신 정보가 없으므로, 최근 7일간 새로운 업데이트 사항이 없습니다.**

- 영향받는 시스템
    *   정보 없음

- GitHub URL
    *   [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- Epic Staff 답변 기술 스레드
    *   **Unreal Engine 5.7 Released**: 공식 릴리즈 발표 스레드. Epic Staff가 직접 게시했으며, 릴리즈 노트 링크 및 주요 변경사항에 대한 논의가 활발합니다.
    *   **MetaHuman 5.7 Released!**: MetaHuman 5.7 릴리즈 발표 스레드. Epic Staff가 게시.
    *   **MetaHuman for Houdini Release**: Houdini용 MetaHuman 릴리즈 발표 스레드. Epic Staff가 게시.

- 포럼 URL
    *   [https://forums.unrealengine.com/c/general/announcements/49](https://forums.unrealengine.com/c/general/announcements/49)

## 6. 신기능 및 실험적 기능

- 새로 추가된 기능
    *   **AI Assistant**: 에디터 내에서 질문, C++ 코드 생성, 단계별 가이드를 제공하는 AI 어시스턴트 기능 추가. (Instant help at your fingertips)
    *   **Selection Sets**: 애니메이션 툴셋에서 여러 컨트롤을 한 번의 클릭으로 선택할 수 있는 기능 추가.
    *   **Dynamic Constraint Component for Props**: 모션 캡처 워크플로우에서 소품이 손 위치에 자동으로 부착되고 부드럽게 보간되는 기능.
    *   **Live Link Broadcast Component**: 언리얼 엔진이 네트워크를 통해 애니메이션 데이터 소스로 작동하여 멀티 머신 VP 및 모캡 스테이지 워크플로우를 지원.

- Beta/Experimental 기능 및 주의사항
    *   **Nanite Foliage**: **Experimental** 기능. 성능, 견고성 및 확장성을 위해 설계된 새로운 지오메트리 렌더링 시스템. **Nanite Voxels** 및 **Nanite Assemblies**를 활용.
    *   **MegaLights**: Experimental에서 **Beta**로 전환. 더 많은 동적 그림자 캐스팅 광원을 지원.
    *   **Composure (업데이트)**: 실시간 컴포지팅 툴이 개선되어 라이브 비디오 입력 및 파일 기반 이미지 미디어 플레이트를 처리하며, 24fps로 실시간 결과를 제공. 새로운 **그림자 및 반사 통합** 기능 추가.

- 성능 영향도
    *   **PCG GPU compute**: 성능 최적화로 **상당히 빨라짐**.
    *   **Substrate**: 모바일 플랫폼까지 확장 가능하도록 구축되어 **일관된 성능과 시각적 충실도** 보장.

## 7. 플러그인 및 문서 업데이트

- 공식 플러그인 업데이트
    *   **MetaHuman Creator Plugin**: Linux 및 macOS 지원 추가.
    *   **MetaHuman for Houdini**: 가이드 기반 헤어 스타일 생성 워크플로우를 제공하는 업데이트 출시.

- 문서 주요 변경사항
    *   Unreal Engine 5.7 릴리즈에 맞춰 PCG, Substrate, Nanite Foliage, MegaLights, MetaHuman, 애니메이션 툴셋, 가상 프로덕션 등 주요 기능에 대한 문서가 업데이트되었습니다.
    *   새로운 **Unreal Editor Home Panel**에서 튜토리얼, 문서, 뉴스, 포럼 및 최근 프로젝트에 직접 접근 가능.
