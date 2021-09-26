[자연어 처리](#자연어-처리)
[NLP task](#nlp-task)
[NLP 이외의 분야](#nlp-이외의-분야)
[Text mining task](#text-mining-task)
[Information retrieval task](#information-retrieval-task)
[NLP 최근 발전](#nlp-최근-발전)

## 자연어 처리

1. NLU(Natural language Understanding): 컴퓨터가 주어진 단어나 문장보다 더 긴 문단이나 글을 이해하는 과정
2. NLG(Natural Language Generation): 단어를 상황에 따라 생성
3. LM(Language Modeling): 현재까지 주어진 문장이나 문단 일부를 보고 다음 단어를 예측
4. Machine Translation: 기계번역. ex) 파파고
5. QA(Question Answering)
6. Documents Classification

![https://blog.kakaocdn.net/dn/bpgcP5/btqEepVw06B/HMSUXIrEzwS3OB4BsWWZOk/img.png](https://blog.kakaocdn.net/dn/bpgcP5/btqEepVw06B/HMSUXIrEzwS3OB4BsWWZOk/img.png)

## NLP task

### Low-level parsing task

1. Tokenization
    - 주어진 문장을 단어 단위로 쪼개어 나가는 것; Tokenization
    - 문장을 이루는 각 단어들은 정보 단위. 단어를 token이라고 부른다.
    - 문장은 이런 token들이 특정 순서로 이루어진 sequence로 볼 수 있다.
2. Stemming

    study란 단어도 어미가 다양하게 변화할 수 있다. (studying, studied ...) 혹은 하늘이 맑다. 맑지만. 맑고.처럼 수많은 어미의 변화 속에서도 그 많은 단어들이 같은 의미를 나타낸다는 것을 컴퓨터도 이해해야 한다.

    → 단어의 다양한 변화를 없애고, 의미만을 보존하는. **단어의 어근**을 전달하는 것을 의미한다.

### Word and Phase level task

1. NER(Named Entity Recognition)

    단일 단어 혹은 여러 단어로 이루어진 고유명사를 인식하는 task.

    ex) New York Times → 3개의 단어로 각각 해석하면 안되고, 하나의 고유명사로 인식해야 한다.

2. POS(Part-of-Speech) tagging

    단어들이 문장 내에서 성분이 무엇인지 알아내는 task.

    ex) 주어, 목적어 or 형용사구가 어떤 명사를 꾸며주는지 인식하는 task

### Sentence level task

1. Sentiment analysis: 주어진 문장이 긍정  or 부정 어조의 문장인지 예측하는 감정 분석
2. Machine Translation

    번역.

    ex) 영어 문장을 한글 무정으로 번역할 때, 주어진 영어 문장을 전체적으로 이해하고, 한글 문장으로 번역할 때, 각 단어별로 적절한 한글 단어로의 번역과 적절한 한글 어순으로 번역하는 것.

### Multi-sentence and Paragraph level task

다수의 문장 및 문단 레벨의 task

1. Entailment prediction

    두 문장간의 논리적인 내포, 모순 관계 예측

    ex) 앞말과의 연계성

2. QA

    독해 기반의 질의응답

    'where did napeleon die' 검색하면 예전에는 각 단어의 검색 결과가 나왔다.

    현재 QA를 적용해 독해를 통하여 정답을 사용자에게 전달.

3. Dialog system: 챗봇과 같은 대화를 수행할 수 있는 NLP 기술
4. (Document) Summarization: 주어진 문서(뉴스 문서 등)을 한 줄로 요약

## NLP 이외의 분야

## Text mining task

1. Extract useful information and insights from text and document data

    빅데이터 분석.

    ex) 과거 1년 동안 나온 뉴스 기사를 전부 모아 특정 keyword들의 빈도를 시간순으로 정리하여 트렌드를 구한다. 그 결과로 특정 유명인의 이미지가 시간이 지남에 따라 어떠한 양상을 띄는지 분석한다. 혹은 회사에서 상품을 출시했을 때 사람들의 반응을 키워드 빈도수를 도출하여 분석한다.

2. Document clustering

    서로 다른 키워드이지만 비슷한 의미인 키워드를 grouping할 때 이를 자동으로 수행할 수 있는 topic modeling.

    이 기술을 통해 어떤 토픽의 세부 내용과 사람들의 의견을 빠르게 모을 수 있다.

3. Highly related to coputational social science

    사화과학, 소셜 미디어 분석해서 요새 사람들은 어떤 신조어를 많이 사용하고 이는 현대 사회 양상과 관련이 있다.와 같이 사회과학 여러 insight를 도출할 수 있다.

## Information retrieval task

구글이나 네이버에서 주로 사용되는 검색 기술 분야.

추천 시스템; 평소에 자주 듣는 음악과 비슷한 음악 추천, 하나의 영상을 볼 때 그와 비슷한 양상의 영상 추천.

→ 사용자가 수동으로 할 법한 검색 과정을 자동화해서 추천. 개인화된 광고 상품 추천 등 다양한 분야에서 쓰인다.

## NLP 최근 발전

ML, DL 일반적으로 숫자로 이루어진 데이터를 입력과 출력의 형태로 필요로 함.

→ 따라서 자연어에서는 주어진 텍스트 문제를 단어 단위로 분리하고(Tokenization), 각 단어 단위를 특정한 dim으로 이루어진 벡터로 표현하는 과정을 거치게 된다. 이는 word를 벡터 공간의 한 점으로 나타낸다는 뜻에서 **Word Embedding**이라고 부른다.

sequence 형식의 데이터이기 때문에 이에 특화된 RNN(Recurrent Neural Network)이 자연어 처리의 핵심 모델로 자리잡게 되었다. 이런 RNN 계열의 모델 중에서 LSTM(Long Short Term Memory)와 이를 보다 단순화해서 계산 속도를 빠르게한 GRU(gated Recurrent Unit)등의 모델이 많이 사용되어 왔다.

2017년 구글에서 Attention is All You Need라는 논문이 나오면서 RNN → self-attention이라 불리는 모듈로 대체할 수 있는 Transformer 모델이 제안되었다. 이는 큰 성능 향상을 일으켰다 !

원래는  기계 번역 분야를 위해 처음 제안 되었다. 기존 Rule기반은 예외 사항이 너무 많았다. (전문가의 의견을 이용한 알고리즘이었기 때문에)

Transformer를 이용하여 Transfer Learning을 적용했을 때 기존 각 task별로 특화되었던 모델을 사용하는 것보다 월등히 성능이 좋았다.

Self-supervised model; 앞뒤 문맥을 보고 중간에 뚫린 단어를 맞추는 것.
