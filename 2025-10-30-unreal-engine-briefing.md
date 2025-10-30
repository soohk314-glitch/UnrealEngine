# 언리얼 엔진 데일리 브리핑 | 2025년 10월 30일

본 보고서는 실무 개발자를 위해 언리얼 엔진의 최신 기술 업데이트, 릴리즈, 패치, 버그 정보를 요약하여 제공합니다.

## 1. 핵심 요약

| 순위 | 주요 업데이트 | 영향 영역 | 출처 URL | 게시일 (YYYY-MM-DD) |
| :---: | :--- | :--- | :--- | :--- |
| 1 | **PCG (Procedural Content Generation Framework) 정식 출시 준비 완료 (Production-Ready)** | 콘텐츠 생성, 성능 | [Epic Developer Community Forums](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) | 2025-09-23 |
| 2 | **MegaLights 베타 전환 및 성능 개선** | 렌더링, 조명 | [Epic Developer Community Forums](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) | 2025-09-23 |
| 3 | **Substrate 머티리얼 시스템 정식 출시 준비 완료 (Production-Ready)** | 렌더링, 머티리얼 | [Epic Developer Community Forums](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) | 2025-09-23 |

**즉시 확인 필요 사항**

*   **UE 5.7 Preview 사용 시 주의:** Preview 버전은 안정성이 보장되지 않으므로, 테스트용 프로젝트 복사본을 사용하여 테스트할 것을 권장합니다.
*   **Android 빌드 문제 (UE 5.6.1):** 최근 포럼에서 UE 5.6.1 버전에서 Android 빌드 시 EOS(Epic Online Services) SDK 업데이트 확인 루프 또는 셰이더 컴파일러 관련 문제로 빌드가 멈추는 현상이 보고되었습니다. 임시 해결책으로 `Intermediate`, `Saved`, `Binaries/Android` 폴더를 삭제하고 EOS 플러그인을 비활성화하는 방법이 제시되었습니다.

## 2. 공식 릴리즈 및 패치

**버전 릴리즈**
가장 최근의 공식 발표된 주요 릴리즈는 **언리얼 엔진 5.7 Preview**입니다.

*   **버전 번호:** 5.7 Preview
*   **주요 변경사항:**
    *   **PCG** 프레임워크가 **Production-Ready**로 전환되어 GPU 성능 및 확장성이 크게 향상되었습니다.
    *   **MegaLights**가 베타로 전환되었으며, 방향성 광원, Niagara 파티클 광원, 투명도 조명, 헤어 그룸을 지원합니다.
    *   **Substrate** 머티리얼 시스템이 **Production-Ready**로 전환되어, 고품질의 물리적 정확도를 가진 복합 머티리얼 레이어 조합이 가능해졌습니다.
*   **Breaking Changes:** Preview 버전이므로 잠재적인 변경 사항이 있을 수 있습니다. 정식 릴리즈 시 릴리즈 노트를 확인해야 합니다.
*   **릴리즈 노트 URL:** [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)
*   **게시일:** 2025-09-23

## 3. 버그 및 이슈

**새로 보고된 주요 버그 (최근 7일 이내)**
*   **UE 5.6.1 Android 빌드 문제:** Android 빌드 시 EOS SDK 업데이트 체크 또는 셰이더 컴파일러 관련 로그 루프 현상으로 빌드가 멈추는 문제가 포럼에 보고되었습니다. (2025-10-27)
    *   **Workaround:** 프로젝트의 `Intermediate`, `Saved`, `Binaries/Android` 폴더를 삭제하고, EOS 플러그인이 불필요하다면 임시로 비활성화합니다.
*   **Issue Tracker 최신 버그:**
    *   Virtual Texture Collection 인덱싱 문제 (`UE - Graphics Features`)
    *   Static Mesh Contact Shadows가 `Cast Shadows` 비활성화 후에도 렌더링되는 문제 (`UE - Graphics Features`)

**수정된 버그 (최신 수정 사항)**
*   **Issue Tracker 최신 수정 사항:**
    *   WP(World Partition) 생성 로그 보고서에 `ActorDescViewMutators` 결과가 포함되지 않는 문제 (`UE - World Creation`)
    *   `GeneSplicerModule`의 개발 빌드 링크 에러 문제 (`MetaHuman`)
    *   UE 5.6부터 에디터 환경설정에서 `Preview Game Language`의 "None" 옵션이 제거된 문제 (`UE - Editor - UI Systems`)

**Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

공식 GitHub 저장소 `EpicGames/UnrealEngine`의 최근 7일 이내 주요 커밋 및 Pull Request 정보는 검색 결과에서 직접적인 상세 내용을 확인하지 못했습니다.

**참고 사항:**
*   UE 5.7 Preview는 GitHub를 통해 다운로드 가능합니다. (릴리즈 노트: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958))
*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**Epic Staff 답변 기술 스레드**
최근 7일 이내 Epic Staff가 직접 답변한 기술 스레드는 명확하게 확인되지 않았습니다.

**주요 논의 스레드 (최근 7일 이내)**
*   **UE 5.6.1 Android 빌드 문제:** EOS SDK 관련 로그 루프 및 셰이더 컴파일러 통계 루프 문제에 대한 논의가 활발히 진행되었습니다. (2025-10-27)
    *   **포럼 URL:** [https://forums.unrealengine.com/t/ue5-6-1-hangs-up-when-building-for-android/2669105](https://forums.unrealengine.com/t/ue5-6-1-hangs-up-when-building-for-android/2669105)
*   **오브젝트 상호작용 프로젝트 도움 요청:** Game Instance에 저장된 변수와 레이캐스트를 사용한 오브젝트 상호작용 시스템 구현에 대한 논의가 있었습니다. (2025-10-27)
    *   **포럼 URL:** [https://forums.unrealengine.com/t/hi-could-someone-help-me-with-a-project-that-involves-interaction-between-objects/2668988](https://forums.unrealengine.com/t/hi-could-someone-help-me-with-a-project-that-involves-interaction-between-objects/2668988)

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.7 Preview 기준)**
*   **PCG Production-Ready:** GPU 성능 최적화 및 GPU 파라미터 오버라이드 기능 추가.
*   **MetaHuman Creator Plugin for Linux and macOS:** Linux 및 macOS 환경에서 MetaHuman Creator 플러그인 사용 가능.
*   **MetaHuman Creator Python and Blueprint API:** Python 또는 블루프린트를 사용하여 MetaHuman 캐릭터 에셋의 편집 및 조립 작업을 스크립팅할 수 있는 API 추가.
*   **애니메이션 Selection Sets:** 리그 내 여러 컨트롤에 빠르게 접근하여 애니메이션 워크플로우를 간소화하는 기능.

**Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview 기준)**

| 기능 | 상태 | 주요 내용 | 주의사항 |
| :--- | :--- | :--- | :--- |
| **Procedural Vegetation Editor** | Experimental | Fab 에셋을 시작점으로 Nanite 지원 폴리지(Foliage)를 생성, 커스터마이징하는 플러그인. PCG 기반 노드 그래프 사용. | Experimental 기능이므로 프로덕션 사용에 주의 필요. |
| **Nanite Foliage** | Experimental | Nanite Assemblies, Nanite Skinning, Nanite Voxel을 기반으로 고밀도, 고디테일 폴리지를 60fps로 렌더링하는 렌더링 경로. | Experimental 기능이므로 프로덕션 사용에 주의 필요. |
| **MegaLights** | Beta | 방향성 광원, Niagara 파티클 광원, 투명도 조명, 헤어 그룸 지원. 성능 튜닝 컨트롤 추가. | Beta 기능이므로 안정성 및 성능 테스트 필요. |
| **Epic Developer Assistant** | UI만 Preview에 포함 | 인스턴트 답변, 가이드, C++ 코드 생성을 에디터 내에서 제공하는 AI 도우미. | **5.7.0 정식 릴리즈 시점에 출시 예정이며, Preview 버전에는 기능이 포함되지 않습니다.** |

**성능 영향도**
*   **PCG:** GPU 생성 및 게임 스레드 성능이 UE 5.5 대비 약 **두 배** 빨라졌습니다.
*   **Nanite Foliage:** 현재 세대 하드웨어에서 고밀도 폴리지를 **60 fps**로 부드럽게 렌더링하도록 설계되었습니다.

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트 (UE 5.7 Preview 기준)**
*   **Procedural Vegetation Editor:** 새로운 Experimental 플러그인.
*   **MetaHuman Creator Plugin:** Linux 및 macOS 지원 추가.

**문서 주요 변경사항**
*   **Substrate:** 정식 출시 준비 완료(Production-Ready) 상태로 문서 업데이트가 예상됩니다.
*   **PCG:** Production-Ready 전환에 따른 문서 업데이트 및 상세 가이드 추가가 예상됩니다.
*   **5.7 Public Roadmap:** 공개 로드맵을 통해 향후 업데이트 계획을 확인할 수 있습니다.
    *   **로드맵 URL:** (릴리즈 노트 내 링크 참조 필요)

---
**출처 목록**
*   [Unreal Engine 5.7 Preview - Epic Developer Community Forums](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)
*   [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)
*   [UE5.6.1 hangs up when building for Android - Epic Developer Community Forums](https://forums.unrealengine.com/t/ue5-6-1-hangs-up-when-building-for-android/2669105)
*   [Hi! Could someone help me with a project that involves interaction between objects? - Epic Developer Community Forums](https://forums.unrealengine.com/t/hi-could-someone-help-me-with-a-project-that-involves-interaction-between-objects/2668988)
