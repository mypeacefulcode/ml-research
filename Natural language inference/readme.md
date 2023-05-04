
Natural language inference는 두 문장의 관계를 {entailment, contradiction, neutral} 세가지로 추론하는 NLP Task 입니다.

Kakao에서 공개한 데이터셋으로 실험을 해보았으며 kakao 에서 공개한 데이터셋과 논문은 아래 링크에서 확인할 수 있습니다.
https://github.com/kakaobrain/kor-nlu-datasets

NLI Task의 경우 Bert model을 사용하면 접근이 보다 쉬워지는데,
학습시 두개의 문장이 입력되는 구조이므로 자연스럽게 두 문장의 관계를 추론하는 문제가 Classification 문제로 정의됩니다.

Pre-trained model은 Huggingface의 "monologg/koelectra-base-v3-discriminator" 을 사용하였고,
학습시 발생하는 지표는 WandB에서 확인했습니다.

Notebook :
[Natural language inference](https://github.com/mypeacefulcode/ml-research/blob/main/Natural%20language%20inference/Natural_language_inference.ipynb)

실험결과 별도의 튜닝 과정없이 accuracy가 74% 정도 나왔습니다.  
  
차후 같은 NLI Task를 다룰 기회가 있다면 두개의 BERT 모델을 이용해 문장의 유사도 및 문장의 관계를 추론하는 Sentence Bert와 비교해보면 좋겠다는 생각을 했습니다.

<img width="400" alt="스크린샷 2023-05-04 오전 11 43 41" src="https://user-images.githubusercontent.com/16236194/236099936-b5eb4853-dec1-42a8-8c0f-0ef5913ed5c6.png">
<sub>[SBERT](https://www.sbert.net/examples/training/nli/README.html)</sub>. 
