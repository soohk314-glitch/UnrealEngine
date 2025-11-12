# 언리얼 엔진 데일리 브리핑 | 2025년 11월 12일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7 공식 릴리즈** |
| | 2. **Nanite Foliage (실험적 기능)**: 대규모 환경에서 고밀도, 고화질의 식물을 효율적으로 렌더링하는 새로운 시스템 도입. |
| | 3. **Substrate (정식 기능)**: 물리적으로 정확한 다중 레이어 및 블렌딩 재질을 제작할 수 있는 모듈식 재질 프레임워크 정식 버전 전환. |
| **즉시 확인 필요 사항** | **Unreal Engine 5.7**의 **Breaking Changes** 및 **Nanite Foliage**와 **MegaLights**의 **Experimental/Beta** 상태 확인. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 is now available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈**: **Unreal Engine 5.7**
- **주요 변경사항 및 Breaking Changes**:
    - **PCG 프레임워크**가 **Production-Ready**로 전환되었습니다.
    - **Substrate** 재질 시스템이 **Production-Ready**로 전환되었습니다.
    - **MegaLights** 기능이 **Beta**로 전환되었습니다.
    - **Nanite Foliage** (Experimental) 기능이 추가되어 대규모 식물 렌더링 성능이 향상되었습니다.
    - **MetaHuman** 통합이 확장되어 Linux 및 macOS에서 MetaHuman Creator 플러그인을 지원하며, Python/Blueprint 스크립팅을 통한 에셋 편집 및 조립 자동화 기능이 추가되었습니다.
    - **애니메이션 툴셋**이 개선되어 Animation Mode 리팩토링, Selection Sets, 향상된 IK Retargeter, 스켈레탈 에디터 내 블렌드 쉐이프 스컬프팅 기능이 추가되었습니다.
    - **가상 프로덕션** 워크플로우가 확장되어 Dynamic Constraint Component for Props, Live Link Broadcast Component, 개선된 Composure 툴셋이 포함되었습니다.
    - 에디터 내에서 질문, C++ 코드 생성, 단계별 가이드를 제공하는 **AI Assistant**가 새로 도입되었습니다.
- **릴리즈 노트 URL**: [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (2025-11-12 기준)**:
    - `GetStaticRayTracingGeometries`가 레이 트레이싱이 비활성화된 메시를 확인하지 않아 ensure가 발생하는 문제 (UE-Unknown)
    - `CreatePatchLibrary`가 손상된 문제 (UE-Unknown)
- **수정된 버그 (2025-11-07 기준)**:
    - 월드 파티션 레벨에서 랜드스케이프 스플라인의 특정 배치가 Nanite 랜드스케이프 프록시를 무효화시키는 문제 (UE-Unknown)
- **Workaround**:
    - 현재까지 공식적으로 알려진 주요 Workaround는 없습니다.
- **Issue Tracker URL**: [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/issue/search)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**:
    - **Unreal Engine 5.7** 릴리즈에 따른 대규모 병합 및 커밋이 진행되었습니다.
    - 최근 7일간의 주요 커밋은 5.7 브랜치 안정화 및 버그 수정에 집중되었을 것으로 추정됩니다. (세부 커밋 내용은 GitHub에서 직접 확인 필요)
- **영향받는 시스템**: 엔진 전반
- **GitHub URL**: [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**:
    - **Unreal Engine 5.7 Released** 스레드에서 릴리즈 관련 논의가 활발하게 진행 중입니다. (예: Linux에서 Side Scroller 템플릿 프로젝트 생성 시 맵이 비어 보이는 Known Issue 언급)
- **포럼 URL**: [Epic Developer Community Forums - Announcements](https://forums.unrealengine.com/c/general/announcements/49)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능**:
    - **AI Assistant**: 에디터 내에서 질문, 코드 생성, 가이드 제공.
    - **PCG Editor Mode**: PCG 프레임워크 기반의 커스터마이징 가능한 툴 라이브러리 제공.
- **Beta/Experimental 기능 및 주의사항**:
    - **Experimental**: **Nanite Foliage** (Nanite Voxels, Nanite Assemblies, Nanite Skinning 사용).
    - **Beta**: **MegaLights** (더 많은 동적 그림자 캐스팅 라이트 지원).
    - **주의사항**: Experimental 또는 Beta 기능은 프로덕션 환경에 적합하지 않을 수 있으며, 향후 변경될 수 있습니다.
- **성능 영향도**:
    - **PCG GPU Compute** 성능이 크게 향상되었습니다.
    - **MegaLights**는 더 많은 동적 라이트를 효율적으로 처리하여 성능에 긍정적인 영향을 미칩니다.
    - **Nanite Foliage**는 고밀도 식물 환경에서 안정적인 프레임 속도를 제공하도록 설계되었습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**:
    - **MetaHuman Creator** 플러그인이 Linux 및 macOS를 지원합니다.
- **문서 주요 변경사항**:
    - **Unreal Engine 5.7 Release Notes** 문서가 업데이트되었습니다.
    - **PCG**, **Substrate**, **Nanite Foliage**, **MegaLights** 관련 문서가 대폭 추가 및 업데이트되었습니다.

---
*본 보고서는 2025년 11월 12일 KST를 기준으로 작성되었습니다.*
