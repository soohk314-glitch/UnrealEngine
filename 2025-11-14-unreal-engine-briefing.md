# 언리얼 엔진 데일리 브리핑 | 2025년 11월 14일

## 1. 핵심 요약

| 순위 | 주요 업데이트 | 즉시 확인 필요 사항 | 출처 URL 및 게시일 (YYYY-MM-DD) |
| :--- | :--- | :--- | :--- |
| 1 | **PCG (Procedural Content Generation) 프레임워크 정식 출시 (Production-Ready)** | 대규모 환경 생성 파이프라인에 PCG를 사용하는 프로젝트는 새로운 **PCG Editor Mode** 및 **GPU 컴퓨팅 최적화**를 확인하고 통합해야 합니다. | [Unreal Engine 5.7 is now available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |
| 2 | **Substrate (재질 시스템) 정식 출시 (Production-Ready)** | **레이어드 및 블렌딩 재질**을 사용하는 프로젝트는 Substrate로의 전환을 고려하여 물리적으로 정확한 고품질 재질 표현을 확보해야 합니다. | [Unreal Engine 5.7 is now available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |
| 3 | **MegaLights 기능 베타 전환** | 동적 그림자 캐스팅 광원 수를 대폭 늘릴 수 있는 **MegaLights**가 베타로 전환되었습니다. 복잡한 조명 환경에서 성능 및 시각적 품질 개선 가능성을 확인해야 합니다. | [Unreal Engine 5.7 is now available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** Unreal Engine **5.7** (2025년 11월 12일 정식 출시)
- **주요 변경사항 및 Breaking Changes:**
    - **PCG** 및 **Substrate**가 정식 버전(Production-Ready)으로 전환되었습니다.
    - **MegaLights**가 베타 버전으로 전환되어 방향성 광원, 반투명, Niagara 파티클의 그림자 캐스팅 지원이 추가되었습니다.
    - **MetaHuman Creator** 플러그인이 **Linux** 및 **macOS**를 지원합니다.
    - **애니메이션 모드**가 리팩토링되어 워크플로우가 간소화되었으며, **Selection Sets** 기능이 추가되었습니다.
    - **IK Retargeter**가 발-지면 접촉 개선, 스쿼시 및 스트레치 리타겟팅, 캐릭터 자체 충돌 방지 기능이 개선되었습니다.
    - **Composure** (실시간 합성 도구)가 개선되어 라이브 비디오 및 파일 기반 이미지 플레이트를 처리하며, 24fps 실시간 결과를 제공합니다.
- **릴리즈 노트 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

| 구분 | 이슈 제목 | 영향받는 시스템/영역 | Workaround/상태 |
| :--- | :--- | :--- | :--- |
| **새로 보고된 주요 버그** | Mesh Variation node usage inside macro - lost of material slot name | UE - Anim - Mutable | 매크로 인스턴스 스크립트 내에서 `Mesh Variation` 노드를 사용할 때 재질 슬롯 이름이 전송되지 않음. |
| | AsyncSaveGameToSlotForLocalPlayer does not properly handle multiple requests | UE - Gameplay | `ULocalPlayerSaveGame::AsyncSaveGameToSlotForLocalPlayer`가 여러 동시 요청을 제대로 처리하지 못함. |
| | Crash at Skeleton Remapping | UE - Anim - Rigging - Retargeting | Skeleton Remapping 시 크래시 발생. |
| **수정된 버그** | Sequencer Crash when Hovering over Binding Properties on a Component with Spaces in its Name | UE - Anim - Sequencer | 이름에 공백이 있는 컴포넌트의 바인딩 속성에 마우스를 올릴 때 크래시 발생 문제 수정. |
| | GetStaticRayTracingGeometries doesn't check if mesh has ray tracing disabled | UE - Graphics Features - Ray Tracing | 레이 트레이싱이 비활성화된 스켈레탈 메시 애셋에 대해 정적 레이 트레이싱 지오메트리 확인 시 문제가 발생하던 부분 수정. |
| **Issue Tracker URL:** | [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/) | | |

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - Unreal Engine 5.7 정식 릴리즈에 맞춰 **`EpicGames/UnrealEngine`** 저장소의 **`release`** 브랜치에 대규모 업데이트가 반영되었습니다.
    - **`ue5-main`** 브랜치에서는 5.7 이후의 개발 작업이 활발하게 진행 중입니다.
    - **최근 7일간의 개별적인 주요 커밋/PR에 대한 상세 정보는 GitHub API 접근 제한으로 인해 직접적인 추출이 어렵습니다.** (일반적인 GitHub 활동은 릴리즈 노트에 통합되어 제공됨)
- **영향받는 시스템:** 엔진 전반
- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **Unreal Engine 5.7 Released** 스레드에서 Epic Games 직원이 릴리즈 관련 질문에 답변하고 있습니다. (게시일: 2일 전)
    - **Unreal Engine 5.7 Preview** 스레드에서 5.7 프리뷰 기간 동안의 성능 및 기능 관련 기술적 논의가 진행되었습니다.
- **포럼 URL:** [Epic Developer Community Forums](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **PCG Editor Mode** | Production-Ready | PCG 프레임워크를 기반으로 스플라인, 페인트, 볼륨 등을 활용하여 환경을 생성하는 편집 모드. | PCG GPU 컴퓨팅 최적화로 성능 향상. |
| **Nanite Foliage** | Experimental | 조밀하고 디테일한 **나뭇잎**을 효율적으로 렌더링하기 위한 새로운 지오메트리 렌더링 시스템. **Nanite Voxels** 및 **Nanite Assemblies** 활용. | 대규모 오픈 월드에서 안정적인 프레임 속도 유지에 도움. |
| **AI Assistant** | New Feature | 에디터 내에서 질문, C++ 코드 생성, 단계별 가이드를 제공하는 AI 기반 도우미. F1 키로 인터페이스 요소에 대한 대화 시작 가능. | 직접적인 런타임 성능 영향은 없으나 개발 생산성 향상. |
| **MegaLights** | Beta | 동적 그림자 캐스팅 광원의 수를 대폭 늘릴 수 있는 조명 시스템. | 성능 개선 및 노이즈 감소.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman Creator** 플러그인이 **Linux** 및 **macOS** 플랫폼을 지원하도록 확장되었습니다.
    - **MetaHuman for Houdini** 업데이트를 통해 가이드 기반 헤어스타일 생성 워크플로우가 제공됩니다.
- **문서 주요 변경사항:**
    - Unreal Engine 5.7 릴리즈에 맞춰 **PCG, Substrate, MegaLights, Nanite Foliage** 등 주요 기능에 대한 공식 문서가 업데이트 및 보강되었습니다.
    - **IK Retargeter** 및 **Animation Mode** 관련 문서가 리팩토링된 워크플로우에 맞춰 업데이트되었습니다.
    - **Composure**의 새로운 버전 및 기능에 대한 문서가 추가되었습니다.
