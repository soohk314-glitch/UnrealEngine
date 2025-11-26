# 언리얼 엔진 데일리 브리핑 | 2025년 11월 27일 (KST)

## 1. 핵심 요약

| 구분 | 내용 |
| :--- | :--- |
| **주요 업데이트 상위 3개** | 1. **Substrate** 재질 시스템 **프로덕션 준비 완료** 및 기본 활성화. 2. **Nanite Foliage and Skinning** (실험적 기능) 도입으로 고밀도 환경의 효율적인 렌더링 가능. 3. **MegaLights** 기능이 **베타**로 전환, 동적 그림자 광원 지원 강화. |
| **즉시 확인 필요 사항** | Linux 사용자는 UE 5.7부터 **SDL2에서 SDL3로 전환**됨에 따라, SDL2 코드에 대한 사용자 정의 사항을 재작업해야 합니다. |
| **출처 URL 및 게시일** | [Unreal Engine 5.7 Release Notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes) (2025-11-12) |

## 2. 공식 릴리즈 및 패치

- **버전 릴리즈:** **Unreal Engine 5.7**
- **주요 변경사항 및 Breaking Changes:**
    - **Substrate** 재질 시스템이 **프로덕션 준비 완료(Production-Ready)** 상태가 되었으며, 기본적으로 활성화됩니다.
    - **MegaLights** 기능이 **베타(Beta)**로 전환되어 노이즈 감소 및 전반적인 성능이 향상되었으며, Directional Light, Niagara Particle Lights, Translucency, Hair Strands에 대한 지원이 추가되었습니다.
    - **Linux** 플랫폼은 UE 5.7부터 **SDL2에서 SDL3로 전환**됩니다. SDL2 코드에 사용자 정의 사항이 있는 경우, SDL3에 맞게 변경해야 합니다.
    - **Experimental Windows arm64 및 arm64ec 지원**이 도입되었습니다. (Launcher 에디터에서는 arm64ec 함수가 작동하지 않음)
- **릴리즈 노트 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)

## 3. 버그 및 이슈

- **새로 보고된 주요 버그:**
    - 릴리즈 노트에서 직접적으로 새로 보고된 주요 버그는 언급되지 않았습니다.
- **수정된 버그:**
    - 릴리즈 노트에 따르면, 이번 릴리즈에는 커뮤니티 기여자들의 개선 사항이 포함되어 있으나, 구체적인 버그 수정 목록은 릴리즈 노트의 후반부(현재 수집된 내용에는 포함되지 않음) 또는 별도의 패치 노트에서 확인해야 합니다.
- **Workaround:**
    - 현재까지 확인된 Workaround는 없습니다.
- **Issue Tracker URL:** [https://issues.unrealengine.com/](https://issues.unrealengine.com/) (가장 최신 정보를 확인하려면 Issue Tracker에서 직접 검색 필요)

## 4. GitHub 업데이트

- **주요 커밋 및 Pull Request:**
    - Unreal Engine 5.7 릴리즈에는 70명 이상의 커뮤니티 기여자가 제출한 개선 사항이 포함되었습니다.
    - **커뮤니티 기여자 목록:** AlexanderVeselov-arm, AlexBlackfrost, Almax27, andreibazi, az6667, Bit-Rot, Brian-PD, brpendle-ti, bturner, chrysos8201, ckendal3, ColinGulliver, CookiePLMonster, Darcy3000s, dasherman-ea, davidbaack, dmergele, DoubleDeez, DrewWeth, DTG-Will-Marshall, dyanikoglu, erebel55, Eric2-Praxinos, Erlandys, faisa-believer, foobit, gamethread, geordiemhall, glecko, GreenLightning, guansdu, H3mul, IngSubstance, iniside, jamesfAnet, jamespark-unreal, JasonCoombs, jdamdami, jerobarraco, jeysym, Jiboo, JohnJFarrow, Jordonbc, jorge-axiomvfx, jorgenpt, jpritchard1010, KaosSpectrum, KarimLUCCIN, KeithRare, kimkun07-k, kissSimple, klukule, KXOC, laurencei, lclara-BARB, LHG-JonAnderJimenez, ligazetom, LightKL, lsandersljungberg, LucaFranzo98, Maigo, MarcusSvensson92, Mario-Azcona, MartinWickhamFB, Mattiwatti, melku, michael-buschbeck-ms, Minus4-44, moumee, nickdarnell, phochstrasser, PICO-XR, QRare, r457-Ao2, rdunnington, reduf, redxdev, RiotJDebern, rohyunsang, sareali, serhanio, SilverWinter0511, slonopotamus, SoulSharer, sportbikerr1, ssutherland-riot, SukenderDontNod, Sythenz, teddemunnik, tioez326, tokyocplusplus, Tt-Wes, tustanivsky, Vaei, vladbelousoff, vogoltsov, WangKan, Wizzard033, wmiller, x157, yangskyboxlabs, yoonbigbear, zachlute-arenanet, ZeroEightSix, ZeroErrors, zhou-
- **영향받는 시스템:** 렌더링, 캐릭터 및 애니메이션, 월드 빌딩, PCG 등 광범위한 영역.
- **GitHub URL:** [https://github.com/EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine)

## 5. 공식 포럼 기술 논의

- **Epic Staff 답변 기술 스레드:**
    - 가장 최근의 주요 포럼 활동은 **Unreal Engine 5.7 Released**에 대한 Tina_Wisdom (Epic Staff)의 발표입니다.
    - **포럼 URL:** [https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913](https://forums.unrealengine.com/t/unreal-engine-5-7-released/2673913)

## 6. 신기능 및 실험적 기능

- **새로 추가된 기능:**
    - **Substrate** 재질 시스템 (Production-Ready)
    - **Procedural Content Generation (PCG)** 프레임워크 (Production-Ready)
    - **In-editor AI Assistant** (에디터 내에서 실시간 가이드, C++ 코드 생성, 단계별 도움 제공)
    - **Home Panel** (튜토리얼, 문서, 뉴스, 포럼, 최근 프로젝트 접근 중앙화)
- **Beta/Experimental 기능 및 주의사항:**
    - **MegaLights**는 **Beta**로 전환되었습니다.
    - **Nanite Foliage and Skinning**은 **Experimental** 기능입니다. (Nanite Voxels, Nanite Assemblies, Nanite Skinning 포함)
    - **SMAA (Subpixel Morphological Anti-Aliasing)**는 모바일 및 데스크톱 렌더러에서 **Experimental**로 지원됩니다.
    - **Motion Matching Chooser Integration**은 **Experimental** 기능입니다.
- **성능 영향도:**
    - **Nanite Foliage**는 "lifelike and animated foliage that can be delivered within a **60fps budget on current generation hardware**"를 목표로 합니다.
    - **MegaLights**는 노이즈 감소 및 **전반적인 성능 향상**이 있었습니다.
    - **SMAA**는 "high-quality edge smoothing with **minimal performance impact**"를 제공합니다.

## 7. 플러그인 및 문서 업데이트

- **공식 플러그인 업데이트:**
    - **MetaHuman Creator** Unreal Engine 플러그인이 **Linux 및 macOS**에서 사용 가능해졌습니다.
    - **Live Link Face**를 통해 iPad 또는 Android 장치의 외부 카메라에서 실시간 퍼포먼스 캡처가 가능해졌습니다.
- **문서 주요 변경사항:**
    - Unreal Engine 5.7에 맞춰 문서가 업데이트되었습니다.
    - **릴리즈 노트 URL:** [https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes](https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-release-notes)
