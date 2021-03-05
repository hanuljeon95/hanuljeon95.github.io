---
layout: post
mathjax: true
comments: true
title:  "어떻게 집합론을 공부할 것인가"
date:   2021-03-05 16:00:00 +0900
categories: posts  set-theory
tags: 
  - set-theory
  - education
published: true
---

*Summary in English: I will introduce references about set theory, and explain my experiences on how to study set theory.*

-------

인터넷을 가끔 돌아다니다 보면 집합론에 눈독들여서 공부하는 사람들을 보게 됩니다. 아쉽게도 한국에서는 집합론을 공부하는 사람이 없기 때문에, 한국어로는 원하는 정보를 찾기 힘든 경우가 대다수입니다. 따라서 부족하게나마 제가 아는 선에서 관련된 정보를 정리해보고자 합니다. 

참고: 해당 글은 불시에 업데이트될 수도 있습니다. 따라서 최신 내용의 반영을 위해 해당 글을 퍼갈 때는 링크만 걸어두기를 추천합니다. 

또한, 이 글은 연구 주제로서 집합론에 대해 초점을 맞춥니다. 즉, 대부분 국내 대학에서 '집합론'이라는 이름으로 열리는, 다른 분야 공부에 조금 도움이 될 만한 수준의 개괄적인 수준의 내용에 대해 설명은 하지만 그 부분을 주된 부분으로서 설명하지는 않습니다. 특히, 수학/철학/컴퓨터과학 (그 중 프로그래밍 언어론 따위) 외 분야를 공부하는 사람이 수학 공부를 위해 집합론을 살짝 보는 게 목적이라면 이 글이 별로 도움되지 않을 수도 있습니다.

**주의: 해당 글은 비록 몇몇 유관 분야에 대한 설명을 포함할 수 있으나 주로 집합론에 대해서 다룹니다. 즉, 집합론 외의 다른 분야에 대해서는 불충분하거나 설명이 전혀 없을 수 있습니다.**


## 기초적인 집합론
보통 이 레벨은 수학과가 있는 학부라면 과목이 개설될 것입니다. 하지만 서수나 선택공리에 대해서 제대로 다루지 않을 수도 있습니다. 유료로 파는 교재라면 다음을 생각해볼 수 있습니다:

1. *Elements of Set Theory* - Herbert B. Enderton.
   보통 한국에서 집합론 책을 추천하면 Pinter나 You-Feng Lin을 추천하지만, 제 생각에는 이 책을 보는 게 더 나을 것 같습니다. (Jech/Hrbacek는 이후에 설명하겠습니다.) 해당 교재는 Pinter나 You-Feng Lin이 다루는 내용보다 조금 더 나아간 수준의 내용을 다루고 있지만, Jech/Hrbacek에서 나오는 어려운 내용들은 안 다루고 설명이 좀 더 붙어 있다는 특징이 있습니다. Pinter는 아예 논리학과 척을 진 사람이고, You-Feng Lin은 일반위상을 하긴 했지만 논리학과 크게 연관된 연구를 한 것 같지 않단 것을 감안했을 때, 논리학자였던 Enderton이 쓴 책이 논리학으로서의 집합론의 관점을 좀 더 잘 담고 있지 않을까 생각합니다.

   번역본은 아예 없는 것으로 압니다만, 어차피 집합론을 더 공부하겠다면 영어는 피할 수 없는 운명입니다. (일본어가 유창하다면 일본 쪽 교재로 그 운명을 좀 늦출 수는 있습니다. 하지만 입문 단계부터 영어에 익숙해지는 편이 미래 공부를 위해서 좀 더 낫습니다.)

1. *Introduction to Set Theory* - Thomas Jech and Karel Hrbacek.
   몇몇 대학에서는 해당 교재로 집합론을 가르칩니다. 그런데 보통 이 교재는 중급자용 교재로 알려져 있습니다. 위의 Enderton과 비슷한 내용을 다루지만, Enderton보다는 설명이 좀 덜 친절하고 뒤에서 몇몇 심화 내용을 더 다룬다는 차이가 있습니다. 그런데 해당 책에 있는 Silver's theorem의 증명은 비추천합니다. 초등적이라고 하고 있지만 motivation은 더 일찍 나온 증명에서 왔기 때문에 이해하기 쉽지 않을 수 있습니다. 그 외의 내용은 볼 가치가 있습니다.

1. *Discovering Modern Set Theory* - Winfried Just and Martin Weese.
    이 책은 1권과 2권이 있는데, 2권은 중급자용 교재 정도에 가깝고 1권이 기초 수준에 해당합니다. 그래도 1권 난이도도 Jech/Hrbacek와 엇비슷한 것으로 보입니다. 2권은 대략 Kunen의 집합론 교재에서 forcing 이전에 해당하는 수준의 내용까지 다루는 것처럼 보입니다. 1권의 경우 집합론을 하는 데 필요한 논리학을 self-contain하고 있긴 한데, 경험상 해당 내용을 짧게 설명해주면 바로 이해하지 못 하는 사람이 의외로 있었기 때문에 그 부분이 충분하지 않을 수도 있습니다. 그 경우에는 후술할 논리학 교재 중 하나를 조금 공부하면 됩니다.


무료로 구할 수 있는 교재 중에서는 다음을 생각해볼 수 있을 듯합니다:

1. *[Open Logic Project](http://builds.openlogicproject.org/)*

    몇몇 논리학자들이 온라인상 배포되는 논리 입문서를 쓰는 프로젝트의 일환으로 나온 책인데, 제법 방대한 수준의 introductory level의 논리학 내용을 풀어뒀습니다. 모든 책의 모든 챕터를 다 읽을 필요는 없고, 집합론에 관심이 있다면 *Set Theory: An Open Introduction*에 집중하는 것이 좋습니다. (수리논리도 벌충해야겠다 싶으면 *Sets, Logic, Computation*도 읽어볼 만 합니다. 다만 역시 다 읽을 필요는 없고, 증명론에 관심이 없다면 8-9장을, 비표준 논리에 관심이 없다면 11장을 건너뛰면 됩니다.)
    
    해당 프로젝트 하에 있는 집합론 책은 Jech/Hrbacek보다 약간 쉬운 수준에서 내용을 다루고 있습니다. 이 정도라도 상위 집합론 내용을 배우기 위한 중간 징검다리 역할은 충분히 할 수 있습니다. 논조가 어느 정도 철학과를 위해 쓰여졌단 면도 고려해야겠지만, 그래봐야 책 내의 몇 개의 절이 수학적인 집합론과 다소 무관하단 정도로만 반영되어 있습니다.

1. 집합론의 직관적 접근과 공리적 이론 - 앨리스.
   
   맛있는 해석학을 쓴 앨리스가 쓴 책이 맞습니다. 원래 앨리스 (현재는 이슬비) 씨가 쓰려던 책은 총 4부작으로, 1부작이 고등학교 수학 리뷰, 3부작은 기초 집합론, 5부작이 맛있는 해석학, 7부작이 실해석학과 복소해석을 다루도록 계획되어 있었습니다. (홀수 번호로 매겼으므로 번호는 맞습니다.) 하지만 현재는 5부작인 맛있는 해석학만 남았고, 나머지 책은 검색해도 잘 나오지 않는 것 같습니다.
    
    전체적인 내용은 Pinter와 비슷했던 것 같습니다. 하지만 해당 책은 서수를 다루지 않습니다. 한국어로 된 무료 교재라는 이점은 있겠지만 현재는 배포하지 않으니 도움될 지는 모르겠습니다.

그 외의 교재를 알아보고 싶다면 Peter Smith의 [Teach Yourself Logic](https://www.logicmatters.net/tyl/)을 확인해보기를 추천합니다. 해당 글에서는 논리학 전 분야에 대한 입문 교재 리뷰를 하고 있으므로 문외한인 논리학 분야를 공부해보겠다고 하면 생각보다 참고할 만합니다.

## 올라가기 전 준비운동

우선 수리논리를 분명히 공부하고 넘어가야 합니다. 집합론을 연구할 때 거의 대부분의 세부분야에서 집합론의 모형을 어떤 형태로든 다루게 될 텐데, 수리논리 입문 수준의 지식이 없으면 그 부분에서 어려울 수 있습니다. 해당 과목은 (2020년 기준으로) 수학과에서는 연세대에서만 열리고 있고, 몇몇 철학과에서 해당 내용에 준하는 수준을 다루는 과목이 열릴 지도 모릅니다.

대략 알고 넘어가야 하는 내용은 다음과 같습니다: soundness theorem, completeness theorem, compactness theorem, incompleteness theorem. 다행히도, 불완전성 정리는 그 증명까지 세세하게 다 알 필요는 없습니다. 제2 불완전성 정리만 기억해도 집합론을 공부하는 데는 무리는 없습니다. 하지만 약간의 멋을 생각해서 아예 포기하고 싶진 않을 것 같습니다.

사용해볼 만한 교재로는 다음이 있습니다. 여기서 다루지 않은 교재들은 Teaching Yourself Logic에 있는 Book Notes를 참고해서 확인해보시면 될 것 같습니다.

1. *A Mathematical Introduction to Logic* - Herbert B. Enderton.

   연세대에서 해당 교재로 수리논리를 가르치고 있습니다. 제법 표준적으로 쓰이는 책인 것 같습니다. 완전성 정리와 컴팩트성 정리까지는 충실히 설명해뒀다는 점이 좋지만, 증명론과 불완전성 부분이 다소 부실하단 단점도 안고 있습니다. 모델론 부분에서는 현대대수를 모르면 예시 부족으로 고전할 수도 있는데, 그런 문제가 없는 논리학 교재가 있을 지 잘 모르겠습니다.

1. *Lecture Notes in Logic* - Yiannis N. Moschovakis.

   검색하면 나오는 강의 노트입니다. 링크는 [이 쪽을 참고하시면 됩니다.](https://www.math.ucla.edu/~ynm/lectures/lnl.pdf) Enderton보다는 조금 어려운 편이고, 대신 증명론과 불완전성 정리는 Enderton보다는 잘 다룬다는 특징이 있습니다. 하지만 강의자 도움이 없으면 혼자서 읽을 수 있는 내용인지는 잘 모르겠습니다.

1. *The Foundations of Mathematics* - Kenneth Kunen.

    이후에 나올 Kunen의 집합론 교재처럼, 이 책도 제법 상세하게 설명을 하고 있는 편입니다. 이 책에서 자체적으로 설명하는 집합론 지식도 적지 않다는 것도 특징입니다. 따라서 이 책을 쭉 본다면 별도로 집합론 책을 더 볼 필요는 없을 것입니다. 다만 이 책도 역시 증명론은 잘 안 다룹니다. 장 이름에 쓰여 있긴 한데 모형론적인 방법에 초점을 맞춥니다. 또한 여기서 나오는 계산가능성 이론 (책에서는 recursion theory라고 하고 있습니다) 역시 집합론 색채가 강하게 물들어 있는 편입니다.

## 집합론, 무엇을 하는가?

본격적으로 들어가기 위한 교재를 추천하기 전에, 집합론이라는 분야에서 무엇을 연구하는 지 간략하게나마 짚고 넘어가는 것이 좋을 것이라는 지적이 있어서 붙입니다.

대부분 대학에서 배우는 집합론 내용 (더 나아가, 수리논리 전반) 과 연구 수준의 내용의 괴리가 크다 보니, 어떤 연구가 이뤄지는 지 알기 힘든 경우가 많습니다. 다른 수학 분야라고 안 그러겠습니다마는, 적어도 집합론은 국내에서 현직으로 연구하는 사람이 없다 보니 문제가 더 커지는 것 같습니다. 다음 설명은 [뒤에서 링크한 Hamkins 교수님의 설명](https://math.stackexchange.com/a/25563/53976)과 Handbook을 많이 참고했습니다. 한편으로, 제가 모든 내용을 철저히 조사해서 작성한 것은 아니기 때문에 현재 연구 추이나 자세한 연구 주제를 잘 반영하지 못 했을 수도 있습니다.

* 강제법 (Forcing): 폴 코언(Paul Cohen)이 연속체 가설의 독립성을 증명하기 위해 확립한 이후 집합론에 굉장히 많은 발전을 가져온 도구이기도 합니다. 강제법을 매우 대충 설명하자면, 주어진 집합론적 모형 $V$와 forcing poset이라고 불리는, 그 안의 구성하려는 대상의 부분적인 정보들로 이뤄진 '설계도 집합' $\mathbb{P}\in V$으로부터 generic filter $G$를 생성해서 $V[G]$라는 새로운 집합론적 모형을 만들어내는 기법입니다.
    
   이것 자체만으로 단독 연구되는 경우도 적지 않지만, 다른 세부분야를 다룰 때 같이 나오는 경우가 더 많습니다. 독립성 증명을 할 때 꼭 필요한 기법이므로 집합론 세부분야 어디서나 나올 가능성이 있는 기법입니다.

* 거대 기수 (Large cardinals): 거대 기수는 거의 집합론의 역사와 같이 등장한 개념입니다. 거대 기수의 명확한 정의는 존재하지 않지만, 대략적으로 '$\mathsf{ZFC}$ 내에서는 그 존재성을 증명할 수 없고 있다고 가정할 시 $\mathsf{ZFC}$의 무모순성을 증명해내는 기수' 정도로 통용되며, 적지 않은 거대 기수는 반영 원리 (reflection principle)에 따라 정의되거나 그와 동치인 서술을 가집니다. 거대 기수 역시 독립성 증명을 할 때 많이 쓰이는데, 강제법과 달리 무모순성 강도 (consistency strength)를 끌어올린다는 특징이 있습니다. 거대 기수는 보통 무모순성 강도에 따라 선형적으로 나열되어 있다고 간주되며, 대략 $0^\sharp$의 존재성을 이끌어내느냐를 기준으로 small large cardinal과 large large cardinal으로 나눕니다. 보통 small large cardinal은 reflection principle을 이용한 서술을 가지고, large large cardinal은 elementary embedding이나 ultrapower를 이용한 기술을 많이 사용합니다. 한편으로 Reinhardt가 도입한 Reinhardt cardinal이라는 것이 있는데, Kunen이 선택공리를 가정하면 이가 존재할 수 없음을 보였습니다:
      
     > **정리.** (Kunen's inconsistency theorem, $\mathsf{ZFC}$) $j:V\prec V$인 elementary embedding $j$는 존재할 수 없다.
     
    거대 기수 자체를 연구하는 기류도 여전히 존재합니다. 특히 최근에는, Gabriel Goldberg와 Farmer Schultzenberg를 위시해서 Reinhardt cardinal 같은 choiceless large cardinal이 연구되고 있습니다.


* 내모형론 (inner model theory): 거대 기수를 써서 독립성 증명을 했는데, 그렇게 사용한 거대 기수가 최적이 아닐 수도 있습니다. 더 약한 가정만으로 충분할 수도 있는데, 어느 정도 강한 거대 기수로 충분할 지 알고 싶다면 독립성을 보인 명제로부터 특정한 거대 기수의 존재성이 무모순함을 이끌어낼 수 있어야 합니다. 이 때 등장하는 것이 내모형론입니다.
     
    보다 구체적으로, 내모형론은 $V$의 부분모형(submodel) 중 잘 정의되고 성질이 좋은 것을 다룹니다 . (여기서 성질이 좋다는 건 가령 $\mathsf{GCH}$와 global choice를 만족한다, $\diamondsuit$를 만족한다 등 여러 가지를 언급할 수 있겠지만, 제가 이 쪽으로 잘 알지 못 하므로 더 언급을 피하겠습니다.) 괴델이 연속체 가설의 무모순성을 보이기 위해서 괴델의 구성가능성 모형 (constructible universe) $L$을 도입한 것이 시초인데, 아쉽게도 $L$은 가측 기수 (measurable cardinal)보다 강한 거대 기수는 못 받아들입니다. 따라서 $L$을 일반화하면서 가측 기수보다 더 거대한 기수를 받아들일 수 있는 모형을 연구하는 것이 이 분야의 목적이라 보면 될 것 같습니다. 또한, 내모형론은 결정공리 (axiom of determinacy) 및 $0^\sharp$의 일반화 따위와 엮여서 연구되는 것 같습니다. 한편으로는, 최근에는 집합론적 지질학 (set-theoretic geology)이라 불리는 forcing extension을 '거꾸로 되돌렸을 때' 얻어지는 모형도 내모형론적 관점에서 활발히 연구되는 듯했습니다.

* 선택공리 (Axiom of choice): 집합론의 역사에서 등장한 후 유구한 떡밥이였던 공리인데, 지금은 그냥 믿는 것 같습니다. 그렇다고 선택공리의 연구 가치가 떨어지는 것은 아닙니다. 선택공리를 얼마만큼 써야 하는가는 여전히 다뤄볼 만한 주제입니다. 특히, 선택공리를 사용할 수 없는 상황에서 얼마만큼의 선택공리가 필요할 것인가는 꽤 중요한 문제겠죠.
     
     선택공리를 연구하는 방향은 대략 두 가지일 것 같습니다: 주어진 명제가 어떤 형태의 선택공리꼴 명제와 동치인가, 그리고 주어진 선택공리꼴 명제의 독립성과 상호 관계를 보일 수 있겠는가. 전자는 증명하려는 명제가 어느 분야에서 왔느냐에 강하게 의존하는 주제입니다. 후자는 주로 symmetric model을 구성하거나 $\mathrm{HOD}$같은 모형을 이용하는 방식으로 이뤄집니다.

* 기수 연산 (Cardinal arithmetic): 아직도 이게 연구되느냐 할 수 있는데, 기수 연산은 $\mathsf{ZFC}$ 안에서 결정되지 않는 면이 많다 보니 아직도 다뤄지는 것 같습니다. Easton의 정리에 의해 정칙기수 (regular cardinal)의 지수 연산은 $\mathsf{ZFC}$ 내에서 통제 불가능함이 알려졌지만, Silver가 다음 사실을 증명해냅니다:
    
    > **정리.** $\kappa$가 비가산 공종도(cofinality)를 가지는 특이기수(singular cardinal)이라 하자. 만약 $\lambda<\kappa$인 모든 기수 $\lambda$에 대해 $2^\lambda=\lambda^+$이면 $2^\kappa=\kappa^+$이다.
      
     현재 연구되는 기수 연산이라 하면 특이기수와 뭔가 연관되어 있다고 생각하면 될 것 같습니다. 그리고 그 중 Shelah가 창시한 pcf 이론을 언급하지 않고 넘어가기는 힘들 것 같습니다. 이를 대략 설명하자면, $\mathsf{ZFC}$ 범위 내에서 통제 가능한 기수 연산을 다룬다고 보면 될 것 같습니다. pcf theory의 맥락에서 Shelah가 증명한 다음 결과는 꽤 유명합니다:
    
    > **정리.** 만약 $\aleph_\omega$가 강극한기수이면 $2^{\aleph_\omega}\le \aleph_{\omega_4}$이다.
     
     뒤의 $\aleph_{\omega_4}$를 $\aleph_{\omega_1}$까지 줄일 수 있을 것이라고 추측하고 있지만 아직 증명되지 않았습니다.


* 강제법 공리 (Forcing axioms): 강제법 공리는 대충 말하면, '특정한 강제법으로 추가할 수 있는 대상은 이미 존재한다'는 내용의 공리입니다. 아마 밑에서 소개할 교재 중 forcing을 처음 배울 때 쓰는 교재를 펼치면 백이면 백 Martin's axiom을 다루게 되는데, Martin's axiom이 강제법 공리의 제일 기초적인 형태입니다. (c.c.c.인 forcing이 generic filter를 갖는다는 형태로 진술됩니다.) 이를 좀 더 강화한 공리로 proper forcing axiom($\mathsf{PFA}$)과 Martin's maximum($\mathsf{MM}$) 따위가 있으며, 이 둘은 Martin's axiom과 달리 large cardinal과 연관되어 있습니다. 특히, proper forcing axiom이 supercompact cardinal의 존재성과 equiconsistent하느냐는 문제는 꽤 오랫동안 안 풀린 미해결 난제에 속합니다.
     
     요즘에 강제법 공리를 연구한다고 하면 가령 연속체 가설이나 Suslin tree의 존재성 등과 양립 가능한, $\mathsf{PFA}$의 약화를 다루는 것 같습니다. (그것만 다루지는 않겠지만 이 쪽은 아직 잘 모릅니다.) 뒤에서 나올 반영 원리와 연관되어서 다뤄지는 것 같았습니다.

* 반영 원리 (Reflection principles): 반영 원리는 대충 설명하면 '큰 모형에서 성립하면 어떤 작은 모형에서도 성립한다', 혹은 '큰 기수에 대해 성립하면 어떤 작은 기수에 대해서도 성립한다'는 형태의 진술입니다. 집합론을 제대로 배우기 시작한다면 나오는 Montague의 reflection principle이 대표적인 예시일 것 같습니다. 적지 않은 거대 기수가 반영 원리의 형태로 기술될 수 있고, 한편으로 stationary reflection같은 명제들은 강제법 공리나 $\diamondsuit$, $\square$같은 무한 조합론적 명제들과의 관계가 연구되는 것 같았습니다. 이 쪽도 현재 활발히 연구되는 주제로 보이지만, 역시 잘 모르므로 더 설명하기는 힘듭니다.

* Cardinal characteristic of the continuum: 역시 Shelah에 의해서 강하게 동력을 받았으며, Wien 대학에서 학파를 이뤄서 연구하는 것으로 압니다. 무한 조합론 혹은 다른 유관 분야에서 나올 법한 조합론적 기수들을 특성짓고, 그 기수들 간의 부등식과 등식이 $\mathsf{ZFC}$ 내에서 증명 가능할 지를 연구하는 분야라는 인상이 강합니다. (물론 이런 기수들은 연속체 가설을 가정하면 다 같아집니다. 하지만 이렇게 재미없는 경우는 상상하고 싶지 않겠죠.) 이 쪽 분야의 응용을 하나 제시해보라고 하면 여섯 명이 쓴 [The Rearrangement Number](https://arxiv.org/abs/1612.07830)가 있을 것 같은데, 대충 소개하자면 '무한히 많은 조건부 수렴 급수를 어떤 전단사함수들의 집합 $\mathcal{F}$에 따라 재정렬했을 때, 해당 급수들이 전부 수렴하게끔 하는 $\mathcal{F}$의 최소 크기는 얼마인가'를 묻는 내용으로 시적하는 것으로 압니다.

* 기술집합론 (Descriptive set theory): 보렐 집합 및 사영집합(Projective set)들의 복잡도를 분류한다는 인상이 강한 분야입니다. 통상적인 '순수 집합론'과 달리 해석학이나 일반위상에 더 가까운 느낌이 나고, 의외로 역사가 꽤 오래된 분야입니다. 당장 칸토어가 집합론을 시작한 계기도 푸리에 급수가 수렴하는 집합을 알아보는 것이였으니 기술집합론적 계기가 큽니다.
     
     이 쪽도 작은 분야가 아니라서 한 단어로 뭉뚱그리는 게 실례일 정도이지만, 제가 잘 몰라서 어쩔 수 없습니다. Effective descriptive set theory같은 세부분야는 아예 computability theory를 하는 사람들이 역수학(reverse mathematics)과 같이 연구한다는 인상이 강하고, determinacy와 sharp과 관련된 주제는 inner model theory를 하는 사람들이 연구하며, 그 응용은 집합론 밖을 벗어나서 동역학계나 측도론 등과 닿아 있는 것으로 압니다.

* Borel equivalence relations: 현재 제일 크게 팽창하고 있는 기술집합론 내의 분야일 것 같습니다. 말 그대로 동치관계 중 Borel set인 것을 연구하는데, 그런 동치관계의 복잡도를 분류하고, 다른 분야에서 자연스레 등장하는 보렐 동치관계를 연구하는 데 초점을 맞추고 있습니다. 이에 대해서는 [Matthew Foreman 교수님의 글을 인용하는 것으로](https://www.ams.org/journals/notices/201810/rnoti-p1263.pdf) 설명을 대신하려고 합니다.


## 자주 참고되는 집합론 교재들

제가 모든 책을 다 꼼꼼히 읽어 보고 작성한 것은 아님에 유의 바랍니다. 어디까지나 관련된 책들의 명단을 모아두었다는 느낌으로 작성했습니다. 특히, descriptive set theory와 관련된 문헌이나 좀 깊게 들어가야 알 수 있는 문헌들은 제가 내용을 파악하고 작성하지 못 했음을 밝혀 둡니다.

1. *Set theory*, Thomas Jech.
    그 엄청 두꺼운 Jech입니다. 초판본이 있고 21세기에 들어 새로 찍어낸 밀레니엄 판본이 있는데, 도서관에 있는 옛날 책을 뒤적이거나 할 게 아니면 보통 밀레니엄 판본을 보게 될 겁니다. 초판본에는 이해를 도울 만한 그림도 있는데 밀레니엄 판본에는 빠져버린 게 아쉽달까요.
    
    이 책으로 입문을 하는 건 보통 추천되지 않습니다. 왜냐면 직관적인 설명을 전혀 해 주고 있지 않기 때문입니다. 혹자의 말을 빌리자면, object language와 metalanguage의 구분도 잘 안 합니다. 하지만 다른 책에 비해 깔끔하게 서술되어 있고, 책을 중간부터 읽어도 배경지식만 있다면 무난하단 점 때문에 진짜 reference book의 역할은 잘 하는 것 같습니다. 그런데 집합론을 본격적으로 연구하겠다면 해당 책에 있는 내용은 진짜 입문에 해당하는 수준으로 보입니다. 그리고 해당 책은 기술집합론 (descriptive set theory)이나 조합론적 집합론에 대한 내용이 부족하단 단점이 있습니다. 세부분야 따지고 보면 어디든지 모자라긴 합니다마는, 저자 한 명이 모든 분야를 다 깊게 다룰 수는 없는 노릇이니깐요.

1. *Set Theory: An Introduction to Independence Proofs*, Kenneth Kunen.
   보통은 이 책으로 공부하는 게 많이 추천됩니다. 여타 교재와 달리 object language와 metalanguage의 차이, 몇몇 철학적 논의 등 초심자가 햇갈리기 좋은 논제도 잘 다루고 있다는 특징이 있습니다. 이름에서 알 수 있듯이, forcing을 다루는 게 주된 목표인 교재입니다. 참고로 옛날 판본과 새 판본의 내용과 구성이 많이 다르기 때문에 주의가 필요합니다. 구 판본은 설명과 연습문제가 나뉘어 있지만 새 판본에서는 섞여 있습니다. 그리고 새 판본은 cardinal characteristic of the continuum에 대한 내용을 조금 추가한 대신 constructible universe에 대한 내용이 다 빠졌습니다. 참고로 이 책의 구판본은 일본어 번역이 있습니다.

1. *Set Theory: Exploring Independence and Truth*, Ralf Schindler.
   이 책은 약간 의식의 흐름으로 쓰였다는 느낌을 받습니다. 비교적 어렵고 최근 내용까지 다루는 책 치고 연습문제가 충실하단 장점이 있습니다. 하지만 이 책도 내용이 초심자가 보기에는 깊다 보니 입문서적은 아닌 것 같습니다. 책의 구성도 설명보다는 증명에 치중했다는 느낌이 강하다는 점도 있습니다. 입문용으로 쓸 거면 강의자나 공부를 도울 사람이 있어야 하고, 그게 아니면 복습용으로 쓰면 될 것 같은 책 같습니다.

1. *Fast Track to Forcing*, Mirna Džamonja.
    비교적 최근에 나온 책이라서 저자 분의 추천을 받고 나서야 이런 책이 있다는 것을 알았습니다. (제 무지에 저자 분에게 죄송함을 표합니다.) Pure한 무한 조합론과 특이 기수 관련 분야 색채를 조금 받았다는 느낌이고, 중급자용 교재로 쓸 수 있어 보입니다. 기본적인 논리학도 안에서 설명해주긴 하지만, object theory와 metatheory의 구분을 해 주지는 않기 때문에 그 부분에서는 강의자의 도움이 필요할 수는 있어 보입니다. (사실 이 구분은 대부분 집합론 교재에서 잘 안 합니다.)

1. *The Higher Infinite*, Akihiro Kanamori.
   굉장히 미려한 문체로 관련 배경을 충실하게 설명하는 것으로 유명한 책입니다. (비단 이 책뿐 아니라 Kanamori 씨가 쓴 글들이 대체로 그렇습니다.) 영어가 잘 된다면 이 책을 읽는 게 굉장히 재밌을 것입니다. 이 책은 증명을 굉장히 세밀하게 해 뒀고, 깔끔하게 쓰였단 장점이 있지만 large cardinal과 관련된 내용이 아니면 설명하지 않았다는 문제가 있습니다. 따라서 관련된 배경 지식은 다른 데서 알아서 배워 와야 합니다. 그리고 descriptive set theory도 약간 야매로 설명한단 느낌이 있습니다. 하지만 이를 제대로 설명하려면 책이 두 배는 불어날 텐데, 물리적으로 집필 가능한 수준이 아니어 보인다는 것을 생각하면 이해 가능한 부분입니다.

    이 책도 일본어 번역본이 있습니다. 역시 미려한 말투로 쓰였다는 모양입니다. 그리고 이 책의 2권이 계획되어 있는데, 30년째 안 나왔습니다. 

1. *Constructibility*, Keith Devlin.
   Constructible universe와 관련 주제의 기초적인 내용을 세밀하게 썼다는 특징이 있습니다. 보통은 reference로 많이 쓰이는 듯한데, [초반부에 오류가 약간 있는 것으로 알고 있습니다.](https://mathoverflow.net/q/77734/48041) 그래도 관련된 다른 문헌 읽으면서 공부하다 막힌다 싶으면 이 책을 참고하는 게 도움이 되고는 합니다.

1. *Axiom of Choice*, Thomas Jech.
    선택공리에 대해 자세히 알아보고 싶다면 봐야 할 책 중 하나입니다. Symmetric model에 대해서 이 책만큼 자세히 다룬 책이 아마 거의 없을 것입니다. 다만 자세히 읽어보지는 않아서 저로서는 내용에 대해서 정확히 평가하긴 힘듭니다.

1. *Introduction to Cardinal Arithmetic*, Michael Holz, Karsten Steffens and Edmund Weitz.
     pcf theory를 처음 공부하겠다면 추천되는 교재로 보입니다. 집합론에 대해 많이 알지 못 해도 접근할 수 있게끔 쓰여져 있다는 게 특징입니다.

1. *Combinatorial Set Theory: With a Gentle Introduction to Forcing*, Lorenz J. Halbeisen.
   조합적 집합론과 선택공리에 대한 내용을 다루는데… 솔직히 선택공리 부분은 Jech의 Axiom of Choice를, 강제법에 대한 부분은 Kunen의 내용을 거의 가져왔다는 인상을 받습니다. 그리고 조합적 집합론을 전공하는 분의 말에 따르면 자기는 이 책을 추천하지 않는다더군요. 다만 다양한 종류의 characteristic과 forcing poset을 다루는 건 호평했던 것으로 기억합니다.

1. *Set Theory: On the Structure of the Real Line*, Tomek Bartoszynski and Haim Judah.
    역시 조합론적 집합론을 다루는데, 이름에서도 알 수 있듯이 cardinal characteristic of the continuum에 초점을 맞췄습니다. 해당 분야의 reference 정도로 보이는데, 역시 자세히 본 적은 없습니다.

1. *Forcing and the structure of the real line: the Bogotá lectures*, Jörg Brendle.
    Bogota note로 흔히 불리는 자료로, 책이라기보단 강의록입니다. 무한 조합론에서 자주 쓸 만한 forcing poset들을 요약해놓은 자료입니다.

1. *Classical Descriptive Set Theory*, Alexander Kechris.
    기술집합론에 대해서 배울 때 처음 읽는 책 정도일 것 같습니다. 집합론적인 사실을 해석학 등에 응용하는 데에 관심이 많다면 이 책을 먼저 보는 게 옳은 선택지이지 않을까 싶습니다. 뒤에서 상술할 Moschovakis와 달리 좀 더 concrete한 대상을 다룬다는 인상이였습니다.

1. *Descriptive Set Theory*, Yiannis N. Moschovakis.
    이 쪽은 거의 본 적이 없습니다만, Kechris보다는 좀 더 순수 집합론에 가까운 쪽에 초점이 맞춰진 것으로 압니다. (Kechris라고 관련 내용이 없지는 않겠지만요.) 

1. *Invariant descriptive set theory*, Su Gao.
     Borel equivalence relation에 대한 교재를 질문했을 때 추천받은 교재인데, 아쉽게도 아직 읽어보진 못 해서 내용은 잘 모릅니다. 하지만 이 쪽 분야가 워낙 최근에 뜨다 보니, 관련 정보 찾기가 쉽진 않을 듯해서 목록에 넣어둡니다.

1. *An Introduction to Itreated Ultrapowers*, John Steel.
    이 쪽도 강의록이고, 말 그대로 ultrapower와 그 일반화의 개괄과 관련된 강의록입니다. 아마도 inner model theory를 처음 시작할 때 쓸 만한 자료 치고 친절한 편인 것으로 보이지만, 오타가 많다는 단점이 있습니다.

1. *Handbook of Set theory* , Matthew Foreman and Akihiro Kanamori (editor.)

   Handbook에 대해 아시는 분이면 아시겠지만, 여러 저자가 각 chapter를 써서 모아둔 책입니다. 너무 방대해서 다 읽으라고 있기보단 필요한 부분을 보면 되는 형태의 책입니다. 각 chapter마다 평가가 상이하게 주어져야 할 것 같습니다. 하지만 일단 제가 본 chapter에 한해서는 괜찮았던 것 같습니다. 특히 Chapter 5는 cardinal characteristic of the continuum을 처음 배울 때 보기 좋은 문헌 중 하나입니다. (다른 하나는 Jörg Brendle의 Bogota note.) 각 chapter를 세부분야 입문 용도로 쓸 수는 있지만, 이 책을 전부 읽으려는 만용은 부리지 마시기 바랍니다. 2000쪽이 넘습니다.


## 공부는 어떻게 할 것인가?

해당 부분은 제 편향된 주관과 부족한 경험에 따라 쓰였기 때문에, 수시로 바뀔 수도 있고 모든 사람에 대해 정확히 적용되지 않을 여지가 큽니다. 그럼에도 책 목록만 딱 던져 주고 알아서 하면 잘 된다고 쓰는 것도 무책임한 것 같기 때문에 조금이나마 어떻게 공부할 지 적어보려고 합니다.

1. 일단 시간을 들여서 공부합시다.
     
   모든 공부에 적용되는 말입니다. 여기서 좀 더 중요한 점은, 수학 어느 분야나 마찬가지겠지만, 단시간에 엄청난 성과가 나진 않을 것입니다. 따라서 중도 포기나 절망하기 쉬울 텐데, 진짜 이해가 하고 싶다면 그 단계에서 접고 넘어가면 안 됩니다. 어떻게든 이해하려고 시도하고, 최대한 직관을 머릿속에서 그려보고, 연습문제를 풀어보고, 증명을 재현하면서 복습해봅시다. 단순무식한 방법이 모두 능사는 아니고, 좀 더 좋은 길이 있으면 이를 따라가는 게 좋겠지만, 이는 다른 사람이 알려주지 않는 한 알기 쉽지 않다는 문제가 있습니다. 누구한테 물어볼 엄두가 안 나면 일단 단순하게 나가는 수밖에 없습니다.
     
    다만 시간을 들이라는 것이 한 책만 뚫어져라 보라는 것은 아닙니다. 저조차 그러고 있다는 문제점이 있지만, 그렇게 하는 것은 보통 집중력이 흐트려져서 공부에 집중하지 못 하는 결론으로 이어지기 쉽습니다. 특히 공부하다 자주 막히면 그렇습니다. 그 경우엔 질문을 하거나, 공부해야 할 다른 분야를 보면서 관심을 잠깐 돌리거나, 과거의 문답을 참고하면서 전체적인 이미지를 그리는 등의 다른 일을 해 보기를 권합니다.
      
   원래 수학은 쉽지 않고, 공부해서 성과를 보려면 시간이 걸립니다. 1-2주 안에 이해가 안 된다고 절망하는 것은 보통 이릅니다.

1. 질문을 할 수 있으면 많이 합시다.
    
    아쉽게도 한국어를 가지고 그런 여건을 누릴 수 있는 사람은 거의 없습니다. 필수적으로 다른 외국어 (특히 영어)에 의존해야 할 것입니다. 그런 여건을 누리는 데 쓸 수 있는 언어로는 일단 유럽 내의 메이저 언어들과 히브리어, 페르시아어, 일본어, 중국어가 있습니다. 다른 언어권은 잘 모르겠습니다. 여하튼 한국어는 아직은 아닙니다. 그 탓에 구두로 질문할 여건은 잘 안 나므로, 이를 대체할 방법을 궁리해봅시다.
     
     Mathematics Stack Exchange와 Mathoverflow에 제법 많은 수준의 질문이 축적되어 있습니다. 다른 분야는 어떤 지 모르겠지만, 집합론의 경우에는 몇몇 분들이 열심히 활약해서 누적된 답변이 많습니다. (K모 씨라거나 C모 교수님, H모 교수님이나 B모 교수님, S모 씨 답변을 제일 많이 보게 될 겁니다. 좀 올라가면 더 보이겠지만 이하 생략. 여튼 생각보다 답변 다는 사람이 한정되어 있습니다.) 그 중에서는 제법 informal한 수준에서 motivation을 설명하는 경우도 많고, 막히는 detail을 설명하는 경우도 있습니다. 집합론의 추상성 안에서 길을 잃거나 엉뚱한 짓을 하고 싶지 않다면 informal한 답변을 많이 읽어 보는 것을 추천합니다. 이 분야가 뭘 하는 분야인지 대충 감을 잡을 수 있을 것입니다. 영어로 되어 있어서 읽기 힘들다고 생각할 수 있겠지만, 정 안 되면 번역기라도 사용하거나, 영어 공부를 좀 더 해서 영어 실력을 늘리는 수밖에 없습니다.
      
    직접 Mathematics Stack Exchange와 Mathoverflow에 질문을 할 수도 있을 것입니다. 그런데 이런 점은 주의하시기 바랍니다:
         
    * 질문만 딱 던지면 질문이 닫히거나 삭제되기 좋습니다. (충분히 어려운 질문이 아닌 한.) 그러니 왜 이해가 안 되고, 어디가 안 되는 지 충분히 서술하는 게 좋습니다. 영어가 부족해서 힘들다고 생각할 수 있지만, 특히 수학을 전공하겠다고 하면 질문을 쓰는 과정도 공부의 일종입니다.
    * Mathoverflow는 연구 수준의 질문을 하는 곳입니다. Enderton 읽다가 안 풀리는 문제가 생기면 질문 올리는 그런 데는 아닙니다. 그 구분을 잘 하는 게 좋은데, 자신이 없으면 Mathematics Stack Exchange에 우선 올리는 것도 방안입니다. Upvote만 잔뜩 찍히고 답변이 없다면 Mathoverflow에 cross-post하는 걸 고려해볼 수 있습니다.
    * 자신의 답변이 이미 답변된 질문은 아닌 지 충분히 검색해보시기 바랍니다. Stackexchange 자체 검색 엔진은 안 좋으므로 구글에 site:(사이트 주소)를 붙인 다음에 적절한 키워드를 넣어서 검색해보기를 추천합니다.
    * <strike> [성차별, 인종차별, 학력차별 등 차별적인 표현을 사용하지 맙시다.](https://twitter.com/hanuljeon95/status/1365699846926073866) </strike>
     
    한국어 사이트에 질문하는 것은 추천하지 않습니다. (수리논리 전반에 대해 그렇게 말하고 싶습니다.) 애초부터 수리논리 하는 사람이 너무 적어서 한국어 커뮤니티에서 그런 사람을 찾을 거라 기대하기 힘들고, 이미 있는 사람도 보통 철학이나 컴퓨터 과학을 하던 사람들일 겁니다. 그리고 관련 이슈에 답할 수 있는 사람이 온라인 커뮤니티에 있을 거란 보장은 더더욱 하기 힘듭니다.

1. 조금이라도 있는 기반을 최대한 활용합시다.
         
    이 부분에 대해서 구체적으로 쓰는 것은 제 주변 분들에게 민폐일 수도 있을 것 같아서 삼가려고 합니다. 하지만 충분히 생각해보고 의지가 강하다면 무슨 뜻인지 알 수 있을 것이라 생각합니다.


## 그 외로 더 볼 만한 글

집합론 및 수리논리 공부에 대해 참고할 만한 글 목록을 정리해둡니다.

### Teaching Yourself Logic

컴퓨터 과학 쪽으로의 설명이 부족하단 문제는 있지만 관련 분야 전반을 잘 review한 글이 이것 외에는 거의 없단 것이 현실인 것 같습니다. 또한 기초적인 개념에 대해서는 자체적인 설명도 하고 있으니 참고할 만합니다.

1. Peter Smith, *Teaching Yourself Logic*. Available at https://www.logicmatters.net/tyl/

### Some online resourses about the outline of set theory

(Possibly be updated without any notification.)

1. Asaf Karagila, *The five wh's of set theory (and a bit more)*. Available on https://ests.files.wordpress.com/2016/01/note1.pdf
1. Joel David Hamkins, *What are the issues in modern set theory?* Available on [https://math.stackexchange.com/a/25563](https://math.stackexchange.com/a/25563/53976)
1. Joan Bagaria, *Set Theory*. Available on [https://plato.stanford.edu/entries/set-theory/](https://plato.stanford.edu/entries/set-theory/)
1. *Exploring the Frontiers of Incompleteness*. Available at [http://logic.harvard.edu/efi.php](http://logic.harvard.edu/efi.php)


### Some references about set theory and logic in Korean
1. Joan Bagaria, *집합론*, at *The Princeton Companion to Mathematics*. Timothy Gowers, J. Barrow-Green, I. Leader (eds.) (Translated by 금종해, 정경훈, 권혜승.) 승산.
1. 기하서, *괴델과 집합론*, at *Gӧdel탄생백주년기념학술대회: 왜 괴델인가?* Available on [http://web.yonsei.ac.kr/bkim/preprints/%EC%99%9C%EA%B4%B4%EB%8D%B8.hwp](http://web.yonsei.ac.kr/bkim/preprints/%EC%99%9C%EA%B4%B4%EB%8D%B8.hwp)
1. 김병한, *괴델과 그의 불완전성 정리*, at *Gӧdel탄생백주년기념학술대회: 왜 괴델인가?* Available on [http://web.yonsei.ac.kr/bkim/preprints/%EC%99%9C%EA%B4%B4%EB%8D%B8.hwp](http://web.yonsei.ac.kr/bkim/preprints/%EC%99%9C%EA%B4%B4%EB%8D%B8.hwp)


## Acknowledgment

Many people helped me and suggested various materials for this article. I would like to thank Iian Smythe, Ivan Di Liberti, Mirna Džamonja, Jason Zesheng Chen, Burak Emir, Toby Meadows, and many others for their help.