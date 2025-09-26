# upgraded 폴더 구조 설명

`upgraded` 폴더는 legacy 폴더의 전체 파일 및 디렉터리 구조를 그대로 복사한 디렉터리입니다. 실제 파일 내용은 legacy의 각 파일을 복사해와야 하며, 현재는 파일명과 구조만 동일하게 생성되어 있습니다.

## 주요 구조

- MANIFEST.in, README.rst, distribute_setup.py, distribute-0.6.10.tar.gz, setup.py: 프로젝트 메타 및 설치 관련 파일
- docs/: 프로젝트 문서 및 빌드 산출물 포함
    - build/: Sphinx 등으로 생성된 문서 결과물
    - source/: 문서 소스 및 설정 파일
- guachi/: 주요 Python 패키지 소스 코드
    - __init__.py, config.py, database.py: 핵심 모듈
    - tests/: 단위 테스트 코드
- guachi.egg-info/: 패키징 메타데이터

> 실제로 코드를 업그레이드하려면 legacy 폴더의 각 파일 내용을 upgraded 폴더로 복사한 뒤, Python 3 호환성 및 최신 패키징 방식으로 리팩터링해야 합니다.
