# 후보 2번 블로그

흰 배경과 검정 글씨, Hi there 48px + 폴더 64px. 모바일은 각각 38px, 52px입니다.
카테고리 6개와 최근 글 5개, 전체 글, 자기소개, 게시글 페이지를 제공합니다.
Chirpy에 덧붙이는 스킨이 아닌 독립 Jekyll 디자인입니다. APPLY.md를 따라 교체하세요.

## 글 추가

`examples/2026-10-27-first-note.md`를 복사해 `_posts/YYYY-MM-DD-영문제목.md`로 저장합니다.
제목, 날짜, 본문을 바꾸고 아래 중 하나를 categories에 정확히 입력합니다.

- 개발
- CTF/Wargame
- Bug Bounty
- 블로그/기술문서
- 논문/컨퍼런스
- 공모전/자격증

예: `categories: ["CTF/Wargame"]`
슬래시가 들어간 이름도 하나의 문자열로 적습니다. tags는 자유롭게 여러 개 넣어도 됩니다.
날짜는 한국 시간으로 입력하고 미래 날짜는 게시되지 않습니다. UTF-8로 저장하세요.
예시 글은 examples에만 있으며 사이트에 자동 게시되지 않습니다.

## 수정 위치

- 인사말: index.html
- 자기소개: about.md
- 글자 크기·간격: assets/css/style.css
- 캐릭터: assets/img/folder.png
- 작성자·GitHub·사이트 정보: _config.yml
- 카테고리명·순서: _data/categories.yml

카테고리 이름을 바꾸면 categories 폴더의 category_name과 각 게시글의 categories도 함께 바꿔야 합니다.
분류 페이지는 비어 있어도 존재하며, 글을 추가하면 자동으로 목록에 표시됩니다.

## 미리보기와 실행

preview.html을 더블클릭하면 홈 디자인을 확인할 수 있습니다.
이 파일은 정적 디자인 미리보기이므로 Posts/About/카테고리 링크의 실제 동작은 배포 후 확인합니다.
로컬 Jekyll 실행은 Ruby 3.3과 Bundler 설치 후 `bundle install`, `bundle exec jekyll serve`.

## 캐릭터 제작

내장 이미지 생성 도구로 사용자 제공 캐릭터를 참고해 투명 PNG를 생성했습니다.
프롬프트: 원본의 하늘색 둥근 폴더·검정 손그림 윤곽·점 눈·웃는 입을 유지하고, 배경·그림자 없이 독립 투명 PNG로 재현.
원본 캐릭터의 권리는 원 권리자에게 있습니다.
