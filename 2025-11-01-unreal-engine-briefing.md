# 언리얼 엔진 데일리 브리핑 | 2025년 11월 01일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **UE 5.7 Preview** 발표: Nanite Foliage, MegaLights(Beta), Substrate(Production-Ready) 등 대규모 신기능 공개. |
| | 2. **UE 5.6.1** 패치: NDI Media Plugin 업데이트 및 Multi-User Editing 지원 강화. |
| | 3. **이슈 트래커** 최신 버그: Virtual Texture Collection Indexing, Static Mesh Contact Shadows 버그 보고. |
| **즉시 확인 필요 사항** | **UE 5.7 Preview**의 **Substrate**가 프로덕션 레디로 전환되었으며, 신규 프로젝트에서 기본으로 활성화됩니다. 기존 프로젝트의 마이그레이션 및 성능 영향을 확인해야 합니다. |
| **출처 URL 및 게시일** | - Unreal Fest Stockholm 하이라이트: [https://www.unrealengine.com/en-US/news/highlights-from-the-unreal-fest-stockholm-opening-session](https://www.unrealengine.com/en-US/news/highlights-from-the-unreal-fest-stockholm-opening-session) (2025-10-02) |
| | - Unreal Engine Issues: [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (2025-11-01) |
| | - UE 5.6.1 업데이트 참고: [https://aximmetry.com/learn/virtual-production-workflow/which-aximmetry-is-right-for-you/software-version-history/](https://aximmetry.com/learn/virtual-production-workflow/which-aximmetry-is-right-for-you/software-version-history/) (2025-10-17) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.6.1** (최신 패치 버전)
- **주요 변경사항 및 Breaking Changes:**
    - **NDI Media Plugin** 업데이트 (v1.0): 블루프린트를 사용한 소스 변경 기능 등 개선.
    - **Multi-User Editing** 지원 강화: Editor Data 모드에서 Multi-User Editing이 완전히 지원됩니다.
    - **UE 5.7 Preview**가 Epic Games Launcher를 통해 다운로드 가능합니다.
- **릴리즈 노트 URL:** 공식 5.6.1 릴리즈 노트는 아직 공식 블로그에서 확인되지 않았으나, 주요 변경사항은 파트너사 업데이트 및 포럼을 통해 확인되었습니다.
    - (참고) Aximmetry DE 업데이트 내역: [https://aximmetry.com/learn/virtual-production-workflow/which-aximmetry-is-right-for-you/software-version-history/](https://aximmetry.com/learn/virtual-production-workflow/which-aximmetry-is-right-for-you/software-version-history/)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (Latest Bugs):**
    - **Virtual Texture Collection Indexing Not Working:** Virtual Texture Collection에서 인덱스 0이 아닌 텍스처를 샘플링할 수 없는 문제 (UE - Rendering Architecture - RHI).
    - **Static Mesh Contact Shadows still render when all LOD sections have Cast Shadows disabled:** 모든 LOD 섹션에서 그림자 캐스트를 비활성화해도 스태틱 메시의 Contact Shadows가 계속 렌더링되는 문제 (UE - Graphics Features).
    - **Path Tracer Normals Issue:** Path Tracing 노멀 맵이 Lit 모드와 다르게 빛을 반사하여 정확하지 않은 문제 (UE - Graphics Features).
- **수정된 버그 (Latest Fixes):**
    - **NiagaraDataInterfaceChaosDestruction:** NiagaraDataInterfaceChaosDestruction에 의해 스폰된 일부 인스턴스가 월드 원점으로 위치가 설정되는 문제 수정.
    - **Video length indicator no longer works:** 비디오 길이 표시기가 작동하지 않는 문제 수정 (TM - Tools).
    - **GeneSplicerModule has linking errors in a Development target:** `FArchiveMemoryStream` 클래스 정의 충돌로 인한 링커 오류 수정 (MetaHuman).
- **Workaround:** 현재 확인된 공식 Workaround는 없습니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:** 최근 7일간 EpicGames/UnrealEngine GitHub 저장소의 주요 기술 커밋에 대한 직접적인 정보는 검색되지 않았습니다.
- **영향받는 시스템:** "최근 7일간 새로운 업데이트 사항이 없습니다."
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:** Epic Staff의 직접적인 답변이 포함된 최신 기술 스레드는 검색되지 않았습니다.
- **포럼 URL:** [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 Preview):**
    - **Substrate (Production-Ready):** 5.7에서 프로덕션 레디로 전환되었으며, 신규 프로젝트에서 기본으로 활성화됩니다. 레거시 머티리얼의 모든 기능을 지원하며, 복잡한 레이어드 토폴로지를 가진 머티리얼과 같은 새로운 기능을 제공합니다.
    - **Procedural Content Generation (PCG) (Production-Ready):** 5.7에서 프로덕션 레디로 전환되었으며, GPU 생성 및 게임 스레드 성능이 최적화되어 5.5 대비 약 2배 빨라졌습니다. 새로운 에디터 모드를 통해 사용 편의성이 향상되었습니다.
- **Beta/Experimental 기능 및 주의사항 (UE 5.7 Preview):**
    - **Nanite Foliage (Experimental):** 고밀도, 고디테일의 폴리지(Foliage)를 렌더링하고 애니메이션할 수 있습니다. Nanite Assemblies를 통해 에셋 변형을 효율적으로 관리하고, Nanite Voxel 렌더링을 통해 원거리 나무의 크로스 페이드 및 팝 현상을 제거합니다.
    - **Procedural Vegetation Editor (Experimental):** 새로운 Quixel 에셋인 Megaplants와 함께 제공됩니다.
    - **MegaLights (Beta):** 조명 품질과 안정성이 향상되었습니다. 디렉셔널 라이트, 헤어 그룸, 반투명 조명, Niagara 파티클 라이트를 지원합니다. 성능 튜닝 컨트롤을 통해 해상도 스케일 및 업데이트 속도를 관리할 수 있습니다.
- **성능 영향도:** PCG 프레임워크는 5.5 대비 약 2배의 속도 향상이 보고되었습니다. Nanite Foliage는 렌더링 비용을 절감하여 성능 향상을 목표로 합니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **NDI Media Plugin** (v1.0)이 UE 5.6.1에 통합되어 블루프린트 기반 소스 변경 등 기능이 개선되었습니다.
- **문서 주요 변경사항:**
    - **Chaos Destruction Optimization** 문서가 UE 5.6에 맞춰 업데이트되었습니다. (2025-10-09)
    - **UGraph** 관련 문서가 UE 5.6에 맞춰 업데이트되었습니다. (2025-10-03)
    - **출처:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/chaos-destruction-optimization](https://dev.epicgames.com/documentation/en-us/unreal-engine/chaos-destruction-optimization)
    - **출처:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/API/Plugins/GameplayGraph/UGraph](https://dev.epicgames.com/documentation/en-us/unreal-engine/API/Plugins/GameplayGraph/UGraph)
