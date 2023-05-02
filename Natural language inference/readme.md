
Natural language inference는 두 문장의 관계를 {entailment, contradiction, neutral} 세가지로 추론하는 NLP Task 입니다.

Kakao에서 공개한 데이터셋으로 실험을 해보았으며 kakao 에서 공개한 데이터셋과 논문은 아래 링크에서 확인할 수 있습니다.
https://github.com/kakaobrain/kor-nlu-datasets

NLI Task의 경우 Bert model을 사용하면 접근이 보다 쉬워지는데,
학습시 두개의 문장이 입력되는 구조이므로 자연스럽게 두 문장의 관계를 추론하는 문제가 Classification 문제로 정의됩니다.

Pre-trained model은 Huggingface의 "monologg/koelectra-base-v3-discriminator" 을 사용하였고,
학습시 발생하는 지표는 WandB에서 확인했습니다.

Notebook :
https://github.com/mypeacefulcode/ml-research/blob/main/Natural%20language%20inference/training.ipynb

