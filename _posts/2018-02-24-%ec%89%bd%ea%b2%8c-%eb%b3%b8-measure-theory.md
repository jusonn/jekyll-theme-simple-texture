---
id: 726
title: 쉽게 본 Measure Theory ~ Probability
date: 2018-02-24T02:53:17+00:00
author: JuHyung Son
layout: post
permalink: '/%ec%89%bd%ea%b2%8c-%eb%b3%b8-measure-theory/'
image: /wp-content/uploads/2017/11/IMG_3818.jpg
tags:
   - Measure theory
   - probability
categories:
  - MATH
---

Youtube의 mathematical monk 채널을 구독 중입니다.
<h1>Measure Theory</h1>
<h2>Banach- Tarski Paradox</h2>
<img class="aligncenter size-full wp-image-730" src="http://dllab.xyz/wp-content/uploads/2018/02/445px-Banach-Tarski_Paradox.png" alt="" width="445" height="100" />

먼저 Measure가 무엇인지 직관적으로 보기 위해 바나흐-탈스키의 역설을 보자. 이 역설은 3차원 상의 공을 유한 개의 조각으로 자른 다음 늘리거나 변형하지 않고 재조합만 하면 원래 공과 같은 부피를 갖는 공 두 개를 만들 수 있다는 정리이다. 이 말도 안되는 상황을 증명하기 위해 바나흐의 탈스키는 체르멜로-프렝켈 집합론에서 선택 공리를 추가하여 증명했다고 한다. (ZFC set 이라고 한다.) 물론 이건 역설이다. 이것을 틀렸음을 증명하는데는 두가지 방법이 있다. 먼저 선택 공리(axiom of choice)라는 것을 제외하거나 공 조각들이 non-measurable set이라는 것을 증명하면 된다. 부피나 크기를 측정할 수 없다는 것이다. 조각들이 non-measurable이니 Borel set이 아니게 되고 그렇게 증명이 된다고 한다. 정확한 건 모르겠지만 그렇다고 한다. 이 부분에 대해 더 궁금하면 아래의 논문을 보자.

<a href="https://www.math.hmc.edu/~su/papers.dir/banachtarski.pdf">The Banach-Tarski Paradox 보기</a>
<h2>$\sigma$ - algebra</h2>
다음으로 $\sigma$ - algebra를 정의한다.
어떤 집합 $\Omega$가 있다면 $\Omega$에서 $\sigma$ - algebra는 $\Omega$의 power set에 공집합이 아닌 부분집합 A이고 다음 두 조건을 만족한다.
<ol>
 	<li>Closed under complements. $E \in A \rightarrow E ^ {c} \in A$</li>
 	<li>Closed under countable unions. $E _ {1} , E _ {2} …. \in A \rightarrow \bigcup E _ {i} \in A$</li>
</ol>
<h3>Ex</h3>
<ol>
 	<li>$A = \{ \varnothing , \Omega \}$ 가장 간단한 예제로 위의 모든 조건을 만족한다.</li>
 	<li>$A = \{ \varnothing, E, E ^ {c} , \Omega \} $</li>
</ol>
<h2>Measure</h2>
드디어 Measure의 정의를 보자. Measure는 $ \sigma$ - algebra A를 실수로 보내는 함수이고 다음의 두 조건을 만족한다.
<ol>
 	<li>공집합의 measure 는 0이다.</li>
 	<li>A의 부분집합 $E _ {i}$ 의 합집합의 measure는 $E _ {i}$의 measure의 합과 같다.</li>
</ol>
여기서 조건 2는 countable additivity 라고 불린다. 위의 정의를 수학적으로 표현해 좀 더 간결하게 나타낼 필요가 있다.

Def)
A measure $\mu$ on $\Omega$ with $\sigma$ - algebra A is a function $\mu : A \rightarrow [0, \infty ]$ such that
<ol>
 	<li>$\mu ( \varnothing) = 0$</li>
 	<li>$\mu (\bigcup E _ {i}) = \sum \mu ( E _ {i} ) $ for any $E _ {i} \in A$ of pairwise disjoint.</li>
</ol>
이렇게 measure가 정의 된다. Measure는 쉽게 어떤 집합의 부분 집합을 한 숫자로 보내는 함수이다. Size, volume, weight 같은 것들이 measure이다. 확률이 이 measure로 부터 정의되는데, 확률이 [0, 1]의 값을 가진다는 걸 알면 [0 무한]의 값을 가진 measure를 [0, 1]로 scaling하면 비슷하다는 걸 알 수 있다.
<h2>Probability</h2>
Def)
Probability measure is a measure P such that $P ( \Omega) = 1$
그리고 이 Probability measure는 통계학에서 배우는 확률의 조건들을 딱 들어맞는다. 확률은 kolmogrov에 의해 수학적으로 엄밀하게 정의되었다. 이후 확률은 도박사들이 하는 일종의 장난에서 학문의 반열로 올랐다는 얘기도 있다.
<h3>Ex)</h3>
위의 이론들을 가지고 흔히 배우는 확률을 기술해보자.
<ol>
 	<li>$\Omega = \{ 1, 2, …., n \} , ~ A = 2 ^ {\Omega} $이고 $P( \{ k \}) = P(k) = \frac {1} {n} \forall k \in \Omega $이라면 이 확률은 uniform 분포를 따른다.</li>
 	<li>$\Omega = \{1,2,… \}, ~ A = 2 ^ {\Omega} $ 이고 $P(k) =$ 동전 던질때 앞면이 나올 확률이라고 하면, 확률은 $a(1-a) ^ {k-1}$이다. 이 경우 확률은 geometric 분포를 따르게 된다.</li>
</ol>
<h2>Basic property of Measure</h2>
이 기본 정리는 여러 정리들을 증명하는데 쓰이는 정리이다.
$ ( \Omega , A , \mu) $ 가 measure space라고 하자. 그러면 다음 3가지 조건이 만족한다.
<ol>
 	<li>monotonicity: $E,F \in A$이고 $E \subset F$ 이면 $\mu (E) \leq \mu (F)$ 이다.</li>
 	<li>subadditivity: $E _ {1}, E _ {2}, … \in A$이면 $\mu ( \bigcup E) \leq \sum \mu (E)$</li>
 	<li>continuity from below: $E _ {1}, E _ {2}, … \in A$ 이고 $E _ {1} \subset E _ {2} \subset …$ 이면 $\mu ( \bigcup E) = lim \mu (E)$</li>
 	<li>continuity from above: $E _ {1}, E _ {2}, … \in A$ 이고 $E _ {1} \supset E _ {2} \supset … $ 이면 $ \mu (E _ {1} ) &lt; \infty $ 이면 $\mu ( \bigcap E) = lim \mu(E)$ 이다.</li>
</ol>
내가 하는 수준에서는 이 정리를 사용하여 무얼 증명하지는 않겠지만, 읽어보면 아주 당연한 정리이고 measure에 대해 이해를 도와준다.
<h2>Facts</h2>
다음 6가지 식은 아주 기본적인, 중요한 확률의 사실이다. 확률 수업이나 책 초반에 나오는 기본 정리이고 끝까지 나오는 정리이기도 하다.

Def)

Let $( \Omega , A, \epsilon) $ be probability measure space with $E, ~ F, ~ E _ {i} \in A$
<ol>
 	<li> $P(E \cup F) = P(E) + P(F) $ if $E \cap F = \varnothing$</li>
 	<li>$ P(E \cup F) = P(E) + P(F) - P( E \cap F) $</li>
 	<li>$ P(E) = 1 - P(E ^ {c}) $</li>
 	<li>$ P(E \cap F ^ {c} ) = P(E) - P( E \cap F ) $</li>
 	<li>$ P( \bigcap ^ {n} _ {i=1} E _ {i}) = \sum P ( E _ {i} - \sum _ {i &lt; j} P ( E _ {i} \cap F _ {j}) +....+ (-1) ^ {n+1} P (E _ {1} \cap .... \cap E _ {n} ) ) $</li>
 	<li>$P(\bigcup E _ {i}) \leq \sum P (E _ {i} ) and P (\bigcup E _ {i} ) \leq \sum P ( E _ {i} ) $</li>
</ol>
<h2>Measures on $ \mathbb{R} $ , $Borel ( \mathbb{R} )$</h2>
Borel measure는 모든 열린 집합에서 정의된 measure이다. 또한 Borel set은 열린 집합들로부터 연산하여 만들 수 있는 집합이다. 일반적으로 $ \mathbb{R} $ , $Borel ( \mathbb{R} )$ 는 단조함수를 이용해 특별한 형태로 바꿀 수 있다. 그리고 probability borel measure에서는 이것이 더 간단한 형태를 갖는다. 여기서 단조함수란 CDF를 말하는 것이다. Borel measure와 CDF의 Theorem을 각각 보자.

Def)

A Borel measure on $\mathbb{R}$ is a measure on $ ( \mathbb{R} , B( \mathbb{R} ) )$

&nbsp;

Thm)
<ol>
 	<li>If F is a CDF, then there is a unique borel probability measure on $ \mathbb{R} $ such that $ P( ( - \infty , x]) = F(x), ~ \forall x \in \mathbb{R} $</li>
 	<li>If P is a Borel probability measure on $ \mathbb{R} $ then there is a unique CDF $F$ such that $F(x) = P (( - \infty , x]) , ~ \forall x \in \mathbb{R}$</li>
</ol>
이 theorem에 의하면 CDF 와 Borel probability measure는 equivalent 즉, 동치관계이다. 그래서 CDF만 알면 그것의 PDF도 구할 수 있기 때문에 CDF는 매우 중요한 함수이다.