# 언리얼 엔진 데일리 브리핑 | 2025년 11월 28일 (KST)

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7 공식 릴리즈**: 렌더링, 캐릭터/애니메이션, 월드 빌딩 등 광범위한 영역에서 개선. <br> 2. **PCG (Procedural Content Generation) 정식 지원**: 베타 딱지를 떼고 프로덕션 환경에서 사용 가능. <br> 3. **MegaLights 베타 전환**: 실험적 기능에서 베타로 전환되어 안정성 및 기능 개선. |
| **즉시 확인 필요 사항** | **Control Rig**의 `bake_transform_with_settings` 메서드가 UE 5.6에서는 작동하나 5.7에서는 작동하지 않는 버그가 보고됨. 파이썬 스크립트를 통한 자동화 프로세스에 영향을 줄 수 있으므로 확인 필요. |
| **출처 URL 및 게시일** | **Unreal Engine 5.7 Release Notes**: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (게시일: 2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈**: **Unreal Engine 5.7**
- **주요 변경사항 및 Breaking Changes**:
    - **PCG Framework**가 **정식 기능(Production Ready)**으로 전환되었습니다.
    - **MegaLights**가 **베타(Beta)**로 전환되었으며, 노이즈 감소, Directional Light, Niagara Particle Lights, Translucency, Hair Strands 지원이 추가되었습니다.
    - **Substrate** 재질 시스템이 모듈형, 물리 기반 재질 프레임워크로 개선되었으며 Adaptive GBuffer 및 Blendable GBuffer를 지원합니다.
    - **Nanite Foliage 및 Skinning** 기능이 **실험적(Experimental)**으로 추가되었습니다.
- **릴리즈 노트 URL**: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (Latest Bugs)**:
    - **Control Rig Creation Crash**: Skeletal Mesh 이름에 "skel" 접두사 또는 포함 시 Control Rig 생성 충돌 발생.
    - **bake_transform_with_settings 5.7 비작동**: Control Rig의 `bake_transform_with_settings` 파이썬 메서드가 5.6에서는 작동하나 5.7에서는 작동하지 않음.
    - **Dataless Mutable Cloth Simulation**: Dataless Mutable 워크플로우에서 Skeletal Mesh Parameter Node를 사용할 때 천 시뮬레이션이 작동하지 않음.
- **수정된 버그 (Latest Fixes)**:
    - **Ortho near plane clips geometry**: 에디터 Top 뷰(ortho)에서 뷰포트 확대/축소 시 근접 평면이 지오메트리를 클리핑하는 문제 수정.
    - **Child widgets Enhanced Input bindings**: 자식 위젯이 부모로부터 Enhanced Input 바인딩을 유지하지 못하는 문제 수정.
- **Workaround**: 현재 확인된 공식 Workaround는 없습니다.
- **Issue Tracker URL**: [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**:
    - 최근 7일 이내 EpicGames/UnrealEngine 저장소의 주요 기술 업데이트 커밋은 검색되지 않았습니다.
- **영향받는 시스템**: 해당 없음.
- **GitHub URL**: [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**:
    - **Groom Issue 5.6 - 5.7, Blurred**: CineCameraActor에서 Depth of Field를 활성화할 때 Groom이 흐려지거나 잘못된 초점 거리를 읽는 문제에 대한 논의가 있습니다. (8시간 전 보고)
- **포럼 URL**: [https://forums.unrealengine.com/](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능**:
    - **PCG Framework**가 정식 기능으로 전환되었습니다.
    - **Control Rig**에 Dependency View가 추가되었고, 성능이 향상되었습니다.
    - **MetaHuman**에 Creator Linux/macOS 지원, Hair, Body Conformation, Calibrations 등 업데이트가 있었습니다.
- **Beta/Experimental 기능 및 주의사항**:
    - **Beta**: MegaLights, Heterogeneous Volumes.
    - **Experimental**: Nanite Foliage and Skinning, SMAA, Motion Matching Chooser Integration.
    - **주의사항**: 실험적 기능은 프로덕션 환경에서 사용 시 예기치 않은 문제나 성능 저하가 발생할 수 있습니다.
- **성능 영향도**:
    - **Unreal Engine 5.7**은 Incremental Cooking, Build Health Dashboard, TraceLog 개선 등 개발 효율성 및 성능 최적화에 중점을 두었습니다.
    - **Nanite Foliage** 시스템은 복셀을 사용하여 폴리지 렌더링에 큰 성능 개선을 가져올 것으로 예상됩니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**:
    - **MetaHuman 5.7**이 릴리즈되어 MetaHuman Creator 및 MetaHuman Animator에 업데이트가 포함되었습니다.
- **문서 주요 변경사항**:
    - **Unreal Engine 5.7 Release Notes**가 업데이트되었습니다.
    - **What's New** 문서에 5.7의 새로운 기능 및 업데이트된 기능 개요가 제공됩니다.
    - **Unreal Engine 5 Migration Guide**가 업데이트되었습니다.
    - **Beta Features** 및 **Experimental Features** 목록이 업데이트되었습니다.
