# 언리얼 엔진 데일리 브리핑 | 2025년 11월 25일

## 1. 핵심 요약

- 주요 업데이트 상위 3개
    - **Substrate Materials 정식 출시(GA):** 모듈형 물리 기반 머티리얼 프레임워크인 Substrate Materials가 UE 5.7에서 정식 버전으로 전환되어 기본 활성화되었습니다.
    - **MegaLights 베타 전환:** 노이즈 감소 및 전반적인 퍼포먼스가 향상된 MegaLights가 베타 버전으로 전환되었습니다.
    - **Nanite Foliage & Skinning (실험 단계):** 폴리지 에셋의 크기를 최소화하고 동적인 움직임을 지원하는 새로운 렌더링 경로가 실험 단계로 도입되었습니다.
- 즉시 확인 필요 사항
    - **Substrate Materials**가 기본 활성화되었으므로, 기존 프로젝트의 머티리얼 시스템과의 호환성 및 성능 변화를 확인해야 합니다.
    - **스크립터블 툴 프레임워크(ScriptableToolsFramework)** 플러그인 활성화 시 배포(shipping) 환경에서 컴파일 오류가 발생하는 버그가 보고되었습니다.
- 출처 URL 및 게시일 (YYYY-MM-DD)
    - Unreal Engine 5.7 Release Notes: [https://dev.epicgames.com/documentation/ko-kr/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/ko-kr/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12)
    - Unreal Engine Issues: [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (최신 업데이트 기준)

## 2. 공식 릴리즈 및 패치

- 버전 릴리즈 (정확한 버전 번호)
    - **Unreal Engine 5.7** (2025년 11월 12일 출시)
- 주요 변경사항 및 Breaking Changes
    - **Substrate Materials**가 정식 버전으로 전환되어 기본 활성화되었습니다.
    - **MegaLights** 및 **Niagara Heterogeneous Volumes**가 베타 버전으로 전환되었습니다.
    - **컨트롤 릭 피직스**에 레벨 콜리전 지원이 추가되었습니다.
    - **메타휴먼 크리에이터**가 Linux 및 macOS를 지원하며, Python/블루프린트를 사용한 편집 및 어셈블리 자동화 API가 추가되었습니다.
- 릴리즈 노트 URL
    - [https://dev.epicgames.com/documentation/ko-kr/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/ko-kr/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- 새로 보고된 주요 버그
    - **Dataless Mutable:** Skeletal Mesh Parameter 노드와 함께 Cloth Simulation이 작동하지 않는 문제. (UE-Anim-Mutable)
    - **ScriptableToolsFramework:** 플러그인 활성화 시 배포(shipping) 환경에서 컴파일 오류 발생. (UE-Graphics Tools-Modeling Tools)
    - **Landscape:** Nanite Landscape에서 Landscape Visualizer가 작동하지 않는 문제. (UE-Graphics Tools-Terrain)
- 수정된 버그
    - **Enhanced Input:** 자식 위젯이 부모의 Enhanced Input 바인딩을 유지하지 못하는 문제.
    - **Blueprint:** "Generate Optimized Blueprint Component Data" 활성화 시 FInstancedStruct 멤버 프로퍼티가 캐시되지 않는 문제.
- Workaround
    - ScriptableToolsFramework 관련 컴파일 오류에 대한 공식적인 Workaround는 아직 보고되지 않았습니다.
- Issue Tracker URL
    - [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- 주요 커밋 및 Pull Request
    - 최근 7일간 EpicGames/UnrealEngine 저장소의 `main` 브랜치에 대한 **주요 기술 커밋은 확인되지 않았습니다.** (마지막 주요 업데이트는 5.7 릴리즈 관련)
- 영향받는 시스템
    - 해당 사항 없음
- GitHub URL
    - [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- Epic Staff 답변 기술 스레드
    - 최근 7일간 Epic Staff가 답변한 **주요 기술 스레드는 확인되지 않았습니다.**
- 포럼 URL
    - [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- 새로 추가된 기능
    - **Substrate Materials** 정식 출시 (GA)
    - **컨트롤 릭 피직스**에 월드 콜리전 지원
    - **메타휴먼 크리에이터** Linux/macOS 지원 및 자동화 API
- Beta/Experimental 기능 및 주의사항
    - **MegaLights (베타):** 노이즈 감소 및 퍼포먼스 향상. 디렉셔널 라이트, 나이아가라 파티클 라이트, 반투명, 헤어 스트랜드 지원 추가.
    - **Niagara Heterogeneous Volumes (베타):** 섀도 캐스팅 기능 향상.
    - **Nanite Foliage & Skinning (실험 단계):** 폴리지 에셋 최적화 및 동적 애니메이션을 위한 새로운 렌더링 경로.
    - **SMAA (실험 단계):** 모바일 및 데스크톱 렌더러에서 지원. `r.Mobile.AntiAliasing=5` 또는 `r.AntiAliasingMethod=5`로 활성화.
    - **모션 매칭 추저 통합 (실험 단계):** 모션 매칭과 추저 통합을 통한 에셋별 필터링 및 제어.
    - **데이터리스 뮤터블 (실험 단계):** 런타임 파라미터 처리를 통한 컴파일 속도 향상 및 패키지 크기 감소.
- 성능 영향도
    - **MegaLights** 및 **Niagara Heterogeneous Volumes**는 베타 전환과 함께 퍼포먼스가 향상되었다고 언급되었습니다.
    - **SMAA**는 퍼포먼스에 대한 영향을 최소화하면서 고퀄리티의 에지 스무딩을 제공한다고 언급되었습니다.

## 7. 플러그인 및 문서 업데이트

- 공식 플러그인 업데이트
    - **메타휴먼 애니메이터 캘리브레이션 다이애그노스틱 플러그인** (실험 단계) 추가.
- 문서 주요 변경사항
    - Unreal Engine 5.7 문서 업데이트.
    - **언리얼 엔진 5 마이그레이션 가이드** 업데이트.
    - **Unreal Engine Web API Documentation** 등 API 레퍼런스 업데이트.
