---
title: "Notes on Common Windows Kernel Bug Classes"
date: 2025-10-26T00:00:02
draft: false
summary: "윈도우 커널에서 자주 보이는 버그 클래스 정리합니다."
authors: ["JSec"]
tags: ["windows", "kernel"]
---
> 이 글은 **컬러 스킴 전수 테스트**를 위한 샘플입니다. 모든 요소에 색이 어떻게 먹는지 확인하세요.

## 1) 본문 텍스트 & 인라인 스타일

일반 본문입니다. **볼드**, *이탤릭*, ~~스트라이크~~, <mark>형광펜(mark)</mark>, <u>밑줄</u>, <sub>아래첨자</sub>와 <sup>위첨자</sup>.

- 링크: [기본 링크](#) / 호버링 / 방문 후
- 코드 인라인: `` `backticks` ``, `123`, `#3123`, `--flag=value`
- 키보드 입력: <kbd>CTRL</kbd> + <kbd>K</kbd>
- 작은 글씨: <small>Small text</small>

```c
#include <stdio.h>

int main(int argc, char** argv)
{
    printf("Hello, world!\n");

    return 0;
}
```

```python
from pwn import *

p = remote("host4.dreamhack.games", 10159)

p.recvline()
p.send(p64(0x40069C) * 30)

p.interactive()
```





수평선 아래 색도 확인 ↓

---

## 2) 리스트

- Bullet 1
  - Nested 1-1
    - Nested 1-1-1
- Bullet 2

1. Ordered 1
2. Ordered 2
   1. Sub 2-1
   2. Sub 2-2

- [ ] Task unchecked
- [x] Task checked

## 3) 블록 인용 / 경고 비슷한 박스

> “색 대비가 충분한지(AA/AAA) 꼭 확인하세요.” — Someone

<details>
  <summary>클릭/토글(Details)</summary>
  토글 콘텐츠의 배경/테두리/텍스트 색 확인.
</details>

## 4) 표 (Tables)

| 상태 | Primary | Secondary | Neutral |
|:----:|:-------:|:---------:|:------:|
| 500  | <span class="chip" style="background: rgb(var(--color-primary-500)); color:#000; padding:.2em .5em; border-radius:.4em;">P-500</span> | <span class="chip" style="background: rgb(var(--color-secondary-500)); color:#000; padding:.2em .5em; border-radius:.4em;">S-500</span> | <span class="chip" style="background: rgb(var(--color-neutral-500)); color:#fff; padding:.2em .5em; border-radius:.4em;">N-500</span> |
| 600  | <span class="chip" style="background: rgb(var(--color-primary-600)); color:#000; padding:.2em .5em; border-radius:.4em;">P-600</span> | <span class="chip" style="background: rgb(var(--color-secondary-600)); color:#fff; padding:.2em .5em; border-radius:.4em;">S-600</span> | <span class="chip" style="background: rgb(var(--color-neutral-600)); color:#fff; padding:.2em .5em; border-radius:.4em;">N-600</span> |
| 900  | <span class="chip" style="background: rgb(var(--color-primary-900)); color:#fff; padding:.2em .5em; border-radius:.4em;">P-900</span> | <span class="chip" style="background: rgb(var(--color-secondary-900)); color:#fff; padding:.2em .5em; border-radius:.4em;">S-900</span> | <span class="chip" style="background: rgb(var(--color-neutral-900)); color:#fff; padding:.2em .5em; border-radius:.4em;">N-900</span> |

> 위 표는 **테마 CSS 변수**(예: `--color-primary-500`)를 직접 사용하므로, 스킴이 제대로 적용됐는지 즉시 보입니다.

## 5) 코드(펜스) — 언어별 하이라이트

### (a) 언어 미지정 (Plain)