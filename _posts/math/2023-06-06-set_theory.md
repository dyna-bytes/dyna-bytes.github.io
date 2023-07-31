---
title:  "Relation and Partition"
categories:
  - math
---
# 관계와 분할
관계는 집합론에서 매우 중요한 내용 중 하나이다.
<br>
<br>
관계의 여러 기초 성질들을 다룬 후 정의 할 수 있는 **순서관계**는 순서집합(ordered set)과 상계, 하계 등의 개념을 정의하기 위해 꼭 필요한 개념이며, **동치관계**는 "같은 것을 '**같다**'"고 말하기 위해 반드시 정의해야 하는 개념이다.
<br>
<br>
한편, 분할은 관계를 설명할 때 꼭 함께 등장하는 개념이다. 분할은 관계에 의해 자연스럽게 존재하고 관계 역시 분할에 의해 자연스럽게 존재한다.
<br>
<br>
관계와 분할에 대해 알아보도록 하자.
<br>
<br>  

# 1. 관계
## 1.1. [DEF] 관계의 정의
데카르트 곱의 부분집합을 이용해 관계를 정의한다.
### (1) 관계 : $A \times B$의 부분집합
곱집합 $A \times B$의 부분집합 $R$을 $A$로부터 $B$로의 관계라 정의한다.  

$$
R = \{(x,\, y) \in A \times B\, |\, P(x, y)\},\; where\; P(x, y)\; is\;  Prospositional\; Function
$$ 

### (2) 정의역 : $Dom(R)$
적당한 $y \in B$에 대하여 ${}_x R_y$를 만족하는 모든 $x \in A$의 집합  

$$
Dom(R) := \{\forall x \in A |\, \exists y \in B \, s.t.\, {}_x R_y \}
$$  

### (3) 상 : $Im(R)$
적당한 $x \in A$에 대하여 ${}_x R_y$를 만족하는 모든 $y \in B$의 집합  

$$
Im(R) := \{\forall y \in B |\, \exists x \in A \, s.t.\, {}_x R_y \}
$$  

관계에서의 상(Image)은 치역(Range)라고도 한다.  

$$
Ran(R) = Im(R)
$$
  
위의 정의를 보면 함수에서의 그것과 유사한 것을 알 수 있다. 사실 함수 역시 관계를 이용해 정의한다.  
<br>
<br>

## 1.2. 관계의 성질
관계가 무엇인지 대충 알아봤으니, 관계의 성질들에 대해 알아보자. 
<br>
<br>
다음의 성질들은 관계를 다루는 데 있어 매우 중요하다. 다음의 성질들을 이용해 관계를 쉽게 분류하고 설명할 수 있다.
<br>
<br>
예를 들어, "어떤 관계 $R$은 ${}_x R_y$와 ${}_y R_x$를 동시에 만족하는 경우가 $x = y$ 일 때 밖에 없다" 고 말하는 대신 "어떤 관계 $R$은 반대칭성을 띄고 있다" 고 말할 수 있다.
<br>
<br>

### (1) 반사성(reflexive) : $\forall x \in A,\, {}_x R_x$ 를 만족
### (2) 대칭성(symmetric) : ${}_x R_y \Leftrightarrow {}_y R_x$ 를 만족
### (3) 반대칭성(anti-symmetric) : ${}_x R_y \wedge {}_y R_x \Rightarrow x = y$ 를 만족
### (4) 추이성(transitive) : ${}_x R_y \wedge {}_y R_z \Rightarrow {}_x R_z$ 를 만족
<br>  

이때, 반사적이고 대칭적이며 추이적인 관계를 **동치관계**라 하고, 반사적이고 반대칭적이며 추이적인 관계를 **순서관계**라 한다.
<br>
<br>
한편, 반사성의 정의에서 집합 $X$로부터 집합 $X$로 정의되는 관계를 볼 수 있다. 이러한 관계는 그냥 "집합 $X$에서의 관계" 라 한다.
<br>
<br>
집합 $X$에서의 관계 중 가장 작은 동치관계는 **대각관계**이며, 가장 큰 동치관계는 $A \times A$ 데카르트 곱 그 자체이다.

### * 대각관계 : $\Delta_A = \\{ (x, x) \in A \times A\, |\; _x R_x \\} $ 

<br>
<br>  

## 1.3. [DEF] 역관계와 합성 관계의 정의
함수와 비슷한 관계의 정의로부터 역관계나 합성관계를 떠올릴 수 있을 것이다. 당연히 역관계와 합성관계 역시 논의할 수 있다. 역관계와 합성관계를 알아보자.
<br>
### (1) 역관계 : $R^{-1}$  

$$
R^{-1} :=  \{ (y, x) \in B \times A\, |\, (x, y) \in R \}
$$  

### (2) 합성관계 : $S \cdot R$
세 집합 $A, B, C$와 두 관계 $R : A \rightarrow B,\, S : B \rightarrow C$ 에 대하여  

$$
S \cdot R := \{ (x, y)\, |\, \exists z \in B s.t. \, (x, z) \in R \wedge (z, y) \in S \}
$$  

<br>

## 1.4. [THM] 역관계와 합성 관계에 관한 정리
관계 $F, G, H$에 대해 다음이 성립한다.  

1. $(F^{-1})^{-1} = F$
2. $(H \cdot G) \cdot F = H \cdot (G \cdot F)$
3. $(G \cdot F)^{-1} = F^{-1} \cdot G^{-1}$

**[PROOF]**
<br>
정의를 이용하면 증명은 크게 어렵지 않다.  

1. 역관계의 정의를 그대로 이용한다.
<br>
$$
\begin{aligned}
(x, y) \in (F^{-1})^{-1} 
&\Leftrightarrow (y, x) \in F^{-1} \\
&\Leftrightarrow (x, y) \in F \quad \square
\end{aligned}
$$

2. 역시 합성 관계의 정의를 이용한다. 합성 관계를 찢어주고 다시 이어붙이면 된다.
<br>
$$
\begin{aligned}
(x, y) \in (H \cdot G) \cdot F 
&\Leftrightarrow \exists z,\; (x, z) \in F \wedge (z, y) \in (H \cdot G) \\
&\Leftrightarrow \exists z, w,\; (x, z) \in F \wedge (z, w) \in G \wedge (w, y) \in H \\
&\Leftrightarrow \exists w, \; (x, w) \in (G \cdot F) \wedge (w, y) \in H \\
&\Leftrightarrow (x, y) \in H \cdot (G \cdot F) \quad \square
\end{aligned}
$$

3. 역관계와 합성관계의 정의를 적절히 이용한다.
<br>
$$
\begin{aligned}
(x, y) \in (G \cdot F)^{-1} 
&\Leftrightarrow (y, x) \in (G \cdot F) \\
&\Leftrightarrow \exists z,\; (y, z) \in F \wedge (z,x) \in G \\
&\Leftrightarrow \exists z,\; (z, y) \in F^{-1} \wedge (x, z) \in G^{-1} \\
&\Leftrightarrow (x, y) \in (F^{-1} \cdot G^{-1}) \quad \square
\end{aligned}
$$
