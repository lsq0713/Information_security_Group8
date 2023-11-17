# Information_security_Group8
Fudan University's lesson:Introduction of Information Security(2023 autumn) Group 8' report
# 恩尼格玛密码机的破译[^0]

## 1. 技术概论

- **恩尼格玛密码机**（德语：Enigma，又译**恩尼格密码机**、**哑谜机**、**奇谜机**[[1\]](https://zh.wikipedia.org/wiki/恩尼格玛密码机#cite_note-1)或**谜式密码机**）是一种用于加密与解密文件的[密码机](https://zh.wikipedia.org/wiki/密码机)。确切地说，恩尼格玛是对二战时期[纳粹德国](https://zh.wikipedia.org/wiki/納粹德國)使用的一系列相似的[转子机械](https://zh.wikipedia.org/wiki/轉子機械)加解密机器的统称，它包括了许多不同的型号，为[密码学](https://zh.wikipedia.org/wiki/密碼學)[对称加密](https://zh.wikipedia.org/wiki/對稱密鑰加密)算法的[流加密](https://zh.wikipedia.org/wiki/流加密)。[^1]

- 恩尼格玛机原理：**（*需要通过一些方式展示和复现恩尼格玛机，画图或者代码模拟*）**
  - [恩尼格玛机的技术细节](https://web.archive.org/web/20150211030140/http://users.telenet.be/d.rijmenants/en/enigmatech.htm)
  
  - 油管上一个关于恩尼格玛机的3D动画，比较直观易懂：[恩尼格玛机如何工作](https://www.youtube.com/watch?v=ybkkiGtJmkM) B站上有相应的搬运及字幕[【油管搬运】恩尼格玛密码机的工作原理[含中文字幕]](【【油管搬运】恩尼格玛密码机的工作原理[含中文字幕]】https://www.bilibili.com/video/BV1r24y1f7DV?vd_source=a9e5405044d29a94540fd7741a011501)
  
  - 数学描述：恩尼格玛对每个字母的加密过程可以以数学的角度看作为一个[组合](https://zh.wikipedia.org/wiki/組合)过程。假设我们有一台德国陆军/空军版3转子恩尼格玛密码机，让P表示接线板的连线（plugboard），U表示反射器，L、M、R表示左（left）、中（middle）、右（right）转子。那么加密后的信息 **E**就可以表示成：$E=PRLMUL^{-1}M^{-1}R^{-1}P^{-1}E_0$
  
  - 代码实现：
  
    > >  Github上[恩尼格玛机模拟器]([justin-oxford/enigmamachine: An Enigma Machine Emulator (github.com)](https://github.com/justin-oxford/enigmamachine))，该项目中有实现恩尼格玛机的Python代码，并通过脚本在网页上实现了美观的展示***（但该项目中似乎并未实现插板交换字母的功能，或许可以试着寻找一些更原始优良的开源项目，由我们进行改进或者参考复现等进行展示）***
    >
    > > 知乎上也有类似的代码，比如[凯撒密码、多表加密、恩尼格玛——这些加密算法，都用Python实现！]([凯撒密码、多表加密、恩尼格玛——这些加密算法，都用Python实现！ - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/399811683))
  
- 恩尼格玛机的历史：***（这方面资料就很多了，无论是文章，书籍，或者视频，下面是一些比较原始权威的材料或者调查）***

  - 英国一位破译亲历者的著作，其中关于[考文垂轰炸]([考文垂大轰炸 - 维基百科，自由的百科全书 (wikipedia.org)](https://zh.wikipedia.org/wiki/考文垂大轟炸))的说法引起了诸多争论。Winterbotham, Frederick (1974). *The Ultra Secret*. London: Weidenfeld and Nicolson. [ISBN](https://en.wikipedia.org/wiki/ISBN_(identifier)) [0-297-76832-8](https://en.wikipedia.org/wiki/Special:BookSources/0-297-76832-8).
  - [恩尼格玛密码机的历史研究与复原 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/498400429)
  - 这方面搜集工作可做的较多，但实际意义不大。重点或许可以放在对称加密算法，流密码算法等，或许更有价值

## 2. 发展现状

- 我觉得这部分没必要纠结在恩尼格玛机上，可以从对称加密算法和流密码算法着手。这方面的内容书上便有介绍，
- 对称加密算法：[深入理解对称加密和非对称加密 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/377558391)里面有提到许多对称加密算法模型，或许可以从中选取比较典型的进行分析，与非对称算法比较等
- 流加密：[浅谈流加密算法和其应用(Chacha20-Poly1305) - 掘金 (juejin.cn)](https://juejin.cn/post/7239619891346276411)流加密作为对称加密算法的一种，上述模型中便有流加密算法的实现，块加密和流加密的比较或许可以体现其部分特点

## 3. 案例分析

- 波兰[时钟解码法](https://zh.wikipedia.org/w/index.php?title=时钟解码法&action=edit&redlink=1)
- [英国](https://zh.wikipedia.org/wiki/英国)[Banburismus解码法](https://zh.wikipedia.org/w/index.php?title=Banburismus解码法&action=edit&redlink=1)
- 现代技术下的解码方法

## 4. 总结与展望

- 恩尼格玛机作为古典密码和现代密码的过渡，从技术上可以进行一定分析
- 从历史和社会角度，恩尼格玛机从商用开端，随后在战争中大放异彩，对其的破译也催生着当代计算理论，电子技术与计算机的出现。
- 当下的加密算法发展趋势与其社会，国家战略等意义。

[^0]:本文中许多资料是通过维基百科相关延申，该技术本身并不难懂复杂，原理就算是中学生也很容易理解，我觉得真正有价值的是其中蕴含的对称加密和流加密的思想，在这方面挖掘或许才符合课程。另一方面作为机械和电子学结合的加密技术，恩尼格玛机也从一定程度上展示了从古典密码学到现代密码学的过渡，此方面可能是非技术层面上有价值值得发掘的地方。另一点是该加密技术的数学层面，可以从复杂度等与现代加密算法比较分析其相同点和不同点。
[^1]: [恩尼格玛密码机 - 维基百科，自由的百科全书 (wikipedia.org)](https://zh.wikipedia.org/wiki/恩尼格玛密码机)
