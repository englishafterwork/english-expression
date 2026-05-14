<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>사고력 영어 | 원어민 표현 대화하기</title>
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
  }

  body {
    background: var(--cream);
    color: var(--deep);
    font-family: 'Noto Sans KR', sans-serif;
    min-height: 100vh;
  }

  /* TOP NAVIGATION TABS */
  .nav-tabs {
    display: flex;
    justify-content: center;
    background: #fff;
    border-bottom: 1px solid var(--peach);
    position: sticky;
    top: 0;
    z-index: 100;
  }
  .nav-tab {
    padding: 16px 24px;
    cursor: pointer;
    font-weight: 700;
    color: #A08070;
    transition: all 0.2s;
    border-bottom: 3px solid transparent;
  }
  .nav-tab.active {
    color: var(--coral);
    border-bottom: 3px solid var(--coral);
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
  .hero-tag {
    display: inline-block;
    background: var(--coral);
    color: #fff;
    font-size: 12px;
    font-weight: 700;
    padding: 6px 16px;
    border-radius: 100px;
    margin-bottom: 20px;
  }
  .hero h1 {
    font-family: 'Gowun Dodum', serif;
    font-size: clamp(26px, 6vw, 42px);
    line-height: 1.35;
    margin-bottom: 16px;
  }
  .hero h1 em { color: var(--peach); font-style: normal; }

  /* CONTENT AREAS */
  .content-section { display: none; }
  .content-section.active { display: block; }

  /* GRID & CARDS */
  .filter-wrap { padding: 28px 20px 8px; display: flex; gap: 8px; flex-wrap: wrap; justify-content: center; }
  .filter-btn { padding: 8px 18px; border-radius: 100px; border: 1.5px solid var(--coral); background: transparent; color: var(--coral); font-size: 13px; cursor: pointer; font-weight: 700; transition: 0.2s; }
  .filter-btn.active { background: var(--coral); color: #fff; }

  .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 16px; padding: 20px 20px 60px; max-width: 1000px; margin: 0 auto; }
  .card { background: #fff; border-radius: 18px; padding: 22px; border: 1.5px solid #EDE3D8; animation: fadeUp 0.4s both; border-left: 4px solid var(--coral); }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(16px); } to { opacity: 1; transform: translateY(0); } }

  .en { font-family: 'Space Grotesk', sans-serif; font-size: 17px; font-weight: 700; margin-bottom: 8px; }
  .ko { font-size: 14px; color: var(--mid); }
  .tip { margin-top: 10px; padding-top: 10px; border-top: 1px dashed #EDE3D8; font-size: 12px; color: #A08070; }

  .welcome-msg { text-align: center; padding: 80px 24px; color: var(--mid); }
  
  /* DOWNLOAD BUTTON */
  .download-btn {
    display: inline-block;
    background-color: var(--coral);
    color: white;
    padding: 14px 28px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: bold;
    margin-top: 30px;
    box-shadow: 0 4px 15px rgba(255,127,92,0.3);
    transition: transform 0.2s;
  }
  .download-btn:hover { transform: scale(1.05); }

  /* CTA */
  .cta-wrap { background: var(--deep); color: var(--cream); text-align: center; padding: 48px 24px; }
  .cta-link { color: var(--peach); text-decoration: none; font-weight: bold; }
</style>
</head>
<body>

<nav class="nav-tabs">
  <div class="nav-tab active" onclick="showTab('home', this)">홈</div>
  <div class="nav-tab" onclick="showTab('phrases', this)">원어민이 쓰는 덩어리 표현</div>
</nav>

<section id="home" class="content-section active">
  <div class="welcome-msg">
    <div style="font-size: 50px; margin-bottom: 20px;">👋</div>
    <h2>영어 사고력을 키우는 대화 가이드</h2>
    <p style="margin-top:20px; line-height: 1.6;">
      상단 메뉴에서 <strong>'원어민이 쓰는 덩어리 표현'</strong>을 클릭하여<br>
      아이와 함께 나눌 수 있는 30가지 질문을 확인해보세요.
    </p>
    
    <a href="english_questions_30.pdf" download class="download-btn">
      📥 전체 질문 리스트 PDF 다운로드
    </a>
  </div>
</section>

<section id="phrases" class="content-section">
  <div class="hero">
    <div class="hero-tag">원어민 부모의 비법 질문법</div>
    <h1>아이의 영어 사고력을 깨우는<br><em>실전 질문 30</em></h1>
  </div>

  <div class="filter-wrap">
    <button class="filter-btn active" onclick="filter('all', this)">전체 30</button>
    <button class="filter-btn" onclick="filter('whatif', this)">🧡 What if</button>
    <button class="filter-btn" onclick="filter('why', this)">💙 Why</button>
    <button class="filter-btn" onclick="filter('tell', this)">💚 Tell me</button>
    <button class="filter-btn" onclick="filter('how', this)">💜 How</button>
  </div>

  <div class="grid" id="grid"></div>
</section>

<section class="cta-wrap">
  <h2>오늘 저녁 식사 시간에 딱 하나만 써보세요!</h2>
  <p style="margin: 15px 0; color: #A08070;">영어는 공부가 아니라 대화니까요.</p>
  <a href="#" class="cta-link">@ 인스타그램 프로필 바로가기 →</a>
</section>

<script>
// 탭 전환 자바스크립트
function showTab(tabId, el) {
  document.querySelectorAll('.content-section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
  
  document.getElementById(tabId).classList.add('active');
  el.classList.add('active');
  window.scrollTo(0,0);
}

// 질문 데이터
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
  { cat: 'how', en: 'How can we make this better?', ko: '이걸 어떻게 더 좋게 만들 수 있을까?', tip: '창의성과 개선 사고력을 함께 자극해요.' }
];

const catLabel = { whatif: 'What if', why: 'Why', tell: 'Tell me', how: 'How' };

// 질문 렌더링 함수
function render(data) {
  const grid = document.getElementById('grid');
  grid.innerHTML = '';
  data.forEach((s, i) => {
    const div = document.createElement('div');
    div.className = `card cat-${s.cat}`;
    div.style.animationDelay = `${i * 0.04}s`;
    div.innerHTML = `
      <div style="font-size:11px; color:#C8B4A0; margin-bottom:8px;">No. ${(sentences.indexOf(s)+1).toString().padStart(2,'0')}</div>
      <span style="font-weight:bold; color:var(--coral); font-size:12px; margin-bottom:8px; display:block;">${catLabel[s.cat]}</span>
      <div class="en">${s.en}</div>
      <div class="ko">${s.ko}</div>
      <div class="tip">💡 ${s.tip}</div>
    `;
    grid.appendChild(div);
  });
}

// 필터 함수
function filter(cat, btn) {
  document.querySelectorAll('.filter-btn').forEach(b => b.classList.remove('active'));
  btn.classList.add('active');
  render(cat === 'all' ? sentences : sentences.filter(s => s.cat === cat));
}

// 초기 실행
render(sentences);
</script>
</body>
</html>
