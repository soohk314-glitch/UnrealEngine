# 언리얼 엔진 데일리 브리핑 | 2025년 12월 22일

## 1. 핵심 요약
- **언리얼 엔진 5.7 정식 출시 및 5.7.1 핫픽스 배포**: Nanite Foliage, Mover 플러그인 등 대규모 기능이 포함된 5.7 버전과 약 100여 개의 버그 수정을 포함한 5.7.1 핫픽스가 최신 상태입니다.
- **Nanite Foliage 실험적 기능 도입**: 수백만 개의 겹치는 요소를 효율적으로 렌더링하는 Nanite Voxels 및 Skinning 기술이 도입되어 대규모 오픈 월드 식생 구현이 가능해졌습니다.
- **주요 렌더링 및 크래시 이슈 대응**: NVIDIA 드라이버 580+ 버전에서의 DoF 품질 저하 및 특정 렌더링 설정 시의 가상 메모리 누수 등 실무 개발에 직결되는 이슈들이 보고 및 수정 중입니다.

| 항목 | 내용 | 출처 및 게시일 |
| :--- | :--- | :--- |
| 최신 버전 | Unreal Engine 5.7.1 Hotfix | [Forums](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235) (2025-12-02) |
| 주요 신기능 | Nanite Foliage (Experimental) | [Official News](https://www.unrealengine.com/en-US/news/unreal-engine-5-7-is-now-available) (2025-11-12) |
| 긴급 확인 | NVIDIA Driver 580+ DoF Issue | [Issue Tracker](https://issues.unrealengine.com/issue/UE-348441) (2025-12-18) |

## 2. 공식 릴리즈 및 패치
- **버전 릴리즈**: **Unreal Engine 5.7.1 Hotfix**
- **주요 변경사항**:
    - **안정성 강화**: 약 100여 개의 크래시 및 버그 수정 완료.
    - **플랫폼 업데이트**: Linux 환경에서 SDL2에서 **SDL3**로의 전환 시작. 기존 SDL2 커스텀 코드를 사용하는 경우 리워크가 필요합니다.
    - **렌더링 수정**: Path Tracing 모드에서 mGPU 사용 시 카메라 이동 시 응답 없음 현상 수정 (UE-193929).
- **릴리즈 노트 URL**: [UE 5.7.1 Hotfix Notes](https://forums.unrealengine.com/t/5-7-1-hotfix-released/2681235)

## 3. 버그 및 이슈
- **새로 보고된 주요 버그**:
    - **가상 메모리 누수 (UE-Rendering Architecture)**: 특정 렌더링 설정(r.GBufferFormat 3, r.Lumen.TraceMeshSDFs 1 등) 사용 시 추적되지 않는 가상 메모리 증가 보고 (2025-12-20).
    - **Skeletal Mesh BLAS 업데이트 이슈**: 애니메이션이 없거나 틱이 발생하지 않는 스켈레탈 메시의 BLAS가 매 프레임 업데이트되어 성능 저하 유발 (2025-12-19).
- **수정된 주요 버그 (5.7.1)**:
    - **NVIDIA 드라이버 581 관련**: DoF(피사체 심도) 플리커 현상 수정 (UE-348441).
    - **PCG 관련**: PIE 실행 시 에디터와 게임 월드가 중복 렌더링되어 렌더링 비용이 두 배로 발생하는 문제 수정 (UE-349638).
- **Issue Tracker URL**: [Unreal Engine Issues](https://issues.unrealengine.com/issue/search?project=unreal_engine&status=Unresolved&sort=created&direction=desc)

## 4. GitHub 업데이트
- **최근 활동**: EpicGames/UnrealEngine 저장소의 `ue5-main` 및 `5.7` 브랜치에서 지속적인 핫픽스 및 성능 최적화 커밋이 진행 중입니다.
- **영향받는 시스템**:
    - **Vulkan RHI**: Vulkan에서 별칭 텍스처(Aliased Textures)가 올바른 뷰를 사용하도록 수정 (GitHub PR 13964).
    - **Virtual Texture**: 맵 로드 시 삭제 대기 중인 가상 텍스처를 즉시 해제하여 Fatal Assert 방지 (GitHub PR 13887).
- **GitHub URL**: [EpicGames/UnrealEngine](https://github.com/EpicGames/UnrealEngine) (계정 연동 필요)

## 5. 공식 포럼 기술 논의
- **주요 스레드**:
    - **NVIDIA Driver 580+ DoF 이슈**: 최신 드라이버 사용 시 DoF 품질이 저하되는 현상에 대해 Epic Staff가 인지하고 5.7.1에서 대응 중임을 확인.
    - **Fab 퍼블리셔 액세스 이슈**: 최근 런칭된 Fab 플랫폼에서 퍼블리셔 권한 부여 지연 문제에 대한 공식 공지 및 대응 논의 진행 중.
- **포럼 URL**: [Epic Developer Community Forums](https://forums.unrealengine.com/latest)

## 6. 신기능 및 실험적 기능
- **Nanite Foliage (Experimental)**:
    - **Nanite Voxels**: 멀리 있는 식생을 고체 질량으로 인식하여 LOD 없이 부드럽게 렌더링.
    - **Nanite Skinning**: 바람 반응 등 동적 동작을 Nanite 수준에서 처리.
- **Mover 플러그인**: 기존 Character Movement Component를 대체할 수 있는 새로운 고성능 이동 시스템. 5.7.1에서 멀티플레이어 복제(Replication) 관련 데싱크 이슈가 일부 수정되었습니다.
- **성능 영향도**: Nanite Foliage 사용 시 메모리 사용량은 증가할 수 있으나, 드로우 콜 감소 및 LOD 연산 제거로 전체적인 프레임 레이트 안정화에 기여.

## 7. 플러그인 및 문서 업데이트
- **공식 플러그인**:
    - **DaySequenceModifier**: 특정 시퀀스가 null일 때 발생하는 크래시 수정.
    - **EOS SDK**: 1.18.1.2 바이너리 업데이트 반영.
- **문서 업데이트**: [Nanite Foliage 공식 문서](https://dev.epicgames.com/documentation/en-us/unreal-engine/nanite-foliage)가 업데이트되어 상세 워크플로우 및 제약 사항이 추가되었습니다.
