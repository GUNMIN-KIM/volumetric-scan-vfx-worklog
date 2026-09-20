# Volumetric Scan VFX 작업 패키지

이 디렉터리는 `SCAN_VFX_HANDOFF.md`만으로는 부족했던 실제 제작 과정을 함께 보존한다.

## 업로드 패키지

- `volumetric-scan-vfx-workflow.zip`: AEP 작업본과 백업, JSX/Python/Swift 제작 스크립트, 트래킹 JSON, 실행 리포트, 자동 매트 확인 JPG 등 98개 파일.
- `volumetric-scan-vfx-previews.zip`: 최신 인물 교체 확인본과 주요 전환·엔딩·에지 검수 이미지를 1600px JPEG로 정리한 미리보기 세트.
- `SCAN_VFX_HANDOFF.md`: 현재 상태, 사용자 피드백, 실패한 방향, 최신 구조와 다음 검수 순서.

압축을 해제하면 원래 작업 폴더 기준 경로인 `docs/`, `work/vfx/`, `outputs/parts-composite/`, `outputs/scan-vfx/` 구조가 복원된다.

## 패키지에 포함된 핵심 항목

- 최신본 `outputs/parts-composite/Parts_Composite_Corrected.aep`
- 교체 전 백업과 잘못된 소스 방향의 첫 합성본
- 이전 Scan VFX AEP 버전과 자동 저장을 제외한 주요 작업본
- 인물 분리, optical flow 정렬, 보호 매트, 표면 분리, 전환, 루프, 컬러와 파티클 관련 제작 스크립트
- 트래킹 성공 프레임 수와 각 단계 실행 리포트
- 마스크와 주요 결과의 검수 이미지

## 용량 제한으로 별도 보관하는 원본

다음 파일은 GitHub 웹 업로드의 단일 파일 제한보다 커서 저장소에 복제하지 않았다. AEP를 다른 컴퓨터에서 열 때 동일 파일을 준비하고 재연결해야 한다.

| 파일 | 크기 | SHA-256 |
| --- | ---: | --- |
| `FINAL_SCAN_VFX_1.mp4` | 369MB | `b4a8adf010a513343964132c29389751705452d11d7bc030af4d7b68a8e56372` |
| `FINAL_SCAN_VFX_20s.mp4` | 369MB | `42235ff537e1d8d681350c7a19907261d93e4dd55ede48f265d4151a8c670bdf` |
| `outputs/parts-composite/Assets/aligned-detail-source.mp4` | 219MB | `b8cf0c787eb8bebc0f5dcd2a8ce6ca62c6772ac635c4d7e7e1cc22aba556a4f8` |

원본 두 파일은 제작 컴퓨터의 `Downloads` 폴더에 있다. `aligned-detail-source.mp4`는 `work/vfx/compose-parts.py`로 다시 만들 수 있다.

## 오디오 식별값

| 파일 | SHA-256 |
| --- | --- |
| `outputs/whisper-hiphop-20s.wav` | `32ce5dbb7e8a87e8d071c136800138be062297aaafb8d101d6d6242047135265` |
| `outputs/whisper-hiphop-20s-lipsync.mp3` | `ee4c92ad541553230fe6130f1ea1ae6b3c54061a49af7a20063ac2e1a212fabc` |

## 제외한 항목

`work/python`, `work/pose-python`, `work/pose-stable`, `work/vfx/swift-cache`는 설치 라이브러리와 컴파일 캐시라 제외했다. 작업 로직은 `work/vfx`의 소스 파일에 있으며, 필요한 패키지 버전과 MediaPipe 관련 제한은 handoff 문서에 기록되어 있다.

최신 AEP는 저장된 상태지만 마지막 인물 소스 교체 이후 전체 재생 검수와 최종 렌더는 완료되지 않았다.
