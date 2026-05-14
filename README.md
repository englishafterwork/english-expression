# english-questionszip
아이의 영어 사고력을 깨우는 실전 질문 30
<!DOCTYPE html>
<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>사고력 영어 질문 30 | 원어민 부모처럼 대화하기</title>
<link href="https://fonts.googleapis.com/css2?family=Gowun+Dodum&family=Noto+Sans+KR:wght@400;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --cream: #FFF8F0;
    --peach: #FFD9B7;
    --coral: #FF7F5C;
    --deep: #2D1B0E;
    --mid: #6B3F2A;
    --soft: #F5EDE4;
    --green: #4CAF87;
    --blue: #5B9BD5;
    --purple: #8B6FD4;
    --yellow: #F5C842;
  }

  body {
    background: var(--cream);
    color: var(--deep);
    font-family: 'Noto Sans KR', sans-serif;
    min-height: 100vh;
  }

  /* HERO */
  .hero {
    background: var(--deep);
    color: var(--cream);
    padding: 64px 24px 56px;
    text-align: center;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse at 30% 50%, #FF7F5C22 0%, transparent 60%),
                radial-gradient(ellipse at 80% 20%, #8B6FD422 0%, transparent 50%);
  }
  .hero-tag {
    display: inline-block;
    background: var(--coral);
    color: #fff;
    font-size: 12px;
    font-weight: 700;
    letter-spacing: 0.12em;
    padding: 6px 16px;
    border-radius: 100px;
    margin-bottom: 20px;
    font-family: 'Space Grotesk', sans-serif;
  }
  .hero h1 {
    font-family: 'Gowun Dodum', serif;
    font-size: clamp(26px, 6vw, 42px);
    line-height: 1.35;
    margin-bottom: 16px;
    position: relative;
  }
  .hero h1 em {
    color: var(--peach);
    font-style: normal;
  }
  .hero p {
    font-size: 15px;
    color: #C8B8AB;
    max-width: 480px;
    margin: 0 auto 32px;
    line-height: 1.7;
  }
  .hero-stats {
    display: flex;
    justify-content: center;
    gap: 32px;
    position: relative;
  }
  .stat {
    text-align: center;
  }
  .stat-num {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 28px;
    font-weight: 700;
    color: var(--peach);
  }
  .stat-label {
    font-size: 12px;
    color: #A08070;
    margin-top: 2px;
  }

  /* FILTER TABS */
  .filter-wrap {
    padding: 28px 20px 8px;
    display: flex;
    gap: 8px;
    flex-wrap: wrap;
    justify-content: center;
    max-width: 720px;
    margin: 0 auto;
  }
  .filter-btn {
    padding: 8px 18px;
    border-radius: 100px;
    border: 1.5px solid var(--coral);
    background: transparent;
    color: var(--coral);
    font-size: 13px;
    font-family: 'Noto Sans KR', sans-serif;
    cursor: pointer;
    transition: all 0.18s;
    font-weight: 700;
  }
  .filter-btn:hover, .filter-btn.active {
    background: var(--coral);
    color: #fff;
  }

  /* GRID */
  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 16px;
    padding: 20px 20px 60px;
    max-width: 1000px;
    margin: 0 auto;
  }

  /* CARD */
  .card {
    background: #fff;
    border-radius: 18px;
    padding: 22px 22px 18px;
    border: 1.5px solid #EDE3D8;
    position: relative;
    transition: transform 0.18s, box-shadow 0.18s;
    cursor: default;
    animation: fadeUp 0.4s both;
  }
  .card:hover {
    transform: translateY(-4px);
    box-shadow: 0 12px 32px rgba(45,27,14,0.10);
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(16px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .card-num {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.08em;
    color: #C8B4A0;
    margin-bottom: 10px;
  }
  .cat-pill {
    display: inline-block;
    font-size: 11px;
    font-weight: 700;
    padding: 3px 10px;
    border-radius: 100px;
    margin-bottom: 12px;
    letter-spacing: 0.04em;
  }
  .cat-whatif .cat-pill { background: #FFF0E8; color: #D4622A; }
  .cat-why    .cat-pill { background: #EAF4FF; color: #2A6FD4; }
  .cat-tell   .cat-pill { background: #F0F8EE; color: #2A8C5F; }
  .cat-how    .cat-pill { background: #F5F0FF; color: #6B40C4; }

  .en {
    font-family: 'Space Grotesk', sans-serif;
    font-size: 17px;
    font-weight: 700;
    color: var(--deep);
    line-height: 1.4;
    margin-bottom: 8px;
  }
  .ko {
    font-size: 14px;
    color: var(--mid);
    line-height: 1.6;
  }
  .tip {
    margin-top: 10px;
    padding-top: 10px;
    border-top: 1px dashed #EDE3D8;
    font-size: 12px;
    color: #A08070;
    line-height: 1.6;
  }
  .tip::before { content: '💡 '; }

  /* accent border */
  .cat-whatif { border-left: 4px solid var(--coral); }
  .cat-why    { border-left: 4px solid var(--blue); }
  .cat-tell   { border-left: 4px solid var(--green); }
  .cat-how    { border-left: 4px solid var(--purple); }

  /* CTA */
  .cta-wrap {
    background: var(--deep);
    color: var(--cream);
    text-align: center;
    padding: 48px 24px;
  }
  .cta-wrap h2 {
    font-family: 'Gowun Dodum', serif;
    font-size: 22px;
    margin-bottom: 10px;
  }
  .cta-wrap p { font-size: 14px; color: #A08070; margin-bottom: 24px; line-height: 1.7; }
  .cta-btn {
    display: inline-block;
    background: var(--coral);
    color: #fff;
    font-weight: 700;
    font-size: 15px;
    padding: 14px 36px;
    border-radius: 100px;
    text-decoration: none;
    font-family: 'Space Grotesk', sans-serif;
    letter-spacing: 0.03em;
    transition: opacity 0.15s;
  }
  .cta-btn:hover { opacity: 0.88; }

  .hidden { display: none !important; }
</style>
</head>
<body>

<section class="hero">
  <div class="hero-tag">원어민 부모의 비법 질문법</div>
  <h1>아이의 영어 사고력을 깨우는<br><em>실전 질문 30</em></h1>
  <p>Yes, No만 반복하는 아이? 질문 하나로 바꿔보세요.<br>어려운 단어 없이도 생각이 트이는 마법의 표현들이에요.</p>
  <div class="hero-stats">
    <div class="stat"><div class="stat-num">30</div><div class="stat-label">실전 예시 문장</div></div>
    <div class="stat"><div class="stat-num">4</div><div class="stat-label">질문 유형</div></div>
    <div class="stat"><div class="stat-num">0</div><div class="stat-label">어려운 단어</div></div>
  </div>
</section>

<div class="filter-wrap">
  <button class="filter-btn active" onclick="filter('all', this)">전체 30</button>
  <button class="filter-btn" onclick="filter('whatif', this)">🧡 What if — 상상 질문</button>
  <button class="filter-btn" onclick="filter('why', this)">💙 Why — 이유 질문</button>
  <button class="filter-btn" onclick="filter('tell', this)">💚 Tell me — 확장 질문</button>
  <button class="filter-btn" onclick="filter('how', this)">💜 How — 방법 질문</button>
</div>

<div class="grid" id="grid"></div>

<section class="cta-wrap">
  <h2>오늘 저녁 식사 시간에<br>딱 하나만 써보세요!</h2>
  <p>영어는 공부가 아니라 대화니까요.<br>더 많은 콘텐츠는 인스타그램 프로필에서 확인하세요.</p>
  <a href="#" class="cta-btn">@ 인스타 프로필 바로가기 →</a>
</section>

<script>
const sentences = [
  { cat: 'whatif', en: 'What if it rains tomorrow?', ko: '내일 비가 오면 어떻게 될까?', tip: '날씨로 시작하면 아이가 쉽게 상상할 수 있어요.' },
  { cat: 'whatif', en: 'What if you were the main character?', ko: '네가 주인공이라면 어땠을까?', tip: '책이나 영화 보고 난 후 써보세요.' },
  { cat: 'whatif', en: 'What if animals could talk?', ko: '동물이 말을 할 수 있다면?', tip: '아이들이 가장 좋아하는 질문 중 하나예요!' },
  { cat: 'whatif', en: 'What if you had a superpower?', ko: '네가 초능력이 있다면?', tip: '어떤 능력을 갖고 싶은지 이유도 물어보세요.' },
  { cat: 'whatif', en: 'What if school was only two days a week?', ko: '학교가 일주일에 이틀만 있다면?', tip: '나머지 시간을 어떻게 쓸지 상상하게 해줘요.' },
  { cat: 'whatif', en: 'What if we lived underwater?', ko: '우리가 물속에서 산다면 어떨까?', tip: '과학적 상상력도 함께 자극할 수 있어요.' },
  { cat: 'whatif', en: 'What if you could fly?', ko: '날 수 있다면 어디를 가고 싶어?', tip: '대답 후 "Why?" 로 꼭 이어가세요!' },
  { cat: 'whatif', en: 'What if there were no colors?', ko: '세상에 색깔이 없다면 어떨까?', tip: '그림 그리며 이야기하면 더 재미있어요.' },
  { cat: 'whatif', en: 'What if you were invisible for one day?', ko: '하루 동안 투명인간이 된다면?', tip: '무엇을 하고 싶은지 이야기해보세요.' },
  { cat: 'whatif', en: 'What if you could go back in time?', ko: '과거로 돌아갈 수 있다면 어디로 가고 싶어?', tip: '역사 수업 연계 대화로 활용해보세요.' },

  { cat: 'why', en: 'Why do you think so?', ko: '너는 왜 그렇게 생각해?', tip: '모든 대화의 필수 후속 질문이에요.' },
  { cat: 'why', en: 'Why is that your favorite?', ko: '왜 그게 제일 좋아?', tip: '좋아하는 것을 주제로 시작하면 말문이 트여요.' },
  { cat: 'why', en: 'Why do you think the character did that?', ko: '주인공이 왜 그렇게 했을까?', tip: '책이나 영화 속 장면에 연결해보세요.' },
  { cat: 'why', en: 'Why is it important to share?', ko: '나눠 쓰는 게 왜 중요할까?', tip: '가치관과 영어를 동시에 배울 수 있어요.' },
  { cat: 'why', en: 'Why do you think we have rules?', ko: '우리에게 규칙이 왜 있을까?', tip: '학교나 집의 규칙을 예로 들어보세요.' },
  { cat: 'why', en: 'Why do plants need sunlight?', ko: '식물은 왜 햇빛이 필요할까?', tip: '과학 개념과 연결한 영어 대화예요.' },
  { cat: 'why', en: 'Why did you choose that?', ko: '왜 그걸 선택했어?', tip: '아이의 선택에 항상 이유를 물어보세요.' },
  { cat: 'why', en: 'Why is it good to be kind?', ko: '친절한 게 왜 좋을까?', tip: '인성 교육과 영어를 함께 할 수 있어요.' },
  { cat: 'why', en: 'Why do we need sleep?', ko: '우리는 왜 잠을 자야 할까?', tip: '잠자리 전 대화로 활용해보세요.' },
  { cat: 'why', en: 'Why do you think the sky is blue?', ko: '하늘이 왜 파랄까?', tip: '"I think..." 로 시작하는 연습을 함께 해요.' },

  { cat: 'tell', en: 'Tell me more about that.', ko: '그것에 대해 더 말해봐.', tip: '아이의 이야기를 늘리는 최고의 표현이에요.' },
  { cat: 'tell', en: 'What do you mean by that?', ko: '그게 무슨 뜻이야?', tip: '설명하는 능력을 키워줘요.' },
  { cat: 'tell', en: 'How did that make you feel?', ko: '그때 기분이 어땠어?', tip: '감정 어휘를 자연스럽게 늘릴 수 있어요.' },
  { cat: 'tell', en: 'What was the best part?', ko: '어떤 부분이 제일 좋았어?', tip: '하루 마무리 대화로 제격이에요.' },
  { cat: 'tell', en: 'What would you do differently?', ko: '다시 한다면 어떻게 할 거야?', tip: '반성과 성장의 사고력을 키워줘요.' },

  { cat: 'how', en: 'How can we fix that?', ko: '어떻게 하면 고칠 수 있을까?', tip: '문제 해결력을 함께 키울 수 있어요.' },
  { cat: 'how', en: 'How would you help a friend who is sad?', ko: '슬픈 친구를 어떻게 도와줄 거야?', tip: '공감 능력과 영어를 동시에 키워요.' },
  { cat: 'how', en: 'How does that work?', ko: '그게 어떻게 되는 거야?', tip: '주변 모든 것에 호기심을 가지게 해줘요.' },
  { cat: 'how', en: 'How did you figure that out?', ko: '어떻게 알아냈어?', tip: '아이의 성취를 구체적으로 칭찬하는 표현이에요.' },
  { cat: 'how', en: 'How can we make this better?', ko: '이걸 어떻게 더 좋게 만들 수 있을까?', tip: '창의성과 개선 사고력을 함께 자극해요.' },
];

const catLabel = { whatif: 'What if', why: 'Why', tell: 'Tell me', how: 'How' };

function render(data) {
  const grid = document.getElementById('grid');
  grid.innerHTML = '';
  data.forEach((s, i) => {
    const div = document.createElement('div');
    div.className = `card cat-${s.cat}`;
    div.style.animationDelay = `${i * 0.04}s`;
    div.innerHTML = `
      <div class="card-num">No. ${(sentences.indexOf(s)+1).toString().padStart(2,'0')}</div>
      <span class="cat-pill">${catLabel[s.cat]}</span>
      <div class="en">${s.en}</div>
      <div class="ko">${s.ko}</div>
      <div class="tip">${s.tip}</div>
    `;
    grid.appendChild(div);
  });
}

function filter(cat, btn) {
  document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  render(cat === 'all' ? sentences : sentences.filter(s => s.cat === cat));
}

render(sentences);
</script>
</body>
</html>
