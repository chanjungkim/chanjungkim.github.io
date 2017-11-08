---
name: opensource
title: 오픈소스
---

<!--
name: 매칭을 위한 문자열(일종의 PK)입니다.
title: 태그별 포스트 목록 페이지 상단에 표시되는 것입니다.
image: 태그별 포스트 목록 페이지 상단에 표시되는 것으로 없어도 됩니다.
layout은 생략했으므로, 위에서 _config.yml에 설정한 tag가 됩니다.
permalink는 생략했으므로, 위에서 _config.yml에 설정한 /tags/:path/가 됩니다.

주의: 새로운 태그가 추가되면 새로운 파일을 만들어줘야 합니다.

태그별 포스트 목록 페이지를 생성하는 과정은 다음과 같습니다:
1. _tags 디렉토리 아래의 파일목록을 수집해서 템플릿 변수 site.tags 에 담아둔다.(_config.yml의 collections 설정에 tags가 있으므로)
2. _tags 디렉토리 아래의 파일들(예: _tags/opensource.md 등)을 처리해서 HTML 파일을 생성한다.(_config.yml의 collections 설정에 output: true 이므로)
3. 각 태그 파일의 데이터를 _layouts/tag.html 레이아웃 템플릿을 결합해서(_config.yml의 defaults 설정에 layout: tag 이므로)
4. tags/opensource/index.html 등의 파일에 저장한다.(_config.yml의 collections 설정에 permalink: /tags/:path/ 이므로)
-->