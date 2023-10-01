---
title: Integer
weight: 1
---

# Interger Representation

## 1 bits and Bytes

why binary?

- easy to realize
- `ENIAC`

32，64，x86-64

<img src="https://cdn.jsdelivr.net/gh/zvictorliu/typoraPics@main/img/image-20231001124156622.png" alt="image-20231001124156622" style="zoom:50%;" />

{{< details title="Extented" >}}

CPU指令集架构：Intel的x86架构（PC），ARM公司的arm架构（手机）

`x86`得名于Intel的CPU8086，现在一般指的是32位的架构（i386），但其实是一个系列，16、32、64都算

为升级64位，Intel开发了IA-64指令集，但不兼容32指令集，导致市场反响不好

而AMD公司开发的却兼容x86的指令集，叫做amd64，为大众接受

所以Intel也得采用amd64，但为了尊严改了个名字叫x86_64

所以是Intel叫x86_64，AMD叫amd64，都是64位指令集，有时也叫x64

win32和win64就单纯是以位来区分的，也就是说的32位、64位

{{< /details >}}

### logic

math $\rightarrow$ bit operation

- `& | ~`：从数学位的角度 `bit operation`
- `&& || !`：从C语言逻辑运算角度，`logic operation`，0为false，非0为true，只返回0或1
  - 小技巧：确保非空指针 `p && *p`

#### shift

算术、逻辑

若小于0或者超过字长：undefined behavior

#### unsigned, signed, 2's complement

转换时要注意一个比较大的数可能是有风险的

<img src="https://cdn.jsdelivr.net/gh/zvictorliu/typoraPics@main/img/image-20231001132444248.png" alt="image-20231001132444248" style="zoom:50%;" />



<img src="https://cdn.jsdelivr.net/gh/zvictorliu/typoraPics@main/img/image-20231001132521592.png" alt="image-20231001132521592" style="zoom:40%;" />

C语言可用后缀`U`表示unsigned

unsigned和signed同时操作时，会将signed转换为unsigned，改变理解方式
