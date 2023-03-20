# LiOn
Lion 은 다양한 데이터와 연결되어 자연어 처리 분야에서의 전문성을 확장할 수 있는 모델입니다.

## LiOnConnect
Lion 모델의 강력한 자연어 처리 능력과 함께, 다양한 DB와의 연결을 통해 자연어 처리 분야에서 높은 성능과 효율성을 제공합니다.

### How
- [alpaca-lora.ipynb](https://colab.research.google.com/drive/1eWAmesrW99p7e1nah5bipn0zikMb8XYC#scrollTo=upOB2AQJSW9-): This notebook contains minimal code for **running [Alpaca-LoRA](https://github.com/tloen/alpaca-lora/)** for demonstration purposes.
- [Make ChatGPT-replica](https://colab.research.google.com/drive/1UcLLV4mLtn8vxGk5U3TxiLNbVBealy16?usp=sharing):  ChatGPT를 만든 원리인 **GPT fine-tuning, 강화학습(PPO), RLHF, ChatGPT 데이터셋 구축**에 대해 다루고 코드 실습.
- [LangChain](https://langchain.readthedocs.io/en/latest/index.html): 이 라이브러리로 **자연어로 데이터베이스 질의**.
- [r-build/sf-restaurants-sql](https://github.com/r-build/sf-restaurants-sql): 샌프란시스코 식품 건강 조사 **데이터**.
- [OpenAI GPT-3 and LangChain](https://blog.devgenius.io/query-database-using-natural-language-openai-gpt-3-d2403636527a): OpenAI GPT-3 및 LangChain을 사용하여 **자연어로 데이터베이스 질의**.

### Related issues
1. [비상업적 연구 목적으로만 본 소프트웨어의 파생 저작물을 제작할 수 있습니다.](https://docs.google.com/forms/d/e/1FAIpQLSfqNECQnMkycAp2jP4Z9TFX0cGR4uf7b_fBxjY_OjhJILlKGA/viewform)

# Talk to Alpaca-LoRA
This notebook contains minimal code for running [Alpaca-LoRA](https://github.com/tloen/alpaca-lora/) for demonstration purposes. Please check the repo for more details.

# MVP
기업 데이터베이스(DB) 접속. **내부 정보를 실시간 접근**하여, 필요작업 수행.
- 예: 기업 전화상담실
- 내부 회계사와 변호사
- 개인 비서와 의사
- 글로벌 심리 상담사와 교수

## Running LangChain
CustomSQLDatabaseChain, CustomOpenAI 를 만들어서 기존에 동작하지 않던 Model 사용 가능.

### Prompts
```
text1 = "What are the top 3 most expensive products"
text2 = "Can you give me a list of the 3 priciest items we have for sale?"
text3 = "Which 3 products are the most expensive ones we offer?"

result = db_chain(text1)
result = db_chain(text2)
result = db_chain(text3)

# for _ in range(15):
#     text = input()
#     result = db_chain(text)
```
