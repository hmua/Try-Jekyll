---
tweets:
  - 2023-6-29:
    - 通商 通路 流通 干支通路
      背景好时惠及全民 背景坏时搜刮民脂
  - 2023-6-28:
    - 基本像个集合，基本前面的变动是集合中每个成员的定义
    - 🌙这些表象 都见过 都熟悉
      实际 表象之后在发生着什么？
  - 2023-6-27:
    - 盲人摸象 有人摸的鼻子 有人摸的耳朵 有人摸的牙
      有人摸的屁股 有人摸的尾巴
      各保存 描述各的讯息
  - 2023-6-26:
    - ♂利器 锐器 锋 刃 好钢 力气都花在准备这里
      传统技法 水滴
    - 从专业转向公共事业
      空间从私人领域转向公共领域
      新开发的庞大空旷的公共空间
      让固守私人领域失去价值 甚至成为累赘
---
{{site.posts|group_by:'date'}}✓
{{page.tweets}}✓

---
{%for a in page.tweets-%}
1. {{a}}
{%endfor%}
✓`for`迭代可以

---
{%for a in page.tweets-%}
{{a[0]}}|{{a[1]}}
{%endfor%}
`i[0]`和`i[1]`都无输出

---
{%for a in page.tweets-%}
{{a|first}}|{{a|last}}
{%endfor%}
`i|first`有输出

{{page.tweets|map:'first'}}
×但不支持`map:'first'`

---
{%assign a=page.tweets|map:'first'-%}
{{a}}×

---
{{a|join:', '}}

---
{%for i in a-%}
{{i}}|{{i|first}}|{{i|last}}
{%endfor%}
×map后可以for，但完全找输出，不到数据在哪