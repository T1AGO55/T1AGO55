from pathlib import Path

svg = r'''<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="320" viewBox="0 0 1200 320" role="img" aria-labelledby="title desc">
  <title id="title">Tiago Toshimitsu — Software Engineering Student</title>
  <desc id="desc">A minimalist black and violet futuristic digital landscape with a glowing horizon and geometric grid.</desc>
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0" stop-color="#07070D"/>
      <stop offset=".55" stop-color="#100B20"/>
      <stop offset="1" stop-color="#1D0D36"/>
    </linearGradient>
    <linearGradient id="horizon" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0" stop-color="#6D28D9" stop-opacity="0"/>
      <stop offset=".5" stop-color="#C084FC" stop-opacity=".95"/>
      <stop offset="1" stop-color="#6D28D9" stop-opacity="0"/>
    </linearGradient>
    <linearGradient id="mountain" x1="0" y1="0" x2="0" y2="1">
      <stop offset="0" stop-color="#3B1769" stop-opacity=".8"/>
      <stop offset="1" stop-color="#090711" stop-opacity="1"/>
    </linearGradient>
    <radialGradient id="glow" cx="50%" cy="72%" r="52%">
      <stop offset="0" stop-color="#9333EA" stop-opacity=".34"/>
      <stop offset="1" stop-color="#9333EA" stop-opacity="0"/>
    </radialGradient>
    <pattern id="stars" width="92" height="68" patternUnits="userSpaceOnUse">
      <circle cx="9" cy="12" r="1" fill="#E9D5FF" opacity=".5"/>
      <circle cx="59" cy="37" r=".8" fill="#C4B5FD" opacity=".4"/>
      <circle cx="82" cy="7" r=".7" fill="#FFFFFF" opacity=".35"/>
    </pattern>
    <clipPath id="round">
      <rect width="1200" height="320" rx="18"/>
    </clipPath>
  </defs>
  <g clip-path="url(#round)">
    <rect width="1200" height="320" fill="url(#bg)"/>
    <rect width="1200" height="250" fill="url(#stars)"/>
    <rect width="1200" height="320" fill="url(#glow)"/>
    <g fill="none" stroke="#8B5CF6" stroke-width="1" opacity=".23">
      <path d="M0 74H1200 M0 106H1200 M0 138H1200 M0 170H1200"/>
      <path d="M90 0V220 M210 0V220 M330 0V220 M450 0V220 M570 0V220 M690 0V220 M810 0V220 M930 0V220 M1050 0V220 M1170 0V220"/>
    </g>
    <circle cx="900" cy="105" r="58" fill="#A855F7" opacity=".08"/>
    <circle cx="900" cy="105" r="41" fill="none" stroke="#A78BFA" stroke-width="1" opacity=".35"/>
    <circle cx="900" cy="105" r="31" fill="none" stroke="#C084FC" stroke-width="1" opacity=".28"/>
    <path d="M0 220 L150 151 L238 194 L355 123 L480 206 L612 146 L725 205 L847 132 L977 203 L1090 158 L1200 215 V320 H0Z" fill="url(#mountain)" opacity=".88"/>
    <path d="M0 245 L155 196 L275 229 L430 179 L560 236 L715 185 L850 229 L1015 188 L1120 220 L1200 200 V320 H0Z" fill="#08070F" opacity=".9"/>
    <path d="M0 230H1200" stroke="url(#horizon)" stroke-width="2"/>
    <g fill="none" stroke="#A855F7" stroke-width="1" opacity=".5">
      <path d="M0 254H1200 M0 272H1200 M0 292H1200 M0 314H1200"/>
      <path d="M600 230L90 320 M600 230L230 320 M600 230L370 320 M600 230L490 320 M600 230L710 320 M600 230L830 320 M600 230L970 320 M600 230L1110 320"/>
    </g>
    <g fill="none" stroke="#C084FC" stroke-width="1.2" opacity=".72">
      <path d="M62 54h35v-16h26"/>
      <circle cx="127" cy="38" r="2" fill="#C084FC"/>
      <path d="M1032 48h32v18h43"/>
      <circle cx="1107" cy="66" r="2" fill="#C084FC"/>
      <path d="M1014 144h30v-13h18"/>
      <circle cx="1062" cy="131" r="2" fill="#C084FC"/>
    </g>
    <rect x="62" y="65" width="4" height="100" rx="2" fill="#A855F7"/>
    <text x="88" y="111" fill="#FFFFFF" font-family="Inter, Segoe UI, Arial, sans-serif" font-size="43" font-weight="700" letter-spacing="-.8">Tiago Toshimitsu</text>
    <text x="90" y="145" fill="#C4B5FD" font-family="Inter, Segoe UI, Arial, sans-serif" font-size="15" font-weight="600" letter-spacing="3.1">SOFTWARE ENGINEERING STUDENT</text>
    <text x="90" y="174" fill="#A1A1AA" font-family="Inter, Segoe UI, Arial, sans-serif" font-size="13" letter-spacing="1.1">JAVA  /  SPRING BOOT  /  FLUTTER  /  PYTHON</text>
    <g transform="translate(1010 255)">
      <circle r="22" fill="#140D22" stroke="#A855F7" stroke-opacity=".6"/>
      <path d="M-8 -3l8 -8 8 8 M0 -11v17 M-8 5h16" fill="none" stroke="#C4B5FD" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
    </g>
    <text x="1138" y="292" text-anchor="end" fill="#A78BFA" opacity=".75" font-family="monospace" font-size="10" letter-spacing="2">BUILD • LEARN • EVOLVE</text>
  </g>
</svg>
'''

out = Path("/mnt/data/banner-tiago.svg")
out.write_text(svg, encoding="utf-8")
print(f"Banner SVG criado: {out} ({out.stat().st_size} bytes)")
