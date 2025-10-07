<!-- File: gears-mindmap-tri-thuc-tinh-cam-y-chi.html -->
<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mối quan hệ: Tri thức – Tình cảm – Ý chí (Mô hình 3 bánh răng)</title>
  <style>
    :root{
      --bg:#f6f4ee;
      --ink:#222;
      --accent:#3a7;
      --knowledge:#f4a62a;   /* Tri thức */
      --emotion:#e4684b;     /* Tình cảm */
      --will:#4c86af;        /* Ý chí */
      --panel:#ffffffcc;
      --ring:#1118;
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font:16px/1.5 system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, "Noto Sans", "Liberation Sans", sans-serif;
      color:var(--ink);
      background:radial-gradient(2000px 1200px at 60% -10%, #fff 0 30%, var(--bg) 70% 100%);
    }
    header{padding:16px 20px 0}
    h1{font-size:clamp(20px,4vw,32px); margin:0 0 6px}
    p.lead{margin:0 0 14px; opacity:.9}
    .wrap{
      display:grid;
      grid-template-columns: 1.1fr 0.9fr;
      gap:18px;
      padding:16px 20px 24px;
    }
    @media (max-width: 980px){
      .wrap{grid-template-columns:1fr; padding:12px}
    }
    .stage{
      position:relative;
      border-radius:18px;
      background:#fff;
      box-shadow:0 8px 30px #0001, inset 0 0 0 1px #00000010;
      overflow:hidden;
      min-height:480px;
    }
    svg{display:block; width:100%; height:min(72vh,720px)}
    /* HUD tốc độ */
    .hud{
      position:absolute; right:10px; top:10px;
      background:var(--panel); backdrop-filter: blur(6px);
      border-radius:12px; padding:10px 12px;
      box-shadow:0 10px 24px #0002, inset 0 0 0 1px #00000012;
      font-variant-numeric:tabular-nums;
      min-width:220px;
    }
    .speed{display:grid; grid-template-columns:78px 1fr auto; gap:6px; align-items:center; margin:6px 0}
    .bar{height:8px; border-radius:6px; background:#0001; overflow:hidden}
    .bar > i{display:block; height:100%; background:linear-gradient(90deg,#0002,#0006)}
    .hud small{opacity:.75}
    .panel{
      background:var(--panel);
      backdrop-filter: blur(6px);
      border-radius:16px;
      box-shadow:0 10px 25px #0001, inset 0 0 0 1px #00000012;
      padding:16px;
    }
    .panel h2{margin:0 0 8px; font-size:18px}
    .panel .row{display:grid; grid-template-columns:1fr auto; align-items:center; gap:10px; margin:10px 0}
    .panel input[type=range]{width:100%}
    .badge{display:inline-block; padding:.15rem .5rem; border-radius:.65rem; font-weight:600; font-size:.85rem}
    .b-knowledge{background:var(--knowledge); color:#000}
    .b-emotion{background:var(--emotion); color:#fff}
    .b-will{background:var(--will); color:#fff}
    small.hint{opacity:.7}
    .legend{
      display:grid; gap:8px; margin-top:8px;
      grid-template-columns: repeat(3, minmax(0,1fr));
    }
    .mind{
      margin-top:14px; background:#fff; border-radius:14px; padding:12px;
      box-shadow: inset 0 0 0 1px #00000010;
    }
    .mind h3{margin:0 0 8px; font-size:16px}
    .mind .flow{display:flex; flex-wrap:wrap; gap:8px; align-items:center}
    .pill{padding:.4rem .6rem; border-radius:999px; font-weight:600; box-shadow:inset 0 0 0 1px #0002}
    .pill.k{background:var(--knowledge)}
    .pill.e{background:var(--emotion); color:#fff}
    .pill.w{background:var(--will); color:#fff}
    .pill.a{background:#ddd}
    .arrow{font-weight:900}
    .stat{font-feature-settings:"tnum"; font-variant-numeric:tabular-nums}
    .explain{margin-top:10px; padding:10px; border-radius:10px; background:#00000008}
    footer{padding:6px 20px 20px; opacity:.7; font-size:13px}
    input:focus-visible{outline:2px solid var(--accent); outline-offset:2px; border-radius:6px}
    .spin-halo { fill:none; stroke:var(--ring); stroke-width:10; stroke-opacity:.18; stroke-linecap:round }
    .label{ font-weight:800; letter-spacing:.3px; }
  </style>
</head>
<body>
  <header>
    <h1>Mô hình 3 bánh răng: <span class="badge b-knowledge">Tri thức</span> · <span class="badge b-emotion">Tình cảm</span> · <span class="badge b-will">Ý chí</span></h1>
    <p class="lead">Hãy xem <strong>Tình cảm</strong> cấp năng lượng, <strong>Ý chí</strong> giữ nhịp & vượt trở lực, còn <strong>Tri thức</strong> là bánh răng trung tâm kết nối và định hướng chuyển động.</p>
  </header>

  <main class="wrap">
    <!-- Sân khấu bánh răng -->
    <section class="stage" aria-label="Mô phỏng 3 bánh răng liên kết">
      <svg id="scene" viewBox="0 0 900 600" role="img" aria-labelledby="title desc">
        <title id="title">Ba bánh răng: Tri thức, Tình cảm, Ý chí</title>
        <desc id="desc">Bánh răng trung tâm là Tri thức. Bánh răng bên trái dưới là Tình cảm (cấp năng lượng). Bánh răng bên phải dưới là Ý chí (duy trì chuyển động). Chúng ăn khớp và quay ngược chiều nhau.</desc>

        <!-- Halos tạo cảm giác chuyển động -->
        <circle class="spin-halo" cx="470" cy="250" r="135"/>
        <circle class="spin-halo" cx="300" cy="410" r="95"/>
        <circle class="spin-halo" cx="620" cy="430" r="95"/>

        <!-- Group cho từng bánh răng -->
        <g id="gear-knowledge" transform="translate(470,250) rotate(0)"></g>
        <g id="gear-emotion"   transform="translate(300,410) rotate(0)"></g>
        <g id="gear-will"      transform="translate(620,430) rotate(0)"></g>

        <!-- Nhãn -->
        <g aria-hidden="true">
          <text x="470" y="260" text-anchor="middle" class="label" style="font-size:22px; fill:#111;">TRI THỨC</text>
          <text x="300" y="420" text-anchor="middle" class="label" style="font-size:18px; fill:#111;">TÌNH CẢM</text>
          <text x="620" y="440" text-anchor="middle" class="label" style="font-size:18px; fill:#111;">Ý CHÍ</text>
        </g>

        <!-- Mũi tên quan hệ -->
        <defs>
          <marker id="arrow" markerWidth="10" markerHeight="7" refX="9" refY="3.5" orient="auto">
            <polygon points="0 0, 10 3.5, 0 7" fill="#111"/>
          </marker>
        </defs>
        <path d="M230 390 C210 300, 350 230, 430 230" fill="none" stroke="#111" stroke-width="2.5" marker-end="url(#arrow)"/>
        <text x="230" y="360" style="font-weight:700">Năng lượng ➜</text>

        <path d="M540 265 C680 300, 700 370, 655 405" fill="none" stroke="#111" stroke-width="2.5" marker-end="url(#arrow)"/>
        <text x="560" y="300" style="font-weight:700">Ổn định & bền bỉ ➜</text>
      </svg>

      <!-- HUD tốc độ & ổn định -->
      <div class="hud" aria-live="polite">
        <div class="speed"><strong style="color:#000">Tình cảm</strong><div class="bar"><i id="barE" style="width:0%"></i></div><b id="rpmE">0.0</b></div>
        <div class="speed"><strong style="color:#000">Tri thức</strong><div class="bar"><i id="barK" style="width:0%"></i></div><b id="rpmK">0.0</b></div>
        <div class="speed"><strong style="color:#000">Ý chí</strong><div class="bar"><i id="barW" style="width:0%"></i></div><b id="rpmW">0.0</b></div>
        <small>Ổn định (dao động Tri thức): <b id="stability">100</b>/100</small>
      </div>
    </section>

    <!-- Bảng điều khiển & Mindmap -->
    <aside class="panel" aria-label="Bảng điều khiển">
      <h2>Điều khiển mô phỏng</h2>

      <div class="row">
        <label for="energy"><strong>Năng lượng cảm xúc</strong> (rpm)</label>
        <output id="outEnergy" class="stat">40</output>
      </div>
      <input id="energy" type="range" min="0" max="120" value="40" step="1" aria-label="Năng lượng cảm xúc">

      <div class="row">
        <label for="will"><strong>Độ bền ý chí</strong> (bù trễ & giữ nhịp)</label>
        <output id="outWill" class="stat">0.6</output>
      </div>
      <input id="will" type="range" min="0" max="1" value="0.6" step="0.01" aria-label="Độ bền ý chí">

      <div class="row">
        <label for="friction"><strong>Ma sát/Lực cản (khó khăn)</strong> (cao ⇒ dễ chậm lại)</label>
        <output id="outFriction" class="stat">12</output>
      </div>
      <input id="friction" type="range" min="0" max="60" value="12" step="1" aria-label="Ma sát">

      <div class="legend">
        <div><span class="badge b-knowledge">Tri thức</span><br><small class="hint">Kết nối, định hướng, lan chuyển động sang hành động.</small></div>
        <div><span class="badge b-emotion">Tình cảm</span><br><small class="hint">Cấp năng lượng khởi động & tăng tốc.</small></div>
        <div><span class="badge b-will">Ý chí</span><br><small class="hint">Chống trượt, giữ nhịp trước biến động.</small></div>
      </div>

      <div class="mind" aria-label="Sơ đồ tư duy">
        <h3>Sơ đồ tư duy (dòng chảy)</h3>
        <div class="flow">
          <span class="pill k">Tri thức</span>
          <span class="arrow">➜</span>
          <span class="pill e">Tình cảm</span>
          <span class="arrow">➜</span>
          <span class="pill w">Ý chí</span>
          <span class="arrow">➜</span>
          <span class="pill a">Kết quả & Hành động</span>
        </div>
        <div id="explain" class="explain"></div>
        <small class="hint">Tri thức càng lớn, ảnh hưởng đến tình cảm và ý chí càng lan tỏa ⇒ hệ ít mất tốc khi gặp khó khăn.</small>
      </div>
    </aside>
  </main>

  <footer>
    © Mô hình minh họa học thuật: ba bánh răng tương tác. Kéo thanh để thấy quan hệ tốc độ.
  </footer>

  <script>
    // Tạo răng bánh răng theo tham số. (dạng tối giản để minh họa)
    function createGear({ teeth=12, radius=100, thickness=18, fill='#ccc', hub=26 }) {
      const g = document.createElementNS('http://www.w3.org/2000/svg','g');

      const body = document.createElementNS('http://www.w3.org/2000/svg','circle');
      body.setAttribute('r', radius);
      body.setAttribute('fill', fill);
      body.setAttribute('stroke', '#0008');
      body.setAttribute('stroke-width', '1.5');
      g.appendChild(body);

      for (let i=0;i<teeth;i++){
        const angle = (i/teeth)*360;
        const tooth = document.createElementNS('http://www.w3.org/2000/svg','rect');
        tooth.setAttribute('x', radius);
        tooth.setAttribute('y', -thickness/2);
        tooth.setAttribute('width', thickness);
        tooth.setAttribute('height', thickness);
        tooth.setAttribute('rx', 3);
        tooth.setAttribute('ry', 3);
        tooth.setAttribute('transform', `rotate(${angle})`);
        tooth.setAttribute('fill', fill);
        tooth.setAttribute('stroke', '#0008');
        tooth.setAttribute('stroke-width', '1.2');
        g.appendChild(tooth);
      }

      const hole = document.createElementNS('http://www.w3.org/2000/svg','circle');
      hole.setAttribute('r', hub);
      hole.setAttribute('fill', '#fff');
      hole.setAttribute('stroke', '#0008');
      hole.setAttribute('stroke-width','1');
      g.appendChild(hole);

      return g;
    }

    // Khởi tạo gears
    const gearK = createGear({teeth:12, radius:110, thickness:20, fill:getComputedStyle(document.documentElement).getPropertyValue('--knowledge')});
    const gearE = createGear({teeth:10, radius:75, thickness:18, fill:getComputedStyle(document.documentElement).getPropertyValue('--emotion')});
    const gearW = createGear({teeth:10, radius:75, thickness:18, fill:getComputedStyle(document.documentElement).getPropertyValue('--will')});

    document.getElementById('gear-knowledge').appendChild(gearK);
    document.getElementById('gear-emotion').appendChild(gearE);
    document.getElementById('gear-will').appendChild(gearW);

    // Tham số động
    const energyEl = document.getElementById('energy');
    const willEl = document.getElementById('will');
    const frictionEl = document.getElementById('friction');
    const outEnergy = document.getElementById('outEnergy');
    const outWill = document.getElementById('outWill');
    const outFriction = document.getElementById('outFriction');

    // HUD refs
    const rpmE = document.getElementById('rpmE');
    const rpmK = document.getElementById('rpmK');
    const rpmW = document.getElementById('rpmW');
    const barE = document.getElementById('barE');
    const barK = document.getElementById('barK');
    const barW = document.getElementById('barW');
    const stabilityEl = document.getElementById('stability');
    const explainEl = document.getElementById('explain');

    function fmt(n, d=0){ return (+n).toFixed(d); }
    energyEl.addEventListener('input', ()=> outEnergy.value = fmt(energyEl.value));
    willEl.addEventListener('input', ()=> outWill.value = fmt(willEl.value,2));
    frictionEl.addEventListener('input', ()=> outFriction.value = fmt(frictionEl.value));

    // Trạng thái quay
    let angleK=0, angleE=0, angleW=0;
    let last = performance.now();
    let velocityK = 0; // deg/s

    // Hằng số (bán kính “vòng chia” đơn giản)
    const rK=110, rE=75, rW=75;

    // Bộ đệm để ước lượng ổn định (dao động tốc độ Tri thức)
    const buf = [];
    const MAXN = 80;

    // Nội suy có đệm để mô phỏng "Ý chí giữ nhịp"
    function smoothStep(curr, target, stiffness){
      // Ý chí càng cao -> càng nhanh đạt target, ít rung.
      const alpha = Math.min(1, Math.max(0.05, stiffness));
      return curr + (target - curr) * alpha;
    }

    function rpmFromDegPerSec(dps){ return (dps/360)*60; }

    function normPct(x, cap){ return Math.min(100, Math.abs(x)/cap*100).toFixed(0)+'%'; }

    function stabilityScore(){
      if (buf.length < 6) return 100;
      const mean = buf.reduce((a,b)=>a+b,0)/buf.length;
      const sd = Math.sqrt(buf.reduce((s,x)=>s+(x-mean)*(x-mean),0)/buf.length);
      const norm = Math.min(1, sd/30); // chuẩn hóa theo biên dao động hợp lý
      return Math.round((1-norm)*100);
    }

    function animate(now){
      const dt = Math.min(0.05, (now - last)/1000); // s (clamp)
      last = now;

      // rpm -> deg/s
      const base = (+energyEl.value) * 360/60;
      const friction = +frictionEl.value;     // kháng tổng hợp
      const will = +willEl.value;             // giữ nhịp

      // Tốc độ mục tiêu cho Tri thức = năng lượng - ma sát (>=0)
      const targetK = Math.max(0, base - friction);
      velocityK = smoothStep(velocityK, targetK, 0.15 + will*0.75);

      // Cập nhật góc quay
      angleK = (angleK + velocityK * dt) % 360;

      // Truyền động ăn khớp: ω * r ≈ const, quay ngược chiều
      const vE = - velocityK * (rK / rE);
      const vW = - velocityK * (rK / rW);

      angleE = (angleE + vE * dt) % 360;
      angleW = (angleW + vW * dt) % 360;

      // Áp transform
      document.getElementById('gear-knowledge').setAttribute('transform', `translate(470,250) rotate(${angleK})`);
      document.getElementById('gear-emotion').setAttribute('transform', `translate(300,410) rotate(${angleE})`);
      document.getElementById('gear-will').setAttribute('transform', `translate(620,430) rotate(${angleW})`);

      // ---- HUD cập nhật ----
      const eRPM = rpmFromDegPerSec(vE);
      const kRPM = rpmFromDegPerSec(velocityK);
      const wRPM = rpmFromDegPerSec(vW);

      rpmE.textContent = eRPM.toFixed(1);
      rpmK.textContent = kRPM.toFixed(1);
      rpmW.textContent = wRPM.toFixed(1);

      // Thanh tốc độ: chuẩn hóa theo trần 220 rpm
      const cap = 220;
      barE.style.width = normPct(eRPM, cap);
      barK.style.width = normPct(kRPM, cap);
      barW.style.width = normPct(wRPM, cap);

      // Ổn định (dao động tốc độ Tri thức)
      buf.push(velocityK); if (buf.length>MAXN) buf.shift();
      stabilityEl.textContent = stabilityScore();

      // Giải thích theo chuỗi: Tri thức → Tình cảm → Ý chí → Kết quả/Hành động
      explainEl.innerHTML = `
        • <b>Tri thức</b> định hướng nhịp trung tâm: mục tiêu ~ <b>${(Math.max(0, base - friction)/360*60).toFixed(1)}</b> rpm.<br>
        • <b>Tình cảm</b> nhận ảnh hưởng từ Tri thức và tạo lực quay: hiện ~ <b>${eRPM.toFixed(1)}</b> rpm.<br>
        • <b>Ý chí</b> (mức ${will.toFixed(2)}) giữ nhịp trước <b>ma sát = ${friction.toFixed(0)}</b> ⇒ Tri thức ~ <b>${kRPM.toFixed(1)}</b> rpm (ổn định: <b>${stabilityEl.textContent}/100</b>).<br>
        • <b>Kết quả & Hành động</b> phản ánh nhịp chung: nhịp ổn định cao → hành động bền bỉ, hiệu quả hơn.
      `;

      requestAnimationFrame(animate);
    }
    requestAnimationFrame(animate);

    // Tooltip demo
    const stage = document.querySelector('.stage');
    stage.addEventListener('mousemove', e=>{
      stage.style.setProperty('--mx', e.offsetX+'px');
      stage.style.setProperty('--my', e.offsetY+'px');
    });
  </script>
</body>
</html>
