# 언리얼 엔진 데일리 브리핑 | 2025년 11월 18일

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate Materials** 프로덕션 준비 완료 및 기본 활성화<br>2. **Procedural Content Generation (PCG)** 프레임워크 프로덕션 준비 완료<br>3. **Nanite Foliage** (실험적 기능) 도입으로 대규모 식생 렌더링 성능 향상 |
| **즉시 확인 필요 사항** | **Substrate Materials**가 기본 활성화되었으므로, 기존 프로젝트의 머티리얼 호환성 및 성능 영향도를 확인해야 합니다. 또한, **MegaLights** (Beta) 및 **AI Assistant** 기능도 검토가 필요합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 is now available](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7**
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate Materials:** 이제 프로덕션 준비가 완료되었으며, 새로운 프로젝트에서 기본 머티리얼 모델로 사용됩니다. 기존 프로젝트는 수동으로 전환해야 합니다.
    - **PCG (Procedural Content Generation):** 대규모 월드 생성을 위한 PCG 프레임워크가 프로덕션 준비를 완료했습니다.
    - **MSVC 컴파일러 업데이트:** 기본 Microsoft Visual C++ 컴파일러가 **MSVC 14.44**로 업데이트되었습니다.
- **릴리즈 노트 URL:** [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:**
    - **Groom assets can no longer be created without curves data** (UE - Graphics Features): Alembic 파일 없이 빈 Groom 에셋 생성이 불가능해짐.
    - **FInstancedStruct member uproperties are not cached when "Generate Optimized Blueprint Component Data" is enabled** (UE - Framework - Blueprint): 최적화된 블루프린트 컴포넌트 데이터 생성 시 `FInstancedStruct` 멤버 속성이 캐시되지 않는 문제.
    - **[AI] SmartObjectPersistentCollection produces errors during Map Validation** (UE - AI - SmartObject): 5.6 버전 이상에서 공간 로딩 액터를 참조할 때 맵 유효성 검사 중 오류 발생.
- **수정된 버그:**
    - **Undoing parent deletion creates duplicate child actors** (UE - Framework - Blueprint): 부모 액터 삭제 취소 시 자식 액터가 중복 생성되는 문제 수정.
    - **Sequencer Crash when Hovering over Binding Properties on a Component with Spaces in its Name** (UE - Anim - Sequencer): 이름에 공백이 있는 컴포넌트의 바인딩 속성에 마우스를 올릴 때 시퀀서 충돌 문제 수정.
- **Workaround:** 현재 보고된 주요 버그에 대한 공식적인 Workaround는 확인되지 않았습니다.
- **Issue Tracker URL:** [Unreal Engine Issues and Bug Tracker](https://issues.unrealengine.com/)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - **최근 7일간의 주요 커밋 정보는 직접적인 접근 제한으로 인해 상세 분석이 어렵습니다.** 일반적으로 EpicGames/UnrealEngine 저장소에는 지속적인 개발 및 버그 수정 커밋이 발생하고 있습니다.
    - **UE 5.7 릴리즈 관련:** 5.7.0 버전이 GitHub에 릴리즈되었으며, 이는 MSVC 14.44 컴파일러 업데이트를 포함합니다.
- **영향받는 시스템:** 엔진 소스 코드 기반으로 빌드하는 모든 개발 환경.
- **GitHub URL:** [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - **MetaHuman 5.7 Released!** (Announcements): Epic Staff인 JamesPullan이 MetaHuman 5.7 릴리즈에 대해 알리는 스레드가 확인되었습니다.
    - **UE5.7 fix for `UE-2705589` causes held inputs to always fire on the next frame** (Programming & Scripting): `UE-2705589` 버그 수정이 입력 처리 방식에 영향을 미쳐 다음 프레임에서 입력이 항상 발생하는 문제에 대한 논의가 진행 중입니다.
- **포럼 URL:** [Epic Developer Community Forums](https://forums.unrealengine.com/)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능:**
    - **AI Assistant:** 에디터 내에서 Unreal Engine에 대한 도움말을 제공하는 새로운 AI 비서 기능이 도입되었습니다.
    - **Polygon2D Data Type:** 새로운 `Polygon2D` 데이터 타입과 관련 연산자가 추가되어 유연성이 향상되었습니다.
- **Beta/Experimental 기능 및 주의사항:**
    - **Nanite Foliage (Experimental):** 대규모 식생 렌더링을 위한 새로운 지오메트리 렌더링 시스템입니다. 성능, 견고성 및 확장성을 위해 설계되었습니다.
    - **MegaLights (Beta):** 새로운 동적 그림자 캐스팅 시스템으로, 렌더링 품질과 성능을 크게 향상시킵니다.
- **성능 영향도:**
    - **Substrate Materials**의 `Adaptive GBuffer`는 픽셀당 복잡한 조명 동작을 가능하게 하지만, 더 무거운 옵션이므로 성능에 영향을 줄 수 있습니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman 5.7**이 릴리즈되었습니다.
- **문서 주요 변경사항:**
    - Unreal Engine 5.7에 맞춰 공식 문서가 업데이트되었습니다.
    - **What's New** 섹션에서 새로운 기능 및 베타/실험적 기능에 대한 정보를 확인할 수 있습니다.
    - **문서 URL:** [Unreal Engine 5.7 Documentation](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation)
