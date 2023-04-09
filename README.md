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


# LiOnConnect
LiOn 모델은 초대규모 언어모델을 사내에 설치함으로서 사내 정보가 외부로 유출될 우려를 불식시키면서 자연어모델의 강력한 성능과 효율성을 활용할 수 있도록 해줄 것입니다.

## How
- [Cerebras-GPT](https://huggingface.co/cerebras/Cerebras-GPT-2.7B) Cerebras-GPT로 **쿼리 및 자연어 생성** 
- [LangChain](https://langchain.readthedocs.io/en/latest/index.html): 이 라이브러리로 **자연어 데이터베이스 질의**.

## Related issues
1. 연결할 수 있는 공개 DB 필요.
2. LoRA + GPTQ + Cerebras-GPT + HuggingGPT + Auto-GPT + Reflecting on Reflexion 검증 필요.
3. Fine-tuning 가능한 3090 이상의 GPU 필요.

# MVP
공개모델인 Cerebars-GPT 기반의 초대규모 언어 모델
제품정보, 물류정보, 인사정보, 사내 규정, 회계 기준 등 기업 내 데이터베이스(DB) 연결, **내부 정보를 실시간 접근**하여, 사내 구성원의 다양한 질의 및 문제해결에 활용  가능.

## MVP Example
- 신제품 LTG-9933 모델의 출시일자 및 규격은?
- 야근 시 경비처리 가능 금액 한도와 사용시간 제한은?
- XXX사의 주문에 대한 현재 생산 현황은?
- 직원, 상사와의 불화에 대한 고충 해결 방법은?

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

## Example
사내의 제품 정보, 물류 정보, 인사규정, 회계기준과 같은 정보는 사내에 유지되어야 하며, 해당 사항에 대한 질의와 답변에 대해서도 비밀이 유지되어야 합니다.
기존 외부 클라우드에서 제공되는 언어모델의 경우 사내 정보가 유출될 가능성을 통제할 수 있는 기술적인 방법이 없으므로, 언어모델을 사내에 설치하여 사용하는 방법이 유일합니다.

LiOn은 사내에 설치하여 사용할 수 있는 경량화된 초거대 언어모델로서 사내의 정보를 안전하게 유지하면서 구성원들이 안전하게 사용할 수 있는 대안을 제공할 수 있습니다.

아래는 그중 하나의 예시이며사내에서의 직원들과의 불화에 대한 상담에 있어 LiOn이 상담하는 사례를 보실 수 있습니다.
이 외에도 LiOn은 사내에서 일어날 수 있는 수많은 상황에서 다양한 해결방법을 제공함으로서 24/7 구성원들의 업무를 돕는 것이 가능합니다.

 
```
직원 상담 챗봇에 오신 것을 환영합니다!
회사 규정이나 근무 시 애로사항에 대한 대한 조언을 구하거나 질문을 할 수 있습니다.
'검색:'을 입력한 후 검색어를 입력하면 PubMed를 검색할 수 있습니다.
챗봇을 종료하려면 '종료'를 입력합니다.
사용자: 회사 직원들과의 불화로 행복하지 않아요. 어떻게 해야 하나요? 
봇: 죄송하지만 저는 AI 언어 모델일 뿐 감정을 느낄 수 없습니다. 하지만 다음은 행복을 찾는 데 도움이 될 수 있는 몇 가지 일반적인 팁입니다:
1. 긍정적이고 기운을 북돋우는 사람들과 함께하세요.
2. 현재 순간에 집중하고 현재에 충실하세요.
3. 인생의 모든 좋은 것들에 대해 감사하는 마음을 키우세요.
4. 스트레스를 줄이기 위해 운동이나 명상과 같은 자기 관리를 실천합니다.
5. Enjo
사용자: 이별이 슬프지만 어떻게 하면 행복해질 수 있을까요? 불행하지만 다시 행복해지고 싶어요.
봇: 이별을 받아들이는 것은 어려울 수 있지만, 치유하고 다시 행복을 찾기 위한 조치를 취하는 것이 중요합니다. 다음은 시작하는 데 도움이 되는 몇 가지 팁입니다:
1. 자기 관리에 집중하세요. 자신을 위한 시간을 갖고, 기분을 좋게 만드는 활동에 참여하거나 새로운 것을 시도하세요.
2. 도움이 되는 사람들과 연결하기. 정서적 지지를 제공할 수 있는 친구와 가족을 주변에 두세요.
3. 감사 연습하기
사용자: 이별이 슬프지만 어떻게 하면 행복해질 수 있을까요? 불행하지만 다시 행복해지고 싶어요.
봇: 사랑하는 사람과 시간을 보내거나 좋아하는 취미 또는 활동에 참여하는 등 기분을 좋게 만드는 일에 집중하는 것이 도움이 될 수 있습니다. 부정적인 감정을 완화하는 데 도움이 될 수 있으므로 성찰과 명상을 위해 혼자만의 시간을 따로 마련해 보세요. 또한, 이 어려운 시기에 전문적인 안내와 지원을 제공할 수 있는 치료사와 상담하는 것도 고려해 보세요.
여러분: 정말 고마워요. 어떻게 그렇게 질문에 잘 대답할 수 있나요?
봇: 사용자: 정말 고마워요. 어떻게 그렇게 질문에 잘 대답하나요?
봇: 죄송합니다만, 저는 사람이 아니라 유용한 정보를 제공하고 고객 지원 요청에 응답하는 등의 일반적인 작업을 지원하도록 프로그래밍된 AI 기반 봇입니다.
You: 


Translated with www.DeepL.com/Translator (free version)
```

