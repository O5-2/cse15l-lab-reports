# Lab Report 2
## Servers and SSH Keys (Week 3)

**Part 1:**

![Image](CSE15L_Lab2_1a.png)

![Image](CSE15L_Lab2_1b.png)

Which methods are called: `handleRequest` is called.

The relevant arguments and fields: `handleRequest`'s argument `url` (value `/add-message?s=Hello%20there`), `Handler`'s field `lines` (value `0`), `Handler`'s field `text` (value `""`)

Changes to relevant fields: `lines` becomes `1` and `text` becomes `"\n1. Hello there"`.

![Image](CSE15L_Lab2_1c.png)

Which methods are called: `handleRequest` is called.

The relevant arguments and fields: `handleRequest`'s argument `url` (value `/add-message?s=How%20are%20you%20doing?`), `Handler`'s field `lines` (value `1`), `Handler`'s field `text` (value `"\n1. Hello there"`)

Changes to relevant fields: `lines` becomes `2` and `text` becomes `"\n1. Hello there\n2. How are you doing?"`.

**Part 2:**

todo: image1

todo: image2

todo: image3
