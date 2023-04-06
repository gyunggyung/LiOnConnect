<h1 align="center"> <img src="image/logo.png" width="400" height="400"> </h1>


<p align="center">
  <a href="https://www.apache.org/licenses/LICENSE-2.0">
    <img alt="licenses" src="https://img.shields.io/github/license/gyunggyung/LiOn?style=flat-square"></a>
  <a href="https://colab.research.google.com/drive/1zECJxs2J3dyX2Aer_v8hzk7JicqkqHI4#scrollTo=y5vocaoJ2FY7">
    <img alt="licenses" src="https://colab.research.google.com/assets/colab-badge.svg"></a>
  <a href="https://github.com/gyunggyung/LiOn/stargazers">
    <img alt="GitHub stars" src="https://img.shields.io/github/stars/gyunggyung/LiOn?style=flat-square&color=yellow"></a>
  <a href="https://github.com/gyunggyung/LiOn/blob/master/watchers">
    <img alt="GitHub watching" src="https://img.shields.io/github/watchers/gyunggyung/LiOn?style=flat-square&color=ff69b4"></a>
  <a href="https://github.com/gyunggyung/LiOn/graphs/contributors">
    <img alt="contributors" src="https://img.shields.io/badge/contributors-welcome-yellowgreen?style=flat-square"></a>
</p>

<div align="center">
    <sub> Let's make good AI publicly available. 🙇‍♂️🙇‍♀️ by <a href="https://github.com/gyunggyung/LiOn/stargazers">Stargazers</a>  </sub>
</div>


# LiOn
LiOn 은 다양한 데이터와 연결되어 자연어 처리 분야에서의 전문성을 확장할 수 있는 모델입니다.

## LiOnConnect
LiOn 모델의 강력한 자연어 처리 능력과 함께, 다양한 DB와의 연결을 통해 자연어 처리 분야에서 높은 성능과 효율성을 제공합니다.

### How
- [Cerebras-GPT](https://huggingface.co/cerebras/Cerebras-GPT-2.7B) Cerebras-GPT로 **쿼리 및 자연어 생성** 
- [LangChain](https://langchain.readthedocs.io/en/latest/index.html): 이 라이브러리로 **자연어 데이터베이스 질의**.

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
