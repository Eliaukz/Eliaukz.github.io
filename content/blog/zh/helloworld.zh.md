---
title: hello world
date: 2024-07-24 23:31:30
featured: true
math: trew
---

# hello world

$1 + 1 = 2$


$$
x + y = 10 \\
x - y = 6 \\
2x = 16 \\
x = 8 \\
y = 2
$$


$\hbar\frac
{\partial \psi}
{\partial t}
= \frac{-\hbar^2}{2m} \left(\frac{\partial^2}
{\partial x^2} + \frac{\partial^2}
{\partial y^2}+\frac{\partial^2}
{\partial z^2}
\right) \psi + V \psi$



```c

void
binit(void)
{
  struct buf *b;

  initlock(&bcache.lock, "bcache");

  // Create linked list of buffers
  bcache.head.prev = &bcache.head;
  bcache.head.next = &bcache.head;
  for(b = bcache.buf; b < bcache.buf+NBUF; b++){
    b->next = bcache.head.next;
    b->prev = &bcache.head;
    initsleeplock(&b->lock, "buffer");
    bcache.head.next->prev = b;
    bcache.head.next = b;
  }
}
```



> 对于传统数据库，搜索功能都是基于不同的索引方式

