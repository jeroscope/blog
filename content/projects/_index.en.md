---
title: "Projects"
description: ""

# 이 파일(섹션 페이지)은 반드시 렌더되도록 허용
_build:
  render: true        # ← 이게 false/never면 /projects/가 404 남
  list: true

# 하위 항목들만 렌더 금지 (URL 생성 금지)
cascade:
  _build:
    render: false     # /projects/<slug>/ 만들지 않음
    list: true        # 리스트에는 보이게
    publishResources: true
---