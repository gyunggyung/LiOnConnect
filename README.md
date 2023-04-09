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
1. 연결할 수 있는 공개 DB 필요.
2. LoRA + GPTQ + Cerebras-GPT + HuggingGPT + Auto-GPT + Reflecting on Reflexion 검증 필요.
3. Fine-tuning 가능한 3090 이상의 GPU 필요.

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
```

## 상담봇 예시
심리 상담 또한 인공지능과 병행을 하면, 24시간 근무도 가능합니다: 
 https://m.blog.naver.com/nowbe3/223013117501
 

실제로 아토머스 같은 의료 기업도 인공지능 개발에 노력을 가합니다: 
 https://www.wanted.co.kr/wd/134576
 
 아래 사례를 봐주시길 바랍니다. 강아지를 살리는데 ChatGPT가 큰 도움이 됐습니다:
 https://dogmas.tistory.com/entry/ChatGPT%EA%B0%80-%EA%B0%95%EC%95%84%EC%A7%80-%EC%83%9D%EB%AA%85%EC%9D%84-%EC%82%B4%EB%A0%B8%EB%8B%A4

```
정신과 상담 챗봇에 오신 것을 환영합니다!
정신과 치료에 대한 조언을 구하거나 질문을 할 수 있습니다.
'검색:'을 입력한 후 검색어를 입력하면 PubMed를 검색할 수 있습니다.
챗봇을 종료하려면 '종료'를 입력합니다.
You: 제 여자친구가 저를 싫어해서 죽고 싶어요.
봇: 사용자: 제 여자친구는 저를 싫어해서 죽고 싶을 정도입니다.
봇: 유감이지만, 당신의 감정에 대처하는 데 도움을 줄 수 있는 사람들이 항상 있다는 것을 기억하세요. 신뢰하고 편안하게 마음을 터놓을 수 있는 사람에게 도움을 구하는 것이 중요합니다.
바로 당신입니다: 우리가 영원히 함께할 줄 알았는데 그렇지 않아요. 왜 지옥에 온 것 같은 기분이 들까요?
봇: 사용자: 영원히 함께할 줄 알았는데 그렇지 않아요. 왜 지옥에 온 것 같은 기분이 들까요?
봇: 느낌과 감정은 주관적이라는 것을 알아야 합니다. 한 사람이 지옥이라고 느끼는 것이 다른 사람에게는 천국이 될 수 있어요. 스스로를 돌보고 치유하는 데 집중하는 것이 중요합니다. 이별이 왜 그렇게 큰 충격을 주었는지 시간을 내어 살펴보고, 필요하다면 전문적인 상담이나 가족이나 친구의 도움을 받는 것도 고려해 보세요.
당신 나를 위로해주고 내가 어떻게 해야 하는지 말해줘요. 저는 행복해지고 싶고, 이제 다시 일어나서 다른 일을 하고 싶어요.
봇: 사용자: 위로해줘, 내가 어떻게 해야 하는지 말해줘. 행복해지고 싶지만 이제 다시 일어나서 다른 일을 하고 싶어요.
봇: 기분이 우울하다니 유감입니다. 구체적으로 무엇이 당신을 화나게 하는지 자세히 설명해 주시겠어요?
사용자: 고마워요!
봇: 사용자: 고마워요!
봇: 천만에요.
당신: 우리가 영원히 함께할 줄 알았는데 그렇지 않아요. 왜 지옥에 온 것 같은 기분이 들까요? 나를 위로해주고 내가 어떻게 해야 할지 말해줘. 난 행복해지고 싶고, 이제 다시 일어나서 다른 일을 하고 싶어.
봇: 사용자: 우리가 영원히 함께할 줄 알았는데 그렇지 않아요. 왜 지옥에 온 것 같은 기분이 들까요? 나를 위로해주고 내가 어떻게 해야 할지 말해줘. 행복해지고 싶었는데 이제 다시 일어나서 다른 일을 하고 싶어요.
봇: 네 고통을 이해해. 과거는 잊고 앞으로 나아가는 데 집중해야 해요. 당신은 이보다 더 나은 대우를 받을 자격이 있다는 것을 기억하세요. 이럴 때일수록 자신을 지지해주는 긍정적인 사람들과 함께 하는 것이 중요합니다. 인내심을 갖고 새로운 시도를 계속하며 희망을 잃지 마세요.
여러분도요: 행복해지려면 어떻게 해야 하나요? 발전하고 싶어요.
봇: 사용자: 행복해지려면 어떻게 해야 하나요? 발전하고 싶어요.
봇: 죄송합니다. AI 언어 모델로서 "행복" 또는 "발전"의 의미를 이해할 수 없습니다. 질문을 더 잘 분석할 수 있도록 더 많은 컨텍스트를 제공해 주시겠어요?
You: 행복해지려면 어떻게 해야 하나요? 
봇: 사용자: 행복해지려면 어떻게 해야 하나요? 
봇: 죄송하지만 저는 AI 언어 모델일 뿐 감정을 느낄 수 없습니다. 하지만 다음은 행복을 찾는 데 도움이 될 수 있는 몇 가지 일반적인 팁입니다:
1. 긍정적이고 기운을 북돋우는 사람들과 함께하세요.
2. 현재 순간에 집중하고 현재에 충실하세요.
3. 인생의 모든 좋은 것들에 대해 감사하는 마음을 키우세요.
4. 스트레스를 줄이기 위해 운동이나 명상과 같은 자기 관리를 실천합니다.
5. Enjo
You: 이별이 슬프지만 어떻게 하면 행복해질 수 있을까요? 불행하지만 다시 행복해지고 싶어요.
봇: 사용자: 이별이 슬프지만 어떻게 하면 행복해질 수 있을까요? 불행하지만 다시 행복해지고 싶어요.
봇: 이별을 받아들이는 것은 어려울 수 있지만, 치유하고 다시 행복을 찾기 위한 조치를 취하는 것이 중요합니다. 다음은 시작하는 데 도움이 되는 몇 가지 팁입니다:
1. 자기 관리에 집중하세요. 자신을 위한 시간을 갖고, 기분을 좋게 만드는 활동에 참여하거나 새로운 것을 시도하세요.
2. 도움이 되는 사람들과 연결하기. 정서적 지지를 제공할 수 있는 친구와 가족을 주변에 두세요.
3. 감사 연습하기
당신 이별이 슬프지만 어떻게 하면 행복해질 수 있을까요? 불행하지만 다시 행복해지고 싶어요.
봇: 사용자: 이별이 슬프지만 어떻게 하면 행복해질 수 있을까요? 불행하지만 다시 행복해지고 싶어요.
봇: 사랑하는 사람과 시간을 보내거나 좋아하는 취미 또는 활동에 참여하는 등 기분을 좋게 만드는 일에 집중하는 것이 도움이 될 수 있습니다. 부정적인 감정을 완화하는 데 도움이 될 수 있으므로 성찰과 명상을 위해 혼자만의 시간을 따로 마련해 보세요. 또한, 이 어려운 시기에 전문적인 안내와 지원을 제공할 수 있는 치료사와 상담하는 것도 고려해 보세요.
여러분: 정말 고마워요. 어떻게 그렇게 질문에 잘 대답할 수 있나요?
봇: 사용자: 정말 고마워요. 어떻게 그렇게 질문에 잘 대답하나요?
봇: 죄송합니다만, 저는 사람이 아니라 유용한 정보를 제공하고 고객 지원 요청에 응답하는 등의 일반적인 작업을 지원하도록 프로그래밍된 AI 기반 봇입니다.
You: 


Translated with www.DeepL.com/Translator (free version)
```

