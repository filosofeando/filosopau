{enunciado:'Descartes utilizó la duda metódica para llegar a una primera certeza: "Cogito ergo sum".',respuesta:true},
  {enunciado:'Platón distingue entre el mundo sensible (doxa) y el mundo inteligible (episteme).',respuesta:true},
  {enunciado:'Para Aristóteles, el ser humano es un "animal político" por naturaleza.',respuesta:true},
  {enunciado:'Hume defiende que el principio de causalidad es una verdad racional necesaria.',respuesta:false,explicacion:'Para Hume la causalidad es un hábito mental basado en la experiencia, no una verdad racional.'},
  {enunciado:'El mito de la caverna de Platón aparece en "La República".',respuesta:true},
  {enunciado:'Nietzsche propone al "último hombre" como ideal a seguir.',respuesta:false,explicacion:'El ideal de Nietzsche es el Übermensch (superhombre). El "último hombre" es su crítica al conformismo.'},
  {enunciado:'Para Kant, el espacio y el tiempo son formas a priori de la intuición sensible.',respuesta:true},
  {enunciado:'Marx y Engels escribieron juntos "El manifiesto comunista" en 1848.',respuesta:true},
  {enunciado:'Descartes fue racionalista y defendía que la experiencia es la fuente del conocimiento.',respuesta:false,explicacion:'Descartes fue racionalista: la razón, no la experiencia, es la fuente del conocimiento verdadero.'},
];
let vmIndex = 0, vmPuntos = 0, vmTotal = 0, vmData = [];
function renderVerdadMentira() {
  vmData = [...verdadMentiraData].sort(()=>Math.random()-0.5).slice(0,10);
  vmIndex=0; vmPuntos=0; vmTotal=vmData.length;
  mostrarVMPregunta();
}
function mostrarVMPregunta() {
  if(vmIndex>=vmTotal){
    document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card" style="text-align:center">
      <div style="font-size:3rem;margin-bottom:0.5rem">${vmPuntos>=8?'🏆':vmPuntos>=5?'👏':'📚'}</div>
      <h3 style="margin-bottom:0.5rem">${vmPuntos>=8?'¡Sobresaliente!':vmPuntos>=5?'¡Bien hecho!':'Sigue estudiando'}</h3>
      <p style="color:var(--text2);margin-bottom:1.5rem">${vmPuntos} de ${vmTotal} correctas</p>
      <button onclick="renderVerdadMentira()" style="background:var(--teal-dim);border:1px solid rgba(62,207,178,0.3);color:var(--teal);padding:0.6rem 1.5rem;border-radius:var(--radius-sm);font-weight:700;cursor:pointer">Jugar de nuevo 🔄</button>
    </div></div>`;
    return;
  }
  const q = vmData[vmIndex];
  document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card">
    <div style="font-size:0.72rem;font-weight:700;color:var(--teal);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:1rem">✅ Verdad o Mentira — ${vmIndex+1}/${vmTotal} · ${vmPuntos} puntos</div>
    <p style="font-size:1rem;line-height:1.6;margin-bottom:2rem;font-weight:500">"${q.enunciado}"</p>
    <div style="display:flex;gap:1rem;justify-content:center">
      <button onclick="responderVM(true)" style="flex:1;padding:1rem;border-radius:var(--radius-sm);background:var(--teal-dim);border:2px solid var(--teal);color:var(--teal);font-size:1.1rem;font-weight:800;cursor:pointer">✅ VERDAD</button>
      <button onclick="responderVM(false)" style="flex:1;padding:1rem;border-radius:var(--radius-sm);background:var(--red-dim);border:2px solid var(--red);color:var(--red);font-size:1.1rem;font-weight:800;cursor:pointer">❌ MENTIRA</button>
    </div>
  </div></div>`;
}
function responderVM(resp) {
  const q = vmData[vmIndex];
  const correcto = resp===q.respuesta;
  if(correcto) vmPuntos++;
  const explicacion = !correcto&&q.explicacion ? `<p style="font-size:0.82rem;color:var(--text2);margin-top:0.5rem;font-style:italic">💡 ${q.explicacion}</p>` : '';
  document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card">
    <div style="font-size:0.72rem;font-weight:700;color:var(--teal);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:1rem">✅ Verdad o Mentira — ${vmIndex+1}/${vmTotal}</div>
    <p style="font-size:1rem;line-height:1.6;margin-bottom:1rem;font-weight:500">"${q.enunciado}"</p>
    <div style="padding:1rem;border-radius:var(--radius-sm);background:${correcto?'var(--teal-dim)':'var(--red-dim)'};border:1px solid ${correcto?'var(--teal)':'var(--red)'};margin-bottom:1rem">
      <strong style="color:${correcto?'var(--teal)':'var(--red)'}">${correcto?'✅ ¡Correcto!':'❌ Incorrecto'}</strong>
      <span style="color:var(--text2);margin-left:0.5rem">Era ${q.respuesta?'VERDAD':'MENTIRA'}</span>
      ${explicacion}
    </div>
    <button onclick="vmIndex++;mostrarVMPregunta()" style="background:var(--card2);border:1px solid var(--border);color:var(--text);padding:0.6rem 1.5rem;border-radius:var(--radius-sm);font-weight:700;cursor:pointer">Siguiente →</button>
  </div></div>`;
}

// ===== ¿QUÉ SIGNIFICA? =====
const definicionData = [
  {concepto:'Alegoría de la caverna',definicion:'Metáfora platónica que ilustra la diferencia entre el mundo sensible (sombras) y el mundo inteligible (realidad verdadera).'},
  {concepto:'Imperativo categórico',definicion:'Mandato moral incondicional de Kant: actúa solo según la máxima que puedas querer como ley universal.'},
  {concepto:'Tabula rasa',definicion:'Expresión de Locke (desarrollada por el empirismo) según la cual la mente es como una pizarra en blanco al nacer.'},
  {concepto:'Superhombre (Übermensch)',definicion:'Ideal de Nietzsche: ser humano que crea sus propios valores, supera la moral de los esclavos y afirma la vida.'},
  {concepto:'Plusvalía',definicion:'Concepto marxista: la diferencia entre el valor que el trabajador produce y el salario que recibe, apropiada por el capitalista.'},
  {concepto:'Res cogitans',definicion:'En Descartes, la "cosa pensante": sustancia inmaterial que identifica al yo como mente o alma.'},
  {concepto:'Eudaimonía',definicion:'Término griego que significa felicidad o florecimiento humano; para Aristóteles es el fin supremo de la vida.'},
  {concepto:'A priori',definicion:'Conocimiento independiente de la experiencia, que precede a ella lógicamente; utilizado por Kant.'},
  {concepto:'Mímesis',definicion:'Concepto de Platón y Aristóteles: imitación de la realidad; en el arte, representación de la naturaleza.'},
  {concepto:'Voluntad de poder',definicion:'Concepto nietzscheano: fuerza creadora y expansiva del ser humano que impulsa a superar límites y crear valores.'},
  {concepto:'Dialéctica',definicion:'Método de Platón (diálogo para llegar a la verdad) y de Hegel/Marx (movimiento de tesis–antítesis–síntesis).'},
  {concepto:'Noúmeno',definicion:'En Kant, la "cosa en sí": realidad que existe pero que no podemos conocer directamente con la experiencia.'},
];
let defIndex=0, defPuntos=0, defData=[];
function renderDefinicion() {
  defData=[...definicionData].sort(()=>Math.random()-0.5).slice(0,8);
  defIndex=0; defPuntos=0;
  mostrarDefPregunta();
}
function mostrarDefPregunta() {
  if(defIndex>=defData.length){
    document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card" style="text-align:center">
      <div style="font-size:3rem;margin-bottom:0.5rem">${defPuntos>=6?'🏆':defPuntos>=4?'👏':'📚'}</div>
      <h3 style="margin-bottom:0.5rem">${defPuntos>=6?'¡Excelente vocabulario!':defPuntos>=4?'¡Bien!':'Repasa los conceptos'}</h3>
      <p style="color:var(--text2);margin-bottom:1.5rem">${defPuntos} de ${defData.length} correctas</p>
      <button onclick="renderDefinicion()" style="background:var(--gold-dim);border:1px solid rgba(201,168,76,0.3);color:var(--gold);padding:0.6rem 1.5rem;border-radius:var(--radius-sm);font-weight:700;cursor:pointer">Jugar de nuevo 🔄</button>
    </div></div>`;
    return;
  }
  const q = defData[defIndex];
  // 3 opciones incorrectas
  const otras = defData.filter((_,i)=>i!==defIndex).sort(()=>Math.random()-0.5).slice(0,3).map(d=>d.concepto);
  const opciones = [q.concepto,...otras].sort(()=>Math.random()-0.5);
  document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card">
    <div style="font-size:0.72rem;font-weight:700;color:var(--gold);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:1rem">📖 ¿Qué significa? — ${defIndex+1}/${defData.length} · ${defPuntos} pts</div>
    <p style="font-size:0.95rem;line-height:1.7;margin-bottom:1.5rem;padding:1rem;background:var(--bg3);border-radius:var(--radius-sm);border-left:3px solid var(--gold)">${q.definicion}</p>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:0.75rem">${opciones.map(op=>`<button onclick="responderDef('${op.replace(/'/g,"\\'")}','${q.concepto.replace(/'/g,"\\'")}',this)" style="padding:0.75rem;border-radius:var(--radius-sm);background:var(--card2);border:2px solid var(--border);color:var(--text);font-size:0.82rem;font-weight:600;cursor:pointer;text-align:left;line-height:1.3;transition:all 0.2s">${op}</button>`).join('')}</div>
  </div></div>`;
}
function responderDef(resp, correcto, btn) {
  const esCorrecta = resp===correcto;
  if(esCorrecta) defPuntos++;
  document.querySelectorAll('#gameZone button[onclick^="responderDef"]').forEach(b=>{
    b.style.pointerEvents='none';
    if(b.textContent.trim()===correcto) {b.style.background='var(--teal-dim)';b.style.borderColor='var(--teal)';b.style.color='var(--teal)';}
    else if(b===btn&&!esCorrecta) {b.style.background='var(--red-dim)';b.style.borderColor='var(--red)';b.style.color='var(--red)';}
  });
  setTimeout(()=>{defIndex++;mostrarDefPregunta();},1200);
}

// ===== RULETA FILOSÓFICA =====
const ruletaPreguntas = {
  'Platón':[
    {p:'¿Cómo se llama la teoría de Platón sobre las ideas perfectas?',r:'Teoría de las Ideas (mundo inteligible)'},
    {p:'¿Qué alegoría usa Platón para explicar el conocimiento y la ignorancia?',r:'La alegoría de la caverna'},
    {p:'¿Qué tipo de gobierno considera Platón el mejor en La República?',r:'La aristocracia gobernada por filósofos-reyes'},
    {p:'¿Qué es la "doxa" para Platón?',r:'La opinión o conocimiento sensible imperfecto'},
    {p:'¿Qué método usaba Sócrates, maestro de Platón, para filosofar?',r:'La mayéutica (arte de parir ideas mediante el diálogo)'},
  ],
  'Aristóteles':[
    {p:'¿Qué es la "eudaimonía" para Aristóteles?',r:'La felicidad o florecimiento humano; el fin supremo de la vida'},
    {p:'¿Qué es el ser humano para Aristóteles en sentido político?',r:'Un "animal político" (zóon politikón) que vive en comunidad'},
    {p:'¿Qué son la materia y la forma en la hilemorfismo de Aristóteles?',r:'Materia: sustrato físico. Forma: esencia que organiza la materia'},
    {p:'¿Qué son las cuatro causas de Aristóteles?',r:'Material, formal, eficiente y final'},
    {p:'¿Cómo critica Aristóteles la teoría de las Ideas de Platón?',r:'Las ideas no pueden estar separadas de las cosas; la esencia está en las cosas mismas'},
  ],
  'Descartes':[
    {p:'¿Cuál es la primera certeza indudable a la que llega Descartes?',r:'"Pienso, luego existo" (Cogito ergo sum)'},
    {p:'¿Qué es la duda metódica en Descartes?',r:'Herramienta para dudar de todo hasta encontrar una verdad indudable'},
    {p:'¿Qué son la res cogitans y la res extensa?',r:'Res cogitans: sustancia pensante (mente). Res extensa: sustancia material (cuerpo)'},
    {p:'¿A qué corriente filosófica pertenece Descartes?',r:'Al racionalismo'},
    {p:'¿Qué papel tiene Dios en la filosofía de Descartes?',r:'Garante de que las ideas claras y distintas son verdaderas'},
  ],
  'Hume':[
    {p:'¿Qué son las impresiones para Hume?',r:'Percepciones directas y vívidas; base del conocimiento empírico'},
    {p:'¿Cómo explica Hume el principio de causalidad?',r:'No es racional sino un hábito mental basado en la experiencia repetida'},
    {p:'¿A qué corriente filosófica pertenece Hume?',r:'Al empirismo'},
    {p:'¿Qué critica Hume sobre la identidad personal?',r:'El "yo" no es más que un haz de impresiones cambiantes; no hay un yo sustancial'},
    {p:'¿Cuál es la famosa guillotina de Hume?',r:'No se puede pasar del "es" al "debe": de los hechos a los valores morales'},
  ],
  'Kant':[
    {p:'¿Qué son los juicios sintéticos a priori de Kant?',r:'Juicios que amplían el conocimiento (sintéticos) pero son universales y necesarios (a priori)'},
    {p:'¿Cuál es el imperativo categórico de Kant?',r:'"Actúa solo según aquella máxima que puedas querer que sea ley universal"'},
    {p:'¿Qué son el noúmeno y el fenómeno?',r:'Fenómeno: cosa tal como la conocemos. Noúmeno: cosa en sí misma, incognoscible'},
    {p:'¿Qué es la "mayoría de edad" en el texto de Kant sobre la Ilustración?',r:'Usar la propia razón sin tutelas ajenas; atreverse a saber (Sapere aude)'},
    {p:'¿Qué son el espacio y el tiempo para Kant?',r:'Formas a priori de la intuición sensible (no cualidades de las cosas)'},
  ],
  'Nietzsche':[
    {p:'¿Qué proclama Nietzsche con "Dios ha muerto"?',r:'La pérdida de los valores absolutos y la necesidad de crear nuevos valores'},
    {p:'¿Qué es el Übermensch (superhombre) en Nietzsche?',r:'El ideal humano que crea sus propios valores más allá del bien y el mal'},
    {p:'¿Qué es la moral de los esclavos según Nietzsche?',r:'Moral del resentimiento que exalta la debilidad y condena los instintos vitales'},
    {p:'¿Qué es el eterno retorno en Nietzsche?',r:'Idea de que la vida se repite infinitamente; afirmar la vida es querer que se repita'},
    {p:'¿Cuál es la voluntad de poder para Nietzsche?',r:'Fuerza creadora y expansiva que impulsa al ser humano a superarse y crear valores'},
  ],
  'Marx':[
    {p:'¿Qué es la alienación del trabajo para Marx?',r:'El trabajador pierde el producto de su trabajo, se enajena de su esencia humana'},
    {p:'¿Qué es la plusvalía para Marx?',r:'La diferencia entre el valor producido por el trabajador y su salario, apropiada por el capitalista'},
    {p:'¿Cuál es la célebre frase de Marx sobre la religión?',r:'"La religión es el opio del pueblo"'},
    {p:'¿Cuál es el materialismo histórico de Marx?',r:'La historia la mueve la lucha de clases y las condiciones materiales de producción'},
    {p:'¿Qué propone Marx como solución a la explotación capitalista?',r:'La revolución del proletariado y la abolición de la propiedad privada'},
  ],
};
let ruletaEstado = {autor:'',preguntas:[],index:0,puntos:0,tiempo:60,interval:null};
function renderRuleta() {
  const autores = Object.keys(ruletaPreguntas);
  const autor = autores[Math.floor(Math.random()*autores.length)];
  clearInterval(ruletaEstado.interval);
  ruletaEstado = {autor,preguntas:[...ruletaPreguntas[autor]].sort(()=>Math.random()-0.5),index:0,puntos:0,tiempo:60,interval:null};
  // animación ruleta
  document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card" style="text-align:center">
    <div style="font-size:3rem;animation:spin 0.8s ease-out">🎰</div>
    <h3 style="margin-top:1rem;color:var(--purple)">Girando la ruleta…</h3>
  </div></div>`;
  setTimeout(()=>mostrarRuletaPregunta(),900);
}
function mostrarRuletaPregunta() {
  const {autor,preguntas,index,puntos,tiempo} = ruletaEstado;
  if(index>=preguntas.length||tiempo<=0){
    clearInterval(ruletaEstado.interval);
    document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card" style="text-align:center">
      <div style="font-size:3rem;margin-bottom:0.5rem">${puntos>=4?'🏆':puntos>=2?'👏':'📚'}</div>
      <h3>Autor: ${autor}</h3>
      <p style="color:var(--text2);margin:0.5rem 0 1.5rem">${puntos} de ${preguntas.length} correctas</p>
      <button onclick="renderRuleta()" style="background:var(--purple-dim);border:1px solid rgba(167,139,250,0.3);color:var(--purple);padding:0.6rem 1.5rem;border-radius:var(--radius-sm);font-weight:700;cursor:pointer">Girar de nuevo 🎲</button>
    </div></div>`;
    return;
  }
  const q = preguntas[index];
  document.getElementById('gameZone').innerHTML=`<div class="quiz-game-container"><div class="qg-card">
    <div style="font-size:0.72rem;font-weight:700;color:var(--purple);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.5rem">🎰 Ruleta: ${autor} — ${index+1}/5 · ⏱️ <span id="ruletaTimer">${ruletaEstado.tiempo}</span>s</div>
    <p style="font-size:1rem;line-height:1.6;margin-bottom:1.5rem;font-weight:500">${q.p}</p>
    <div id="ruletaRespArea">
      <textarea id="ruletaInput" rows="3" placeholder="Escribe tu respuesta…" style="width:100%;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);padding:0.75rem;font-family:var(--font-body);font-size:0.9rem;resize:none"></textarea>
      <button onclick="verRuletaRespuesta()" style="margin-top:0.75rem;background:var(--purple-dim);border:1px solid rgba(167,139,250,0.3);color:var(--purple);padding:0.6rem 1.5rem;border-radius:var(--radius-sm);font-weight:700;cursor:pointer">Ver respuesta correcta</button>
    </div>
  </div></div>`;
  clearInterval(ruletaEstado.interval);
  ruletaEstado.interval = setInterval(()=>{
    ruletaEstado.tiempo--;
    const el = document.getElementById('ruletaTimer');
    if(el) el.textContent=ruletaEstado.tiempo;
    if(ruletaEstado.tiempo<=0){clearInterval(ruletaEstado.interval);mostrarRuletaPregunta();}
  },1000);
}
function verRuletaRespuesta() {
  clearInterval(ruletaEstado.interval);
  const q = ruletaEstado.preguntas[ruletaEstado.index];
  const area = document.getElementById('ruletaRespArea');
  if(area) area.innerHTML=`
    <div style="padding:1rem;background:var(--teal-dim);border:1px solid var(--teal);border-radius:var(--radius-sm);margin-bottom:1rem">
      <strong style="color:var(--teal);display:block;margin-bottom:0.4rem">✅ Respuesta modelo:</strong>
      <p style="font-size:0.9rem;line-height:1.6">${q.r}</p>
    </div>
    <div style="display:flex;gap:0.75rem">
      <button onclick="ruletaEstado.puntos++;ruletaEstado.index++;ruletaEstado.tiempo=60;mostrarRuletaPregunta()" style="flex:1;padding:0.6rem;background:var(--teal-dim);border:1px solid var(--teal);color:var(--teal);border-radius:var(--radius-sm);font-weight:700;cursor:pointer">✅ La sabía</button>
      <button onclick="ruletaEstado.index++;ruletaEstado.tiempo=60;mostrarRuletaPregunta()" style="flex:1;padding:0.6rem;background:var(--red-dim);border:1px solid var(--red);color:var(--red);border-radius:var(--radius-sm);font-weight:700;cursor:pointer">❌ No la sabía</button>
    </div>`;
}

function renderQuienSoy() {
  qgIndex=Math.floor(Math.random()*quienSoyData.length);
  qgPistaIndex=0; qgAnswered=false;
  const d=quienSoyData[qgIndex];
  const otros=autoresData.map(a=>a.nombre).filter(n=>n!==d.filosofo);
  const shuffled=[d.filosofo,...otros.sort(()=>Math.random()-0.5).slice(0,3)].sort(()=>Math.random()-0.5);
  document.getElementById('gameZone').innerHTML = `
    <div class="quiz-game-container">
      <div class="qg-card">
        <div style="font-size:0.72rem;font-weight:700;color:var(--gold);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:1rem">¿Quién soy? — Pista ${qgPistaIndex+1} de ${d.pistas.length}</div>
        <div class="qg-clue-label">Pista ${qgPistaIndex+1}</div>
        <div class="qg-clue" id="qgClue">${d.pistas[qgPistaIndex]}</div>
        <div class="qg-options" id="qgOptions">${shuffled.map(n=>`<button class="qg-opt" onclick="answerQuienSoy('${n}','${d.filosofo}',this)">${n}</button>`).join('')}</div>
        <div style="margin-top:1rem;display:flex;gap:0.75rem;justify-content:center;flex-wrap:wrap">
          <button onclick="nextPista()" style="background:var(--card2);border:1px solid var(--border);color:var(--text2);padding:0.5rem 1rem;border-radius:var(--radius-sm);font-size:0.82rem;font-weight:600;cursor:pointer">Siguiente pista →</button>
          <button onclick="showGame('quiensoy')" style="background:var(--gold-dim);border:1px solid rgba(201,168,76,0.3);color:var(--gold);padding:0.5rem 1rem;border-radius:var(--radius-sm);font-size:0.82rem;font-weight:600;cursor:pointer">Nuevo filósofo 🔄</button>
        </div>
      </div>
    </div>`;
}

function nextPista() {
  const d=quienSoyData[qgIndex];
  if(qgPistaIndex<d.pistas.length-1) {
    qgPistaIndex++;
    document.querySelector('.qg-clue-label').textContent=`Pista ${qgPistaIndex+1}`;
    document.querySelector('.qg-clue').textContent=d.pistas[qgPistaIndex];
    document.querySelector('.quiz-game-container .qg-card > div:first-child').textContent=`¿Quién soy? — Pista ${qgPistaIndex+1} de ${d.pistas.length}`;
  }
}

function answerQuienSoy(answer, correct, btn) {
  if(qgAnswered) return;
  qgAnswered=true;
  document.querySelectorAll('.qg-opt').forEach(b => { b.disabled=true; if(b.textContent===correct) b.classList.add('correct'); else if(b===btn && answer!==correct) b.classList.add('wrong'); });
}

function renderWordle() {
  const wordObj = wordleWords[Math.floor(Math.random()*wordleWords.length)];
  const word = wordObj.word.toUpperCase();
  let currentRow=0, currentCol=0, gameOver=false;
  const grid=Array(6).fill(null).map(()=>Array(word.length).fill(''));
  
  const rows=6, cols=word.length;
  document.getElementById('gameZone').innerHTML=`
    <div class="wordle-container">
      <div style="text-align:center;margin-bottom:1rem">
        <div style="font-size:0.72rem;font-weight:700;color:var(--purple);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.4rem">FiloWordle</div>
        <div style="font-size:0.85rem;color:var(--text2)">Pista: ${wordObj.hint}</div>
      </div>
      <div class="wordle-grid" style="grid-template-columns:repeat(${cols},1fr)" id="wordleGrid">
        ${Array(rows*cols).fill('<div class="wordle-cell" id="wc"></div>').join('')}
      </div>
      <div class="wordle-keyboard" id="wordleKeyboard">
        <div class="wordle-row">${'QWERTYUIOP'.split('').map(l=>`<button class="wk" onclick="wkPress('${l}')">${l}</button>`).join('')}</div>
        <div class="wordle-row">${'ASDFGHJKL'.split('').map(l=>`<button class="wk" onclick="wkPress('${l}')">${l}</button>`).join('')}</div>
        <div class="wordle-row"><button class="wk" onclick="wkPress('ENTER')" style="min-width:60px;font-size:0.7rem">ENTER</button>${'ZXCVBNM'.split('').map(l=>`<button class="wk" onclick="wkPress('${l}')">${l}</button>`).join('')}<button class="wk" onclick="wkPress('BACK')" style="min-width:44px">⌫</button></div>
      </div>
      <div id="wordleMsg" style="text-align:center;margin-top:1rem;font-size:0.875rem;font-weight:600;color:var(--gold);min-height:24px"></div>
      <div style="text-align:center;margin-top:1rem"><button onclick="renderWordle()" style="background:var(--card2);border:1px solid var(--border);color:var(--text2);padding:0.5rem 1.1rem;border-radius:var(--radius-sm);font-size:0.82rem;cursor:pointer">Nueva palabra 🔄</button></div>
    </div>`;

  const cells = document.getElementById('wordleGrid').children;
  
  window.wkPress = function(key) {
    if(gameOver) return;
    if(key==='BACK') { if(currentCol>0){currentCol--;grid[currentRow][currentCol]='';cells[currentRow*cols+currentCol].textContent='';cells[currentRow*cols+currentCol].classList.remove('filled');} }
    else if(key==='ENTER') {
      if(currentCol<cols){document.getElementById('wordleMsg').textContent='Completa la fila primero';return;}
      const guess=grid[currentRow].join('');
      const result=Array(cols).fill('absent');
      const wordArr=word.split('');
      const guessArr=guess.split('');
      guessArr.forEach((l,i)=>{if(l===wordArr[i])result[i]='correct';});
      const remaining=wordArr.filter((l,i)=>result[i]!=='correct');
      guessArr.forEach((l,i)=>{if(result[i]!=='correct'&&remaining.includes(l)){result[i]='present';remaining.splice(remaining.indexOf(l),1);}});
      result.forEach((r,i)=>{const cell=cells[currentRow*cols+i];cell.classList.add(r);});
      if(guess===word){document.getElementById('wordleMsg').textContent='¡Correcto! 🎉 Es '+word;gameOver=true;return;}
      currentRow++;currentCol=0;
      if(currentRow>=rows){document.getElementById('wordleMsg').textContent='La palabra era: '+word;gameOver=true;}
    } else {
      if(currentCol<cols&&!gameOver){grid[currentRow][currentCol]=key;const cell=cells[currentRow*cols+currentCol];cell.textContent=key;cell.classList.add('filled');currentCol++;}
    }
  };
}

function renderParejas() {
  const items=[...parejasData].sort(()=>Math.random()-0.5).slice(0,6);
  const cards=[...items.map(i=>({text:i.concepto,pair:i.autor,type:'concepto'})),...items.map(i=>({text:i.autor,pair:i.concepto,type:'autor'}))].sort(()=>Math.random()-0.5);
  let flipped=[],matched=[],moves=0,startTime=Date.now();
  
  document.getElementById('gameZone').innerHTML=`
    <div style="max-width:700px;margin:0 auto">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:1rem;flex-wrap:wrap;gap:0.5rem">
        <div style="font-size:0.72rem;font-weight:700;color:var(--blue);text-transform:uppercase;letter-spacing:0.08em">Parejas Filosóficas</div>
        <div style="font-size:0.82rem;color:var(--text3);font-family:var(--font-mono)">Movimientos: <span id="pMoves">0</span> | Pares: <span id="pMatched">0</span>/${items.length}</div>
      </div>
      <div style="display:grid;grid-template-columns:repeat(4,1fr);gap:0.65rem" id="parejasGrid">
        ${cards.map((c,i)=>`<div class="autor-card" id="pc${i}" onclick="flipCard(${i})" style="cursor:pointer;min-height:80px;display:flex;align-items:center;justify-content:center;text-align:center;padding:0.85rem;font-size:0.82rem;font-weight:600;background:var(--bg3);border:1px solid var(--border)">${c.text}</div>`).join('')}
      </div>
      <div id="parejasMsg" style="text-align:center;margin-top:1rem;font-size:0.875rem;font-weight:600;color:var(--gold);min-height:24px"></div>
      <div style="text-align:center;margin-top:0.75rem"><button onclick="renderParejas()" style="background:var(--card2);border:1px solid var(--border);color:var(--text2);padding:0.5rem 1.1rem;border-radius:var(--radius-sm);font-size:0.82rem;cursor:pointer">Nuevo juego 🔄</button></div>
    </div>`;

  window.flipCard=function(i) {
    if(flipped.length>=2||matched.includes(i)||flipped.includes(i)) return;
    document.getElementById(`pc${i}`).style.background='var(--blue-dim)';
    document.getElementById(`pc${i}`).style.borderColor='var(--blue)';
    flipped.push(i);
    if(flipped.length===2) {
      moves++;
      document.getElementById('pMoves').textContent=moves;
      const [a,b]=flipped;
      if(cards[a].pair===cards[b].text||cards[b].pair===cards[a].text) {
        matched.push(a,b);
        [a,b].forEach(idx=>{document.getElementById(`pc${idx}`).style.background='var(--teal-dim)';document.getElementById(`pc${idx}`).style.borderColor='var(--teal)';});
        document.getElementById('pMatched').textContent=matched.length/2;
        if(matched.length===cards.length){const t=Math.round((Date.now()-startTime)/1000);document.getElementById('parejasMsg').textContent=`¡Completado en ${moves} movimientos y ${t} segundos! 🎉`;}
        flipped=[];
      } else {
        setTimeout(()=>{[a,b].forEach(idx=>{document.getElementById(`pc${idx}`).style.background='var(--bg3)';document.getElementById(`pc${idx}`).style.borderColor='var(--border)';});flipped=[];},900);
      }
    }
  };
}

function renderOrdenar() {
  const items=[...ordenarData].sort(()=>Math.random()-0.5);
  let selected=null;
  document.getElementById('gameZone').innerHTML=`
    <div style="max-width:600px;margin:0 auto">
      <div style="font-size:0.72rem;font-weight:700;color:var(--purple);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:1rem;text-align:center">Ordena los filósofos cronológicamente (del más antiguo al más reciente)</div>
      <div id="ordenarList" style="display:flex;flex-direction:column;gap:0.5rem">
        ${items.map((item,i)=>`<div class="autor-card" id="oi${i}" onclick="selectOrdenar(${i})" style="cursor:pointer;padding:1rem;display:flex;justify-content:space-between;align-items:center"><span style="font-weight:600">${item.nombre}</span><span class="tag tag-blue" id="orank${i}">?</span></div>`).join('')}
      </div>
      <div style="text-align:center;margin-top:1.25rem;display:flex;gap:0.75rem;justify-content:center;flex-wrap:wrap">
        <button onclick="checkOrdenar(${JSON.stringify(items).replace(/"/g,"'")})" style="background:var(--gold);color:#0d0f14;border:none;padding:0.65rem 1.35rem;border-radius:var(--radius-sm);font-weight:700;font-size:0.875rem;cursor:pointer">Comprobar orden ✓</button>
        <button onclick="renderOrdenar()" style="background:var(--card2);border:1px solid var(--border);color:var(--text2);padding:0.65rem 1.1rem;border-radius:var(--radius-sm);font-size:0.82rem;cursor:pointer">Reiniciar 🔄</button>
      </div>
      <div id="ordenarMsg" style="text-align:center;margin-top:1rem;font-size:0.875rem;min-height:24px"></div>
    </div>`;
  
  let order=items.map((_,i)=>i), swapFrom=null;
  window.selectOrdenar=function(i) {
    if(swapFrom===null) { swapFrom=i; document.getElementById(`oi${i}`).style.borderColor='var(--gold)'; }
    else {
      const tmp=order[swapFrom]; order[swapFrom]=order[i]; order[i]=tmp;
      [swapFrom,i].forEach(idx=>document.getElementById(`oi${idx}`).style.borderColor='var(--border)');
      order.forEach((realIdx,pos)=>{ const el=document.getElementById(`orank${realIdx}`); });
      const list=document.getElementById('ordenarList');
      const newOrder=[...order];
      list.innerHTML=newOrder.map((realIdx,pos)=>`<div class="autor-card" id="oi${realIdx}" onclick="selectOrdenar(${realIdx})" style="cursor:pointer;padding:1rem;display:flex;justify-content:space-between;align-items:center"><span style="font-weight:600">${items[realIdx].nombre}</span><span class="tag tag-blue">${pos+1}º</span></div>`).join('');
      swapFrom=null;
    }
  };
  
  window.checkOrdenar=function(originalItems) {
    const listItems=document.querySelectorAll('#ordenarList .autor-card span:first-child');
    const currentOrder=[...listItems].map(el=>el.textContent.trim());
    const correctOrder=[...ordenarData].sort((a,b)=>a.año-b.año).map(i=>i.nombre);
    let correct=0;
    currentOrder.forEach((name,i)=>{ if(correctOrder[i]===name) correct++; });
    const pct=Math.round(correct/currentOrder.length*100);
    document.getElementById('ordenarMsg').innerHTML=`<span style="color:var(--gold)">${correct}/${currentOrder.length} en posición correcta</span> · Orden correcto: ${correctOrder.join(' → ')}`;
  };
}

// ===== TIMELINE =====
const timelineData = [
  {fecha:"470–399 a.C.",titulo:"Sócrates",corriente:"Filosofía Antigua",color:"var(--gold)",desc:"No dejó escritos. Método socrático (mayéutica). «Solo sé que no sé nada». Condenado a muerte por corromper a la juventud.",lado:"izq"},
  {fecha:"427–347 a.C.",titulo:"Platón",corriente:"Idealismo Clásico",color:"var(--gold)",desc:"Funda la Academia. Teoría de las Ideas, alegoría de la caverna, dualismo alma-cuerpo, Estado ideal gobernado por filósofos-reyes.",lado:"der"},
  {fecha:"384–322 a.C.",titulo:"Aristóteles",corriente:"Empirismo Clásico",color:"var(--teal)",desc:"Funda el Liceo. Metafísica hilemórfica, lógica formal, ética de la eudaimonia, zoon politikon. Tutor de Alejandro Magno.",lado:"izq"},
  {fecha:"1225–1274",titulo:"Tomás de Aquino",corriente:"Escolástica Medieval",color:"var(--purple)",desc:"Síntesis del aristotelismo con la teología cristiana. Las cinco vías para demostrar la existencia de Dios. Fe y razón son compatibles.",lado:"der"},
  {fecha:"1561–1626",titulo:"Francis Bacon",corriente:"Empirismo moderno",color:"var(--teal)",desc:"Nuevo método inductivo. Crítica a los ídolos del conocimiento. «Saber es poder». Precursor del empirismo y la revolución científica.",lado:"izq"},
  {fecha:"1596–1650",titulo:"Descartes",corriente:"Racionalismo",color:"var(--blue)",desc:"Padre del racionalismo moderno. Duda metódica, cogito ergo sum, dualismo mente-cuerpo. Fundador de la filosofía moderna.",lado:"der"},
  {fecha:"1632–1677",titulo:"Spinoza",corriente:"Racionalismo",color:"var(--blue)",desc:"Deus sive Natura: Dios y la Naturaleza son lo mismo. Monismo. Ética demostrada more geometrico. Determinismo y libertad como comprensión.",lado:"izq"},
  {fecha:"1646–1716",titulo:"Leibniz",corriente:"Racionalismo",color:"var(--blue)",desc:"Las mónadas como sustancias simples. Teodicea: vivimos en el mejor de los mundos posibles. Optimismo metafísico racionalista.",lado:"der"},
  {fecha:"1632–1704",titulo:"John Locke",corriente:"Empirismo",color:"var(--teal)",desc:"La mente es una tabula rasa. Ideas simples (de la experiencia) e ideas complejas. Padre del liberalismo político moderno.",lado:"izq"},
  {fecha:"1711–1776",titulo:"David Hume",corriente:"Empirismo Escocés",color:"var(--teal)",desc:"Escepticismo radical. La causalidad es hábito, no necesidad. El yo es solo un haz de percepciones. Despertó a Kant de su sueño dogmático.",lado:"der"},
  {fecha:"1712–1778",titulo:"Jean-Jacques Rousseau",corriente:"Ilustración",color:"var(--purple)",desc:"El ser humano nace bueno y la sociedad le corrompe. Contrato social. Voluntad general. Educación natural (Emilio).",lado:"izq"},
  {fecha:"1724–1804",titulo:"Immanuel Kant",corriente:"Idealismo Crítico",color:"var(--blue)",desc:"Giro copernicano: el sujeto conforma el objeto. Síntesis racionalismo-empirismo. Imperativo categórico. Paz perpetua.",lado:"der"},
  {fecha:"1770–1831",titulo:"Georg W. F. Hegel",corriente:"Idealismo Absoluto",color:"var(--purple)",desc:"Dialéctica tesis-antítesis-síntesis. El Espíritu Absoluto se realiza en la Historia. El búho de Minerva alza el vuelo al anochecer.",lado:"izq"},
  {fecha:"1806–1873",titulo:"John Stuart Mill",corriente:"Utilitarismo",color:"var(--teal)",desc:"La acción correcta maximiza la felicidad del mayor número. Utilitarismo cualitativo: no solo cantidad de placer. Defensor del sufragio femenino.",lado:"der"},
  {fecha:"1818–1883",titulo:"Karl Marx",corriente:"Materialismo Histórico",color:"var(--red)",desc:"La historia es lucha de clases. Materialismo histórico y dialéctico. Alienación del trabajador. El Capital. Manifiesto Comunista.",lado:"izq"},
  {fecha:"1844–1900",titulo:"Friedrich Nietzsche",corriente:"Vitalismo",color:"var(--gold)",desc:"Muerte de Dios. Nihilismo y transvaloración. Voluntad de poder. Eterno retorno. Übermensch. Amor fati. Contra el resentimiento.",lado:"der"},
  {fecha:"1858–1917",titulo:"Émile Durkheim",corriente:"Sociología / Positivismo",color:"var(--purple)",desc:"Fundador de la sociología moderna. Los hechos sociales como cosas. La solidaridad orgánica de las sociedades industriales.",lado:"izq"},
  {fecha:"1856–1939",titulo:"Sigmund Freud",corriente:"Psicoanálisis",color:"var(--teal)",desc:"El inconsciente como motor de la conducta. Ello, yo y superyó. La represión y la civilización. Influye profundamente en la filosofía del siglo XX.",lado:"der"},
  {fecha:"1883–1955",titulo:"Ortega y Gasset",corriente:"Raciovitalismo",color:"var(--gold)",desc:"«Yo soy yo y mi circunstancia». Raciovitalismo: la razón vital e histórica. La rebelión de las masas y el hombre-masa.",lado:"izq"},
  {fecha:"1889–1951",titulo:"Wittgenstein",corriente:"Filosofía del Lenguaje",color:"var(--blue)",desc:"Primer Wittgenstein: el lenguaje pinta la realidad (Tractatus). Segundo Wittgenstein: los juegos de lenguaje (Investigaciones filosóficas).",lado:"der"},
  {fecha:"1900–1961",titulo:"Merleau-Ponty",corriente:"Fenomenología",color:"var(--purple)",desc:"La percepción como fundamento del conocimiento. El cuerpo vivido como sujeto. Crítica al dualismo cartesiano desde la experiencia encarnada.",lado:"izq"},
  {fecha:"1908–1986",titulo:"Simone de Beauvoir",corriente:"Existencialismo feminista",color:"var(--red)",desc:"«No se nace mujer, se llega a serlo». El Segundo Sexo: crítica a la opresión de la mujer. Existencialismo aplicado a la emancipación femenina.",lado:"der"},
  {fecha:"1929–",titulo:"Jürgen Habermas",corriente:"Teoría Crítica",color:"var(--blue)",desc:"Acción comunicativa: la racionalidad reside en el diálogo entre iguales. Ética discursiva. Defensa de la democracia deliberativa.",lado:"izq"},
];

function renderTimeline() {
  document.getElementById('timeline').innerHTML = timelineData.map((item,i) => `
    <div class="timeline-item reveal">
      ${item.lado==='izq'
        ? `<div class="timeline-content" style="border-top:2px solid ${item.color}">
             <div class="timeline-date" style="color:${item.color}">${item.fecha}</div>
             <div style="font-size:0.65rem;font-weight:700;color:${item.color}88;text-transform:uppercase;letter-spacing:0.07em;margin-bottom:0.3rem">${item.corriente}</div>
             <div class="timeline-title">${item.titulo}</div>
             <div class="timeline-desc">${item.desc}</div>
           </div>
           <div class="timeline-spacer"></div>`
        : `<div class="timeline-spacer"></div>
           <div class="timeline-content" style="border-top:2px solid ${item.color}">
             <div class="timeline-date" style="color:${item.color}">${item.fecha}</div>
             <div style="font-size:0.65rem;font-weight:700;color:${item.color}88;text-transform:uppercase;letter-spacing:0.07em;margin-bottom:0.3rem">${item.corriente}</div>
             <div class="timeline-title">${item.titulo}</div>
             <div class="timeline-desc">${item.desc}</div>
           </div>`
      }
      <div class="timeline-dot" style="background:${item.color};box-shadow:0 0 0 3px ${item.color}33"></div>
    </div>`).join('');
}


// ===== BANCO =====
function renderBanco(items) {
  document.getElementById('bancoList').innerHTML = items.map((item,i) => `
    <div class="banco-item">
      <div class="banco-meta"><span class="tag tag-gold">${item.autor}</span><span class="tag tag-teal">${item.año}</span><span class="tag tag-blue">${item.tipo}</span></div>
      <div class="banco-q">${item.q}</div>
      <button class="banco-answer-toggle" onclick="toggleBancoAnswer(this,'banco-ans-${i}')">▸ Ver orientación de respuesta</button>
      <div class="banco-answer" id="banco-ans-${i}">${item.resp}</div>
    </div>`).join('');
}
function toggleBancoAnswer(btn, id) {
  const isOpen=document.getElementById(id).classList.toggle('show');
  btn.textContent=isOpen?'▾ Ocultar orientación':'▸ Ver orientación de respuesta';
}
function filterBanco() {
  const search=document.getElementById('bancoSearch').value.toLowerCase();
  const filter=document.getElementById('bancoFilter').value;
  renderBanco(bancoData.filter(item=>(filter==='all'||item.autor===filter)&&(item.q.toLowerCase().includes(search)||item.autor.toLowerCase().includes(search)||item.resp.toLowerCase().includes(search))));
}

// ===== EXÁMENES =====
function toggleExamen(id, btn) {
  const isOpen=document.getElementById(id).style.display==='block';
  document.getElementById(id).style.display=isOpen?'none':'block';
  btn.textContent=isOpen?'Ver corrección completa ↓':'Ocultar corrección ↑';
}
function renderExamenes() {
  const grid=document.getElementById('examenesGrid');
  if(!grid) return;
  grid.innerHTML=examenesData.map((ex,i) => `
    <div class="exam-year-card reveal">
      <div style="display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:0.65rem">
        <div style="font-family:var(--font-display);font-size:1.65rem;font-weight:900;color:var(--gold)">${ex.año}</div>
        <span class="tag tag-teal">Corregido ✓</span>
      </div>
      <div style="font-size:0.78rem;color:var(--text3);margin-bottom:0.75rem;font-family:var(--font-mono)">${ex.autor}</div>
      <div style="font-size:0.8rem;color:var(--text2);margin-bottom:0.4rem"><strong style="color:var(--gold)">A:</strong> ${ex.opcionA}</div>
      <div style="font-size:0.8rem;color:var(--text2);margin-bottom:0.9rem"><strong style="color:var(--teal)">B:</strong> ${ex.opcionB}</div>
      <div id="corr-${i}" style="display:none">
        <div style="background:var(--bg3);border-radius:8px;padding:0.8rem;margin-bottom:0.6rem;border-left:3px solid var(--gold)"><div style="font-size:0.68rem;font-weight:700;color:var(--gold);margin-bottom:0.3rem">ORIENTACIÓN A</div><p style="font-size:0.78rem;color:var(--text2);line-height:1.6">${ex.corrA}</p></div>
        <div style="background:var(--bg3);border-radius:8px;padding:0.8rem;margin-bottom:0.75rem;border-left:3px solid var(--teal)"><div style="font-size:0.68rem;font-weight:700;color:var(--teal);margin-bottom:0.3rem">ORIENTACIÓN B</div><p style="font-size:0.78rem;color:var(--text2);line-height:1.6">${ex.corrB}</p></div>
        <a href="${ex.url}" target="_blank" rel="noopener" style="font-size:0.78rem;color:var(--gold);font-weight:600">📄 Examen oficial PDF →</a>
      </div>
      <button onclick="toggleExamen('corr-${i}',this)" style="background:var(--card2);border:1px solid var(--border);color:var(--text2);padding:0.45rem 0.9rem;border-radius:var(--radius-sm);font-size:0.78rem;font-weight:600;cursor:pointer;width:100%;margin-top:0.25rem;transition:all 0.25s">Ver orientación ↓</button>
    </div>`).join('');
  observeReveal();
}

// ===== PODCASTS =====
function renderPodcasts() {
  document.getElementById('podcastsGrid').innerHTML = podcastsData.map(p => `
    <div class="podcast-card reveal">
      <div class="podcast-cover" style="background:${p.color==='#1db954'?'rgba(29,185,84,0.15)':p.color==='#ff0000'?'rgba(255,0,0,0.12)':'rgba(255,107,53,0.15)'}">
        ${p.icon}
      </div>
      <div class="podcast-platform">${p.plataforma}</div>
      <div class="podcast-name">${p.nombre}</div>
      <div class="podcast-desc">${p.desc}</div>
      <div class="podcast-eps">📻 ${p.episodios}</div>
      <div class="podcast-tags">${p.tags.map(t=>`<span class="tag tag-purple">${t}</span>`).join('')}</div>
      <a href="${p.url}" target="_blank" rel="noopener" class="btn-podcast">
        <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 14.5v-9l6 4.5-6 4.5z"/></svg>
        Escuchar ahora →
      </a>
    </div>`).join('');
  observeReveal();
}

// ===== LIBROS =====
function renderLibros(filter='all') {
  const items = filter==='all' ? librosData : librosData.filter(l=>l.cat===filter);
  document.getElementById('librosGrid').innerHTML = items.map(l => `
    <div class="libro-card reveal">
      <div class="libro-spine" style="background:${l.color}">${l.emoji}</div>
      <div class="libro-body">
        <div class="libro-titulo">${l.titulo}</div>
        <div class="libro-autor">${l.autor}</div>
        <div class="libro-desc">${l.desc}</div>
        <span class="libro-nivel ${l.nivel==='basico'?'nivel-basico':l.nivel==='medio'?'nivel-medio':'nivel-avanzado'}">${l.nivel==='basico'?'Básico':l.nivel==='medio'?'Medio':'Avanzado'}</span>
      </div>
    </div>`).join('');
  observeReveal();
}

// ===== PROGRESO =====
function renderProgreso() {
  document.getElementById('autorProgressList').innerHTML = autoresData.map(a => `
    <div class="apl-item">
      <label>${a.nombre} <span>${a.progreso}%</span></label>
      <div class="apl-bar"><div class="apl-fill" style="width:0%" data-width="${a.progreso}%"></div></div>
    </div>`).join('');
}

// ===== SIMULACRO =====
let examRunning=false, examSeconds=90*60, examInterval;
document.getElementById('startExam').addEventListener('click', function() {
  if(!examRunning) {
    examRunning=true; this.textContent='⏸ Pausar';
    examInterval=setInterval(()=>{
      examSeconds--;
      const m=Math.floor(examSeconds/60),s=examSeconds%60;
      const el=document.getElementById('examTimer');
      el.textContent=`${String(m).padStart(2,'0')}:${String(s).padStart(2,'0')}`;
      if(examSeconds<=600) el.classList.add('warning');
      if(examSeconds<=0){clearInterval(examInterval);el.textContent='00:00';submitExam();}
    },1000);
  } else { clearInterval(examInterval); examRunning=false; this.textContent='▶ Reanudar'; }
});

function updateWC(id,text) { document.getElementById(id).textContent=`${text.trim().split(/\s+/).filter(w=>w).length} palabras`; }

function submitExam() {
  clearInterval(examInterval); examRunning=false;
  const rs=[document.getElementById('resp1a').value.trim(),document.getElementById('resp1b').value.trim(),document.getElementById('resp1c').value.trim(),document.getElementById('resp2a').value.trim(),document.getElementById('resp2b').value.trim()];
  let score=0; const feedback=[];
  const checks=[(r)=>r.length>50,(r)=>r.length>80,(r)=>r.toLowerCase().includes('idea')||r.toLowerCase().includes('caverna')||r.toLowerCase().includes('conocimiento'),(r)=>r.length>100,(r)=>r.length>80];
  const msgs=[['Buenas definiciones de términos.','Las definiciones son demasiado cortas. Desarrolla más cada término.'],['Buena exposición de la idea principal.','Desarrolla más la idea principal y la estructura del texto.'],['Buen uso del vocabulario filosófico de Platón.','Usa el vocabulario técnico: Ideas, mundo inteligible, episteme...'],['Buena relación con otro autor.','Desarrolla más la relación: semejanzas y diferencias.'],['Buena valoración personal.','Argumenta más tu valoración con ejemplos concretos.']];
  rs.forEach((r,i)=>{const ok=checks[i](r);if(ok)score+=1.5+0.5*(i===2?0.5:0);feedback.push({ok,msg:(ok?'✓ ':'✗ ')+msgs[i][ok?0:1]});});
  const fb=document.getElementById('examFeedback');
  fb.style.display='block';
  fb.innerHTML=`<div style="background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem"><h3 style="font-family:var(--font-display);font-size:1.2rem;margin-bottom:0.9rem">Resultado del Simulacro</h3><div style="font-family:var(--font-display);font-size:3rem;font-weight:900;color:var(--gold);margin-bottom:0.9rem">${Math.min(score,10).toFixed(1)} / 10</div><div style="display:flex;flex-direction:column;gap:0.5rem">${feedback.map(f=>`<div style="font-size:0.85rem;padding:0.55rem 0.85rem;border-radius:8px;background:${f.ok?'var(--teal-dim)':'var(--red-dim)'};border:1px solid ${f.ok?'rgba(62,207,178,0.3)':'rgba(224,92,92,0.3)'};color:${f.ok?'var(--teal)':'var(--red)'}">${f.msg}</div>`).join('')}</div><div style="margin-top:1.1rem;padding:0.9rem;background:var(--card2);border-radius:8px;font-size:0.83rem;color:var(--text2)"><strong style="color:var(--gold)">💡 Consejo:</strong> Recuerda que en la PAU se valora el vocabulario filosófico preciso, la estructura clara y la argumentación coherente.</div></div>`;
  fb.scrollIntoView({behavior:'smooth'});
}

// ===== THEME =====
document.getElementById('themeToggle').addEventListener('click', () => {
  const isDark=document.documentElement.dataset.theme==='dark';
  document.documentElement.dataset.theme=isDark?'light':'dark';
  document.getElementById('themeToggle').textContent=isDark?'☀️':'🌙';
});

// ===== HAMBURGER =====
document.getElementById('hamburger').addEventListener('click', () => document.getElementById('navLinks').classList.toggle('open'));

// ===== REVEAL =====
function observeReveal() {
  const obs=new IntersectionObserver(entries=>entries.forEach(e=>{if(e.isIntersecting){e.target.classList.add('visible');obs.unobserve(e.target);}}),{threshold:0.08});
  document.querySelectorAll('.reveal').forEach(el=>obs.observe(el));
}

function animateProgressBars() {
  const obs=new IntersectionObserver(entries=>entries.forEach(e=>{if(e.isIntersecting){e.target.querySelectorAll('.apl-fill[data-width]').forEach(bar=>{setTimeout(()=>{bar.style.width=bar.dataset.width;},300)});obs.unobserve(e.target);}}),{threshold:0.3});
  const prog=document.getElementById('progreso');
  if(prog) obs.observe(prog);
}

// ===== FORMULARIO SUGERENCIAS =====
async function enviarSugerencia(e) {
  e.preventDefault();
  const form = document.getElementById('sugerenciasForm');
  const btn = form.querySelector('button[type="submit"]');
  btn.textContent = '⏳ Enviando…';
  btn.disabled = true;
  try {
    const res = await fetch(form.action, {method:'POST',body:new FormData(form),headers:{Accept:'application/json'}});
    if(res.ok) {
      form.style.display='none';
      document.getElementById('sugerenciasOk').style.display='block';
      document.getElementById('formsprееAviso').style.display='none';
    } else {
      btn.textContent='❌ Error al enviar. Inténtalo de nuevo';
      btn.disabled=false;
    }
  } catch {
    btn.textContent='❌ Error de conexión';
    btn.disabled=false;
  }
}

// ===== BUSCADOR GLOBAL =====
const searchIndex = [
  // AUTORES
  {tipo:'autor',icon:'🏛️',titulo:'Platón',subtitulo:'Filósofo griego · Antigua (427-347 a.C.)',texto:'teoría de las ideas mundo inteligible sensible caverna mito alegoría república justicia alma dialéctica episteme doxa reminiscencia anamnesis filósofo rey política dualismo idealismo bien sol',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Platón')); if(c)c.click(); },300); },color:'var(--gold)'},
  {tipo:'autor',icon:'🏺',titulo:'Aristóteles',subtitulo:'Filósofo griego · Antigua (384-322 a.C.)',texto:'eudaimonia felicidad virtud término medio hilemorfismo materia forma alma cuerpo política animal polis bien hábito prudencia justicia metafísica cuatro causas empirismo crítica platón',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Aristóteles')); if(c)c.click(); },300); },color:'var(--teal)'},
  {tipo:'autor',icon:'🔍',titulo:'Descartes',subtitulo:'Racionalismo · Moderna (1596-1650)',texto:'duda metódica cogito ergo sum pienso luego existo res cogitans extensa dios racionalismo método evidencia análisis síntesis enumeración innatas sustancias dualismo mecanicismo',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Descartes')); if(c)c.click(); },300); },color:'var(--blue)'},
  {tipo:'autor',icon:'🔬',titulo:'Hume',subtitulo:'Empirismo · Moderna (1711-1776)',texto:'empirismo impresiones ideas causalidad hábito costumbre yo identidad personal escepticismo inducción guillotina es debe razón esclava pasiones moral sentimiento bunddle haz percepciones',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Hume')); if(c)c.click(); },300); },color:'var(--purple)'},
  {tipo:'autor',icon:'📐',titulo:'Kant',subtitulo:'Idealismo trascendental · Moderna (1724-1804)',texto:'imperativo categórico deber razón práctica pura fenómeno noúmeno cosa en sí formas a priori intuición espacio tiempo categorías juicios sintéticos analíticos ilustración mayoría edad sapere aude autonomía heteronomía dignidad',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Kant')); if(c)c.click(); },300); },color:'var(--teal)'},
  {tipo:'autor',icon:'⚡',titulo:'Nietzsche',subtitulo:'Vitalismo · Contemporánea (1844-1900)',texto:'muerte dios nihilismo voluntad poder superhombre übermensch eterno retorno transvaloración valores moral esclavos rebaño resentimiento apolíneo dionisíaco zaratustra gaya ciencia más allá bien mal',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Nietzsche')); if(c)c.click(); },300); },color:'var(--red)'},
  {tipo:'autor',icon:'✊',titulo:'Marx',subtitulo:'Materialismo histórico · Contemporánea (1818-1883)',texto:'alienación trabajo plusvalía capital clases sociales proletariado burguesía materialismo histórico dialéctico infraestructura superestructura ideología lucha clases revolución comunismo religión opio pueblo fetichismo mercancía',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Marx')); if(c)c.click(); },300); },color:'var(--red)'},
  // CONCEPTOS CLAVE
  {tipo:'concepto',icon:'💡',titulo:'Imperativo Categórico',subtitulo:'Kant · Ética',texto:'actúa solo según la máxima que puedas querer que sea ley universal deber incondicional autonomía moral razón práctica',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Kant')); if(c)c.click(); },300); },color:'var(--teal)'},
  {tipo:'concepto',icon:'🔦',titulo:'Mito de la Caverna',subtitulo:'Platón · Gnoseología',texto:'prisioneros sombras pared sol idea del bien ascenso conocimiento verdadero mundo sensible inteligible educación filósofo',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Platón')); if(c)c.click(); },300); },color:'var(--gold)'},
  {tipo:'concepto',icon:'⚙️',titulo:'Alienación',subtitulo:'Marx · Filosofía social',texto:'trabajador pierde producto trabajo esencia humana cuatro formas producto proceso otros seres genérico capital plusvalía',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Marx')); if(c)c.click(); },300); },color:'var(--red)'},
  {tipo:'concepto',icon:'🧠',titulo:'Cogito ergo sum',subtitulo:'Descartes · Gnoseología',texto:'pienso luego existo primera certeza duda metódica res cogitans sustancia pensante fundamento sistema cartesiano',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Descartes')); if(c)c.click(); },300); },color:'var(--blue)'},
  {tipo:'concepto',icon:'🌊',titulo:'Causalidad (Hume)',subtitulo:'Hume · Gnoseología',texto:'no hay impresión de la conexión causal hábito costumbre conjunción constante crítica a la causalidad necesaria inducción escepticismo',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Hume')); if(c)c.click(); },300); },color:'var(--purple)'},
  {tipo:'concepto',icon:'💪',titulo:'Voluntad de Poder',subtitulo:'Nietzsche · Ontología',texto:'fuerza creadora expansiva superhombre transvalora valores supera límites afirmación vida dionisíaco',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Nietzsche')); if(c)c.click(); },300); },color:'var(--red)'},
  {tipo:'concepto',icon:'😊',titulo:'Eudaimonía',subtitulo:'Aristóteles · Ética',texto:'felicidad florecimiento humano fin supremo vida virtud término medio actividad excelencia alma razón bien bien vivir',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Aristóteles')); if(c)c.click(); },300); },color:'var(--teal)'},
  {tipo:'concepto',icon:'👁️',titulo:'Noúmeno y Fenómeno',subtitulo:'Kant · Gnoseología',texto:'cosa en sí noúmeno incognoscible fenómeno cosa tal como aparece categorías formas a priori experiencia posible',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Kant')); if(c)c.click(); },300); },color:'var(--teal)'},
  {tipo:'concepto',icon:'☠️',titulo:'Muerte de Dios',subtitulo:'Nietzsche · Metafísica',texto:'dios ha muerto nosotros lo hemos matado nihilismo vacío valores pérdida fundamento cultura occidental transvaloración superhombre',accion:()=>{ document.querySelector('[data-filter="all"]').click(); setTimeout(()=>{ const cards=[...document.querySelectorAll('.autor-card')]; const c=cards.find(x=>x.textContent.includes('Nietzsche')); if(c)c.click(); },300); },color:'var(--red)'},
  // CORRIENTES
  {tipo:'corriente',icon:'📘',titulo:'Racionalismo',subtitulo:'Corriente filosófica · Moderna',texto:'razón fuente conocimiento ideas innatas método deductivo descartes spinoza leibniz certeza evidencia matemáticas',accion:()=>{ document.getElementById('autores').scrollIntoView({behavior:'smooth'}); },color:'var(--blue)'},
  {tipo:'corriente',icon:'📗',titulo:'Empirismo',subtitulo:'Corriente filosófica · Moderna',texto:'experiencia fuente conocimiento tabula rasa impresiones locke berkeley hume inducción a posteriori sentidos',accion:()=>{ document.getElementById('autores').scrollIntoView({behavior:'smooth'}); },color:'var(--teal)'},
  {tipo:'corriente',icon:'📙',titulo:'Idealismo Trascendental',subtitulo:'Kant · Moderna',texto:'síntesis racionalismo empirismo giro copernicano formas a priori categorías fenómeno noúmeno sujeto constituyente',accion:()=>{ document.getElementById('autores').scrollIntoView({behavior:'smooth'}); },color:'var(--gold)'},
  {tipo:'corriente',icon:'📕',titulo:'Materialismo Histórico',subtitulo:'Marx · Contemporánea',texto:'condiciones materiales producción infraestructura superestructura lucha clases dialéctica historia revolución',accion:()=>{ document.getElementById('autores').scrollIntoView({behavior:'smooth'}); },color:'var(--red)'},
  // SECCIONES
  {tipo:'sección',icon:'🎮',titulo:'Juegos Filosóficos',subtitulo:'8 juegos interactivos',texto:'quién soy wordle parejas ordenar ahorcado verdad mentira definición ruleta filosófica',accion:()=>document.getElementById('juegos').scrollIntoView({behavior:'smooth'}),color:'var(--purple)'},
  {tipo:'sección',icon:'🃏',titulo:'Flashcards',subtitulo:'Repaso rápido de conceptos',texto:'tarjetas conceptos autores flip girar voltear repasar memorizar',accion:()=>document.getElementById('flashcards').scrollIntoView({behavior:'smooth'}),color:'var(--blue)'},
  {tipo:'sección',icon:'📝',titulo:'Tests Autocorregibles',subtitulo:'Comprueba tu nivel',texto:'test preguntas autocorrección respuestas nivel ejercicios evaluar',accion:()=>document.getElementById('tests').scrollIntoView({behavior:'smooth'}),color:'var(--teal)'},
  {tipo:'sección',icon:'⏱️',titulo:'Simulacro de Examen',subtitulo:'90 minutos como en la PAU real',texto:'simulacro examen tiempo 90 minutos corregir nota selectividad práctica',accion:()=>document.getElementById('simulacro').scrollIntoView({behavior:'smooth'}),color:'var(--gold)'},
  {tipo:'sección',icon:'📚',titulo:'Exámenes Anteriores',subtitulo:'2015–2026 con orientaciones',texto:'examen año anterior resuelto corrección orientación real selectividad 2015 2016 2017 2018 2019 2020 2021 2022 2023 2024 2025',accion:()=>document.getElementById('examenes').scrollIntoView({behavior:'smooth'}),color:'var(--red)'},
  {tipo:'sección',icon:'🎧',titulo:'Podcasts Recomendados',subtitulo:'12 podcasts y canales de filosofía',texto:'podcast audio spotify ivoox youtube escuchar filosofía bachillerato',accion:()=>document.getElementById('podcasts').scrollIntoView({behavior:'smooth'}),color:'var(--purple)'},
  {tipo:'sección',icon:'📖',titulo:'Libros Recomendados',subtitulo:'25 libros seleccionados',texto:'libros leer originales divulgación pau recomendados bibliografía estudio',accion:()=>document.getElementById('libros').scrollIntoView({behavior:'smooth'}),color:'var(--gold)'},
  {tipo:'sección',icon:'💬',titulo:'Sugerencias',subtitulo:'Dinos qué quieres que añadamos',texto:'sugerencia mejora propuesta comentario idea añadir',accion:()=>document.getElementById('sugerencias').scrollIntoView({behavior:'smooth'}),color:'var(--teal)'},
];

function highlight(text, query) {
  if(!query) return text;
  const escaped = query.replace(/[.*+?^${}()|[\]\\]/g,'\\$&');
  return text.replace(new RegExp(`(${escaped})`, 'gi'), '<mark>$1</mark>');
}

function buscarFilo(q) {
  const btn = document.getElementById('buscadorClear');
  const sugs = document.getElementById('sugerenciasRapidas');
  const res = document.getElementById('buscadorResultados');
  btn.style.display = q ? 'block' : 'none';
  sugs.style.display = q ? 'none' : 'flex';
  if(!q.trim()) { res.innerHTML=''; return; }
  const query = q.toLowerCase().trim();
  const results = searchIndex.filter(item =>
    item.titulo.toLowerCase().includes(query) ||
    item.subtitulo.toLowerCase().includes(query) ||
    item.texto.toLowerCase().includes(query)
  ).slice(0,8);
  if(!results.length) {
    res.innerHTML=`<div style="text-align:center;padding:2rem;color:var(--text3)"><div style="font-size:2rem;margin-bottom:0.5rem">🔭</div><p>Sin resultados para "<strong style="color:var(--text2)">${q}</strong>".<br>Prueba con otro término.</p></div>`;
    return;
  }
  const typeColors = {autor:'var(--gold)',concepto:'var(--teal)',corriente:'var(--blue)',sección:'var(--purple)'};
  const typeBg = {autor:'var(--gold-dim)',concepto:'var(--teal-dim)',corriente:'var(--blue-dim)',sección:'var(--purple-dim)'};
  res.innerHTML = results.map(r => `
    <div class="search-result" onclick="(${r.accion.toString()})();document.getElementById('buscadorInput').blur()">
      <div class="search-result-icon">${r.icon}</div>
      <div class="search-result-body">
        <div class="search-result-title">${highlight(r.titulo, q)}</div>
        <div class="search-result-subtitle">${r.subtitulo}</div>
        <div class="search-result-excerpt">${highlight(r.texto.split(' ').slice(0,12).join(' ')+'…', q)}</div>
      </div>
      <span class="search-result-type" style="background:${typeBg[r.tipo]||'var(--card2)'};color:${typeColors[r.tipo]||'var(--text2)'}">${r.tipo}</span>
    </div>`).join('');
}

function buscarYFocar(term) {
  const input = document.getElementById('buscadorInput');
  input.value = term;
  buscarFilo(term);
  document.getElementById('buscador').scrollIntoView({behavior:'smooth'});
  setTimeout(()=>input.focus(), 400);
}

function limpiarBusqueda() {
  const input = document.getElementById('buscadorInput');
  input.value='';
  buscarFilo('');
  input.focus();
}

// ===== POPUP SOCIAL =====
function closePopup() {
  document.getElementById('socialPopup').classList.remove('show');
  localStorage.setItem('popupClosed', Date.now());
}
setTimeout(() => {
  const last = localStorage.getItem('popupClosed');
  const now = Date.now();
  if(!last || now - last > 24*60*60*1000) {
    document.getElementById('socialPopup').classList.add('show');
  }
}, 15000);


// ===== CALCULADORA DE NOTA =====
function calcularNota() {
  const vals = ['n1a','n1b','n1c','n2a','n2b'].map(id => {
    const v = parseFloat(document.getElementById(id).value) || 0;
    return Math.min(2, Math.max(0, v));
  });
  const total = vals.reduce((a,b) => a+b, 0);
  const nota = Math.min(10, total);
  const el = document.getElementById('notaFinal');
  const label = document.getElementById('notaLabel');
  const cont = document.getElementById('resultadoCalc');
  el.textContent = nota.toFixed(2);
  let color, msg, border;
  if(nota >= 9) { color='var(--gold)'; msg='🏆 Sobresaliente — ¡Excelente trabajo!'; border='rgba(201,168,76,0.5)'; }
  else if(nota >= 7) { color='var(--teal)'; msg='✅ Notable — Muy buena nota.'; border='rgba(62,207,178,0.4)'; }
  else if(nota >= 5) { color='var(--blue)'; msg='📘 Aprobado — Sigue practicando.'; border='rgba(91,141,238,0.4)'; }
  else { color='var(--red)'; msg='❌ Suspenso — Repasa y vuelve a intentarlo.'; border='rgba(224,92,92,0.4)'; }
  el.style.color = color;
  label.textContent = msg;
  label.style.color = color;
  cont.style.borderColor = border;
}


// ===== DATOS CURIOSOS =====
const curiosidadesData = [
  { icon:'🏋️', autor:'Platón', color:'var(--gold)', colorDim:'var(--gold-dim)', titulo:'El luchador campeón',
    texto:'«Platón» significa <strong>ancho de espaldas</strong> en griego. Su nombre real era <strong>Aristocles</strong>. Fue luchador y compitió en los Juegos Ístmicos. Su maestro de gimnasia le puso el apodo por su complexión atlética.' },
  { icon:'🐬', autor:'Aristóteles', color:'var(--teal)', colorDim:'var(--teal-dim)', titulo:'El primer biólogo del mundo',
    texto:'Aristóteles catalogó más de <strong>500 especies animales</strong> e identificó correctamente que los <strong>delfines son mamíferos</strong> más de 2.000 años antes que nadie más. También describió la pesca con caña, la migración de aves y el desarrollo embrionario.' },
  { icon:'🛏️', autor:'Descartes', color:'var(--blue)', colorDim:'var(--blue-dim)', titulo:'El filósofo dormilón',
    texto:'Descartes era famoso por <strong>quedarse en cama hasta el mediodía</strong>. Sus mejores ideas se le ocurrían al despertar. Cuando la reina Cristina de Suecia le obligó a dar clases filosóficas a las <strong>5 de la mañana</strong> en el frío de Estocolmo, murió de neumonía a los tres meses.' },
  { icon:'🎭', autor:'Hume', color:'var(--purple)', colorDim:'var(--purple-dim)', titulo:'«Le bon David»',
    texto:'Hume era conocido en París como <strong>«le bon David»</strong> por su simpatía y sentido del humor. Era bibliotecario, secretario de embajada y asesor político. Los salones parisinos le adoraban, aunque sus ideas sobre la religión escandalizaban a la Iglesia.' },
  { icon:'⏰', autor:'Kant', color:'var(--blue)', colorDim:'var(--blue-dim)', titulo:'El reloj humano de Königsberg',
    texto:'Kant era tan puntual en sus paseos diarios que los vecinos <strong>ajustaban sus relojes</strong> al verle pasar. Solo rompió esa rutina dos veces en su vida: al leer el <em>Emilio</em> de Rousseau y al enterarse de la Revolución Francesa. <strong>Nunca salió de Königsberg</strong>.' },
  { icon:'📰', autor:'Marx', color:'var(--red)', colorDim:'var(--red-dim)', titulo:'Vivía en la pobreza',
    texto:'Marx vivió en extrema pobreza en Londres. Tres de sus siete hijos murieron de pequeños. Su principal fuente de ingresos era escribir para el <strong>New York Tribune</strong>. <strong>Friedrich Engels</strong> le financió económicamente durante décadas para que pudiera escribir <em>El Capital</em>.' },
  { icon:'🎸', autor:'Nietzsche', color:'var(--gold)', colorDim:'var(--gold-dim)', titulo:'El músico fracasado',
    texto:'Nietzsche era un pianista brillante. Wagner decía que si no se hubiera dedicado a la filosofía habría sido un gran músico. Rompió con Wagner porque consideró que su música se volvía <strong>«enfermiza y cristiana»</strong>. Sufrió un colapso mental a los 44 años y ya no se recuperó.' },
  { icon:'🦉', autor:'Ortega', color:'var(--teal)', colorDim:'var(--teal-dim)', titulo:'El filósofo de café',
    texto:'Ortega y Gasset desarrolló gran parte de su filosofía en los <strong>cafés madrileños</strong>, especialmente en la Granja El Henar. Fue diputado, fundó la <em>Revista de Occidente</em> y durante el franquismo vivió exiliado, siendo figura intelectual de referencia en toda la España de posguerra.' },
  { icon:'🪂', autor:'Wittgenstein', color:'var(--purple)', colorDim:'var(--purple-dim)', titulo:'Voluntario de guerra',
    texto:'Durante la Primera Guerra Mundial, Wittgenstein se alistó <strong>voluntariamente</strong> en el ejército austriaco y pidió ser destinado a los puestos de mayor peligro. En las trincheras escribió el <em>Tractatus Logico-Philosophicus</em>, uno de los libros filosóficos más influyentes del siglo XX.' },
  { icon:'🧮', autor:'Habermas', color:'var(--blue)', colorDim:'var(--blue-dim)', titulo:'El filósofo más citado vivo',
    texto:'Jürgen Habermas (nacido en 1929) es considerado el <strong>filósofo vivo más citado del mundo</strong> en ciencias sociales. A los 15 años escuchó las transmisiones de los juicios de Núremberg por radio, lo que le marcó profundamente y orientó toda su filosofía hacia la democracia y la razón comunicativa.' },
];

function renderCuriosidades() {
  const grid = document.getElementById('curiosidadesGrid');
  if(!grid) return;
  grid.innerHTML = curiosidadesData.map((c,i) => `
    <div class="pau-card reveal" style="border-left:3px solid ${c.color};cursor:default;animation-delay:${i*0.05}s">
      <div style="display:flex;align-items:center;gap:0.75rem;margin-bottom:0.85rem">
        <div style="width:42px;height:42px;border-radius:10px;background:${c.colorDim};border:1px solid ${c.color}33;display:flex;align-items:center;justify-content:center;font-size:1.4rem;flex-shrink:0">${c.icon}</div>
        <div>
          <div style="font-size:0.68rem;font-weight:700;color:${c.color};text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.1rem">${c.autor}</div>
          <div style="font-weight:700;font-size:0.95rem">${c.titulo}</div>
        </div>
      </div>
      <p style="font-size:0.83rem;color:var(--text2);line-height:1.7;margin:0">${c.texto}</p>
    </div>`).join('');
  observeReveal();
}


// ===== MAPA DE RELACIONES =====
const relacionesData = [
  { par:'Platón — Aristóteles', tagColor:'var(--gold)', emoji:'🏛️',
    semejanzas:['Ambos buscan la verdad universal y objetiva','Los dos conciben la ética ligada a la política','Para ambos la razón es la facultad superior humana','Comparten el ideal del Estado justo'],
    diferencias:['Platón: Ideas separadas del mundo · Aristóteles: formas en la materia','Platón: alma inmortal y separada del cuerpo · Aristóteles: alma como forma del cuerpo','Platón: conocimiento como recuerdo (anamnesis) · Aristóteles: parte de los sentidos','Platón: filósofo-rey · Aristóteles: deliberación entre ciudadanos'],
    frec:'⭐⭐⭐ Muy frecuente en la PAU' },
  { par:'Descartes — Hume', tagColor:'var(--blue)', emoji:'💡',
    semejanzas:['Ambos buscan el fundamento seguro del conocimiento','Los dos reflexionan sobre la causalidad','Ambos cuestionan el conocimiento previo no examinado'],
    diferencias:['Descartes: racionalista (razón como fuente) · Hume: empirista (experiencia como fuente)','Descartes: ideas innatas · Hume: todas las ideas vienen de impresiones','Descartes: certeza del yo pensante · Hume: el yo es solo un haz de percepciones','Descartes: la causalidad es racional · Hume: es solo hábito y costumbre'],
    frec:'⭐⭐⭐ Muy frecuente en la PAU' },
  { par:'Hume — Kant', tagColor:'var(--purple)', emoji:'🌐',
    semejanzas:['Ambos reflexionan sobre los límites del conocimiento humano','Los dos cuestionan la metafísica dogmática tradicional','Ambos tienen una visión crítica de la causalidad'],
    diferencias:['Hume: la causalidad es solo hábito · Kant: la causalidad es una categoría a priori del entendimiento','Hume: escepticismo · Kant: fundamentación crítica del conocimiento','Hume: la moral es sentimiento · Kant: la moral es razón pura práctica','Hume: niega el yo sustancial · Kant: el yo trascendental es condición del conocimiento'],
    frec:'⭐⭐⭐ Muy frecuente en la PAU' },
  { par:'Platón — Kant', tagColor:'var(--teal)', emoji:'🔮',
    semejanzas:['Ambos distinguen entre el mundo de la apariencia y el de la verdad','Los dos conciben una ética de principios universales','Para ambos, la razón es la facultad suprema','Ambos valoran la autonomía moral'],
    diferencias:['Platón: Ideas ontológicamente reales · Kant: las categorías son formas del sujeto, no del ser','Platón: el bien es un Idea objetiva · Kant: el bien depende del imperativo de la razón práctica','Platón: el conocimiento es recuerdo · Kant: es síntesis de experiencia y categorías a priori','Platón: teoría del Estado ideal · Kant: paz perpetua y derecho cosmopolita'],
    frec:'⭐⭐ Frecuente' },
  { par:'Marx — Nietzsche', tagColor:'var(--red)', emoji:'⚡',
    semejanzas:['Ambos son críticos radicales de la sociedad burguesa y occidental','Los dos cuestionan los valores dominantes de su época','Ambos parten del sufrimiento real del ser humano concreto','Ambos rechazan el idealismo de Hegel (a su modo)'],
    diferencias:['Marx: la alienación es económica y social · Nietzsche: es cultural y de valores','Marx: solución colectiva y revolucionaria · Nietzsche: solución individual y aristocrática','Marx: materialismo histórico · Nietzsche: voluntad de poder y vitalismo','Marx: el superhombre es el proletariado liberado · Nietzsche: el superhombre es el individuo creador de valores'],
    frec:'⭐⭐ Frecuente' },
  { par:'Aristóteles — Kant', tagColor:'var(--blue)', emoji:'⚖️',
    semejanzas:['Ambos buscan una fundamentación racional de la ética','Los dos conciben al ser humano como fin en sí mismo (en sus términos)','Para ambos, la razón práctica tiene un papel central en la moral'],
    diferencias:['Aristóteles: ética de la virtud y la eudaimonia · Kant: ética del deber y el imperativo','Aristóteles: el bien depende del contexto y la polis · Kant: el bien moral es universal e incondicional','Aristóteles: teleológico (fin natural) · Kant: deontológico (deber racional)','Aristóteles: la virtud se aprende con la práctica · Kant: la ley moral es apriorística'],
    frec:'⭐⭐ Frecuente' },
  { par:'Marx — Platón', tagColor:'var(--gold)', emoji:'🏗️',
    semejanzas:['Ambos proponen una organización racional de la sociedad','Los dos critican la sociedad de su tiempo','Ambos piensan que las condiciones materiales/sociales forman al individuo'],
    diferencias:['Platón: el Estado ideal es estático y jerárquico · Marx: la sociedad ideal llega por revolución histórica','Platón: el conocimiento de las Ideas es la clave · Marx: la praxis transformadora es la clave','Platón: idealismo · Marx: materialismo histórico','Platón: la injusticia viene del alma desequilibrada · Marx: viene de la explotación económica'],
    frec:'⭐ Ocasional' },
  { par:'Descartes — Platón', tagColor:'var(--teal)', emoji:'💭',
    semejanzas:['Ambos son racionalistas: la razón es la fuente del conocimiento verdadero','Los dos distinguen entre el mundo aparente y el verdadero','Ambos defienden la existencia de ideas o conocimientos independientes de los sentidos','Los dos tienen una visión dualista del ser humano (alma/cuerpo)'],
    diferencias:['Platón: las Ideas existen independientemente en el mundo inteligible · Descartes: las ideas innatas están en la mente del sujeto','Platón: el conocimiento es reminiscencia · Descartes: es deducción racional a partir del cogito','Platón: el alma es inmortal y transmigra · Descartes: la mente es res cogitans, no transmigra','Platón: mito como recurso filosófico · Descartes: método matemático estricto'],
    frec:'⭐ Ocasional' },
];

let relacionAbierta = null;

function renderRelaciones() {
  const grid = document.getElementById('relacionesGrid');
  if(!grid) return;
  grid.innerHTML = relacionesData.map((r,i) => `
    <div class="pau-card reveal" style="cursor:pointer;border:1px solid var(--border);transition:all 0.25s" onclick="toggleRelacion(${i})" id="rel-card-${i}">
      <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:0.65rem">
        <div style="display:flex;align-items:center;gap:0.6rem">
          <span style="font-size:1.4rem">${r.emoji}</span>
          <div style="font-weight:800;font-size:0.95rem">${r.par}</div>
        </div>
        <span style="font-size:1rem;color:var(--text3);transition:transform 0.25s" id="rel-arrow-${i}">▸</span>
      </div>
      <div style="font-size:0.72rem;color:${r.tagColor};font-weight:600;margin-bottom:0.5rem">${r.frec}</div>
      <div id="rel-body-${i}" style="display:none;margin-top:0.75rem;border-top:1px solid var(--border);padding-top:0.85rem">
        <div style="margin-bottom:0.85rem">
          <div style="font-size:0.7rem;font-weight:800;color:var(--teal);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.4rem">✓ Semejanzas</div>
          <ul style="list-style:none;padding:0;margin:0;display:flex;flex-direction:column;gap:0.3rem">
            ${r.semejanzas.map(s=>`<li style="font-size:0.8rem;color:var(--text2);padding:0.3rem 0.6rem;background:var(--teal-dim);border-radius:6px;border-left:2px solid var(--teal)">• ${s}</li>`).join('')}
          </ul>
        </div>
        <div>
          <div style="font-size:0.7rem;font-weight:800;color:var(--red);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.4rem">✗ Diferencias</div>
          <ul style="list-style:none;padding:0;margin:0;display:flex;flex-direction:column;gap:0.3rem">
            ${r.diferencias.map(d=>`<li style="font-size:0.8rem;color:var(--text2);padding:0.3rem 0.6rem;background:var(--red-dim);border-radius:6px;border-left:2px solid var(--red)">• ${d}</li>`).join('')}
          </ul>
        </div>
      </div>
    </div>`).join('');
  observeReveal();
}

function toggleRelacion(i) {
  const body = document.getElementById('rel-body-'+i);
  const arrow = document.getElementById('rel-arrow-'+i);
  const card = document.getElementById('rel-card-'+i);
  const open = body.style.display === 'block';
  if(!open && relacionAbierta !== null && relacionAbierta !== i) {
    document.getElementById('rel-body-'+relacionAbierta).style.display='none';
    document.getElementById('rel-arrow-'+relacionAbierta).style.transform='rotate(0deg)';
    document.getElementById('rel-card-'+relacionAbierta).style.borderColor='var(--border)';
  }
  body.style.display = open ? 'none' : 'block';
  arrow.style.transform = open ? 'rotate(0deg)' : 'rotate(90deg)';
  card.style.borderColor = open ? 'var(--border)' : 'rgba(201,168,76,0.4)';
  relacionAbierta = open ? null : i;
}

// ===== FECHA AUTOMÁTICA =====
(function() {
  const now = new Date();
  const opciones = { day: 'numeric', month: 'long', year: 'numeric' };
  const fechaLarga = now.toLocaleDateString('es-ES', opciones);
  const fechaCorta = now.toLocaleDateString('es-ES', { day: 'numeric', month: 'short', year: 'numeric' });
  const badge = document.getElementById('heroBadge');
  if(badge) badge.textContent = `✦ Actualizado · ${fechaLarga} · PAU Andalucía`;
  const fechaHoy = document.getElementById('fechaHoy');
  if(fechaHoy) fechaHoy.textContent = `Hoy · ${fechaCorta}`;
  const fechaFooter = document.getElementById('fechaFooter');
  if(fechaFooter) fechaFooter.textContent = `Actualizada a ${fechaLarga}`;
})();
renderAutores();
renderQuiz();
renderTimeline();
renderCuriosidades();
renderRelaciones();
renderBanco(bancoData);
renderProgreso();
renderExamenes();
renderPodcasts();
renderLibros();
updateFC();
observeReveal();
animateProgressBars();
setTimeout(()=>{ const f=document.getElementById('radialFill'); if(f) f.style.strokeDashoffset=314*(1-0.30); },500);
</script>
</body>
</html>
