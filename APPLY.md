# 기존 GitHub 블로그에 적용하기

이 파일은 기존 Chirpy를 교체하는 디자인입니다. 실제 저장소 수정과 배포는 아직 하지 않았습니다.

## 1. 백업

기존 vrynmn.github.io 저장소에서 Code → 초록 Code 버튼 → Download ZIP으로 백업합니다.
직접 작성한 글과 이미지가 있으면 별도 보관하세요.

## 2. 교체

1. 제공된 ZIP을 압축 해제합니다.
2. 브라우저에서 기존 저장소를 열고 키보드 `.`을 눌러 github.dev 편집기를 엽니다.
3. 기존 루트 index.md가 있으면 삭제합니다. 새 index.html과 중복되면 안 됩니다.
4. 기존 Gemfile.lock이 있으면 삭제합니다. 새 Gemfile에 맞게 의존성을 설치해야 합니다.
5. 기존 .github/workflows 안의 YAML 파일들을 삭제합니다. 새 배포 파일 하나만 사용할 것입니다.
6. 백업한 뒤 기존 _layouts, _includes, _sass, _plugins, _tabs, _data와 assets 폴더를 삭제합니다. Chirpy 파일과 새 디자인이 섞이지 않도록 합니다. 직접 추가한 이미지는 보관했다가 다시 추가하세요.
7. 압축 해제한 field-notes-blog 폴더 **안의 파일과 폴더 전체**를 편집기 왼쪽 파일 탐색기에 드래그해서 올립니다. 바깥 field-notes-blog 폴더 자체를 올리지 마세요.
8. _config.yml, index.html, Gemfile이 저장소 최상위에 있고, .github/workflows/pages-deploy.yml이 있는지 확인합니다. 숨김 폴더 .github도 필요합니다.
9. _posts의 기존 글은 유지합니다. examples의 글은 배포되지 않습니다.
10. Source Control에서 메시지를 적고 Commit & Push로 저장합니다. 버튼명은 Commit 또는 Sync Changes로 표시될 수도 있습니다.

기존 .nojekyll은 남아 있어도 제공된 Actions가 직접 Jekyll을 빌드하므로 사용할 수 있습니다.
.git 폴더는 삭제하지 마세요. github.dev에서는 보통 표시되지 않습니다.
브라우저 업로드가 어렵다면 GitHub Desktop으로 Clone한 뒤 로컬 VS Code에서 같은 파일 교체를 하고 Commit/Push해도 됩니다.

## 3. 배포

- Settings → Pages → Source: **GitHub Actions**
- Actions 탭 → **Build and deploy blog**가 초록 체크로 끝나는지 확인
- https://vrynmn.github.io/ 접속

설정 전에 실행되어 실패했다면 해당 실행의 Re-run all jobs를 누르세요.
이전 디자인이 남으면 Ctrl+Shift+R 또는 시크릿 창에서 확인하세요.
Chirpy 오프라인 캐시가 계속 남으면 해당 사이트의 저장된 사이트 데이터를 삭제하세요.

## 4. 확인

- 인사말과 폴더 크기
- 카테고리 링크 6개
- About의 본인 소개 내용
- 첫 글 작성 후 Recent posts와 해당 카테고리에 글이 표시되는지

예시 자기소개는 기존 대화 내용을 바탕으로 작성했습니다. 공개 전 확인해주세요.
자동 배포 설정 참고: https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages
