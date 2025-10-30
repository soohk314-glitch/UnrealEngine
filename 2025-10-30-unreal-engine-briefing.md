# 언리얼 엔진 데일리 브리핑 | 2025년 10월 30일

## 1. 핵심 요약
- **주요 업데이트 상위 3개**
    1. **PCG (Procedural Content Generation Framework) 정식 버전(Production-Ready) 전환**: UE 5.7 Preview에서 PCG가 정식 기능으로 전환되었으며, GPU 성능 최적화 및 워크플로우 개선이 이루어졌습니다.
    2. **Nanite Foliage (실험적 기능) 도입**: 밀도 높고 디테일한 폴리지(Foliage)를 60fps로 부드럽게 렌더링할 수 있는 새로운 렌더링 경로가 실험적 기능으로 추가되었습니다.
    3. **Substrate 재질 시스템 정식 버전(Production-Ready) 전환**: 모듈식 셰이딩 시스템인 Substrate가 정식 기능으로 전환되어, 물리적으로 정확한 다중 재질 레이어 조합이 가능해졌습니다.
- **즉시 확인 필요 사항**
    - **Unreal Engine 5.7 Preview**가 릴리즈되었습니다. 프로덕션 프로젝트에 적용하기 전 테스트 환경에서 호환성 및 새로운 기능들을 검토해야 합니다.
    - **Epic Developer Assistant**는 5.7 Preview에는 포함되지 않으며, 5.7 정식 릴리즈 시점에 제공될 예정입니다.
- **출처 URL 및 게시일 (YYYY-MM-DD)**
    - Unreal Engine 5.7 Preview: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (2025-09-23)

## 2. 공식 릴리즈 및 패치
- **버전 릴리즈 (정확한 버전 번호)**
    - **Unreal Engine 5.7 Preview**
- **주요 변경사항 및 Breaking Changes**
    - **PCG**가 Production-Ready로 전환되었습니다. GPU 생성 및 게임 스레드 성능이 최적화되어 UE 5.5 대비 약 두 배 빨라졌습니다.
    - **Substrate** 재질 시스템이 Production-Ready로 전환되었습니다. 고정된 셰이딩 모델을 대체하며, Adaptive GBuffer와 Blendable GBuffer를 제공합니다.
    - **MegaLights**가 Beta 버전으로 전환되었으며, 디렉셔널 라이트, 나이아가라 파티클 라이트, 투명도 라이팅, 헤어 그룸을 지원합니다.
    - **MetaHuman Creator 플러그인**이 Linux 및 macOS에서도 사용 가능해졌으며, Python 및 Blueprint API가 추가되었습니다.
- **릴리즈 노트 URL**
    - [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (Preview 릴리즈 노트)

## 3. 버그 및 이슈
- **새로 보고된 주요 버그**
    - 5.7 Preview와 관련된 새로운 버그는 공식 포럼 스레드에 지속적으로 보고되고 있습니다. (별도 특정 버그 정보 미확인)
- **수정된 버그**
    - 5.7에서 수정된 이슈 목록은 별도의 링크를 통해 확인할 수 있습니다. (Preview 릴리즈 시점의 정보이므로, 최신 수정 사항은 GitHub 커밋을 통해 추가 확인 필요)
- **Workaround**
    - 해당 없음
- **Issue Tracker URL**
    - [https://issues.unrealengine.com/](https://issues.unrealengine.com/)
    - 5.7 Preview 관련 Known & Fixed Issues: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958) (게시물 하단 링크 참조)

## 4. GitHub 업데이트
- **주요 커밋 및 Pull Request**
    - 공식 포럼의 5.7 Preview 공지에서 GitHub를 통해 다운로드할 수 있음을 언급하고 있으나, 특정 주요 커밋 내용은 별도로 제공되지 않았습니다.
    - **MetaHuman Creator Python 및 Blueprint API** 관련 업데이트와 **Nanite Foliage** 관련 코드가 주요 커밋으로 예상되지만, 상세 내용은 GitHub 저장소 직접 분석이 필요합니다.
- **영향받는 시스템**
    - PCG, Nanite, Substrate, MetaHuman, Animation, Rigging
- **GitHub URL**
    - [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의
- **Epic Staff 답변 기술 스레드**
    - **Unreal Engine 5.7 Preview** 릴리즈 스레드에 Epic Staff의 답변과 커뮤니티의 활발한 논의가 진행 중입니다. (게시물 활동: 16시간 전)
    - **Epic Developer Assistant** 관련 논의도 진행 중입니다.
- **포럼 URL**
    - Unreal Engine 5.7 Preview: [https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958](https://forums.unrealengine.com/t/unreal-engine-5-7-preview/2658958)

## 6. 신기능 및 실험적 기능
- **새로 추가된 기능**
    - **Procedural Vegetation Editor (Experimental)**: Fab 에셋을 사용하여 Nanite-ready 폴리지를 에디터 내에서 실시간으로 생성, 모양 변경 및 커스터마이징할 수 있습니다. PCG 기반 노드 그래프로 작동합니다.
    - **Animation Selection Sets (Experimental)**: 애니메이션 워크플로우를 간소화하여 리그 내 여러 컨트롤에 빠르게 접근할 수 있도록 합니다.
    - **Rigging Blend shapes and Sculpting (Experimental)**: 업계 표준 스컬프팅 워크플로우를 언리얼 엔진 내로 가져왔습니다.
    - **Skeletal Editor 업데이트 (Experimental)**: 모프 쉐이프, 본, 스킨 웨이트를 원활하게 생성 및 편집할 수 있는 기능이 추가되었습니다.
    - **Physics World Collisions (Experimental)**: 캐릭터가 환경과 사실적으로 상호작용하도록 합니다.
- **Beta/Experimental 기능 및 주의사항**
    - **Nanite Foliage (Experimental)**: Nanite Assemblies, Nanite Skinning, Nanite Voxel의 세 가지 시스템을 기반으로 합니다.
    - **MegaLights (Beta)**: 성능 튜닝 컨트롤이 추가되었습니다.
    - **주의사항**: Preview 릴리즈는 불안정할 수 있으므로, 테스트용 프로젝트 사본을 사용하여 테스트할 것을 권장합니다.
- **성능 영향도**
    - **PCG**: GPU 생성 및 게임 스레드 성능 최적화로 UE 5.5 대비 약 두 배 빨라졌습니다.

## 7. 플러그인 및 문서 업데이트
- **공식 플러그인 업데이트**
    - **Procedural Vegetation Editor** 플러그인이 Experimental로 추가되었습니다.
    - **MetaHuman Creator 플러그인**이 Linux 및 macOS를 지원합니다.
- **문서 주요 변경사항**
    - 5.7 Preview의 새로운 기능 및 변경사항에 대한 문서 업데이트가 진행 중입니다. (What's New 섹션 확인 필요)
    - **Epic Developer Assistant**의 UI가 Preview에 표시되지만, 기능은 5.7 정식 릴리즈에 맞춰 제공될 예정입니다.

---
*본 보고서는 Unreal Engine 공식 포럼 및 검색 결과를 기반으로 작성되었으며, 최신 정보가 아닐 수 있습니다. 항상 공식 출처를 통해 정보를 확인하시기 바랍니다.*
