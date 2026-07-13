<svg width="1000" height="200" viewBox="0 0 1000 200" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <style>
      @import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&amp;family=DM+Mono:wght@400;500&amp;display=swap');

      .bg { fill: #0A0E14; }
      .grid line { stroke: #1B2233; stroke-width: 1; }
      .name {
        font-family: 'DM Serif Display', Georgia, serif;
        font-size: 58px;
        fill: #EAF4F4;
        letter-spacing: 1px;
      }
      .accent { fill: #5EEAD4; }
      .role {
        font-family: 'DM Mono', 'Courier New', monospace;
        font-size: 16px;
        fill: #8B96A8;
        letter-spacing: 0.5px;
      }
      .tag {
        font-family: 'DM Mono', 'Courier New', monospace;
        font-size: 11px;
        fill: #E3A857;
        letter-spacing: 3px;
      }
      .rule { stroke: #1B2233; stroke-width: 1; }

      .fade-in {
        opacity: 0;
        animation: fadeIn 1.1s ease-out forwards;
      }
      .fade-in.d2 { animation-delay: 0.25s; }
      .fade-in.d3 { animation-delay: 0.5s; }
      @keyframes fadeIn {
        from { opacity: 0; transform: translateY(6px); }
        to   { opacity: 1; transform: translateY(0); }
      }

      .cursor {
        fill: #5EEAD4;
        animation: blink 1.1s steps(1) infinite;
      }
      @keyframes blink {
        0%, 45% { opacity: 1; }
        50%, 100% { opacity: 0; }
      }

      .scan {
        fill: url(#scanGrad);
        animation: sweep 5s ease-in-out infinite;
      }
      @keyframes sweep {
        0%   { transform: translateX(-120px); opacity: 0; }
        10%  { opacity: 0.5; }
        50%  { opacity: 0.5; }
        90%  { opacity: 0; }
        100% { transform: translateX(1000px); opacity: 0; }
      }
    </style>

    <linearGradient id="scanGrad" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#5EEAD4" stop-opacity="0" />
      <stop offset="50%" stop-color="#5EEAD4" stop-opacity="0.35" />
      <stop offset="100%" stop-color="#5EEAD4" stop-opacity="0" />
    </linearGradient>
  </defs>

  <rect class="bg" width="1000" height="200" />

  <!-- faint structural grid, restrained -->
  <g class="grid" opacity="0.5">
    <line x1="0" y1="40" x2="1000" y2="40" />
    <line x1="0" y1="160" x2="1000" y2="160" />
    <line x1="60" y1="0" x2="60" y2="200" />
  </g>

  <!-- scanning light sweep -->
  <rect class="scan" x="0" y="0" width="90" height="200" />

  <!-- mark -->
  <g class="fade-in">
    <rect x="60" y="66" width="6" height="46" class="accent" />
  </g>

  <!-- wordmark -->
  <text x="86" y="105" class="name fade-in">Codurrr</text>

  <!-- role line -->
  <g class="fade-in d2">
    <text x="88" y="134" class="role">full-stack developer — javascript-first</text>
    <rect x="470" y="120" width="9" height="16" class="cursor" />
  </g>

  <line x1="60" y1="160" x2="940" y2="160" class="rule fade-in d3" />

  <text x="940" y="182" text-anchor="end" class="tag fade-in d3">RAJASTHAN · INDIA</text>
</svg>
