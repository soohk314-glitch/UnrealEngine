# 언리얼 엔진 데일리 브리핑 | 2025년 12월 06일

## 1. 핵심 요약

- **주요 업데이트 상위 3개**
    - **Unreal Engine 5.7.1 Hotfix 릴리즈**: 약 100여 개의 주요 버그 및 안정성 문제가 해결되었습니다.
    - **Substrate Material Framework 정식 도입**: 기존 셰이딩 모델을 대체하는 모듈형, 물리 기반 재질 시스템이 도입되어 표현력과 성능이 향상되었습니다. (UE 5.7 기준)
    - **PCG (Procedural Content Generation) 프로덕션 레디**: PCG 프레임워크가 정식 출시되어 에디터 및 런타임 환경에서 안정적으로 사용할 수 있게 되었습니다. (UE 5.7 기준)

- **즉시 확인 필요 사항**
    - **Linux 사용자는 SDL2에서 SDL3로 전환됩니다.** UE 5.7부터 Linux 빌드 환경이 SDL3로 전환됨에 따라, SDL2 코드를 커스터마이징한 사용자는 해당 변경 사항을 SDL3에 맞게 재작업해야 합니다.

- **출처 URL 및 게시일 (YYYY-MM-DD)**
    - 5.7.1 Hotfix 릴리즈: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02)
    - Unreal Engine 5.7 릴리즈 노트: [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12)

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈 (정확한 버전 번호)**
    - **Unreal Engine 5.7.1 Hotfix**

- **주요 변경사항 및 Breaking Changes**
    - **주요 변경사항**: 약 100여 개의 버그 수정 및 안정성 개선이 포함된 핫픽스입니다. 특히 에디터 충돌, MetaHuman, Control Rig, PCG 관련 문제가 다수 해결되었습니다.
    - **Breaking Changes**:
        - **Linux SDL 전환**: UE 5.7부터 Linux 플랫폼에서 SDL2 대신 **SDL3**를 사용합니다. SDL2 관련 커스터마이징 코드는 SDL3에 맞게 업데이트가 필요합니다.
        - **Control Rig 및 Runtime API 변경**: 일부 Control Rig 및 Runtime 관련 API가 변경되어 기존 스크립트 또는 플러그인 호환성에 영향을 줄 수 있습니다.

- **릴리즈 노트 URL**
    - [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그**
    - 최근 7일 이내에 공식적으로 '새로 보고된' 주요 버그에 대한 특정 정보는 확인되지 않았습니다.

- **수정된 버그 (5.7.1 Hotfix 기준)**
    - `UE-193929`: Path Tracing 뷰 모드 활성화 시 에디터 응답 없음 (mGPU 사용 시).
    - `UE-227868`: Cinematic MetaHumans가 레벨 뷰포트에서 AMD GPU 충돌을 유발하는 문제.
    - `UE-349638`: PCG 생성 시 PIE(Play In Editor)에서 에디터와 게임 월드가 모두 렌더링되어 렌더링 비용이 두 배가 되는 문제.
    - `MH-16702`: MetaHuman 캐릭터가 고화질 LOD로 변경될 때 여러 플랫폼에서 발생하는 충돌.
    - `UE-352089`: Full Body IK Solver에 IK Goal 추가 시 발생하는 충돌.

- **Workaround**
    - 5.7.1 Hotfix에서 대부분의 문제가 해결되었으므로, **5.7.1 버전으로 업데이트**하는 것이 권장되는 해결책입니다.

- **Issue Tracker URL**
    - [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**
    - 최근 7일간 EpicGames/UnrealEngine의 주요 커밋이나 Pull Request에 대한 구체적인 내용은 확인되지 않았습니다.
    - **참고**: Epic Games는 일반적으로 릴리즈 브랜치에 대한 커밋을 제한하며, 주요 변경 사항은 릴리즈 노트에 통합됩니다.

- **영향받는 시스템**
    - 해당 사항 없음.

- **GitHub URL**
    - [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**
    - 가장 최근의 Epic Staff 활동은 **5.7.1 Hotfix 릴리즈** 발표 스레드입니다. 해당 스레드에서 사용자 피드백을 받고 있습니다.
    - **주요 논의**: 5.7.1 핫픽스에 포함된 버그 수정 사항에 대한 사용자들의 확인 및 추가적인 이슈 보고.

- **포럼 URL**
    - 5.7.1 Hotfix 릴리즈 스레드: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준)**
    - **MegaLights (Beta)**: 노이즈 감소, 성능 최적화, 향상된 그림자 및 조명 품질을 제공하는 새로운 조명 시스템.
    - **Substrate Material Framework**: 모듈형 재질 시스템으로, 복잡한 재질 표현을 위한 새로운 워크플로우를 제공합니다.
    - **PCG (Procedural Content Generation)**: 정식 버전으로 출시되어 대규모 월드 제작에 안정적으로 사용 가능합니다.

- **Beta/Experimental 기능 및 주의사항 (UE 5.7 기준)**
    - **Nanite Foliage and Skinning (Experimental)**: 나나이트를 이용한 식생 및 스키닝 렌더링 기능. 애니메이션과 풍동 효과를 결합한 정교한 렌더링이 가능하나, **실험적 기능**이므로 프로덕션 환경에 적용 시 주의가 필요합니다.
    - **SMAA (Experimental)**: 새로운 안티앨리어싱 기법이 실험적으로 추가되었습니다.

- **성능 영향도**
    - UE 5.7은 MegaLights, Substrate, Nanite 개선을 통해 전반적인 **렌더링 성능 및 품질 향상**을 목표로 합니다. 다만, 새로운 실험적 기능을 사용할 경우 성능 프로파일링이 필수적입니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**
    - **Game Animation Sample Project (GASP) 업데이트**: UE 5.7에 맞춰 업데이트되었으며, **Mover 플러그인**을 활용하는 새로운 캐릭터와 로코모션 데이터셋이 포함되었습니다.
    - **Cineware for Unreal Engine 2026.1 업데이트**: Skeletal Mesh 임포트 옵션 추가 등 업데이트가 있었습니다. (2025-12-03)

- **문서 주요 변경사항**
    - Unreal Engine 5.7 릴리즈에 맞춰 모든 관련 문서가 업데이트되었습니다. 특히 **Substrate** 및 **PCG** 관련 문서에 중요한 내용이 추가되었습니다.
    - **Linux SDL3 전환**에 대한 문서화가 이루어졌습니다.
