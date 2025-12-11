# 언리얼 엔진 데일리 브리핑 | 2025년 12월 12일

## 1. 핵심 요약

금일(2025년 12월 12일 KST) 기준, 언리얼 엔진의 가장 중요한 최신 기술 업데이트는 **UE 5.7.1 핫픽스** 릴리즈입니다. 이 핫픽스는 5.7 버전 출시 이후 보고된 약 100여 개의 버그 및 크래시를 수정하여 안정성을 크게 향상시켰습니다.

- **주요 업데이트 상위 3개**
    1.  **UE 5.7.1 핫픽스 릴리즈:** 약 100여 개의 버그 및 크래시 수정으로 5.7 버전의 안정성 대폭 개선.
    2.  **PCG (Procedural Content Generation) 안정화:** PCG 관련 크래시 및 오류 수정 (예: `[PCG] Polygon offset can create metadata errors`, `[PCG] FPCGGraphCompilerGPU::BuildComputeGraphTask` 오류).
    3.  **렌더링 및 메타휴먼 관련 크래시 수정:** Path Tracing, Cinematic MetaHumans, Substrate/MegaLight 조합 사용 시 발생하던 주요 크래시 문제 해결.

- **즉시 확인 필요 사항**
    *   **UE 5.7 사용자:** 5.7.0 버전에서 발생하던 다수의 크래시 및 버그가 5.7.1에서 해결되었으므로, **즉시 5.7.1로 업데이트**하는 것을 권장합니다.
    *   **Linux 사용자:** UE 5.7부터 Linux 빌드 환경이 SDL2에서 **SDL3**로 전환되었습니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 변경 사항을 재작업해야 합니다.

- **출처 URL 및 게시일 (YYYY-MM-DD)**
    *   UE 5.7.1 Hotfix Released: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02)

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈 (정확한 버전 번호)**
    *   **Unreal Engine 5.7.1 Hotfix**

- **주요 변경사항 및 Breaking Changes**
    *   **주요 변경사항:** 약 100여 개의 버그 수정 및 안정성 개선.
    *   **Breaking Changes (주의사항):** Linux 환경에서 SDL2에서 SDL3로의 전환이 이루어졌습니다. 기존 SDL2 기반 커스터마이징 코드는 호환성 문제가 발생할 수 있습니다.

- **릴리즈 노트 URL**
    *   [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그**
    *   최근 7일간 5.7.1 핫픽스보다 더 중요한 새로운 버그 보고는 확인되지 않았습니다. 핫픽스 이후의 안정화 단계에 있습니다.

- **수정된 버그 (5.7.1 Hotfix 주요 수정 사항)**
    *   `UE-193929`: mGPU 환경에서 Path Tracing 뷰 모드 활성화 시 카메라 이동 중 에디터 응답 없음 현상.
    *   `UE-227868`: 레벨 뷰포트에서 Cinematic MetaHumans 사용 시 AMD GPU 크래시.
    *   `UE-349638`: PCG(Procedural Content Generation) 사용 시 PIE(Play In Editor)에서 에디터와 게임 월드가 동시에 렌더링되어 렌더링 비용이 두 배로 증가하는 문제.
    *   `UE-349535`: `megalight=1`, `Substrate=1`, `GBufferFormat=1` 설정 조합에서 발생하는 크래시.
    *   `UE-352426`: EOS(Epic Online Services) 바이너리 업데이트 (1.18.1.2).

- **Workaround**
    *   5.7.1 핫픽스가 대부분의 주요 문제를 해결했으므로, **5.7.1로 업데이트**하는 것이 가장 확실한 Workaround입니다.

- **Issue Tracker URL**
    *   [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request**
    *   최근 7일간의 주요 커밋은 5.7.1 핫픽스에 통합되었습니다. 외부에서 주목할 만한 신규 커밋은 확인되지 않았습니다.
    *   **주목할 만한 수정 커밋:** `UE-347106` (GitHub 13887) - `Loadmap` 시 `FVirtualTextureAllocator::AcquireBlock`에서 치명적인 어서트(assert)를 피하기 위해 보류 중인(pending-delete) Virtual Texture를 즉시 해제하는 수정.

- **영향받는 시스템**
    *   Virtual Texture System, Engine Core

- **GitHub URL**
    *   [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드**
    *   가장 최근의 Epic Staff(TinaWisdom) 공식 발표는 **5.7.1 Hotfix Released** 스레드입니다. 이 스레드에서 사용자 피드백을 받고 있습니다.

- **포럼 URL**
    *   5.7.1 Hotfix Released: [https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능**
    *   최근 7일간 핫픽스 외에 새로운 기능 추가는 없었습니다. 가장 최신 메이저 버전인 **UE 5.7**의 주요 기능은 다음과 같습니다.
        *   **Substrate (Production-Ready):** 모듈형 머티리얼 프레임워크가 정식 버전으로 전환되어, 자동차 페인트나 피부와 같은 물리적으로 정확한 레이어드 머티리얼 제작이 가능해졌습니다.
        *   **PCG (Procedural Content Generation) 안정화:** 대규모 오픈 월드 제작을 위한 PCG 시스템이 더욱 안정화되고 성능이 개선되었습니다.
        *   **Nanite Foliage:** 나나이트 기반의 새로운 폴리지(Foliage) 시스템이 도입되어, 대규모 초목 환경을 높은 디테일과 효율로 렌더링할 수 있게 되었습니다.

- **Beta/Experimental 기능 및 주의사항**
    *   **Procedural Vegetation Editor (Experimental):** 커스텀 Nanite 지원 나무를 생성할 수 있는 실험적 기능이 5.7에 포함되었습니다.
    *   **성능 영향도:** UE 5.7은 전반적으로 성능 향상을 목표로 했으며, 특히 Nanite Foliage 시스템은 대규모 초목 렌더링 비용을 크게 절감하는 **게임 체인저**로 평가받고 있습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트**
    *   **EOS (Epic Online Services) Binary Update:** 5.7.1 핫픽스에 EOS 1.18.1.2 바이너리 업데이트가 포함되었습니다.
    *   **SDL Camera Plugin:** AMD 하드웨어에서 SDL Camera 플러그인 유효성 검사 관련 수정 사항이 5.7.1에 포함되었습니다.

- **문서 주요 변경사항**
    *   UE 5.7 릴리즈에 맞춰 공식 문서가 업데이트되었습니다. 특히 **Substrate**, **PCG**, **Nanite Foliage** 관련 문서가 최신 정보로 갱신되었습니다.
    *   **최근 문서 업데이트 예시:** `UDeveloperSettings` API 문서 (2025-12-11 업데이트 확인).
    *   **공식 문서 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine](https://dev.epicgames.com/documentation/en-us/unreal-engine)
