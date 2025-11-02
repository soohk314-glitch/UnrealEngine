# 언리얼 엔진 데일리 브리핑 | 2025년 11월 02일

**작성일시:** 2025년 11월 02일 20시 36분 58초 KST

## 1. 핵심 요약

최신 공식 릴리즈는 **언리얼 엔진 5.6**이며, 2025년 6월 3일에 출시되었습니다. 최근 7일간의 공식 릴리즈 및 패치 업데이트는 확인되지 않았습니다. 주요 업데이트는 주로 렌더링 성능 최적화와 새로운 기능의 베타 전환에 집중되어 있습니다.

| 구분 | 내용 | 출처 URL 및 게시일 |
| :--- | :--- | :--- |
| **주요 업데이트 상위 3개** | **Lumen Hardware Ray Tracing Optimizations**: HWRT 모드 성능 향상으로 60hz 일관된 프레임 속도 달성 기여. | [UE 5.6 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes) (2025-06-03) |
| | **RHI - Renderer Parallelization**: 렌더 스레드 작업 병렬화로 성능 개선. | [UE 5.6 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes) (2025-06-03) |
| | **First Person Rendering (Beta)**: 1인칭 렌더링 방식이 베타로 전환, 클리핑 방지 및 별도 FOV 설정 가능. | [UE 5.6 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes) (2025-06-03) |
| **즉시 확인 필요 사항** | **Virtual Texture Collection Indexing Not Working** 버그가 최신 버그로 보고됨. Virtual Texture Collection을 사용하는 프로젝트는 인덱스 0이 아닌 텍스처 샘플링 문제를 확인해야 합니다. | [Unreal Engine Issues](https://issues.unrealengine.com/) (2025-11-01 기준) |

## 2. 공식 릴리즈 및 패치

최근 7일간 새로운 공식 릴리즈 또는 패치 업데이트 사항은 없습니다. 가장 최신 주요 릴리즈는 **Unreal Engine 5.6**입니다.

- **버전 릴리즈:** Unreal Engine 5.6
- **주요 변경사항:**
    - **렌더링:** Lumen HWRT 최적화, RHI 병렬화 및 바인드리스 리소스 지원, Niagara Heterogeneous Volumes 최적화, Virtual Shadow Maps 최적화, Petzval Bokeh Depth of Field, GPU Profiler 2.0 도입.
    - **월드 빌딩:** Fast Geometry Streaming Plugin (Experimental) 추가.
- **Breaking Changes:** 릴리즈 노트에서 명시적인 Breaking Changes는 확인되지 않았습니다.
- **릴리즈 노트 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-6-release-notes)

## 3. 버그 및 이슈

최신 정보는 언리얼 엔진 이슈 트래커(Issue Tracker)를 기준으로 합니다.

- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)
- **새로 보고된 주요 버그 (Latest Bugs):**
    - **Virtual Texture Collection Indexing Not Working (UE-Rendering Architecture - RHI):** Virtual Texture Collection에서 인덱스 0이 아닌 텍스처를 샘플링할 수 없는 문제.
    - **Static Mesh Contact Shadows still render when all LOD sections have Cast Shadows dissabled (UE-Graphics Features):** 모든 LOD 섹션에서 그림자 캐스트를 비활성화해도 스태틱 메시 접촉 그림자가 계속 렌더링되는 문제.
    - **Path Tracer Normals Issue (UE-Graphics Features):** 패스 트레이서 노멀 맵이 Lit 모드와 다르게 빛을 반사하며 정확하지 않은 문제.
- **수정된 버그 (Latest Fixes):**
    - **Some instances spawned by NeagaraDataInterfaceChaosDestruction breaking event will be set location to the world origin (UE-Niagara - Data Interface):** NiagaraDataInterfaceChaosDestruction 파괴 이벤트로 생성된 일부 인스턴스가 월드 원점으로 위치가 설정되는 문제 수정.
    - **“None” option removed from “Preview Game Language” in Editor Preferences since UE 5.6 (UE-Editor - UI Systems):** UE 5.6부터 에디터 환경설정에서 "Preview Game Language"의 "None" 옵션이 제거된 문제 수정.
- **Workaround:** 별도로 명시된 Workaround는 확인되지 않았습니다.

## 4. GitHub 업데이트

최근 7일간 EpicGames/UnrealEngine 공식 저장소의 주요 커밋 및 Pull Request 정보는 웹 검색을 통해 직접적으로 확인되지 않았습니다.

- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)
- **주요 커밋 및 Pull Request:** 최근 7일간의 공식 저장소 커밋 정보는 수집되지 않았습니다.
- **영향받는 시스템:** 정보 없음.

## 5. 공식 포럼 기술 논의

Epic Staff가 직접 답변한 최신 기술 스레드는 확인되지 않았습니다.

- **포럼 URL:** [https://forums.unrealengine.com/c/development-discussion/pipeline-plugins/147](https://forums.unrealengine.com/c/development-discussion/pipeline-plugins/147)
- **주요 논의 주제:**
    - **Twinmotion to Unreal Importer**
    - **Feature request: One file per actor, include actor name in external actor file name**
    - **Where is pxr header file in Unreal Engine 5.5 source code**

## 6. 신기능 및 실험적 기능

Unreal Engine 5.6 릴리즈를 기준으로 가장 최신 정보를 제공합니다.

- **새로 추가된 기능:**
    - **GPU Profiler 2.0:** 기존 프로파일링 시스템을 통합하고 GPU 타임라인의 정확도와 일관성을 높인 재설계된 Insights GPU 프로파일러.
    - **Depth of Field - Petzval Bokeh:** 새로운 Petzval Bokeh 설정이 실시간 및 패스 트레이서 렌더링에 모두 지원됩니다.
- **Beta/Experimental 기능 및 주의사항:**
    - **Beta:** **Substrate Materials**, **First Person Rendering**.
    - **Experimental:** **Fast Geometry Streaming Plugin**.
    - **주의사항:** 베타 및 실험적 기능은 아직 개발 중이며, 상용 프로젝트에 사용하기에는 적합하지 않을 수 있습니다.
- **성능 영향도:**
    - **성능 향상:** Lumen HWRT 최적화, RHI 병렬화, Niagara Heterogeneous Volumes 최적화 등은 전반적인 렌더링 성능 및 CPU 리소스 활용에 긍정적인 영향을 미칩니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:** Twinmotion to Unreal Importer 관련 포럼 논의가 활발합니다.
- **문서 주요 변경사항:** Unreal Engine 5.6 Documentation이 업데이트되었습니다.
    - **Unreal Engine 5.6 Release Notes**
    - **Unreal Engine 5 Migration Guide**
    - **Beta Features**
    - **Experimental Features**
