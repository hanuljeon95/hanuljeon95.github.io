---
layout: post
mathjax: true
comments: true
title:  "집합론을 잊어도 될까 — 반(反)논리학자 Halmos의 조언을 비평하며"
date:   2026-05-27 19:35 -0400
categories: posts 
tags: 
  - foundation of mathematics
published: true
---


### 서문

[어제 즈음에 트위터를 켜서 보다 누군가가 Halmos의 글을 인용하면서 집합론에 대해 '배우고 잊으라'](https://x.com/AstralDexter/status/2058602694785561073)는 이야기를 한 것을 보았다. 해당 서문을 우선 옮겨본다.

> This is not to say that the contents of this book are unusually difficult or profound. What is true is that the concepts are very general and very abstract, and that, therefore, they may take some getting used to. It is a mathematical truism, however, that the more generally a theorem applies, the less deep it is. The student’s task in learning set theory is to steep himself in unfamiliar but essentially shallow generalities till they become so familiar that they can be used with almost no conscious effort. In other words, general set theory is pretty trivial stuff really, but, if you want to be a mathematician, you need some, and here it is; read it, absorb it, and forget it. **P. R. H.**
> 
> 이것이 이 책의 내용이 유난히 어렵거나 심오하다는 뜻은 아닙니다. 사실인즉슨, 그 개념들이 매우 일반적이고 매우 추상적이라서, 결과적으로 익숙해지는 데 시간이 좀 걸릴 수 있다는 것입니다. 하지만 정리(theorem)가 더 일반적으로 적용될수록 그 깊이는 덜해진다는 것이 수학계의 자명한 이치입니다. 집합론을 배우는 학생에게 주어진 과제는 낯설지만 본질적으로는 얄팍한 일반적인 내용에 완전히 몰두해서, 의식적인 노력 없이도 거의 바로 사용할 수 있을 만큼 익숙해지도록 만드는 것입니다. 다시 말해, 일반 집합론은 정말이지 꽤나 사소한 내용에 불과하지만, 수학자가 되고 싶다면 어느 정도는 필요하며, 바로 여기에 필요한 내용들이 있습니다. 읽고, 흡수하고, 그리고 잊어버리십시오. **P. R. H.**

Halmos의 발언은 수학을 처음 공부하면서 거쳐가는 과정으로 집합론을 공부하는 사람에게 있어서 널리 받아들여지는 주장인 듯하다. 대부분 수학자들이 집합론 등 기초론적인 고민 없이 별 탈 없이 수학을 한다는 맥락에서 등장하는 조언일텐데, 개인적으로도 논리학 혹은 집합론 자체에 관심이 있는 것이 아니라면 집합론 공부에 너무 많은 노력을 쏟지는 말라고 권고하기도 한다. 하지만, "무언가를 하지 말라"는 조언은 필요에 의한 조언일 수도 있고 신념을 반영하는 조언일 수도 있으며, 이에 따라 해당 질문에서 이어질 가령 "집합론을 전공하고 싶어요" 라는 질문에 대한 답이 달라질 수 있다. 그런 의미에서, 저러한 조언을 쓴 Halmos가 집합론, 더 나아가 논리학에 어떤 태도를 갖고 있었는 지 살펴보는 것은, 그 조언을 그대로 받아들이기 전에 해 볼 만한 질문이다. 


### Paul Halmos는 누구인가

Paul Halmos는 20세기의 저명한 해석학자 중 한 명으로, 확률론, 에르고딕 이론, 함수해석 등을 연구하였다. 하지만 그와 함께, Halmos는 논리학과 비표준 해석학에 공공연히 적대적인 입장을 취한 것으로도 알려져 있다. 이는 그의 과거 발언과 행동들로 명확히 비쳐지는 것으로 보인다. 이는 Halmos의 발언과 행적에서 명백히 드러나는데, 해당 논문에서 Halmos의 논리학 및 비표준 해석학에 대한 태도를 체계적으로 정리한 바 있다.

> Piotr Błaszczyk et al., "A non-standard analysis of a cultural icon: The case of Paul Halmos." Logica Universalis 10 (2016), no. 4, 393-405.

이 논문은 그리 길지 않으며 [arXiv에도 공개되어 있다.](https://arxiv.org/abs/1607.00149) 해당 논문에서 제시하는 Halmos의 행적 몇 가지를 살펴보자. 첫째, 그의 범주론에 대한 태도이다. 그는 자신의 에세이 “Applied mathematics is bad mathematics”에서, 응용수학자가 범주론을 abstract nonsense라고 할 때 진심으로 말하는 것이라고 주장했다.[^1] 범주론자들이 자조적으로 사용하는 단어를 거꾸로 범주론을 폄하하는 데 사용한 셈이다. 둘째, 그의 논리학에 대한 태도이다. Halmos가 논리학 전반에 대해 가지고 있던 감정은 그가 1957년에 쓴[^2] 리머릭 (5행시의 일종)에 잘 반영되어 있다:

>If you think that your paper is vacuous,
>
>Use the first-order functional calculus.
>
>It then becomes logic,
>
> And, as if by magic,
>
> The obvious is hailed as miraculous.
> 
> 만약 논문에 아무 내용도 없다면,
>
> 일차 논리 체계를 집어 넣어봐라.
>
> 그렇게 논리학 논문이 되고,
>
> 그리고 마치 마법을 부린 듯이,
>
> 자명한 사실이 기적이라 칭송받게 된다.

해당 리머릭에서 읽을 수 있는 Halmos의 관점은, 논리학 논문에는 공허한 형식만 있고 실질적 내용이 없다는 주장일 것이다. 하지만 나중에 소개하겠지만, 논리학 내의 결과 중 기존의 관점을 뒤집은 결과는 적지 않다. 셋째, 비표준 해석학에 대한 발언이다.[^3] Halmos는 본인의 자서전에 비표준 해석학을 받아들인 동료 수학자들을 "전향자" (converts)로 묘사했으며, 자신의 제자인 에른스트 비숍(Errett Bishop)의 말의 인용하면서 그 반대파가 이를 "악마 숭배"로 간주한다고 썼다. 다소 당혹스러운 점은, Halmos가 인용한 비숍의 발언은 고전 수학 전반을 겨냥했지 비표준 해석학을 특정해서 겨냥한 적이 없다는 점이다. Halmos가 인용한 비숍의 주장은 비숍의 에세이인 "Schizophrenia in contemporary mathematics"에서 등장하는데, 비숍은 고전 수학을 가리켜 "깔끔한 악마"라 칭하며 공격하고 있으나, 그의 에세이에서는 비표준 해석학에 대한 이야기를 하고 있지 않다. Halmos의 비표준 해석학에 대한 논평에 대해 Piotr Błaszczyk 외는 다음과 같이 논평한다:

> Halmos’ description of both Nelson and Loeb as “converts” in the comment quoted above raises questions of motivation behind applying this kind of epithet to fellow leading mathematicians, or for that matter of invoking Errett Bishop on “devil worship,” remarks that are dangerously close to the category of expletives. 
>
> Halmos가 Nelson과 Loeb를 모두 "전향자"라고 묘사한 대목은, 동료이자 당대의 저명한 수학자들에게 그러한 호칭을 붙인 저의가 무엇인지, 나아가 Errett Bishop을 거론하며 "악마 숭배"라는 표현까지 동원한 것이 과연 합당한지에 대한 의문을 불러일으킵니다. 이는 자칫 욕설의 범주에까지 근접할 수 있는 위험천만한 발언이기 때문입니다. (Błaszczyk et al., p. 400–401)

이러한 맥락 속에서 Halmos의 서문을 다시 읽으면, "집합론을 배우고 잊으라"는 표현이 단순한 학습 전략으로만 들리지 않을 것이다. 논리학과 기초론 전반에 대한, "논리학이란 분야는 본질적으로 얕다"는 그의 사유의 연장선상에 놓인 발언으로 읽힐 수밖에 없다. 이는 집합론을 "거쳐가는 분야로서 가볍게 배워라"라고 말하는 것과 전혀 다른 주장이다.

불행하게도 이러한 시선은 Halmos에 국한된 시선이 아니라 수학계 전반에 퍼져 있는 문화이기도 하다. 적어도 수리논리를 하는 입장에서 익숙한 광경들이 있다. 분야가 철학과 컴퓨터과학에 걸쳐 있다는 입장 때문에 "당신이 하는 것은 수학이 아니라 철학이다"라는 말을 듣기도 한다. 중학교 수준, 혹은 학부 때 배운 논리학과 집합론만 상상하면서 분야 전체를 평가절하하는 시선도 마주하곤 한다. 연장선상에서 논리학이 새로운 지식을 창출하지 않는다는 주장, 그리고 추상적인 것을 "너무 깊게 공부하면 위험하다"는 주장도 이따금 들린다.


### "집합론을 정말 잊어도" 괜찮을까

하지만 이러한 주장들이 논리학 전체를 제대로 설명하고 있을까? 논리학 안에서는 수학이라 부를 수밖에 없는 세부분야도 엄연히 존재하며, 이러한 분야들은 수학 내 타 분야에서도 성과를 도출한 바 있다. Ehud Hrushovski는 모형론적인 방법을 이용해서 대수기하에 기여했으며, 이로 인해 모형론이 대수기하와 정수론에서도 어색하지 않게 등장하는 개념이 되었다. Ulrich Kohlenbach에 의해 발전한 proof mining은 증명론적인 방법들을 이용해서 비구성적으로 보이는 근사열 존재성 증명으로부터 근사열의 근사 속도를 알아내기도 했다. 러셀과 화이트헤드, 그리고 마틴뢰프(Martin-Löf)의 기초론적인 질문으로 시작해서 등장한 유형론(type theory)은 Rocq (구 Coq), Lean으로 대표되는 증명 보조기(proof assistant)의 기초를 형성하고 있으며, 수학의 형식화에 없어서는 안 되는 도구가 되었다. 혹자는 앞서 제시된 예시는 극히 일부의 사례에 불과하다고 주장할 지도 모른다. 또한 논리학이 타 분야에 비해 다른 수학 분야와 다소 고립되어 보이는 것은 어느 정도 사실같아 보인다. 하지만 이러한 주장은 순수수학 분야 전체에도 적용되는 주장이기도 하다. 대부분의 정수론 혹은 대수위상 연구들이 다른 곳에 바로 응용될 것이라 생각되지는 않는다. 그러한 비교가 타 분야에 비해 정당하게 이루어지고 있는가? 

설사 논리학이 수학 내 다른 분야에 전혀 기여하지 못 했다 하더라도, 논리학적 결과가 수학계에 던진 새로운 관점들조차 가치 없다고 말하기는 힘들 것이다. 논리학이 수학에 대해 제기한 중요한 화두 중 하나는, "수학적 진리의 경계가 어떤 공리를 받아들이냐에 따라 비자명하게 바뀔 수 있다"는 점일 것이다. 대부분 수학자들은 어떤 공리를 고르든 수학적 명제의 증명 가부 여부가 바뀌지 않을 것이라 생각하지만 그렇지 않다는 것이다. 쿠르트 괴델과 폴 코언 (Paul Cohen)은 연속체 가설이 ZFC만으로 결정 불가능함을 보인 바 있다. 하지만 연속체 가설보다 좀 더 "수학자들의 수학"에 근접하면서 좀 더 안 당연한, 르벡 가측 집합에 대한 사실을 들여다보려고 한다.

ZFC 위에서 르벡 비가측 집합이 있음을 보일 수 있다. 하지만 알려진 르벡 비가측 집합의 구성은 선택공리를 사용한다. 선택공리를 사용하지 않으면서 르벡 비가측 집합을 구성할 수 있을까? 그 답은 "그렇지 않다"이다. 로버트 솔로베이(Robert Solovay)는 르벡 비가측 집합의 구성에서 선택공리의 사용이 불가피함을 증명했다. 보다 정확히는, 솔로베이는 "ZFC + 도달 불가능한 기수 (inaccessible cardinal)[^4] 가 있다"가 무모순하면 "ZF + DC[^5] + 르벡 비가측 집합이 없다"도 무모순함을 보였다.[^6]

여기서 "그렇지 않다"라는 답이 생각보다 뒤틀린 양상을 보인다. "ZFC + 도달 불가능한 기수가 있다"는 ZFC의 범주를 벗어난다. 그렇다면 도달 불가능한 기수 없이 ZFC의 무모순성만으로 "ZF + DC + 르벡 비가측 집합이 없다"가 무모순함을 보일 수 있는가? 답은 그렇지 않다. 사하론 셸라흐(Saharon Shelah)는 "ZF + DC + 르벡 비가측 집합이 없다"가 무모순하면 "ZFC + 도달 불가능한 기수가 있다" 또한 무모순함을 보였다. 그럴 수 있다고 느낄 지도 모른다. 하지만 이를 이렇게 적으면 다소 충격적으로 들릴 수 있다: "ZFC가 도달 불가능한 기수가 없음을 증명한다면, 선택공리 없이 ZF + DC만으로도 르벡 비가측 집합이 있음을 증명할 수 있다." 다시 말하면, 르벡 비가측 집합을 구성할 때 선택공리가 필요할까라는 문제는 도달 불가능한 기수라는, 전혀 무관해 보이는 개념과 연결되어 있다.

이 사실이 시사하는 바는, "수학적 사실이 어디까지 사실인가"는 질문이 생각보다 공리계 의존적이라는 점이며, 특히 "무엇이 증명 불가능한가"라는 메타수학적인 주장조차 공리계 의존적이라는 것이다. 선택공리 없이 르벡 비가측 집합을 구성할 수 없다는 "사실"조차 굉장히 당연하지 않은 주제들을 숨기고 있다. 이러한 사실이 독자의 수학하는 방법을 당장 바꾸지는 않을 것이다. 하지만, 당연하게만 생각했던 "수학적 사실의 경계"가 생각보다 당연하게 주어지지 않는다는 점은 무시하기 힘들다. 이 사실을 입증해내는 데는 강제법 (forcing), 구성가능한 우주 (constructible universe), 거대 기수 (large cardinal) 등에 대해 적잖은 이해가 필요했다. Halmos가 리머릭에서 주장한 것과 다르게, 이러한 사실을 두고 논리학을 공허한 형식 놀이로 볼 수는 없을 것이다.


### 마무리지으며

수학자 중 일부가 논리학에 대해 취하는 태도를 볼 때마다 자연스럽게 비교되는 장면이 있다. 공학자가 수학자한테 "수학은 구체적인 것을 다루지 않으므로 가치가 없다", "수학자들은 모든 것을 너무 고리타분하게 따져서 아무 것도 못 한다", "수학을 너무 깊게 공부하는 것은 위험하다"라고 말하는 상황이다. 이에 대해 "분야의 가치와 방법론을 그 분야 밖의 수단으로만 평가해서는 안 되며" "무언가를 공부하는 것이 나쁘다고 평가하는 것이야말로 위험하다"고 반박할 수 있을 것이다. 모든 연구는 보통 내적인 기준을 가지고 있다는 데에서, 그리고 지적 흥미를 불필요한 이유에서 제한할 필요가 없다는 데서 이러한 비평이 일반적으로 합당하다고 생각한다. 그리고 이러한 반박은 논리학에도 적용된다.

(해당 글의 작성 시 AI의 도움을 받았으며, 그럼에도 글 전체가 AI에 의해 생성되지는 않았음을 밝힙니다.)

-----

[^1]: 좀 더 정확히는 다음과 같이 이야기했다: To many pure mathematicians applied mathematics is nothing but a bag of tricks, with no merit except that they work, and to many applied mathematicians much of pure mathematics deserves to be described as meaningless abstraction for its own sake with no merit at all. (I mention in passing that in moments of indulgent self-depreciation the students of one particular branch of pure mathematics, category theory, refer to their branch as "abstract nonsense"; applied mathematicians tend to refer to it the same way, and. they seem to mean it.) (출처: Halmos, P. “Applied mathematics is bad mathematics.” In Mathematics tomorrow, edited by Lynn Arthur Steen, Springer-Verlag, New York–Berlin, 9–20.)

[^2]: p. 216 of Halmos, P.: I want to be a mathematician. An automathography. Springer, New York (1985)

[^3]: 비표준 해석학의 발전사는 논리학의 발전사와 밀접한 연관이 있다. 비표준 해석학을 창시한 Abraham Robinson부터 논리학을 이용해 수학 내 다른 분야의 문제를 공략하는 데에 관심이 있었다. 따라서 Halmos의 비표준 해석학에 대한 태도를 논리학에 대한 태도와 연관짓는 것이 자연스러워 보인다.

[^4]: "도달 불가능한 기수 (inaccessible cardinal)가 있다"는 거대 기수 공리 (large cardinal axiom)의 일종이다. 여기서 그 정확한 진술을 알 필요는 없다. 도달 불가능한 기수의 존재성은 ZFC에서 증명도 반증도 할 수 없으며, "ZFC + 도달 불가능한 기수가 있다"가 ZFC의 무모순성을 증명한다는 관점에서, "ZFC + 도달 불가능한 기수가 있다"가 ZFC보다 훨씬 강력하다는 점만 기억하면 충분하다.

[^5]: DC는 종속 선택공리 (Dependent Choice)라고 불린다. 해석학을 하는 데 피하기 힘든 공리로 받아들여지고 있으며, 구성주의 수학의 관점에서도 자주 받아들여지는 약한 선택공리의 일종이다.

[^6]: 좀 더 정확히는, "ZFC + 도달 불가능한 기수가 있다"로부터 시작해서 ZF + DC + "모든 R의 부분집합이 르벡 가측이다"를 만족하는 class model을 구성했다. 또한, "ZFC + inaccessible cardinal이 있다"는 ZFC의 무모순성을 증명한다는 데서 ZFC보다 더 강력한 이론이며, 특히 ZFC는 inaccessible cardinal이 있음을 증명할 수 없다.

