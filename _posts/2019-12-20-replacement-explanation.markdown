---
layout: post
mathjax: true
comments: true
title:  "치환공리"
date:   2019-12-20 04:54:00 +0900
categories: posts set-theory
tags:
  - set-theory
---
*(Brief summary in English: This post is for explaining what Replacement is. First, I will review some descriptions of the axiom of replacement written in Korean. Then, I will explain the meaning of the axiom of replacement, its consequences and its equivalent forms.)*

[체르멜로-프렝켈 집합론](https://ko.wikipedia.org/wiki/%EC%B2%B4%EB%A5%B4%EB%A9%9C%EB%A1%9C-%ED%94%84%EB%A0%9D%EC%BC%88_%EC%A7%91%ED%95%A9%EB%A1%A0) (이하 ZF)을 다룰 때 언급되는 공리 중 하나로 치환공리가 있다. 치환공리의 형식적인 기술을 적자면 다음과 같다: 임의의 1차 술어식 $\phi(x,y)$에 대해 

$$\forall X (\forall x\in X\exists! y \phi(x,y) \to \exists Y\forall x\in X \exists y\in Y \phi(x,y))$$

인 것이다.

한국어로 된 집합론 컨텐츠 자체가 부족한 탓일까, ZF의 공리를 설명하는 글도 그렇게 많지 않다. 그 중 인터넷을 통해 쉽게 찾아볼 수 있는 자료라면 더더욱 적은 듯하다.

우선, 체르멜로-프렝켈 집합론이라고 검색하면 나오는 글들에서 치환공리를 어떻게 다루는지 보도록 하자. [위키백과의 경우엔 다음과 같이 서술하고 있다](https://ko.wikipedia.org/wiki/%EC%B2%B4%EB%A5%B4%EB%A9%9C%EB%A1%9C-%ED%94%84%EB%A0%9D%EC%BC%88_%EC%A7%91%ED%95%A9%EB%A1%A0#%EC%B9%98%ED%99%98_%EA%B3%B5%EB%A6%AC%EA%BC%B4):

> 치환 공리꼴에 따라, 어떤 논리식이 어떤 집합에서 함수 관계라면, 그 집합의 그 함수에 대한 상을 취할 수 있다.

그리고 우리들의 정보와 취소선, 장작의 보고인 [나무위키에선 이렇게 서술하고 있다](https://namu.wiki/w/ZFC%20%EA%B3%B5%EB%A6%AC%EA%B3%84?from=ZFC#s-2.9):

> 이 공리의 전건부는 $\phi(x,y)$가 각 $x$에 대해 $y$를 정확히 하나씩 대응시켜준다는 것을 뜻한다. 후건부는 $X$의 원소들에 대응되는 원소들의 집합 $Y$가 존재한다는 것이다. 이 때 $X$와 $Y$ 사이에는 일대일 대응이 존재하게 되므로 크기가 같게 된다.
> 
> 즉, 쉽게 말하자면 임의의 집합에 대해, 그 집합과 '같은 크기'의 모임은 집합이 될 수 있다는 것이다. 러셀의 역설 등에서 모순을 발생시키는 집합은 모두 크기가 너무 커서 문제를 일으키는 것이었으므로, 이 공리는 어떤 집합이 집합이 될 수 있을 정도로 크기가 '충분히 작다'면, 그 집합과 크기가 같은 모임도 집합이 될 수 있을 정도로 '충분히 작다'는 것을 말해준다.

비교적 최근에 [이상엽](https://www.youtube.com/channel/UC-7H7ZImLfGF97Y_EJ0vZzA) 씨란 분이 집합론에 대한 유튜브 강의를 했단 사실을 알았다. [그 분의 설명이 어떤 지 들어보자](https://youtu.be/0PJ4NJ-PGP0?t=2117). 

> (...) 여기에 아브라함 프렌켈이 치환공리를 추가시키면서 ZF라고 불리는 집합론을 완성시키는데, (중략) 치환공리꼴을 간단히 말씀드리자면, 두 개의 미지수 $x$, $y$를 갖는 논리식 $\phi(x,y)$가 있다고 합시다. $x$에 대해 $\phi$가 참이 되게 하는 $y$가 유일할 때, 그러한 $y$들의 집합이 존재한다는 것이 치환공리꼴입니다. 일종의 상집합이라고 할 수 있겠네요.
(원래 한 말에 약간 각색이 되어 있으니 참고할 것.)

개인적으로, 세 설명 다 문제점이 있는 같다. 우선, 위키백과의 설명은 크게 틀린 점은 없다. 다만 두 가지 점에서 아쉽다: 우선, 함수란 단어를 조금 분명히 했으면 좋았을 것이다. 
여기서 "함수"는 이산수학 시간에서 언급할 법한 두 집합의 곱집합의 부분집합이 아니다. 정의역에 대해선 집합일 것을 요구하고 있으나 공역에 대해서는 아무런 이야기도 없다. 공역이 proper class일 수도 있다는 것이다. (물론 치환공리가 그럴 가능성을 차단하긴 한다.)
두 번째로, 치환공리가 말하는 건 "사상의 상집합이 존재한다"가 전부이다시피 하다. 따라서 "치환공리꼴에 따라"라고 쓸 필요가 없다. 그냥 "치환공리는 이러한 것을 말한다"고 단도직입적으로 나가도 될 것이다.

나무위키의 설명은 우선 논리식부터 잘못 읽은 것처럼 보인다. $\forall x\in X \exists! y\phi(x,y)$는 $y$가 유일하단 주장뿐 아니라 **존재한다**는 주장 또한 포함하고 있다. 게다가, 나무위키의 주장과 달리 $\phi$로 주어지는 사상이 일대일이여야 할 이유가 없다.
그 이후로 나오는 말들은 전부 틀린 해석 위에 쌓인 주장이므로 타당성이 없단 걸 쉽게 미뤄볼 수 있을 것이다. 그럼에도 한 가지 더 지적하자면, 치환공리꼴은 러셀의 역설 등 "지나치게 큰 집합"의 등장을 막기 위해 도입된 공리가 아니다. 도리어 분류공리꼴의 power를 제한한 것이 역설들을 해소하기 위해 이뤄졌단 것에 가깝다.

유튜브 강의에서 나온 설명도 논리식을 잘못 읽은 면이 있다. 나무위키와 비슷하게 유일성만 언급하고 존재성을 빼 먹었다. 하지만 나무위키와 달리 사상이 일대일이란 결론을 내진 않는다. 어느 정도 공리를 이해하고 설명하려는 시도는 있었던 듯한데, 차라리 형식적인 기호를 들고 와서 서술했다면 조금 낫지 않았을까 싶어진다.

----

그러면 치환공리가 말하고자 하는 바는 무엇인가? 개인적으로 제일 와 닿았던 설명은 Jech의 기술[1]이였다:

> If a class $F$ is a function, then for every set $X$, $F[X]$ is a set.

물론 이 서술 자체가 치환공리인 것은 아니다. 왜냐면, 여기선 $F$가 모든 집합들의 class $V$ 위에서 정의되어 있을 것을 요구하기 때문이다. 하지만 이러한 문제는 쉽게 비껴갈 수 있다: $F$가 집합 $X$ 위에서 정의된 class function일 때

$$G(a) = \begin{cases} F(a) & \text{if $a\in X$,} \\ \varnothing & \text{otherwise.}\end{cases}$$

으로 두면 되기 때문이다. 

치환공리의 뜻을 풀어 쓰자면, **논리식으로 정의 가능한 class function**의 상집합(image)가 항상 존재한다는 것을 가리키는 명제이다. ZF 위에서 class란 개념은 논리식을 다른 방식으로 표현하는 방법일 뿐이란 걸 생각하면 그냥 class function이라고 해도 별 문제 없을 것이다.

사실 치환공리는 간단한 수준의 수학만 할 거라면 필요하지 않다. 우리들이 보통 하는 수학은 $\mathbb{R}$의 멱집합, 멱집합의 멱집합의 원소들 수준에서 다뤄지고, 그 정도 수준이면 치환공리가 없어도 충분히 다룰 수 있다. 하지만 무한 자체를 연구하기 시작하겠다면 이야기가 달라진다. 치환공리가 없으면 $\omega+\omega$란 서수가 존재한단 사실조차 증명할 수 없다![^1]

----

치환공리의 귀결에 대해서 이 글에서 길게 이야기하진 않으려고 한다. 치환공리를 어떻게 쓰는지 보고 싶다면 아무 집합론 책을 펴서 서수 단원을 보면 된다. 서수에 대한 사실은 치환공리가 없으면 증명할 수 없기 때문이다. 당장 "모든 정렬순서가 어떤 서수와 순서동형이다"란 사실도 치환공리를 요구한다.
하지만, 치환공리의 동치인 형태는 언급할 가치가 있는 듯해 이를 언급하고 글을 마치려고 한다.

치환공리의 다른 형태로 Axiom of collection이 있다. 공리 형태는 치환공리에서 $\exists!$를 단순히 $\exists$로 바꾼 형태를 취하고 있다:

$$\forall X (\forall x\in X\exists y \phi(x,y) \to \forall x\in X\exists y\in Y \phi(x,y)).$$

조금 informal한 용어를 빌려서 Collection을 다시 서술하자면 이렇다: $\langle \Phi_x \mid x\in X\rangle$를 class들의 족이라 하자. (즉, 각 $\Phi_x$가 class이다.) 이 때 집합족 $\langle \tilde{\Phi}_x \mid x\in X\rangle$이 존재해서 임의의 $x$에 대해 $\tilde{\Phi}_x\subset \Phi_x$을 만족한다.
작은 크기의 class족이 있을 때 이를 집합 크기 정도로 줄일 수 있다는 주장이라 해도 큰 무리는 없을 것이다.

Collection을 이용하면 치환공리를 증명할 수 있다. 증명 자체도 어렵지 않다. 놀랍게도, 역도 성립한다. 치환공리만 가지고도 Collection을 증명할 수 있다. 이 증명에는 정칙성 공리를 사용하며, 정칙성 공리를 사용하지 않는 증명이 있는 지는 잘 모르겠다.

치환공리의 다른 형태로 조금 비자명한 것으로, 반영 원리(reflection principle)가 있다. 반영 원리의 진술은 다음과 같다:
> 유한 개의 명제 $\phi_1$, $\cdots$, $\phi_n$에 대해 어떤 서수 $\alpha$가 있어 $\phi_1\land\cdots \phi_n \leftrightarrow V_\alpha\models\phi_1\land\cdots\land \phi_n$이다.

여기서 $V_\alpha\models\phi_1\land\cdots\land \phi_n$는 $V_\alpha$ 위에서 $\phi_1\land\cdots\land \phi_n$가 성립한단 의미이다. 특히나, $\phi_1$, $\cdots$, $\phi_n$이 ZF의 정리라면 $V_\alpha$는 $\phi_1\land\cdots\land \phi_n$를 만족시키게 된다.

반영 원리의 진술과 그 뒤에 숨겨져 있는 함정을 설명하려면 많은 사전지식을 요구하기 때문에 여기서 설명하진 않을 것이다. 하지만 반영 원리의 귀결을 짚고 넘어가지 않을 수 없다. 반영 원리를 이용하면 ZF가 유한 개의 공리로 공리화될 수 없음을 보일 수 있다.

**정리.** ZF는 유한 개의 공리로 공리화될 수 없다.

증명. 만약 그렇다고 가정하자. $\phi_1$, $\cdots$, $\phi_n$가 ZF를 공리화한다고 가정하자. 반영 원리에 의해, 어떤 $\alpha$가 있어 $V_\alpha\models \phi_1\land \cdots \phi_n$이다. 

이제 $\alpha$를 $V_\alpha\models \phi_1\land \cdots\land  \phi_n$를 만족하는 제일 작은 서수라 하자. 그러면 $V_\alpha$ 위에서의 반영 원리에 의해, 어떤 서수 $\beta\in V_\alpha$가 있어 $V_\beta\models \phi_1\land\cdots\land \phi_n$이다. 특히, 이 때 $\beta<\alpha$여야 한다. 이는 $\alpha$가 제일 작다는 가정에 모순된다.

Reference
---
[1] T. Jech. *Set theory*, Springer Science & Business Media, 2013.



----

[^1]: 증명이 불가능하단 사실을 어떻게 확인하느냐 물을 수 있다. 일반적인 방법을 설명하려면 글을 몇 개를 더 써야 할테니 자세한 이야기는 하지 않을 것이다. 이 경우엔, $V_{\omega+\omega}$가 체르멜로 집합론, 즉, ZF에서 치환공리를 제외한 이론을 만족시킴을 보일 수 있다. 또한 $\omega+\omega\notin V_{\omega+\omega}$이다. 요약하자면, $V_{\omega+\omega}$는 $\omega+\omega$의 존재성을 보일 수 없는 체르멜로 집합론의 *모형*이다.

