---
layout: post
title:  "Binary-Tree"
date:   2020-04-19 16:03:36 +0530
categories: DataStructure
---

이진트리와 이진탐색트리 등 그와 관련된 지식

## 이진 트리

이진트리란 자식노드의 개수가 최대 2개인 노드들로 구성된 트리를 말함

종류는 다음과 같다.

- Full Binary Tree

- Complete Binary Tree

- Blanced Binary Tree

정이진트리Full Binary Tree의 성질에는 다음과 같은 성질이 있다.

![](/assets/post/full_binary_tree.jpg)

### Level (i) 에서의 최대 노드의 수

i 레벨에서의 이진트리의 최대 노드수는 다음과 같다는 가정을 하자.

가정 : 레벨 i의 노드 수 = m = <img src="https://latex.codecogs.com/gif.latex?2^{i-1}" title="2^{i-1}" />


이진트리는 자식이 최대 두개이다.

모든 노드가 최대의 개수로 자식노드를 갖는다고 가정하자,
> 최대의 노드 수를 찾기 위함이다.

1. Level : 1 <br/>
루트 레벨에서는 단 하나의 루트 노드만이 존재하므로 1개가 존재한다
> 2^(1-1) = 2^(0) = 1 이므로 가정은 참이다.

2. Level : k<br/>
k 레벨에서는 위에 가정을 따르면, 다음과 같은 최대 노드개수를 갖는다
> 2^(k-1) 

3. Level : k+1<br/>
k+1 레벨에서는 위의 가정을 따르면, 다음과 같은 최대 노드개수를 갖는다
> 2^(k) 

여기서 이진트리의 성질 상, 

모든 노드는 자식을 최대 2개 이상 가질 수 없다고 하였다

그러므로 k레벨에 속하는 노드들이 가질 수 있는 자식의 개수는

k레벨에 속하는 노드의 개수를 m이라고 하였을 때, 2m 개이며,

m = 2^(k-1) 이므로 2m = 2^(k-1) x 2 이므로, 2^(k)를 만족한다.

고로 가정은 참이 된다.

그러므로 i레벨의 노드의 갯수 m  = <img src="https://latex.codecogs.com/gif.latex?2^{i-1}" title="2^{i-1}" /> 이다.

### Depth d 에서 이진트리의 최대 노드의 개수

가정 : Depth d에서 이진트리의 최대 노드의 개수는 <img src="https://latex.codecogs.com/gif.latex?2^{d}-1" title="2^{d}-1" /> 이다.

![](/assets/post/depth_d.JPG)

초항이 1이고, 등비가 2인 등비수열의 합을 구하는 간단한 공식은 다음과 같다.

다음과 같이 생각을 해보는 것이다.

![](/assets/post/binary_math.png)


~~~
고로 Depth 가 d인 이진트리의 최대 노드의 개수는  2^(d) - 1 이 된다
~~~

### n개의 노드를 가진 이진트리의 높이

위의 증명에서는,

이진트리의 노드의 개수를 n이라 하고,

높이를 h라고 했을 때,

둘의 상관관계를 다음과 같이 보였다.

~~~
n <= 2^h -1
~~~

양변에 +1을 취하고,

~~~
n +1 <= 2^h
~~~

양변에 log (base2)를 취하면

~~~
log(n+1) <= h
~~~

임을 만족하므로,

n에 대한 높이 h는 

~~~
log n <= h
~~~

다음을 만족한다


