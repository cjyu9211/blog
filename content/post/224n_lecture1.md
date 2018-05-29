---
title: "Lecture 1: NLP with DL"
date: 2018-05-29T12:00:33+09:00
tags: ["CS 224n", "NLP", "Data Science"]
topics: ["NLP with Deep Learning"]
---

# Lecture 1: NLP with DL

본 카테고리는 Stanford University School of Engineering 에서 공개한 내용인 CS224n- NLP with Deep Learning 강의를 개인 공부하고 요약한 내용이다. 원본은 본문 최하단의 링크를 참조하면 된다. 



#### What is Natural Language Processing (NLP)?

- NLP는 1) 전산과학, 2) 인공지능, 3) 언어학이 교차하는 부분의 학문이다. 
- NLP는 컴퓨터로 하여금 자연어를 이해하고 처리하는 능력을 배양하는 기술이다. 최근 적용된 사례로는 Apple의 Siri, Google의 Google Assistant, Facebook의 Facebook M을 예로 들 수 있다. 

#### NLP Levels

일반적으로, NLP level은 다음과 같이 정의 된다. 

![nlp_levels](/Users/macbookpro/Desktop/blog/draft/img_src/nlp_level.png)

- 자연어의 input은 크게 음성과 텍스트 두 가지로 나뉜다. 각각의 input은 음성학/음운론 분석, 그리고 OCR/토큰화 작업을 거친다.
- 이후에는 두 input에 대해 같은 단계를 거친다. 첫 번째는 '**Morphological analysis**'이다. 이는 형태소 분석을 의미하는데 뜻을 지닌 가장 작은 말의 단위로 쪼개는 분석이다.
- '**Syntactic analysis**': 그 다음은 문장의 구조를 이해하는 syntactic analysis이다. 주어, 동사, 목적어 등을 구분하는 작업이다. 
- '**Semantic Interpretation**': 문장의 정확한 의미, 즉 문맥적 의미를 파악하는 것이다. 
- 본 강의에서는 특히 speech input과 {Syntactic analysis, Semantic Interpretation}을 주로 다룬다.



#### What's Deep Learning (DL)?

Deep Learning(DL)은 Machine Learning(ML)의 한 분야로 볼 수 있다. 다만, 기존의 logistic regression, naive bayes, decision tree, SVM으로 대표되는 전통적인 ML과는 큰 차이가 있다. 이러한 기존의 ML 알고리즘들은 대부분이 human-designed representation과 input features를 설계하고 이를 numerically 최적화하는 데 많은 시간을 할애한 반면, DL 알고리즘은 이러한 representation이나 최적의 결과를 위한 최적의 feature를 알고리즘이 직접 학습한다. 



예시로, 2015년 이전까지의 Google 검색 엔지니어들은 검색어(input signal)가 회사 이름인 지 등을 구분 짓기 위해 첫 letter가 대문자인지 소문자인지 '-'(hypen)의 유무 등의 feature들을 설계하고 추가함으로써 검색 기능 개선을 꾀했다. 

















[강의 영상 원본](https://www.youtube.com/watch?v=OQQ-W_63UgQ&list=PL3FW7Lu3i5Jsnh1rnUwq_TcylNr7EkRe6&index=1) - Stanford CS 224n **Lecture 1**

[강의 Lecture note](http://web.stanford.edu/class/cs224n/syllabus.html)