<html lang="ko">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>사고력 영어 가이드</title>
<link href="https://fonts.googleapis.com/css2?family=Gowun+Dodum&family=Noto+Sans+KR:wght@400;700&family=Space+Grotesk:wght@500;700&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root { --cream: #FFF8F0; --peach: #FFD9B7; --coral: #FF7F5C; --deep: #2D1B0E; --mid: #6B3F2A; }
  body { background: var(--cream); color: var(--deep); font-family: 'Noto Sans KR', sans-serif; }

  /* NAVIGATION TABS */
  .nav-tabs { display: flex; justify-content: center; background: #fff; border-bottom: 1px solid var(--peach); position: sticky; top: 0; z-index: 100; }
  .nav-tab { padding: 16px 24px; cursor: pointer; font-weight: 700; color: #A08070; border-bottom: 3px solid transparent; }
  .nav-tab.active { color: var(--coral); border-bottom: 3px solid var(--coral); }

  .content-section { display: none; min-height: 80vh; }
  .content-section.active { display: block; }

  /* CATEGORY LIST VIEW */
  .category-container { max-width: 800px; margin: 40px auto; padding: 0 20px; }
  .category-card { 
    background: #fff; border-radius: 15px; padding: 30px; margin-bottom: 20px; 
    border: 1px solid var(--peach); display: flex; justify-content: space-between; align-items: center;
    cursor: pointer; transition: 0.2s;
  }
  .category-card:hover { transform: translateY(-3px); box-shadow: 0 10px 20px rgba(0,0,0,0.05); }
  .category-info h3 { font-family: 'Gowun Dodum'; font-size: 20px; margin-bottom: 5px; }
  .category-info p { font-size: 14px; color: var(--mid); }

  /* CONTENT DETAIL VIEW */
  .detail-view { max-width: 1000px; margin: 0 auto; padding: 20px; display: none; }
  .detail-header { text-align: center; padding: 40px 0; background: var(--deep); color: #fff; border-radius: 20px; margin-bottom: 30px; }
  .download-bar { background: #fff; padding: 15px; border-radius: 10px; margin-bottom: 20px; text-align: center; border: 1px dashed var(--coral); }
  .pdf-link { color: var(--coral); text-decoration: none; font-weight: bold; }

  .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 15px; }
  .card { background: #fff; padding: 20px; border-radius: 15px; border-left: 5px solid var(--coral); border: 1px solid #eee; border-left: 5px solid var(--coral); }
  .back-btn { margin-bottom: 20px; cursor: pointer; color: var(--mid); display: inline-block; font-weight: bold; }

  /* HOME */
  .welcome { text-align: center; padding: 100px 20px; }
</style>
</head>
<body>

<nav class="nav-tabs">
  <div class="nav-tab active" onclick="showTab('home', this)">홈</div>
  <div class="nav-tab" onclick="showTab('expressions', this)">원어민이 쓰는 덩어리 표현</div>
</nav>

<section id="home" class="content-section active">
  <div class="welcome">
    <h1 style="font-family:'Gowun Dodum'; font-size: 32px;">사고력 영어 대화 가이드</h1>
    <p style="margin-top:20px;">원어민 표현 탭에서 상황별 학습 자료를 확인하세요.</p>
  </div>
</section>

<section id="expressions" class="content-section">
  <div id="category-list" class="category-container">
    </div>

  <div id="detail-view" class="detail-view">
    <div class="back-btn" onclick="hideDetail()">← 뒤로가기</div>
    <div id="detail-content"></div>
  </div>
</section>

<script>
// 1. 카테고리 데이터 (여기에 추가하면 자동으로 늘어납니다)
const categories = [
  {
    id: 'cat1',
    title: '아이 사고력을 키우는 질문 30',
    desc: 'Yes/No 대답을 넘어 생각이 깊어지는 질문 모음',
    pdf: 'category1_questions.pdf',
    items: [
      { en: 'What if it rains tomorrow?', ko: '내일 비가 오면 어떻게 될까?', tip: '날씨로 시작하면 아이가 쉽게 상상할 수 있어요.' },
      { en: 'Why do you think so?', ko: '너는 왜 그렇게 생각해?', tip: '모든 대화의 필수 후속 질문이에요.' },
      { en: 'Tell me more about that.', ko: '그것에 대해 더 말해봐.', tip: '아이의 이야기를 늘리는 최고의 표현이에요.' }
    ]
  }
  // 나중에 카테고리를 추가하려면 여기에 { id: 'cat2', ... } 형식으로 넣으시면 됩니다.
];

// 탭 전환
function showTab(id, el) {
  document.querySelectorAll('.content-section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(t => t.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  el.classList.add('active');
  hideDetail(); // 탭 이동 시 상세페이지는 닫음
}

// 카테고리 목록 그리기
function renderCategories() {
  const list = document.getElementById('category-list');
  list.innerHTML = categories.map(cat => `
    <div class="category-card" onclick="showDetail('${cat.id}')">
      <div class="category-info">
        <h3>${cat.title}</h3>
        <p>${cat.desc}</p>
      </div>
      <div style="color:var(--coral); font-weight:bold;">보기 →</div>
    </div>
  `).join('');
}

// 상세 페이지 열기
function showDetail(id) {
  const cat = categories.find(c => c.id === id);
  document.getElementById('category-list').style.display = 'none';
  const detail = document.getElementById('detail-view');
  detail.style.display = 'block';

  document.getElementById('detail-content').innerHTML = `
    <div class="detail-header">
      <h2>${cat.title}</h2>
    </div>
    <div class="download-bar">
      <span>📄 이 카테고리 전체 자료를 보관하세요! </span>
      <a href="${cat.pdf}" download class="pdf-link">PDF 다운로드 받기</a>
    </div>
    <div class="grid">
      ${cat.items.map(item => `
        <div class="card">
          <div style="font-weight:bold; color:var(--coral); margin-bottom:10px;">Expression</div>
          <div style="font-size:18px; font-weight:700; margin-bottom:8px;">${item.en}</div>
          <div style="color:var(--mid); font-size:14px;">${item.ko}</div>
          <div style="margin-top:10px; font-size:12px; color:#A08070; border-top:1px dashed #eee; padding-top:10px;">💡 ${item.tip}</div>
        </div>
      `).join('')}
    </div>
  `;
}

function hideDetail() {
  document.getElementById('category-list').style.display = 'block';
  document.getElementById('detail-view').style.display = 'none';
}

renderCategories();
</script>
</body>
</html>
