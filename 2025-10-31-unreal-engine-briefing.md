# 언리얼 엔진 데일리 브리핑 | 2025년 10월 31일

## 1. 핵심 요약

| 항목 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | **1. Lumen 하드웨어 레이 트레이싱 최적화:** UE 5.6에서 HWRT 성능이 크게 향상되어 소프트웨어 레이 트레이싱 모드와 유사한 프레임 예산을 달성하며 CPU 리소스를 절약합니다. (출처: [UE 5.6 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes))<br>**2. RHI - 렌더러 병렬화:** 렌더 스레드 성능을 개선하기 위해 RHI API를 리팩터링하여 멀티스레딩 기능을 최대한 활용합니다. (출처: [UE 5.6 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes))<br>**3. Substrate Materials (베타):** UE 5.6에서 베타로 제공되며, 기존 셰이딩 모델을 대체하는 보다 표현력이 풍부하고 모듈화된 프레임워크입니다. 성능 동등성 개선 작업이 진행 중입니다. (출처: [UE 5.6 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes)) |
| **즉시 확인 필요 사항** | **UE 5.6.1 핫픽스:** 2025년 8월 12일에 릴리즈된 5.6.1 핫픽스는 MetaHumans, PCG, 모션 디자인 툴 등을 포함하여 270개 이상의 수정 사항을 포함하고 있습니다. 5.6 사용자라면 안정성 향상을 위해 적용을 고려해야 합니다. (출처: [5.6.1 Just Released - Forums](https://forums.unrealengine.com/t/5-6-1-just-released-where-do-we-see-what-it-changed/2639140), [80.lv](https://80.lv/articles/unreal-engine-5-6-gets-first-hotfix-update)) |
| **출처 URL 및 게시일** | - **UE 5.6 Release Notes:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes) (게시일 미상, 5.6 릴리즈는 2025년 6월 3일)<br>- **UE 5.6.1 Hotfix:** [https://forums.unrealengine.com/t/5-6-1-just-released-where-do-we-see-what-it-changed/2639140](https://forums.unrealengine.com/t/5-6-1-just-released-where-do-we-see-what-it-changed/2639140) (2025-08-12) |

## 2. 공식 릴리즈 및 패치

**최신 공식 릴리즈:** 언리얼 엔진 **5.6** (2025년 6월 3일 릴리즈)

**최신 핫픽스:** 언리얼 엔진 **5.6.1** (2025년 8월 12일 릴리즈, 270개 이상의 수정 사항 포함)

**주요 변경사항 및 Breaking Changes (UE 5.6 기준):**

*   **렌더링:** Lumen HWRT 최적화, RHI 렌더러 병렬화, RHI 바인드리스 리소스 지원 추가.
*   **월드 빌딩:** Fast Geometry Streaming 플러그인 (실험단계) 추가.
*   **애니메이션:** First Person Rendering (베타), GPU Profiler 2.0 도입.

**릴리즈 노트 URL:**
*   UE 5.6 Release Notes: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes)
*   UE 5.6.1 Hotfix 포럼 공지: [https://forums.unrealengine.com/t/5-6-1-just-released-where-do-we-see-what-it-changed/2639140](https://forums.unrealengine.com/t/5-6-1-just-released-where-do-we-see-what-it-changed/2639140)

## 3. 버그 및 이슈

**최근 7일간의 주요 버그 및 수정 사항 (Issue Tracker 기준, 2025년 10월 31일 확인)**

| 구분 | 이슈 ID | 설명 | 영향받는 시스템 |
| :--- | :--- | :--- | :--- |
| **새로 보고된 주요 버그** | Virtual Texture Collection Indexing Not Working | 0이 아닌 인덱스의 텍스처를 버추얼 텍스처 컬렉션에서 샘플링할 수 없음. | Graphics Features |
| | Static Mesh Contact Shadows still render when all LOD sections have Cast Shadows dissabled | 모든 LOD 섹션에서 그림자 캐스팅을 비활성화해도 스태틱 메시 접촉 그림자가 계속 렌더링됨. | Graphics Features |
| **수정된 버그** | “None” option removed from “Preview Game Language” in Editor Preferences since UE 5.6 | UE 5.6부터 에디터 환경설정에서 'Preview Game Language'의 "None" 옵션이 제거됨. (수정됨) | Editor - UI Systems |
| | GeneSplicerModule has linking errors in a Development target | `GeneSplicerModule`과 `RigLogicModule`에 `FArchiveMemoryStream` 클래스가 중복 정의되어 개발 빌드에서 링커 오류 발생. (수정됨) | MetaHuman |
| **Workaround** | **Workaround 정보 없음** | Issue Tracker에 명시적인 Workaround 정보는 제공되지 않았습니다. | N/A |

**Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

**최근 7일간 새로운 업데이트 사항이 없습니다.**

**가장 최근의 주요 커밋 및 Pull Request (검색 결과 기준):**

*   **주요 커밋:** TTuple 관련 이슈 디버깅 중 발견된 Workaround 커밋 ([https://github.com/EpicGames/UnrealEngine/commit/...](https://developercommunity.visualstudio.com/VisualStudio?q=unreal&sort=newest) 스니펫에서 언급).
*   **영향받는 시스템:** TTuple을 사용하는 C++ 코드베이스.

**GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

**최근 7일간 Epic Staff 답변이 포함된 새로운 기술 스레드 정보는 검색되지 않았습니다.**

**가장 최근의 기술 논의 동향 (검색 결과 기준):**

*   **UE 5.7 프리뷰:** **MegaLights**가 방향성 광원 지원과 함께 베타로 전환되고, **Procedural Vegetation Editor**, **Rig Mapper for MetaHumans** 등의 새로운 툴과 개선 사항이 논의되고 있습니다. (출처: [Unreal Engine 5.7 Preview - Forums](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958), 2025년 9월 23일)

**포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

**새로 추가된 기능 (UE 5.6 기준):**

*   **Depth of Field - Petzval Bokeh:** 실시간 및 패스 트레이서 렌더링 모두에서 지원되는 새로운 Petzval Bokeh 설정이 추가되었습니다.

**Beta/Experimental 기능 및 주의사항 (UE 5.6 기준):**

| 기능 | 상태 | 주요 내용 | 성능 영향도 |
| :--- | :--- | :--- | :--- |
| **Substrate Materials** | 베타 (Beta) | 기존 셰이딩 모델을 대체하는 모듈형 프레임워크. | 성능 동등성 개선 작업 진행 중. |
| **First Person Rendering** | 베타 (Beta) | 플레이어 손/무기가 월드 오브젝트에 클리핑되는 것을 방지하고, 별도의 FOV를 제공. VSM, 레이 트레이싱 등 통합. | 명시적인 성능 영향 정보는 릴리즈 노트에 없음. |
| **Fast Geometry Streaming Plugin** | 실험단계 (Experimental) | 월드 빌딩을 위한 빠른 지오메트리 스트리밍 플러그인. | 명시적인 성능 영향 정보는 릴리즈 노트에 없음. |

## 7. 플러그인 및 문서 업데이트

**공식 플러그인 업데이트:**

*   **MetaHuman:** `GeneSplicerModule`의 링커 오류가 수정되었습니다. (UE 5.6.1 핫픽스에 포함된 것으로 추정)
*   **Niagara Heterogeneous Volumes:** 다운샘플링 및 런타임 성능 최적화가 이루어졌습니다.

**문서 주요 변경사항:**

*   **UE 5.6 문서:** Lumen HWRT 최적화, RHI 병렬화/바인드리스 리소스, VSM 최적화, Substrate Materials (베타), First Person Rendering (베타) 등 광범위한 영역에 대한 문서 업데이트가 이루어졌습니다.

**문서 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine](https://dev.epicgames.com/documentation/en-us/unreal-engine)
