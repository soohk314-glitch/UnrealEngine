# 언리얼 엔진 데일리 브리핑 | 2025년 11월 16일

## 1. 핵심 요약

| 항목 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Unreal Engine 5.7 공식 릴리즈** (2025-11-12) |
| | 2. **Substrate** (모듈식 머티리얼 시스템) **프로덕션 준비 완료** |
| | 3. **PCG** (절차적 콘텐츠 생성) **프레임워크 프로덕션 준비 완료** |
| **즉시 확인 필요 사항** | UE 5.7에서 **Linux 환경의 SDL2가 SDL3로 전환**되어, 기존 SDL2 커스터마이징 코드를 사용하는 경우 재작업이 필요합니다. 또한, **Side Scroller 템플릿 프로젝트 생성 시 Linux에서 맵이 비어 보이는 버그**가 보고되었습니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Released (포럼)](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7** (2025-11-12)
- **주요 변경사항 및 Breaking Changes:**
    - **PCG 프레임워크** 및 **Substrate** 머티리얼 시스템이 **프로덕션 준비 완료(Production-Ready)** 상태로 전환되었습니다.
    - **Experimental Nanite Foliage** 시스템이 도입되어 대규모 환경에서 고밀도, 고디테일 식생 렌더링이 가능해졌습니다.
    - **MegaLights**가 베타로 전환되어 동적 그림자를 드리우는 광원을 더 많이 사용할 수 있게 되었습니다.
    - **Linux 환경의 SDL2가 SDL3로 전환**되었습니다. 이는 기존 SDL2 기반 코드를 사용하는 개발자에게 **Breaking Change**가 될 수 있습니다.
    - **Experimental Windows arm64 및 arm64ec 지원**이 도입되었습니다.
    - 에디터 내 **AI Assistant** 및 **Home Panel**이 새로 추가되었습니다.
- **릴리즈 노트 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그 (UE 5.7 관련):**
    - **Linux Side Scroller 템플릿 맵 공백:** Side Scroller 변형으로 Third Person 프로젝트 생성 시 Linux에서 맵이 비어 보이는 문제. (5.7.1에서 수정 예정)
    - **Lumen DX11/DX12 SM5 컴파일 에러:** `r.Lumen.Supported.SM5=1` 설정 시 컴파일 에러 발생.
    - **Linux Wayland 환경 불안정:** Wayland 환경에서 에디터 충돌, 메뉴 위치 이상, 버튼 클릭 문제 등 다수 보고. (`SDL_VIDEODRIVER=x11` 설정으로 일부 해결 가능)
    - **Background Blur 위젯 렌더링 문제:** `Corner Radius`가 0보다 큰 `Background Blur` 위젯이 패키징된 게임에서 렌더링되지 않음.
    - **TextBox 위젯 에디터 충돌:** `TextBox` 위젯이 포함된 위젯에서 `Pre-Construct` 이벤트에 스타일 설정 호출 시 에디터 충돌 발생.
- **수정된 버그:**
    - **최근 7일간 공식적으로 수정된 버그에 대한 정보는 Issue Tracker에서 명확히 확인되지 않았습니다.** (Issue Tracker에서 'Fixed' 상태로 필터링하여 추가 확인 필요)
- **Workaround:**
    - **Side Scroller 템플릿 맵 공백 (Linux):** 포럼에서 `manifest.json` 파일 수정 및 프로젝트 콘텐츠 폴더 복사 관련 임시 해결책이 제시되었습니다.
    - **UE 5.7 시작 시 충돌 (`Unable to use default cache graph`):** `C:\Users\[YourName]\AppData\Local\UnrealEngine\Common\Zen` 및 `...\DerivedDataCache\Zen` 폴더를 삭제하고 에디터를 재시작합니다.
    - **Lumen 하드웨어 레이 트레이싱 충돌:** `r.Lumen.HardwareRayTracing.LightingMode`를 0으로 설정하여 충돌을 피할 수 있습니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/issue/search)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - **최근 7일간 EpicGames/UnrealEngine 저장소의 주요 커밋 정보는 직접 확인되지 않았습니다.** (주요 릴리즈 직후에는 릴리즈 관련 커밋이 주를 이루는 경향이 있습니다.)
    - **OldUnreal/UnrealTournamentPatches 저장소**에서 에디터가 무버 스케일을 잘못 적용하는 버그 등 일부 버그 수정 커밋이 있었습니다. (2025-11-09)
- **영향받는 시스템:** 엔진 코어, 빌드 시스템 (UE 5.7 릴리즈 관련)
- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **Unreal Engine 5.7 Released** 스레드에서 Epic Staff (Tina_Wisdom, MorganC)가 릴리즈 관련 공지 및 알려진 이슈(Known Issues)를 공유했습니다.
    - 특히, **MorganC**는 UE 5.7의 **Side Scroller 템플릿 Linux 버그** 및 **Mobile Multi-View 렌더링 버그**에 대한 **Known Issue와 Workaround**를 제공했습니다.
- **포럼 URL:** [Unreal Engine 5.7 Released (포럼)](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능:**
    - **PCG Editor Mode:** PCG 프레임워크를 위한 새로운 에디터 모드.
    - **Procedural Vegetation Editor (PVE):** PCG를 활용하여 식생 에셋을 생성하고 커스터마이징하는 실험적 기능.
    - **Nanite Foliage (Experimental):** 고밀도 식생을 효율적으로 렌더링하는 새로운 시스템.
    - **In-editor AI Assistant:** 에디터 내에서 실시간 가이드, C++ 코드 생성 등을 제공하는 AI 도우미.
    - **Home Panel:** 튜토리얼, 문서, 뉴스, 최근 프로젝트 등을 중앙 집중화한 새로운 패널.
    - **Selection Sets (Animation):** 애니메이션 리깅 컨트롤을 빠르게 선택하고 공유하는 기능.
- **Beta/Experimental 기능 및 주의사항:**
    - **Nanite Foliage**는 **Experimental** 기능입니다.
    - **MegaLights**는 **Beta**로 전환되었습니다.
    - **Windows arm64/arm64ec 지원**은 **Experimental**이며, Launcher 에디터에서는 arm64ec 함수가 지원되지 않습니다.
- **성능 영향도:**
    - PCG 프레임워크에서 GPU 연산 속도 및 파라미터 오버라이드 성능이 향상되었습니다.
    - MegaLights는 향상된 성능으로 더 많은 동적 광원을 지원합니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman Creator Unreal Engine 플러그인**이 **Linux 및 macOS**에서도 사용 가능해졌습니다.
    - **MetaHuman** 에셋을 **Python 또는 Blueprint 스크립팅**을 사용하여 자동화 및 배치 처리할 수 있는 기능이 추가되었습니다.
- **문서 주요 변경사항:**
    - Unreal Engine 5.7 릴리즈에 맞춰 모든 공식 문서가 업데이트되었습니다.
    - **MetaHuman 5.7 Release Notes**가 별도로 제공되어 Groom 플러그인의 개선 사항 등이 포함되었습니다.
    - **릴리즈 노트 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
