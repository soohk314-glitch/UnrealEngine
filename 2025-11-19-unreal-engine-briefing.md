# 언리얼 엔진 데일리 브리핑 | 2025년 11월 19일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Nanite Foliage and Skinning (Experimental):** 대규모 애니메이션 식물 렌더링을 위한 Nanite Assemblies, Skinning, Voxels 통합. <br> 2. **Substrate (Production Ready):** 모듈식 물리 기반 재질 프레임워크 정식 출시 및 기본 활성화. <br> 3. **PCG Framework (Production Ready):** 절차적 콘텐츠 생성 프레임워크 정식 출시 및 PCG Editor Mode 추가. |
| **즉시 확인 필요 사항** | Unreal Engine 5.7 버전에서 **MSVC 컴파일러가 14.44로 업데이트**되었습니다. C++ 프로젝트의 빌드 환경 및 호환성 확인이 필요합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (게시일: 2025-11-11경) |

## 2. 공식 릴리즈 및 패치

**버전 릴리즈:** Unreal Engine 5.7 (최신 메이저 버전)

**주요 변경사항 및 Breaking Changes:**
Unreal Engine 5.7은 렌더링, 캐릭터/애니메이션, 월드 빌딩, PCG 등 광범위한 영역에서 개선 사항을 제공합니다.

*   **렌더링:** **MegaLights** 및 **Niagara Heterogeneous Volumes**가 베타(Beta)로 전환되었으며, 모바일 및 데스크톱 렌더러에서 **SMAA** (Subpixel Morphological Anti-Aliasing)가 실험적(Experimental) 기능으로 추가되었습니다.
*   **애니메이션:** **Motion Matching Chooser Integration**, **Spatially Aware Retargeting**, **Sequence Validator**가 실험적 기능으로 추가되어 애니메이션 워크플로우를 개선합니다.
*   **빌드 시스템 변경:** 기본 Microsoft Visual C++ 컴파일러가 **MSVC 14.44**로 업데이트되었습니다.

**릴리즈 노트 URL:**
[https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

| 구분 | 이슈 제목 | 영향받는 시스템 | 보고일 |
| :--- | :--- | :--- | :--- |
| **새로 보고된 주요 버그** | FInstancedStruct member uproperties are not cached when "Generate Optimized Blueprint Component Data" is enabled | Framework - Blueprint | 2025-11-18 |
| | [AI] SmartObjectPersistentCollection produces errors during Map Validation | AI - SmartObject | 2025-11-18 |
| **수정된 버그** | Groom assets can no longer be created without curves data | Graphics Features | 2025-11-18 |
| | DataAsset blueprints have the wrong NativeClass | Gameplay | 2025-11-18 |
| **Workaround** | **LWCLength precision issues:** Large World Coordinates (LWC)의 정밀도 문제로 인한 아티팩트는 **Won't Fix**로 처리되었으며, LWC 사용 시 월드 원점에서 멀리 떨어진 곳에서의 정밀도 이슈를 인지하고 있어야 합니다. |
| **Issue Tracker URL** | [https://issues.unrealengine.com/issue/search](https://issues.unrealengine.com/issue/search) |

## 4. GitHub 업데이트

금일(2025년 11월 19일) EpicGames/UnrealEngine 저장소의 주요 커밋 및 Pull Request에 대한 특정 기술 정보는 검색되지 않았습니다.

*   **주요 커밋 및 Pull Request:** 최근 7일간의 주요 커밋 내역은 일반 검색으로 확인되지 않았습니다.
*   **영향받는 시스템:** 정보 없음.
*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

최근 7일간 Epic Staff가 답변한 특정 기술 스레드는 검색되지 않았습니다.

*   **Epic Staff 답변 기술 스레드:** 최근 업데이트 사항 없음.
*   **포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

| 기능 구분 | 기능명 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **Production Ready** | **Substrate** | 모듈식 물리 기반 재질 시스템. | 장기적으로 유연성과 확장성 제공. |
| | **PCG Framework** | 절차적 콘텐츠 생성 프레임워크. | 안정적인 환경에서 빠른 반복 작업 가능. |
| **Beta** | **MegaLights** | 노이즈 감소 및 전반적인 성능 개선. | 개선된 성능 제공. |
| | **Niagara Heterogeneous Volumes** | 그림자 캐스팅 개선 (Beer Shadow Map 지원). | 그림자 생성 시간 대폭 개선. |
| | **Audio Insights** | 오디오 프로파일링 및 디버깅 도구. | - |
| **Experimental** | **Nanite Foliage and Skinning** | Nanite를 활용한 고성능 식물 렌더링. | 현세대 하드웨어에서 60fps 예산 내에서 구현 가능. |
| | **SMAA** | 모바일 및 데스크톱 렌더러에서 지원. | 최소한의 성능 영향으로 고품질 에지 스무딩 제공. |
| | **Motion Matching Chooser Integration** | 모션 매칭에 대한 에셋 선택 제어 기능 추가. | - |
| | **Spatially Aware Retargeting** | 리타겟팅 시 자체 충돌 방지 기능. | - |
| | **Sequence Validator** | 시네마틱 시퀀스의 콘텐츠 오류 검사. | - |
| | **Procedural Vegetation Editor** | PCG 기반의 식물 메시 생성 및 편집 도구. | - |

## 7. 플러그인 및 문서 업데이트

*   **공식 플러그인 업데이트:**
    *   **Motion Design** 플러그인이 **Production Ready** 상태로 전환되었습니다. Text3D의 Rich Text 지원, Transition Logic 안정화 등 개선.
    *   **MetaHuman Creator**가 Linux 및 macOS를 지원하며, Python/Blueprint를 통한 자동화 API가 추가되었습니다.
*   **문서 주요 변경사항:**
    *   MetaHuman for Houdini 및 MetaHuman for Maya가 업데이트되었으며, Linux 지원이 추가되었습니다.
    *   **Custom HLODs** 기능이 추가되어 사용자 정의 HLOD 표현을 제공할 수 있게 되었습니다.
