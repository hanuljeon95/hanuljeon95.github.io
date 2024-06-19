---
layout: post
mathjax: true
comments: true
title:  "연속체 가설을 중심으로 한 집합론의 역사"
date:   2020-06-11 03:33:00 +0900
categories: posts set-theory
tags: 
  - set-theory
published: true
---

*Summary in English: I will briefly explain the history of set theory, especially for the continuum hypothesis. Cantor's continuum hypothesis bears various topics like descriptive set theory, inner model theory, and forcing, and introduces a variety of viewpoints on the set-theoretic universe. I will briefly explain how they formed from the continuum hypothesis.*

*Acknowledgement: This post was a part of a proposal for a scholarship. I decided not to include this article in my proposal, and I instead post it on my website separately. I am grateful for Naehoon Kang, Hansol Jeon, Finn Lim, and Chanjin Lee for proofreading my proposal.*

-----

 1873년에 칸토어가 실수들의 집합과 자연수의 집합의 크기가 같지 않다는 것을 보인 것을 시작으로 기수란 개념의 도입과 함께 집합론이란 분야가 시작했고, 크로네커 등을 비롯한 몇몇 수학자의 반대에도 불구하고 모든 수학을 올려놓을 만한 기틀로써 각광받으며 뿌리내리기 시작한다. 하지만 그 뿌리내리는 과정이 마냥 순탄치는 않았다.

 가령, 1896년에 칸토어가 확립한 기수와 서수의 개념이 역설을 불러일으킴이 드러났다. 칸토어는 모든 서수들의 집합을 정의했고, 그 또한 정렬순서집합이 됨을 확인할 수 있었다. 만약 $\mathrm{Ord}$가 모든 서수들의 집합이고 $O$가 $\mathrm{Ord}$의 순서형을 대변하는 서수라 하면, $O+1\in \mathrm{Ord}$여야 한다. 하지만 이는 $O+1<O$임을 이끌어내서 모순이다. 이를 부랄리포르티 역설(Burali-Forti Paradox)이라 부른다.

 한편으로, 칸토어는 모든 기수 $\kappa$에 대해 $\kappa<2^\kappa$임을 보일 수 있었다. 만약 $C$가 모든 기수들의 집합이고 $\aleph=\sup C$이라 하자. 이 때 $\aleph<2^\aleph \in C$이므로 $\aleph<2^\aleph\le\aleph$여서 모순이 발생한다. 이를 칸토어의 역설이라 부른다.

 그리고 1901년에는 집합론뿐 아니라 프레게의 시도까지 좌절시킨 러셀의 역설이 발견되었다. 이러한 역설들은 칸토어가 상정한 소박한 집합론에 문제가 있단 공감대를 불러일으키기 충분했다.

 이 역설들을 해결하기 위해서  1908 에른스트 체르멜로(Ernst Zermelo)가 집합론의 공리를 제시했다. 체르멜로가 제시했던 공리는 다음과 같다:
- 외연공리 (Axiom of extensionality): 두 집합이 같은 원소를 가지면 두 집합은 같다.
- 공집합 공리 (Axiom of empty set): 공집합이 존재한다.
- 순서쌍 공리 (Axiom of pairing): 두 집합 $a$, $b$가 있을 때 $\\{a,b\\}$도 집합이다.
- 분리공리 (Axiom of separation): $a$가 집합이고 $P(x)$가 $a$의 모든 원소에 대해 명확히 주어진 성질(property)일 때 $\\{x\in a\mid P(x)\\}$도 집합이다.
- 멱집합 공리 (Axiom of power set): 집합 $a$가 있을 때 그 부분집합들의 집합 $\mathcal{P}(a)$도 집합이다.
- 합집합 공리 (Axiom of union): 집합 $a$의 모든 원소들의 합집합 $\bigcup a$도 집합이다.
- 선택공리 (Axiom of choice): 쌍마다 서로소인 집합들을 원소로 갖는 집합 $a$에 대해 어떤 집합 $b$가 있어 임의의 $c\in a$에 대해 $c\cap b$는 단원집합(singleton)이다.
- 무한공리 (Axiom of infintiy): 무한집합이 존재한다.

 하지만 위에서 '명확히 주어진 성질'이 무엇인가는 애매한 상태로 남아있었을 뿐 아니라, 해당 체계를 가지고는 가령 $\omega+\omega$의 존재성조차 보일 수 없었다. 1922년에 토랄프 스콜렘(Thoralf Skolem)과  아브라함 프렌켈(Abraham Fraenkel)이 '명확히 주어진 성질'을 '1차 논리로 표현되는 논리식'으로 정할 것을 제안했고, 추가적으로 다음 공리를 제안했다:
- 치환공리 (Axiom of replacement): $F$가 1차 술어 논리로 정의되는 함수 관계라 하자. 이 때 임의의 집합 $a$에 대해 $\\{F(x) \mid x\in a\\}$도 집합이다.

 이렇게 제시된 공리계를 체르멜로-프렌켈 집합론(ZFC)라 부르며, 이후에 정칙공리(Axiom of regularity)를 추가한 공리계가 표준적인 집합론 체계로 받아들여지고 있다.

-----

 다시 칸토어에 대한 이야기로 돌아가자. 칸토어가 집합론을 그 자체의 분야로서 연구하면서 무한서수와 무한기수에 초점을 맞추게 되었고, 그 와중에 실수 집합의 크기가 무엇이느냔 질문에 봉착한다. 칸토어는 알레프 수(Aleph number)라는, 모든 무한기수를 나열한 열을 포착해냈다. 제일 작은 무한기수는 $\aleph_0$이라 나타내어지고, 자연수 집합의 크기와 같다. 그 다음으로 큰 기수는 $\aleph_1$이고, 그 다음에는 또 $\aleph_2$가 있다. 하지만 칸토어는 이렇게 끝없는 알레프 수 중에서 실수 집합의 크기 $\mathfrak{c}$가  어떤 알레프 수에 대응하는 지는 알 수 없었다. 칸토어는 실수 집합의 크기 $\mathfrak{c}$가 $\aleph_1$일 것이라 추측했고, 이는 연속체 가설이란 이름이 붙게 된다. 칸토어는 연속체 가설을 풀지 못한 채 정신병원에서 삶을 마쳤고, 힐베르트가 세계 수학자 대회에서 23개의 풀어야 할 난제를 소개하면서 연속체 가설을 첫 번째 문제로 언급한 덕에 연속체 가설은 더 유명해졌다.

 그렇다고 칸토어의 시도가 완전히 헛된 것으로 끝난 것은 아니였다. 1884년에 그는 칸토어-벤딕슨 정리(Cantor-Bendixson theorem)을 증명한다:
> **정리.** $C\subseteq\mathbb{R}$이 닫힌 집합이라 하자. 그러면 $C$는 가산집합이거나 완전집합(perfect set)을 부분집합으로 포함한다.

여기서 완전집합은 모든 점이 해당 집합 위의 수열의 수렴값으로 주어지는 집합을 가리킨다. 완전집합의 크기는 항상 $\mathfrak{c}$이기 때문에, 이에 따르면 모든 닫힌 집합의 크기는 항상 $\aleph_0$이거나 $\mathfrak{c}$이다. 닫힌 집합의 크기라는 관점에서 보았을 때 가능한 크기가 둘밖에 없단 뜻이고, 이는 닫힌 집합에 대해서 연속체 가설이 성립한단 것으로 받아들여질 수 있다.
 칸토어는 이러한 증명을 실수 집합의 다른 부분집합에 대해서 일반화하려고 시도했지만, 칸토어가 이에 성공했단 증거는 없는 것처럼 보인다. 하지만 이후에 펠릭스 하우스도르프(Felix Hausdorff)가 1916년에 모든 보렐 집합에 대해서 연속체 가설이 성립함을 증명했다. 니콜라이 루진(Nikolai Luzin)이 1917년에 다음과 같이 정의되는 해석집합(Analytic set)에 대해 연속체 가설이 성립함을 보인다:
> **정의.** 집합 $A\subseteq \mathbb{R}$이 해석집합이란 것은 $A$가 어떤 보렐 집합의 연속함수에 의한 상(image)이라는 것이다.

 하지만 1965년이 될 때까지 더 이상의 진전은 없었다.

-----

 한편, 그와 별개로 서수와 기수 자체에 대한 연구도 계속 이뤄졌다. 힐베르트가 한 격언

> 무한! 이것만큼 사람의 관심을 근본적으로 흔드는 질문은 없었다. 
>
> (Das Unendliche hat wie keine andere Frage von jeher so tief das Gemüt der Menschen bewegt.)

에서도 알 수 있듯이, 무한 자체의 매력 때문에 연구가 진척되지 않았나 생각된다. 하우스도르프나 파울 말로(Paul Mahlo), 체르멜로 등에 의해 비교적 내적인 이유로 연구된 이 주제는 예상치 않게 측도론에서 그 모습을 드러낸다.

 앙리 르베그(Henri Lebesgue)가 실수 집합의 '길이'를 재기 위해서 측도론을 도입하고 르베그 측도를 정의했지만, 실수 집합의 모든 부분집합을 르베그 측도로 잴 수 있는 지 알 수 없었다. 르베그 측도를 잘 확장해서 가산가법성(countable additivity) 같은 좋은 성질을 유지하면서 모든 집합을 잴 수 있겠느냔 문제가 떠올랐지만, 이는 주세페 비탈리(Giuseppe Vitali)가 반례를 구성하면서 불가능함을 보였다. 
> **정리.** 다음 성질을 만족하는 함수 $\mu:\mathcal{P}(\mathbb{R})\to [0,\infty]$는 존재하지 않는다:
> 1. $\mu\neq 0$,
> 2. $\langle A_i\mid i<\omega\rangle$이 쌍마다 서로소인 가산 부분집합들의 열일 때 $\mu\left(\bigcup_iA_i\right)=\sum_i\mu(A_i)$이다.
> 3. 임의의 부분집합 $A$와 실수 $r$에 대해 $\mu(A) = \mu(A+r)$이다.

 스테판 바나흐(Stefan Banach)는 세 번째 조건을 $\mu(\\{a\\})=0$으로 약화시켰을 때 나머지 조건을 모두 만족하는 측도가 존재하느냐는 문제를 제기했다. 이 문제에서 $\mathbb{R}$을 다른 집합으로 쉽게 일반화시킬 수 있었고, 바나흐의 제자인 스타니스와프 울람(Stanislaw Ulam)이 1930년에 이 문제가 거대 기수와 연관지어져 있단 사실을 밝힌다: 특정 조건들을 만족하는 측도를 갖는 집합이 존재한다면, 그 집합의 기수는 약한 도달 불가능 기수여야 한단 것이다. 또한 그 집합의 기수는 실수 집합의 크기 $\mathfrak{c}$ 이하이거나, 가측 기수라 불리우는 매우 거대 기수여야 한단 사실 또한 알아냈다:

> **정리.** $\kappa$의 부분집합에 대해 다음 조건을 만족하는 측도 $\mu$가 존재한다고 하자:
>
> 1. $\mu\neq 0$,
> 2. $\langle A_i\mid i<\omega\rangle$이 쌍마다 서로소인 가산 부분집합들의 열일 때 $\mu\left(\bigcup_iA_i\right)=\sum_i\mu(A_i)$이다.
> 3. 임의의 $\xi\in\kappa$에 대해 $\mu(\\{\xi\\})=0$이다.
> 
> 그러면 $\kappa\le\mathfrak{c}$이거나 $\kappa$는 **가측 기수**이다. 즉, $\kappa$는 다음 조건을 만족하는 측도 $\mu$를 갖는다:
>
> 1. $\mu\neq 0$,
> 2. $\langle A_\xi\mid \xi<\gamma\rangle$이 쌍마다 서로소인 $\gamma<\kappa$개의 부분집합들의 열일 때 $\mu\left(\bigcup_{\xi<\gamma}A_\xi\right)=\sum_\xi\mu(A_\xi)$이다.
> 3. 임의의 $\xi\in\kappa$에 대해 $\mu(\\{\xi\\})=0$이다.

이후에 설명하겠지만, 가측 기수를 비롯한 거대 기수 역시 연속체 가설과 엮이게 된다.

------

 한동안 연속체 가설에 대해서는 추측과 틀린 증명만이 이어졌지만, 괴델 대에 이르러서 의미 있는 결과가 나왔다. 괴델은 상당한 플라톤주의자였다. 따라서 자신이 증명한 불완전성 정리가 수학의 불완전함을 의미한다고 생각하지 않았다. 도리어 그는 집합들로 이뤄진 집합론적 우주가 만족하는 '참인 공리'들을 찾아나감으로써 ZFC로부터 독립인 문제들을 증명할 수 있다고 생각했다.
 1938년에 괴델은 구성가능성 공리 ($V=L$)를 도입해서 연속체 가설을 증명했고, 새로 도입한 구성가능성 공리가 무한집합이라는 애매한 개념을 구체적으로 정립한다고 주장했다. 괴델의 구성가능성 공리는 내부 모형론(inner model theory)라 부르는, 주어진 집합론적 모형의 성질이 좋은 부분모형을 연구하는 중요한 분야의 시작점을 끊었다.

 괴델의 구성가능성 공리가 뭔지 알아보기 위해서 집합들의 모임의 구조를 알아보도록 하자. 집합들을 가지고 수학을 할 수 있다는 데에서 집합들의 모임을 수학자들의 관념이 거주하는 우주처럼 생각할 수 있고, 따라서 집합들의 모임 대신 '집합론적 우주'라는 표현을 쓰겠다. 우리들이 살고 있는 집합론적 우주는 다음과 같이 서수와 멱집합을 이용해서 '분해'할 수 있다:
- $V_0 = \varnothing$
- $V_{\alpha+1} = \mathcal{P}(V_\alpha)$,
- $V_\delta = \bigcup_{\alpha<\delta} V_\alpha$ ($\delta$가 극한서수일 때.)

 이렇게 구성된 집합열 $\langle V_\alpha : \alpha\in\mathrm{Ord}\rangle$을 **폰 노이만 계층** 혹은 누적 계층(cumulative hierarchy)이라 부른다. $V=\bigcup_{\alpha\in\mathrm{Ord}} V_\alpha$라 했을 때 모든 집합은 $V$의 원소이다. 즉, 모든 집합은 어떤 $V_\alpha$에 들어간다. 여기서 서수들의 모임 $\mathrm{Ord}$는 집합론적 우주의 '높이'를 결정하는 것처럼 볼 수 있고, 누적 계층을 구성하는 데 쓰인 멱집합 연산은 집합론적 우주의 '너비'를 결정하는 것처럼 생각할 수 있다.

 위의 방식 말고 다른 방식으로 집합론적 우주의 계층을 나눌 수 있을까? 괴델은 정의 가능성을 이용해서 이를 찾아냈다. 집합 $X$에 대해 $\operatorname{Def}(X)$를 $X$의 원소들로부터 정의 가능한 $X$의 부분집합들의 집합이라 하자. 이제 다음과 같이 주어지는 계층을 생각하자: 
- $L_0 = \varnothing$
- $L_{\alpha+1} = \operatorname{Def}(L_\alpha)$,
- $L_\delta = \bigcup_{\alpha<\delta} L_\alpha$ ($\delta$가 극한서수일 때.)

(참고로, $n$이 자연수이면 $V_n=L_n$이다. 따라서 $V_\omega=L_\omega$이다. 하지만 $V_{\omega+1}\neq L_{\omega+1}$이다.)

 $L=\bigcup_{\alpha\in\mathrm{Ord}} L_\alpha$라 정의했을 때 $L$을 **구성가능한 우주**(Constructible universe)라 부른다. 구성가능한 우주는 항상 ZFC의 모형이 된다고 알려져 있다. 그뿐 아니라 $L$은 항상 연속체 가설을 만족한다. 특히 모든 집합이 구성가능하면, 즉, $V=L$이 성립하면 연속체 가설이 성립한다.

> **정리.** $V=L$이 성립하면 연속체 가설이 성립한다.

 하지만 구성가능성 공리가 연속체 가설에 대한 괴델의 마음을 굳히진 못 했다. 1944년에 괴델은 연속체 가설이 원치 않는 해석학적 결과를 내놓는단 사실을 보고 생각을 바꾸었다. 괴델의 마음을 바꾼 문제는 강하게 측도 0인 집합(strongly measure zero set)에 대한 문제이다:

> **정의.** 어떤 집합 $A\subseteq\mathbb{R}$이 **강하게 측도 0**이라는 것은 임의의 가산 실수열 $\langle\varepsilon_n\mid n<\omega\rangle$에 대해 어떤 구간열 $\langle I_n\mid n<\omega\rangle$이 있어 $I_n$의 길이가 $\varepsilon_n$ 이하이고 $A\subseteq\bigcup_{n<\omega} I_n$인 것이다.

모든 가산집합은 강하게 측도 0인데, 그 역이 성립하느냐 물을 수 있다. 괴델은 그 역이 당연히 성립할 것이라 생각했지만, 연속체 가설을 가정하면 비가산 집합 중 강하게 측도 0인 집합을 찾을 수 있다. 따라서 괴델은 연속체 가설이 성립하지 않아야 한다고 생각했다. 하지만 ZFC의 모형 중 연속체 가설이 성립하는 것이 이미 있기 때문에, ZFC로부터 연속체 가설을 반증할 수는 없다. 따라서 괴델은 연속체 가설이 ZFC만을 가지고는 증명이 불가능할 것이라 추측했다.

-----

 괴델의 첫 추측을 증명한 것은 폴 코언(Paul Cohen)이다. 해석학자였던 그는 연속체 가설을 보고 집합론 연구에 뛰어들었고, 1963년에 강제법(forcing)이라는 새로운 기법을 도입해서 연속체 가설이 ZFC와 독립임을 증명하게 된다. 이 결과 덕분에 코언은 1966년에 필즈상을 받게 된다.

 코언의 강제법은 대충 말하자면, 기존의 집합론적 우주 $V$에 새로운 집합 $G$를 추가해서 새로운 우주 $V[G]$를 만들어내는 과정이라 할 수 있다. 조금 더 설명하자면, 강제법은 강제법 순서(forcing poset)이라 불리는, 추가할 집합 $G$의 부분적인 정보들을 담고 있는 순서집합으로부터 포괄적(generic)인 집합을 조립하는 과정이다. 코언은 자연수 집합의 부분집합을 $\aleph_2$개 추가할 수 있다는 것을 보임으로써 연속체 가설의 독립성을 보였다:

> **정리.** ZFC가 무모순하다면 ZFC + $2^{\aleph_0}\ge \aleph_2$ 역시 무모순하다. 따라서 ZFC + ￢CH 역시 무모순하다.

 코언의 결과 자체도 놀랄 만한 것이였지만, 코언의 강제법이 집합론이란 분야에 준 충격은 더 컸다. 코언의 강제법은 많은 집합론적 명제의 독립성을 증명하기 용이한 도구로 밝혀졌고, 코언의 발견을 시점으로 현대적인 집합론이 시작되었다.

 괴델은 한편으로, 거대 기수를 이용하면 연속체 가설의 진위를 결정할 수도 있을 것이란 희망을 표한다. 가령, 1961년에 데이나 스콧(Dana Scott)은 다음 사실을 보였다:

> **정리.** 가측 기수가 존재하면 $V\neq L$이다.

 $V=L$은 연속체 가설을 함의하므로, $V=L$을 연속체 가설을 강화한 정리라고 볼 수도 있다. $V=L$은 가측 기수의 존재성으로 반증되므로, 좀 더 강력한 거대 기수 공리를 가져 오면 연속체 가설도 반증할 수 있지 않을까 생각할 수 있을 것이다. 아이러니하게도 코언의 강제법은 괴델이 희망을 걸었던 거대 기수가 연속체 가설을 결정하기에 적당하지 않은 도구라는 사실 또한 드러냈다. 가령, 1967년에 아즈리엘 레비(Azriel Levy)와 솔로베이는 가측 기수를 이용해서 연속체 가설을 결정할 수 없다는 것을 보였다.

> **정리.** (Levy and Solovay) $\kappa$가 가측 기수이고 $P$가 $\vert P \vert <\kappa$를 만족하는 강제법 순서집합이라 하자. 만약 $G$가 $P$-범용 필터라면 $V[G]$ 위에서 $\kappa$는 여전히 가측 기수이다.

 여기서 '가측 기수'란 단어를 다른 거대 기수로 바꿔도 여전히 성립하고, 특히 $P$를 $\omega$에서 $2^{\aleph_0}$보다 작은 기수로 가는 **전사 함수**를 추가하는 강제법 순서집합으로 잡을 수 있다. 그 경우 $V$에서 $2^{\aleph_0}$보다 작은 기수들은 $V[G]$ 위에서 기수가 아니게 될 것이고, $V[G]$ 위에서 $2^{\aleph_0}=\aleph_1$이 될 것이다.

-----

 하지만 괴델의 예측이 아주 틀린 것도 아니였다. 루진의 해석집합을 좀 더 확장해서, 다음과 같이 주어지는 사영집합계층(Projective hierarchy)를 생각해보자:
- $\mathbf{\Sigma}^1_1$은 모든 해석집합들의 집합이다.
- $\mathbf{\Pi}^1_n = \\{ A\subseteq\mathbb{R} \mid \mathbb{R}\setminus A \in \mathbf{\Sigma}^1_1\\}$이다.
- $\mathbf{\Sigma}^1_{n+1}$은 어떤 $\mathbf{\Pi}^1_n$ 집합의 연속함수에 의한 상으로 주어진다.

 어떤 집합이 사영집합(Projective set)이란 것은 어떤 $n$에 대해 $A\in \mathbf{\Sigma}^1_n$이라는 것이다.

 루진이 1917년에 해석집합에 대해 연속체 가설이 성립함을 보인 이래로 진전이 없었는데, 1965년에 솔로베이가 가측 기수가 존재한다면 $\mathbf{\Sigma}^1_2$-집합에 대해 연속체 가설이 성립함을 보인다. 

> **정리.** (Solovay) 가측 기수가 존재한다고 가정하자. 만약 $A\in\mathbf{\Sigma}^1_2$이라면 $A$는 가산집합이거나 완전집합을 부분집합으로 가진다.

 그리고 1969년에는 도널드 마틴(Donald Martin)과 솔로베이가 가측 기수가 존재하면 $\mathbf{\Sigma}^1_3$-집합에 대해서 연속체 가설이 성립함을 보인다. 캘리포니아를 근거지로 둔 카발(Cabal) 학파는 마틴과 솔로베이의 논의를 계속 연장했다. 이윽고 1984년에 휴 우딘(Hugh Woodin)이 I0라고 알려진 굉장히 강력한 거대 기수 가정 하에서 사영결정공리(Axiom of projective determinacy)를 증명해낸다. 그리고 사영결정공리에 따르면, 모든 사영집합에 대해 연속체 가설이 성립한다. (다만 이후에 I0라는 전제는 약화된다.) 사실, 우딘은 좀 더 강력한 결과를 증명했다. 이를 알아보기 전에 다음 정의를 보자:

- $L_0(\mathbb{R}) = \mathbb{R}\cup\\{\mathbb{R}\\}$,
- $L_{\alpha+1}(\mathbb{R}) = \operatorname{Def}(L_\alpha(\mathbb{R}))$,
- $L_\delta(\mathbb{R}) = \bigcup_{\alpha<\delta} L_\alpha(\mathbb{R})$ ($\delta$가 극한서수일 때.)

 구성가능한 우주 $L$과 흡사하게 정의되는데, 차이점이라면 실수를 매개변수로 사용한 정의가 허용된다는 것이다. 우딘은 다음과 같은 사실을 보였다:

> **정리.** 만약 I0가 성립한다면 $\mathrm{AD}^{L(\mathbb{R})}$이다.

 즉, 우딘은 $L(\mathbb{R})$에 속한 모든 실수의 부분집합에 대해 결정공리가 성립함을 보였다. (여기서 결정공리가 무엇인지는 설명하지 않으려고 한다.) 특히 이로부터 $L(\mathbb{R})$에 속한 모든 실수의 부분집합에 대해 연속체 가설이 성립하며 르베그 가측이라는 결과가 나온다.

하지만 위에서 상술했듯, 거대 기수만을 가지고는 연속체 가설을 완전히 결정할 수 없다. 따라서 다른 도구가 등장하게 된다.

-----
 
 1988년에, 사하론 셸라흐(Saharon Shelah), 메나헴 마기도르(Menachem Magidor), 매튜 포어만(Matthew Foreman)에 의해 마틴의 최대(Martin's maximum)라는 공리가 소개된다. 마틴의 최대는 강제법 공리(forcing axiom)의 일종으로, 대략 '특정한 강제법을 이용해서 추가할 수 있는 집합은 이미 존재한다'는 주장을 하는 공리이다. 이는 일반위상 등 일반적인 수학에도 유의미한 결과를 내는 공리이기 때문에 저스틴 무어(Justin T. Moore)[14]나 스테보 토도르세비치(Stevo Todorčević)[15]와 같이 무한 조합론이나 일반위상 등도 같이 연구하는 집합론자들이 이 쪽을 지지한다. 특히나, 마틴의 최대는 연속체 가설을 부정하므로 이를 받아들이면 연속체 가설이 거짓이란 결론에 도달하게 된다.

 한편 1999년에 우딘은 Ω-논리와 스타 공리 (*)라는 개념을 다소 정교한 논의와 함께 도입했고, 스타 공리는 연속체 가설의 부정을 증명한다. 이를 기반으로 우딘은 연속체 가설이 거짓일 것이라 주장한다. 흥미롭게도, 우딘의 경우 내부 모형 이론과 관련된 논지 때문에 연속체 가설이 성립할 것 같다는 쪽으로 의견을 선회했다고 한다.

 하지만 카발 학파 등과 같이 연속체 가설이 결정 가능하다는 주장이 마냥 지배적인 견해인 것은 아니다. 강제법, 내부 모형 등의 방법은 기존의 집합론적 모형들로부터 새로운 모형을 만들어내는 과정이고, 그렇게 새로이 생겨난 '집합론적 우주'도 기존의 '우주'만큼이나 동등하게 존재론적 지위를 가진단, 집합론적 다중우주(set-theoretic multiverse)를 주장하는 의견이 나타났다. 

 가령, 셸라흐는 [9]에서 다음과 같은 발언을 통해 집합론적 우주가 유일하다기보단 다양하게 있을 것이란 주장을 했다: 
>  "내 심상은 ZFC를 포함하는 다양한 집합론이 있다고 말한다. 'ZFC의 우주'는 마치 '태양'같이 유일한 것이라기보단 '인류'나 '특정 국적을 가진 사람'과 같은 것으로 보인다. (...) 연속체 가설이 성립하느냐 묻는 것은 마치 '평범한 미국인이 카톨릭 교도인가?'를 묻는 것과 같다"
>
> My mental picture is that we have many possible set theories, all conforming to ZFC. I do not feel “a universe of ZFC” is like “the sun”, it is rather like “a human being” or “a human being of some fixed nationality” (...) You may think “does CH, i.e., $2^{\aleph_0} = \aleph_1$ hold?” being like “can a typical American be Catholic”.

 2012년에 조엘 데이비드 햄킨스(Joel David Hamkins)는 좀 더 극단적인 주장을 내놓았다. (자세한 논의는 [12]의 마지막 장이나 [16]을 참고할 것.) 비단 ZFC뿐 아니라 그보다 더 약한 집합론에 상응하는 집합론적 우주도 존재하며, 비록 집합론자들이 특정 모형을 편애할 수는 있을지언정 그 특정 모형이 다른 모형보다 더 집합론적이여야 할 이유는 없다고 주장했다.

-----

 연속체 가설에 대한 현재까지 이어지는 끊임없는 질문은 수학 내의 질문이라기보다는 수학 외의 질문처럼 보인다. 하지만 집합론과 수리논리학의 역사는 수학 밖에 있는 철학적인 논의를 안으로 끌어들이면서, 그리고 이걸 왜 신경쓰느냐 할 만한 것들을 대답하면서 성장했단 걸 염두해야 하지 않나 싶다.
 집합론이란 분야가 성장한 배경에는 이전에는 신경쓰지 않았던 기초론적 위기가 있었고, 칸토어 이전에는 실무한을 실재하는 수학적 개념으로 연구한 수학자가 거의 없었으며, 칸토어의 연구 이후에야 인류는 실무한이 무엇인지 제대로 이해할 수 있었다. 연속체 가설에 대해 신경 쓰지 않아도 수학을 하는 데 문제가 없겠지만, 이를 대답하려는 시도는 내부 모형론과 강제법과 같은 명제의 독립성을 증명할 때 쓸 수 있는 도구들을 낳았으며 이는 무한과 실수 집합, 그리고 집합으로 이뤄진 수학적 우주에 대한 인류의 이해를 더 깊게 하였다.

 지금 이어지는 연속체 가설에 대한 논의를 단순히 연속체 가설이 옳고 그르냐는 논의로 보기 보다는 집합론적 우주라는 개념을 이해하려는 시도의 일환, 그리고 집합론적 우주와 다중우주라는 개념을 이해하려는 시도의 초기 단계라고 봐야 하지 않을까 싶다. 그 시도의 결과가 무한과 집합론적 우주에 대해 어떤 설명을 하게 될 지 기대될 따름이다.

-----
참고문헌

[1] Amir D. Aczel, 무한의 신비. 신현용, 승영조 역. 승산, 2002.

[2] Kanamori, Akihiro. *The higher infinite: large cardinals in set theory from their beginnings.* Springer Science & Business Media, 2008.

[3] Maddy, Penelope. "Believing the axioms. I." *The Journal of Symbolic Logic* 53.2 (1988): 481-511.

[4] Maddy, Penelope. "Believing the axioms. II." *The Journal of Symbolic Logic* 53.3 (1988): 736-764.

[5] Ferreirós, José, "The Early Development of Set Theory", *The Stanford Encyclopedia of Philosophy* (Summer 2019 Edition), Edward N. Zalta (ed.), [https://plato.stanford.edu/archives/sum2019/entries/settheory-early](https://plato.stanford.edu/archives/sum2019/entries/settheory-early). Accessed 11 June 2020.

[6] Irvine, Andrew David and Deutsch, Harry, "Russell's Paradox", *The Stanford Encyclopedia of Philosophy* (Winter 2016 Edition), Edward N. Zalta (ed.), [https://plato.stanford.edu/archives/win2016/entries/russell-paradox](https://plato.stanford.edu/archives/win2016/entries/russell-paradox). Accessed 11 June 2020.

[7] Gödel, Kurt. "What is Cantor's continuum problem?." *The American Mathematical Monthly* 54.9 (1947): 515-525.

[8] Rittberg, Colin J. "How Woodin changed his mind: new thoughts on the Continuum Hypothesis." *Archive for History of Exact Sciences* 69.2 (2015): 125-151.

[9] Shelah, Saharon. "Logical dreams." *arXiv preprint [math/0211398](https://arxiv.org/abs/math/0211398)* (2002).

[10] Shelah, Saharon. "The future of set theory." *arXiv preprint [math/0211397](https://arxiv.org/abs/math/0211397)* (2002).

[11] Antos, Carolin, et al. "Multiverse conceptions in set theory." *Synthese* 192.8 (2015): 2463-2488.

[12] Nik, Weaver. *Forcing for mathematicians*. World Scientific, 2014.

[13] Andrés E. Caicedo, "Why is the continuum hypothesis believed to be false by the majority of modern set theorists?", [https://math.stackexchange.com/q/499947](https://math.stackexchange.com/q/499947). Accessed 11 June 2020.

[14] Wolchover, Natalie. "To Settle Infinity Question, a New Law of Mathematics." *Quanta Magazine*, [https://www.quantamagazine.org/to-settle-infinity-question-a-new-law-of-mathematics-20131126](https://www.quantamagazine.org/to-settle-infinity-question-a-new-law-of-mathematics-20131126). Accessed 11 June 2020.

[15] Todorcevic, Stevo. "The power-set of ω1 and the continuum problem." *Talk given at the Harvard EFI Project in the Spring of 2012*. [https://logic.harvard.edu/Todorcevic_Structure4.pdf](https://logic.harvard.edu/Todorcevic_Structure4.pdf) Accessed 11 June 2020.

[16] Hamkins, Joel David. "The set-theoretic multiverse." *The Review of Symbolic Logic* 5.3 (2012): 416-449.