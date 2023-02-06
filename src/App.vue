<template>
<div class="wrapper">
  <div class="top-panel">
    <button class="show-grid" @click="sTabShow='grid'">show grid</button>
    <button class="show-list" @click="sTabShow='list'">show list</button>
    <button class="show-table" @click="sTabShow='table'">show table</button>

    <button class="prev-start" @click="fnStart">Start</button>
    <button class="prev" @click="fnPrev">Prev</button>
    <div class="page">{{iCurrentPage}}/{{iMaxPages-1}}</div>
    <button class="next" @click="fnNext">Next</button>
    <button class="next-end" @click="fnEnd">End</button>
  </div>
  <div class="tab grid" v-if="sTabShow=='grid'">
    <div class="cell" v-for="(sIcon, iIndex) in aPagedIcons" :key="iIndex">{{sIcon}}</div>
  </div>
  <div class="tab list" v-if="sTabShow=='list'"><pre>{{sList}}</pre></div>

  <div class="tab table">
  <table style="border-collapse:collapse;background:#FFFFFF;font-size:large;font-family:'Apple Color Emoji','Segoe UI Emoji','Segoe UI Symbol','Noto Color Emoji';text-align:center;min-width:365pt">
<tbody><tr>
<th colspan="17" style="background:#F8F8F8;font-size:small;font-family:sans-serif"></th></tr>
<tr style="background:#F8F8F8;font-size:small;font-family:sans-serif">
<td style="width:45pt">&nbsp;</td>
<td style="width:20pt">0</td>
<td style="width:20pt">1</td>
<td style="width:20pt">2</td>
<td style="width:20pt">3</td>
<td style="width:20pt">4</td>
<td style="width:20pt">5</td>
<td style="width:20pt">6</td>
<td style="width:20pt">7</td>
<td style="width:20pt">8</td>
<td style="width:20pt">9</td>
<td style="width:20pt">A</td>
<td style="width:20pt">B</td>
<td style="width:20pt">C</td>
<td style="width:20pt">D</td>
<td style="width:20pt">E</td>
<td style="width:20pt">F
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+00Ax
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+00A9: COPYRIGHT SIGN"><a href="/wiki/%C2%A9" class="mw-redirect" title="©">©️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+00AE: REGISTERED SIGN"><a href="/wiki/%C2%AE" class="mw-redirect" title="®">®️</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+203x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+203C: DOUBLE EXCLAMATION MARK"><a href="/wiki/!!_(disambiguation)" class="mw-redirect mw-disambig" title="!! (disambiguation)"> ‼️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+204x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2049: EXCLAMATION QUESTION MARK"><a href="/wiki/%E2%81%89" class="mw-redirect" title="⁉">⁉️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+212x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2122: TRADE MARK SIGN"><a href="/wiki/%E2%84%A2" class="mw-redirect" title="™">™️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+213x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2139: INFORMATION SOURCE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ℹ️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+219x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2194: LEFT RIGHT ARROW"><a href="/wiki/%E2%86%94" class="mw-redirect" title="↔">↔️</a>
</td>
<td title="U+2195: UP DOWN ARROW"><a href="/wiki/Vertical_(disambiguation)" class="mw-redirect mw-disambig" title="Vertical (disambiguation)"> ↕️</a>
</td>
<td title="U+2196: NORTH WEST ARROW"><a href="/wiki/%E2%86%96" class="mw-redirect" title="↖">↖️</a>
</td>
<td title="U+2197: NORTH EAST ARROW"><a href="/wiki/%E2%86%97" class="mw-redirect" title="↗">↗️</a>
</td>
<td title="U+2198: SOUTH EAST ARROW"><a href="/wiki/%E2%86%98" class="mw-redirect" title="↘">↘️</a>
</td>
<td title="U+2199: SOUTH WEST ARROW"><a href="/wiki/%E2%86%99" class="mw-redirect" title="↙">↙️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+21Ax
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+21A9: LEFTWARDS ARROW WITH HOOK"><a href="/wiki/%E2%86%A9" class="mw-redirect" title="↩">↩️</a>
</td>
<td title="U+21AA: RIGHTWARDS ARROW WITH HOOK"><a href="/wiki/%E2%86%AA" class="mw-redirect" title="↪">↪️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+231x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+231A: WATCH"><a href="/wiki/%E2%8C%9A" class="mw-redirect" title="⌚">⌚️</a>
</td>
<td title="U+231B: HOURGLASS"><a href="/wiki/%E2%8C%9B" class="mw-redirect" title="⌛">⌛️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+232x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2328: KEYBOARD"><a href="/wiki/%E2%8C%A8" class="mw-redirect" title="⌨">⌨️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+23Cx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+23CF: EJECT SYMBOL"><a href="/wiki/%E2%8F%8F" class="mw-redirect" title="⏏">⏏️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+23Ex
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+23E9: BLACK RIGHT-POINTING DOUBLE TRIANGLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏩️</a>
</td>
<td title="U+23EA: BLACK LEFT-POINTING DOUBLE TRIANGLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏪️</a>
</td>
<td title="U+23EB: BLACK UP-POINTING DOUBLE TRIANGLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏫️</a>
</td>
<td title="U+23EC: BLACK DOWN-POINTING DOUBLE TRIANGLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏬️</a>
</td>
<td title="U+23ED: BLACK RIGHT-POINTING DOUBLE TRIANGLE WITH VERTICAL BAR"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏭️</a>
</td>
<td title="U+23EE: BLACK LEFT-POINTING DOUBLE TRIANGLE WITH VERTICAL BAR"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏮️</a>
</td>
<td title="U+23EF: BLACK RIGHT-POINTING TRIANGLE WITH DOUBLE VERTICAL BAR"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏯️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+23Fx
</td>
<td title="U+23F0: ALARM CLOCK"><a href="/wiki/%E2%8F%B0" class="mw-redirect" title="⏰">⏰️</a>
</td>
<td title="U+23F1: STOPWATCH"><a href="/wiki/%E2%8F%B1" class="mw-redirect" title="⏱">⏱️</a>
</td>
<td title="U+23F2: TIMER CLOCK"><a href="/wiki/%E2%8F%B2" class="mw-redirect" title="⏲">⏲️</a>
</td>
<td title="U+23F3: HOURGLASS WITH FLOWING SAND"><a href="/wiki/%E2%8F%B3" class="mw-redirect" title="⏳">⏳️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+23F8: DOUBLE VERTICAL BAR"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏸️</a>
</td>
<td title="U+23F9: BLACK SQUARE FOR STOP"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏹️</a>
</td>
<td title="U+23FA: BLACK CIRCLE FOR RECORD"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⏺️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+24Cx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+24C2: CIRCLED LATIN CAPITAL LETTER M"><a href="/wiki/%E2%93%82" class="mw-redirect" title="Ⓜ">Ⓜ️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+25Ax
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+25AA: BLACK SMALL SQUARE"><a href="/wiki/%E2%96%AA" class="mw-redirect" title="▪">▪️</a>
</td>
<td title="U+25AB: WHITE SMALL SQUARE"><a href="/wiki/%E2%96%AB" class="mw-redirect" title="▫">▫️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+25Bx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+25B6: BLACK RIGHT-POINTING TRIANGLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ▶️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+25Cx
</td>
<td title="U+25C0: BLACK LEFT-POINTING TRIANGLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ◀️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+25Fx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+25FB: WHITE MEDIUM SQUARE"><a href="/wiki/%E2%97%BB" class="mw-redirect" title="◻">◻️</a>
</td>
<td title="U+25FC: BLACK MEDIUM SQUARE"><a href="/wiki/%E2%97%BC" class="mw-redirect" title="◼">◼️</a>
</td>
<td title="U+25FD: WHITE MEDIUM SMALL SQUARE"><a href="/wiki/%E2%97%BD" class="mw-redirect" title="◽">◽️</a>
</td>
<td title="U+25FE: BLACK MEDIUM SMALL SQUARE"><a href="/wiki/%E2%97%BE" class="mw-redirect" title="◾">◾️</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+260x
</td>
<td title="U+2600: BLACK SUN WITH RAYS"><a href="/wiki/%E2%98%80" class="mw-redirect" title="☀">☀️</a>
</td>
<td title="U+2601: CLOUD"><a href="/wiki/%E2%98%81" class="mw-redirect" title="☁">☁️</a>
</td>
<td title="U+2602: UMBRELLA"><a href="/wiki/%E2%98%82" class="mw-redirect" title="☂">☂️</a>
</td>
<td title="U+2603: SNOWMAN"><a href="/wiki/%E2%98%83" class="mw-redirect" title="☃">☃️</a>
</td>
<td title="U+2604: COMET"><a href="/wiki/%E2%98%84" class="mw-redirect" title="☄">☄️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+260E: BLACK TELEPHONE"><a href="/wiki/%E2%98%8E" class="mw-redirect" title="☎">☎️</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+261x
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2611: BALLOT BOX WITH CHECK"><a href="/wiki/%E2%98%91" class="mw-redirect" title="☑">☑️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2614: UMBRELLA WITH RAIN DROPS"><a href="/wiki/%E2%98%94" class="mw-redirect" title="☔">☔️</a>
</td>
<td title="U+2615: HOT BEVERAGE"><a href="/wiki/%E2%98%95" class="mw-redirect" title="☕">☕️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2618: SHAMROCK"><a href="/wiki/%E2%98%98" class="mw-redirect" title="☘">☘️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+261D: WHITE UP POINTING INDEX"><a href="/wiki/%E2%98%9D" class="mw-redirect" title="☝">☝️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+262x
</td>
<td title="U+2620: SKULL AND CROSSBONES"><a href="/wiki/Skull_and_crossbones_(symbol)" class="mw-redirect" title="Skull and crossbones (symbol)">☠️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2622: RADIOACTIVE SIGN"><a href="/wiki/%E2%98%A2" class="mw-redirect" title="☢">☢️</a>
</td>
<td title="U+2623: BIOHAZARD SIGN"><a href="/wiki/%E2%98%A3" class="mw-redirect" title="☣">☣️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2626: ORTHODOX CROSS"><a href="/wiki/%E2%98%A6" class="mw-redirect" title="☦">☦️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+262A: STAR AND CRESCENT"><a href="/wiki/%E2%98%AA" class="mw-redirect" title="☪">☪️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+262E: PEACE SYMBOL"><a href="/wiki/%E2%98%AE" class="mw-redirect" title="☮">☮️</a>
</td>
<td title="U+262F: YIN YANG"><a href="/wiki/%E2%98%AF" class="mw-redirect" title="☯">☯️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+263x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2638: WHEEL OF DHARMA"><a href="/wiki/%E2%98%B8" class="mw-redirect" title="☸">☸️</a>
</td>
<td title="U+2639: WHITE FROWNING FACE"><a href="/wiki/%E2%98%B9" class="mw-redirect" title="☹">☹️</a>
</td>
<td title="U+263A: WHITE SMILING FACE"><a href="/wiki/%E2%98%BA" class="mw-redirect" title="☺">☺️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+264x
</td>
<td title="U+2640: FEMALE SIGN"><a href="/wiki/%E2%99%80" class="mw-redirect" title="♀">♀️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2642: MALE SIGN"><a href="/wiki/%E2%99%82" class="mw-redirect" title="♂">♂️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2648: ARIES"><a href="/wiki/%E2%99%88" class="mw-redirect" title="♈">♈️</a>
</td>
<td title="U+2649: TAURUS"><a href="/wiki/%E2%99%89" class="mw-redirect" title="♉">♉️</a>
</td>
<td title="U+264A: GEMINI"><a href="/wiki/%E2%99%8A" class="mw-redirect" title="♊">♊️</a>
</td>
<td title="U+264B: CANCER"><a href="/wiki/%E2%99%8B" class="mw-redirect" title="♋">♋️</a>
</td>
<td title="U+264C: LEO"><a href="/wiki/%E2%99%8C" class="mw-redirect" title="♌">♌️</a>
</td>
<td title="U+264D: VIRGO"><a href="/wiki/%E2%99%8D" class="mw-redirect" title="♍">♍️</a>
</td>
<td title="U+264E: LIBRA"><a href="/wiki/%E2%99%8E" class="mw-redirect" title="♎">♎️</a>
</td>
<td title="U+264F: SCORPIUS"><a href="/wiki/%E2%99%8F" class="mw-redirect" title="♏">♏️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+265x
</td>
<td title="U+2650: SAGITTARIUS"><a href="/wiki/%E2%99%90" class="mw-redirect" title="♐">♐️</a>
</td>
<td title="U+2651: CAPRICORN"><a href="/wiki/%E2%99%91" class="mw-redirect" title="♑">♑️</a>
</td>
<td title="U+2652: AQUARIUS"><a href="/wiki/%E2%99%92" class="mw-redirect" title="♒">♒️</a>
</td>
<td title="U+2653: PISCES"><a href="/wiki/%E2%99%93" class="mw-redirect" title="♓">♓️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+265F: BLACK CHESS PAWN"><a href="/wiki/%E2%99%9F" class="mw-redirect" title="♟">♟️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+266x
</td>
<td title="U+2660: BLACK SPADE SUIT"><a href="/wiki/Suit_(cards)" class="mw-redirect" title="Suit (cards)">♠️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2663: BLACK CLUB SUIT"><a href="/wiki/Suit_(cards)" class="mw-redirect" title="Suit (cards)">♣️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2665: BLACK HEART SUIT"><a href="/wiki/Suit_(cards)" class="mw-redirect" title="Suit (cards)">♥️</a>
</td>
<td title="U+2666: BLACK DIAMOND SUIT"><a href="/wiki/Suit_(cards)" class="mw-redirect" title="Suit (cards)">♦️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2668: HOT SPRINGS"><a href="/wiki/%E2%99%A8" class="mw-redirect" title="♨">♨️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+267x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+267B: BLACK UNIVERSAL RECYCLING SYMBOL"><a href="/wiki/%E2%99%BB" class="mw-redirect" title="♻">♻️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+267E: PERMANENT PAPER SIGN"><a href="/wiki/%E2%99%BE" class="mw-redirect" title="♾">♾️</a>
</td>
<td title="U+267F: WHEELCHAIR SYMBOL"><a href="/wiki/%E2%99%BF" class="mw-redirect" title="♿">♿️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+269x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2692: HAMMER AND PICK"><a href="/wiki/%E2%9A%92" class="mw-redirect" title="⚒">⚒️</a>
</td>
<td title="U+2693: ANCHOR"><a href="/wiki/%E2%9A%93" class="mw-redirect" title="⚓">⚓️</a>
</td>
<td title="U+2694: CROSSED SWORDS"><a href="/wiki/%E2%9A%94" class="mw-redirect" title="⚔">⚔️</a>
</td>
<td title="U+2695: STAFF OF AESCULAPIUS"><a href="/wiki/%E2%9A%95" class="mw-redirect" title="⚕">⚕️</a>
</td>
<td title="U+2696: SCALES"><a href="/wiki/%E2%9A%96" class="mw-redirect" title="⚖">⚖️</a>
</td>
<td title="U+2697: ALEMBIC"><a href="/wiki/%E2%9A%97" class="mw-redirect" title="⚗">⚗️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2699: GEAR"><a href="/wiki/%E2%9A%99" class="mw-redirect" title="⚙">⚙️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+269B: ATOM SYMBOL"><a href="/wiki/%E2%9A%9B" class="mw-redirect" title="⚛">⚛️</a>
</td>
<td title="U+269C: FLEUR-DE-LIS"><a href="/wiki/%E2%9A%9C" class="mw-redirect" title="⚜">⚜️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+26Ax
</td>
<td title="U+26A0: WARNING SIGN"><a href="/wiki/%E2%9A%A0" class="mw-redirect" title="⚠">⚠️</a>
</td>
<td title="U+26A1: HIGH VOLTAGE SIGN"><a href="/wiki/%E2%9A%A1" class="mw-redirect" title="⚡">⚡️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26A7: MALE WITH STROKE AND MALE AND FEMALE SIGN"><a href="/wiki/%E2%9A%A7" class="mw-redirect" title="⚧">⚧️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26AA: MEDIUM WHITE CIRCLE"><a href="/wiki/%E2%9A%AA" class="mw-redirect" title="⚪">⚪️</a>
</td>
<td title="U+26AB: MEDIUM BLACK CIRCLE"><a href="/wiki/Media_controls" class="mw-redirect" title="Media controls"> ⚫️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+26Bx
</td>
<td title="U+26B0: COFFIN"><a href="/wiki/%E2%9A%B0" class="mw-redirect" title="⚰">⚰️</a>
</td>
<td title="U+26B1: FUNERAL URN"><a href="/wiki/%E2%9A%B1" class="mw-redirect" title="⚱">⚱️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26BD: SOCCER BALL"><a href="/wiki/%E2%9A%BD" class="mw-redirect" title="⚽">⚽️</a>
</td>
<td title="U+26BE: BASEBALL"><a href="/wiki/%E2%9A%BE" class="mw-redirect" title="⚾">⚾️</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+26Cx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26C4: SNOWMAN WITHOUT SNOW"><a href="/wiki/%E2%9B%84" class="mw-redirect" title="⛄">⛄️</a>
</td>
<td title="U+26C5: SUN BEHIND CLOUD"><a href="/wiki/%E2%9B%85" class="mw-redirect" title="⛅">⛅️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26C8: THUNDER CLOUD AND RAIN"><a href="/wiki/%E2%9B%88" class="mw-redirect" title="⛈">⛈️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26CE: OPHIUCHUS"><a href="/wiki/%E2%9B%8E" class="mw-redirect" title="⛎">⛎️</a>
</td>
<td title="U+26CF: PICK"><a href="/wiki/%E2%9B%8F" class="mw-redirect" title="⛏">⛏️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+26Dx
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26D1: HELMET WITH WHITE CROSS"><a href="/wiki/%E2%9B%91" class="mw-redirect" title="⛑">⛑️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26D3: CHAINS"><a href="/wiki/%E2%9B%93" class="mw-redirect" title="⛓">⛓️</a>
</td>
<td title="U+26D4: NO ENTRY"><a href="/wiki/%E2%9B%94" class="mw-redirect" title="⛔">⛔️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td colspan="17">
</td></tr>
<tr style="background:#F8F8F8;font-size:small;font-family:sans-serif">
<td style="width:45pt">&nbsp;</td>
<td style="width:20pt">0</td>
<td style="width:20pt">1</td>
<td style="width:20pt">2</td>
<td style="width:20pt">3</td>
<td style="width:20pt">4</td>
<td style="width:20pt">5</td>
<td style="width:20pt">6</td>
<td style="width:20pt">7</td>
<td style="width:20pt">8</td>
<td style="width:20pt">9</td>
<td style="width:20pt">A</td>
<td style="width:20pt">B</td>
<td style="width:20pt">C</td>
<td style="width:20pt">D</td>
<td style="width:20pt">E</td>
<td style="width:20pt">F
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+26Ex
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26E9: SHINTO SHRINE"><a href="/wiki/%E2%9B%A9" class="mw-redirect" title="⛩">⛩️</a>
</td>
<td title="U+26EA: CHURCH"><a href="/wiki/%E2%9B%AA" class="mw-redirect" title="⛪">⛪️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+26Fx
</td>
<td title="U+26F0: MOUNTAIN"><a href="/wiki/%E2%9B%B0" class="mw-redirect" title="⛰">⛰️</a>
</td>
<td title="U+26F1: UMBRELLA ON GROUND"><a href="/wiki/%E2%9B%B1" class="mw-redirect" title="⛱">⛱️</a>
</td>
<td title="U+26F2: FOUNTAIN"><a href="/wiki/%E2%9B%B2" class="mw-redirect" title="⛲">⛲️</a>
</td>
<td title="U+26F3: FLAG IN HOLE"><a href="/wiki/%E2%9B%B3" class="mw-redirect" title="⛳">⛳️</a>
</td>
<td title="U+26F4: FERRY"><a href="/wiki/%E2%9B%B4" class="mw-redirect" title="⛴">⛴️</a>
</td>
<td title="U+26F5: SAILBOAT"><a href="/wiki/%E2%9B%B5" class="mw-redirect" title="⛵">⛵️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26F7: SKIER"><a href="/wiki/%E2%9B%B7" class="mw-redirect" title="⛷">⛷️</a>
</td>
<td title="U+26F8: ICE SKATE"><a href="/wiki/%E2%9B%B8" class="mw-redirect" title="⛸">⛸️</a>
</td>
<td title="U+26F9: PERSON WITH BALL"><a href="/wiki/%E2%9B%B9" class="mw-redirect" title="⛹">⛹️</a>
</td>
<td title="U+26FA: TENT"><a href="/wiki/%E2%9B%BA" class="mw-redirect" title="⛺">⛺️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+26FD: FUEL PUMP"><a href="/wiki/%E2%9B%BD" class="mw-redirect" title="⛽">⛽️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+270x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2702: BLACK SCISSORS"><a href="/wiki/%E2%9C%82" class="mw-redirect" title="✂">✂️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2705: WHITE HEAVY CHECK MARK"><a href="/wiki/%E2%9C%85" class="mw-redirect" title="✅">✅️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2708: AIRPLANE"><a href="/wiki/%E2%9C%88" class="mw-redirect" title="✈">✈️</a>
</td>
<td title="U+2709: ENVELOPE"><a href="/wiki/%E2%9C%89" class="mw-redirect" title="✉">✉️</a>
</td>
<td title="U+270A: RAISED FIST"><a href="/wiki/%E2%9C%8A" class="mw-redirect" title="✊">✊️</a>
</td>
<td title="U+270B: RAISED HAND"><a href="/wiki/%E2%9C%8B" class="mw-redirect" title="✋">✋️</a>
</td>
<td title="U+270C: VICTORY HAND"><a href="/wiki/%E2%9C%8C" class="mw-redirect" title="✌">✌️</a>
</td>
<td title="U+270D: WRITING HAND"><a href="/wiki/%E2%9C%8D" class="mw-redirect" title="✍">✍️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+270F: PENCIL"><a href="/wiki/%E2%9C%8F" class="mw-redirect" title="✏">✏️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+271x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2712: BLACK NIB"><a href="/wiki/%E2%9C%92" class="mw-redirect" title="✒">✒️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2714: HEAVY CHECK MARK"><a href="/wiki/%E2%9C%94" class="mw-redirect" title="✔">✔️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2716: HEAVY MULTIPLICATION X"><a href="/wiki/X_mark" title="X mark">✖️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+271D: LATIN CROSS"><a href="/wiki/%E2%9C%9D" class="mw-redirect" title="✝">✝️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+272x
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2721: STAR OF DAVID"><a href="/wiki/%E2%9C%A1" class="mw-redirect" title="✡">✡️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2728: SPARKLES"><a href="/wiki/%E2%9C%A8" class="mw-redirect" title="✨">✨️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+273x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2733: EIGHT SPOKED ASTERISK"><a href="/wiki/%E2%9C%B3" class="mw-redirect" title="✳">✳️</a>
</td>
<td title="U+2734: EIGHT POINTED BLACK STAR"><a href="/wiki/%E2%9C%B4" class="mw-redirect" title="✴">✴️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+274x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2744: SNOWFLAKE"><a href="/wiki/%E2%9D%84" class="mw-redirect" title="❄">❄️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2747: SPARKLE"><a href="/wiki/%E2%9D%87" class="mw-redirect" title="❇">❇️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+274C: CROSS MARK"><a href="/wiki/%E2%9D%8C" class="mw-redirect" title="❌">❌️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+274E: NEGATIVE SQUARED CROSS MARK"><a href="/wiki/%E2%9D%8E" class="mw-redirect" title="❎">❎️</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+275x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2753: BLACK QUESTION MARK ORNAMENT"><a href="/wiki/%E2%9D%93" class="mw-redirect" title="❓">❓️</a>
</td>
<td title="U+2754: WHITE QUESTION MARK ORNAMENT"><a href="/wiki/%E2%9D%94" class="mw-redirect" title="❔">❔️</a>
</td>
<td title="U+2755: WHITE EXCLAMATION MARK ORNAMENT"><a href="/wiki/%E2%9D%95" class="mw-redirect" title="❕">❕️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2757: HEAVY EXCLAMATION MARK SYMBOL"><a href="/wiki/%E2%9D%97" class="mw-redirect" title="❗">❗️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+276x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2763: HEAVY HEART EXCLAMATION MARK ORNAMENT"><a href="/wiki/%E2%9D%A3" class="mw-redirect" title="❣">❣️</a>
</td>
<td title="U+2764: HEAVY BLACK HEART"><a href="/wiki/%E2%9D%A4" class="mw-redirect" title="❤">❤️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+279x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2795: HEAVY PLUS SIGN"><a href="/wiki/%E2%9E%95" class="mw-redirect" title="➕">➕️</a>
</td>
<td title="U+2796: HEAVY MINUS SIGN"><a href="/wiki/%E2%9E%96" class="mw-redirect" title="➖">➖️</a>
</td>
<td title="U+2797: HEAVY DIVISION SIGN"><a href="/wiki/%E2%9E%97" class="mw-redirect" title="➗">➗️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+27Ax
</td>
<td style="background-color:#CCC">
</td>
<td title="U+27A1: BLACK RIGHTWARDS ARROW"><a href="/wiki/%E2%9E%A1" class="mw-redirect" title="➡">➡️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+27Bx
</td>
<td title="U+27B0: CURLY LOOP"><a href="/wiki/Loop_the_loop_(disambiguation)" class="mw-redirect mw-disambig" title="Loop the loop (disambiguation)">➰️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+27BF: DOUBLE CURLY LOOP"><a href="/wiki/Loop_the_loop_(disambiguation)" class="mw-redirect mw-disambig" title="Loop the loop (disambiguation)">➿️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+293x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2934: ARROW POINTING RIGHTWARDS THEN CURVING UPWARDS"><a href="/wiki/%E2%A4%B4" class="mw-redirect" title="⤴">⤴️</a>
</td>
<td title="U+2935: ARROW POINTING RIGHTWARDS THEN CURVING DOWNWARDS"><a href="/wiki/%E2%A4%B5" class="mw-redirect" title="⤵">⤵️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+2B0x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2B05: LEFTWARDS BLACK ARROW"><a href="/wiki/%E2%AC%85" class="mw-redirect" title="⬅">⬅️</a>
</td>
<td title="U+2B06: UPWARDS BLACK ARROW"><a href="/wiki/%E2%AC%86" class="mw-redirect" title="⬆">⬆️</a>
</td>
<td title="U+2B07: DOWNWARDS BLACK ARROW"><a href="/wiki/%E2%86%93_(disambiguation)" class="mw-redirect mw-disambig" title="↓ (disambiguation)"> ⬇️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+2B1x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2B1B: BLACK LARGE SQUARE"><a href="/wiki/%E2%AC%9B" class="mw-redirect" title="⬛">⬛️</a>
</td>
<td title="U+2B1C: WHITE LARGE SQUARE"><a href="/wiki/%E2%AC%9C" class="mw-redirect" title="⬜">⬜️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+2B5x
</td>
<td title="U+2B50: WHITE MEDIUM STAR"><a href="/wiki/%E2%AD%90" class="mw-redirect" title="⭐">⭐️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+2B55: HEAVY LARGE CIRCLE"><a href="/wiki/Circle_symbol_(disambiguation)" class="mw-redirect mw-disambig" title="Circle symbol (disambiguation)">⭕️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+303x
</td>
<td title="U+3030: WAVY DASH"><a href="/wiki/%E3%80%B0" class="mw-redirect" title="〰">〰️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+303D: PART ALTERNATION MARK"><a href="/wiki/%E3%80%BD" class="mw-redirect" title="〽">〽️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+329x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+3297: CIRCLED IDEOGRAPH CONGRATULATION"><a href="https://en.wiktionary.org/wiki/%E7%A5%9D%E3%81%84" class="extiw" title="wikt:祝い">㊗️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+3299: CIRCLED IDEOGRAPH SECRET"><a href="https://en.wiktionary.org/wiki/%E7%A7%98" class="extiw" title="wikt:秘">㊙️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F00x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F004: MAHJONG TILE RED DRAGON"><a href="/wiki/%F0%9F%80%84" class="mw-redirect" title="🀄">🀄</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F0Cx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F0CF: PLAYING CARD BLACK JOKER"><a href="/wiki/%F0%9F%83%8F" class="mw-redirect" title="🃏">🃏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F17x
</td>
<td title="U+1F170: NEGATIVE SQUARED LATIN CAPITAL LETTER A"><a href="/wiki/%F0%9F%85%B0" class="mw-redirect" title="🅰">🅰️</a>
</td>
<td title="U+1F171: NEGATIVE SQUARED LATIN CAPITAL LETTER B"><a href="/wiki/%F0%9F%85%B1" class="mw-redirect" title="🅱">🅱️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F17E: NEGATIVE SQUARED LATIN CAPITAL LETTER O"><a href="/wiki/%F0%9F%85%BE" class="mw-redirect" title="🅾">🅾️</a>
</td>
<td title="U+1F17F: NEGATIVE SQUARED LATIN CAPITAL LETTER P"><a href="/wiki/%F0%9F%85%BF" class="mw-redirect" title="🅿">🅿️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F18x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F18E: NEGATIVE SQUARED AB"><a href="/wiki/%F0%9F%86%8E" class="mw-redirect" title="🆎">🆎</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F19x
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F191: SQUARED CL"><a href="/wiki/CL_(disambiguation)" class="mw-redirect mw-disambig" title="CL (disambiguation)">🆑</a>
</td>
<td title="U+1F192: SQUARED COOL"><a href="/wiki/%F0%9F%86%92" class="mw-redirect" title="🆒">🆒</a>
</td>
<td title="U+1F193: SQUARED FREE"><a href="/wiki/%F0%9F%86%93" class="mw-redirect" title="🆓">🆓</a>
</td>
<td title="U+1F194: SQUARED ID"><a href="/wiki/%F0%9F%86%94" class="mw-redirect" title="🆔">🆔</a>
</td>
<td title="U+1F195: SQUARED NEW"><a href="/wiki/New_(disambiguation)" class="mw-redirect mw-disambig" title="New (disambiguation)">🆕</a>
</td>
<td title="U+1F196: SQUARED NG"><a href="/wiki/No_Good_(disambiguation)" class="mw-redirect mw-disambig" title="No Good (disambiguation)">🆖</a>
</td>
<td title="U+1F197: SQUARED OK"><a href="/wiki/%F0%9F%86%97" class="mw-redirect" title="🆗">🆗</a>
</td>
<td title="U+1F198: SQUARED SOS"><a href="/wiki/%F0%9F%86%98" class="mw-redirect" title="🆘">🆘</a>
</td>
<td title="U+1F199: SQUARED UP WITH EXCLAMATION MARK"><a href="/wiki/Up_(disambiguation)" class="mw-redirect mw-disambig" title="Up (disambiguation)">🆙</a>
</td>
<td title="U+1F19A: SQUARED VS"><a href="/wiki/Versus_(disambiguation)" class="mw-redirect mw-disambig" title="Versus (disambiguation)">🆚</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F20x
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F201: SQUARED KATAKANA KOKO"><a href="https://en.wiktionary.org/wiki/%F0%9F%88%81" class="extiw" title="wikt:🈁">🈁</a>
</td>
<td title="U+1F202: SQUARED KATAKANA SA"><a href="/wiki/%F0%9F%88%82" class="mw-redirect" title="🈂">🈂️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F21x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F21A: SQUARED CJK UNIFIED IDEOGRAPH-7121"><a href="/wiki/%F0%9F%88%9A" class="mw-redirect" title="🈚">🈚</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F22x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F22F: SQUARED CJK UNIFIED IDEOGRAPH-6307"><a href="/w/index.php?title=%F0%9F%88%AF&amp;action=edit&amp;redlink=1" class="new" title="🈯 (page does not exist)">🈯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F23x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F232: SQUARED CJK UNIFIED IDEOGRAPH-7981"><a href="https://en.wiktionary.org/wiki/%E7%A6%81" class="extiw" title="wikt:禁">🈲</a>
</td>
<td title="U+1F233: SQUARED CJK UNIFIED IDEOGRAPH-7A7A"><a href="https://en.wiktionary.org/wiki/%E7%A9%BA" class="extiw" title="wikt:空">🈳</a>
</td>
<td title="U+1F234: SQUARED CJK UNIFIED IDEOGRAPH-5408"><a href="https://en.wiktionary.org/wiki/%E5%90%88" class="extiw" title="wikt:合">🈴</a>
</td>
<td title="U+1F235: SQUARED CJK UNIFIED IDEOGRAPH-6E80"><a href="https://en.wiktionary.org/wiki/%E6%BA%80" class="extiw" title="wikt:満">🈵</a>
</td>
<td title="U+1F236: SQUARED CJK UNIFIED IDEOGRAPH-6709"><a href="https://en.wiktionary.org/wiki/%E6%9C%89" class="extiw" title="wikt:有">🈶</a>
</td>
<td title="U+1F237: SQUARED CJK UNIFIED IDEOGRAPH-6708"><a href="https://en.wiktionary.org/wiki/%E6%9C%88" class="extiw" title="wikt:月">🈷️</a>
</td>
<td title="U+1F238: SQUARED CJK UNIFIED IDEOGRAPH-7533"><a href="https://en.wiktionary.org/wiki/%E7%94%B3" class="extiw" title="wikt:申">🈸</a>
</td>
<td title="U+1F239: SQUARED CJK UNIFIED IDEOGRAPH-5272"><a href="https://en.wiktionary.org/wiki/%E5%89%B2" class="extiw" title="wikt:割">🈹</a>
</td>
<td title="U+1F23A: SQUARED CJK UNIFIED IDEOGRAPH-55B6"><a href="https://en.wiktionary.org/wiki/%E5%96%B6" class="extiw" title="wikt:営">🈺</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F25x
</td>
<td title="U+1F250: CIRCLED IDEOGRAPH ADVANTAGE"><a href="https://en.wiktionary.org/wiki/%E5%BE%97" class="extiw" title="wikt:得">🉐</a>
</td>
<td title="U+1F251: CIRCLED IDEOGRAPH ACCEPT"><a href="https://en.wiktionary.org/wiki/%E5%8F%AF" class="extiw" title="wikt:可">🉑</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F30x
</td>
<td title="U+1F300: CYCLONE"><a href="/wiki/%F0%9F%8C%80" class="mw-redirect" title="🌀">🌀</a>
</td>
<td title="U+1F301: FOGGY"><a href="/wiki/%F0%9F%8C%81" class="mw-redirect" title="🌁">🌁</a>
</td>
<td title="U+1F302: CLOSED UMBRELLA"><a href="/wiki/%F0%9F%8C%82" class="mw-redirect" title="🌂">🌂</a>
</td>
<td title="U+1F303: NIGHT WITH STARS"><a href="/wiki/%F0%9F%8C%83" class="mw-redirect" title="🌃">🌃</a>
</td>
<td title="U+1F304: SUNRISE OVER MOUNTAINS"><a href="/wiki/%F0%9F%8C%84" class="mw-redirect" title="🌄">🌄</a>
</td>
<td title="U+1F305: SUNRISE"><a href="/wiki/%F0%9F%8C%85" class="mw-redirect" title="🌅">🌅</a>
</td>
<td title="U+1F306: CITYSCAPE AT DUSK"><a href="/wiki/%F0%9F%8C%86" class="mw-redirect" title="🌆">🌆</a>
</td>
<td title="U+1F307: SUNSET OVER BUILDINGS"><a href="/wiki/%F0%9F%8C%87" class="mw-redirect" title="🌇">🌇</a>
</td>
<td title="U+1F308: RAINBOW"><a href="/wiki/%F0%9F%8C%88" class="mw-redirect" title="🌈">🌈</a>
</td>
<td title="U+1F309: BRIDGE AT NIGHT"><a href="/wiki/%F0%9F%8C%89" class="mw-redirect" title="🌉">🌉</a>
</td>
<td title="U+1F30A: WATER WAVE"><a href="/wiki/%F0%9F%8C%8A" class="mw-redirect" title="🌊">🌊</a>
</td>
<td title="U+1F30B: VOLCANO"><a href="/wiki/%F0%9F%8C%8B" class="mw-redirect" title="🌋">🌋</a>
</td>
<td title="U+1F30C: MILKY WAY"><a href="/wiki/%F0%9F%8C%8C" class="mw-redirect" title="🌌">🌌</a>
</td>
<td title="U+1F30D: EARTH GLOBE EUROPE-AFRICA"><a href="/wiki/%F0%9F%8C%8D" class="mw-redirect" title="🌍">🌍</a>
</td>
<td title="U+1F30E: EARTH GLOBE AMERICAS"><a href="/wiki/%F0%9F%8C%8E" class="mw-redirect" title="🌎">🌎</a>
</td>
<td title="U+1F30F: EARTH GLOBE ASIA-AUSTRALIA"><a href="/wiki/%F0%9F%8C%8F" class="mw-redirect" title="🌏">🌏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F31x
</td>
<td title="U+1F310: GLOBE WITH MERIDIANS"><a href="/wiki/%F0%9F%8C%90" class="mw-redirect" title="🌐">🌐</a>
</td>
<td title="U+1F311: NEW MOON SYMBOL"><a href="/wiki/%F0%9F%8C%91" class="mw-redirect" title="🌑">🌑</a>
</td>
<td title="U+1F312: WAXING CRESCENT MOON SYMBOL"><a href="/wiki/%F0%9F%8C%92" class="mw-redirect" title="🌒">🌒</a>
</td>
<td title="U+1F313: FIRST QUARTER MOON SYMBOL"><a href="/wiki/%F0%9F%8C%93" class="mw-redirect" title="🌓">🌓</a>
</td>
<td title="U+1F314: WAXING GIBBOUS MOON SYMBOL"><a href="/wiki/%F0%9F%8C%94" class="mw-redirect" title="🌔">🌔</a>
</td>
<td title="U+1F315: FULL MOON SYMBOL"><a href="/wiki/%F0%9F%8C%95" class="mw-redirect" title="🌕">🌕</a>
</td>
<td title="U+1F316: WANING GIBBOUS MOON SYMBOL"><a href="/wiki/%F0%9F%8C%96" class="mw-redirect" title="🌖">🌖</a>
</td>
<td title="U+1F317: LAST QUARTER MOON SYMBOL"><a href="/wiki/%F0%9F%8C%97" class="mw-redirect" title="🌗">🌗</a>
</td>
<td title="U+1F318: WANING CRESCENT MOON SYMBOL"><a href="/wiki/%F0%9F%8C%98" class="mw-redirect" title="🌘">🌘</a>
</td>
<td title="U+1F319: CRESCENT MOON"><a href="/wiki/%F0%9F%8C%99" class="mw-redirect" title="🌙">🌙</a>
</td>
<td title="U+1F31A: NEW MOON WITH FACE"><a href="/wiki/%F0%9F%8C%9A" class="mw-redirect" title="🌚">🌚</a>
</td>
<td title="U+1F31B: FIRST QUARTER MOON WITH FACE"><a href="/wiki/%F0%9F%8C%9B" class="mw-redirect" title="🌛">🌛</a>
</td>
<td title="U+1F31C: LAST QUARTER MOON WITH FACE"><a href="/wiki/%F0%9F%8C%9C" class="mw-redirect" title="🌜">🌜</a>
</td>
<td title="U+1F31D: FULL MOON WITH FACE"><a href="/wiki/%F0%9F%8C%9D" class="mw-redirect" title="🌝">🌝</a>
</td>
<td title="U+1F31E: SUN WITH FACE"><a href="/wiki/%F0%9F%8C%9E" class="mw-redirect" title="🌞">🌞</a>
</td>
<td title="U+1F31F: GLOWING STAR"><a href="/wiki/%F0%9F%8C%9F" class="mw-redirect" title="🌟">🌟</a>
</td></tr>
<tr>
<td colspan="17">
</td></tr>
<tr style="background:#F8F8F8;font-size:small;font-family:sans-serif">
<td style="width:45pt">&nbsp;</td>
<td style="width:20pt">0</td>
<td style="width:20pt">1</td>
<td style="width:20pt">2</td>
<td style="width:20pt">3</td>
<td style="width:20pt">4</td>
<td style="width:20pt">5</td>
<td style="width:20pt">6</td>
<td style="width:20pt">7</td>
<td style="width:20pt">8</td>
<td style="width:20pt">9</td>
<td style="width:20pt">A</td>
<td style="width:20pt">B</td>
<td style="width:20pt">C</td>
<td style="width:20pt">D</td>
<td style="width:20pt">E</td>
<td style="width:20pt">F
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F32x
</td>
<td title="U+1F320: SHOOTING STAR"><a href="/wiki/%F0%9F%8C%A0" class="mw-redirect" title="🌠">🌠</a>
</td>
<td title="U+1F321: THERMOMETER"><a href="/wiki/%F0%9F%8C%A1" class="mw-redirect" title="🌡">🌡️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F324: WHITE SUN WITH SMALL CLOUD"><a href="/wiki/%F0%9F%8C%A4" class="mw-redirect" title="🌤">🌤️</a>
</td>
<td title="U+1F325: WHITE SUN BEHIND CLOUD"><a href="/wiki/%F0%9F%8C%A5" class="mw-redirect" title="🌥">🌥️</a>
</td>
<td title="U+1F326: WHITE SUN BEHIND CLOUD WITH RAIN"><a href="/wiki/%F0%9F%8C%A6" class="mw-redirect" title="🌦">🌦️</a>
</td>
<td title="U+1F327: CLOUD WITH RAIN"><a href="/wiki/%F0%9F%8C%A7" class="mw-redirect" title="🌧">🌧️</a>
</td>
<td title="U+1F328: CLOUD WITH SNOW"><a href="/wiki/%F0%9F%8C%A8" class="mw-redirect" title="🌨">🌨️</a>
</td>
<td title="U+1F329: CLOUD WITH LIGHTNING"><a href="/wiki/%F0%9F%8C%A9" class="mw-redirect" title="🌩">🌩️</a>
</td>
<td title="U+1F32A: CLOUD WITH TORNADO"><a href="/wiki/%F0%9F%8C%AA" class="mw-redirect" title="🌪">🌪️</a>
</td>
<td title="U+1F32B: FOG"><a href="/wiki/%F0%9F%8C%AB" class="mw-redirect" title="🌫">🌫️</a>
</td>
<td title="U+1F32C: WIND BLOWING FACE"><a href="/wiki/%F0%9F%8C%AC" class="mw-redirect" title="🌬">🌬️</a>
</td>
<td title="U+1F32D: HOT DOG"><a href="/wiki/%F0%9F%8C%AD" class="mw-redirect" title="🌭">🌭</a>
</td>
<td title="U+1F32E: TACO"><a href="/wiki/%F0%9F%8C%AE" class="mw-redirect" title="🌮">🌮</a>
</td>
<td title="U+1F32F: BURRITO"><a href="/wiki/%F0%9F%8C%AF" class="mw-redirect" title="🌯">🌯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F33x
</td>
<td title="U+1F330: CHESTNUT"><a href="/wiki/%F0%9F%8C%B0" class="mw-redirect" title="🌰">🌰</a>
</td>
<td title="U+1F331: SEEDLING"><a href="/wiki/%F0%9F%8C%B1" class="mw-redirect" title="🌱">🌱</a>
</td>
<td title="U+1F332: EVERGREEN TREE"><a href="/wiki/%F0%9F%8C%B2" class="mw-redirect" title="🌲">🌲</a>
</td>
<td title="U+1F333: DECIDUOUS TREE"><a href="/wiki/%F0%9F%8C%B3" class="mw-redirect" title="🌳">🌳</a>
</td>
<td title="U+1F334: PALM TREE"><a href="/wiki/%F0%9F%8C%B4" class="mw-redirect" title="🌴">🌴</a>
</td>
<td title="U+1F335: CACTUS"><a href="/wiki/%F0%9F%8C%B5" class="mw-redirect" title="🌵">🌵</a>
</td>
<td title="U+1F336: HOT PEPPER"><a href="/wiki/%F0%9F%8C%B6" class="mw-redirect" title="🌶">🌶️</a>
</td>
<td title="U+1F337: TULIP"><a href="/wiki/%F0%9F%8C%B7" class="mw-redirect" title="🌷">🌷</a>
</td>
<td title="U+1F338: CHERRY BLOSSOM"><a href="/wiki/%F0%9F%8C%B8" class="mw-redirect" title="🌸">🌸</a>
</td>
<td title="U+1F339: ROSE"><a href="/wiki/%F0%9F%8C%B9" class="mw-redirect" title="🌹">🌹</a>
</td>
<td title="U+1F33A: HIBISCUS"><a href="/wiki/%F0%9F%8C%BA" class="mw-redirect" title="🌺">🌺</a>
</td>
<td title="U+1F33B: SUNFLOWER"><a href="/wiki/%F0%9F%8C%BB" class="mw-redirect" title="🌻">🌻</a>
</td>
<td title="U+1F33C: BLOSSOM"><a href="/wiki/%F0%9F%8C%BC" class="mw-redirect" title="🌼">🌼</a>
</td>
<td title="U+1F33D: EAR OF MAIZE"><a href="/wiki/%F0%9F%8C%BD" class="mw-redirect" title="🌽">🌽</a>
</td>
<td title="U+1F33E: EAR OF RICE"><a href="/wiki/%F0%9F%8C%BE" class="mw-redirect" title="🌾">🌾</a>
</td>
<td title="U+1F33F: HERB"><a href="/wiki/%F0%9F%8C%BF" class="mw-redirect" title="🌿">🌿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F34x
</td>
<td title="U+1F340: FOUR LEAF CLOVER"><a href="/wiki/%F0%9F%8D%80" class="mw-redirect" title="🍀">🍀</a>
</td>
<td title="U+1F341: MAPLE LEAF"><a href="/wiki/%F0%9F%8D%81" class="mw-redirect" title="🍁">🍁</a>
</td>
<td title="U+1F342: FALLEN LEAF"><a href="/wiki/%F0%9F%8D%82" class="mw-redirect" title="🍂">🍂</a>
</td>
<td title="U+1F343: LEAF FLUTTERING IN WIND"><a href="/wiki/%F0%9F%8D%83" class="mw-redirect" title="🍃">🍃</a>
</td>
<td title="U+1F344: MUSHROOM"><a href="/wiki/%F0%9F%8D%84" class="mw-redirect" title="🍄">🍄</a>
</td>
<td title="U+1F345: TOMATO"><a href="/wiki/%F0%9F%8D%85" class="mw-redirect" title="🍅">🍅</a>
</td>
<td title="U+1F346: AUBERGINE"><a href="/wiki/%F0%9F%8D%86" class="mw-redirect" title="🍆">🍆</a>
</td>
<td title="U+1F347: GRAPES"><a href="/wiki/%F0%9F%8D%87" class="mw-redirect" title="🍇">🍇</a>
</td>
<td title="U+1F348: MELON"><a href="/wiki/%F0%9F%8D%88" class="mw-redirect" title="🍈">🍈</a>
</td>
<td title="U+1F349: WATERMELON"><a href="/wiki/%F0%9F%8D%89" class="mw-redirect" title="🍉">🍉</a>
</td>
<td title="U+1F34A: TANGERINE"><a href="/wiki/%F0%9F%8D%8A" class="mw-redirect" title="🍊">🍊</a>
</td>
<td title="U+1F34B: LEMON"><a href="/wiki/%F0%9F%8D%8B" class="mw-redirect" title="🍋">🍋</a>
</td>
<td title="U+1F34C: BANANA"><a href="/wiki/%F0%9F%8D%8C" class="mw-redirect" title="🍌">🍌</a>
</td>
<td title="U+1F34D: PINEAPPLE"><a href="/wiki/%F0%9F%8D%8D" class="mw-redirect" title="🍍">🍍</a>
</td>
<td title="U+1F34E: RED APPLE"><a href="/wiki/%F0%9F%8D%8E" class="mw-redirect" title="🍎">🍎</a>
</td>
<td title="U+1F34F: GREEN APPLE"><a href="/wiki/%F0%9F%8D%8F" class="mw-redirect" title="🍏">🍏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F35x
</td>
<td title="U+1F350: PEAR"><a href="/wiki/%F0%9F%8D%90" class="mw-redirect" title="🍐">🍐</a>
</td>
<td title="U+1F351: PEACH"><a href="/wiki/%F0%9F%8D%91" class="mw-redirect" title="🍑">🍑</a>
</td>
<td title="U+1F352: CHERRIES"><a href="/wiki/%F0%9F%8D%92" class="mw-redirect" title="🍒">🍒</a>
</td>
<td title="U+1F353: STRAWBERRY"><a href="/wiki/%F0%9F%8D%93" class="mw-redirect" title="🍓">🍓</a>
</td>
<td title="U+1F354: HAMBURGER"><a href="/wiki/%F0%9F%8D%94" class="mw-redirect" title="🍔">🍔</a>
</td>
<td title="U+1F355: SLICE OF PIZZA"><a href="/wiki/%F0%9F%8D%95" class="mw-redirect" title="🍕">🍕</a>
</td>
<td title="U+1F356: MEAT ON BONE"><a href="/wiki/%F0%9F%8D%96" class="mw-redirect" title="🍖">🍖</a>
</td>
<td title="U+1F357: POULTRY LEG"><a href="/wiki/%F0%9F%8D%97" class="mw-redirect" title="🍗">🍗</a>
</td>
<td title="U+1F358: RICE CRACKER"><a href="/wiki/%F0%9F%8D%98" class="mw-redirect" title="🍘">🍘</a>
</td>
<td title="U+1F359: RICE BALL"><a href="/wiki/%F0%9F%8D%99" class="mw-redirect" title="🍙">🍙</a>
</td>
<td title="U+1F35A: COOKED RICE"><a href="/wiki/%F0%9F%8D%9A" class="mw-redirect" title="🍚">🍚</a>
</td>
<td title="U+1F35B: CURRY AND RICE"><a href="/wiki/%F0%9F%8D%9B" class="mw-redirect" title="🍛">🍛</a>
</td>
<td title="U+1F35C: STEAMING BOWL"><a href="/wiki/%F0%9F%8D%9C" class="mw-redirect" title="🍜">🍜</a>
</td>
<td title="U+1F35D: SPAGHETTI"><a href="/wiki/%F0%9F%8D%9D" class="mw-redirect" title="🍝">🍝</a>
</td>
<td title="U+1F35E: BREAD"><a href="/wiki/%F0%9F%8D%9E" class="mw-redirect" title="🍞">🍞</a>
</td>
<td title="U+1F35F: FRENCH FRIES"><a href="/wiki/%F0%9F%8D%9F" class="mw-redirect" title="🍟">🍟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F36x
</td>
<td title="U+1F360: ROASTED SWEET POTATO"><a href="/wiki/%F0%9F%8D%A0" class="mw-redirect" title="🍠">🍠</a>
</td>
<td title="U+1F361: DANGO"><a href="/wiki/%F0%9F%8D%A1" class="mw-redirect" title="🍡">🍡</a>
</td>
<td title="U+1F362: ODEN"><a href="/wiki/%F0%9F%8D%A2" class="mw-redirect" title="🍢">🍢</a>
</td>
<td title="U+1F363: SUSHI"><a href="/wiki/%F0%9F%8D%A3" class="mw-redirect" title="🍣">🍣</a>
</td>
<td title="U+1F364: FRIED SHRIMP"><a href="/wiki/%F0%9F%8D%A4" class="mw-redirect" title="🍤">🍤</a>
</td>
<td title="U+1F365: FISH CAKE WITH SWIRL DESIGN"><a href="/wiki/%F0%9F%8D%A5" class="mw-redirect" title="🍥">🍥</a>
</td>
<td title="U+1F366: SOFT ICE CREAM"><a href="/wiki/%F0%9F%8D%A6" class="mw-redirect" title="🍦">🍦</a>
</td>
<td title="U+1F367: SHAVED ICE"><a href="/wiki/%F0%9F%8D%A7" class="mw-redirect" title="🍧">🍧</a>
</td>
<td title="U+1F368: ICE CREAM"><a href="/wiki/%F0%9F%8D%A8" class="mw-redirect" title="🍨">🍨</a>
</td>
<td title="U+1F369: DOUGHNUT"><a href="/wiki/%F0%9F%8D%A9" class="mw-redirect" title="🍩">🍩</a>
</td>
<td title="U+1F36A: COOKIE"><a href="/wiki/%F0%9F%8D%AA" class="mw-redirect" title="🍪">🍪</a>
</td>
<td title="U+1F36B: CHOCOLATE BAR"><a href="/wiki/%F0%9F%8D%AB" class="mw-redirect" title="🍫">🍫</a>
</td>
<td title="U+1F36C: CANDY"><a href="/wiki/%F0%9F%8D%AC" class="mw-redirect" title="🍬">🍬</a>
</td>
<td title="U+1F36D: LOLLIPOP"><a href="/wiki/%F0%9F%8D%AD" class="mw-redirect" title="🍭">🍭</a>
</td>
<td title="U+1F36E: CUSTARD"><a href="/wiki/%F0%9F%8D%AE" class="mw-redirect" title="🍮">🍮</a>
</td>
<td title="U+1F36F: HONEY POT"><a href="/wiki/%F0%9F%8D%AF" class="mw-redirect" title="🍯">🍯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F37x
</td>
<td title="U+1F370: SHORTCAKE"><a href="/wiki/%F0%9F%8D%B0" class="mw-redirect" title="🍰">🍰</a>
</td>
<td title="U+1F371: BENTO BOX"><a href="/wiki/%F0%9F%8D%B1" class="mw-redirect" title="🍱">🍱</a>
</td>
<td title="U+1F372: POT OF FOOD"><a href="/wiki/%F0%9F%8D%B2" class="mw-redirect" title="🍲">🍲</a>
</td>
<td title="U+1F373: COOKING"><a href="/wiki/%F0%9F%8D%B3" class="mw-redirect" title="🍳">🍳</a>
</td>
<td title="U+1F374: FORK AND KNIFE"><a href="/wiki/%F0%9F%8D%B4" class="mw-redirect" title="🍴">🍴</a>
</td>
<td title="U+1F375: TEACUP WITHOUT HANDLE"><a href="/wiki/%F0%9F%8D%B5" class="mw-redirect" title="🍵">🍵</a>
</td>
<td title="U+1F376: SAKE BOTTLE AND CUP"><a href="/wiki/%F0%9F%8D%B6" class="mw-redirect" title="🍶">🍶</a>
</td>
<td title="U+1F377: WINE GLASS"><a href="/wiki/%F0%9F%8D%B7" class="mw-redirect" title="🍷">🍷</a>
</td>
<td title="U+1F378: COCKTAIL GLASS"><a href="/wiki/%F0%9F%8D%B8" class="mw-redirect" title="🍸">🍸</a>
</td>
<td title="U+1F379: TROPICAL DRINK"><a href="/wiki/%F0%9F%8D%B9" class="mw-redirect" title="🍹">🍹</a>
</td>
<td title="U+1F37A: BEER MUG"><a href="/wiki/%F0%9F%8D%BA" class="mw-redirect" title="🍺">🍺</a>
</td>
<td title="U+1F37B: CLINKING BEER MUGS"><a href="/wiki/%F0%9F%8D%BB" class="mw-redirect" title="🍻">🍻</a>
</td>
<td title="U+1F37C: BABY BOTTLE"><a href="/wiki/%F0%9F%8D%BC" class="mw-redirect" title="🍼">🍼</a>
</td>
<td title="U+1F37D: FORK AND KNIFE WITH PLATE"><a href="/wiki/%F0%9F%8D%BD" class="mw-redirect" title="🍽">🍽️</a>
</td>
<td title="U+1F37E: BOTTLE WITH POPPING CORK"><a href="/wiki/%F0%9F%8D%BE" class="mw-redirect" title="🍾">🍾</a>
</td>
<td title="U+1F37F: POPCORN"><a href="/wiki/%F0%9F%8D%BF" class="mw-redirect" title="🍿">🍿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F38x
</td>
<td title="U+1F380: RIBBON"><a href="/wiki/%F0%9F%8E%80" class="mw-redirect" title="🎀">🎀</a>
</td>
<td title="U+1F381: WRAPPED PRESENT"><a href="/wiki/%F0%9F%8E%81" class="mw-redirect" title="🎁">🎁</a>
</td>
<td title="U+1F382: BIRTHDAY CAKE"><a href="/wiki/%F0%9F%8E%82" class="mw-redirect" title="🎂">🎂</a>
</td>
<td title="U+1F383: JACK-O-LANTERN"><a href="/wiki/%F0%9F%8E%83" class="mw-redirect" title="🎃">🎃</a>
</td>
<td title="U+1F384: CHRISTMAS TREE"><a href="/wiki/%F0%9F%8E%84" class="mw-redirect" title="🎄">🎄</a>
</td>
<td title="U+1F385: FATHER CHRISTMAS"><a href="/wiki/%F0%9F%8E%85" class="mw-redirect" title="🎅">🎅</a>
</td>
<td title="U+1F386: FIREWORKS"><a href="/wiki/%F0%9F%8E%86" class="mw-redirect" title="🎆">🎆</a>
</td>
<td title="U+1F387: FIREWORK SPARKLER"><a href="/wiki/%F0%9F%8E%87" class="mw-redirect" title="🎇">🎇</a>
</td>
<td title="U+1F388: BALLOON"><a href="/wiki/%F0%9F%8E%88" class="mw-redirect" title="🎈">🎈</a>
</td>
<td title="U+1F389: PARTY POPPER"><a href="/wiki/%F0%9F%8E%89" class="mw-redirect" title="🎉">🎉</a>
</td>
<td title="U+1F38A: CONFETTI BALL"><a href="/wiki/%F0%9F%8E%8A" class="mw-redirect" title="🎊">🎊</a>
</td>
<td title="U+1F38B: TANABATA TREE"><a href="/wiki/%F0%9F%8E%8B" class="mw-redirect" title="🎋">🎋</a>
</td>
<td title="U+1F38C: CROSSED FLAGS"><a href="/wiki/%F0%9F%8E%8C" class="mw-redirect" title="🎌">🎌</a>
</td>
<td title="U+1F38D: PINE DECORATION"><a href="/wiki/%F0%9F%8E%8D" class="mw-redirect" title="🎍">🎍</a>
</td>
<td title="U+1F38E: JAPANESE DOLLS"><a href="/wiki/%F0%9F%8E%8E" class="mw-redirect" title="🎎">🎎</a>
</td>
<td title="U+1F38F: CARP STREAMER"><a href="/wiki/%F0%9F%8E%8F" class="mw-redirect" title="🎏">🎏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F39x
</td>
<td title="U+1F390: WIND CHIME"><a href="/wiki/%F0%9F%8E%90" class="mw-redirect" title="🎐">🎐</a>
</td>
<td title="U+1F391: MOON VIEWING CEREMONY"><a href="/wiki/%F0%9F%8E%91" class="mw-redirect" title="🎑">🎑</a>
</td>
<td title="U+1F392: SCHOOL SATCHEL"><a href="/wiki/%F0%9F%8E%92" class="mw-redirect" title="🎒">🎒</a>
</td>
<td title="U+1F393: GRADUATION CAP"><a href="/wiki/%F0%9F%8E%93" class="mw-redirect" title="🎓">🎓</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F396: MILITARY MEDAL"><a href="/wiki/%F0%9F%8E%96" class="mw-redirect" title="🎖">🎖️</a>
</td>
<td title="U+1F397: REMINDER RIBBON"><a href="/wiki/%F0%9F%8E%97" class="mw-redirect" title="🎗">🎗️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F399: STUDIO MICROPHONE"><a href="/wiki/%F0%9F%8E%99" class="mw-redirect" title="🎙">🎙️</a>
</td>
<td title="U+1F39A: LEVEL SLIDER"><a href="/wiki/%F0%9F%8E%9A" class="mw-redirect" title="🎚">🎚️</a>
</td>
<td title="U+1F39B: CONTROL KNOBS"><a href="/wiki/%F0%9F%8E%9B" class="mw-redirect" title="🎛">🎛️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F39E: FILM FRAMES"><a href="/wiki/%F0%9F%8E%9E" class="mw-redirect" title="🎞">🎞️</a>
</td>
<td title="U+1F39F: ADMISSION TICKETS"><a href="/wiki/%F0%9F%8E%9F" class="mw-redirect" title="🎟">🎟️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F3Ax
</td>
<td title="U+1F3A0: CAROUSEL HORSE"><a href="/wiki/%F0%9F%8E%A0" class="mw-redirect" title="🎠">🎠</a>
</td>
<td title="U+1F3A1: FERRIS WHEEL"><a href="/wiki/%F0%9F%8E%A1" class="mw-redirect" title="🎡">🎡</a>
</td>
<td title="U+1F3A2: ROLLER COASTER"><a href="/wiki/%F0%9F%8E%A2" class="mw-redirect" title="🎢">🎢</a>
</td>
<td title="U+1F3A3: FISHING POLE AND FISH"><a href="/wiki/%F0%9F%8E%A3" class="mw-redirect" title="🎣">🎣</a>
</td>
<td title="U+1F3A4: MICROPHONE"><a href="/wiki/%F0%9F%8E%A4" class="mw-redirect" title="🎤">🎤</a>
</td>
<td title="U+1F3A5: MOVIE CAMERA"><a href="/wiki/%F0%9F%8E%A5" class="mw-redirect" title="🎥">🎥</a>
</td>
<td title="U+1F3A6: CINEMA"><a href="/wiki/%F0%9F%8E%A6" class="mw-redirect" title="🎦">🎦</a>
</td>
<td title="U+1F3A7: HEADPHONE"><a href="/wiki/%F0%9F%8E%A7" class="mw-redirect" title="🎧">🎧</a>
</td>
<td title="U+1F3A8: ARTIST PALETTE"><a href="/wiki/%F0%9F%8E%A8" class="mw-redirect" title="🎨">🎨</a>
</td>
<td title="U+1F3A9: TOP HAT"><a href="/wiki/%F0%9F%8E%A9" class="mw-redirect" title="🎩">🎩</a>
</td>
<td title="U+1F3AA: CIRCUS TENT"><a href="/wiki/%F0%9F%8E%AA" class="mw-redirect" title="🎪">🎪</a>
</td>
<td title="U+1F3AB: TICKET"><a href="/wiki/%F0%9F%8E%AB" class="mw-redirect" title="🎫">🎫</a>
</td>
<td title="U+1F3AC: CLAPPER BOARD"><a href="/wiki/%F0%9F%8E%AC" class="mw-redirect" title="🎬">🎬</a>
</td>
<td title="U+1F3AD: PERFORMING ARTS"><a href="/wiki/%F0%9F%8E%AD" class="mw-redirect" title="🎭">🎭</a>
</td>
<td title="U+1F3AE: VIDEO GAME"><a href="/wiki/%F0%9F%8E%AE" class="mw-redirect" title="🎮">🎮</a>
</td>
<td title="U+1F3AF: DIRECT HIT"><a href="/wiki/%F0%9F%8E%AF" class="mw-redirect" title="🎯">🎯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F3Bx
</td>
<td title="U+1F3B0: SLOT MACHINE"><a href="/wiki/%F0%9F%8E%B0" class="mw-redirect" title="🎰">🎰</a>
</td>
<td title="U+1F3B1: BILLIARDS"><a href="/wiki/%F0%9F%8E%B1" class="mw-redirect" title="🎱">🎱</a>
</td>
<td title="U+1F3B2: GAME DIE"><a href="/wiki/%F0%9F%8E%B2" class="mw-redirect" title="🎲">🎲</a>
</td>
<td title="U+1F3B3: BOWLING"><a href="/wiki/%F0%9F%8E%B3" class="mw-redirect" title="🎳">🎳</a>
</td>
<td title="U+1F3B4: FLOWER PLAYING CARDS"><a href="/wiki/%F0%9F%8E%B4" class="mw-redirect" title="🎴">🎴</a>
</td>
<td title="U+1F3B5: MUSICAL NOTE"><a href="/wiki/%F0%9F%8E%B5" class="mw-redirect" title="🎵">🎵</a>
</td>
<td title="U+1F3B6: MULTIPLE MUSICAL NOTES"><a href="/wiki/%F0%9F%8E%B6" class="mw-redirect" title="🎶">🎶</a>
</td>
<td title="U+1F3B7: SAXOPHONE"><a href="/wiki/%F0%9F%8E%B7" class="mw-redirect" title="🎷">🎷</a>
</td>
<td title="U+1F3B8: GUITAR"><a href="/wiki/%F0%9F%8E%B8" class="mw-redirect" title="🎸">🎸</a>
</td>
<td title="U+1F3B9: MUSICAL KEYBOARD"><a href="/wiki/%F0%9F%8E%B9" class="mw-redirect" title="🎹">🎹</a>
</td>
<td title="U+1F3BA: TRUMPET"><a href="/wiki/%F0%9F%8E%BA" class="mw-redirect" title="🎺">🎺</a>
</td>
<td title="U+1F3BB: VIOLIN"><a href="/wiki/%F0%9F%8E%BB" class="mw-redirect" title="🎻">🎻</a>
</td>
<td title="U+1F3BC: MUSICAL SCORE"><a href="/wiki/%F0%9F%8E%BC" class="mw-redirect" title="🎼">🎼</a>
</td>
<td title="U+1F3BD: RUNNING SHIRT WITH SASH"><a href="/wiki/%F0%9F%8E%BD" class="mw-redirect" title="🎽">🎽</a>
</td>
<td title="U+1F3BE: TENNIS RACQUET AND BALL"><a href="/wiki/%F0%9F%8E%BE" class="mw-redirect" title="🎾">🎾</a>
</td>
<td title="U+1F3BF: SKI AND SKI BOOT"><a href="/wiki/%F0%9F%8E%BF" class="mw-redirect" title="🎿">🎿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F3Cx
</td>
<td title="U+1F3C0: BASKETBALL AND HOOP"><a href="/wiki/%F0%9F%8F%80" class="mw-redirect" title="🏀">🏀</a>
</td>
<td title="U+1F3C1: CHEQUERED FLAG"><a href="/wiki/%F0%9F%8F%81" class="mw-redirect" title="🏁">🏁</a>
</td>
<td title="U+1F3C2: SNOWBOARDER"><a href="/wiki/%F0%9F%8F%82" class="mw-redirect" title="🏂">🏂</a>
</td>
<td title="U+1F3C3: RUNNER"><a href="/wiki/%F0%9F%8F%83" class="mw-redirect" title="🏃">🏃</a>
</td>
<td title="U+1F3C4: SURFER"><a href="/wiki/%F0%9F%8F%84" class="mw-redirect" title="🏄">🏄</a>
</td>
<td title="U+1F3C5: SPORTS MEDAL"><a href="/wiki/%F0%9F%8F%85" class="mw-redirect" title="🏅">🏅</a>
</td>
<td title="U+1F3C6: TROPHY"><a href="/wiki/%F0%9F%8F%86" class="mw-redirect" title="🏆">🏆</a>
</td>
<td title="U+1F3C7: HORSE RACING"><a href="/wiki/%F0%9F%8F%87" class="mw-redirect" title="🏇">🏇</a>
</td>
<td title="U+1F3C8: AMERICAN FOOTBALL"><a href="/wiki/%F0%9F%8F%88" class="mw-redirect" title="🏈">🏈</a>
</td>
<td title="U+1F3C9: RUGBY FOOTBALL"><a href="/wiki/%F0%9F%8F%89" class="mw-redirect" title="🏉">🏉</a>
</td>
<td title="U+1F3CA: SWIMMER"><a href="/wiki/%F0%9F%8F%8A" class="mw-redirect" title="🏊">🏊</a>
</td>
<td title="U+1F3CB: WEIGHT LIFTER"><a href="/w/index.php?title=Weightlifting_(disambiguation)&amp;action=edit&amp;redlink=1" class="new" title="Weightlifting (disambiguation) (page does not exist)">🏋️</a>
</td>
<td title="U+1F3CC: GOLFER"><a href="/wiki/%F0%9F%8F%8C" class="mw-redirect" title="🏌">🏌️</a>
</td>
<td title="U+1F3CD: RACING MOTORCYCLE"><a href="/wiki/%F0%9F%8F%8D" class="mw-redirect" title="🏍">🏍️</a>
</td>
<td title="U+1F3CE: RACING CAR"><a href="/wiki/%F0%9F%8F%8E" class="mw-redirect" title="🏎">🏎️</a>
</td>
<td title="U+1F3CF: CRICKET BAT AND BALL"><a href="/wiki/%F0%9F%8F%8F" class="mw-redirect" title="🏏">🏏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F3Dx
</td>
<td title="U+1F3D0: VOLLEYBALL"><a href="/wiki/%F0%9F%8F%90" class="mw-redirect" title="🏐">🏐</a>
</td>
<td title="U+1F3D1: FIELD HOCKEY STICK AND BALL"><a href="/wiki/%F0%9F%8F%91" class="mw-redirect" title="🏑">🏑</a>
</td>
<td title="U+1F3D2: ICE HOCKEY STICK AND PUCK"><a href="/wiki/%F0%9F%8F%92" class="mw-redirect" title="🏒">🏒</a>
</td>
<td title="U+1F3D3: TABLE TENNIS PADDLE AND BALL"><a href="/wiki/%F0%9F%8F%93" class="mw-redirect" title="🏓">🏓</a>
</td>
<td title="U+1F3D4: SNOW CAPPED MOUNTAIN"><a href="/wiki/%F0%9F%8F%94" class="mw-redirect" title="🏔">🏔️</a>
</td>
<td title="U+1F3D5: CAMPING"><a href="/wiki/%F0%9F%8F%95" class="mw-redirect" title="🏕">🏕️</a>
</td>
<td title="U+1F3D6: BEACH WITH UMBRELLA"><a href="/wiki/%F0%9F%8F%96" class="mw-redirect" title="🏖">🏖️</a>
</td>
<td title="U+1F3D7: BUILDING CONSTRUCTION"><a href="/wiki/%F0%9F%8F%97" class="mw-redirect" title="🏗">🏗️</a>
</td>
<td title="U+1F3D8: HOUSE BUILDINGS"><a href="/wiki/%F0%9F%8F%98" class="mw-redirect" title="🏘">🏘️</a>
</td>
<td title="U+1F3D9: CITYSCAPE"><a href="/wiki/%F0%9F%8F%99" class="mw-redirect" title="🏙">🏙️</a>
</td>
<td title="U+1F3DA: DERELICT HOUSE BUILDING"><a href="/wiki/%F0%9F%8F%9A" class="mw-redirect" title="🏚">🏚️</a>
</td>
<td title="U+1F3DB: CLASSICAL BUILDING"><a href="/wiki/%F0%9F%8F%9B" class="mw-redirect" title="🏛">🏛️</a>
</td>
<td title="U+1F3DC: DESERT"><a href="/wiki/%F0%9F%8F%9C" class="mw-redirect" title="🏜">🏜️</a>
</td>
<td title="U+1F3DD: DESERT ISLAND"><a href="/wiki/%F0%9F%8F%9D" class="mw-redirect" title="🏝">🏝️</a>
</td>
<td title="U+1F3DE: NATIONAL PARK"><a href="/wiki/%F0%9F%8F%9E" class="mw-redirect" title="🏞">🏞️</a>
</td>
<td title="U+1F3DF: STADIUM"><a href="/wiki/%F0%9F%8F%9F" class="mw-redirect" title="🏟">🏟️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F3Ex
</td>
<td title="U+1F3E0: HOUSE BUILDING"><a href="/wiki/%F0%9F%8F%A0" class="mw-redirect" title="🏠">🏠</a>
</td>
<td title="U+1F3E1: HOUSE WITH GARDEN"><a href="/wiki/%F0%9F%8F%A1" class="mw-redirect" title="🏡">🏡</a>
</td>
<td title="U+1F3E2: OFFICE BUILDING"><a href="/wiki/%F0%9F%8F%A2" class="mw-redirect" title="🏢">🏢</a>
</td>
<td title="U+1F3E3: JAPANESE POST OFFICE"><a href="/wiki/%E3%80%92" class="mw-redirect" title="〒">🏣</a>
</td>
<td title="U+1F3E4: EUROPEAN POST OFFICE"><a href="/wiki/%F0%9F%8F%A4" class="mw-redirect" title="🏤">🏤</a>
</td>
<td title="U+1F3E5: HOSPITAL"><a href="/wiki/%F0%9F%8F%A5" class="mw-redirect" title="🏥">🏥</a>
</td>
<td title="U+1F3E6: BANK"><a href="/wiki/%F0%9F%8F%A6" class="mw-redirect" title="🏦">🏦</a>
</td>
<td title="U+1F3E7: AUTOMATED TELLER MACHINE"><a href="/wiki/%F0%9F%8F%A7" class="mw-redirect" title="🏧">🏧</a>
</td>
<td title="U+1F3E8: HOTEL"><a href="/wiki/%F0%9F%8F%A8" class="mw-redirect" title="🏨">🏨</a>
</td>
<td title="U+1F3E9: LOVE HOTEL"><a href="/wiki/%F0%9F%8F%A9" class="mw-redirect" title="🏩">🏩</a>
</td>
<td title="U+1F3EA: CONVENIENCE STORE"><a href="/wiki/%F0%9F%8F%AA" class="mw-redirect" title="🏪">🏪</a>
</td>
<td title="U+1F3EB: SCHOOL"><a href="/wiki/%F0%9F%8F%AB" class="mw-redirect" title="🏫">🏫</a>
</td>
<td title="U+1F3EC: DEPARTMENT STORE"><a href="/wiki/%F0%9F%8F%AC" class="mw-redirect" title="🏬">🏬</a>
</td>
<td title="U+1F3ED: FACTORY"><a href="/wiki/%F0%9F%8F%AD" class="mw-redirect" title="🏭">🏭</a>
</td>
<td title="U+1F3EE: IZAKAYA LANTERN"><a href="/wiki/%F0%9F%8F%AE" class="mw-redirect" title="🏮">🏮</a>
</td>
<td title="U+1F3EF: JAPANESE CASTLE"><a href="/wiki/%F0%9F%8F%AF" class="mw-redirect" title="🏯">🏯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F3Fx
</td>
<td title="U+1F3F0: EUROPEAN CASTLE"><a href="/wiki/%F0%9F%8F%B0" class="mw-redirect" title="🏰">🏰</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F3F3: WAVING WHITE FLAG"><a href="/wiki/%F0%9F%8F%B3" class="mw-redirect" title="🏳">🏳️</a>
</td>
<td title="U+1F3F4: WAVING BLACK FLAG"><a href="/wiki/%F0%9F%8F%B4" class="mw-redirect" title="🏴">🏴</a>
</td>
<td title="U+1F3F5: ROSETTE"><a href="/wiki/%F0%9F%8F%B5" class="mw-redirect" title="🏵">🏵️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F3F7: LABEL"><a href="/wiki/%F0%9F%8F%B7" class="mw-redirect" title="🏷">🏷️</a>
</td>
<td title="U+1F3F8: BADMINTON RACQUET AND SHUTTLECOCK"><a href="/wiki/%F0%9F%8F%B8" class="mw-redirect" title="🏸">🏸</a>
</td>
<td title="U+1F3F9: BOW AND ARROW"><a href="/wiki/%F0%9F%8F%B9" class="mw-redirect" title="🏹">🏹</a>
</td>
<td title="U+1F3FA: AMPHORA"><a href="/wiki/%F0%9F%8F%BA" class="mw-redirect" title="🏺">🏺</a>
</td>
<td title="U+1F3FB: EMOJI MODIFIER FITZPATRICK TYPE-1-2"><a href="/wiki/%F0%9F%8F%BB" class="mw-redirect" title="🏻">🏻</a>
</td>
<td title="U+1F3FC: EMOJI MODIFIER FITZPATRICK TYPE-3"><a href="/wiki/%F0%9F%8F%BC" class="mw-redirect" title="🏼">🏼</a>
</td>
<td title="U+1F3FD: EMOJI MODIFIER FITZPATRICK TYPE-4"><a href="/wiki/%F0%9F%8F%BD" class="mw-redirect" title="🏽">🏽</a>
</td>
<td title="U+1F3FE: EMOJI MODIFIER FITZPATRICK TYPE-5"><a href="/wiki/%F0%9F%8F%BE" class="mw-redirect" title="🏾">🏾</a>
</td>
<td title="U+1F3FF: EMOJI MODIFIER FITZPATRICK TYPE-6"><a href="/wiki/%F0%9F%8F%BF" class="mw-redirect" title="🏿">🏿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F40x
</td>
<td title="U+1F400: RAT"><a href="/wiki/%F0%9F%90%80" class="mw-redirect" title="🐀">🐀</a>
</td>
<td title="U+1F401: MOUSE"><a href="/wiki/%F0%9F%90%81" class="mw-redirect" title="🐁">🐁</a>
</td>
<td title="U+1F402: OX"><a href="/wiki/%F0%9F%90%82" class="mw-redirect" title="🐂">🐂</a>
</td>
<td title="U+1F403: WATER BUFFALO"><a href="/wiki/%F0%9F%90%83" class="mw-redirect" title="🐃">🐃</a>
</td>
<td title="U+1F404: COW"><a href="/wiki/%F0%9F%90%84" class="mw-redirect" title="🐄">🐄</a>
</td>
<td title="U+1F405: TIGER"><a href="/wiki/%F0%9F%90%85" class="mw-redirect" title="🐅">🐅</a>
</td>
<td title="U+1F406: LEOPARD"><a href="/wiki/%F0%9F%90%86" class="mw-redirect" title="🐆">🐆</a>
</td>
<td title="U+1F407: RABBIT"><a href="/wiki/%F0%9F%90%87" class="mw-redirect" title="🐇">🐇</a>
</td>
<td title="U+1F408: CAT"><a href="/wiki/%F0%9F%90%88" class="mw-redirect" title="🐈">🐈</a>
</td>
<td title="U+1F409: DRAGON"><a href="/wiki/%F0%9F%90%89" class="mw-redirect" title="🐉">🐉</a>
</td>
<td title="U+1F40A: CROCODILE"><a href="/wiki/%F0%9F%90%8A" class="mw-redirect" title="🐊">🐊</a>
</td>
<td title="U+1F40B: WHALE"><a href="/wiki/%F0%9F%90%8B" class="mw-redirect" title="🐋">🐋</a>
</td>
<td title="U+1F40C: SNAIL"><a href="/wiki/%F0%9F%90%8C" class="mw-redirect" title="🐌">🐌</a>
</td>
<td title="U+1F40D: SNAKE"><a href="/wiki/%F0%9F%90%8D" class="mw-redirect" title="🐍">🐍</a>
</td>
<td title="U+1F40E: HORSE"><a href="/wiki/%F0%9F%90%8E" class="mw-redirect" title="🐎">🐎</a>
</td>
<td title="U+1F40F: RAM"><a href="/wiki/%F0%9F%90%8F" class="mw-redirect" title="🐏">🐏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F41x
</td>
<td title="U+1F410: GOAT"><a href="/wiki/%F0%9F%90%90" class="mw-redirect" title="🐐">🐐</a>
</td>
<td title="U+1F411: SHEEP"><a href="/wiki/%F0%9F%90%91" class="mw-redirect" title="🐑">🐑</a>
</td>
<td title="U+1F412: MONKEY"><a href="/wiki/%F0%9F%90%92" class="mw-redirect" title="🐒">🐒</a>
</td>
<td title="U+1F413: ROOSTER"><a href="/wiki/%F0%9F%90%93" class="mw-redirect" title="🐓">🐓</a>
</td>
<td title="U+1F414: CHICKEN"><a href="/wiki/%F0%9F%90%94" class="mw-redirect" title="🐔">🐔</a>
</td>
<td title="U+1F415: DOG"><a href="/wiki/%F0%9F%90%95" class="mw-redirect" title="🐕">🐕</a>
</td>
<td title="U+1F416: PIG"><a href="/wiki/%F0%9F%90%96" class="mw-redirect" title="🐖">🐖</a>
</td>
<td title="U+1F417: BOAR"><a href="/wiki/%F0%9F%90%97" class="mw-redirect" title="🐗">🐗</a>
</td>
<td title="U+1F418: ELEPHANT"><a href="/wiki/%F0%9F%90%98" class="mw-redirect" title="🐘">🐘</a>
</td>
<td title="U+1F419: OCTOPUS"><a href="/wiki/%F0%9F%90%99" class="mw-redirect" title="🐙">🐙</a>
</td>
<td title="U+1F41A: SPIRAL SHELL"><a href="/wiki/%F0%9F%90%9A" class="mw-redirect" title="🐚">🐚</a>
</td>
<td title="U+1F41B: BUG"><a href="/wiki/Bug_(disambiguation)#Biology" class="mw-redirect mw-disambig" title="Bug (disambiguation)">🐛</a>
</td>
<td title="U+1F41C: ANT"><a href="/wiki/%F0%9F%90%9C" class="mw-redirect" title="🐜">🐜</a>
</td>
<td title="U+1F41D: HONEYBEE"><a href="/wiki/%F0%9F%90%9D" class="mw-redirect" title="🐝">🐝</a>
</td>
<td title="U+1F41E: LADY BEETLE"><a href="/wiki/%F0%9F%90%9E" class="mw-redirect" title="🐞">🐞</a>
</td>
<td title="U+1F41F: FISH"><a href="/wiki/%F0%9F%90%9F" class="mw-redirect" title="🐟">🐟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F42x
</td>
<td title="U+1F420: TROPICAL FISH"><a href="/wiki/%F0%9F%90%A0" class="mw-redirect" title="🐠">🐠</a>
</td>
<td title="U+1F421: BLOWFISH"><a href="/wiki/%F0%9F%90%A1" class="mw-redirect" title="🐡">🐡</a>
</td>
<td title="U+1F422: TURTLE"><a href="/wiki/%F0%9F%90%A2" class="mw-redirect" title="🐢">🐢</a>
</td>
<td title="U+1F423: HATCHING CHICK"><a href="/wiki/%F0%9F%90%A3" class="mw-redirect" title="🐣">🐣</a>
</td>
<td title="U+1F424: BABY CHICK"><a href="/wiki/%F0%9F%90%A4" class="mw-redirect" title="🐤">🐤</a>
</td>
<td title="U+1F425: FRONT-FACING BABY CHICK"><a href="/wiki/%F0%9F%90%A5" class="mw-redirect" title="🐥">🐥</a>
</td>
<td title="U+1F426: BIRD"><a href="/wiki/%F0%9F%90%A6" class="mw-redirect" title="🐦">🐦</a>
</td>
<td title="U+1F427: PENGUIN"><a href="/wiki/%F0%9F%90%A7" class="mw-redirect" title="🐧">🐧</a>
</td>
<td title="U+1F428: KOALA"><a href="/wiki/%F0%9F%90%A8" class="mw-redirect" title="🐨">🐨</a>
</td>
<td title="U+1F429: POODLE"><a href="/wiki/%F0%9F%90%A9" class="mw-redirect" title="🐩">🐩</a>
</td>
<td title="U+1F42A: DROMEDARY CAMEL"><a href="/wiki/%F0%9F%90%AA" class="mw-redirect" title="🐪">🐪</a>
</td>
<td title="U+1F42B: BACTRIAN CAMEL"><a href="/wiki/%F0%9F%90%AB" class="mw-redirect" title="🐫">🐫</a>
</td>
<td title="U+1F42C: DOLPHIN"><a href="/wiki/%F0%9F%90%AC" class="mw-redirect" title="🐬">🐬</a>
</td>
<td title="U+1F42D: MOUSE FACE"><a href="/wiki/%F0%9F%90%AD" class="mw-redirect" title="🐭">🐭</a>
</td>
<td title="U+1F42E: COW FACE"><a href="/wiki/%F0%9F%90%AE" class="mw-redirect" title="🐮">🐮</a>
</td>
<td title="U+1F42F: TIGER FACE"><a href="/wiki/%F0%9F%90%AF" class="mw-redirect" title="🐯">🐯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F43x
</td>
<td title="U+1F430: RABBIT FACE"><a href="/wiki/%F0%9F%90%B0" class="mw-redirect" title="🐰">🐰</a>
</td>
<td title="U+1F431: CAT FACE"><a href="/wiki/%F0%9F%90%B1" class="mw-redirect" title="🐱">🐱</a>
</td>
<td title="U+1F432: DRAGON FACE"><a href="/wiki/%F0%9F%90%B2" class="mw-redirect" title="🐲">🐲</a>
</td>
<td title="U+1F433: SPOUTING WHALE"><a href="/wiki/%F0%9F%90%B3" class="mw-redirect" title="🐳">🐳</a>
</td>
<td title="U+1F434: HORSE FACE"><a href="/wiki/%F0%9F%90%B4" class="mw-redirect" title="🐴">🐴</a>
</td>
<td title="U+1F435: MONKEY FACE"><a href="/wiki/%F0%9F%90%B5" class="mw-redirect" title="🐵">🐵</a>
</td>
<td title="U+1F436: DOG FACE"><a href="/wiki/%F0%9F%90%B6" class="mw-redirect" title="🐶">🐶</a>
</td>
<td title="U+1F437: PIG FACE"><a href="/wiki/%F0%9F%90%B7" class="mw-redirect" title="🐷">🐷</a>
</td>
<td title="U+1F438: FROG FACE"><a href="/wiki/%F0%9F%90%B8" class="mw-redirect" title="🐸">🐸</a>
</td>
<td title="U+1F439: HAMSTER FACE"><a href="/wiki/%F0%9F%90%B9" class="mw-redirect" title="🐹">🐹</a>
</td>
<td title="U+1F43A: WOLF FACE"><a href="/wiki/%F0%9F%90%BA" class="mw-redirect" title="🐺">🐺</a>
</td>
<td title="U+1F43B: BEAR FACE"><a href="/wiki/%F0%9F%90%BB" class="mw-redirect" title="🐻">🐻</a>
</td>
<td title="U+1F43C: PANDA FACE"><a href="/wiki/%F0%9F%90%BC" class="mw-redirect" title="🐼">🐼</a>
</td>
<td title="U+1F43D: PIG NOSE"><a href="/wiki/%F0%9F%90%BD" class="mw-redirect" title="🐽">🐽</a>
</td>
<td title="U+1F43E: PAW PRINTS"><a href="/wiki/%F0%9F%90%BE" class="mw-redirect" title="🐾">🐾</a>
</td>
<td title="U+1F43F: CHIPMUNK"><a href="/wiki/%F0%9F%90%BF" class="mw-redirect" title="🐿">🐿️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F44x
</td>
<td title="U+1F440: EYES"><a href="/wiki/%F0%9F%91%80" class="mw-redirect" title="👀">👀</a>
</td>
<td title="U+1F441: EYE"><a href="/wiki/%F0%9F%91%81" class="mw-redirect" title="👁">👁️</a>
</td>
<td title="U+1F442: EAR"><a href="/wiki/%F0%9F%91%82" class="mw-redirect" title="👂">👂</a>
</td>
<td title="U+1F443: NOSE"><a href="/wiki/%F0%9F%91%83" class="mw-redirect" title="👃">👃</a>
</td>
<td title="U+1F444: MOUTH"><a href="/wiki/%F0%9F%91%84" class="mw-redirect" title="👄">👄</a>
</td>
<td title="U+1F445: TONGUE"><a href="/wiki/%F0%9F%91%85" class="mw-redirect" title="👅">👅</a>
</td>
<td title="U+1F446: WHITE UP POINTING BACKHAND INDEX"><a href="/wiki/%F0%9F%91%86" class="mw-redirect" title="👆">👆</a>
</td>
<td title="U+1F447: WHITE DOWN POINTING BACKHAND INDEX"><a href="/wiki/%F0%9F%91%87" class="mw-redirect" title="👇">👇</a>
</td>
<td title="U+1F448: WHITE LEFT POINTING BACKHAND INDEX"><a href="/wiki/%F0%9F%91%88" class="mw-redirect" title="👈">👈</a>
</td>
<td title="U+1F449: WHITE RIGHT POINTING BACKHAND INDEX"><a href="/wiki/%F0%9F%91%89" class="mw-redirect" title="👉">👉</a>
</td>
<td title="U+1F44A: FISTED HAND SIGN"><a href="/wiki/Fist_(hand)" class="mw-redirect" title="Fist (hand)">👊</a>
</td>
<td title="U+1F44B: WAVING HAND SIGN"><a href="/wiki/%F0%9F%91%8B" class="mw-redirect" title="👋">👋</a>
</td>
<td title="U+1F44C: OK HAND SIGN"><a href="/wiki/%F0%9F%91%8C" class="mw-redirect" title="👌">👌</a>
</td>
<td title="U+1F44D: THUMBS UP SIGN"><a href="/wiki/%F0%9F%91%8D" class="mw-redirect" title="👍">👍</a>
</td>
<td title="U+1F44E: THUMBS DOWN SIGN"><a href="/wiki/%F0%9F%91%8E" class="mw-redirect" title="👎">👎</a>
</td>
<td title="U+1F44F: CLAPPING HANDS SIGN"><a href="/wiki/%F0%9F%91%8F" class="mw-redirect" title="👏">👏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F45x
</td>
<td title="U+1F450: OPEN HANDS SIGN"><a href="/wiki/%F0%9F%91%90" class="mw-redirect" title="👐">👐</a>
</td>
<td title="U+1F451: CROWN"><a href="/wiki/%F0%9F%91%91" class="mw-redirect" title="👑">👑</a>
</td>
<td title="U+1F452: WOMANS HAT"><a href="/wiki/%F0%9F%91%92" class="mw-redirect" title="👒">👒</a>
</td>
<td title="U+1F453: EYEGLASSES"><a href="/wiki/%F0%9F%91%93" class="mw-redirect" title="👓">👓</a>
</td>
<td title="U+1F454: NECKTIE"><a href="/wiki/%F0%9F%91%94" class="mw-redirect" title="👔">👔</a>
</td>
<td title="U+1F455: T-SHIRT"><a href="/wiki/%F0%9F%91%95" class="mw-redirect" title="👕">👕</a>
</td>
<td title="U+1F456: JEANS"><a href="/wiki/%F0%9F%91%96" class="mw-redirect" title="👖">👖</a>
</td>
<td title="U+1F457: DRESS"><a href="/wiki/%F0%9F%91%97" class="mw-redirect" title="👗">👗</a>
</td>
<td title="U+1F458: KIMONO"><a href="/wiki/%F0%9F%91%98" class="mw-redirect" title="👘">👘</a>
</td>
<td title="U+1F459: BIKINI"><a href="/wiki/%F0%9F%91%99" class="mw-redirect" title="👙">👙</a>
</td>
<td title="U+1F45A: WOMANS CLOTHES"><a href="/wiki/%F0%9F%91%9A" class="mw-redirect" title="👚">👚</a>
</td>
<td title="U+1F45B: PURSE"><a href="/wiki/%F0%9F%91%9B" class="mw-redirect" title="👛">👛</a>
</td>
<td title="U+1F45C: HANDBAG"><a href="/wiki/%F0%9F%91%9C" class="mw-redirect" title="👜">👜</a>
</td>
<td title="U+1F45D: POUCH"><a href="/wiki/Pouch_(disambiguation)" class="mw-redirect mw-disambig" title="Pouch (disambiguation)">👝</a>
</td>
<td title="U+1F45E: MANS SHOE"><a href="/wiki/%F0%9F%91%9E" class="mw-redirect" title="👞">👞</a>
</td>
<td title="U+1F45F: ATHLETIC SHOE"><a href="/wiki/%F0%9F%91%9F" class="mw-redirect" title="👟">👟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F46x
</td>
<td title="U+1F460: HIGH-HEELED SHOE"><a href="/wiki/%F0%9F%91%A0" class="mw-redirect" title="👠">👠</a>
</td>
<td title="U+1F461: WOMANS SANDAL"><a href="/wiki/%F0%9F%91%A1" class="mw-redirect" title="👡">👡</a>
</td>
<td title="U+1F462: WOMANS BOOTS"><a href="/wiki/%F0%9F%91%A2" class="mw-redirect" title="👢">👢</a>
</td>
<td title="U+1F463: FOOTPRINTS"><a href="/wiki/%F0%9F%91%A3" class="mw-redirect" title="👣">👣</a>
</td>
<td title="U+1F464: BUST IN SILHOUETTE"><a href="/wiki/%F0%9F%91%A4" class="mw-redirect" title="👤">👤</a>
</td>
<td title="U+1F465: BUSTS IN SILHOUETTE"><a href="/wiki/%F0%9F%91%A5" class="mw-redirect" title="👥">👥</a>
</td>
<td title="U+1F466: BOY"><a href="/wiki/%F0%9F%91%A6" class="mw-redirect" title="👦">👦</a>
</td>
<td title="U+1F467: GIRL"><a href="/wiki/%F0%9F%91%A7" class="mw-redirect" title="👧">👧</a>
</td>
<td title="U+1F468: MAN"><a href="/wiki/%F0%9F%91%A8" class="mw-redirect" title="👨">👨</a>
</td>
<td title="U+1F469: WOMAN"><a href="/wiki/%F0%9F%91%A9" class="mw-redirect" title="👩">👩</a>
</td>
<td title="U+1F46A: FAMILY"><a href="/wiki/%F0%9F%91%AA" class="mw-redirect" title="👪">👪</a>
</td>
<td title="U+1F46B: MAN AND WOMAN HOLDING HANDS"><a href="/wiki/%F0%9F%91%AB" class="mw-redirect" title="👫">👫</a>
</td>
<td title="U+1F46C: TWO MEN HOLDING HANDS"><a href="/wiki/%F0%9F%91%AC" class="mw-redirect" title="👬">👬</a>
</td>
<td title="U+1F46D: TWO WOMEN HOLDING HANDS"><a href="/wiki/%F0%9F%91%AD" class="mw-redirect" title="👭">👭</a>
</td>
<td title="U+1F46E: POLICE OFFICER"><a href="/wiki/%F0%9F%91%AE" class="mw-redirect" title="👮">👮</a>
</td>
<td title="U+1F46F: WOMAN WITH BUNNY EARS"><a href="/wiki/%F0%9F%91%AF" class="mw-redirect" title="👯">👯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F47x
</td>
<td title="U+1F470: BRIDE WITH VEIL"><a href="/wiki/%F0%9F%91%B0" class="mw-redirect" title="👰">👰</a>
</td>
<td title="U+1F471: PERSON WITH BLOND HAIR"><a href="/wiki/%F0%9F%91%B1" class="mw-redirect" title="👱">👱</a>
</td>
<td title="U+1F472: MAN WITH GUA PI MAO"><a href="/wiki/%F0%9F%91%B2" class="mw-redirect" title="👲">👲</a>
</td>
<td title="U+1F473: MAN WITH TURBAN"><a href="/wiki/%F0%9F%91%B3" class="mw-redirect" title="👳">👳</a>
</td>
<td title="U+1F474: OLDER MAN"><a href="/wiki/%F0%9F%91%B4" class="mw-redirect" title="👴">👴</a>
</td>
<td title="U+1F475: OLDER WOMAN"><a href="/wiki/%F0%9F%91%B5" class="mw-redirect" title="👵">👵</a>
</td>
<td title="U+1F476: BABY"><a href="/wiki/%F0%9F%91%B6" class="mw-redirect" title="👶">👶</a>
</td>
<td title="U+1F477: CONSTRUCTION WORKER"><a href="/wiki/%F0%9F%91%B7" class="mw-redirect" title="👷">👷</a>
</td>
<td title="U+1F478: PRINCESS"><a href="/wiki/%F0%9F%91%B8" class="mw-redirect" title="👸">👸</a>
</td>
<td title="U+1F479: JAPANESE OGRE"><a href="/wiki/%F0%9F%91%B9" class="mw-redirect" title="👹">👹</a>
</td>
<td title="U+1F47A: JAPANESE GOBLIN"><a href="/wiki/%F0%9F%91%BA" class="mw-redirect" title="👺">👺</a>
</td>
<td title="U+1F47B: GHOST"><a href="/wiki/%F0%9F%91%BB" class="mw-redirect" title="👻">👻</a>
</td>
<td title="U+1F47C: BABY ANGEL"><a href="/wiki/%F0%9F%91%BC" class="mw-redirect" title="👼">👼</a>
</td>
<td title="U+1F47D: EXTRATERRESTRIAL ALIEN"><a href="/wiki/%F0%9F%91%BD" class="mw-redirect" title="👽">👽</a>
</td>
<td title="U+1F47E: ALIEN MONSTER"><a href="/wiki/%F0%9F%91%BE" class="mw-redirect" title="👾">👾</a>
</td>
<td title="U+1F47F: IMP"><a href="/wiki/%F0%9F%91%BF" class="mw-redirect" title="👿">👿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F48x
</td>
<td title="U+1F480: SKULL"><a href="/wiki/%F0%9F%92%80" class="mw-redirect" title="💀">💀</a>
</td>
<td title="U+1F481: INFORMATION DESK PERSON"><a href="/w/index.php?title=%F0%9F%92%81&amp;action=edit&amp;redlink=1" class="new" title="💁 (page does not exist)">💁</a>
</td>
<td title="U+1F482: GUARDSMAN"><a href="/wiki/%F0%9F%92%82" class="mw-redirect" title="💂">💂</a>
</td>
<td title="U+1F483: DANCER"><a href="/wiki/%F0%9F%92%83" class="mw-redirect" title="💃">💃</a>
</td>
<td title="U+1F484: LIPSTICK"><a href="/wiki/%F0%9F%92%84" class="mw-redirect" title="💄">💄</a>
</td>
<td title="U+1F485: NAIL POLISH"><a href="/wiki/%F0%9F%92%85" class="mw-redirect" title="💅">💅</a>
</td>
<td title="U+1F486: FACE MASSAGE"><a href="/wiki/%F0%9F%92%86" class="mw-redirect" title="💆">💆</a>
</td>
<td title="U+1F487: HAIRCUT"><a href="/wiki/%F0%9F%92%87" class="mw-redirect" title="💇">💇</a>
</td>
<td title="U+1F488: BARBER POLE"><a href="/wiki/%F0%9F%92%88" class="mw-redirect" title="💈">💈</a>
</td>
<td title="U+1F489: SYRINGE"><a href="/wiki/%F0%9F%92%89" class="mw-redirect" title="💉">💉</a>
</td>
<td title="U+1F48A: PILL"><a href="/wiki/%F0%9F%92%8A" class="mw-redirect" title="💊">💊</a>
</td>
<td title="U+1F48B: KISS MARK"><a href="/wiki/%F0%9F%92%8B" class="mw-redirect" title="💋">💋</a>
</td>
<td title="U+1F48C: LOVE LETTER"><a href="/wiki/%F0%9F%92%8C" class="mw-redirect" title="💌">💌</a>
</td>
<td title="U+1F48D: RING"><a href="/wiki/%F0%9F%92%8D" class="mw-redirect" title="💍">💍</a>
</td>
<td title="U+1F48E: GEM STONE"><a href="/wiki/%F0%9F%92%8E" class="mw-redirect" title="💎">💎</a>
</td>
<td title="U+1F48F: KISS"><a href="/wiki/%F0%9F%92%8F" class="mw-redirect" title="💏">💏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F49x
</td>
<td title="U+1F490: BOUQUET"><a href="/wiki/%F0%9F%92%90" class="mw-redirect" title="💐">💐</a>
</td>
<td title="U+1F491: COUPLE WITH HEART"><a href="/wiki/%F0%9F%92%91" class="mw-redirect" title="💑">💑</a>
</td>
<td title="U+1F492: WEDDING"><a href="/wiki/%F0%9F%92%92" class="mw-redirect" title="💒">💒</a>
</td>
<td title="U+1F493: BEATING HEART"><a href="/wiki/%F0%9F%92%93" class="mw-redirect" title="💓">💓</a>
</td>
<td title="U+1F494: BROKEN HEART"><a href="/wiki/%F0%9F%92%94" class="mw-redirect" title="💔">💔</a>
</td>
<td title="U+1F495: TWO HEARTS"><a href="/wiki/%F0%9F%92%95" class="mw-redirect" title="💕">💕</a>
</td>
<td title="U+1F496: SPARKLING HEART"><a href="/wiki/%F0%9F%92%96" class="mw-redirect" title="💖">💖</a>
</td>
<td title="U+1F497: GROWING HEART"><a href="/wiki/%F0%9F%92%97" class="mw-redirect" title="💗">💗</a>
</td>
<td title="U+1F498: HEART WITH ARROW"><a href="/wiki/%F0%9F%92%98" class="mw-redirect" title="💘">💘</a>
</td>
<td title="U+1F499: BLUE HEART"><a href="/wiki/%F0%9F%92%99" class="mw-redirect" title="💙">💙</a>
</td>
<td title="U+1F49A: GREEN HEART"><a href="/wiki/%F0%9F%92%9A" class="mw-redirect" title="💚">💚</a>
</td>
<td title="U+1F49B: YELLOW HEART"><a href="/wiki/%F0%9F%92%9B" class="mw-redirect" title="💛">💛</a>
</td>
<td title="U+1F49C: PURPLE HEART"><a href="/wiki/%F0%9F%92%9C" class="mw-redirect" title="💜">💜</a>
</td>
<td title="U+1F49D: HEART WITH RIBBON"><a href="/wiki/%F0%9F%92%9D" class="mw-redirect" title="💝">💝</a>
</td>
<td title="U+1F49E: REVOLVING HEARTS"><a href="/wiki/%F0%9F%92%9E" class="mw-redirect" title="💞">💞</a>
</td>
<td title="U+1F49F: HEART DECORATION"><a href="/wiki/%F0%9F%92%9F" class="mw-redirect" title="💟">💟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F4Ax
</td>
<td title="U+1F4A0: DIAMOND SHAPE WITH A DOT INSIDE"><a href="/wiki/%F0%9F%92%A0" class="mw-redirect" title="💠">💠</a>
</td>
<td title="U+1F4A1: ELECTRIC LIGHT BULB"><a href="/wiki/%F0%9F%92%A1" class="mw-redirect" title="💡">💡</a>
</td>
<td title="U+1F4A2: ANGER SYMBOL"><a href="/wiki/%F0%9F%92%A2" class="mw-redirect" title="💢">💢</a>
</td>
<td title="U+1F4A3: BOMB"><a href="/wiki/%F0%9F%92%A3" class="mw-redirect" title="💣">💣</a>
</td>
<td title="U+1F4A4: SLEEPING SYMBOL"><a href="/wiki/%F0%9F%92%A4" class="mw-redirect" title="💤">💤</a>
</td>
<td title="U+1F4A5: COLLISION SYMBOL"><a href="/wiki/%F0%9F%92%A5" class="mw-redirect" title="💥">💥</a>
</td>
<td title="U+1F4A6: SPLASHING SWEAT SYMBOL"><a href="/wiki/%F0%9F%92%A6" class="mw-redirect" title="💦">💦</a>
</td>
<td title="U+1F4A7: DROPLET"><a href="/wiki/%F0%9F%92%A7" class="mw-redirect" title="💧">💧</a>
</td>
<td title="U+1F4A8: DASH SYMBOL"><a href="/wiki/%F0%9F%92%A8" class="mw-redirect" title="💨">💨</a>
</td>
<td title="U+1F4A9: PILE OF POO"><a href="/wiki/%F0%9F%92%A9" class="mw-redirect" title="💩">💩</a>
</td>
<td title="U+1F4AA: FLEXED BICEPS"><a href="/wiki/%F0%9F%92%AA" class="mw-redirect" title="💪">💪</a>
</td>
<td title="U+1F4AB: DIZZY SYMBOL"><a href="/wiki/%F0%9F%92%AB" class="mw-redirect" title="💫">💫</a>
</td>
<td title="U+1F4AC: SPEECH BALLOON"><a href="/wiki/%F0%9F%92%AC" class="mw-redirect" title="💬">💬</a>
</td>
<td title="U+1F4AD: THOUGHT BALLOON"><a href="/wiki/%F0%9F%92%AD" class="mw-redirect" title="💭">💭</a>
</td>
<td title="U+1F4AE: WHITE FLOWER"><a href="/wiki/%F0%9F%92%AE" class="mw-redirect" title="💮">💮</a>
</td>
<td title="U+1F4AF: HUNDRED POINTS SYMBOL"><a href="/wiki/%F0%9F%92%AF" class="mw-redirect" title="💯">💯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F4Bx
</td>
<td title="U+1F4B0: MONEY BAG"><a href="/wiki/%F0%9F%92%B0" class="mw-redirect" title="💰">💰</a>
</td>
<td title="U+1F4B1: CURRENCY EXCHANGE"><a href="/wiki/%F0%9F%92%B1" class="mw-redirect" title="💱">💱</a>
</td>
<td title="U+1F4B2: HEAVY DOLLAR SIGN"><a href="/wiki/%F0%9F%92%B2" class="mw-redirect" title="💲">💲</a>
</td>
<td title="U+1F4B3: CREDIT CARD"><a href="/wiki/%F0%9F%92%B3" class="mw-redirect" title="💳">💳</a>
</td>
<td title="U+1F4B4: BANKNOTE WITH YEN SIGN"><a href="/wiki/%F0%9F%92%B4" class="mw-redirect" title="💴">💴</a>
</td>
<td title="U+1F4B5: BANKNOTE WITH DOLLAR SIGN"><a href="/wiki/%F0%9F%92%B5" class="mw-redirect" title="💵">💵</a>
</td>
<td title="U+1F4B6: BANKNOTE WITH EURO SIGN"><a href="/wiki/%F0%9F%92%B6" class="mw-redirect" title="💶">💶</a>
</td>
<td title="U+1F4B7: BANKNOTE WITH POUND SIGN"><a href="/wiki/%F0%9F%92%B7" class="mw-redirect" title="💷">💷</a>
</td>
<td title="U+1F4B8: MONEY WITH WINGS"><a href="/wiki/%F0%9F%92%B8" class="mw-redirect" title="💸">💸</a>
</td>
<td title="U+1F4B9: CHART WITH UPWARDS TREND AND YEN SIGN"><a href="/wiki/%F0%9F%92%B9" class="mw-redirect" title="💹">💹</a>
</td>
<td title="U+1F4BA: SEAT"><a href="/wiki/%F0%9F%92%BA" class="mw-redirect" title="💺">💺</a>
</td>
<td title="U+1F4BB: PERSONAL COMPUTER"><a href="/wiki/%F0%9F%92%BB" class="mw-redirect" title="💻">💻</a>
</td>
<td title="U+1F4BC: BRIEFCASE"><a href="/wiki/%F0%9F%92%BC" class="mw-redirect" title="💼">💼</a>
</td>
<td title="U+1F4BD: MINIDISC"><a href="/wiki/%F0%9F%92%BD" class="mw-redirect" title="💽">💽</a>
</td>
<td title="U+1F4BE: FLOPPY DISK"><a href="/wiki/%F0%9F%92%BE" class="mw-redirect" title="💾">💾</a>
</td>
<td title="U+1F4BF: OPTICAL DISC"><a href="/wiki/%F0%9F%92%BF" class="mw-redirect" title="💿">💿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F4Cx
</td>
<td title="U+1F4C0: DVD"><a href="/wiki/%F0%9F%93%80" class="mw-redirect" title="📀">📀</a>
</td>
<td title="U+1F4C1: FILE FOLDER"><a href="/wiki/%F0%9F%93%81" class="mw-redirect" title="📁">📁</a>
</td>
<td title="U+1F4C2: OPEN FILE FOLDER"><a href="/wiki/%F0%9F%93%82" class="mw-redirect" title="📂">📂</a>
</td>
<td title="U+1F4C3: PAGE WITH CURL"><a href="/wiki/%F0%9F%93%83" class="mw-redirect" title="📃">📃</a>
</td>
<td title="U+1F4C4: PAGE FACING UP"><a href="/wiki/%F0%9F%93%84" class="mw-redirect" title="📄">📄</a>
</td>
<td title="U+1F4C5: CALENDAR"><a href="/wiki/%F0%9F%93%85" class="mw-redirect" title="📅">📅</a>
</td>
<td title="U+1F4C6: TEAR-OFF CALENDAR"><a href="/wiki/%F0%9F%93%86" class="mw-redirect" title="📆">📆</a>
</td>
<td title="U+1F4C7: CARD INDEX"><a href="/wiki/%F0%9F%93%87" class="mw-redirect" title="📇">📇</a>
</td>
<td title="U+1F4C8: CHART WITH UPWARDS TREND"><a href="/wiki/%F0%9F%93%88" class="mw-redirect" title="📈">📈</a>
</td>
<td title="U+1F4C9: CHART WITH DOWNWARDS TREND"><a href="/wiki/%F0%9F%93%89" class="mw-redirect" title="📉">📉</a>
</td>
<td title="U+1F4CA: BAR CHART"><a href="/wiki/%F0%9F%93%8A" class="mw-redirect" title="📊">📊</a>
</td>
<td title="U+1F4CB: CLIPBOARD"><a href="/wiki/%F0%9F%93%8B" class="mw-redirect" title="📋">📋</a>
</td>
<td title="U+1F4CC: PUSHPIN"><a href="/wiki/%F0%9F%93%8C" class="mw-redirect" title="📌">📌</a>
</td>
<td title="U+1F4CD: ROUND PUSHPIN"><a href="/wiki/%F0%9F%93%8D" class="mw-redirect" title="📍">📍</a>
</td>
<td title="U+1F4CE: PAPERCLIP"><a href="/wiki/%F0%9F%93%8E" class="mw-redirect" title="📎">📎</a>
</td>
<td title="U+1F4CF: STRAIGHT RULER"><a href="/wiki/%F0%9F%93%8F" class="mw-redirect" title="📏">📏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F4Dx
</td>
<td title="U+1F4D0: TRIANGULAR RULER"><a href="/wiki/%F0%9F%93%90" class="mw-redirect" title="📐">📐</a>
</td>
<td title="U+1F4D1: BOOKMARK TABS"><a href="/wiki/%F0%9F%93%91" class="mw-redirect" title="📑">📑</a>
</td>
<td title="U+1F4D2: LEDGER"><a href="/wiki/%F0%9F%93%92" class="mw-redirect" title="📒">📒</a>
</td>
<td title="U+1F4D3: NOTEBOOK"><a href="/wiki/%F0%9F%93%93" class="mw-redirect" title="📓">📓</a>
</td>
<td title="U+1F4D4: NOTEBOOK WITH DECORATIVE COVER"><a href="/wiki/%F0%9F%93%94" class="mw-redirect" title="📔">📔</a>
</td>
<td title="U+1F4D5: CLOSED BOOK"><a href="/wiki/%F0%9F%93%95" class="mw-redirect" title="📕">📕</a>
</td>
<td title="U+1F4D6: OPEN BOOK"><a href="/wiki/%F0%9F%93%96" class="mw-redirect" title="📖">📖</a>
</td>
<td title="U+1F4D7: GREEN BOOK"><a href="/wiki/%F0%9F%93%97" class="mw-redirect" title="📗">📗</a>
</td>
<td title="U+1F4D8: BLUE BOOK"><a href="/wiki/%F0%9F%93%98" class="mw-redirect" title="📘">📘</a>
</td>
<td title="U+1F4D9: ORANGE BOOK"><a href="/wiki/%F0%9F%93%99" class="mw-redirect" title="📙">📙</a>
</td>
<td title="U+1F4DA: BOOKS"><a href="/wiki/%F0%9F%93%9A" class="mw-redirect" title="📚">📚</a>
</td>
<td title="U+1F4DB: NAME BADGE"><a href="/wiki/%F0%9F%93%9B" class="mw-redirect" title="📛">📛</a>
</td>
<td title="U+1F4DC: SCROLL"><a href="/wiki/%F0%9F%93%9C" class="mw-redirect" title="📜">📜</a>
</td>
<td title="U+1F4DD: MEMO"><a href="/wiki/%F0%9F%93%9D" class="mw-redirect" title="📝">📝</a>
</td>
<td title="U+1F4DE: TELEPHONE RECEIVER"><a href="/wiki/%F0%9F%93%9E" class="mw-redirect" title="📞">📞</a>
</td>
<td title="U+1F4DF: PAGER"><a href="/wiki/%F0%9F%93%9F" class="mw-redirect" title="📟">📟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F4Ex
</td>
<td title="U+1F4E0: FAX MACHINE"><a href="/wiki/%F0%9F%93%A0" class="mw-redirect" title="📠">📠</a>
</td>
<td title="U+1F4E1: SATELLITE ANTENNA"><a href="/wiki/%F0%9F%93%A1" class="mw-redirect" title="📡">📡</a>
</td>
<td title="U+1F4E2: PUBLIC ADDRESS LOUDSPEAKER"><a href="/wiki/%F0%9F%93%A2" class="mw-redirect" title="📢">📢</a>
</td>
<td title="U+1F4E3: CHEERING MEGAPHONE"><a href="/wiki/%F0%9F%93%A3" class="mw-redirect" title="📣">📣</a>
</td>
<td title="U+1F4E4: OUTBOX TRAY"><a href="/wiki/%F0%9F%93%A4" class="mw-redirect" title="📤">📤</a>
</td>
<td title="U+1F4E5: INBOX TRAY"><a href="/wiki/%F0%9F%93%A5" class="mw-redirect" title="📥">📥</a>
</td>
<td title="U+1F4E6: PACKAGE"><a href="/wiki/%F0%9F%93%A6" class="mw-redirect" title="📦">📦</a>
</td>
<td title="U+1F4E7: E-MAIL SYMBOL"><a href="/wiki/%F0%9F%93%A7" class="mw-redirect" title="📧">📧</a>
</td>
<td title="U+1F4E8: INCOMING ENVELOPE"><a href="/wiki/%F0%9F%93%A8" class="mw-redirect" title="📨">📨</a>
</td>
<td title="U+1F4E9: ENVELOPE WITH DOWNWARDS ARROW ABOVE"><a href="/wiki/%F0%9F%93%A9" class="mw-redirect" title="📩">📩</a>
</td>
<td title="U+1F4EA: CLOSED MAILBOX WITH LOWERED FLAG"><a href="/wiki/%F0%9F%93%AA" class="mw-redirect" title="📪">📪</a>
</td>
<td title="U+1F4EB: CLOSED MAILBOX WITH RAISED FLAG"><a href="/wiki/%F0%9F%93%AB" class="mw-redirect" title="📫">📫</a>
</td>
<td title="U+1F4EC: OPEN MAILBOX WITH RAISED FLAG"><a href="/wiki/%F0%9F%93%AC" class="mw-redirect" title="📬">📬</a>
</td>
<td title="U+1F4ED: OPEN MAILBOX WITH LOWERED FLAG"><a href="/wiki/%F0%9F%93%AD" class="mw-redirect" title="📭">📭</a>
</td>
<td title="U+1F4EE: POSTBOX"><a href="/wiki/%F0%9F%93%AE" class="mw-redirect" title="📮">📮</a>
</td>
<td title="U+1F4EF: POSTAL HORN"><a href="/wiki/%F0%9F%93%AF" class="mw-redirect" title="📯">📯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F4Fx
</td>
<td title="U+1F4F0: NEWSPAPER"><a href="/wiki/%F0%9F%93%B0" class="mw-redirect" title="📰">📰</a>
</td>
<td title="U+1F4F1: MOBILE PHONE"><a href="/wiki/%F0%9F%93%B1" class="mw-redirect" title="📱">📱</a>
</td>
<td title="U+1F4F2: MOBILE PHONE WITH RIGHTWARDS ARROW AT LEFT"><a href="/wiki/%F0%9F%93%B2" class="mw-redirect" title="📲">📲</a>
</td>
<td title="U+1F4F3: VIBRATION MODE"><a href="/wiki/%F0%9F%93%B3" class="mw-redirect" title="📳">📳</a>
</td>
<td title="U+1F4F4: MOBILE PHONE OFF"><a href="/wiki/%F0%9F%93%B4" class="mw-redirect" title="📴">📴</a>
</td>
<td title="U+1F4F5: NO MOBILE PHONES"><a href="/wiki/%F0%9F%93%B5" class="mw-redirect" title="📵">📵</a>
</td>
<td title="U+1F4F6: ANTENNA WITH BARS"><a href="/wiki/%F0%9F%93%B6" class="mw-redirect" title="📶">📶</a>
</td>
<td title="U+1F4F7: CAMERA"><a href="/wiki/%F0%9F%93%B7" class="mw-redirect" title="📷">📷</a>
</td>
<td title="U+1F4F8: CAMERA WITH FLASH"><a href="/wiki/%F0%9F%93%B8" class="mw-redirect" title="📸">📸</a>
</td>
<td title="U+1F4F9: VIDEO CAMERA"><a href="/wiki/%F0%9F%93%B9" class="mw-redirect" title="📹">📹</a>
</td>
<td title="U+1F4FA: TELEVISION"><a href="/wiki/%F0%9F%93%BA" class="mw-redirect" title="📺">📺</a>
</td>
<td title="U+1F4FB: RADIO"><a href="/wiki/%F0%9F%93%BB" class="mw-redirect" title="📻">📻</a>
</td>
<td title="U+1F4FC: VIDEOCASSETTE"><a href="/wiki/%F0%9F%93%BC" class="mw-redirect" title="📼">📼</a>
</td>
<td title="U+1F4FD: FILM PROJECTOR"><a href="/wiki/%F0%9F%93%BD" class="mw-redirect" title="📽">📽️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F4FF: PRAYER BEADS"><a href="/wiki/%F0%9F%93%BF" class="mw-redirect" title="📿">📿</a>
</td></tr>
<tr>
<td colspan="17">
</td></tr>
<tr style="background:#F8F8F8;font-size:small;font-family:sans-serif">
<td style="width:45pt">&nbsp;</td>
<td style="width:20pt">0</td>
<td style="width:20pt">1</td>
<td style="width:20pt">2</td>
<td style="width:20pt">3</td>
<td style="width:20pt">4</td>
<td style="width:20pt">5</td>
<td style="width:20pt">6</td>
<td style="width:20pt">7</td>
<td style="width:20pt">8</td>
<td style="width:20pt">9</td>
<td style="width:20pt">A</td>
<td style="width:20pt">B</td>
<td style="width:20pt">C</td>
<td style="width:20pt">D</td>
<td style="width:20pt">E</td>
<td style="width:20pt">F
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F50x
</td>
<td title="U+1F500: TWISTED RIGHTWARDS ARROWS"><a href="/wiki/%F0%9F%94%80" class="mw-redirect" title="🔀">🔀</a>
</td>
<td title="U+1F501: CLOCKWISE RIGHTWARDS AND LEFTWARDS OPEN CIRCLE ARROWS"><a href="/wiki/%F0%9F%94%81" class="mw-redirect" title="🔁">🔁</a>
</td>
<td title="U+1F502: CLOCKWISE RIGHTWARDS AND LEFTWARDS OPEN CIRCLE ARROWS WITH CIRCLED ONE OVERLAY"><a href="/wiki/%F0%9F%94%82" class="mw-redirect" title="🔂">🔂</a>
</td>
<td title="U+1F503: CLOCKWISE DOWNWARDS AND UPWARDS OPEN CIRCLE ARROWS"><a href="/wiki/%F0%9F%94%83" class="mw-redirect" title="🔃">🔃</a>
</td>
<td title="U+1F504: ANTICLOCKWISE DOWNWARDS AND UPWARDS OPEN CIRCLE ARROWS"><a href="/wiki/%F0%9F%94%84" class="mw-redirect" title="🔄">🔄</a>
</td>
<td title="U+1F505: LOW BRIGHTNESS SYMBOL"><a href="/wiki/%F0%9F%94%85" class="mw-redirect" title="🔅">🔅</a>
</td>
<td title="U+1F506: HIGH BRIGHTNESS SYMBOL"><a href="/wiki/%F0%9F%94%86" class="mw-redirect" title="🔆">🔆</a>
</td>
<td title="U+1F507: SPEAKER WITH CANCELLATION STROKE"><a href="/wiki/Mute_(disambiguation)" class="mw-redirect mw-disambig" title="Mute (disambiguation)">🔇</a>
</td>
<td title="U+1F508: SPEAKER"><a href="/wiki/%F0%9F%94%88" class="mw-redirect" title="🔈">🔈</a>
</td>
<td title="U+1F509: SPEAKER WITH ONE SOUND WAVE"><a href="/wiki/%F0%9F%94%89" class="mw-redirect" title="🔉">🔉</a>
</td>
<td title="U+1F50A: SPEAKER WITH THREE SOUND WAVES"><a href="/wiki/%F0%9F%94%8A" class="mw-redirect" title="🔊">🔊</a>
</td>
<td title="U+1F50B: BATTERY"><a href="/wiki/%F0%9F%94%8B" class="mw-redirect" title="🔋">🔋</a>
</td>
<td title="U+1F50C: ELECTRIC PLUG"><a href="/wiki/%F0%9F%94%8C" class="mw-redirect" title="🔌">🔌</a>
</td>
<td title="U+1F50D: LEFT-POINTING MAGNIFYING GLASS"><a href="/wiki/%F0%9F%94%8D" class="mw-redirect" title="🔍">🔍</a>
</td>
<td title="U+1F50E: RIGHT-POINTING MAGNIFYING GLASS"><a href="/wiki/%F0%9F%94%8E" class="mw-redirect" title="🔎">🔎</a>
</td>
<td title="U+1F50F: LOCK WITH INK PEN"><a href="/wiki/%F0%9F%94%8F" class="mw-redirect" title="🔏">🔏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F51x
</td>
<td title="U+1F510: CLOSED LOCK WITH KEY"><a href="/wiki/%F0%9F%94%90" class="mw-redirect" title="🔐">🔐</a>
</td>
<td title="U+1F511: KEY"><a href="/wiki/%F0%9F%94%91" class="mw-redirect" title="🔑">🔑</a>
</td>
<td title="U+1F512: LOCK"><a href="/wiki/%F0%9F%94%92" class="mw-redirect" title="🔒">🔒</a>
</td>
<td title="U+1F513: OPEN LOCK"><a href="/wiki/%F0%9F%94%93" class="mw-redirect" title="🔓">🔓</a>
</td>
<td title="U+1F514: BELL"><a href="/wiki/Bell_character" title="Bell character"> 🔔</a>
</td>
<td title="U+1F515: BELL WITH CANCELLATION STROKE"><a href="/wiki/%F0%9F%94%95" class="mw-redirect" title="🔕">🔕</a>
</td>
<td title="U+1F516: BOOKMARK"><a href="/wiki/%F0%9F%94%96" class="mw-redirect" title="🔖">🔖</a>
</td>
<td title="U+1F517: LINK SYMBOL"><a href="/wiki/%F0%9F%94%97" class="mw-redirect" title="🔗">🔗</a>
</td>
<td title="U+1F518: RADIO BUTTON"><a href="/wiki/%F0%9F%94%98" class="mw-redirect" title="🔘">🔘</a>
</td>
<td title="U+1F519: BACK WITH LEFTWARDS ARROW ABOVE"><a href="/wiki/%F0%9F%94%99" class="mw-redirect" title="🔙">🔙</a>
</td>
<td title="U+1F51A: END WITH LEFTWARDS ARROW ABOVE"><a href="/wiki/%F0%9F%94%9A" class="mw-redirect" title="🔚">🔚</a>
</td>
<td title="U+1F51B: ON WITH EXCLAMATION MARK WITH LEFT RIGHT ARROW ABOVE"><a href="/wiki/%F0%9F%94%9B" class="mw-redirect" title="🔛">🔛</a>
</td>
<td title="U+1F51C: SOON WITH RIGHTWARDS ARROW ABOVE"><a href="/wiki/%F0%9F%94%9C" class="mw-redirect" title="🔜">🔜</a>
</td>
<td title="U+1F51D: TOP WITH UPWARDS ARROW ABOVE"><a href="/wiki/%F0%9F%94%9D" class="mw-redirect" title="🔝">🔝</a>
</td>
<td title="U+1F51E: NO ONE UNDER EIGHTEEN SYMBOL"><a href="/wiki/Age_of_majority#Age_18" title="Age of majority">🔞</a>
</td>
<td title="U+1F51F: KEYCAP TEN"><a href="/wiki/%F0%9F%94%9F" class="mw-redirect" title="🔟">🔟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F52x
</td>
<td title="U+1F520: INPUT SYMBOL FOR LATIN CAPITAL LETTERS"><a href="/wiki/%F0%9F%94%A0" class="mw-redirect" title="🔠">🔠</a>
</td>
<td title="U+1F521: INPUT SYMBOL FOR LATIN SMALL LETTERS"><a href="/wiki/%F0%9F%94%A1" class="mw-redirect" title="🔡">🔡</a>
</td>
<td title="U+1F522: INPUT SYMBOL FOR NUMBERS"><a href="/wiki/%F0%9F%94%A2" class="mw-redirect" title="🔢">🔢</a>
</td>
<td title="U+1F523: INPUT SYMBOL FOR SYMBOLS"><a href="/wiki/%F0%9F%94%A3" class="mw-redirect" title="🔣">🔣</a>
</td>
<td title="U+1F524: INPUT SYMBOL FOR LATIN LETTERS"><a href="/wiki/%F0%9F%94%A4" class="mw-redirect" title="🔤">🔤</a>
</td>
<td title="U+1F525: FIRE"><a href="/wiki/%F0%9F%94%A5" class="mw-redirect" title="🔥">🔥</a>
</td>
<td title="U+1F526: ELECTRIC TORCH"><a href="/wiki/%F0%9F%94%A6" class="mw-redirect" title="🔦">🔦</a>
</td>
<td title="U+1F527: WRENCH"><a href="/wiki/%F0%9F%94%A7" class="mw-redirect" title="🔧">🔧</a>
</td>
<td title="U+1F528: HAMMER"><a href="/wiki/%F0%9F%94%A8" class="mw-redirect" title="🔨">🔨</a>
</td>
<td title="U+1F529: NUT AND BOLT"><a href="/wiki/%F0%9F%94%A9" class="mw-redirect" title="🔩">🔩</a>
</td>
<td title="U+1F52A: HOCHO"><a href="/wiki/%F0%9F%94%AA" class="mw-redirect" title="🔪">🔪</a>
</td>
<td title="U+1F52B: PISTOL"><a href="/wiki/%F0%9F%94%AB" class="mw-redirect" title="🔫">🔫</a>
</td>
<td title="U+1F52C: MICROSCOPE"><a href="/wiki/%F0%9F%94%AC" class="mw-redirect" title="🔬">🔬</a>
</td>
<td title="U+1F52D: TELESCOPE"><a href="/wiki/%F0%9F%94%AD" class="mw-redirect" title="🔭">🔭</a>
</td>
<td title="U+1F52E: CRYSTAL BALL"><a href="/wiki/%F0%9F%94%AE" class="mw-redirect" title="🔮">🔮</a>
</td>
<td title="U+1F52F: SIX POINTED STAR WITH MIDDLE DOT"><a href="/wiki/%F0%9F%94%AF" class="mw-redirect" title="🔯">🔯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F53x
</td>
<td title="U+1F530: JAPANESE SYMBOL FOR BEGINNER"><a href="/wiki/%F0%9F%94%B0" class="mw-redirect" title="🔰">🔰</a>
</td>
<td title="U+1F531: TRIDENT EMBLEM"><a href="/wiki/%F0%9F%94%B1" class="mw-redirect" title="🔱">🔱</a>
</td>
<td title="U+1F532: BLACK SQUARE BUTTON"><a href="/wiki/%F0%9F%94%B2" class="mw-redirect" title="🔲">🔲</a>
</td>
<td title="U+1F533: WHITE SQUARE BUTTON"><a href="/wiki/%F0%9F%94%B3" class="mw-redirect" title="🔳">🔳</a>
</td>
<td title="U+1F534: LARGE RED CIRCLE"><a href="/wiki/Red_Circle_(disambiguation)" class="mw-redirect mw-disambig" title="Red Circle (disambiguation)">🔴</a>
</td>
<td title="U+1F535: LARGE BLUE CIRCLE"><a href="/wiki/%F0%9F%94%B5" class="mw-redirect" title="🔵">🔵</a>
</td>
<td title="U+1F536: LARGE ORANGE DIAMOND"><a href="/wiki/%F0%9F%94%B6" class="mw-redirect" title="🔶">🔶</a>
</td>
<td title="U+1F537: LARGE BLUE DIAMOND"><a href="/wiki/%F0%9F%94%B7" class="mw-redirect" title="🔷">🔷</a>
</td>
<td title="U+1F538: SMALL ORANGE DIAMOND"><a href="/wiki/%F0%9F%94%B8" class="mw-redirect" title="🔸">🔸</a>
</td>
<td title="U+1F539: SMALL BLUE DIAMOND"><a href="/wiki/%F0%9F%94%B9" class="mw-redirect" title="🔹">🔹</a>
</td>
<td title="U+1F53A: UP-POINTING RED TRIANGLE"><a href="/wiki/%F0%9F%94%BA" class="mw-redirect" title="🔺">🔺</a>
</td>
<td title="U+1F53B: DOWN-POINTING RED TRIANGLE"><a href="/wiki/%F0%9F%94%BB" class="mw-redirect" title="🔻">🔻</a>
</td>
<td title="U+1F53C: UP-POINTING SMALL RED TRIANGLE"><a href="/wiki/%F0%9F%94%BC" class="mw-redirect" title="🔼">🔼</a>
</td>
<td title="U+1F53D: DOWN-POINTING SMALL RED TRIANGLE"><a href="/wiki/%F0%9F%94%BD" class="mw-redirect" title="🔽">🔽</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F54x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F549: OM SYMBOL"><a href="/wiki/%F0%9F%95%89" class="mw-redirect" title="🕉">🕉️</a>
</td>
<td title="U+1F54A: DOVE OF PEACE"><a href="/wiki/%F0%9F%95%8A" class="mw-redirect" title="🕊">🕊️</a>
</td>
<td title="U+1F54B: KAABA"><a href="/wiki/%F0%9F%95%8B" class="mw-redirect" title="🕋">🕋</a>
</td>
<td title="U+1F54C: MOSQUE"><a href="/wiki/%F0%9F%95%8C" class="mw-redirect" title="🕌">🕌</a>
</td>
<td title="U+1F54D: SYNAGOGUE"><a href="/wiki/%F0%9F%95%8D" class="mw-redirect" title="🕍">🕍</a>
</td>
<td title="U+1F54E: MENORAH WITH NINE BRANCHES"><a href="/wiki/%F0%9F%95%8E" class="mw-redirect" title="🕎">🕎</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F55x
</td>
<td title="U+1F550: CLOCK FACE ONE OCLOCK"><a href="/wiki/%F0%9F%95%90" class="mw-redirect" title="🕐">🕐</a>
</td>
<td title="U+1F551: CLOCK FACE TWO OCLOCK"><a href="/wiki/%F0%9F%95%91" class="mw-redirect" title="🕑">🕑</a>
</td>
<td title="U+1F552: CLOCK FACE THREE OCLOCK"><a href="/wiki/%F0%9F%95%92" class="mw-redirect" title="🕒">🕒</a>
</td>
<td title="U+1F553: CLOCK FACE FOUR OCLOCK"><a href="/wiki/%F0%9F%95%93" class="mw-redirect" title="🕓">🕓</a>
</td>
<td title="U+1F554: CLOCK FACE FIVE OCLOCK"><a href="/wiki/%F0%9F%95%94" class="mw-redirect" title="🕔">🕔</a>
</td>
<td title="U+1F555: CLOCK FACE SIX OCLOCK"><a href="/wiki/%F0%9F%95%95" class="mw-redirect" title="🕕">🕕</a>
</td>
<td title="U+1F556: CLOCK FACE SEVEN OCLOCK"><a href="/wiki/%F0%9F%95%96" class="mw-redirect" title="🕖">🕖</a>
</td>
<td title="U+1F557: CLOCK FACE EIGHT OCLOCK"><a href="/wiki/%F0%9F%95%97" class="mw-redirect" title="🕗">🕗</a>
</td>
<td title="U+1F558: CLOCK FACE NINE OCLOCK"><a href="/wiki/%F0%9F%95%98" class="mw-redirect" title="🕘">🕘</a>
</td>
<td title="U+1F559: CLOCK FACE TEN OCLOCK"><a href="/wiki/%F0%9F%95%99" class="mw-redirect" title="🕙">🕙</a>
</td>
<td title="U+1F55A: CLOCK FACE ELEVEN OCLOCK"><a href="/wiki/%F0%9F%95%9A" class="mw-redirect" title="🕚">🕚</a>
</td>
<td title="U+1F55B: CLOCK FACE TWELVE OCLOCK"><a href="/wiki/%F0%9F%95%9B" class="mw-redirect" title="🕛">🕛</a>
</td>
<td title="U+1F55C: CLOCK FACE ONE-THIRTY"><a href="/wiki/%F0%9F%95%9C" class="mw-redirect" title="🕜">🕜</a>
</td>
<td title="U+1F55D: CLOCK FACE TWO-THIRTY"><a href="/wiki/%F0%9F%95%9D" class="mw-redirect" title="🕝">🕝</a>
</td>
<td title="U+1F55E: CLOCK FACE THREE-THIRTY"><a href="/wiki/%F0%9F%95%9E" class="mw-redirect" title="🕞">🕞</a>
</td>
<td title="U+1F55F: CLOCK FACE FOUR-THIRTY"><a href="/wiki/%F0%9F%95%9F" class="mw-redirect" title="🕟">🕟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F56x
</td>
<td title="U+1F560: CLOCK FACE FIVE-THIRTY"><a href="/wiki/%F0%9F%95%A0" class="mw-redirect" title="🕠">🕠</a>
</td>
<td title="U+1F561: CLOCK FACE SIX-THIRTY"><a href="/wiki/%F0%9F%95%A1" class="mw-redirect" title="🕡">🕡</a>
</td>
<td title="U+1F562: CLOCK FACE SEVEN-THIRTY"><a href="/wiki/%F0%9F%95%A2" class="mw-redirect" title="🕢">🕢</a>
</td>
<td title="U+1F563: CLOCK FACE EIGHT-THIRTY"><a href="/wiki/%F0%9F%95%A3" class="mw-redirect" title="🕣">🕣</a>
</td>
<td title="U+1F564: CLOCK FACE NINE-THIRTY"><a href="/wiki/%F0%9F%95%A4" class="mw-redirect" title="🕤">🕤</a>
</td>
<td title="U+1F565: CLOCK FACE TEN-THIRTY"><a href="/wiki/%F0%9F%95%A5" class="mw-redirect" title="🕥">🕥</a>
</td>
<td title="U+1F566: CLOCK FACE ELEVEN-THIRTY"><a href="/wiki/%F0%9F%95%A6" class="mw-redirect" title="🕦">🕦</a>
</td>
<td title="U+1F567: CLOCK FACE TWELVE-THIRTY"><a href="/wiki/%F0%9F%95%A7" class="mw-redirect" title="🕧">🕧</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F56F: CANDLE"><a href="/wiki/%F0%9F%95%AF" class="mw-redirect" title="🕯">🕯️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F57x
</td>
<td title="U+1F570: MANTELPIECE CLOCK"><a href="/wiki/%F0%9F%95%B0" class="mw-redirect" title="🕰">🕰️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F573: HOLE"><a href="/wiki/Hole_(disambiguation)" class="mw-disambig" title="Hole (disambiguation)">🕳️</a>
</td>
<td title="U+1F574: MAN IN BUSINESS SUIT LEVITATING"><a href="/wiki/%F0%9F%95%B4" class="mw-redirect" title="🕴">🕴️</a>
</td>
<td title="U+1F575: SLEUTH OR SPY"><a href="/wiki/%F0%9F%95%B5" class="mw-redirect" title="🕵">🕵️</a>
</td>
<td title="U+1F576: DARK SUNGLASSES"><a href="/wiki/%F0%9F%95%B6" class="mw-redirect" title="🕶">🕶️</a>
</td>
<td title="U+1F577: SPIDER"><a href="/wiki/%F0%9F%95%B7" class="mw-redirect" title="🕷">🕷️</a>
</td>
<td title="U+1F578: SPIDER WEB"><a href="/wiki/%F0%9F%95%B8" class="mw-redirect" title="🕸">🕸️</a>
</td>
<td title="U+1F579: JOYSTICK"><a href="/wiki/%F0%9F%95%B9" class="mw-redirect" title="🕹">🕹️</a>
</td>
<td title="U+1F57A: MAN DANCING"><a href="/wiki/%F0%9F%95%BA" class="mw-redirect" title="🕺">🕺</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F58x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F587: LINKED PAPERCLIPS"><a href="/wiki/%F0%9F%96%87" class="mw-redirect" title="🖇">🖇️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F58A: LOWER LEFT BALLPOINT PEN"><a href="/wiki/%F0%9F%96%8A" class="mw-redirect" title="🖊">🖊️</a>
</td>
<td title="U+1F58B: LOWER LEFT FOUNTAIN PEN"><a href="/wiki/%F0%9F%96%8B" class="mw-redirect" title="🖋">🖋️</a>
</td>
<td title="U+1F58C: LOWER LEFT PAINTBRUSH"><a href="/wiki/%F0%9F%96%8C" class="mw-redirect" title="🖌">🖌️</a>
</td>
<td title="U+1F58D: LOWER LEFT CRAYON"><a href="/wiki/%F0%9F%96%8D" class="mw-redirect" title="🖍">🖍️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F59x
</td>
<td title="U+1F590: RAISED HAND WITH FINGERS SPLAYED"><a href="/wiki/%F0%9F%96%90" class="mw-redirect" title="🖐">🖐️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F595: REVERSED HAND WITH MIDDLE FINGER EXTENDED"><a href="/wiki/%F0%9F%96%95" class="mw-redirect" title="🖕">🖕</a>
</td>
<td title="U+1F596: RAISED HAND WITH PART BETWEEN MIDDLE AND RING FINGERS"><a href="/wiki/%F0%9F%96%96" class="mw-redirect" title="🖖">🖖</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F5Ax
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5A4: BLACK HEART"><a href="/wiki/%F0%9F%96%A4" class="mw-redirect" title="🖤">🖤</a>
</td>
<td title="U+1F5A5: DESKTOP COMPUTER"><a href="/wiki/%F0%9F%96%A5" class="mw-redirect" title="🖥">🖥️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5A8: PRINTER"><a href="/wiki/%F0%9F%96%A8" class="mw-redirect" title="🖨">🖨️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F5Bx
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5B1: THREE BUTTON MOUSE"><a href="/wiki/%F0%9F%96%B1" class="mw-redirect" title="🖱">🖱️</a>
</td>
<td title="U+1F5B2: TRACKBALL"><a href="/wiki/%F0%9F%96%B2" class="mw-redirect" title="🖲">🖲️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5BC: FRAME WITH PICTURE"><a href="/wiki/%F0%9F%96%BC" class="mw-redirect" title="🖼">🖼️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F5Cx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5C2: CARD INDEX DIVIDERS"><a href="/wiki/%F0%9F%97%82" class="mw-redirect" title="🗂">🗂️</a>
</td>
<td title="U+1F5C3: CARD FILE BOX"><a href="/wiki/%F0%9F%97%83" class="mw-redirect" title="🗃">🗃️</a>
</td>
<td title="U+1F5C4: FILE CABINET"><a href="/wiki/%F0%9F%97%84" class="mw-redirect" title="🗄">🗄️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F5Dx
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5D1: WASTEBASKET"><a href="/wiki/%F0%9F%97%91" class="mw-redirect" title="🗑">🗑️</a>
</td>
<td title="U+1F5D2: SPIRAL NOTE PAD"><a href="/wiki/%F0%9F%97%92" class="mw-redirect" title="🗒">🗒️</a>
</td>
<td title="U+1F5D3: SPIRAL CALENDAR PAD"><a href="/wiki/%F0%9F%97%93" class="mw-redirect" title="🗓">🗓️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5DC: COMPRESSION"><a href="/wiki/%F0%9F%97%9C" class="mw-redirect" title="🗜">🗜️</a>
</td>
<td title="U+1F5DD: OLD KEY"><a href="/wiki/%F0%9F%97%9D" class="mw-redirect" title="🗝">🗝️</a>
</td>
<td title="U+1F5DE: ROLLED-UP NEWSPAPER"><a href="/wiki/%F0%9F%97%9E" class="mw-redirect" title="🗞">🗞️</a>
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F5Ex
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5E1: DAGGER KNIFE"><a href="/wiki/%F0%9F%97%A1" class="mw-redirect" title="🗡">🗡️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5E3: SPEAKING HEAD IN SILHOUETTE"><a href="/wiki/%F0%9F%97%A3" class="mw-redirect" title="🗣">🗣️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5E8: LEFT SPEECH BUBBLE"><a href="/wiki/%F0%9F%97%A8" class="mw-redirect" title="🗨">🗨️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5EF: RIGHT ANGER BUBBLE"><a href="/wiki/%F0%9F%97%AF" class="mw-redirect" title="🗯">🗯️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F5Fx
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5F3: BALLOT BOX WITH BALLOT"><a href="/wiki/%F0%9F%97%B3" class="mw-redirect" title="🗳">🗳️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F5FA: WORLD MAP"><a href="/wiki/%F0%9F%97%BA" class="mw-redirect" title="🗺">🗺️</a>
</td>
<td title="U+1F5FB: MOUNT FUJI"><a href="/wiki/%F0%9F%97%BB" class="mw-redirect" title="🗻">🗻</a>
</td>
<td title="U+1F5FC: TOKYO TOWER"><a href="/wiki/%F0%9F%97%BC" class="mw-redirect" title="🗼">🗼</a>
</td>
<td title="U+1F5FD: STATUE OF LIBERTY"><a href="/wiki/%F0%9F%97%BD" class="mw-redirect" title="🗽">🗽</a>
</td>
<td title="U+1F5FE: SILHOUETTE OF JAPAN"><a href="/wiki/%F0%9F%97%BE" class="mw-redirect" title="🗾">🗾</a>
</td>
<td title="U+1F5FF: MOYAI"><a href="/wiki/%F0%9F%97%BF" class="mw-redirect" title="🗿">🗿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F60x
</td>
<td title="U+1F600: GRINNING FACE"><a href="/wiki/%F0%9F%98%80" class="mw-redirect" title="😀">😀</a>
</td>
<td title="U+1F601: GRINNING FACE WITH SMILING EYES"><a href="/wiki/%F0%9F%98%81" class="mw-redirect" title="😁">😁</a>
</td>
<td title="U+1F602: FACE WITH TEARS OF JOY"><a href="/wiki/%F0%9F%98%82" class="mw-redirect" title="😂">😂</a>
</td>
<td title="U+1F603: SMILING FACE WITH OPEN MOUTH"><a href="/wiki/%F0%9F%98%83" class="mw-redirect" title="😃">😃</a>
</td>
<td title="U+1F604: SMILING FACE WITH OPEN MOUTH AND SMILING EYES"><a href="/wiki/%F0%9F%98%84" class="mw-redirect" title="😄">😄</a>
</td>
<td title="U+1F605: SMILING FACE WITH OPEN MOUTH AND COLD SWEAT"><a href="/wiki/%F0%9F%98%85" class="mw-redirect" title="😅">😅</a>
</td>
<td title="U+1F606: SMILING FACE WITH OPEN MOUTH AND TIGHTLY-CLOSED EYES"><a href="/wiki/%F0%9F%98%86" class="mw-redirect" title="😆">😆</a>
</td>
<td title="U+1F607: SMILING FACE WITH HALO"><a href="/wiki/%F0%9F%98%87" class="mw-redirect" title="😇">😇</a>
</td>
<td title="U+1F608: SMILING FACE WITH HORNS"><a href="/wiki/%F0%9F%98%88" class="mw-redirect" title="😈">😈</a>
</td>
<td title="U+1F609: WINKING FACE"><a href="/wiki/%F0%9F%98%89" class="mw-redirect" title="😉">😉</a>
</td>
<td title="U+1F60A: SMILING FACE WITH SMILING EYES"><a href="/wiki/%F0%9F%98%8A" class="mw-redirect" title="😊">😊</a>
</td>
<td title="U+1F60B: FACE SAVOURING DELICIOUS FOOD"><a href="/wiki/%F0%9F%98%8B" class="mw-redirect" title="😋">😋</a>
</td>
<td title="U+1F60C: RELIEVED FACE"><a href="/wiki/%F0%9F%98%8C" class="mw-redirect" title="😌">😌</a>
</td>
<td title="U+1F60D: SMILING FACE WITH HEART-SHAPED EYES"><a href="/wiki/%F0%9F%98%8D" class="mw-redirect" title="😍">😍</a>
</td>
<td title="U+1F60E: SMILING FACE WITH SUNGLASSES"><a href="/wiki/%F0%9F%98%8E" class="mw-redirect" title="😎">😎</a>
</td>
<td title="U+1F60F: SMIRKING FACE"><a href="/wiki/%F0%9F%98%8F" class="mw-redirect" title="😏">😏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F61x
</td>
<td title="U+1F610: NEUTRAL FACE"><a href="/wiki/%F0%9F%98%90" class="mw-redirect" title="😐">😐</a>
</td>
<td title="U+1F611: EXPRESSIONLESS FACE"><a href="/wiki/%F0%9F%98%91" class="mw-redirect" title="😑">😑</a>
</td>
<td title="U+1F612: UNAMUSED FACE"><a href="/wiki/%F0%9F%98%92" class="mw-redirect" title="😒">😒</a>
</td>
<td title="U+1F613: FACE WITH COLD SWEAT"><a href="/wiki/%F0%9F%98%93" class="mw-redirect" title="😓">😓</a>
</td>
<td title="U+1F614: PENSIVE FACE"><a href="/wiki/%F0%9F%98%94" class="mw-redirect" title="😔">😔</a>
</td>
<td title="U+1F615: CONFUSED FACE"><a href="/wiki/%F0%9F%98%95" title="😕">😕</a>
</td>
<td title="U+1F616: CONFOUNDED FACE"><a href="/wiki/%F0%9F%98%96" class="mw-redirect" title="😖">😖</a>
</td>
<td title="U+1F617: KISSING FACE"><a href="/wiki/%F0%9F%98%97" class="mw-redirect" title="😗">😗</a>
</td>
<td title="U+1F618: FACE THROWING A KISS"><a href="/wiki/%F0%9F%98%98" class="mw-redirect" title="😘">😘</a>
</td>
<td title="U+1F619: KISSING FACE WITH SMILING EYES"><a href="/wiki/%F0%9F%98%99" class="mw-redirect" title="😙">😙</a>
</td>
<td title="U+1F61A: KISSING FACE WITH CLOSED EYES"><a href="/wiki/%F0%9F%98%9A" class="mw-redirect" title="😚">😚</a>
</td>
<td title="U+1F61B: FACE WITH STUCK-OUT TONGUE"><a href="/wiki/%F0%9F%98%9B" class="mw-redirect" title="😛">😛</a>
</td>
<td title="U+1F61C: FACE WITH STUCK-OUT TONGUE AND WINKING EYE"><a href="/wiki/%F0%9F%98%9C" class="mw-redirect" title="😜">😜</a>
</td>
<td title="U+1F61D: FACE WITH STUCK-OUT TONGUE AND TIGHTLY-CLOSED EYES"><a href="/wiki/%F0%9F%98%9D" class="mw-redirect" title="😝">😝</a>
</td>
<td title="U+1F61E: DISAPPOINTED FACE"><a href="/wiki/%F0%9F%98%9E" class="mw-redirect" title="😞">😞</a>
</td>
<td title="U+1F61F: WORRIED FACE"><a href="/wiki/%F0%9F%98%9F" class="mw-redirect" title="😟">😟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F62x
</td>
<td title="U+1F620: ANGRY FACE"><a href="/wiki/%F0%9F%98%A0" class="mw-redirect" title="😠">😠</a>
</td>
<td title="U+1F621: POUTING FACE"><a href="/wiki/%F0%9F%98%A1" class="mw-redirect" title="😡">😡</a>
</td>
<td title="U+1F622: CRYING FACE"><a href="/wiki/%F0%9F%98%A2" class="mw-redirect" title="😢">😢</a>
</td>
<td title="U+1F623: PERSEVERING FACE"><a href="/wiki/%F0%9F%98%A3" class="mw-redirect" title="😣">😣</a>
</td>
<td title="U+1F624: FACE WITH LOOK OF TRIUMPH"><a href="/wiki/%F0%9F%98%A4" class="mw-redirect" title="😤">😤</a>
</td>
<td title="U+1F625: DISAPPOINTED BUT RELIEVED FACE"><a href="/wiki/%F0%9F%98%A5" class="mw-redirect" title="😥">😥</a>
</td>
<td title="U+1F626: FROWNING FACE WITH OPEN MOUTH"><a href="/wiki/%F0%9F%98%A6" class="mw-redirect" title="😦">😦</a>
</td>
<td title="U+1F627: ANGUISHED FACE"><a href="/wiki/%F0%9F%98%A7" class="mw-redirect" title="😧">😧</a>
</td>
<td title="U+1F628: FEARFUL FACE"><a href="/wiki/%F0%9F%98%A8" class="mw-redirect" title="😨">😨</a>
</td>
<td title="U+1F629: WEARY FACE"><a href="/wiki/%F0%9F%98%A9" class="mw-redirect" title="😩">😩</a>
</td>
<td title="U+1F62A: SLEEPY FACE"><a href="/wiki/%F0%9F%98%AA" class="mw-redirect" title="😪">😪</a>
</td>
<td title="U+1F62B: TIRED FACE"><a href="/wiki/%F0%9F%98%AB" class="mw-redirect" title="😫">😫</a>
</td>
<td title="U+1F62C: GRIMACING FACE"><a href="/wiki/%F0%9F%98%AC" class="mw-redirect" title="😬">😬</a>
</td>
<td title="U+1F62D: LOUDLY CRYING FACE"><a href="/wiki/%F0%9F%98%AD" class="mw-redirect" title="😭">😭</a>
</td>
<td title="U+1F62E: FACE WITH OPEN MOUTH"><a href="/wiki/%F0%9F%98%AE" class="mw-redirect" title="😮">😮</a>
</td>
<td title="U+1F62F: HUSHED FACE"><a href="/wiki/%F0%9F%98%AF" class="mw-redirect" title="😯">😯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F63x
</td>
<td title="U+1F630: FACE WITH OPEN MOUTH AND COLD SWEAT"><a href="/wiki/%F0%9F%98%B0" class="mw-redirect" title="😰">😰</a>
</td>
<td title="U+1F631: FACE SCREAMING IN FEAR"><a href="/wiki/%F0%9F%98%B1" class="mw-redirect" title="😱">😱</a>
</td>
<td title="U+1F632: ASTONISHED FACE"><a href="/wiki/%F0%9F%98%B2" class="mw-redirect" title="😲">😲</a>
</td>
<td title="U+1F633: FLUSHED FACE"><a href="/wiki/%F0%9F%98%B3" class="mw-redirect" title="😳">😳</a>
</td>
<td title="U+1F634: SLEEPING FACE"><a href="/wiki/%F0%9F%98%B4" class="mw-redirect" title="😴">😴</a>
</td>
<td title="U+1F635: DIZZY FACE"><a href="/wiki/%F0%9F%98%B5" class="mw-redirect" title="😵">😵</a>
</td>
<td title="U+1F636: FACE WITHOUT MOUTH"><a href="/wiki/%F0%9F%98%B6" class="mw-redirect" title="😶">😶</a>
</td>
<td title="U+1F637: FACE WITH MEDICAL MASK"><a href="/wiki/%F0%9F%98%B7" class="mw-redirect" title="😷">😷</a>
</td>
<td title="U+1F638: GRINNING CAT FACE WITH SMILING EYES"><a href="/wiki/%F0%9F%98%B8" class="mw-redirect" title="😸">😸</a>
</td>
<td title="U+1F639: CAT FACE WITH TEARS OF JOY"><a href="/wiki/%F0%9F%98%B9" class="mw-redirect" title="😹">😹</a>
</td>
<td title="U+1F63A: SMILING CAT FACE WITH OPEN MOUTH"><a href="/wiki/%F0%9F%98%BA" class="mw-redirect" title="😺">😺</a>
</td>
<td title="U+1F63B: SMILING CAT FACE WITH HEART-SHAPED EYES"><a href="/wiki/%F0%9F%98%BB" class="mw-redirect" title="😻">😻</a>
</td>
<td title="U+1F63C: CAT FACE WITH WRY SMILE"><a href="/wiki/%F0%9F%98%BC" class="mw-redirect" title="😼">😼</a>
</td>
<td title="U+1F63D: KISSING CAT FACE WITH CLOSED EYES"><a href="/wiki/%F0%9F%98%BD" class="mw-redirect" title="😽">😽</a>
</td>
<td title="U+1F63E: POUTING CAT FACE"><a href="/wiki/%F0%9F%98%BE" class="mw-redirect" title="😾">😾</a>
</td>
<td title="U+1F63F: CRYING CAT FACE"><a href="/wiki/%F0%9F%98%BF" class="mw-redirect" title="😿">😿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F64x
</td>
<td title="U+1F640: WEARY CAT FACE"><a href="/wiki/%F0%9F%99%80" class="mw-redirect" title="🙀">🙀</a>
</td>
<td title="U+1F641: SLIGHTLY FROWNING FACE"><a href="/wiki/%F0%9F%99%81" class="mw-redirect" title="🙁">🙁</a>
</td>
<td title="U+1F642: SLIGHTLY SMILING FACE"><a href="/wiki/%F0%9F%99%82" class="mw-redirect" title="🙂">🙂</a>
</td>
<td title="U+1F643: UPSIDE-DOWN FACE"><a href="/wiki/%F0%9F%99%83" class="mw-redirect" title="🙃">🙃</a>
</td>
<td title="U+1F644: FACE WITH ROLLING EYES"><a href="/wiki/%F0%9F%99%84" class="mw-redirect" title="🙄">🙄</a>
</td>
<td title="U+1F645: FACE WITH NO GOOD GESTURE"><a href="/wiki/%F0%9F%99%85" class="mw-redirect" title="🙅">🙅</a>
</td>
<td title="U+1F646: FACE WITH OK GESTURE"><a href="/wiki/%F0%9F%99%86" class="mw-redirect" title="🙆">🙆</a>
</td>
<td title="U+1F647: PERSON BOWING DEEPLY"><a href="/wiki/%F0%9F%99%87" class="mw-redirect" title="🙇">🙇</a>
</td>
<td title="U+1F648: SEE-NO-EVIL MONKEY"><a href="/wiki/%F0%9F%99%88" class="mw-redirect" title="🙈">🙈</a>
</td>
<td title="U+1F649: HEAR-NO-EVIL MONKEY"><a href="/wiki/%F0%9F%99%89" class="mw-redirect" title="🙉">🙉</a>
</td>
<td title="U+1F64A: SPEAK-NO-EVIL MONKEY"><a href="/wiki/%F0%9F%99%8A" class="mw-redirect" title="🙊">🙊</a>
</td>
<td title="U+1F64B: HAPPY PERSON RAISING ONE HAND"><a href="/wiki/%F0%9F%99%8B" class="mw-redirect" title="🙋">🙋</a>
</td>
<td title="U+1F64C: PERSON RAISING BOTH HANDS IN CELEBRATION"><a href="/wiki/%F0%9F%99%8C" class="mw-redirect" title="🙌">🙌</a>
</td>
<td title="U+1F64D: PERSON FROWNING"><a href="/wiki/%F0%9F%99%8D" class="mw-redirect" title="🙍">🙍</a>
</td>
<td title="U+1F64E: PERSON WITH POUTING FACE"><a href="/wiki/%F0%9F%99%8E" class="mw-redirect" title="🙎">🙎</a>
</td>
<td title="U+1F64F: PERSON WITH FOLDED HANDS"><a href="/wiki/%F0%9F%99%8F" class="mw-redirect" title="🙏">🙏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F68x
</td>
<td title="U+1F680: ROCKET"><a href="/wiki/%F0%9F%9A%80" class="mw-redirect" title="🚀">🚀</a>
</td>
<td title="U+1F681: HELICOPTER"><a href="/wiki/%F0%9F%9A%81" class="mw-redirect" title="🚁">🚁</a>
</td>
<td title="U+1F682: STEAM LOCOMOTIVE"><a href="/wiki/%F0%9F%9A%82" class="mw-redirect" title="🚂">🚂</a>
</td>
<td title="U+1F683: RAILWAY CAR"><a href="/wiki/%F0%9F%9A%83" class="mw-redirect" title="🚃">🚃</a>
</td>
<td title="U+1F684: HIGH-SPEED TRAIN"><a href="/wiki/%F0%9F%9A%84" class="mw-redirect" title="🚄">🚄</a>
</td>
<td title="U+1F685: HIGH-SPEED TRAIN WITH BULLET NOSE"><a href="/wiki/%F0%9F%9A%85" class="mw-redirect" title="🚅">🚅</a>
</td>
<td title="U+1F686: TRAIN"><a href="/wiki/%F0%9F%9A%86" class="mw-redirect" title="🚆">🚆</a>
</td>
<td title="U+1F687: METRO"><a href="/wiki/%F0%9F%9A%87" class="mw-redirect" title="🚇">🚇</a>
</td>
<td title="U+1F688: LIGHT RAIL"><a href="/wiki/%F0%9F%9A%88" class="mw-redirect" title="🚈">🚈</a>
</td>
<td title="U+1F689: STATION"><a href="/wiki/%F0%9F%9A%89" class="mw-redirect" title="🚉">🚉</a>
</td>
<td title="U+1F68A: TRAM"><a href="/wiki/%F0%9F%9A%8A" class="mw-redirect" title="🚊">🚊</a>
</td>
<td title="U+1F68B: TRAM CAR"><a href="/wiki/%F0%9F%9A%8B" class="mw-redirect" title="🚋">🚋</a>
</td>
<td title="U+1F68C: BUS"><a href="/wiki/%F0%9F%9A%8C" class="mw-redirect" title="🚌">🚌</a>
</td>
<td title="U+1F68D: ONCOMING BUS"><a href="/wiki/%F0%9F%9A%8D" class="mw-redirect" title="🚍">🚍</a>
</td>
<td title="U+1F68E: TROLLEYBUS"><a href="/wiki/%F0%9F%9A%8E" class="mw-redirect" title="🚎">🚎</a>
</td>
<td title="U+1F68F: BUS STOP"><a href="/wiki/%F0%9F%9A%8F" class="mw-redirect" title="🚏">🚏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F69x
</td>
<td title="U+1F690: MINIBUS"><a href="/wiki/%F0%9F%9A%90" class="mw-redirect" title="🚐">🚐</a>
</td>
<td title="U+1F691: AMBULANCE"><a href="/wiki/%F0%9F%9A%91" class="mw-redirect" title="🚑">🚑</a>
</td>
<td title="U+1F692: FIRE ENGINE"><a href="/wiki/%F0%9F%9A%92" class="mw-redirect" title="🚒">🚒</a>
</td>
<td title="U+1F693: POLICE CAR"><a href="/wiki/%F0%9F%9A%93" class="mw-redirect" title="🚓">🚓</a>
</td>
<td title="U+1F694: ONCOMING POLICE CAR"><a href="/wiki/%F0%9F%9A%94" class="mw-redirect" title="🚔">🚔</a>
</td>
<td title="U+1F695: TAXI"><a href="/wiki/%F0%9F%9A%95" class="mw-redirect" title="🚕">🚕</a>
</td>
<td title="U+1F696: ONCOMING TAXI"><a href="/wiki/%F0%9F%9A%96" class="mw-redirect" title="🚖">🚖</a>
</td>
<td title="U+1F697: AUTOMOBILE"><a href="/wiki/%F0%9F%9A%97" class="mw-redirect" title="🚗">🚗</a>
</td>
<td title="U+1F698: ONCOMING AUTOMOBILE"><a href="/wiki/%F0%9F%9A%98" class="mw-redirect" title="🚘">🚘</a>
</td>
<td title="U+1F699: RECREATIONAL VEHICLE"><a href="/wiki/%F0%9F%9A%99" class="mw-redirect" title="🚙">🚙</a>
</td>
<td title="U+1F69A: DELIVERY TRUCK"><a href="/wiki/%F0%9F%9A%9A" class="mw-redirect" title="🚚">🚚</a>
</td>
<td title="U+1F69B: ARTICULATED LORRY"><a href="/wiki/%F0%9F%9A%9B" class="mw-redirect" title="🚛">🚛</a>
</td>
<td title="U+1F69C: TRACTOR"><a href="/wiki/%F0%9F%9A%9C" class="mw-redirect" title="🚜">🚜</a>
</td>
<td title="U+1F69D: MONORAIL"><a href="/wiki/%F0%9F%9A%9D" class="mw-redirect" title="🚝">🚝</a>
</td>
<td title="U+1F69E: MOUNTAIN RAILWAY"><a href="/wiki/%F0%9F%9A%9E" class="mw-redirect" title="🚞">🚞</a>
</td>
<td title="U+1F69F: SUSPENSION RAILWAY"><a href="/wiki/%F0%9F%9A%9F" class="mw-redirect" title="🚟">🚟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F6Ax
</td>
<td title="U+1F6A0: MOUNTAIN CABLEWAY"><a href="/wiki/%F0%9F%9A%A0" class="mw-redirect" title="🚠">🚠</a>
</td>
<td title="U+1F6A1: AERIAL TRAMWAY"><a href="/wiki/%F0%9F%9A%A1" class="mw-redirect" title="🚡">🚡</a>
</td>
<td title="U+1F6A2: SHIP"><a href="/wiki/%F0%9F%9A%A2" class="mw-redirect" title="🚢">🚢</a>
</td>
<td title="U+1F6A3: ROWBOAT"><a href="/wiki/%F0%9F%9A%A3" class="mw-redirect" title="🚣">🚣</a>
</td>
<td title="U+1F6A4: SPEEDBOAT"><a href="/wiki/%F0%9F%9A%A4" class="mw-redirect" title="🚤">🚤</a>
</td>
<td title="U+1F6A5: HORIZONTAL TRAFFIC LIGHT"><a href="/wiki/%F0%9F%9A%A5" class="mw-redirect" title="🚥">🚥</a>
</td>
<td title="U+1F6A6: VERTICAL TRAFFIC LIGHT"><a href="/wiki/%F0%9F%9A%A6" class="mw-redirect" title="🚦">🚦</a>
</td>
<td title="U+1F6A7: CONSTRUCTION SIGN"><a href="/wiki/%F0%9F%9A%A7" class="mw-redirect" title="🚧">🚧</a>
</td>
<td title="U+1F6A8: POLICE CARS REVOLVING LIGHT"><a href="/wiki/%F0%9F%9A%A8" class="mw-redirect" title="🚨">🚨</a>
</td>
<td title="U+1F6A9: TRIANGULAR FLAG ON POST"><a href="/wiki/%F0%9F%9A%A9" class="mw-redirect" title="🚩">🚩</a>
</td>
<td title="U+1F6AA: DOOR"><a href="/wiki/%F0%9F%9A%AA" class="mw-redirect" title="🚪">🚪</a>
</td>
<td title="U+1F6AB: NO ENTRY SIGN"><a href="/wiki/%F0%9F%9A%AB" class="mw-redirect" title="🚫">🚫</a>
</td>
<td title="U+1F6AC: SMOKING SYMBOL"><a href="/wiki/%F0%9F%9A%AC" class="mw-redirect" title="🚬">🚬</a>
</td>
<td title="U+1F6AD: NO SMOKING SYMBOL"><a href="/wiki/%F0%9F%9A%AD" class="mw-redirect" title="🚭">🚭</a>
</td>
<td title="U+1F6AE: PUT LITTER IN ITS PLACE SYMBOL"><a href="/wiki/%F0%9F%9A%AE" class="mw-redirect" title="🚮">🚮</a>
</td>
<td title="U+1F6AF: DO NOT LITTER SYMBOL"><a href="/wiki/%F0%9F%9A%AF" class="mw-redirect" title="🚯">🚯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F6Bx
</td>
<td title="U+1F6B0: POTABLE WATER SYMBOL"><a href="/wiki/%F0%9F%9A%B0" class="mw-redirect" title="🚰">🚰</a>
</td>
<td title="U+1F6B1: NON-POTABLE WATER SYMBOL"><a href="/wiki/%F0%9F%9A%B1" class="mw-redirect" title="🚱">🚱</a>
</td>
<td title="U+1F6B2: BICYCLE"><a href="/wiki/%F0%9F%9A%B2" class="mw-redirect" title="🚲">🚲</a>
</td>
<td title="U+1F6B3: NO BICYCLES"><a href="/wiki/%F0%9F%9A%B3" class="mw-redirect" title="🚳">🚳</a>
</td>
<td title="U+1F6B4: BICYCLIST"><a href="/wiki/%F0%9F%9A%B4" class="mw-redirect" title="🚴">🚴</a>
</td>
<td title="U+1F6B5: MOUNTAIN BICYCLIST"><a href="/wiki/%F0%9F%9A%B5" class="mw-redirect" title="🚵">🚵</a>
</td>
<td title="U+1F6B6: PEDESTRIAN"><a href="/wiki/%F0%9F%9A%B6" class="mw-redirect" title="🚶">🚶</a>
</td>
<td title="U+1F6B7: NO PEDESTRIANS"><a href="/wiki/%F0%9F%9A%B7" class="mw-redirect" title="🚷">🚷</a>
</td>
<td title="U+1F6B8: CHILDREN CROSSING"><a href="/wiki/%F0%9F%9A%B8" class="mw-redirect" title="🚸">🚸</a>
</td>
<td title="U+1F6B9: MENS SYMBOL"><a href="/wiki/%F0%9F%9A%B9" class="mw-redirect" title="🚹">🚹</a>
</td>
<td title="U+1F6BA: WOMENS SYMBOL"><a href="/wiki/%F0%9F%9A%BA" class="mw-redirect" title="🚺">🚺</a>
</td>
<td title="U+1F6BB: RESTROOM"><a href="/wiki/%F0%9F%9A%BB" class="mw-redirect" title="🚻">🚻</a>
</td>
<td title="U+1F6BC: BABY SYMBOL"><a href="/wiki/%F0%9F%9A%BC" class="mw-redirect" title="🚼">🚼</a>
</td>
<td title="U+1F6BD: TOILET"><a href="/wiki/%F0%9F%9A%BD" class="mw-redirect" title="🚽">🚽</a>
</td>
<td title="U+1F6BE: WATER CLOSET"><a href="/wiki/%F0%9F%9A%BE" class="mw-redirect" title="🚾">🚾</a>
</td>
<td title="U+1F6BF: SHOWER"><a href="/wiki/%F0%9F%9A%BF" class="mw-redirect" title="🚿">🚿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F6Cx
</td>
<td title="U+1F6C0: BATH"><a href="/wiki/%F0%9F%9B%80" class="mw-redirect" title="🛀">🛀</a>
</td>
<td title="U+1F6C1: BATHTUB"><a href="/wiki/%F0%9F%9B%81" class="mw-redirect" title="🛁">🛁</a>
</td>
<td title="U+1F6C2: PASSPORT CONTROL"><a href="/wiki/%F0%9F%9B%82" class="mw-redirect" title="🛂">🛂</a>
</td>
<td title="U+1F6C3: CUSTOMS"><a href="/wiki/%F0%9F%9B%83" class="mw-redirect" title="🛃">🛃</a>
</td>
<td title="U+1F6C4: BAGGAGE CLAIM"><a href="/wiki/%F0%9F%9B%84" class="mw-redirect" title="🛄">🛄</a>
</td>
<td title="U+1F6C5: LEFT LUGGAGE"><a href="/wiki/%F0%9F%9B%85" class="mw-redirect" title="🛅">🛅</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F6CB: COUCH AND LAMP"><a href="/wiki/%F0%9F%9B%8B" class="mw-redirect" title="🛋">🛋️</a>
</td>
<td title="U+1F6CC: SLEEPING ACCOMMODATION"><a href="/wiki/%F0%9F%9B%8C" class="mw-redirect" title="🛌">🛌</a>
</td>
<td title="U+1F6CD: SHOPPING BAGS"><a href="/wiki/%F0%9F%9B%8D" class="mw-redirect" title="🛍">🛍️</a>
</td>
<td title="U+1F6CE: BELLHOP BELL"><a href="/wiki/%F0%9F%9B%8E" class="mw-redirect" title="🛎">🛎️</a>
</td>
<td title="U+1F6CF: BED"><a href="/wiki/%F0%9F%9B%8F" class="mw-redirect" title="🛏">🛏️</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F6Dx
</td>
<td title="U+1F6D0: PLACE OF WORSHIP"><a href="/wiki/%F0%9F%9B%90" class="mw-redirect" title="🛐">🛐</a>
</td>
<td title="U+1F6D1: OCTAGONAL SIGN"><a href="/wiki/%F0%9F%9B%91" class="mw-redirect" title="🛑">🛑</a>
</td>
<td title="U+1F6D2: SHOPPING TROLLEY"><a href="/wiki/%F0%9F%9B%92" class="mw-redirect" title="🛒">🛒</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F6D5: HINDU TEMPLE"><a href="/wiki/%F0%9F%9B%95" class="mw-redirect" title="🛕">🛕</a>
</td>
<td title="U+1F6D6: HUT"><a href="/wiki/%F0%9F%9B%96" class="mw-redirect" title="🛖">🛖</a>
</td>
<td title="U+1F6D7: ELEVATOR"><a href="/wiki/%F0%9F%9B%97" class="mw-redirect" title="🛗">🛗</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F6DC: WIRELESS"><a href="/wiki/%F0%9F%9B%9C" class="mw-redirect" title="🛜">🛜</a>
</td>
<td title="U+1F6DD: PLAYGROUND SLIDE"><a href="/wiki/%F0%9F%9B%9D" class="mw-redirect" title="🛝">🛝</a>
</td>
<td title="U+1F6DE: WHEEL"><a href="/wiki/%F0%9F%9B%9E" class="mw-redirect" title="🛞">🛞</a>
</td>
<td title="U+1F6DF: RING BUOY"><a href="/wiki/%F0%9F%9B%9F" class="mw-redirect" title="🛟">🛟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F6Ex
</td>
<td title="U+1F6E0: HAMMER AND WRENCH"><a href="/wiki/%F0%9F%9B%A0" class="mw-redirect" title="🛠">🛠️</a>
</td>
<td title="U+1F6E1: SHIELD"><a href="/wiki/%F0%9F%9B%A1" class="mw-redirect" title="🛡">🛡️</a>
</td>
<td title="U+1F6E2: OIL DRUM"><a href="/wiki/%F0%9F%9B%A2" class="mw-redirect" title="🛢">🛢️</a>
</td>
<td title="U+1F6E3: MOTORWAY"><a href="/wiki/%F0%9F%9B%A3" class="mw-redirect" title="🛣">🛣️</a>
</td>
<td title="U+1F6E4: RAILWAY TRACK"><a href="/wiki/%F0%9F%9B%A4" class="mw-redirect" title="🛤">🛤️</a>
</td>
<td title="U+1F6E5: MOTOR BOAT"><a href="/wiki/%F0%9F%9B%A5" class="mw-redirect" title="🛥">🛥️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F6E9: SMALL AIRPLANE"><a href="/wiki/%F0%9F%9B%A9" class="mw-redirect" title="🛩">🛩️</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F6EB: AIRPLANE DEPARTURE"><a href="/wiki/%F0%9F%9B%AB" class="mw-redirect" title="🛫">🛫</a>
</td>
<td title="U+1F6EC: AIRPLANE ARRIVING"><a href="/wiki/%F0%9F%9B%AC" class="mw-redirect" title="🛬">🛬</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F6Fx
</td>
<td title="U+1F6F0: SATELLITE"><a href="/wiki/%F0%9F%9B%B0" class="mw-redirect" title="🛰">🛰️</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F6F3: PASSENGER SHIP"><a href="/wiki/%F0%9F%9B%B3" class="mw-redirect" title="🛳">🛳️</a>
</td>
<td title="U+1F6F4: SCOOTER"><a href="/wiki/%F0%9F%9B%B4" class="mw-redirect" title="🛴">🛴</a>
</td>
<td title="U+1F6F5: MOTOR SCOOTER"><a href="/wiki/%F0%9F%9B%B5" class="mw-redirect" title="🛵">🛵</a>
</td>
<td title="U+1F6F6: CANOE"><a href="/wiki/%F0%9F%9B%B6" class="mw-redirect" title="🛶">🛶</a>
</td>
<td title="U+1F6F7: SLED"><a href="/wiki/%F0%9F%9B%B7" class="mw-redirect" title="🛷">🛷</a>
</td>
<td title="U+1F6F8: FLYING SAUCER"><a href="/wiki/%F0%9F%9B%B8" class="mw-redirect" title="🛸">🛸</a>
</td>
<td title="U+1F6F9: SKATEBOARD"><a href="/wiki/%F0%9F%9B%B9" class="mw-redirect" title="🛹">🛹</a>
</td>
<td title="U+1F6FA: AUTO RICKSHAW"><a href="/wiki/%F0%9F%9B%BA" class="mw-redirect" title="🛺">🛺</a>
</td>
<td title="U+1F6FB: PICKUP TRUCK"><a href="/wiki/%F0%9F%9B%BB" class="mw-redirect" title="🛻">🛻</a>
</td>
<td title="U+1F6FC: ROLLER SKATE"><a href="/wiki/%F0%9F%9B%BC" class="mw-redirect" title="🛼">🛼</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F7Ex
</td>
<td title="U+1F7E0: LARGE ORANGE CIRCLE"><a href="/wiki/%F0%9F%9F%A0" class="mw-redirect" title="🟠">🟠</a>
</td>
<td title="U+1F7E1: LARGE YELLOW CIRCLE"><a href="/wiki/%F0%9F%9F%A1" class="mw-redirect" title="🟡">🟡</a>
</td>
<td title="U+1F7E2: LARGE GREEN CIRCLE"><a href="/wiki/%F0%9F%9F%A2" class="mw-redirect" title="🟢">🟢</a>
</td>
<td title="U+1F7E3: LARGE PURPLE CIRCLE"><a href="/wiki/%F0%9F%9F%A3" class="mw-redirect" title="🟣">🟣</a>
</td>
<td title="U+1F7E4: LARGE BROWN CIRCLE"><a href="/wiki/%F0%9F%9F%A4" class="mw-redirect" title="🟤">🟤</a>
</td>
<td title="U+1F7E5: LARGE RED SQUARE"><a href="/wiki/%F0%9F%9F%A5" class="mw-redirect" title="🟥">🟥</a>
</td>
<td title="U+1F7E6: LARGE BLUE SQUARE"><a href="/wiki/%F0%9F%9F%A6" class="mw-redirect" title="🟦">🟦</a>
</td>
<td title="U+1F7E7: LARGE ORANGE SQUARE"><a href="/wiki/%F0%9F%9F%A7" class="mw-redirect" title="🟧">🟧</a>
</td>
<td title="U+1F7E8: LARGE YELLOW SQUARE"><a href="/wiki/%F0%9F%9F%A8" class="mw-redirect" title="🟨">🟨</a>
</td>
<td title="U+1F7E9: LARGE GREEN SQUARE"><a href="/wiki/%F0%9F%9F%A9" class="mw-redirect" title="🟩">🟩</a>
</td>
<td title="U+1F7EA: LARGE PURPLE SQUARE"><a href="/wiki/%F0%9F%9F%AA" class="mw-redirect" title="🟪">🟪</a>
</td>
<td title="U+1F7EB: LARGE BROWN SQUARE"><a href="/wiki/%F0%9F%9F%AB" class="mw-redirect" title="🟫">🟫</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td colspan="17">
</td></tr>
<tr style="background:#F8F8F8;font-size:small;font-family:sans-serif">
<td style="width:45pt">&nbsp;</td>
<td style="width:20pt">0</td>
<td style="width:20pt">1</td>
<td style="width:20pt">2</td>
<td style="width:20pt">3</td>
<td style="width:20pt">4</td>
<td style="width:20pt">5</td>
<td style="width:20pt">6</td>
<td style="width:20pt">7</td>
<td style="width:20pt">8</td>
<td style="width:20pt">9</td>
<td style="width:20pt">A</td>
<td style="width:20pt">B</td>
<td style="width:20pt">C</td>
<td style="width:20pt">D</td>
<td style="width:20pt">E</td>
<td style="width:20pt">F
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F7Fx
</td>
<td title="U+1F7F0: HEAVY EQUALS SIGN"><a href="/wiki/%F0%9F%9F%B0" class="mw-redirect" title="🟰">🟰</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F90x
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F90C: PINCHED FINGERS"><a href="/wiki/%F0%9F%A4%8C" class="mw-redirect" title="🤌">🤌</a>
</td>
<td title="U+1F90D: WHITE HEART"><a href="/wiki/%F0%9F%A4%8D" class="mw-redirect" title="🤍">🤍</a>
</td>
<td title="U+1F90E: BROWN HEART"><a href="/wiki/%F0%9F%A4%8E" class="mw-redirect" title="🤎">🤎</a>
</td>
<td title="U+1F90F: PINCHING HAND"><a href="/wiki/%F0%9F%A4%8F" class="mw-redirect" title="🤏">🤏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F91x
</td>
<td title="U+1F910: ZIPPER-MOUTH FACE"><a href="/wiki/%F0%9F%A4%90" class="mw-redirect" title="🤐">🤐</a>
</td>
<td title="U+1F911: MONEY-MOUTH FACE"><a href="/wiki/%F0%9F%A4%91" class="mw-redirect" title="🤑">🤑</a>
</td>
<td title="U+1F912: FACE WITH THERMOMETER"><a href="/wiki/%F0%9F%A4%92" class="mw-redirect" title="🤒">🤒</a>
</td>
<td title="U+1F913: NERD FACE"><a href="/wiki/%F0%9F%A4%93" class="mw-redirect" title="🤓">🤓</a>
</td>
<td title="U+1F914: THINKING FACE"><a href="/wiki/%F0%9F%A4%94" class="mw-redirect" title="🤔">🤔</a>
</td>
<td title="U+1F915: FACE WITH HEAD-BANDAGE"><a href="/wiki/%F0%9F%A4%95" class="mw-redirect" title="🤕">🤕</a>
</td>
<td title="U+1F916: ROBOT FACE"><a href="/wiki/%F0%9F%A4%96" class="mw-redirect" title="🤖">🤖</a>
</td>
<td title="U+1F917: HUGGING FACE"><a href="/wiki/%F0%9F%A4%97" class="mw-redirect" title="🤗">🤗</a>
</td>
<td title="U+1F918: SIGN OF THE HORNS"><a href="/wiki/%F0%9F%A4%98" class="mw-redirect" title="🤘">🤘</a>
</td>
<td title="U+1F919: CALL ME HAND"><a href="/wiki/%F0%9F%A4%99" class="mw-redirect" title="🤙">🤙</a>
</td>
<td title="U+1F91A: RAISED BACK OF HAND"><a href="/wiki/%F0%9F%A4%9A" class="mw-redirect" title="🤚">🤚</a>
</td>
<td title="U+1F91B: LEFT-FACING FIST"><a href="/wiki/%F0%9F%A4%9B" class="mw-redirect" title="🤛">🤛</a>
</td>
<td title="U+1F91C: RIGHT-FACING FIST"><a href="/wiki/%F0%9F%A4%9C" class="mw-redirect" title="🤜">🤜</a>
</td>
<td title="U+1F91D: HANDSHAKE"><a href="/wiki/%F0%9F%A4%9D" class="mw-redirect" title="🤝">🤝</a>
</td>
<td title="U+1F91E: HAND WITH INDEX AND MIDDLE FINGERS CROSSED"><a href="/wiki/%F0%9F%A4%9E" class="mw-redirect" title="🤞">🤞</a>
</td>
<td title="U+1F91F: I LOVE YOU HAND SIGN"><a href="/wiki/%F0%9F%A4%9F" class="mw-redirect" title="🤟">🤟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F92x
</td>
<td title="U+1F920: FACE WITH COWBOY HAT"><a href="/wiki/%F0%9F%A4%A0" class="mw-redirect" title="🤠">🤠</a>
</td>
<td title="U+1F921: CLOWN FACE"><a href="/wiki/%F0%9F%A4%A1" class="mw-redirect" title="🤡">🤡</a>
</td>
<td title="U+1F922: NAUSEATED FACE"><a href="/wiki/%F0%9F%A4%A2" class="mw-redirect" title="🤢">🤢</a>
</td>
<td title="U+1F923: ROLLING ON THE FLOOR LAUGHING"><a href="/wiki/%F0%9F%A4%A3" class="mw-redirect" title="🤣">🤣</a>
</td>
<td title="U+1F924: DROOLING FACE"><a href="/wiki/%F0%9F%A4%A4" class="mw-redirect" title="🤤">🤤</a>
</td>
<td title="U+1F925: LYING FACE"><a href="/wiki/%F0%9F%A4%A5" class="mw-redirect" title="🤥">🤥</a>
</td>
<td title="U+1F926: FACE PALM"><a href="/wiki/%F0%9F%A4%A6" class="mw-redirect" title="🤦">🤦</a>
</td>
<td title="U+1F927: SNEEZING FACE"><a href="/wiki/%F0%9F%A4%A7" class="mw-redirect" title="🤧">🤧</a>
</td>
<td title="U+1F928: FACE WITH ONE EYEBROW RAISED"><a href="/wiki/%F0%9F%A4%A8" class="mw-redirect" title="🤨">🤨</a>
</td>
<td title="U+1F929: GRINNING FACE WITH STAR EYES"><a href="/wiki/%F0%9F%A4%A9" class="mw-redirect" title="🤩">🤩</a>
</td>
<td title="U+1F92A: GRINNING FACE WITH ONE LARGE AND ONE SMALL EYE"><a href="/wiki/%F0%9F%A4%AA" class="mw-redirect" title="🤪">🤪</a>
</td>
<td title="U+1F92B: FACE WITH FINGER COVERING CLOSED LIPS"><a href="/wiki/%F0%9F%A4%AB" class="mw-redirect" title="🤫">🤫</a>
</td>
<td title="U+1F92C: SERIOUS FACE WITH SYMBOLS COVERING MOUTH"><a href="/wiki/%F0%9F%A4%AC" class="mw-redirect" title="🤬">🤬</a>
</td>
<td title="U+1F92D: SMILING FACE WITH SMILING EYES AND HAND COVERING MOUTH"><a href="/wiki/%F0%9F%A4%AD" class="mw-redirect" title="🤭">🤭</a>
</td>
<td title="U+1F92E: FACE WITH OPEN MOUTH VOMITING"><a href="/wiki/%F0%9F%A4%AE" class="mw-redirect" title="🤮">🤮</a>
</td>
<td title="U+1F92F: SHOCKED FACE WITH EXPLODING HEAD"><a href="/wiki/%F0%9F%A4%AF" class="mw-redirect" title="🤯">🤯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F93x
</td>
<td title="U+1F930: PREGNANT WOMAN"><a href="/wiki/%F0%9F%A4%B0" class="mw-redirect" title="🤰">🤰</a>
</td>
<td title="U+1F931: BREAST-FEEDING"><a href="/wiki/%F0%9F%A4%B1" class="mw-redirect" title="🤱">🤱</a>
</td>
<td title="U+1F932: PALMS UP TOGETHER"><a href="/wiki/%F0%9F%A4%B2" class="mw-redirect" title="🤲">🤲</a>
</td>
<td title="U+1F933: SELFIE"><a href="/wiki/%F0%9F%A4%B3" class="mw-redirect" title="🤳">🤳</a>
</td>
<td title="U+1F934: PRINCE"><a href="/wiki/%F0%9F%A4%B4" class="mw-redirect" title="🤴">🤴</a>
</td>
<td title="U+1F935: MAN IN TUXEDO"><a href="/wiki/%F0%9F%A4%B5" class="mw-redirect" title="🤵">🤵</a>
</td>
<td title="U+1F936: MOTHER CHRISTMAS"><a href="/wiki/%F0%9F%A4%B6" class="mw-redirect" title="🤶">🤶</a>
</td>
<td title="U+1F937: SHRUG"><a href="/wiki/%F0%9F%A4%B7" class="mw-redirect" title="🤷">🤷</a>
</td>
<td title="U+1F938: PERSON DOING CARTWHEEL"><a href="/wiki/%F0%9F%A4%B8" class="mw-redirect" title="🤸">🤸</a>
</td>
<td title="U+1F939: JUGGLING"><a href="/wiki/%F0%9F%A4%B9" class="mw-redirect" title="🤹">🤹</a>
</td>
<td title="U+1F93A: FENCER"><a href="/wiki/%F0%9F%A4%BA" class="mw-redirect" title="🤺">🤺</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F93C: WRESTLERS"><a href="/wiki/%F0%9F%A4%BC" class="mw-redirect" title="🤼">🤼</a>
</td>
<td title="U+1F93D: WATER POLO"><a href="/wiki/%F0%9F%A4%BD" class="mw-redirect" title="🤽">🤽</a>
</td>
<td title="U+1F93E: HANDBALL"><a href="/wiki/%F0%9F%A4%BE" class="mw-redirect" title="🤾">🤾</a>
</td>
<td title="U+1F93F: DIVING MASK"><a href="/wiki/%F0%9F%A4%BF" class="mw-redirect" title="🤿">🤿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F94x
</td>
<td title="U+1F940: WILTED FLOWER"><a href="/wiki/%F0%9F%A5%80" class="mw-redirect" title="🥀">🥀</a>
</td>
<td title="U+1F941: DRUM WITH DRUMSTICKS"><a href="/wiki/%F0%9F%A5%81" class="mw-redirect" title="🥁">🥁</a>
</td>
<td title="U+1F942: CLINKING GLASSES"><a href="/wiki/%F0%9F%A5%82" class="mw-redirect" title="🥂">🥂</a>
</td>
<td title="U+1F943: TUMBLER GLASS"><a href="/wiki/%F0%9F%A5%83" class="mw-redirect" title="🥃">🥃</a>
</td>
<td title="U+1F944: SPOON"><a href="/wiki/%F0%9F%A5%84" class="mw-redirect" title="🥄">🥄</a>
</td>
<td title="U+1F945: GOAL NET"><a href="/wiki/%F0%9F%A5%85" class="mw-redirect" title="🥅">🥅</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1F947: FIRST PLACE MEDAL"><a href="/wiki/%F0%9F%A5%87" class="mw-redirect" title="🥇">🥇</a>
</td>
<td title="U+1F948: SECOND PLACE MEDAL"><a href="/wiki/%F0%9F%A5%88" class="mw-redirect" title="🥈">🥈</a>
</td>
<td title="U+1F949: THIRD PLACE MEDAL"><a href="/wiki/%F0%9F%A5%89" class="mw-redirect" title="🥉">🥉</a>
</td>
<td title="U+1F94A: BOXING GLOVE"><a href="/wiki/%F0%9F%A5%8A" class="mw-redirect" title="🥊">🥊</a>
</td>
<td title="U+1F94B: MARTIAL ARTS UNIFORM"><a href="/wiki/%F0%9F%A5%8B" class="mw-redirect" title="🥋">🥋</a>
</td>
<td title="U+1F94C: CURLING STONE"><a href="/wiki/%F0%9F%A5%8C" class="mw-redirect" title="🥌">🥌</a>
</td>
<td title="U+1F94D: LACROSSE STICK AND BALL"><a href="/wiki/%F0%9F%A5%8D" class="mw-redirect" title="🥍">🥍</a>
</td>
<td title="U+1F94E: SOFTBALL"><a href="/wiki/%F0%9F%A5%8E" class="mw-redirect" title="🥎">🥎</a>
</td>
<td title="U+1F94F: FLYING DISC"><a href="/wiki/%F0%9F%A5%8F" class="mw-redirect" title="🥏">🥏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F95x
</td>
<td title="U+1F950: CROISSANT"><a href="/wiki/%F0%9F%A5%90" class="mw-redirect" title="🥐">🥐</a>
</td>
<td title="U+1F951: AVOCADO"><a href="/wiki/%F0%9F%A5%91" class="mw-redirect" title="🥑">🥑</a>
</td>
<td title="U+1F952: CUCUMBER"><a href="/wiki/%F0%9F%A5%92" class="mw-redirect" title="🥒">🥒</a>
</td>
<td title="U+1F953: BACON"><a href="/wiki/%F0%9F%A5%93" class="mw-redirect" title="🥓">🥓</a>
</td>
<td title="U+1F954: POTATO"><a href="/wiki/%F0%9F%A5%94" class="mw-redirect" title="🥔">🥔</a>
</td>
<td title="U+1F955: CARROT"><a href="/wiki/%F0%9F%A5%95" class="mw-redirect" title="🥕">🥕</a>
</td>
<td title="U+1F956: BAGUETTE BREAD"><a href="/wiki/%F0%9F%A5%96" class="mw-redirect" title="🥖">🥖</a>
</td>
<td title="U+1F957: GREEN SALAD"><a href="/wiki/%F0%9F%A5%97" class="mw-redirect" title="🥗">🥗</a>
</td>
<td title="U+1F958: SHALLOW PAN OF FOOD"><a href="/wiki/%F0%9F%A5%98" class="mw-redirect" title="🥘">🥘</a>
</td>
<td title="U+1F959: STUFFED FLATBREAD"><a href="/wiki/%F0%9F%A5%99" class="mw-redirect" title="🥙">🥙</a>
</td>
<td title="U+1F95A: EGG"><a href="/wiki/%F0%9F%A5%9A" class="mw-redirect" title="🥚">🥚</a>
</td>
<td title="U+1F95B: GLASS OF MILK"><a href="/wiki/%F0%9F%A5%9B" class="mw-redirect" title="🥛">🥛</a>
</td>
<td title="U+1F95C: PEANUTS"><a href="/wiki/%F0%9F%A5%9C" class="mw-redirect" title="🥜">🥜</a>
</td>
<td title="U+1F95D: KIWIFRUIT"><a href="/wiki/%F0%9F%A5%9D" class="mw-redirect" title="🥝">🥝</a>
</td>
<td title="U+1F95E: PANCAKES"><a href="/wiki/%F0%9F%A5%9E" class="mw-redirect" title="🥞">🥞</a>
</td>
<td title="U+1F95F: DUMPLING"><a href="/wiki/%F0%9F%A5%9F" class="mw-redirect" title="🥟">🥟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F96x
</td>
<td title="U+1F960: FORTUNE COOKIE"><a href="/wiki/%F0%9F%A5%A0" class="mw-redirect" title="🥠">🥠</a>
</td>
<td title="U+1F961: TAKEOUT BOX"><a href="/wiki/%F0%9F%A5%A1" class="mw-redirect" title="🥡">🥡</a>
</td>
<td title="U+1F962: CHOPSTICKS"><a href="/wiki/%F0%9F%A5%A2" class="mw-redirect" title="🥢">🥢</a>
</td>
<td title="U+1F963: BOWL WITH SPOON"><a href="/wiki/%F0%9F%A5%A3" title="🥣">🥣</a>
</td>
<td title="U+1F964: CUP WITH STRAW"><a href="/wiki/%F0%9F%A5%A4" title="🥤">🥤</a>
</td>
<td title="U+1F965: COCONUT"><a href="/wiki/%F0%9F%A5%A5" class="mw-redirect" title="🥥">🥥</a>
</td>
<td title="U+1F966: BROCCOLI"><a href="/wiki/%F0%9F%A5%A6" class="mw-redirect" title="🥦">🥦</a>
</td>
<td title="U+1F967: PIE"><a href="/wiki/%F0%9F%A5%A7" class="mw-redirect" title="🥧">🥧</a>
</td>
<td title="U+1F968: PRETZEL"><a href="/wiki/%F0%9F%A5%A8" class="mw-redirect" title="🥨">🥨</a>
</td>
<td title="U+1F969: CUT OF MEAT"><a href="/wiki/%F0%9F%A5%A9" class="mw-redirect" title="🥩">🥩</a>
</td>
<td title="U+1F96A: SANDWICH"><a href="/wiki/%F0%9F%A5%AA" class="mw-redirect" title="🥪">🥪</a>
</td>
<td title="U+1F96B: CANNED FOOD"><a href="/wiki/%F0%9F%A5%AB" class="mw-redirect" title="🥫">🥫</a>
</td>
<td title="U+1F96C: LEAFY GREEN"><a href="/wiki/%F0%9F%A5%AC" class="mw-redirect" title="🥬">🥬</a>
</td>
<td title="U+1F96D: MANGO"><a href="/wiki/%F0%9F%A5%AD" class="mw-redirect" title="🥭">🥭</a>
</td>
<td title="U+1F96E: MOON CAKE"><a href="/wiki/%F0%9F%A5%AE" class="mw-redirect" title="🥮">🥮</a>
</td>
<td title="U+1F96F: BAGEL"><a href="/wiki/%F0%9F%A5%AF" class="mw-redirect" title="🥯">🥯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F97x
</td>
<td title="U+1F970: SMILING FACE WITH SMILING EYES AND THREE HEARTS"><a href="/wiki/%F0%9F%A5%B0" class="mw-redirect" title="🥰">🥰</a>
</td>
<td title="U+1F971: YAWNING FACE"><a href="/wiki/%F0%9F%A5%B1" class="mw-redirect" title="🥱">🥱</a>
</td>
<td title="U+1F972: SMILING FACE WITH TEAR"><a href="/wiki/%F0%9F%A5%B2" class="mw-redirect" title="🥲">🥲</a>
</td>
<td title="U+1F973: FACE WITH PARTY HORN AND PARTY HAT"><a href="/wiki/%F0%9F%A5%B3" class="mw-redirect" title="🥳">🥳</a>
</td>
<td title="U+1F974: FACE WITH UNEVEN EYES AND WAVY MOUTH"><a href="/wiki/%F0%9F%A5%B4" class="mw-redirect" title="🥴">🥴</a>
</td>
<td title="U+1F975: OVERHEATED FACE"><a href="/wiki/%F0%9F%A5%B5" class="mw-redirect" title="🥵">🥵</a>
</td>
<td title="U+1F976: FREEZING FACE"><a href="/wiki/%F0%9F%A5%B6" class="mw-redirect" title="🥶">🥶</a>
</td>
<td title="U+1F977: NINJA"><a href="/wiki/%F0%9F%A5%B7" class="mw-redirect" title="🥷">🥷</a>
</td>
<td title="U+1F978: DISGUISED FACE"><a href="/wiki/%F0%9F%A5%B8" class="mw-redirect" title="🥸">🥸</a>
</td>
<td title="U+1F979: FACE HOLDING BACK TEARS"><a href="/wiki/%F0%9F%A5%B9" class="mw-redirect" title="🥹">🥹</a>
</td>
<td title="U+1F97A: FACE WITH PLEADING EYES"><a href="/wiki/%F0%9F%A5%BA" title="🥺">🥺</a>
</td>
<td title="U+1F97B: SARI"><a href="/wiki/%F0%9F%A5%BB" class="mw-redirect" title="🥻">🥻</a>
</td>
<td title="U+1F97C: LAB COAT"><a href="/wiki/%F0%9F%A5%BC" class="mw-redirect" title="🥼">🥼</a>
</td>
<td title="U+1F97D: GOGGLES"><a href="/wiki/%F0%9F%A5%BD" class="mw-redirect" title="🥽">🥽</a>
</td>
<td title="U+1F97E: HIKING BOOT"><a href="/wiki/%F0%9F%A5%BE" class="mw-redirect" title="🥾">🥾</a>
</td>
<td title="U+1F97F: FLAT SHOE"><a href="/wiki/%F0%9F%A5%BF" class="mw-redirect" title="🥿">🥿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F98x
</td>
<td title="U+1F980: CRAB"><a href="/wiki/%F0%9F%A6%80" class="mw-redirect" title="🦀">🦀</a>
</td>
<td title="U+1F981: LION FACE"><a href="/wiki/%F0%9F%A6%81" class="mw-redirect" title="🦁">🦁</a>
</td>
<td title="U+1F982: SCORPION"><a href="/wiki/%F0%9F%A6%82" class="mw-redirect" title="🦂">🦂</a>
</td>
<td title="U+1F983: TURKEY"><a href="/wiki/%F0%9F%A6%83" class="mw-redirect" title="🦃">🦃</a>
</td>
<td title="U+1F984: UNICORN FACE"><a href="/wiki/%F0%9F%A6%84" class="mw-redirect" title="🦄">🦄</a>
</td>
<td title="U+1F985: EAGLE"><a href="/wiki/%F0%9F%A6%85" class="mw-redirect" title="🦅">🦅</a>
</td>
<td title="U+1F986: DUCK"><a href="/wiki/%F0%9F%A6%86" class="mw-redirect" title="🦆">🦆</a>
</td>
<td title="U+1F987: BAT"><a href="/wiki/%F0%9F%A6%87" class="mw-redirect" title="🦇">🦇</a>
</td>
<td title="U+1F988: SHARK"><a href="/wiki/%F0%9F%A6%88" class="mw-redirect" title="🦈">🦈</a>
</td>
<td title="U+1F989: OWL"><a href="/wiki/%F0%9F%A6%89" class="mw-redirect" title="🦉">🦉</a>
</td>
<td title="U+1F98A: FOX FACE"><a href="/wiki/%F0%9F%A6%8A" class="mw-redirect" title="🦊">🦊</a>
</td>
<td title="U+1F98B: BUTTERFLY"><a href="/wiki/%F0%9F%A6%8B" class="mw-redirect" title="🦋">🦋</a>
</td>
<td title="U+1F98C: DEER"><a href="/wiki/%F0%9F%A6%8C" class="mw-redirect" title="🦌">🦌</a>
</td>
<td title="U+1F98D: GORILLA"><a href="/wiki/%F0%9F%A6%8D" class="mw-redirect" title="🦍">🦍</a>
</td>
<td title="U+1F98E: LIZARD"><a href="/wiki/%F0%9F%A6%8E" class="mw-redirect" title="🦎">🦎</a>
</td>
<td title="U+1F98F: RHINOCEROS"><a href="/wiki/%F0%9F%A6%8F" class="mw-redirect" title="🦏">🦏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F99x
</td>
<td title="U+1F990: SHRIMP"><a href="/wiki/%F0%9F%A6%90" class="mw-redirect" title="🦐">🦐</a>
</td>
<td title="U+1F991: SQUID"><a href="/wiki/%F0%9F%A6%91" class="mw-redirect" title="🦑">🦑</a>
</td>
<td title="U+1F992: GIRAFFE FACE"><a href="/wiki/%F0%9F%A6%92" class="mw-redirect" title="🦒">🦒</a>
</td>
<td title="U+1F993: ZEBRA FACE"><a href="/wiki/%F0%9F%A6%93" class="mw-redirect" title="🦓">🦓</a>
</td>
<td title="U+1F994: HEDGEHOG"><a href="/wiki/%F0%9F%A6%94" class="mw-redirect" title="🦔">🦔</a>
</td>
<td title="U+1F995: SAUROPOD"><a href="/wiki/%F0%9F%A6%95" class="mw-redirect" title="🦕">🦕</a>
</td>
<td title="U+1F996: T-REX"><a href="/wiki/%F0%9F%A6%96" class="mw-redirect" title="🦖">🦖</a>
</td>
<td title="U+1F997: CRICKET"><a href="/wiki/%F0%9F%A6%97" class="mw-redirect" title="🦗">🦗</a>
</td>
<td title="U+1F998: KANGAROO"><a href="/wiki/%F0%9F%A6%98" class="mw-redirect" title="🦘">🦘</a>
</td>
<td title="U+1F999: LLAMA"><a href="/wiki/%F0%9F%A6%99" class="mw-redirect" title="🦙">🦙</a>
</td>
<td title="U+1F99A: PEACOCK"><a href="/wiki/%F0%9F%A6%9A" class="mw-redirect" title="🦚">🦚</a>
</td>
<td title="U+1F99B: HIPPOPOTAMUS"><a href="/wiki/%F0%9F%A6%9B" class="mw-redirect" title="🦛">🦛</a>
</td>
<td title="U+1F99C: PARROT"><a href="/wiki/%F0%9F%A6%9C" class="mw-redirect" title="🦜">🦜</a>
</td>
<td title="U+1F99D: RACCOON"><a href="/wiki/%F0%9F%A6%9D" class="mw-redirect" title="🦝">🦝</a>
</td>
<td title="U+1F99E: LOBSTER"><a href="/wiki/%F0%9F%A6%9E" class="mw-redirect" title="🦞">🦞</a>
</td>
<td title="U+1F99F: MOSQUITO"><a href="/wiki/%F0%9F%A6%9F" class="mw-redirect" title="🦟">🦟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F9Ax
</td>
<td title="U+1F9A0: MICROBE"><a href="/wiki/%F0%9F%A6%A0" class="mw-redirect" title="🦠">🦠</a>
</td>
<td title="U+1F9A1: BADGER"><a href="/wiki/%F0%9F%A6%A1" class="mw-redirect" title="🦡">🦡</a>
</td>
<td title="U+1F9A2: SWAN"><a href="/wiki/%F0%9F%A6%A2" class="mw-redirect" title="🦢">🦢</a>
</td>
<td title="U+1F9A3: MAMMOTH"><a href="/wiki/%F0%9F%A6%A3" class="mw-redirect" title="🦣">🦣</a>
</td>
<td title="U+1F9A4: DODO"><a href="/wiki/%F0%9F%A6%A4" class="mw-redirect" title="🦤">🦤</a>
</td>
<td title="U+1F9A5: SLOTH"><a href="/wiki/%F0%9F%A6%A5" class="mw-redirect" title="🦥">🦥</a>
</td>
<td title="U+1F9A6: OTTER"><a href="/wiki/%F0%9F%A6%A6" class="mw-redirect" title="🦦">🦦</a>
</td>
<td title="U+1F9A7: ORANGUTAN"><a href="/wiki/%F0%9F%A6%A7" class="mw-redirect" title="🦧">🦧</a>
</td>
<td title="U+1F9A8: SKUNK"><a href="/wiki/%F0%9F%A6%A8" class="mw-redirect" title="🦨">🦨</a>
</td>
<td title="U+1F9A9: FLAMINGO"><a href="/wiki/%F0%9F%A6%A9" class="mw-redirect" title="🦩">🦩</a>
</td>
<td title="U+1F9AA: OYSTER"><a href="/wiki/%F0%9F%A6%AA" class="mw-redirect" title="🦪">🦪</a>
</td>
<td title="U+1F9AB: BEAVER"><a href="/wiki/%F0%9F%A6%AB" class="mw-redirect" title="🦫">🦫</a>
</td>
<td title="U+1F9AC: BISON"><a href="/wiki/%F0%9F%A6%AC" class="mw-redirect" title="🦬">🦬</a>
</td>
<td title="U+1F9AD: SEAL"><a href="/wiki/%F0%9F%A6%AD" class="mw-redirect" title="🦭">🦭</a>
</td>
<td title="U+1F9AE: GUIDE DOG"><a href="/wiki/%F0%9F%A6%AE" class="mw-redirect" title="🦮">🦮</a>
</td>
<td title="U+1F9AF: PROBING CANE"><a href="/wiki/%F0%9F%A6%AF" class="mw-redirect" title="🦯">🦯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F9Bx
</td>
<td title="U+1F9B0: EMOJI COMPONENT RED HAIR"><a href="/wiki/%F0%9F%A6%B0" class="mw-redirect" title="🦰">🦰</a>
</td>
<td title="U+1F9B1: EMOJI COMPONENT CURLY HAIR"><a href="/wiki/%F0%9F%A6%B1" class="mw-redirect" title="🦱">🦱</a>
</td>
<td title="U+1F9B2: EMOJI COMPONENT BALD"><a href="/wiki/%F0%9F%A6%B2" class="mw-redirect" title="🦲">🦲</a>
</td>
<td title="U+1F9B3: EMOJI COMPONENT WHITE HAIR"><a href="/wiki/%F0%9F%A6%B3" class="mw-redirect" title="🦳">🦳</a>
</td>
<td title="U+1F9B4: BONE"><a href="/wiki/%F0%9F%A6%B4" class="mw-redirect" title="🦴">🦴</a>
</td>
<td title="U+1F9B5: LEG"><a href="/wiki/%F0%9F%A6%B5" class="mw-redirect" title="🦵">🦵</a>
</td>
<td title="U+1F9B6: FOOT"><a href="/wiki/%F0%9F%A6%B6" class="mw-redirect" title="🦶">🦶</a>
</td>
<td title="U+1F9B7: TOOTH"><a href="/wiki/%F0%9F%A6%B7" class="mw-redirect" title="🦷">🦷</a>
</td>
<td title="U+1F9B8: SUPERHERO"><a href="/wiki/%F0%9F%A6%B8" class="mw-redirect" title="🦸">🦸</a>
</td>
<td title="U+1F9B9: SUPERVILLAIN"><a href="/wiki/%F0%9F%A6%B9" class="mw-redirect" title="🦹">🦹</a>
</td>
<td title="U+1F9BA: SAFETY VEST"><a href="/wiki/%F0%9F%A6%BA" class="mw-redirect" title="🦺">🦺</a>
</td>
<td title="U+1F9BB: EAR WITH HEARING AID"><a href="/wiki/%F0%9F%A6%BB" class="mw-redirect" title="🦻">🦻</a>
</td>
<td title="U+1F9BC: MOTORIZED WHEELCHAIR"><a href="/wiki/%F0%9F%A6%BC" class="mw-redirect" title="🦼">🦼</a>
</td>
<td title="U+1F9BD: MANUAL WHEELCHAIR"><a href="/wiki/%F0%9F%A6%BD" class="mw-redirect" title="🦽">🦽</a>
</td>
<td title="U+1F9BE: MECHANICAL ARM"><a href="/wiki/%F0%9F%A6%BE" class="mw-redirect" title="🦾">🦾</a>
</td>
<td title="U+1F9BF: MECHANICAL LEG"><a href="/wiki/%F0%9F%A6%BF" class="mw-redirect" title="🦿">🦿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F9Cx
</td>
<td title="U+1F9C0: CHEESE WEDGE"><a href="/wiki/%F0%9F%A7%80" class="mw-redirect" title="🧀">🧀</a>
</td>
<td title="U+1F9C1: CUPCAKE"><a href="/wiki/%F0%9F%A7%81" class="mw-redirect" title="🧁">🧁</a>
</td>
<td title="U+1F9C2: SALT SHAKER"><a href="/wiki/%F0%9F%A7%82" class="mw-redirect" title="🧂">🧂</a>
</td>
<td title="U+1F9C3: BEVERAGE BOX"><a href="/wiki/%F0%9F%A7%83" class="mw-redirect" title="🧃">🧃</a>
</td>
<td title="U+1F9C4: GARLIC"><a href="/wiki/%F0%9F%A7%84" class="mw-redirect" title="🧄">🧄</a>
</td>
<td title="U+1F9C5: ONION"><a href="/wiki/%F0%9F%A7%85" class="mw-redirect" title="🧅">🧅</a>
</td>
<td title="U+1F9C6: FALAFEL"><a href="/wiki/%F0%9F%A7%86" class="mw-redirect" title="🧆">🧆</a>
</td>
<td title="U+1F9C7: WAFFLE"><a href="/wiki/%F0%9F%A7%87" class="mw-redirect" title="🧇">🧇</a>
</td>
<td title="U+1F9C8: BUTTER"><a href="/wiki/%F0%9F%A7%88" class="mw-redirect" title="🧈">🧈</a>
</td>
<td title="U+1F9C9: MATE DRINK"><a href="/wiki/%F0%9F%A7%89" class="mw-redirect" title="🧉">🧉</a>
</td>
<td title="U+1F9CA: ICE CUBE"><a href="/wiki/%F0%9F%A7%8A" class="mw-redirect" title="🧊">🧊</a>
</td>
<td title="U+1F9CB: BUBBLE TEA"><a href="/wiki/%F0%9F%A7%8B" class="mw-redirect" title="🧋">🧋</a>
</td>
<td title="U+1F9CC: TROLL"><a href="/wiki/%F0%9F%A7%8C" class="mw-redirect" title="🧌">🧌</a>
</td>
<td title="U+1F9CD: STANDING PERSON"><a href="/wiki/%F0%9F%A7%8D" class="mw-redirect" title="🧍">🧍</a>
</td>
<td title="U+1F9CE: KNEELING PERSON"><a href="/wiki/%F0%9F%A7%8E" class="mw-redirect" title="🧎">🧎</a>
</td>
<td title="U+1F9CF: DEAF PERSON"><a href="/wiki/%F0%9F%A7%8F" class="mw-redirect" title="🧏">🧏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F9Dx
</td>
<td title="U+1F9D0: FACE WITH MONOCLE"><a href="/wiki/%F0%9F%A7%90" class="mw-redirect" title="🧐">🧐</a>
</td>
<td title="U+1F9D1: ADULT"><a href="/wiki/%F0%9F%A7%91" class="mw-redirect" title="🧑">🧑</a>
</td>
<td title="U+1F9D2: CHILD"><a href="/wiki/%F0%9F%A7%92" class="mw-redirect" title="🧒">🧒</a>
</td>
<td title="U+1F9D3: OLDER ADULT"><a href="/wiki/%F0%9F%A7%93" class="mw-redirect" title="🧓">🧓</a>
</td>
<td title="U+1F9D4: BEARDED PERSON"><a href="/wiki/%F0%9F%A7%94" class="mw-redirect" title="🧔">🧔</a>
</td>
<td title="U+1F9D5: PERSON WITH HEADSCARF"><a href="/wiki/%F0%9F%A7%95" class="mw-redirect" title="🧕">🧕</a>
</td>
<td title="U+1F9D6: PERSON IN STEAMY ROOM"><a href="/wiki/%F0%9F%A7%96" class="mw-redirect" title="🧖">🧖</a>
</td>
<td title="U+1F9D7: PERSON CLIMBING"><a href="/wiki/%F0%9F%A7%97" class="mw-redirect" title="🧗">🧗</a>
</td>
<td title="U+1F9D8: PERSON IN LOTUS POSITION"><a href="/wiki/%F0%9F%A7%98" class="mw-redirect" title="🧘">🧘</a>
</td>
<td title="U+1F9D9: MAGE"><a href="/wiki/%F0%9F%A7%99" class="mw-redirect" title="🧙">🧙</a>
</td>
<td title="U+1F9DA: FAIRY"><a href="/wiki/%F0%9F%A7%9A" class="mw-redirect" title="🧚">🧚</a>
</td>
<td title="U+1F9DB: VAMPIRE"><a href="/wiki/%F0%9F%A7%9B" class="mw-redirect" title="🧛">🧛</a>
</td>
<td title="U+1F9DC: MERPERSON"><a href="/wiki/Merfolk" title="Merfolk">🧜</a>
</td>
<td title="U+1F9DD: ELF"><a href="/wiki/%F0%9F%A7%9D" class="mw-redirect" title="🧝">🧝</a>
</td>
<td title="U+1F9DE: GENIE"><a href="/wiki/%F0%9F%A7%9E" class="mw-redirect" title="🧞">🧞</a>
</td>
<td title="U+1F9DF: ZOMBIE"><a href="/wiki/%F0%9F%A7%9F" class="mw-redirect" title="🧟">🧟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F9Ex
</td>
<td title="U+1F9E0: BRAIN"><a href="/wiki/%F0%9F%A7%A0" class="mw-redirect" title="🧠">🧠</a>
</td>
<td title="U+1F9E1: ORANGE HEART"><a href="/wiki/%F0%9F%A7%A1" class="mw-redirect" title="🧡">🧡</a>
</td>
<td title="U+1F9E2: BILLED CAP"><a href="/wiki/%F0%9F%A7%A2" class="mw-redirect" title="🧢">🧢</a>
</td>
<td title="U+1F9E3: SCARF"><a href="/wiki/%F0%9F%A7%A3" class="mw-redirect" title="🧣">🧣</a>
</td>
<td title="U+1F9E4: GLOVES"><a href="/wiki/%F0%9F%A7%A4" class="mw-redirect" title="🧤">🧤</a>
</td>
<td title="U+1F9E5: COAT"><a href="/wiki/%F0%9F%A7%A5" class="mw-redirect" title="🧥">🧥</a>
</td>
<td title="U+1F9E6: SOCKS"><a href="/wiki/%F0%9F%A7%A6" class="mw-redirect" title="🧦">🧦</a>
</td>
<td title="U+1F9E7: RED GIFT ENVELOPE"><a href="/wiki/%F0%9F%A7%A7" class="mw-redirect" title="🧧">🧧</a>
</td>
<td title="U+1F9E8: FIRECRACKER"><a href="/wiki/%F0%9F%A7%A8" class="mw-redirect" title="🧨">🧨</a>
</td>
<td title="U+1F9E9: JIGSAW PUZZLE PIECE"><a href="/wiki/%F0%9F%A7%A9" class="mw-redirect" title="🧩">🧩</a>
</td>
<td title="U+1F9EA: TEST TUBE"><a href="/wiki/%F0%9F%A7%AA" class="mw-redirect" title="🧪">🧪</a>
</td>
<td title="U+1F9EB: PETRI DISH"><a href="/wiki/%F0%9F%A7%AB" class="mw-redirect" title="🧫">🧫</a>
</td>
<td title="U+1F9EC: DNA DOUBLE HELIX"><a href="/wiki/%F0%9F%A7%AC" class="mw-redirect" title="🧬">🧬</a>
</td>
<td title="U+1F9ED: COMPASS"><a href="/wiki/%F0%9F%A7%AD" class="mw-redirect" title="🧭">🧭</a>
</td>
<td title="U+1F9EE: ABACUS"><a href="/wiki/%F0%9F%A7%AE" class="mw-redirect" title="🧮">🧮</a>
</td>
<td title="U+1F9EF: FIRE EXTINGUISHER"><a href="/wiki/%F0%9F%A7%AF" class="mw-redirect" title="🧯">🧯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1F9Fx
</td>
<td title="U+1F9F0: TOOLBOX"><a href="/wiki/%F0%9F%A7%B0" class="mw-redirect" title="🧰">🧰</a>
</td>
<td title="U+1F9F1: BRICK"><a href="/wiki/%F0%9F%A7%B1" class="mw-redirect" title="🧱">🧱</a>
</td>
<td title="U+1F9F2: MAGNET"><a href="/wiki/%F0%9F%A7%B2" class="mw-redirect" title="🧲">🧲</a>
</td>
<td title="U+1F9F3: LUGGAGE"><a href="/wiki/%F0%9F%A7%B3" class="mw-redirect" title="🧳">🧳</a>
</td>
<td title="U+1F9F4: LOTION BOTTLE"><a href="/wiki/%F0%9F%A7%B4" class="mw-redirect" title="🧴">🧴</a>
</td>
<td title="U+1F9F5: SPOOL OF THREAD"><a href="/wiki/%F0%9F%A7%B5" class="mw-redirect" title="🧵">🧵</a>
</td>
<td title="U+1F9F6: BALL OF YARN"><a href="/wiki/%F0%9F%A7%B6" class="mw-redirect" title="🧶">🧶</a>
</td>
<td title="U+1F9F7: SAFETY PIN"><a href="/wiki/%F0%9F%A7%B7" class="mw-redirect" title="🧷">🧷</a>
</td>
<td title="U+1F9F8: TEDDY BEAR"><a href="/wiki/%F0%9F%A7%B8" class="mw-redirect" title="🧸">🧸</a>
</td>
<td title="U+1F9F9: BROOM"><a href="/wiki/%F0%9F%A7%B9" class="mw-redirect" title="🧹">🧹</a>
</td>
<td title="U+1F9FA: BASKET"><a href="/wiki/%F0%9F%A7%BA" class="mw-redirect" title="🧺">🧺</a>
</td>
<td title="U+1F9FB: ROLL OF PAPER"><a href="/wiki/%F0%9F%A7%BB" class="mw-redirect" title="🧻">🧻</a>
</td>
<td title="U+1F9FC: BAR OF SOAP"><a href="/wiki/%F0%9F%A7%BC" class="mw-redirect" title="🧼">🧼</a>
</td>
<td title="U+1F9FD: SPONGE"><a href="/wiki/%F0%9F%A7%BD" class="mw-redirect" title="🧽">🧽</a>
</td>
<td title="U+1F9FE: RECEIPT"><a href="/wiki/%F0%9F%A7%BE" class="mw-redirect" title="🧾">🧾</a>
</td>
<td title="U+1F9FF: NAZAR AMULET"><a href="/wiki/%F0%9F%A7%BF" class="mw-redirect" title="🧿">🧿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FA7x
</td>
<td title="U+1FA70: BALLET SHOES"><a href="/wiki/%F0%9F%A9%B0" class="mw-redirect" title="🩰">🩰</a>
</td>
<td title="U+1FA71: ONE-PIECE SWIMSUIT"><a href="/wiki/%F0%9F%A9%B1" class="mw-redirect" title="🩱">🩱</a>
</td>
<td title="U+1FA72: BRIEFS"><a href="/wiki/%F0%9F%A9%B2" class="mw-redirect" title="🩲">🩲</a>
</td>
<td title="U+1FA73: SHORTS"><a href="/wiki/%F0%9F%A9%B3" class="mw-redirect" title="🩳">🩳</a>
</td>
<td title="U+1FA74: THONG SANDAL"><a href="/wiki/%F0%9F%A9%B4" class="mw-redirect" title="🩴">🩴</a>
</td>
<td title="U+1FA75: LIGHT BLUE HEART"><a href="/wiki/%F0%9F%A9%B5" class="mw-redirect" title="🩵">🩵</a>
</td>
<td title="U+1FA76: GREY HEART"><a href="/wiki/%F0%9F%A9%B6" class="mw-redirect" title="🩶">🩶</a>
</td>
<td title="U+1FA77: PINK HEART"><a href="/wiki/%F0%9F%A9%B7" class="mw-redirect" title="🩷">🩷</a>
</td>
<td title="U+1FA78: DROP OF BLOOD"><a href="/wiki/%F0%9F%A9%B8" class="mw-redirect" title="🩸">🩸</a>
</td>
<td title="U+1FA79: ADHESIVE BANDAGE"><a href="/wiki/%F0%9F%A9%B9" class="mw-redirect" title="🩹">🩹</a>
</td>
<td title="U+1FA7A: STETHOSCOPE"><a href="/wiki/%F0%9F%A9%BA" class="mw-redirect" title="🩺">🩺</a>
</td>
<td title="U+1FA7B: X-RAY"><a href="/wiki/%F0%9F%A9%BB" class="mw-redirect" title="🩻">🩻</a>
</td>
<td title="U+1FA7C: CRUTCH"><a href="/wiki/%F0%9F%A9%BC" class="mw-redirect" title="🩼">🩼</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FA8x
</td>
<td title="U+1FA80: YO-YO"><a href="/wiki/%F0%9F%AA%80" class="mw-redirect" title="🪀">🪀</a>
</td>
<td title="U+1FA81: KITE"><a href="/wiki/%F0%9F%AA%81" class="mw-redirect" title="🪁">🪁</a>
</td>
<td title="U+1FA82: PARACHUTE"><a href="/wiki/%F0%9F%AA%82" class="mw-redirect" title="🪂">🪂</a>
</td>
<td title="U+1FA83: BOOMERANG"><a href="/wiki/%F0%9F%AA%83" class="mw-redirect" title="🪃">🪃</a>
</td>
<td title="U+1FA84: MAGIC WAND"><a href="/wiki/%F0%9F%AA%84" class="mw-redirect" title="🪄">🪄</a>
</td>
<td title="U+1FA85: PINATA"><a href="/wiki/%F0%9F%AA%85" class="mw-redirect" title="🪅">🪅</a>
</td>
<td title="U+1FA86: NESTING DOLLS"><a href="/wiki/%F0%9F%AA%86" class="mw-redirect" title="🪆">🪆</a>
</td>
<td title="U+1FA87: MARACAS"><a href="/wiki/%F0%9F%AA%87" class="mw-redirect" title="🪇">🪇</a>
</td>
<td title="U+1FA88: FLUTE"><a href="/wiki/%F0%9F%AA%88" class="mw-redirect" title="🪈">🪈</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FA9x
</td>
<td title="U+1FA90: RINGED PLANET"><a href="/wiki/%F0%9F%AA%90" class="mw-redirect" title="🪐">🪐</a>
</td>
<td title="U+1FA91: CHAIR"><a href="/wiki/%F0%9F%AA%91" class="mw-redirect" title="🪑">🪑</a>
</td>
<td title="U+1FA92: RAZOR"><a href="/wiki/%F0%9F%AA%92" class="mw-redirect" title="🪒">🪒</a>
</td>
<td title="U+1FA93: AXE"><a href="/wiki/%F0%9F%AA%93" class="mw-redirect" title="🪓">🪓</a>
</td>
<td title="U+1FA94: DIYA LAMP"><a href="/wiki/%F0%9F%AA%94" class="mw-redirect" title="🪔">🪔</a>
</td>
<td title="U+1FA95: BANJO"><a href="/wiki/%F0%9F%AA%95" class="mw-redirect" title="🪕">🪕</a>
</td>
<td title="U+1FA96: MILITARY HELMET"><a href="/wiki/%F0%9F%AA%96" class="mw-redirect" title="🪖">🪖</a>
</td>
<td title="U+1FA97: ACCORDION"><a href="/wiki/%F0%9F%AA%97" class="mw-redirect" title="🪗">🪗</a>
</td>
<td title="U+1FA98: LONG DRUM"><a href="/wiki/%F0%9F%AA%98" class="mw-redirect" title="🪘">🪘</a>
</td>
<td title="U+1FA99: COIN"><a href="/wiki/%F0%9F%AA%99" class="mw-redirect" title="🪙">🪙</a>
</td>
<td title="U+1FA9A: CARPENTRY SAW"><a href="/wiki/%F0%9F%AA%9A" class="mw-redirect" title="🪚">🪚</a>
</td>
<td title="U+1FA9B: SCREWDRIVER"><a href="/wiki/%F0%9F%AA%9B" class="mw-redirect" title="🪛">🪛</a>
</td>
<td title="U+1FA9C: LADDER"><a href="/wiki/%F0%9F%AA%9C" class="mw-redirect" title="🪜">🪜</a>
</td>
<td title="U+1FA9D: HOOK"><a href="/wiki/%F0%9F%AA%9D" class="mw-redirect" title="🪝">🪝</a>
</td>
<td title="U+1FA9E: MIRROR"><a href="/wiki/%F0%9F%AA%9E" class="mw-redirect" title="🪞">🪞</a>
</td>
<td title="U+1FA9F: WINDOW"><a href="/wiki/%F0%9F%AA%9F" class="mw-redirect" title="🪟">🪟</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FAAx
</td>
<td title="U+1FAA0: PLUNGER"><a href="/wiki/%F0%9F%AA%A0" class="mw-redirect" title="🪠">🪠</a>
</td>
<td title="U+1FAA1: SEWING NEEDLE"><a href="/wiki/%F0%9F%AA%A1" class="mw-redirect" title="🪡">🪡</a>
</td>
<td title="U+1FAA2: KNOT"><a href="/wiki/%F0%9F%AA%A2" class="mw-redirect" title="🪢">🪢</a>
</td>
<td title="U+1FAA3: BUCKET"><a href="/wiki/%F0%9F%AA%A3" class="mw-redirect" title="🪣">🪣</a>
</td>
<td title="U+1FAA4: MOUSE TRAP"><a href="/wiki/%F0%9F%AA%A4" class="mw-redirect" title="🪤">🪤</a>
</td>
<td title="U+1FAA5: TOOTHBRUSH"><a href="/wiki/%F0%9F%AA%A5" class="mw-redirect" title="🪥">🪥</a>
</td>
<td title="U+1FAA6: HEADSTONE"><a href="/wiki/%F0%9F%AA%A6" class="mw-redirect" title="🪦">🪦</a>
</td>
<td title="U+1FAA7: PLACARD"><a href="/wiki/%F0%9F%AA%A7" class="mw-redirect" title="🪧">🪧</a>
</td>
<td title="U+1FAA8: ROCK"><a href="/wiki/%F0%9F%AA%A8" class="mw-redirect" title="🪨">🪨</a>
</td>
<td title="U+1FAA9: MIRROR BALL"><a href="/wiki/%F0%9F%AA%A9" class="mw-redirect" title="🪩">🪩</a>
</td>
<td title="U+1FAAA: IDENTIFICATION CARD"><a href="/wiki/%F0%9F%AA%AA" class="mw-redirect" title="🪪">🪪</a>
</td>
<td title="U+1FAAB: LOW BATTERY"><a href="/wiki/%F0%9F%AA%AB" class="mw-redirect" title="🪫">🪫</a>
</td>
<td title="U+1FAAC: HAMSA"><a href="/wiki/%F0%9F%AA%AC" class="mw-redirect" title="🪬">🪬</a>
</td>
<td title="U+1FAAD: FOLDING HAND FAN"><a href="/wiki/%F0%9F%AA%AD" class="mw-redirect" title="🪭">🪭</a>
</td>
<td title="U+1FAAE: HAIR PICK"><a href="/wiki/%F0%9F%AA%AE" class="mw-redirect" title="🪮">🪮</a>
</td>
<td title="U+1FAAF: KHANDA"><a href="/wiki/%F0%9F%AA%AF" class="mw-redirect" title="🪯">🪯</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FABx
</td>
<td title="U+1FAB0: FLY"><a href="/wiki/%F0%9F%AA%B0" class="mw-redirect" title="🪰">🪰</a>
</td>
<td title="U+1FAB1: WORM"><a href="/wiki/%F0%9F%AA%B1" class="mw-redirect" title="🪱">🪱</a>
</td>
<td title="U+1FAB2: BEETLE"><a href="/wiki/%F0%9F%AA%B2" class="mw-redirect" title="🪲">🪲</a>
</td>
<td title="U+1FAB3: COCKROACH"><a href="/wiki/%F0%9F%AA%B3" class="mw-redirect" title="🪳">🪳</a>
</td>
<td title="U+1FAB4: POTTED PLANT"><a href="/wiki/%F0%9F%AA%B4" class="mw-redirect" title="🪴">🪴</a>
</td>
<td title="U+1FAB5: WOOD"><a href="/wiki/%F0%9F%AA%B5" class="mw-redirect" title="🪵">🪵</a>
</td>
<td title="U+1FAB6: FEATHER"><a href="/wiki/%F0%9F%AA%B6" class="mw-redirect" title="🪶">🪶</a>
</td>
<td title="U+1FAB7: LOTUS"><a href="/wiki/%F0%9F%AA%B7" class="mw-redirect" title="🪷">🪷</a>
</td>
<td title="U+1FAB8: CORAL"><a href="/wiki/%F0%9F%AA%B8" class="mw-redirect" title="🪸">🪸</a>
</td>
<td title="U+1FAB9: EMPTY NEST"><a href="/wiki/%F0%9F%AA%B9" class="mw-redirect" title="🪹">🪹</a>
</td>
<td title="U+1FABA: NEST WITH EGGS"><a href="/wiki/%F0%9F%AA%BA" class="mw-redirect" title="🪺">🪺</a>
</td>
<td title="U+1FABB: HYACINTH"><a href="/wiki/%F0%9F%AA%BB" class="mw-redirect" title="🪻">🪻</a>
</td>
<td title="U+1FABC: JELLYFISH"><a href="/wiki/%F0%9F%AA%BC" class="mw-redirect" title="🪼">🪼</a>
</td>
<td title="U+1FABD: WING"><a href="/wiki/%F0%9F%AA%BD" class="mw-redirect" title="🪽">🪽</a>
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1FABF: GOOSE"><a href="/wiki/%F0%9F%AA%BF" class="mw-redirect" title="🪿">🪿</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FACx
</td>
<td title="U+1FAC0: ANATOMICAL HEART"><a href="/wiki/%F0%9F%AB%80" class="mw-redirect" title="🫀">🫀</a>
</td>
<td title="U+1FAC1: LUNGS"><a href="/wiki/%F0%9F%AB%81" class="mw-redirect" title="🫁">🫁</a>
</td>
<td title="U+1FAC2: PEOPLE HUGGING"><a href="/wiki/%F0%9F%AB%82" class="mw-redirect" title="🫂">🫂</a>
</td>
<td title="U+1FAC3: PREGNANT MAN"><a href="/wiki/%F0%9F%AB%83" class="mw-redirect" title="🫃">🫃</a>
</td>
<td title="U+1FAC4: PREGNANT PERSON"><a href="/wiki/%F0%9F%AB%84" class="mw-redirect" title="🫄">🫄</a>
</td>
<td title="U+1FAC5: PERSON WITH CROWN"><a href="/wiki/%F0%9F%AB%85" class="mw-redirect" title="🫅">🫅</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td title="U+1FACE: MOOSE"><a href="/wiki/%F0%9F%AB%8E" class="mw-redirect" title="🫎">🫎</a>
</td>
<td title="U+1FACF: DONKEY"><a href="/wiki/%F0%9F%AB%8F" class="mw-redirect" title="🫏">🫏</a>
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FADx
</td>
<td title="U+1FAD0: BLUEBERRIES"><a href="/wiki/%F0%9F%AB%90" class="mw-redirect" title="🫐">🫐</a>
</td>
<td title="U+1FAD1: BELL PEPPER"><a href="/wiki/%F0%9F%AB%91" class="mw-redirect" title="🫑">🫑</a>
</td>
<td title="U+1FAD2: OLIVE"><a href="/wiki/%F0%9F%AB%92" class="mw-redirect" title="🫒">🫒</a>
</td>
<td title="U+1FAD3: FLATBREAD"><a href="/wiki/%F0%9F%AB%93" class="mw-redirect" title="🫓">🫓</a>
</td>
<td title="U+1FAD4: TAMALE"><a href="/wiki/%F0%9F%AB%94" class="mw-redirect" title="🫔">🫔</a>
</td>
<td title="U+1FAD5: FONDUE"><a href="/wiki/%F0%9F%AB%95" class="mw-redirect" title="🫕">🫕</a>
</td>
<td title="U+1FAD6: TEAPOT"><a href="/wiki/%F0%9F%AB%96" class="mw-redirect" title="🫖">🫖</a>
</td>
<td title="U+1FAD7: POURING LIQUID"><a href="/w/index.php?title=%F0%9F%AB%97&amp;action=edit&amp;redlink=1" class="new" title="🫗 (page does not exist)">🫗</a>
</td>
<td title="U+1FAD8: BEANS"><a href="/wiki/%F0%9F%AB%98" class="mw-redirect" title="🫘">🫘</a>
</td>
<td title="U+1FAD9: JAR"><a href="/wiki/%F0%9F%AB%99" class="mw-redirect" title="🫙">🫙</a>
</td>
<td title="U+1FADA: GINGER ROOT"><a href="/wiki/%F0%9F%AB%9A" class="mw-redirect" title="🫚">🫚</a>
</td>
<td title="U+1FADB: PEA POD"><a href="/wiki/%F0%9F%AB%9B" class="mw-redirect" title="🫛">🫛</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FAEx
</td>
<td title="U+1FAE0: MELTING FACE"><a href="/wiki/%F0%9F%AB%A0" class="mw-redirect" title="🫠">🫠</a>
</td>
<td title="U+1FAE1: SALUTING FACE"><a href="/wiki/%F0%9F%AB%A1" class="mw-redirect" title="🫡">🫡</a>
</td>
<td title="U+1FAE2: FACE WITH OPEN EYES AND HAND OVER MOUTH"><a href="/wiki/%F0%9F%AB%A2" class="mw-redirect" title="🫢">🫢</a>
</td>
<td title="U+1FAE3: FACE WITH PEEKING EYE"><a href="/wiki/%F0%9F%AB%A3" class="mw-redirect" title="🫣">🫣</a>
</td>
<td title="U+1FAE4: FACE WITH DIAGONAL MOUTH"><a href="/wiki/%F0%9F%AB%A4" class="mw-redirect" title="🫤">🫤</a>
</td>
<td title="U+1FAE5: DOTTED LINE FACE"><a href="/wiki/%F0%9F%AB%A5" class="mw-redirect" title="🫥">🫥</a>
</td>
<td title="U+1FAE6: BITING LIP"><a href="/wiki/%F0%9F%AB%A6" class="mw-redirect" title="🫦">🫦</a>
</td>
<td title="U+1FAE7: BUBBLES"><a href="/wiki/%F0%9F%AB%A7" class="mw-redirect" title="🫧">🫧</a>
</td>
<td title="U+1FAE8: SHAKING FACE"><a href="/w/index.php?title=%F0%9F%AB%A8&amp;action=edit&amp;redlink=1" class="new" title="🫨 (page does not exist)">🫨</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr>
<td style="background:#F8F8F8;font-size:small;font-family:sans-serif">U+1FAFx
</td>
<td title="U+1FAF0: HAND WITH INDEX FINGER AND THUMB CROSSED"><a href="/wiki/%F0%9F%AB%B0" class="mw-redirect" title="🫰">🫰</a>
</td>
<td title="U+1FAF1: RIGHTWARDS HAND"><a href="/w/index.php?title=%F0%9F%AB%B1&amp;action=edit&amp;redlink=1" class="new" title="🫱 (page does not exist)">🫱</a>
</td>
<td title="U+1FAF2: LEFTWARDS HAND"><a href="/w/index.php?title=%F0%9F%AB%B2&amp;action=edit&amp;redlink=1" class="new" title="🫲 (page does not exist)">🫲</a>
</td>
<td title="U+1FAF3: PALM DOWN HAND"><a href="/w/index.php?title=%F0%9F%AB%B3&amp;action=edit&amp;redlink=1" class="new" title="🫳 (page does not exist)">🫳</a>
</td>
<td title="U+1FAF4: PALM UP HAND"><a href="/w/index.php?title=%F0%9F%AB%B4&amp;action=edit&amp;redlink=1" class="new" title="🫴 (page does not exist)">🫴</a>
</td>
<td title="U+1FAF5: INDEX POINTING AT THE VIEWER"><a href="/wiki/%F0%9F%AB%B5" class="mw-redirect" title="🫵">🫵</a>
</td>
<td title="U+1FAF6: HEART HANDS"><a href="/wiki/%F0%9F%AB%B6" class="mw-redirect" title="🫶">🫶</a>
</td>
<td title="U+1FAF7: LEFTWARDS PUSHING HAND"><a href="/w/index.php?title=%F0%9F%AB%B7&amp;action=edit&amp;redlink=1" class="new" title="🫷 (page does not exist)">🫷</a>
</td>
<td title="U+1FAF8: RIGHTWARDS PUSHING HAND"><a href="/w/index.php?title=%F0%9F%AB%B8&amp;action=edit&amp;redlink=1" class="new" title="🫸 (page does not exist)">🫸</a>
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td>
<td style="background-color:#CCC">
</td></tr>
<tr style="background:#F8F8F8;font-size:small;font-family:sans-serif">
<td style="width:45pt">&nbsp;</td>
<td style="width:20pt">0</td>
<td style="width:20pt">1</td>
<td style="width:20pt">2</td>
<td style="width:20pt">3</td>
<td style="width:20pt">4</td>
<td style="width:20pt">5</td>
<td style="width:20pt">6</td>
<td style="width:20pt">7</td>
<td style="width:20pt">8</td>
<td style="width:20pt">9</td>
<td style="width:20pt">A</td>
<td style="width:20pt">B</td>
<td style="width:20pt">C</td>
<td style="width:20pt">D</td>
<td style="width:20pt">E</td>
<td style="width:20pt">F
</td></tr>
<tr style="font-family:sans-serif">
<td colspan="17" style="background:#F8F8F8;font-size:small;text-align:left">
</td></tr></tbody></table>
  </div>
</div>
</template>

<script>
var sList = `
2194..2199    ; Emoji                #   [6] (↔️..↙️)  LEFT RIGHT ARROW..SOUTH WEST ARROW
21A9..21AA    ; Emoji                #   [2] (↩️..↪️)  LEFTWARDS ARROW WITH HOOK..RIGHTWARDS ARROW WITH HOOK
231A..231B    ; Emoji                #   [2] (⌚️..⌛️)  WATCH..HOURGLASS
23E9..23F3    ; Emoji                #  [11] (⏩..⏳)    BLACK RIGHT-POINTING DOUBLE TRIANGLE..HOURGLASS WITH FLOWING SAND
24C2          ; Emoji                #   [1] (Ⓜ️)      CIRCLED LATIN CAPITAL LETTER M
25AA..25AB    ; Emoji                #   [2] (▪️..▫️)  BLACK SMALL SQUARE..WHITE SMALL SQUARE
25B6          ; Emoji                #   [1] (▶️)      BLACK RIGHT-POINTING TRIANGLE
25C0          ; Emoji                #   [1] (◀️)      BLACK LEFT-POINTING TRIANGLE
25FB..25FE    ; Emoji                #   [4] (◻️..◾️)  WHITE MEDIUM SQUARE..BLACK MEDIUM SMALL SQUARE
26AA..26AB    ; Emoji                #   [2] (⚪️..⚫️)  MEDIUM WHITE CIRCLE..MEDIUM BLACK CIRCLE
26BD..26BE    ; Emoji                #   [2] (⚽️..⚾️)  SOCCER BALL..BASEBALL
26C4..26C5    ; Emoji                #   [2] (⛄️..⛅️)  SNOWMAN WITHOUT SNOW..SUN BEHIND CLOUD
26C8          ; Emoji                #   [1] (⛈)       THUNDER CLOUD AND RAIN
26CE..26CF    ; Emoji                #   [2] (⛎..⛏)    OPHIUCHUS..PICK
26D1          ; Emoji                #   [1] (⛑)       HELMET WITH WHITE CROSS
26D3..26D4    ; Emoji                #   [2] (⛓..⛔️)   CHAINS..NO ENTRY
26E9..26EA    ; Emoji                #   [2] (⛩..⛪️)   SHINTO SHRINE..CHURCH
26F0..26F5    ; Emoji                #   [6] (⛰..⛵️)   MOUNTAIN..SAILBOAT
26F7..26FA    ; Emoji                #   [4] (⛷..⛺️)   SKIER..TENT
26FD          ; Emoji                #   [1] (⛽️)      FUEL PUMP
2705          ; Emoji                #   [1] (✅)       WHITE HEAVY CHECK MARK
2728          ; Emoji                #   [1] (✨)       SPARKLES
274C          ; Emoji                #   [1] (❌)       CROSS MARK
274E          ; Emoji                #   [1] (❎)       NEGATIVE SQUARED CROSS MARK
2753..2755    ; Emoji                #   [3] (❓..❕)    BLACK QUESTION MARK ORNAMENT..WHITE EXCLAMATION MARK ORNAMENT
2757          ; Emoji                #   [1] (❗️)      HEAVY EXCLAMATION MARK SYMBOL
2763..2764    ; Emoji                #   [2] (❣..❤️)   HEAVY HEART EXCLAMATION MARK ORNAMENT..HEAVY BLACK HEART
2795..2797    ; Emoji                #   [3] (➕..➗)    HEAVY PLUS SIGN..HEAVY DIVISION SIGN
27A1          ; Emoji                #   [1] (➡️)      BLACK RIGHTWARDS ARROW
27B0          ; Emoji                #   [1] (➰)       CURLY LOOP
27BF          ; Emoji                #   [1] (➿)       DOUBLE CURLY LOOP
2934..2935    ; Emoji                #   [2] (⤴️..⤵️)  ARROW POINTING RIGHTWARDS THEN CURVING UPWARDS..ARROW POINTING RIGHTWARDS THEN CURVING DOWNWARDS
2B05..2B07    ; Emoji                #   [3] (⬅️..⬇️)  LEFTWARDS BLACK ARROW..DOWNWARDS BLACK ARROW
2B1B..2B1C    ; Emoji                #   [2] (⬛️..⬜️)  BLACK LARGE SQUARE..WHITE LARGE SQUARE
2B50          ; Emoji                #   [1] (⭐️)      WHITE MEDIUM STAR
2B55          ; Emoji                #   [1] (⭕️)      HEAVY LARGE CIRCLE
3030          ; Emoji                #   [1] (〰️)      WAVY DASH
303D          ; Emoji                #   [1] (〽️)      PART ALTERNATION MARK
3297          ; Emoji                #   [1] (㊗️)      CIRCLED IDEOGRAPH CONGRATULATION
3299          ; Emoji                #   [1] (㊙️)      CIRCLED IDEOGRAPH SECRET
1F004         ; Emoji                #   [1] (🀄️)      MAHJONG TILE RED DRAGON
1F0CF         ; Emoji                #   [1] (🃏)       PLAYING CARD BLACK JOKER
1F170..1F171  ; Emoji                #   [2] (🅰️..🅱️)  NEGATIVE SQUARED LATIN CAPITAL LETTER A..NEGATIVE SQUARED LATIN CAPITAL LETTER B
1F17E..1F17F  ; Emoji                #   [2] (🅾️..🅿️)  NEGATIVE SQUARED LATIN CAPITAL LETTER O..NEGATIVE SQUARED LATIN CAPITAL LETTER P
1F18E         ; Emoji                #   [1] (🆎)       NEGATIVE SQUARED AB
1F191..1F19A  ; Emoji                #  [10] (🆑..🆚)    SQUARED CL..SQUARED VS
1F1E6..1F1FF  ; Emoji                #  [26] (🇦..🇿)    REGIONAL INDICATOR SYMBOL LETTER A..REGIONAL INDICATOR SYMBOL LETTER Z
1F201..1F202  ; Emoji                #   [2] (🈁..🈂️)   SQUARED KATAKANA KOKO..SQUARED KATAKANA SA
1F21A         ; Emoji                #   [1] (🈚️)      SQUARED CJK UNIFIED IDEOGRAPH-7121
1F22F         ; Emoji                #   [1] (🈯️)      SQUARED CJK UNIFIED IDEOGRAPH-6307
1F232..1F23A  ; Emoji                #   [9] (🈲..🈺)    SQUARED CJK UNIFIED IDEOGRAPH-7981..SQUARED CJK UNIFIED IDEOGRAPH-55B6
1F250..1F251  ; Emoji                #   [2] (🉐..🉑)    CIRCLED IDEOGRAPH ADVANTAGE..CIRCLED IDEOGRAPH ACCEPT
1F300..1F321  ; Emoji                #  [34] (🌀..🌡)    CYCLONE..THERMOMETER
1F324..1F393  ; Emoji                # [112] (🌤..🎓)    WHITE SUN WITH SMALL CLOUD..GRADUATION CAP
1F396..1F397  ; Emoji                #   [2] (🎖..🎗)    MILITARY MEDAL..REMINDER RIBBON
1F399..1F39B  ; Emoji                #   [3] (🎙..🎛)    STUDIO MICROPHONE..CONTROL KNOBS
1F39E..1F3F0  ; Emoji                #  [83] (🎞..🏰)    FILM FRAMES..EUROPEAN CASTLE
1F3F3..1F3F5  ; Emoji                #   [3] (🏳..🏵)    WAVING WHITE FLAG..ROSETTE
1F3F7..1F4FD  ; Emoji                # [263] (🏷..📽)    LABEL..FILM PROJECTOR
1F4FF..1F53D  ; Emoji                #  [63] (📿..🔽)    PRAYER BEADS..DOWN-POINTING SMALL RED TRIANGLE
1F549..1F54E  ; Emoji                #   [6] (🕉..🕎)    OM SYMBOL..MENORAH WITH NINE BRANCHES
1F550..1F567  ; Emoji                #  [24] (🕐..🕧)    CLOCK FACE ONE OCLOCK..CLOCK FACE TWELVE-THIRTY
1F56F..1F570  ; Emoji                #   [2] (🕯..🕰)    CANDLE..MANTELPIECE CLOCK
1F573..1F579  ; Emoji                #   [7] (🕳..🕹)    HOLE..JOYSTICK
1F587         ; Emoji                #   [1] (🖇)       LINKED PAPERCLIPS
1F58A..1F58D  ; Emoji                #   [4] (🖊..🖍)    LOWER LEFT BALLPOINT PEN..LOWER LEFT CRAYON
1F590         ; Emoji                #   [1] (🖐)       RAISED HAND WITH FINGERS SPLAYED
1F595..1F596  ; Emoji                #   [2] (🖕..🖖)    REVERSED HAND WITH MIDDLE FINGER EXTENDED..RAISED HAND WITH PART BETWEEN MIDDLE AND RING FINGERS
1F5A5         ; Emoji                #   [1] (🖥)       DESKTOP COMPUTER
1F5A8         ; Emoji                #   [1] (🖨)       PRINTER
1F5B1..1F5B2  ; Emoji                #   [2] (🖱..🖲)    THREE BUTTON MOUSE..TRACKBALL
1F5BC         ; Emoji                #   [1] (🖼)       FRAME WITH PICTURE
1F5C2..1F5C4  ; Emoji                #   [3] (🗂..🗄)    CARD INDEX DIVIDERS..FILE CABINET
1F5D1..1F5D3  ; Emoji                #   [3] (🗑..🗓)    WASTEBASKET..SPIRAL CALENDAR PAD
1F5DC..1F5DE  ; Emoji                #   [3] (🗜..🗞)    COMPRESSION..ROLLED-UP NEWSPAPER
1F5E1         ; Emoji                #   [1] (🗡)       DAGGER KNIFE
1F5E3         ; Emoji                #   [1] (🗣)       SPEAKING HEAD IN SILHOUETTE
1F5E8         ; Emoji                #   [1] (🗨)       LEFT SPEECH BUBBLE
1F5EF         ; Emoji                #   [1] (🗯)       RIGHT ANGER BUBBLE
1F5F3         ; Emoji                #   [1] (🗳)       BALLOT BOX WITH BALLOT
1F5FA..1F64F  ; Emoji                #  [86] (🗺..🙏)    WORLD MAP..PERSON WITH FOLDED HANDS
1F680..1F6C5  ; Emoji                #  [70] (🚀..🛅)    ROCKET..LEFT LUGGAGE
1F6CB..1F6D0  ; Emoji                #   [6] (🛋..🛐)    COUCH AND LAMP..PLACE OF WORSHIP
1F6E0..1F6E5  ; Emoji                #   [6] (🛠..🛥)    HAMMER AND WRENCH..MOTOR BOAT
1F6E9         ; Emoji                #   [1] (🛩)       SMALL AIRPLANE
1F6EB..1F6EC  ; Emoji                #   [2] (🛫..🛬)    AIRPLANE DEPARTURE..AIRPLANE ARRIVING
1F6F0         ; Emoji                #   [1] (🛰)       SATELLITE
1F6F3         ; Emoji                #   [1] (🛳)       PASSENGER SHIP
1F910..1F918  ; Emoji                #   [9] (🤐..🤘)    ZIPPER-MOUTH FACE..SIGN OF THE HORNS
1F980..1F984  ; Emoji                #   [5] (🦀..🦄)    CRAB..UNICORN FACE
1F9C0         ; Emoji                #   [1] (🧀)       CHEESE WEDGE
231A..231B    ; Emoji_Presentation   #   [2] (⌚️..⌛️)  WATCH..HOURGLASS
23E9..23EC    ; Emoji_Presentation   #   [4] (⏩..⏬)    BLACK RIGHT-POINTING DOUBLE TRIANGLE..BLACK DOWN-POINTING DOUBLE TRIANGLE
23F0          ; Emoji_Presentation   #   [1] (⏰)       ALARM CLOCK
23F3          ; Emoji_Presentation   #   [1] (⏳)       HOURGLASS WITH FLOWING SAND
25FD..25FE    ; Emoji_Presentation   #   [2] (◽️..◾️)  WHITE MEDIUM SMALL SQUARE..BLACK MEDIUM SMALL SQUARE
2614..2615    ; Emoji_Presentation   #   [2] (☔️..☕️)  UMBRELLA WITH RAIN DROPS..HOT BEVERAGE
2648..2653    ; Emoji_Presentation   #  [12] (♈️..♓️)  ARIES..PISCES
267F          ; Emoji_Presentation   #   [1] (♿️)      WHEELCHAIR SYMBOL
2693          ; Emoji_Presentation   #   [1] (⚓️)      ANCHOR
26A1          ; Emoji_Presentation   #   [1] (⚡️)      HIGH VOLTAGE SIGN
26AA..26AB    ; Emoji_Presentation   #   [2] (⚪️..⚫️)  MEDIUM WHITE CIRCLE..MEDIUM BLACK CIRCLE
26BD..26BE    ; Emoji_Presentation   #   [2] (⚽️..⚾️)  SOCCER BALL..BASEBALL
26C4..26C5    ; Emoji_Presentation   #   [2] (⛄️..⛅️)  SNOWMAN WITHOUT SNOW..SUN BEHIND CLOUD
26CE          ; Emoji_Presentation   #   [1] (⛎)       OPHIUCHUS
26D4          ; Emoji_Presentation   #   [1] (⛔️)      NO ENTRY
26EA          ; Emoji_Presentation   #   [1] (⛪️)      CHURCH
26F2..26F3    ; Emoji_Presentation   #   [2] (⛲️..⛳️)  FOUNTAIN..FLAG IN HOLE
26F5          ; Emoji_Presentation   #   [1] (⛵️)      SAILBOAT
26FA          ; Emoji_Presentation   #   [1] (⛺️)      TENT
26FD          ; Emoji_Presentation   #   [1] (⛽️)      FUEL PUMP
2705          ; Emoji_Presentation   #   [1] (✅)       WHITE HEAVY CHECK MARK
270A..270B    ; Emoji_Presentation   #   [2] (✊..✋)    RAISED FIST..RAISED HAND
2728          ; Emoji_Presentation   #   [1] (✨)       SPARKLES
274C          ; Emoji_Presentation   #   [1] (❌)       CROSS MARK
274E          ; Emoji_Presentation   #   [1] (❎)       NEGATIVE SQUARED CROSS MARK
2753..2755    ; Emoji_Presentation   #   [3] (❓..❕)    BLACK QUESTION MARK ORNAMENT..WHITE EXCLAMATION MARK ORNAMENT
2757          ; Emoji_Presentation   #   [1] (❗️)      HEAVY EXCLAMATION MARK SYMBOL
2795..2797    ; Emoji_Presentation   #   [3] (➕..➗)    HEAVY PLUS SIGN..HEAVY DIVISION SIGN
27B0          ; Emoji_Presentation   #   [1] (➰)       CURLY LOOP
27BF          ; Emoji_Presentation   #   [1] (➿)       DOUBLE CURLY LOOP
2B1B..2B1C    ; Emoji_Presentation   #   [2] (⬛️..⬜️)  BLACK LARGE SQUARE..WHITE LARGE SQUARE
2B50          ; Emoji_Presentation   #   [1] (⭐️)      WHITE MEDIUM STAR
2B55          ; Emoji_Presentation   #   [1] (⭕️)      HEAVY LARGE CIRCLE
1F004         ; Emoji_Presentation   #   [1] (🀄️)      MAHJONG TILE RED DRAGON
1F0CF         ; Emoji_Presentation   #   [1] (🃏)       PLAYING CARD BLACK JOKER
1F18E         ; Emoji_Presentation   #   [1] (🆎)       NEGATIVE SQUARED AB
1F191..1F19A  ; Emoji_Presentation   #  [10] (🆑..🆚)    SQUARED CL..SQUARED VS
1F1E6..1F1FF  ; Emoji_Presentation   #  [26] (🇦..🇿)    REGIONAL INDICATOR SYMBOL LETTER A..REGIONAL INDICATOR SYMBOL LETTER Z
1F201         ; Emoji_Presentation   #   [1] (🈁)       SQUARED KATAKANA KOKO
1F21A         ; Emoji_Presentation   #   [1] (🈚️)      SQUARED CJK UNIFIED IDEOGRAPH-7121
1F22F         ; Emoji_Presentation   #   [1] (🈯️)      SQUARED CJK UNIFIED IDEOGRAPH-6307
1F232..1F236  ; Emoji_Presentation   #   [5] (🈲..🈶)    SQUARED CJK UNIFIED IDEOGRAPH-7981..SQUARED CJK UNIFIED IDEOGRAPH-6709
1F238..1F23A  ; Emoji_Presentation   #   [3] (🈸..🈺)    SQUARED CJK UNIFIED IDEOGRAPH-7533..SQUARED CJK UNIFIED IDEOGRAPH-55B6
1F250..1F251  ; Emoji_Presentation   #   [2] (🉐..🉑)    CIRCLED IDEOGRAPH ADVANTAGE..CIRCLED IDEOGRAPH ACCEPT
1F300..1F320  ; Emoji_Presentation   #  [33] (🌀..🌠)    CYCLONE..SHOOTING STAR
1F32D..1F335  ; Emoji_Presentation   #   [9] (🌭..🌵)    HOT DOG..CACTUS
1F337..1F37C  ; Emoji_Presentation   #  [70] (🌷..🍼)    TULIP..BABY BOTTLE
1F37E..1F393  ; Emoji_Presentation   #  [22] (🍾..🎓)    BOTTLE WITH POPPING CORK..GRADUATION CAP
1F3A0..1F3CA  ; Emoji_Presentation   #  [43] (🎠..🏊)    CAROUSEL HORSE..SWIMMER
1F3CF..1F3D3  ; Emoji_Presentation   #   [5] (🏏..🏓)    CRICKET BAT AND BALL..TABLE TENNIS PADDLE AND BALL
1F3E0..1F3F0  ; Emoji_Presentation   #  [17] (🏠..🏰)    HOUSE BUILDING..EUROPEAN CASTLE
1F3F4         ; Emoji_Presentation   #   [1] (🏴)       WAVING BLACK FLAG
1F3F8..1F43E  ; Emoji_Presentation   #  [71] (🏸..🐾)    BADMINTON RACQUET AND SHUTTLECOCK..PAW PRINTS
1F440         ; Emoji_Presentation   #   [1] (👀)       EYES
1F442..1F4FC  ; Emoji_Presentation   # [187] (👂..📼)    EAR..VIDEOCASSETTE
1F4FF..1F53D  ; Emoji_Presentation   #  [63] (📿..🔽)    PRAYER BEADS..DOWN-POINTING SMALL RED TRIANGLE
1F54B..1F54E  ; Emoji_Presentation   #   [4] (🕋..🕎)    KAABA..MENORAH WITH NINE BRANCHES
1F550..1F567  ; Emoji_Presentation   #  [24] (🕐..🕧)    CLOCK FACE ONE OCLOCK..CLOCK FACE TWELVE-THIRTY
1F595..1F596  ; Emoji_Presentation   #   [2] (🖕..🖖)    REVERSED HAND WITH MIDDLE FINGER EXTENDED..RAISED HAND WITH PART BETWEEN MIDDLE AND RING FINGERS
1F5FB..1F64F  ; Emoji_Presentation   #  [85] (🗻..🙏)    MOUNT FUJI..PERSON WITH FOLDED HANDS
1F680..1F6C5  ; Emoji_Presentation   #  [70] (🚀..🛅)    ROCKET..LEFT LUGGAGE
1F6CC         ; Emoji_Presentation   #   [1] (🛌)       SLEEPING ACCOMMODATION
1F6D0         ; Emoji_Presentation   #   [1] (🛐)       PLACE OF WORSHIP
1F6EB..1F6EC  ; Emoji_Presentation   #   [2] (🛫..🛬)    AIRPLANE DEPARTURE..AIRPLANE ARRIVING
1F910..1F918  ; Emoji_Presentation   #   [9] (🤐..🤘)    ZIPPER-MOUTH FACE..SIGN OF THE HORNS
1F980..1F984  ; Emoji_Presentation   #   [5] (🦀..🦄)    CRAB..UNICORN FACE
1F9C0         ; Emoji_Presentation   #   [1] (🧀)       CHEESE WEDGE
261D          ; Emoji_Modifier_Base  #   [1] (☝️)      WHITE UP POINTING INDEX
26F9          ; Emoji_Modifier_Base  #   [1] (⛹)       PERSON WITH BALL
270A..270D    ; Emoji_Modifier_Base  #   [4] (✊..✍)    RAISED FIST..WRITING HAND
1F385         ; Emoji_Modifier_Base  #   [1] (🎅)       FATHER CHRISTMAS
1F3C3..1F3C4  ; Emoji_Modifier_Base  #   [2] (🏃..🏄)    RUNNER..SURFER
1F3CA..1F3CB  ; Emoji_Modifier_Base  #   [2] (🏊..🏋)    SWIMMER..WEIGHT LIFTER
1F442..1F443  ; Emoji_Modifier_Base  #   [2] (👂..👃)    EAR..NOSE
1F446..1F450  ; Emoji_Modifier_Base  #  [11] (👆..👐)    WHITE UP POINTING BACKHAND INDEX..OPEN HANDS SIGN
1F466..1F469  ; Emoji_Modifier_Base  #   [4] (👦..👩)    BOY..WOMAN
1F46E         ; Emoji_Modifier_Base  #   [1] (👮)       POLICE OFFICER
1F470..1F478  ; Emoji_Modifier_Base  #   [9] (👰..👸)    BRIDE WITH VEIL..PRINCESS
1F47C         ; Emoji_Modifier_Base  #   [1] (👼)       BABY ANGEL
1F481..1F483  ; Emoji_Modifier_Base  #   [3] (💁..💃)    INFORMATION DESK PERSON..DANCER
1F485..1F487  ; Emoji_Modifier_Base  #   [3] (💅..💇)    NAIL POLISH..HAIRCUT
1F4AA         ; Emoji_Modifier_Base  #   [1] (💪)       FLEXED BICEPS
1F575         ; Emoji_Modifier_Base  #   [1] (🕵)       SLEUTH OR SPY
1F590         ; Emoji_Modifier_Base  #   [1] (🖐)       RAISED HAND WITH FINGERS SPLAYED
1F595..1F596  ; Emoji_Modifier_Base  #   [2] (🖕..🖖)    REVERSED HAND WITH MIDDLE FINGER EXTENDED..RAISED HAND WITH PART BETWEEN MIDDLE AND RING FINGERS
1F645..1F647  ; Emoji_Modifier_Base  #   [3] (🙅..🙇)    FACE WITH NO GOOD GESTURE..PERSON BOWING DEEPLY
1F64B..1F64F  ; Emoji_Modifier_Base  #   [5] (🙋..🙏)    HAPPY PERSON RAISING ONE HAND..PERSON WITH FOLDED HANDS
1F6A3         ; Emoji_Modifier_Base  #   [1] (🚣)       ROWBOAT
1F6B4..1F6B6  ; Emoji_Modifier_Base  #   [3] (🚴..🚶)    BICYCLIST..PEDESTRIAN
1F6C0         ; Emoji_Modifier_Base  #   [1] (🛀)       BATH
1F918         ; Emoji_Modifier_Base  #   [1] (🤘)       SIGN OF THE HORNS
`

var sEmojiList = `
ℹ️⌚️⌛️⏩️⏪️⏫️⏬️⏭️⏮️⏯️⏰️⏱️⏲️⏳️⏸️⏹️⏺️Ⓜ️▪️▫️▶️◀️◻️◼️◽️◾️☀️☁️☂️☃️☄️☎️☑️☔️☕️☘️☝️☠️☢️☣️☦️☪️☮️☯️☸️☹️☺️♀️♂️♈️♉️♊️♋️♌️♍️♎️♏️♐️♑️♒️♓️♟️♠️♣️♥️♦️♨️♻️♾️♿️⚒️⚓️⚔️⚕️⚖️⚗️⚙️⚛️⚜️⚠️⚡️⚧️⚪️⚫️⚰️⚱️⚽️⚾️⛄️⛅️⛈️⛎️⛏️⛑️⛓️⛔️⛩️⛪️⛰️⛱️⛲️⛳️⛴️⛵️⛷️⛸️⛹️⛺️⛽️✂️✅️✈️✉️✊️✋️✌️✍️✏️✒️✔️✖️✝️✡️✨️✳️✴️❄️❇️❌️❎️❓️❔️❕️❗️❣️❤️➕️➖️➗️➡️➰️➿️⤴️⤵️⬅️⬆️⬇️⬛️⬜️⭐️⭕️〰️〽️㊗️㊙️🀄🃏🅰️🅱️🅾️🅿️🆎🆑🆒🆓🆔🆕🆖🆗🆘🆙🆚🈁🈂️🈚🈯🈲🈳🈴🈵🈶🈷️🈸🈹🈺🉐🉑🌀🌁🌂🌃🌄🌅🌆🌇🌈🌉🌊🌋🌌🌍🌎🌏🌐🌑🌒🌓🌔🌕🌖🌗🌘🌙🌚🌛🌜🌝🌞🌟🌠🌡️🌤️🌥️🌦️🌧️🌨️🌩️🌪️🌫️🌬️🌭🌮🌯🌰🌱🌲🌳🌴🌵🌶️🌷🌸🌹🌺🌻🌼🌽🌾🌿🍀🍁🍂🍃🍄🍅🍆🍇🍈🍉🍊🍋🍌🍍🍎🍏🍐🍑🍒🍓🍔🍕🍖🍗🍘🍙🍚🍛🍜🍝🍞🍟🍠🍡🍢🍣🍤🍥🍦🍧🍨🍩🍪🍫🍬🍭🍮🍯🍰🍱🍲🍳🍴🍵🍶🍷🍸🍹🍺🍻🍼🍽️🍾🍿🎀🎁🎂🎃🎄🎅🎆🎇🎈🎉🎊🎋🎌🎍🎎🎏🎐🎑🎒🎓🎖️🎗️🎙️🎚️🎛️🎞️🎟️🎠🎡🎢🎣🎤🎥🎦🎧🎨🎩🎪🎫🎬🎭🎮🎯🎰🎱🎲🎳🎴🎵🎶🎷🎸🎹🎺🎻🎼🎽🎾🎿🏀🏁🏂🏃🏄🏅🏆🏇🏈🏉🏊🏋️🏌️🏍️🏎️🏏🏐🏑🏒🏓🏔️🏕️🏖️🏗️🏘️🏙️🏚️🏛️🏜️🏝️🏞️🏟️🏠🏡🏢🏣🏤🏥🏦🏧🏨🏩🏪🏫🏬🏭🏮🏯🏰🏳️🏴🏵️🏷️🏸🏹🏺🏻🏼🏽🏾🏿🐀🐁🐂🐃🐄🐅🐆🐇🐈🐉🐊🐋🐌🐍🐎🐏🐐🐑🐒🐓🐔🐕🐖🐗🐘🐙🐚🐛🐜🐝🐞🐟🐠🐡🐢🐣🐤🐥🐦🐧🐨🐩🐪🐫🐬🐭🐮🐯🐰🐱🐲🐳🐴🐵🐶🐷🐸🐹🐺🐻🐼🐽🐾🐿️👀👁️👂👃👄👅👆👇👈👉👊👋👌👍👎👏👐👑👒👓👔👕👖👗👘👙👚👛👜👝👞👟👠👡👢👣👤👥👦👧👨👩👪👫👬👭👮👯👰👱👲👳👴👵👶👷👸👹👺👻👼👽👾👿💀💁💂💃💄💅💆💇💈💉💊💋💌💍💎💏💐💑💒💓💔💕💖💗💘💙💚💛💜💝💞💟💠💡💢💣💤💥💦💧💨💩💪💫💬💭💮💯💰💱💲💳💴💵💶💷💸💹💺💻💼💽💾💿📀📁📂📃📄📅📆📇📈📉📊📋📌📍📎📏📐📑📒📓📔📕📖📗📘📙📚📛📜📝📞📟📠📡📢📣📤📥📦📧📨📩📪📫📬📭📮📯📰📱📲📳📴📵📶📷📸📹📺📻📼📽️📿🔀🔁🔂🔃🔄🔅🔆🔇🔈🔉🔊🔋🔌🔍🔎🔏🔐🔑🔒🔓🔔🔕🔖🔗🔘🔙🔚🔛🔜🔝🔞🔟🔠🔡🔢🔣🔤🔥🔦🔧🔨🔩🔪🔫🔬🔭🔮🔯🔰🔱🔲🔳🔴🔵🔶🔷🔸🔹🔺🔻🔼🔽🕉️🕊️🕋🕌🕍🕎🕐🕑🕒🕓🕔🕕🕖🕗🕘🕙🕚🕛🕜🕝🕞🕟🕠🕡🕢🕣🕤🕥🕦🕧🕯️🕰️🕳️🕴️🕵️🕶️🕷️🕸️🕹️🕺🖇️🖊️🖋️🖌️🖍️🖐️🖕🖖🖤🖥️🖨️🖱️🖲️🖼️🗂️🗃️🗄️🗑️🗒️🗓️🗜️🗝️🗞️🗡️🗣️🗨️🗯️🗳️🗺️🗻🗼🗽🗾🗿😀😁😂😃😄😅😆😇😈😉😊😋😌😍😎😏😐😑😒😓😔😕😖😗😘😙😚😛😜😝😞😟😠😡😢😣😤😥😦😧😨😩😪😫😬😭😮😯😰😱😲😳😴😵😶😷😸😹😺😻😼😽😾😿🙀🙁🙂🙃🙄🙅🙆🙇🙈🙉🙊🙋🙌🙍🙎🙏🚀🚁🚂🚃🚄🚅🚆🚇🚈🚉🚊🚋🚌🚍🚎🚏🚐🚑🚒🚓🚔🚕🚖🚗🚘🚙🚚🚛🚜🚝🚞🚟🚠🚡🚢🚣🚤🚥🚦🚧🚨🚩🚪🚫🚬🚭🚮🚯🚰🚱🚲🚳🚴🚵🚶🚷🚸🚹🚺🚻🚼🚽🚾🚿🛀🛁🛂🛃🛄🛅🛋️🛌🛍️🛎️🛏️🛐🛑🛒🛕🛖🛗🛜🛝🛞🛟🛠️🛡️🛢️🛣️🛤️🛥️🛩️🛫🛬🛰️🛳️🛴🛵🛶🛷🛸🛹🛺🛻🛼🟠🟡🟢🟣🟤🟥🟦🟧🟨🟩🟪🟫🟰🤌🤍🤎🤏🤐🤑🤒🤓🤔🤕🤖🤗🤘🤙🤚🤛🤜🤝🤞🤟🤠🤡🤢🤣🤤🤥🤦🤧🤨🤩🤪🤫🤬🤭🤮🤯🤰🤱🤲🤳🤴🤵🤶🤷🤸🤹🤺🤼🤽🤾🤿🥀🥁🥂🥃🥄🥅🥇🥈🥉🥊🥋🥌🥍🥎🥏🥐🥑🥒🥓🥔🥕🥖🥗🥘🥙🥚🥛🥜🥝🥞🥟🥠🥡🥢🥣🥤🥥🥦🥧🥨🥩🥪🥫🥬🥭🥮🥯🥰🥱🥲🥳🥴🥵🥶🥷🥸🥹🥺🥻🥼🥽🥾🥿🦀🦁🦂🦃🦄🦅🦆🦇🦈🦉🦊🦋🦌🦍🦎🦏🦐🦑🦒🦓🦔🦕🦖🦗🦘🦙🦚🦛🦜🦝🦞🦟🦠🦡🦢🦣🦤🦥🦦🦧🦨🦩🦪🦫🦬🦭🦮🦯🦰🦱🦲🦳🦴🦵🦶🦷🦸🦹🦺🦻🦼🦽🦾🦿🧀🧁🧂🧃🧄🧅🧆🧇🧈🧉🧊🧋🧌🧍🧎🧏🧐🧑🧒🧓🧔🧕🧖🧗🧘🧙🧚🧛🧜🧝🧞🧟🧠🧡🧢🧣🧤🧥🧦🧧🧨🧩🧪🧫🧬🧭🧮🧯🧰🧱🧲🧳🧴🧵🧶🧷🧸🧹🧺🧻🧼🧽🧾🧿🩰🩱🩲🩳🩴🩵🩶🩷🩸🩹🩺🩻🩼🪀🪁🪂🪃🪄🪅🪆🪇🪈🪐🪑🪒🪓🪔🪕🪖🪗🪘🪙🪚🪛🪜🪝🪞🪟🪠🪡🪢🪣🪤🪥🪦🪧🪨🪩🪪🪫🪬🪭🪮🪯🪰🪱🪲🪳🪴🪵🪶🪷🪸🪹🪺🪻🪼🪽🪿🫀🫁🫂🫃🫄🫅🫎🫏🫐🫑🫒🫓🫔🫕🫖🫗🫘🫙🫚🫛🫠🫡🫢🫣🫤🫥🫦🫧🫨🫰🫱🫲🫳🫴🫵🫶
`


export default {
  name: 'App',
  components: {
    
  },

  computed: {
    aPagedIcons() {
      return this.aIcons.slice(this.iCurrentPage*this.iPageItems, (this.iCurrentPage+1)*this.iPageItems);
    }
  },

  methods: {
    fnStart() {
      this.iCurrentPage=0
    },
    fnEnd() {
      this.iCurrentPage=this.iMaxPages-1
    },
    fnNext() {
      if (this.iCurrentPage<this.iMaxPages-1)
      this.iCurrentPage++
    },
    fnPrev() {
      if (this.iCurrentPage>0)
      this.iCurrentPage--
    },
    // fnGetPage() {
    //   return this.aIcons.slice().splice(this.iCurrentPage*this.iPageItems, this.iPageItems)
    // }
  },

  data() {
    var aIcons = []
    var iPageItems = Math.floor((window.innerHeight-30)/85)*Math.floor((window.innerWidth)/85)
    // var aList = sList.split(/\n/)
    // aList = aList.filter((sI) => sI)
    // aList = aList.map((sI) => sI.split(';'))
    // aList = aList.map((aI) => aI[0].split('..'))
    aIcons = Array.from(sEmojiList).filter((sI) => sI!="️" && sI!="\n") // .split(/([\uD800-\uDBFF][\uDC00-\uDFFF])/)
    
    // for (var aItem of aList) {
    //   if (aItem.length>1) {
    //     for (var iI=parseInt(aItem[0], 16); iI<=parseInt(aItem[1], 16); iI++) { aIcons.push(String.fromCodePoint(iI)) }
    //   } else {
    //     aIcons.push(String.fromCharCode(aItem[0]))
    //   }
    // }
    return {
      iPageItems: iPageItems,
      iCurrentPage: 0,
      iMaxPages: Math.ceil(aIcons.length/iPageItems),
      sList,
      sTabShow: "grid",
      aIcons: aIcons
    }
  }

}
</script>


<style>
html, body {
  margin: 0px;
  padding: 0px;
}

.grid {
  display: flex;
  flex-wrap: wrap;
  font-size: 50px;
}

.cell {
  padding: 5px;
  margin: 5px;
  border: 1px solid #eee;
  height: 60px;
  width: 60px;
}

.top-panel {
  display: flex;
  gap: 10px;
  justify-content: center;
}

.top-panel > * {
  padding: 5px;
  font-size: 16px;
}

.list {
  overflow-y: scroll;
  height: calc(100vh - 30px);
}
</style>
