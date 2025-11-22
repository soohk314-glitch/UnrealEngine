# 언리얼 엔진 데일리 브리핑 | 2025년 11월 15일

## 1. 핵심 요약

| 순위 | 주요 업데이트 | 상태 | 출처 URL | 게시일 (KST) |
| :--- | :--- | :--- | :--- | :--- |
| 1 | **Unreal Engine 5.7 공식 릴리즈** | 정식 | [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) | 2025-11-12 |
| 2 | **PCG 및 Substrate 프로덕션 레디** | 정식 | [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) | 2025-11-12 |
| 3 | **Nanite Foliage 및 In-editor AI Assistant 추가** | 실험적/새 기능 | [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913) | 2025-11-12 |

**즉시 확인 필요 사항:**
*   **UE 5.7 Linux 사용자:** SDL2에서 SDL3로 전환되어, 기존 SDL2 커스터마이징 코드는 SDL3에 맞게 수정해야 합니다.
*   **UE 5.7 Crash on Launch:** `Unable to use default cache graph` 오류 발생 시, `C:\Users\[YourName]\AppData\Local\UnrealEngine\Common\Zen` 및 `C:\Users\[YourName]\AppData\Local\UnrealEngine\DerivedDataCache\Zen` 폴더를 삭제하여 ZenServer 캐시를 재설정해야 합니다.
*   **UE 5.7 Side Scroller 템플릿 버그 (Linux):** 프로젝트 생성 시 Side Scroller 맵이 비어 보이는 버그가 있으며, 임시 해결책(Workaround)이 포럼에 공유되었습니다.

## 2. 공식 릴리즈 및 패치

*   **버전 릴리즈:** **Unreal Engine 5.7.0** (2025년 11월 12일)
*   **주요 변경사항:**
    *   **PCG (Procedural Content Generation) 프레임워크**가 **프로덕션 레디(Production-Ready)**로 전환되었습니다.
    *   **Substrate** 모듈형 머티리얼 시스템이 **프로덕션 레디**로 전환되었습니다.
    *   **MegaLights** 기능이 **베타(Beta)**로 전환되어, 더 많은 동적 그림자 캐스팅 라이트를 지원합니다.
    *   **MetaHuman Creator** 플러그인이 **Linux 및 macOS**를 지원합니다.
    *   **Animation Mode**가 리팩토링되어 워크플로우가 간소화되었습니다.
*   **Breaking Changes:**
    *   **Linux 플랫폼:** UE 5.7부터 **SDL2에서 SDL3로 전환**되었습니다. SDL2 코드를 커스터마이징한 사용자는 SDL3에 맞게 코드를 수정해야 합니다.
    *   **Visual C++ 컴파일러:** 기본 Microsoft Visual C++ 컴파일러가 **MSVC 14.44**로 업데이트되었습니다.
*   **릴리즈 노트 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

| 유형 | 설명 | Workaround | Issue Tracker URL |
| :--- | :--- | :--- | :--- |
| **새로 보고된 주요 버그** | **UE-353908:** Sequencer 사용 시 BP 벡터의 3D 위젯이 액터로 스냅되는 문제. | 없음 | [https://issues.unrealengine.com/issue/UE-353908](https://issues.unrealengine.com/issue/UE-353908) |
| | **UE-353882:** 매크로 내에서 Mesh Variation 노드 사용 시 머티리얼 슬롯 이름이 손실되는 문제. | 없음 | [https://issues.unrealengine.com/issue/UE-353882](https://issues.unrealengine.com/issue/UE-353882) |
| **수정된 버그** | **UE-352954:** 이름에 공백이 있는 컴포넌트의 바인딩 속성에 마우스를 올릴 때 Sequencer가 충돌하는 문제. | 해당 없음 | [https://issues.unrealengine.com/issue/UE-352954](https://issues.unrealengine.com/issue/UE-352954) |
| | **UE-351823:** PCG 액터 삭제를 되돌릴 때 PCG 컴포넌트에서 인스턴스 카테고리가 제거되는 문제. | 해당 없음 | [https://issues.unrealengine.com/issue/UE-351823](https://issues.unrealengine.com/issue/UE-351823) |
| **Workaround** | **UE 5.7 Linux Side Scroller 템플릿 버그:** `manifest.json` 파일의 대소문자 수정 및 `__ExternalActors__`, `__ExternalObjects__` 폴더의 콘텐츠를 프로젝트 디렉토리로 복사. | [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913/5](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913/5) | 해당 없음 |
| | **UE 5.7 Crash on Launch (ZenServer):** `C:\Users\[YourName]\AppData\Local\UnrealEngine\Common\Zen` 및 `DerivedDataCache\Zen` 폴더 삭제. | [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913/14](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913/14) | 해당 없음 |

**Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

Unreal Engine 5.7 릴리즈가 3일 전에 이루어졌으며, 릴리즈 이후의 주요 커밋은 주로 핫픽스 및 안정화 작업에 집중될 것으로 예상됩니다. 현재 시점(2025-11-15)에서 릴리즈 직후의 대규모 기능 커밋은 확인되지 않았습니다.

*   **주요 커밋 및 Pull Request:** Unreal Engine 5.7.0 릴리즈에 포함된 변경사항이 가장 최근의 주요 업데이트입니다.
*   **영향받는 시스템:** 엔진 전반 (UE 5.7 릴리즈)
*   **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

*   **Epic Staff 답변 기술 스레드:**
    *   **UE 5.7 Known Issues:** Epic Staff인 **MorganC**가 UE 5.7의 알려진 이슈(Linux Side Scroller 템플릿 버그, Mobile Multi-View 라이팅 문제)와 임시 해결책을 공유했습니다.
    *   **UE 5.7 Crash on Launch (ZenServer):** 사용자 **Avytus**가 `Unable to use default cache graph` 오류에 대한 해결책(ZenServer 캐시 폴더 삭제)을 상세히 공유했습니다.
*   **포럼 URL:** [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)

## 6. 신기능 및 실험적 기능

| 기능 | 상태 | 주요 내용 | 성능 영향도/주의사항 |
| :--- | :--- | :--- | :--- |
| **Nanite Foliage** | **Experimental** | Nanite Voxels를 사용하여 조밀하고 상세한 환경을 효율적으로 렌더링합니다. Nanite Assemblies 및 Nanite Skinning을 활용합니다. | LOD나 팝핑 없이 고밀도 지오메트리 표현 가능. PVE로 생성된 메시 지원. |
| **Procedural Vegetation Editor (PVE)** | **Experimental** | UE 내에서 식생 에셋을 생성하고 커스터마이징할 수 있는 PCG 기반 툴입니다. Nanite Skeletal Assemblies를 출력합니다. | Quixel Megaplants 지원. PCG의 유연성을 보여주는 예시. |
| **MegaLights** | **Beta** | 동적이고 그림자를 캐스팅하는 라이트를 장면당 훨씬 더 많이 지원하여 복잡한 광원에서 사실적인 부드러운 그림자를 구현합니다. | 전반적인 시각적 충실도 향상. 수동 최적화 필요성 감소. |
| **In-editor AI Assistant** | **New Feature** | 에디터 내에서 실시간으로 C++ 코드 생성, 질문 답변, 단계별 도움을 제공하는 AI 도우미입니다. | **F1** 키를 눌러 컨텍스트 대화 시작 가능. |
| **Windows arm64/arm64ec 지원** | **Experimental** | Windows arm64 및 arm64ec에 대한 실험적 지원이 도입되었습니다. | arm64ec는 전체 소스 빌드에서만 작동하며, 런처 에디터에서는 지원되지 않습니다. arm64 패키징은 매우 실험적입니다. |

## 7. 플러그인 및 문서 업데이트

*   **공식 플러그인 업데이트:**
    *   **MetaHuman Creator 플러그인:** 이제 **Linux 및 macOS**에서 사용 가능합니다.
    *   **MetaHuman Animator:** Linux 및 macOS 지원은 향후 릴리즈에 예정되어 있습니다.
    *   **Live Link Face:** iPad 또는 Android 장치의 외부 카메라를 통한 실시간 퍼포먼스 캡처 지원.
*   **문서 주요 변경사항:**
    *   **PCG 프레임워크** 및 **Substrate**의 프로덕션 레디 전환에 따라 관련 문서가 업데이트되었습니다.
    *   **UE 5.7 릴리즈 노트**가 공식적으로 게시되었습니다.
*   **문서 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
