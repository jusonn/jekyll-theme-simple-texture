---
title: Udacity AIND 후기
date: 2018-05-08
author: JuHyung Son
layout: post
tags:
  - udacity
  - review
categories:
  - Writing
---

2017년 9월에 시작한 AIND에 대한 후기입니다. 현재 AIND는 약간 개편이 되었다고 하네요.

# Artificial Intelligence Nano Degree

Udacity의 AIND 는 말 그대로 인공지능에 대해 공부를 합니다. Term1과 Term2, 두 파트로 나누어져 있고 Term1 은 현재 대세인 딥러닝 이전의 인공지능 기술들에 대해 배우고 Term2는 딥러닝에 초점이 맞춰져 있습니다. 저는 딥러닝을 좀 더 배우고 싶었지만 Term1에서 배우는 것들은 그렇게 잘 쓰이진 않는 거 같지만 Term1에서 배운 것들도 재미있었고 가치있는 것이었다고 생각합니다. 인공지능을 공부하는데 꽤 기초가 되는 개념들이었습니다. Term1 에서는 다음과 같은 프로젝트를 진행하며 공부합니다.
### 스도쿠 문제 풀기

rule based의 스도쿠를 푸는 프로그램은 만듭니다. 코딩을 잘한다면 별 무리없이 프로젝트를 끝낼 수 있습니다.

### Isolation 게임 에이전트 만들기

<div align="center"> <img src="/image/aind/1.png" /> </div>

isolation이라는 체스판에서 하는 게임 에이전트를 만듭니다. 요즘 게임 에이전트라 하면 강화학습이 떠오르지만 여기서 배우는 에이전트는 예전의 컴퓨터 체스 게이머 딥 블루와 같은 방식으로 만듭니다. 무한히 커지는 게임의 경우의 수에서 최선의 선택을 하는 검색 트리, loss 함수 모델링을 배우며 프로젝트를 진행하죠.

### Planning

<div align="center"> <img src="/image/aind/2.png" /> </div>

비행기의 이동 경로를 Planning을 이용해 구성하는 프로젝트입니다. 도시들이 있고 각각의 도시에는 목적지가 있는 화물들이 있습니다. 각각의 도시에서 어떤 경로로 비행기를 비용해 화물을 보내야 가장 최적인지를 보는 것입니다. 도시와 화물의 숫자가 조금만 늘어나도 모델에 따라서 900초가 넘는 꽤 많은 경우의 수가 나타납니다. 이번 프로젝트에서도 경우의 수를 다루는 방법이죠.
isolation에서는 loss 함수로 경우의 수를 다뤘다면 여기서는 BFS, DFS, A*, greedy search 와 같은 방법으로 검색을 합니다. 그리고 Planning 이라는 꽤 고전적인 방법으로 비행기의 경로를 세워봅니다.

### Recognizer

<div align="center"> <img src="/image/aind/3.png" /> </div>

이번엔 수화를 인식하는 프로그램을 만듭니다. 이미 전체적인 코드는 제공해주기 때문에 영상을 다룰 일은 없습니다. 여기서는 HMM(Hidden Markov Model)을 이용해 수화를 인식하죠. HMM 역시 요즘은 잘 안쓰이는 거 같지만 알아두면 꽤 좋은 모델입니다. 저는 HMM 이라는 모델 자체가 굉장히 흥미롭더라고요. 딥러닝과 약간 닮은 부분도 있고요.

<div align="center"> <img src="/image/aind/4.png" /> </div>

## Term1

이렇게 Term1은 고전적이고 기초를 이루는 인공지능에 대해 배웁니다. 저는 코딩을 하는데에 꽤 어려움을 겪었는데 Term2에 비해 요구되는 코딩 실력이 높습니다. 또 AIMA라는 책을 읽을거리로 주는데 꽤 유명한 책으로 필요한 부분만 읽게되니 좋기도 했고요. 반면 여기서 배우는 것들은 요즘은 안쓰이는 방법들이고 AIMA도 요새는 잘 다루지 않는 것들이 많아 왜 이런걸 배우나 생각도 들기도 합니다. 프로젝트를 하면서는 코딩이 가장 어려웠지만, 제 나름 다른 연구에서 term1에서 배운 것들을 써먹어보니 재미있었습니다. HMM을 끝으로 term1이 끝나고 2~3주 쉰 후 term2를 시작하게 됩니다.

# Deep learning

Term2 에서는 딥러닝을 위주로 진행됩니다. 기본적인 인공신경망의 개념을 시작으로 CNN,AutoEncoder, RNN, text generation, GAN을 진행합니다. GAN과 같은 경우 ian goodfellow가 직접 나오기도 하고요.
Term2 의 가장 큰 특징은 조그만 프로젝트가 더 많습니다. 프로젝트라기 보다는 learn by doing으로 udacity에서 제공하는 notebook 파일로 모델을 직접 짜보며 진행하죠.

제출해야하는 프로젝트는

- Dog breed classification

캐글에도 있는 개 품종 분류 프로젝트입니다. CNN 파트에 포함되어 있고 가장 첫 프로젝트죠. 이미 CNN을 좀 다뤄본 저로써는 쉬운 느낌이 좀 있었습니다.
- Text generation

RNN, LSTM 등을 이용해 소설을 생성하는 프로젝트입니다. 직접해보면 사실 모델의 성능이 좋진 않습니다. 자연어 쪽은 아직 발전할 부분이 많다는 거겠죠. RNN은 제가 해야지 생각만하고 미뤘던 터라 개인적으로는 처음 접해보게 되면서 이 부분이 특히 좋았습니다.

## Term2

Term2는 개념만 간단하게 알려주기 때문에 제공하는 notebook 파일을 성실하게 하는 게 중요합니다. 개인적으로 term2의 퀄리티는 term1 보다는 떨어지는 것 같습니다. 핫한 분야 몇가지만 맛보기로 보여주는 느낌이 들기도 하였고요. 이미 어느정도 공부한 분야는 또 쉽기도 했습니다. 딥러닝의 핫한 분야들을 한번씩 간단한 모델이라도 구현해보고 모델을 이해하는 것이 주된 목적 같습니다.

# Concentration

Term2 에서 딥러닝에 발을 들여놓았습니다. 다음 Concentration은 Computer vision, NLP, Voice User Interface 중 한가지를 선택해 그것만 집중적으로 공부하게 됩니다. Term2를 진행한다면 기본적으로 하나의 Concentration을 진행하고 추가적으로 수강비를 내면 다른 Concentration도 진행할 수 있습니다. 저는 voice user interface 와 NLP를 고민하다 NLP를 선택했습니다.

NLP Concentration에서는 자연어 처리에서 쓰이는 방법들을 좀 더 세부적으로 다루게 됩니다. 기본적인 자연어 처리를 하고 텍스트를 딥러닝 모델에 넣기까지의 과정을 좀 더 집중적으로 배우고 프로젝트로는 기계 번역을 다룹니다. 물론 아주 간단한 데이터셋에 대해서 영어-프랑스어를 번역하는 프로젝트죠. 그 다음은 word-embedding, seq2seq로 Concentration을 마치게 됩니다.

저는 자연어 처리를 이전에는 접해보지 않았기 때문에 배울 것이 많았습니다. 검색하고 찾아보며 혼자할 수 있는 것들이지만 다른 일들에 치여 안하기 때문에 이렇게라도 하면서 어떤 가이드를 받고, 공부의 방향을 잡는게 특히 좋았죠. 이전에 이미 이미지 쪽을 공부해 본 저로써 computer vision을 선택했다면 별로라고 생각했을 거 같습니다. Concentration 이지만 현재도 계속 발전되는 분야라 아주 깊은 수준의 자료가 제공되지는 않는 거 같기도 하고요.

# Pros and Cons

마지막으로 AIND의 장단점을 적어보자면 이렇습니다. 물론 주관적입니다.

### 장점

- 억지로라도 공부하게 된다.
- Term1에서는 평생 안할 거 같은 고전적인 인공지능에 대해 공부한다.
- 꽤 수준 높은 코드를 보며 학습한다.
- 다양한 분야를 접해보며 어느 것이 나에게 흥미가 있는지 쉽게 찾아볼 수 있다.
- 공부를 하는데 가이드를 받고 방향성을 잡을 수 있다.

### 단점

- 사실 안하지만 검색하고 찾아보며 할 수 있는 것들이다.
- term2 부분은 퀄리티가 좀 더 낮다는 느낌이 든다.
- 이것만으로 공부를 끝낸다고 하면 안된다.
- 실제 무언가를 하기엔 겉핥기만 하는 느낌이다.
- 좀 비싼 느낌이다.