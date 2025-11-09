---
title: "Quick Tips: Building a Stable Fuzzing Harness"
date: 2025-10-26T00:00:01
draft: false
summary: "크래시 발생 확률을 높이는 하네스 작성 팁 5가지에 대해서 설명합니다."
authors: ["JSec", "ssongk"]
tags: ["fuzzing", "harness", "tips"]
---

## 1) 본문 텍스트 & 인라인 스타일

일반 본문입니다. **볼드**, *이탤릭*, ~~스트라이크~~, <mark>형광펜(mark)</mark>, <u>밑줄</u>, <sub>아래첨자</sub>와 <sup>위첨자</sup>.

- 링크: [기본 링크](#) / 호버링 / 방문 후
- 코드 인라인: `` `backticks` ``, `123`, `#3123`, `--flag=value`

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

p = remote("test", 10159)

p.recvline()
p.send(p64(0x40069C))

p.interactive()
```



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

## 3) 인용

> “색 대비가 확인"


## 4) 표 (Tables)

| 상태 |                           Primary                            |                          Secondary                           |                           Neutral                            |
| :--: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| 500  | <span class="chip" style="background: rgb(var(--color-primary-500)); color:#000; padding:.2em .5em; border-radius:.4em;">P-500</span> | <span class="chip" style="background: rgb(var(--color-secondary-500)); color:#000; padding:.2em .5em; border-radius:.4em;">S-500</span> | <span class="chip" style="background: rgb(var(--color-neutral-500)); color:#fff; padding:.2em .5em; border-radius:.4em;">N-500</span> |
| 600  | <span class="chip" style="background: rgb(var(--color-primary-600)); color:#000; padding:.2em .5em; border-radius:.4em;">P-600</span> | <span class="chip" style="background: rgb(var(--color-secondary-600)); color:#fff; padding:.2em .5em; border-radius:.4em;">S-600</span> | <span class="chip" style="background: rgb(var(--color-neutral-600)); color:#fff; padding:.2em .5em; border-radius:.4em;">N-600</span> |
| 900  | <span class="chip" style="background: rgb(var(--color-primary-900)); color:#fff; padding:.2em .5em; border-radius:.4em;">P-900</span> | <span class="chip" style="background: rgb(var(--color-secondary-900)); color:#fff; padding:.2em .5em; border-radius:.4em;">S-900</span> | <span class="chip" style="background: rgb(var(--color-neutral-900)); color:#fff; padding:.2em .5em; border-radius:.4em;">N-900</span> |

