# 언리얼 엔진 데일리 브리핑 | 2025년 11월 20일

## 1. 핵심 요약

| 항목 | 내용 | 출처 URL 및 게시일 (KST) |
| :--- | :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate** 머티리얼 시스템 정식 출시 (Production-Ready) | [포럼](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) (2025-11-12) |
| | 2. **Procedural Content Generation (PCG)** 프레임워크 정식 출시 | [포럼](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) (2025-11-12) |
| | 3. **MegaLights** 베타 버전 출시 (동적 그림자 캐스팅 광원 대폭 증가) | [포럼](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) (2025-11-12) |
| **즉시 확인 필요 사항** | UE 5.7부터 **Linux**에서 SDL2가 **SDL3**로 전환됩니다. SDL2 코드를 커스터마이징한 사용자는 변경 사항을 적용해야 합니다. | [포럼](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** Unreal Engine 5.7 (2025-11-12)
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate** 머티리얼 시스템이 정식 출시되어 물리적으로 정확한 레이어링 머티리얼(금속, 클리어 코트, 피부 등)을 지원합니다.
    - **PCG** 프레임워크가 정식 출시되어 대규모 환경을 절차적으로 생성하는 데 사용할 수 있습니다.
    - **Linux** 플랫폼에서 SDL2가 **SDL3**로 전환됩니다.
    - **실험적 기능:** Windows arm64 및 arm64ec 지원이 추가되었습니다.
- **릴리즈 노트 URL:** [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:**
    - **UE-354235:** (3일 전 보고) 상세 내용은 공개되지 않았으나, 이슈 트래커에 최근 활동이 있습니다.
    - **TM-22650:** (3일 전 보고) 상세 내용은 공개되지 않았으나, 이슈 트래커에 최근 활동이 있습니다.
- **수정된 버그:**
    - 최근 7일 이내에 특정 버전의 버그 수정 패치에 대한 공식적인 발표는 확인되지 않았습니다.
- **Workaround:**
    - 최근 7일 이내에 공식적으로 제공된 Workaround 정보는 확인되지 않았습니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/issue/search](https://issues.unrealengine.com/issue/search)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - Epic Games의 공식 GitHub 저장소에 대한 최근 7일간의 주요 커밋 내용은 릴리즈 노트에 포함된 내용 외에 별도로 강조된 사항은 확인되지 않았습니다.
- **영향받는 시스템:**
    - Unreal Engine 5.7 소스 코드 전반
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **Unity와 Epic Games의 협력 발표:** Unity와 Epic Games가 개방적이고 상호 운용 가능한 미래를 위해 협력한다는 발표가 있었습니다. 이는 업계 전반에 영향을 미칠 수 있는 중요한 소식입니다.
    - **UE5.7 입력 버그 논의:** UE 5.7에서 `UE-270589` 수정으로 인해 입력(Input)이 항상 재트리거되는 문제가 발생한다는 논의가 있습니다. (2일 전)
- **포럼 URL:** [https://forums.unrealengine.com/latest](https://forums.unrealengine.com/latest)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능 (UE 5.7 기준):**
    - **AI Assistant:** 에디터 내에서 실시간 가이드, C++ 코드 생성, 단계별 도움을 제공하는 AI 비서 기능이 추가되었습니다. (F1 키로 컨텍스트 대화 시작)
    - **Home Panel:** 튜토리얼, 문서, 뉴스, 포럼 및 최근 프로젝트에 대한 접근을 중앙 집중화합니다.
    - **MetaHuman Creator Linux/macOS 지원:** MetaHuman Creator 플러그인이 Linux 및 macOS에서도 사용 가능해졌습니다.
- **Beta/Experimental 기능 및 주의사항 (UE 5.7 기준):**
    - **Beta:** **MegaLights** (더 많은 동적 그림자 캐스팅 광원 지원)
    - **Experimental:** **Nanite Foliage** (밀집된 환경을 효율적으로 렌더링), **Windows arm64/arm64ec 지원** (Launcher 에디터에서는 arm64ec 기능 미지원, arm64 패키징은 실험적)
- **성능 영향도:**
    - **MegaLights**는 더 많은 광원을 지원하면서도 성능 향상을 목표로 합니다.
    - **Nanite Foliage**는 LOD나 팝핑 없이 고밀도 환경을 효율적으로 렌더링하여 성능에 긍정적인 영향을 줄 수 있습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman Creator 플러그인:** Linux 및 macOS 지원 추가.
    - **Live Link Face:** iPad 또는 Android 장치에서 외부 카메라를 사용한 실시간 퍼포먼스 캡처 지원.
- **문서 주요 변경사항:**
    - Unreal Engine 5.7 릴리즈에 맞춰 모든 공식 문서가 업데이트되었습니다.
    - **Verse API 변경 (Fortnite/UEFN 관련):** `AllowPaidRandomItems` 및 `AllowDirectPromptsToPurchase`가 `RestrictPaidRandomItems` 및 `RestrictDirectPromptsToPurchase`로 대체되었습니다. 기존 코드는 컴파일되지 않으므로 로직을 반전하여 수정해야 합니다. (2025-11-19)
    - **Verse API 변경 URL:** [https://forums.unrealengine.com/t/transactions-sur-l-ile-modification-de-l-api-verse-du-module-marche/2676500](https://forums.unrealengine.com/t/transactions-sur-l-ile-modification-de-l-api-verse-du-module-marche/2676500)
