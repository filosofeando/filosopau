<!DOCTYPE html>
<html lang="es" data-theme="dark">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>FilosoFEANDO — PAU Filosofía Andalucía</title>
<meta name="description" content="La plataforma gratuita más completa para preparar la PAU de Filosofía en Andalucía. Temario, tests, exámenes corregidos, flashcards y más.">
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-RW528WSNZ8"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-RW528WSNZ8');
</script>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500;600&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#0d0f14;--bg2:#13161e;--bg3:#1a1e28;--card:#1e2233;--card2:#252a3a;
  --border:rgba(255,255,255,0.08);--gold:#c9a84c;--gold2:#e8c96a;--gold-dim:rgba(201,168,76,0.15);
  --teal:#3ecfb2;--teal-dim:rgba(62,207,178,0.12);--red:#e05c5c;--red-dim:rgba(224,92,92,0.12);
  --blue:#5b8dee;--blue-dim:rgba(91,141,238,0.12);--purple:#a78bfa;--purple-dim:rgba(167,139,250,0.12);
  --text:#e8eaf0;--text2:#9aa0b8;--text3:#636880;
  --radius:14px;--radius-sm:8px;--shadow:0 8px 32px rgba(0,0,0,0.4);
  --transition:0.25s cubic-bezier(0.4,0,0.2,1);
  --font-display:'Playfair Display',serif;--font-body:'DM Sans',sans-serif;--font-mono:'DM Mono',monospace;
}
[data-theme="light"]{
  --bg:#f5f3ee;--bg2:#ede9e0;--bg3:#e3ddd2;--card:#fff;--card2:#f9f7f3;
  --border:rgba(0,0,0,0.08);--text:#1a1c24;--text2:#4a4e60;--text3:#8a8ea8;
  --shadow:0 8px 32px rgba(0,0,0,0.1);
}
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{font-family:var(--font-body);background:var(--bg);color:var(--text);line-height:1.65;overflow-x:hidden;transition:background var(--transition),color var(--transition)}
a{color:var(--gold);text-decoration:none;transition:color var(--transition)}
a:hover{color:var(--gold2)}
button{cursor:pointer;font-family:var(--font-body);border:none;outline:none}
h1,h2,h3,h4,h5{font-family:var(--font-display);line-height:1.2}
::-webkit-scrollbar{width:5px}
::-webkit-scrollbar-track{background:var(--bg)}
::-webkit-scrollbar-thumb{background:var(--gold);border-radius:3px}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:900;background:rgba(13,15,20,0.9);backdrop-filter:blur(20px);border-bottom:1px solid var(--border);padding:0 1.5rem;height:60px;display:flex;align-items:center;justify-content:space-between;transition:background var(--transition)}
[data-theme="light"] nav{background:rgba(245,243,238,0.95)}
.nav-brand{font-family:var(--font-display);font-size:1.25rem;font-weight:700;color:var(--gold);display:flex;align-items:center;gap:0.4rem;white-space:nowrap}
.nav-brand span{color:var(--text);font-weight:400}
.nav-links{display:flex;align-items:center;gap:0.15rem;flex-wrap:nowrap}
.nav-links a{padding:0.35rem 0.7rem;border-radius:var(--radius-sm);font-size:0.82rem;font-weight:500;color:var(--text2);transition:all var(--transition);white-space:nowrap}
.nav-links a:hover{color:var(--text);background:var(--card)}
.nav-premium{background:linear-gradient(135deg,var(--gold),#a8732e);color:#0d0f14 !important;font-weight:700 !important}
.nav-premium:hover{transform:translateY(-1px);box-shadow:0 4px 16px rgba(201,168,76,0.4)}
.theme-toggle{width:34px;height:34px;border-radius:50%;background:var(--card);border:1px solid var(--border);display:flex;align-items:center;justify-content:center;font-size:0.95rem;transition:all var(--transition);color:var(--text2);flex-shrink:0}
.theme-toggle:hover{border-color:var(--gold);color:var(--gold)}
.hamburger{display:none;flex-direction:column;gap:4px;padding:8px;background:none;cursor:pointer}
.hamburger span{display:block;width:20px;height:2px;background:var(--text2);border-radius:2px;transition:all var(--transition)}

/* HERO */
.hero{min-height:100vh;display:flex;align-items:center;justify-content:center;padding:7rem 2rem 5rem;position:relative;overflow:hidden;background:radial-gradient(ellipse 80% 60% at 50% -10%,rgba(201,168,76,0.1) 0%,transparent 70%)}
.hero-grid{position:absolute;inset:0;background-image:linear-gradient(var(--border) 1px,transparent 1px),linear-gradient(90deg,var(--border) 1px,transparent 1px);background-size:60px 60px;mask-image:radial-gradient(ellipse 80% 70% at 50% 50%,black 20%,transparent 80%)}
.hero-content{max-width:820px;text-align:center;position:relative;z-index:2}
.hero-badge{display:inline-flex;align-items:center;gap:0.5rem;background:var(--gold-dim);border:1px solid rgba(201,168,76,0.3);color:var(--gold);padding:0.35rem 1rem;border-radius:50px;font-size:0.78rem;font-weight:700;letter-spacing:0.05em;text-transform:uppercase;margin-bottom:1.75rem;animation:fadeUp 0.8s ease both}
.hero h1{font-size:clamp(2.5rem,7vw,4.8rem);font-weight:900;color:var(--text);margin-bottom:1.25rem;animation:fadeUp 0.8s 0.15s ease both;line-height:1.05}
.hero h1 em{color:var(--gold);font-style:normal}
.hero-sub{font-size:1.1rem;color:var(--text2);max-width:580px;margin:0 auto 2.5rem;animation:fadeUp 0.8s 0.3s ease both}
.hero-ctas{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;animation:fadeUp 0.8s 0.45s ease both}
.btn-primary{padding:0.8rem 1.75rem;border-radius:var(--radius);background:linear-gradient(135deg,var(--gold),#a8732e);color:#0d0f14;font-weight:700;font-size:0.95rem;transition:all var(--transition);box-shadow:0 4px 20px rgba(201,168,76,0.3);display:inline-block;text-align:center}
.btn-primary:hover{transform:translateY(-2px);box-shadow:0 8px 30px rgba(201,168,76,0.45);color:#0d0f14}
.btn-secondary{padding:0.8rem 1.75rem;border-radius:var(--radius);background:var(--card);border:1px solid var(--border);color:var(--text);font-weight:600;font-size:0.95rem;transition:all var(--transition);display:inline-block;text-align:center}
.btn-secondary:hover{border-color:var(--gold);transform:translateY(-2px)}
.hero-stats{display:flex;gap:2.5rem;justify-content:center;margin-top:3.5rem;animation:fadeUp 0.8s 0.6s ease both;flex-wrap:wrap}
.stat{text-align:center}
.stat-num{font-family:var(--font-display);font-size:1.9rem;font-weight:700;color:var(--gold)}
.stat-label{font-size:0.75rem;color:var(--text3);letter-spacing:0.05em;text-transform:uppercase}

/* SOCIAL BANNER */
.social-banner{background:linear-gradient(135deg,var(--bg2),var(--bg3));border-top:1px solid var(--border);border-bottom:1px solid var(--border);padding:1.5rem 2rem}
.social-banner-inner{max-width:1200px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;gap:1.5rem;flex-wrap:wrap}
.social-banner-text h3{font-size:1.05rem;font-weight:700;margin-bottom:0.25rem}
.social-banner-text p{font-size:0.85rem;color:var(--text2)}
.social-banner-text em{color:var(--gold);font-style:normal;font-weight:700}
.social-btns{display:flex;gap:0.75rem;flex-wrap:wrap}
.btn-tiktok{display:inline-flex;align-items:center;gap:0.5rem;background:linear-gradient(135deg,#010101,#1a1a1a);color:#fff;padding:0.65rem 1.25rem;border-radius:var(--radius-sm);font-weight:700;font-size:0.875rem;border:1px solid rgba(255,255,255,0.1);transition:all var(--transition)}
.btn-tiktok:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(0,0,0,0.4);color:#fff}
.btn-instagram{display:inline-flex;align-items:center;gap:0.5rem;background:linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045);color:#fff;padding:0.65rem 1.25rem;border-radius:var(--radius-sm);font-weight:700;font-size:0.875rem;transition:all var(--transition)}
.btn-instagram:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(131,58,180,0.4);color:#fff}
.btn-paypal{display:inline-flex;align-items:center;gap:0.5rem;background:#0070ba;color:#fff;padding:0.65rem 1.25rem;border-radius:var(--radius-sm);font-weight:700;font-size:0.875rem;transition:all var(--transition)}
.btn-paypal:hover{transform:translateY(-2px);box-shadow:0 6px 20px rgba(0,112,186,0.4);color:#fff}

/* SECTIONS */
section{padding:5rem 2rem}
.container{max-width:1200px;margin:0 auto}
.section-label{font-size:0.72rem;font-weight:700;letter-spacing:0.12em;text-transform:uppercase;color:var(--gold);margin-bottom:0.6rem}
.section-title{font-size:clamp(1.7rem,4vw,2.6rem);font-weight:800;color:var(--text);margin-bottom:0.85rem}
.section-sub{font-size:0.95rem;color:var(--text2);max-width:560px}
.tag{display:inline-block;padding:0.2rem 0.6rem;border-radius:50px;font-size:0.72rem;font-weight:600}
.tag-gold{background:var(--gold-dim);color:var(--gold)}
.tag-teal{background:var(--teal-dim);color:var(--teal)}
.tag-red{background:var(--red-dim);color:var(--red)}
.tag-blue{background:var(--blue-dim);color:var(--blue)}
.tag-purple{background:var(--purple-dim);color:var(--purple)}

/* PAU INFO */
.pau-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-top:2.5rem}
.pau-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.6rem;transition:all var(--transition)}
.pau-card:hover{border-color:rgba(201,168,76,0.3);transform:translateY(-3px);box-shadow:var(--shadow)}
.pau-card-icon{font-size:1.75rem;margin-bottom:0.85rem}
.pau-card h3{font-size:1.05rem;font-weight:700;margin-bottom:0.65rem}
.pau-card p,.pau-card ul{font-size:0.875rem;color:var(--text2)}
.pau-card ul{padding-left:1.1rem}
.pau-card ul li{margin-bottom:0.35rem}
.structure-table{width:100%;border-collapse:collapse;margin-top:0.85rem;font-size:0.83rem}
.structure-table th{background:var(--gold-dim);color:var(--gold);padding:0.55rem 0.85rem;text-align:left;font-weight:600}
.structure-table td{padding:0.55rem 0.85rem;border-bottom:1px solid var(--border);color:var(--text2)}
.structure-table tr:hover td{background:var(--card2)}

/* AUTORES */
.autores-tabs{display:flex;gap:0.5rem;flex-wrap:wrap;margin-top:2.5rem;margin-bottom:1.75rem}
.tab-btn{padding:0.45rem 1rem;border-radius:50px;font-size:0.82rem;font-weight:600;background:var(--card);border:1px solid var(--border);color:var(--text2);transition:all var(--transition)}
.tab-btn:hover,.tab-btn.active{background:var(--gold);color:#0d0f14;border-color:var(--gold)}
.autores-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1.25rem}
.autor-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.6rem;cursor:pointer;transition:all var(--transition);position:relative;overflow:hidden}
.autor-card::before{content:'';position:absolute;inset:0;background:linear-gradient(135deg,var(--gold-dim),transparent);opacity:0;transition:opacity var(--transition)}
.autor-card:hover{border-color:rgba(201,168,76,0.4);transform:translateY(-4px);box-shadow:0 12px 40px rgba(0,0,0,0.3)}
.autor-card:hover::before{opacity:1}
.autor-era{font-size:0.7rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;color:var(--gold);margin-bottom:0.4rem}
.autor-name{font-size:1.25rem;font-weight:800;margin-bottom:0.25rem;position:relative}
.autor-dates{font-size:0.78rem;color:var(--text3);margin-bottom:0.85rem;font-family:var(--font-mono)}
.autor-desc{font-size:0.85rem;color:var(--text2);margin-bottom:1.1rem;line-height:1.55}
.autor-tags{display:flex;gap:0.35rem;flex-wrap:wrap;margin-bottom:1.1rem}
.autor-progress{display:flex;align-items:center;gap:0.65rem}
.progress-bar{flex:1;height:4px;background:var(--bg3);border-radius:2px;overflow:hidden}
.progress-fill{height:100%;background:linear-gradient(90deg,var(--gold),var(--gold2));border-radius:2px;transition:width 1s ease}
.progress-label{font-size:0.72rem;color:var(--text3);min-width:28px;text-align:right;font-family:var(--font-mono)}

/* MODAL */
.modal-overlay{position:fixed;inset:0;background:rgba(0,0,0,0.85);backdrop-filter:blur(8px);z-index:2000;display:flex;align-items:flex-start;justify-content:center;padding:2rem;overflow-y:auto;opacity:0;pointer-events:none;transition:opacity var(--transition)}
.modal-overlay.open{opacity:1;pointer-events:all}
.modal{background:var(--bg2);border:1px solid var(--border);border-radius:20px;width:100%;max-width:860px;margin:auto;transform:translateY(30px);transition:transform var(--transition)}
.modal-overlay.open .modal{transform:translateY(0)}
.modal-header{padding:1.75rem 2rem 1.25rem;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:flex-start;background:linear-gradient(135deg,var(--gold-dim),transparent);border-radius:20px 20px 0 0}
.modal-close{width:34px;height:34px;border-radius:50%;background:var(--card);border:1px solid var(--border);color:var(--text2);font-size:1rem;display:flex;align-items:center;justify-content:center;flex-shrink:0;transition:all var(--transition)}
.modal-close:hover{border-color:var(--red);color:var(--red)}
.modal-nav{display:flex;gap:0.2rem;padding:0.85rem 1.5rem;border-bottom:1px solid var(--border);overflow-x:auto}
.modal-nav-btn{padding:0.35rem 0.85rem;border-radius:50px;font-size:0.78rem;font-weight:600;background:none;border:1px solid transparent;color:var(--text3);transition:all var(--transition);white-space:nowrap}
.modal-nav-btn:hover{color:var(--text);background:var(--card)}
.modal-nav-btn.active{background:var(--gold-dim);border-color:rgba(201,168,76,0.3);color:var(--gold)}
.modal-body{padding:1.75rem}
.modal-section{display:none}
.modal-section.active{display:block;animation:fadeIn 0.3s ease}
.content-block{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.35rem;margin-bottom:1.1rem}
.content-block h4{font-size:0.95rem;font-weight:700;color:var(--gold);margin-bottom:0.65rem}
.content-block p,.content-block ul{font-size:0.875rem;color:var(--text2);line-height:1.7}
.content-block ul{padding-left:1.1rem}
.content-block ul li{margin-bottom:0.45rem}
.concept-grid{display:grid;grid-template-columns:1fr 1fr;gap:0.85rem}
.concept-item{background:var(--card2);border:1px solid var(--border);border-radius:var(--radius-sm);padding:0.9rem}
.concept-term{font-weight:700;font-size:0.875rem;color:var(--teal);margin-bottom:0.35rem;font-family:var(--font-mono)}
.concept-def{font-size:0.8rem;color:var(--text2);line-height:1.55}

/* JUEGOS */
#juegos{background:var(--bg2)}
.juegos-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:1.25rem;margin-top:2.5rem}
.juego-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.6rem;cursor:pointer;transition:all var(--transition);text-align:center}
.juego-card:hover{transform:translateY(-4px);box-shadow:0 12px 40px rgba(0,0,0,0.3)}
.juego-icon{font-size:2.5rem;margin-bottom:1rem;display:block}
.juego-card h3{font-size:1rem;font-weight:700;margin-bottom:0.5rem}
.juego-card p{font-size:0.83rem;color:var(--text2);margin-bottom:1.1rem}
.juego-badge{display:inline-block;padding:0.25rem 0.75rem;border-radius:50px;font-size:0.72rem;font-weight:700;text-transform:uppercase;letter-spacing:0.06em}

/* QUIZ GAME (Quién soy) */
.quiz-game-container{max-width:600px;margin:2.5rem auto 0}
.qg-card{background:var(--card);border:1px solid var(--border);border-radius:20px;padding:2rem;text-align:center}
.qg-clue{font-size:0.875rem;color:var(--text2);margin-bottom:0.75rem;padding:0.75rem;background:var(--bg3);border-radius:var(--radius-sm);line-height:1.6}
.qg-clue-label{font-size:0.7rem;font-weight:700;color:var(--gold);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.35rem}
.qg-options{display:grid;grid-template-columns:1fr 1fr;gap:0.65rem;margin-top:1.25rem}
.qg-opt{padding:0.7rem;border-radius:var(--radius-sm);border:1px solid var(--border);background:var(--bg3);color:var(--text2);font-size:0.875rem;transition:all var(--transition)}
.qg-opt:hover{border-color:var(--gold);color:var(--gold)}
.qg-opt.correct{border-color:var(--teal);background:var(--teal-dim);color:var(--teal)}
.qg-opt.wrong{border-color:var(--red);background:var(--red-dim);color:var(--red)}
.qg-score{font-family:var(--font-display);font-size:2.5rem;font-weight:900;color:var(--gold);margin:0.5rem 0}

/* WORDLE FILOSÓFICO */
.wordle-container{max-width:460px;margin:2.5rem auto 0}
.wordle-grid{display:grid;grid-template-columns:repeat(6,1fr);gap:6px;margin-bottom:1.25rem;justify-content:center;max-width:320px;margin-left:auto;margin-right:auto}
.wordle-cell{width:48px;height:48px;border:2px solid var(--border);border-radius:6px;display:flex;align-items:center;justify-content:center;font-family:var(--font-mono);font-size:1.2rem;font-weight:800;text-transform:uppercase;transition:all var(--transition)}
.wordle-cell.filled{border-color:var(--gold);color:var(--gold)}
.wordle-cell.correct{background:var(--teal);border-color:var(--teal);color:#0d0f14}
.wordle-cell.present{background:#b59a2a;border-color:#b59a2a;color:#0d0f14}
.wordle-cell.absent{background:var(--bg3);border-color:var(--bg3);color:var(--text3)}
.wordle-keyboard{display:flex;flex-direction:column;gap:6px;align-items:center}
.wordle-row{display:flex;gap:5px}
.wk{padding:0.55rem 0.75rem;border-radius:5px;background:var(--card2);border:1px solid var(--border);color:var(--text);font-size:0.8rem;font-weight:700;min-width:32px;transition:all var(--transition)}
.wk:hover{background:var(--gold);color:#0d0f14}
.wk.correct{background:var(--teal);color:#0d0f14;border-color:var(--teal)}
.wk.present{background:#b59a2a;color:#0d0f14;border-color:#b59a2a}
.wk.absent{background:var(--bg3);color:var(--text3);border-color:var(--bg3)}

/* FLASHCARDS */
.flashcard-container{max-width:540px;margin:2.5rem auto 0;perspective:1000px}
.flashcard{width:100%;height:260px;position:relative;cursor:pointer;transform-style:preserve-3d;transition:transform 0.6s cubic-bezier(0.4,0,0.2,1)}
.flashcard.flipped{transform:rotateY(180deg)}
.flashcard-face{position:absolute;inset:0;background:var(--card);border:1px solid var(--border);border-radius:20px;display:flex;align-items:center;justify-content:center;flex-direction:column;padding:2.25rem;backface-visibility:hidden;text-align:center}
.flashcard-back{transform:rotateY(180deg)}
.flashcard-face.flashcard-front{border-color:rgba(201,168,76,0.3)}
.flashcard-face.flashcard-back{background:linear-gradient(135deg,var(--card),var(--card2));border-color:rgba(62,207,178,0.3)}
.flashcard-label{font-size:0.72rem;font-weight:700;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:0.85rem}
.flashcard-front .flashcard-label{color:var(--gold)}
.flashcard-back .flashcard-label{color:var(--teal)}
.flashcard-q{font-family:var(--font-display);font-size:1.1rem;font-weight:700;color:var(--text);line-height:1.4}
.flashcard-a{font-size:0.875rem;color:var(--text2);line-height:1.65}
.flashcard-controls{display:flex;gap:1rem;justify-content:center;margin-top:1.5rem;align-items:center}
.fc-btn{width:42px;height:42px;border-radius:50%;background:var(--card);border:1px solid var(--border);font-size:1rem;color:var(--text2);display:flex;align-items:center;justify-content:center;transition:all var(--transition)}
.fc-btn:hover{border-color:var(--gold);color:var(--gold)}
.fc-count{font-size:0.82rem;color:var(--text3);font-family:var(--font-mono)}

/* TESTS */
.quiz-container{max-width:700px;margin:2.5rem auto 0}
.quiz-question{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.6rem;margin-bottom:1.35rem}
.quiz-q-num{font-size:0.72rem;font-weight:700;color:var(--gold);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.65rem}
.quiz-q-text{font-size:0.975rem;font-weight:600;margin-bottom:1.1rem;line-height:1.5}
.quiz-options{display:flex;flex-direction:column;gap:0.55rem}
.quiz-option{padding:0.7rem 0.95rem;border-radius:var(--radius-sm);border:1px solid var(--border);background:var(--bg3);color:var(--text2);text-align:left;font-size:0.875rem;transition:all var(--transition)}
.quiz-option:hover{border-color:var(--gold);color:var(--text);background:var(--gold-dim)}
.quiz-option.correct{border-color:var(--teal);background:var(--teal-dim);color:var(--teal)}
.quiz-option.wrong{border-color:var(--red);background:var(--red-dim);color:var(--red)}
.quiz-explanation{margin-top:0.85rem;padding:0.8rem 0.95rem;border-radius:var(--radius-sm);background:var(--card2);border-left:3px solid var(--teal);font-size:0.83rem;color:var(--text2);display:none}
.quiz-explanation.show{display:block;animation:fadeIn 0.3s ease}
.quiz-score{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem;text-align:center;display:none}
.quiz-score.show{display:block;animation:fadeUp 0.5s ease}
.score-num{font-family:var(--font-display);font-size:3.5rem;font-weight:900;color:var(--gold)}

/* CRONOLOGÍA */
.timeline{position:relative;max-width:800px;margin:2.5rem auto 0;padding:1rem 0}
.timeline::before{content:'';position:absolute;left:50%;transform:translateX(-50%);top:0;bottom:0;width:2px;background:linear-gradient(var(--gold),var(--teal))}
.timeline-item{display:flex;gap:2rem;margin-bottom:2rem;position:relative}
.timeline-item:nth-child(even){flex-direction:row-reverse}
.timeline-dot{position:absolute;left:50%;transform:translate(-50%,-50%);top:50%;width:14px;height:14px;border-radius:50%;background:var(--gold);border:3px solid var(--bg2);box-shadow:0 0 0 4px var(--gold-dim);z-index:1;flex-shrink:0}
.timeline-content{flex:1;background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.1rem;transition:all var(--transition)}
.timeline-content:hover{border-color:rgba(201,168,76,0.3);transform:translateY(-2px)}
.timeline-date{font-family:var(--font-mono);font-size:0.78rem;color:var(--gold);margin-bottom:0.35rem}
.timeline-title{font-size:0.9rem;font-weight:700;margin-bottom:0.25rem}
.timeline-desc{font-size:0.8rem;color:var(--text2);line-height:1.55}
.timeline-spacer{flex:1}

/* COMPARATIVA */
.compare-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:1.25rem;margin-top:2.5rem}
.compare-col{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);overflow:hidden}
.compare-header{padding:1.1rem;background:var(--gold-dim);border-bottom:1px solid rgba(201,168,76,0.2);text-align:center}
.compare-author{font-size:0.95rem;font-weight:800;color:var(--gold);font-family:var(--font-display)}
.compare-dates{font-size:0.72rem;color:var(--text3);font-family:var(--font-mono)}
.compare-row{padding:0.8rem 1rem;border-bottom:1px solid var(--border);font-size:0.8rem;color:var(--text2);transition:background var(--transition)}
.compare-row:hover{background:var(--card2)}
.compare-row:last-child{border-bottom:none}
.compare-row strong{display:block;font-size:0.7rem;color:var(--text3);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:0.2rem}

/* SIMULACRO */
.exam-container{max-width:760px;margin:2.5rem auto 0}
.exam-header-box{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.35rem;margin-bottom:1.35rem;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:1rem}
.exam-timer{font-family:var(--font-mono);font-size:1.9rem;font-weight:700;color:var(--gold)}
.exam-timer.warning{color:var(--red);animation:pulse 1s ease infinite}
.exam-section-title{font-size:0.85rem;font-weight:700;color:var(--text3);text-transform:uppercase;letter-spacing:0.08em;margin:1.75rem 0 0.85rem}
.exam-textarea{width:100%;background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.1rem;color:var(--text);font-family:var(--font-body);font-size:0.875rem;resize:vertical;min-height:130px;transition:border-color var(--transition);outline:none}
.exam-textarea:focus{border-color:var(--gold)}
.word-count{font-size:0.72rem;color:var(--text3);text-align:right;margin-top:0.3rem;font-family:var(--font-mono)}

/* BANCO */
.banco-search{display:flex;gap:0.85rem;margin-top:2.5rem;margin-bottom:1.75rem;flex-wrap:wrap}
.search-input{flex:1;min-width:180px;padding:0.7rem 0.95rem;background:var(--card);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-family:var(--font-body);font-size:0.875rem;outline:none;transition:border-color var(--transition)}
.search-input:focus{border-color:var(--gold)}
.filter-select{padding:0.7rem 0.95rem;background:var(--card);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-family:var(--font-body);font-size:0.85rem;outline:none;cursor:pointer}
.banco-list{display:flex;flex-direction:column;gap:0.65rem}
.banco-item{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.1rem;cursor:pointer;transition:all var(--transition)}
.banco-item:hover{border-color:rgba(201,168,76,0.3);background:var(--card2)}
.banco-meta{display:flex;gap:0.4rem;align-items:center;margin-bottom:0.55rem;flex-wrap:wrap}
.banco-q{font-size:0.875rem;font-weight:500;color:var(--text);line-height:1.45}
.banco-answer{margin-top:0.85rem;padding:0.9rem;background:var(--card2);border-radius:var(--radius-sm);border-left:3px solid var(--gold);font-size:0.83rem;color:var(--text2);line-height:1.65;display:none}
.banco-answer.show{display:block;animation:fadeIn 0.3s ease}
.banco-answer-toggle{margin-top:0.65rem;font-size:0.78rem;color:var(--gold);font-weight:600;background:none;border:none;cursor:pointer;display:flex;align-items:center;gap:0.3rem}

/* EXÁMENES */
.exam-year-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem;transition:all var(--transition)}
.exam-year-card:hover{border-color:rgba(201,168,76,0.3);transform:translateY(-3px)}

/* PODCASTS */
#podcasts{background:var(--bg2)}
.podcasts-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1.25rem;margin-top:2.5rem}
.podcast-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem;transition:all var(--transition);display:flex;flex-direction:column}
.podcast-card:hover{border-color:rgba(167,139,250,0.4);transform:translateY(-3px);box-shadow:0 8px 32px rgba(0,0,0,0.3)}
.podcast-cover{width:72px;height:72px;border-radius:12px;margin-bottom:1rem;object-fit:cover;background:var(--purple-dim);display:flex;align-items:center;justify-content:center;font-size:2rem;flex-shrink:0}
.podcast-platform{font-size:0.7rem;font-weight:700;letter-spacing:0.08em;text-transform:uppercase;color:var(--purple);margin-bottom:0.35rem}
.podcast-name{font-size:1rem;font-weight:700;margin-bottom:0.35rem}
.podcast-desc{font-size:0.83rem;color:var(--text2);line-height:1.55;margin-bottom:1rem;flex:1}
.podcast-eps{font-size:0.78rem;color:var(--text3);margin-bottom:1rem;font-family:var(--font-mono)}
.podcast-tags{display:flex;gap:0.35rem;flex-wrap:wrap;margin-bottom:1rem}
.btn-podcast{display:inline-flex;align-items:center;gap:0.4rem;background:var(--purple-dim);border:1px solid rgba(167,139,250,0.3);color:var(--purple);padding:0.5rem 1rem;border-radius:var(--radius-sm);font-size:0.82rem;font-weight:600;transition:all var(--transition);text-decoration:none}
.btn-podcast:hover{background:var(--purple);color:#fff;transform:translateY(-1px)}

/* LIBROS */
#libros{background:var(--bg)}
.libros-tabs{display:flex;gap:0.5rem;flex-wrap:wrap;margin-top:2.5rem;margin-bottom:1.75rem}
.libros-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:1.25rem}
.libro-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);overflow:hidden;transition:all var(--transition)}
.libro-card:hover{transform:translateY(-4px);box-shadow:0 12px 40px rgba(0,0,0,0.35);border-color:rgba(201,168,76,0.3)}
.libro-spine{height:140px;display:flex;align-items:center;justify-content:center;font-size:3rem;position:relative;overflow:hidden}
.libro-body{padding:1.1rem}
.libro-titulo{font-size:0.9rem;font-weight:700;margin-bottom:0.25rem;line-height:1.3}
.libro-autor{font-size:0.78rem;color:var(--gold);margin-bottom:0.5rem;font-weight:600}
.libro-desc{font-size:0.78rem;color:var(--text2);line-height:1.5;margin-bottom:0.75rem}
.libro-nivel{display:inline-block;padding:0.2rem 0.6rem;border-radius:50px;font-size:0.68rem;font-weight:700;text-transform:uppercase;letter-spacing:0.06em}
.nivel-basico{background:var(--teal-dim);color:var(--teal)}
.nivel-medio{background:var(--gold-dim);color:var(--gold)}
.nivel-avanzado{background:var(--red-dim);color:var(--red)}

/* PROGRESO */
.progreso-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-top:2.5rem}
.progreso-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.5rem}
.progreso-card h3{font-size:0.9rem;font-weight:700;margin-bottom:1.1rem;display:flex;justify-content:space-between}
.progreso-card h3 span{font-size:0.78rem;font-weight:400;color:var(--text3)}
.radial-wrap{display:flex;justify-content:center;margin-bottom:1.35rem}
.radial-chart{position:relative;width:130px;height:130px}
.radial-chart svg{transform:rotate(-90deg)}
.radial-bg{fill:none;stroke:var(--bg3);stroke-width:10}
.radial-fill{fill:none;stroke:var(--gold);stroke-width:10;stroke-linecap:round;transition:stroke-dashoffset 1.5s ease}
.radial-label{position:absolute;inset:0;display:flex;flex-direction:column;align-items:center;justify-content:center}
.radial-pct{font-family:var(--font-display);font-size:1.65rem;font-weight:800;color:var(--gold)}
.radial-sub{font-size:0.7rem;color:var(--text3)}
.autor-progress-list{display:flex;flex-direction:column;gap:0.65rem}
.apl-item label{display:flex;justify-content:space-between;font-size:0.8rem;color:var(--text2);margin-bottom:0.3rem}
.apl-item label span{color:var(--text3);font-family:var(--font-mono)}
.apl-bar{height:5px;background:var(--bg3);border-radius:3px;overflow:hidden}
.apl-fill{height:100%;border-radius:3px;background:linear-gradient(90deg,var(--gold),var(--teal));transition:width 1.2s ease}
.streak-day{width:34px;height:34px;border-radius:7px;background:var(--bg3);display:flex;align-items:center;justify-content:center;font-size:0.68rem;font-weight:700;color:var(--text3);border:1px solid var(--border);transition:all var(--transition)}
.streak-day.done{background:var(--gold-dim);border-color:var(--gold);color:var(--gold)}
.streak-day.today{background:var(--gold);color:#0d0f14}

/* PREMIUM */
#premium{background:linear-gradient(135deg,var(--bg) 0%,rgba(201,168,76,0.04) 50%,var(--bg) 100%);position:relative;overflow:hidden}
.premium-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.25rem;margin-top:2.5rem}
.premium-card{background:var(--card);border:1px solid var(--border);border-radius:20px;padding:1.75rem;transition:all var(--transition);position:relative;overflow:hidden}
.premium-card.featured{background:linear-gradient(135deg,#1e1a0f,#2a2210);border-color:rgba(201,168,76,0.5)}
.premium-card.featured::after{content:'MÁS POPULAR';position:absolute;top:16px;right:-26px;background:var(--gold);color:#0d0f14;font-size:0.62rem;font-weight:800;padding:0.22rem 2rem;transform:rotate(45deg);letter-spacing:0.05em}
.premium-card:hover{transform:translateY(-4px);box-shadow:0 16px 48px rgba(0,0,0,0.3)}
.plan-name{font-size:0.78rem;font-weight:700;color:var(--text3);letter-spacing:0.1em;text-transform:uppercase;margin-bottom:0.65rem}
.plan-price{font-family:var(--font-display);font-size:2.8rem;font-weight:900;color:var(--text);margin-bottom:0.2rem;line-height:1}
.plan-price sup{font-size:1.1rem;vertical-align:top;margin-top:0.35rem;color:var(--gold)}
.plan-price span{font-size:0.85rem;font-weight:400;color:var(--text3)}
.plan-desc{font-size:0.83rem;color:var(--text2);margin-bottom:1.25rem}
.plan-features{list-style:none;margin-bottom:1.5rem;display:flex;flex-direction:column;gap:0.55rem}
.plan-features li{font-size:0.83rem;color:var(--text2);display:flex;align-items:flex-start;gap:0.55rem}
.plan-features li::before{content:'✓';color:var(--gold);font-weight:700;flex-shrink:0;margin-top:0.05rem}
.plan-features li.no::before{content:'✗';color:var(--text3)}
.plan-features li.no{color:var(--text3)}
.btn-plan{width:100%;padding:0.8rem;border-radius:var(--radius-sm);font-weight:700;font-size:0.875rem;transition:all var(--transition);display:block;text-align:center}
.btn-plan-free{background:var(--card2);border:1px solid var(--border);color:var(--text)}
.btn-plan-free:hover{border-color:var(--gold);color:var(--gold)}
.btn-plan-premium{background:linear-gradient(135deg,var(--gold),#a8732e);color:#0d0f14}
.btn-plan-premium:hover{transform:translateY(-1px);box-shadow:0 6px 20px rgba(201,168,76,0.4)}

/* CONSEJOS */
.consejos-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:1.1rem;margin-top:2.5rem}
.consejo-card{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.35rem;transition:all var(--transition)}
.consejo-card:hover{border-color:rgba(201,168,76,0.3);transform:translateY(-2px)}
.consejo-num{width:38px;height:38px;border-radius:9px;background:var(--gold-dim);display:flex;align-items:center;justify-content:center;font-family:var(--font-display);font-size:1rem;font-weight:800;color:var(--gold);margin-bottom:0.85rem}
.consejo-card h4{font-size:0.9rem;font-weight:700;margin-bottom:0.45rem}
.consejo-card p{font-size:0.82rem;color:var(--text2);line-height:1.6}

/* COMMUNITY WIDGET */
.community-widget{background:linear-gradient(135deg,var(--bg2),var(--bg3));border:1px solid var(--border);border-radius:20px;padding:2.5rem;margin-top:3rem;text-align:center;position:relative;overflow:hidden}
.community-widget::before{content:'';position:absolute;top:-100px;left:50%;transform:translateX(-50%);width:400px;height:400px;border-radius:50%;background:radial-gradient(circle,rgba(201,168,76,0.06) 0%,transparent 70%);pointer-events:none}
.community-widget h3{font-size:1.6rem;font-weight:800;margin-bottom:0.75rem}
.community-widget p{font-size:0.95rem;color:var(--text2);max-width:500px;margin:0 auto 2rem;line-height:1.65}
.community-btns{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;margin-bottom:1.75rem}
.community-steps{display:flex;gap:1.5rem;justify-content:center;flex-wrap:wrap;margin-top:1.5rem}
.community-step{display:flex;flex-direction:column;align-items:center;gap:0.5rem;max-width:140px}
.community-step-icon{width:48px;height:48px;border-radius:50%;background:var(--gold-dim);border:1px solid rgba(201,168,76,0.3);display:flex;align-items:center;justify-content:center;font-size:1.25rem}
.community-step p{font-size:0.78rem;color:var(--text2);text-align:center;line-height:1.4}

/* FOOTER */
footer{background:var(--bg3);border-top:1px solid var(--border);padding:3rem 2rem;text-align:center}
.footer-brand{font-family:var(--font-display);font-size:1.4rem;font-weight:700;color:var(--gold);margin-bottom:0.4rem}
.footer-sub{font-size:0.82rem;color:var(--text3)}
.footer-links{margin-top:1.35rem;display:flex;gap:1.25rem;justify-content:center;flex-wrap:wrap;align-items:center}
.footer-links a{font-size:0.82rem;color:var(--text3);transition:color var(--transition)}
.footer-links a:hover{color:var(--gold)}

/* FLOATING SOCIAL BUTTONS */
.float-social{
  position:fixed;right:1.25rem;bottom:1.25rem;z-index:800;
  display:flex;flex-direction:column;gap:0.6rem;align-items:flex-end;
}
.float-btn{
  display:flex;align-items:center;gap:0.6rem;
  padding:0.6rem 1rem;border-radius:50px;
  font-size:0.82rem;font-weight:700;color:#fff;
  box-shadow:0 4px 20px rgba(0,0,0,0.35);
  transition:all 0.25s;cursor:pointer;text-decoration:none;
  white-space:nowrap;
}
.float-btn:hover{transform:translateX(-4px) scale(1.04);color:#fff}
.float-btn-label{transition:all 0.3s;overflow:hidden;max-width:0;opacity:0}
.float-btn:hover .float-btn-label{max-width:160px;opacity:1}
.float-tiktok{background:linear-gradient(135deg,#010101,#2a2a2a);border:1px solid rgba(255,255,255,0.15)}
.float-instagram{background:linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045)}
.float-icon{width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:1rem;flex-shrink:0}

/* POPUP REMINDER */
.social-popup{
  position:fixed;bottom:5.5rem;right:1.25rem;z-index:801;
  background:var(--card);border:1px solid rgba(201,168,76,0.4);
  border-radius:16px;padding:1.25rem;width:260px;
  box-shadow:0 8px 32px rgba(0,0,0,0.4);
  animation:popIn 0.4s cubic-bezier(0.34,1.56,0.64,1) both;
  display:none;
}
.social-popup.show{display:block}
/* SEARCH */
.search-tag{background:var(--card);border:1px solid var(--border);color:var(--text2);padding:0.3rem 0.75rem;border-radius:50px;font-size:0.75rem;cursor:pointer;transition:all 0.2s;font-family:var(--font-body)}
.search-tag:hover{border-color:var(--gold);color:var(--gold);background:var(--gold-dim)}
.search-result{background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1rem 1.25rem;margin-bottom:0.6rem;cursor:pointer;transition:all 0.2s;display:flex;align-items:flex-start;gap:1rem}
.search-result:hover{border-color:rgba(201,168,76,0.4);transform:translateX(4px);box-shadow:0 4px 20px rgba(0,0,0,0.2)}
.search-result-icon{font-size:1.5rem;flex-shrink:0;margin-top:2px}
.search-result-body{flex:1;min-width:0}
.search-result-title{font-weight:700;font-size:0.95rem;margin-bottom:0.2rem}
.search-result-subtitle{font-size:0.78rem;color:var(--text2);margin-bottom:0.3rem}
.search-result-excerpt{font-size:0.8rem;color:var(--text3);line-height:1.5;overflow:hidden;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical}
.search-result-type{display:inline-block;padding:0.15rem 0.5rem;border-radius:50px;font-size:0.68rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;margin-left:auto;flex-shrink:0;align-self:flex-start}
mark{background:rgba(201,168,76,0.3);color:var(--gold);border-radius:2px;padding:0 1px}
@keyframes popIn{from{opacity:0;transform:scale(0.8) translateY(20px)}to{opacity:1;transform:scale(1) translateY(0)}}
.popup-close{position:absolute;top:8px;right:10px;background:none;border:none;color:var(--text3);font-size:1rem;cursor:pointer;line-height:1}
.popup-close:hover{color:var(--text)}
.popup-title{font-size:0.9rem;font-weight:700;margin-bottom:0.4rem;padding-right:1rem}
.popup-sub{font-size:0.78rem;color:var(--text2);margin-bottom:1rem;line-height:1.5}
.popup-btns{display:flex;flex-direction:column;gap:0.5rem}
.popup-btn{display:flex;align-items:center;gap:0.5rem;padding:0.55rem 0.85rem;border-radius:var(--radius-sm);font-size:0.82rem;font-weight:700;color:#fff;text-decoration:none;transition:all 0.2s}
.popup-btn:hover{transform:translateX(3px);color:#fff}
.popup-btn-tt{background:linear-gradient(135deg,#010101,#2a2a2a)}
.popup-btn-ig{background:linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045)}
@keyframes fadeUp{from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:translateY(0)}}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes pulse{0%,100%{opacity:1}50%{opacity:0.5}}
@keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-8px)}}
.reveal{opacity:0;transform:translateY(20px);transition:opacity 0.6s ease,transform 0.6s ease}
.reveal.visible{opacity:1;transform:translateY(0)}

/* MOBILE */
@media(max-width:768px){
  .nav-links{position:fixed;top:60px;left:0;right:0;background:var(--bg2);border-bottom:1px solid var(--border);flex-direction:column;gap:0;padding:0.75rem;display:none;z-index:850}
  .nav-links.open{display:flex}
  .nav-links a{width:100%;text-align:left;padding:0.7rem 1rem;border-radius:var(--radius-sm)}
  .hamburger{display:flex}
  .pau-grid,.compare-grid,.premium-grid,.progreso-grid,.concept-grid{grid-template-columns:1fr}
  .timeline::before{left:20px}
  .timeline-item,.timeline-item:nth-child(even){flex-direction:column;padding-left:46px}
  .timeline-dot{left:20px;top:1.5rem}
  .timeline-spacer{display:none}
  .modal{border-radius:12px}
  .modal-body{padding:1.1rem}
  .qg-options{grid-template-columns:1fr}
  .social-banner-inner{flex-direction:column;text-align:center}
}
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-brand">📚 <span>Filosof</span>EANDO</div>
  <div class="nav-links" id="navLinks">
    <a href="#buscador">🔍 Buscador</a>
    <a href="#pau-info">La PAU</a>
    <a href="#autores">Autores</a>
    <a href="#juegos">Juegos</a>
    <a href="#flashcards">Flashcards</a>
    <a href="#tests">Tests</a>
    <a href="#simulacro">Simulacro</a>
    <a href="#examenes">Exámenes</a>
    <a href="#podcasts">Podcasts</a>
    <a href="#libros">Libros</a>
    <a href="#progreso">Progreso</a>
    <a href="#sugerencias">💬 Sugerencias</a>
    <a href="#premium" class="nav-premium" style="border-radius:var(--radius-sm);padding:0.35rem 0.85rem">✦ Premium</a>
  </div>
  <div style="display:flex;gap:0.6rem;align-items:center">
    <button class="theme-toggle" id="themeToggle" title="Cambiar tema">🌙</button>
    <button class="hamburger" id="hamburger"><span></span><span></span><span></span></button>
  </div>
</nav>

<!-- HERO -->
<section class="hero" id="inicio">
  <div class="hero-grid"></div>
  <div class="hero-content">
    <div class="hero-badge" id="heroBadge">✦ Actualizado · PAU Andalucía</div>
    <h1>Aprueba la <em>Selectividad</em><br>de Filosofía</h1>
    <p class="hero-sub">La plataforma <strong>100% gratuita</strong> más completa para preparar la PAU de Filosofía en Andalucía. Temario, tests, juegos, podcasts y más.</p>
    <div class="hero-ctas">
      <a href="#autores" class="btn-primary">Empezar a estudiar →</a>
      <a href="#pau-info" class="btn-secondary">Conocer la PAU</a>
    </div>
    <div class="hero-stats">
      <div class="stat"><div class="stat-num">12+</div><div class="stat-label">Autores PAU</div></div>
      <div class="stat"><div class="stat-num">500+</div><div class="stat-label">Preguntas</div></div>
      <div class="stat"><div class="stat-num">100%</div><div class="stat-label">Gratuito</div></div>
      <div class="stat"><div class="stat-num">11</div><div class="stat-label">Años de exámenes</div></div>
    </div>
  </div>
</section>

<!-- SOCIAL BANNER -->
<div class="social-banner">
  <div class="social-banner-inner">
    <div class="social-banner-text">
      <h3>🎓 Esta plataforma es <em>completamente gratis</em></h3>
      <p>Si te ayuda a aprobar, sígueme en TikTok e Instagram y apoya el proyecto. ¡Juntos crecemos!</p>
    </div>
    <div class="social-btns">
      <a href="https://www.tiktok.com/@filosofeando_para_aproba" target="_blank" rel="noopener" class="btn-tiktok">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M19.59 6.69a4.83 4.83 0 01-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 01-2.88 2.5 2.89 2.89 0 01-2.89-2.89 2.89 2.89 0 012.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 00-.79-.05 6.34 6.34 0 00-6.34 6.34 6.34 6.34 0 006.34 6.34 6.34 6.34 0 006.33-6.34V8.69a8.17 8.17 0 004.77 1.52V6.75a4.85 4.85 0 01-1-.06z"/></svg>
        Seguir en TikTok
      </a>
      <a href="https://www.instagram.com/filosofeando_para_aprobar/" target="_blank" rel="noopener" class="btn-instagram">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
        Seguir en Instagram
      </a>
      <a href="https://paypal.me/alvato" target="_blank" rel="noopener" class="btn-paypal">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M7.076 21.337H2.47a.641.641 0 0 1-.633-.74L4.944.901C5.026.382 5.474 0 5.998 0h7.46c2.57 0 4.578.543 5.69 1.81 1.01 1.15 1.304 2.42 1.012 4.287-.023.143-.047.288-.077.437-.983 5.05-4.349 6.797-8.647 6.797h-2.19c-.524 0-.968.382-1.05.9l-1.12 7.106zm14.146-14.42a3.35 3.35 0 0 0-.607-.541c-.013.076-.026.175-.041.254-.93 4.778-4.005 7.201-9.138 7.201h-2.19a.563.563 0 0 0-.556.479l-1.187 7.527h-.506l-.24 1.516a.56.56 0 0 0 .554.647h3.882c.46 0 .85-.334.922-.788.06-.26.76-4.852.816-5.09a.932.932 0 0 1 .923-.788h.58c3.76 0 6.705-1.528 7.565-5.946.36-1.847.174-3.388-.777-4.471z"/></svg>
        Apoyar con PayPal
      </a>
    </div>
  </div>
</div>

<!-- PAU INFO -->
<section id="pau-info" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">La selectividad</div>
    <h2 class="section-title">¿Cómo es la PAU de Filosofía en Andalucía?</h2>
    <p class="section-sub">Estructura, criterios y claves para organizarte bien desde el primer día.</p>
    <div class="pau-grid reveal">
      <div class="pau-card">
        <div class="pau-card-icon">📋</div>
        <h3>Estructura del Examen</h3>
        <table class="structure-table">
          <tr><th>Pregunta</th><th>Contenido</th><th>Puntos</th></tr>
          <tr><td>1a</td><td>Definición de 2 términos</td><td>2 pts</td></tr>
          <tr><td>1b</td><td>Idea principal y estructura</td><td>2 pts</td></tr>
          <tr><td>1c</td><td>Posición filosófica del autor</td><td>2 pts</td></tr>
          <tr><td>2a</td><td>Relación con otro autor</td><td>2 pts</td></tr>
          <tr><td>2b</td><td>Valoración personal</td><td>2 pts</td></tr>
        </table>
      </div>
      <div class="pau-card">
        <div class="pau-card-icon">📚</div>
        <h3>Autores del Currículo Andaluz</h3>
        <div style="display:flex;flex-wrap:wrap;gap:0.4rem;margin-top:0.5rem">
          <span class="tag tag-gold">Platón</span><span class="tag tag-gold">Aristóteles</span>
          <span class="tag tag-teal">Descartes</span><span class="tag tag-teal">Hume</span><span class="tag tag-teal">Kant</span>
          <span class="tag tag-blue">Marx</span><span class="tag tag-blue">Nietzsche</span><span class="tag tag-blue">Ortega y Gasset</span>
          <span class="tag tag-red">Habermas</span><span class="tag tag-red">Rawls</span><span class="tag tag-red">Nussbaum</span><span class="tag tag-red">Wittgenstein</span>
        </div>
      </div>
      <div class="pau-card">
        <div class="pau-card-icon">🎯</div>
        <h3>Criterios de Corrección</h3>
        <ul>
          <li>Rigor conceptual y vocabulario filosófico preciso</li>
          <li>Comprensión e interpretación correcta del texto</li>
          <li>Relación coherente con el pensamiento del autor</li>
          <li>Establecimiento de relaciones históricas y filosóficas</li>
          <li>Argumentación propia clara y bien fundamentada</li>
          <li>Corrección ortográfica y expresión escrita cuidada</li>
        </ul>
      </div>
      <div class="pau-card">
        <div class="pau-card-icon">💡</div>
        <h3>Claves del Éxito</h3>
        <ul>
          <li><strong>Domina el vocabulario</strong> de cada autor</li>
          <li><strong>Contextualiza</strong> cada texto en su época</li>
          <li><strong>Practica comentarios</strong> completos cronometrados</li>
          <li><strong>Aprende relaciones</strong> entre autores</li>
          <li><strong>Prepara la valoración</strong> personal con argumentos</li>
          <li><strong>Revisa exámenes</strong> anteriores de Andalucía</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- AUTORES -->
<section id="buscador" style="background:linear-gradient(180deg,var(--bg2) 0%,var(--bg) 100%);padding:2.5rem 0">
  <div class="container" style="max-width:760px">
    <div style="text-align:center;margin-bottom:1.5rem">
      <div class="section-label">Búsqueda inteligente</div>
      <h2 style="font-family:var(--font-display);font-size:1.8rem;margin-bottom:0.5rem">🔍 Buscador de Filosofía</h2>
      <p style="color:var(--text2);font-size:0.9rem">Busca autores, conceptos, obras, corrientes o cualquier término del currículo PAU</p>
    </div>
    <div style="position:relative">
      <input type="text" id="buscadorInput" placeholder="Ej: imperativo categórico, Platón, empirismo, alma, República…" autocomplete="off"
        style="width:100%;padding:1rem 1rem 1rem 3.2rem;background:var(--card);border:2px solid var(--border);border-radius:50px;color:var(--text);font-family:var(--font-body);font-size:1rem;outline:none;transition:all 0.25s;box-shadow:0 4px 24px rgba(0,0,0,0.2)"
        onfocus="this.style.borderColor='var(--gold)';this.style.boxShadow='0 4px 32px rgba(201,168,76,0.2)'"
        onblur="this.style.borderColor='var(--border)';this.style.boxShadow='0 4px 24px rgba(0,0,0,0.2)'"
        oninput="buscarFilo(this.value)">
      <svg style="position:absolute;left:1.1rem;top:50%;transform:translateY(-50%);opacity:0.5;pointer-events:none" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.35-4.35"/></svg>
      <button id="buscadorClear" onclick="limpiarBusqueda()" style="display:none;position:absolute;right:1rem;top:50%;transform:translateY(-50%);background:var(--card2);border:none;color:var(--text3);width:26px;height:26px;border-radius:50%;font-size:0.9rem;cursor:pointer;line-height:1">✕</button>
    </div>
    <!-- SUGERENCIAS RÁPIDAS -->
    <div style="margin-top:0.75rem;display:flex;flex-wrap:wrap;gap:0.4rem;justify-content:center" id="sugerenciasRapidas">
      <span style="font-size:0.75rem;color:var(--text3);align-self:center">Búsquedas frecuentes:</span>
      <button onclick="buscarYFocar('imperativo categórico')" class="search-tag">imperativo categórico</button>
      <button onclick="buscarYFocar('mito de la caverna')" class="search-tag">mito de la caverna</button>
      <button onclick="buscarYFocar('alienación')" class="search-tag">alienación</button>
      <button onclick="buscarYFocar('cogito')" class="search-tag">cogito ergo sum</button>
      <button onclick="buscarYFocar('voluntad de poder')" class="search-tag">voluntad de poder</button>
      <button onclick="buscarYFocar('eudaimonia')" class="search-tag">eudaimonía</button>
    </div>
    <!-- RESULTADOS -->
    <div id="buscadorResultados" style="margin-top:1.25rem"></div>
  </div>
</section>

<section id="autores" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Temario completo</div>
    <h2 class="section-title">Autores del Currículo Andaluz</h2>
    <p class="section-sub">Haz clic en cualquier autor para ver su temario completo con 9 secciones, conceptos, preguntas PAU y comentario resuelto.</p>
    <div class="autores-tabs">
      <button class="tab-btn active" data-filter="all">Todos</button>
      <button class="tab-btn" data-filter="antigua">Antigua</button>
      <button class="tab-btn" data-filter="moderna">Moderna</button>
      <button class="tab-btn" data-filter="contemporanea">Contemporánea</button>
    </div>
    <div class="autores-grid" id="autoresGrid"></div>
  </div>
</section>

<!-- MODAL AUTOR -->
<div class="modal-overlay" id="modalOverlay">
  <div class="modal" id="autorModal">
    <div class="modal-header">
      <div>
        <div class="autor-era" id="modalEra"></div>
        <h2 style="font-size:1.6rem;font-weight:900" id="modalName"></h2>
        <div style="font-family:var(--font-mono);font-size:0.82rem;color:var(--text3);margin-top:0.25rem" id="modalDates"></div>
      </div>
      <button class="modal-close" id="modalClose">✕</button>
    </div>
    <div class="modal-nav">
      <button class="modal-nav-btn active" data-section="contexto">Contexto</button>
      <button class="modal-nav-btn" data-section="conocimiento">Conocimiento</button>
      <button class="modal-nav-btn" data-section="realidad">Realidad</button>
      <button class="modal-nav-btn" data-section="ser-humano">Ser humano</button>
      <button class="modal-nav-btn" data-section="etica">Ética y Política</button>
      <button class="modal-nav-btn" data-section="conceptos">Conceptos</button>
      <button class="modal-nav-btn" data-section="resumen">Resumen</button>
      <button class="modal-nav-btn" data-section="pau">Preguntas PAU</button>
      <button class="modal-nav-btn" data-section="comentario">Comentario</button>
    </div>
    <div class="modal-body" id="modalBody"></div>
  </div>
</div>

<!-- JUEGOS -->
<section id="juegos">
  <div class="container">
    <div class="section-label">Aprende jugando</div>
    <h2 class="section-title">Juegos Filosóficos</h2>
    <p class="section-sub">Repasa los conceptos de forma divertida. Cuanto más juegas, más recuerdas en el examen.</p>
    <div class="juegos-grid">
      <div class="juego-card" onclick="showGame('quiensoy')" style="border-color:rgba(201,168,76,0.3)">
        <span class="juego-icon">🤔</span>
        <h3>¿Quién soy?</h3>
        <p>Lee las pistas y adivina el filósofo. Cuantas menos pistas necesites, más puntos.</p>
        <span class="juego-badge" style="background:var(--gold-dim);color:var(--gold)">⭐ Favorito</span>
      </div>
      <div class="juego-card" onclick="showGame('wordle')" style="border-color:rgba(62,207,178,0.3)">
        <span class="juego-icon">🔤</span>
        <h3>FiloWordle</h3>
        <p>Adivina el concepto filosófico de 6 letras. Una nueva palabra filosófica cada día.</p>
        <span class="juego-badge" style="background:var(--teal-dim);color:var(--teal)">🧩 Wordle</span>
      </div>
      <div class="juego-card" onclick="showGame('parejas')" style="border-color:rgba(91,141,238,0.3)">
        <span class="juego-icon">🃏</span>
        <h3>Parejas Filosóficas</h3>
        <p>Une cada concepto con su autor. Cronometra tu récord y bate tu marca.</p>
        <span class="juego-badge" style="background:var(--blue-dim);color:var(--blue)">⚡ Velocidad</span>
      </div>
      <div class="juego-card" onclick="showGame('ordenar')" style="border-color:rgba(167,139,250,0.3)">
        <span class="juego-icon">📅</span>
        <h3>Ordena la Historia</h3>
        <p>Coloca a los filósofos en orden cronológico. Perfecto para estudiar la cronología.</p>
        <span class="juego-badge" style="background:var(--purple-dim);color:var(--purple)">🏆 Reto</span>
      </div>
      <div class="juego-card" onclick="showGame('ahorcado')" style="border-color:rgba(224,92,92,0.3)">
        <span class="juego-icon">🪢</span>
        <h3>FiloAhorcado</h3>
        <p>Adivina el concepto o el autor letra a letra. Clásico pero adictivo.</p>
        <span class="juego-badge" style="background:var(--red-dim);color:var(--red)">💀 Clásico</span>
      </div>
      <div class="juego-card" onclick="showGame('verdadmentira')" style="border-color:rgba(62,207,178,0.3)">
        <span class="juego-icon">✅</span>
        <h3>Verdad o Mentira</h3>
        <p>¿Es cierto este enunciado filosófico? Responde rápido antes de que se acabe el tiempo.</p>
        <span class="juego-badge" style="background:var(--teal-dim);color:var(--teal)">⏱️ Rapidez</span>
      </div>
      <div class="juego-card" onclick="showGame('definicion')" style="border-color:rgba(201,168,76,0.3)">
        <span class="juego-icon">📖</span>
        <h3>¿Qué significa?</h3>
        <p>Te damos una definición y tú eliges el concepto correcto entre 4 opciones.</p>
        <span class="juego-badge" style="background:var(--gold-dim);color:var(--gold)">📚 Vocabulario</span>
      </div>
      <div class="juego-card" onclick="showGame('ruleta')" style="border-color:rgba(167,139,250,0.3)">
        <span class="juego-icon">🎰</span>
        <h3>Ruleta Filosófica</h3>
        <p>La ruleta elige un autor al azar y tienes 60 segundos para responder 5 preguntas sobre él.</p>
        <span class="juego-badge" style="background:var(--purple-dim);color:var(--purple)">🎲 Azar</span>
      </div>
    </div>

    <!-- ZONA DE JUEGO -->
    <div id="gameZone" style="display:none;margin-top:2.5rem"></div>
  </div>
</section>

<!-- FLASHCARDS -->
<section id="flashcards" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Repaso rápido</div>
    <h2 class="section-title">Flashcards de Filosofía</h2>
    <p class="section-sub">Haz clic en la tarjeta para ver la respuesta. 20 conceptos clave de la PAU.</p>
    <div class="flashcard-container">
      <div class="flashcard" id="flashcard">
        <div class="flashcard-face flashcard-front">
          <div class="flashcard-label">Pregunta</div>
          <div class="flashcard-q" id="fc-question"></div>
        </div>
        <div class="flashcard-face flashcard-back">
          <div class="flashcard-label">Respuesta</div>
          <div class="flashcard-a" id="fc-answer"></div>
        </div>
      </div>
      <div class="flashcard-controls">
        <button class="fc-btn" id="fcPrev">←</button>
        <span class="fc-count" id="fcCount">1 / 20</span>
        <button class="fc-btn" id="fcNext">→</button>
      </div>
    </div>
  </div>
</section>

<!-- TESTS -->
<section id="tests" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Test autocorregible</div>
    <h2 class="section-title">Pon a prueba tus conocimientos</h2>
    <p class="section-sub">Responde y obtén corrección inmediata con explicación para cada pregunta.</p>
    <div class="quiz-container" id="quizContainer"></div>
  </div>
</section>

<!-- CRONOLOGÍA -->
<section id="cronologia" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Historia de la Filosofía</div>
    <h2 class="section-title">Cronología Interactiva</h2>
    <p class="section-sub">Sitúa a cada autor en su contexto histórico y comprende la evolución del pensamiento filosófico occidental.</p>
    <div class="timeline" id="timeline"></div>
  </div>
</section>

<!-- COMPARATIVA -->
<section id="comparativa" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Relaciones entre autores</div>
    <h2 class="section-title">Comparativa de Autores</h2>
    <p class="section-sub">Esquemas comparativos para preparar la pregunta 2a del examen.</p>
    <div class="compare-grid reveal">
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Platón</div><div class="compare-dates">427–347 a.C.</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>Dos mundos: inteligible (verdadero) y sensible (aparente)</div>
          <div class="compare-row"><strong>Conocimiento</strong>Solo las Ideas son objeto de conocimiento verdadero</div>
          <div class="compare-row"><strong>Ser Humano</strong>Alma inmortal prisionera del cuerpo; razón debe dominar</div>
          <div class="compare-row"><strong>Ética</strong>Virtud como armonía del alma; Bien supremo como fin</div>
          <div class="compare-row"><strong>Política</strong>Estado ideal gobernado por filósofos-reyes</div>
        </div>
      </div>
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Aristóteles</div><div class="compare-dates">384–322 a.C.</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>La sustancia individual es lo real; forma en la materia</div>
          <div class="compare-row"><strong>Conocimiento</strong>Parte de la experiencia sensible; abstracción de universales</div>
          <div class="compare-row"><strong>Ser Humano</strong>Animal racional; alma como forma del cuerpo (unidad)</div>
          <div class="compare-row"><strong>Ética</strong>Eudaimonia como fin; virtud como término medio</div>
          <div class="compare-row"><strong>Política</strong>Animal político; polis como comunidad natural</div>
        </div>
      </div>
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Kant</div><div class="compare-dates">1724–1804</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>Fenómeno (cognoscible) vs noúmeno (cosa en sí)</div>
          <div class="compare-row"><strong>Conocimiento</strong>Síntesis sensibilidad-entendimiento; formas a priori</div>
          <div class="compare-row"><strong>Ser Humano</strong>Ser racional y autónomo; fin en sí mismo</div>
          <div class="compare-row"><strong>Ética</strong>Imperativo categórico; deber moral universal</div>
          <div class="compare-row"><strong>Política</strong>Paz perpetua; federación de estados republicanos</div>
        </div>
      </div>
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Descartes</div><div class="compare-dates">1596–1650</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>Dualismo: res cogitans (mente) y res extensa (materia)</div>
          <div class="compare-row"><strong>Conocimiento</strong>Razón + ideas innatas; duda metódica como método</div>
          <div class="compare-row"><strong>Ser Humano</strong>Unión de mente y cuerpo; cogito como primera certeza</div>
          <div class="compare-row"><strong>Ética</strong>Moral provisional; dominio de las pasiones por la razón</div>
          <div class="compare-row"><strong>Dios</strong>Garantía del conocimiento verdadero; prueba ontológica</div>
        </div>
      </div>
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Hume</div><div class="compare-dates">1711–1776</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>Solo podemos conocer impresiones e ideas derivadas de ellas</div>
          <div class="compare-row"><strong>Conocimiento</strong>Empirismo radical; la causalidad es hábito, no necesidad</div>
          <div class="compare-row"><strong>Ser Humano</strong>El yo es un haz de percepciones sin sustancia permanente</div>
          <div class="compare-row"><strong>Ética</strong>La moral se basa en el sentimiento (simpatía), no en la razón</div>
          <div class="compare-row"><strong>Religión</strong>Escepticismo: critica los milagros y el argumento del diseño</div>
        </div>
      </div>
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Marx</div><div class="compare-dates">1818–1883</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>Materialismo histórico: la base económica determina la superestructura</div>
          <div class="compare-row"><strong>Conocimiento</strong>La praxis (acción transformadora) es el criterio de verdad</div>
          <div class="compare-row"><strong>Ser Humano</strong>Ser genérico alienado por el capitalismo; se realiza en el trabajo libre</div>
          <div class="compare-row"><strong>Ética</strong>No hay moral universal; la moral es ideología de clase dominante</div>
          <div class="compare-row"><strong>Política</strong>Lucha de clases → revolución proletaria → sociedad sin clases</div>
        </div>
      </div>
      <div class="compare-col">
        <div class="compare-header"><div class="compare-author">Nietzsche</div><div class="compare-dates">1844–1900</div></div>
        <div>
          <div class="compare-row"><strong>Realidad</strong>El mundo es pura voluntad de poder; no hay verdades eternas</div>
          <div class="compare-row"><strong>Conocimiento</strong>Perspectivismo: no existe la verdad objetiva, solo interpretaciones</div>
          <div class="compare-row"><strong>Ser Humano</strong>Animal que debe superarse: del último hombre al superhombre</div>
          <div class="compare-row"><strong>Ética</strong>Transvaloración: superar la moral del rebaño por la moral del señor</div>
          <div class="compare-row"><strong>Historia</strong>Eterno retorno; amor fati; nihilismo como punto de partida</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GUÍA RESPONDER PAU -->
<section id="guia-pau" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Guía práctica</div>
    <h2 class="section-title">📋 Cómo Responder Cada Pregunta</h2>
    <p class="section-sub">Estructura exacta, tiempo recomendado y errores que te cuestan puntos. Aprende el método antes de practicar.</p>

    <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1.25rem;margin-top:2rem">

      <!-- 1a -->
      <div style="background:var(--card);border:1px solid rgba(201,168,76,0.3);border-radius:var(--radius);padding:1.5rem;border-top:3px solid var(--gold)">
        <div style="display:flex;align-items:center;gap:0.75rem;margin-bottom:1rem">
          <div style="width:36px;height:36px;border-radius:50%;background:var(--gold-dim);border:2px solid var(--gold);display:flex;align-items:center;justify-content:center;font-weight:800;color:var(--gold);flex-shrink:0">1a</div>
          <div>
            <div style="font-weight:700">Definición de 2 términos</div>
            <div style="font-size:0.75rem;color:var(--gold)">2 puntos · ~15 minutos</div>
          </div>
        </div>
        <div style="font-size:0.83rem;line-height:1.7;color:var(--text2)">
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Estructura:</strong> Definición concisa (2-4 líneas) → Contexto en la obra → Relación con otro concepto del autor.</p>
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Longitud ideal:</strong> 8-10 líneas por término.</p>
          <p style="padding:0.5rem 0.75rem;background:var(--red-dim);border-left:3px solid var(--red);border-radius:4px;color:var(--text2)">❌ <strong>Error frecuente:</strong> Definir con sinónimos o de forma circular. Siempre aporta el contenido filosófico concreto del autor.</p>
        </div>
      </div>

      <!-- 1b -->
      <div style="background:var(--card);border:1px solid rgba(62,207,178,0.3);border-radius:var(--radius);padding:1.5rem;border-top:3px solid var(--teal)">
        <div style="display:flex;align-items:center;gap:0.75rem;margin-bottom:1rem">
          <div style="width:36px;height:36px;border-radius:50%;background:var(--teal-dim);border:2px solid var(--teal);display:flex;align-items:center;justify-content:center;font-weight:800;color:var(--teal);flex-shrink:0">1b</div>
          <div>
            <div style="font-weight:700">Idea principal y estructura</div>
            <div style="font-size:0.75rem;color:var(--teal)">2 puntos · ~15 minutos</div>
          </div>
        </div>
        <div style="font-size:0.83rem;line-height:1.7;color:var(--text2)">
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Estructura:</strong> 1) Idea principal en una frase → 2) Estructura del texto (divide en partes) → 3) Hilo argumentativo que las une.</p>
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Frase de inicio:</strong> <em>"La idea principal del texto es…"</em> o <em>"El autor defiende en este texto que…"</em></p>
          <p style="padding:0.5rem 0.75rem;background:var(--red-dim);border-left:3px solid var(--red);border-radius:4px;color:var(--text2)">❌ <strong>Error frecuente:</strong> Resumir el texto en lugar de identificar su estructura lógica y el argumento central.</p>
        </div>
      </div>

      <!-- 1c -->
      <div style="background:var(--card);border:1px solid rgba(91,141,238,0.3);border-radius:var(--radius);padding:1.5rem;border-top:3px solid var(--blue)">
        <div style="display:flex;align-items:center;gap:0.75rem;margin-bottom:1rem">
          <div style="width:36px;height:36px;border-radius:50%;background:var(--blue-dim);border:2px solid var(--blue);display:flex;align-items:center;justify-content:center;font-weight:800;color:var(--blue);flex-shrink:0">1c</div>
          <div>
            <div style="font-weight:700">Posición filosófica del autor</div>
            <div style="font-size:0.75rem;color:var(--blue)">2 puntos · ~20 minutos</div>
          </div>
        </div>
        <div style="font-size:0.83rem;line-height:1.7;color:var(--text2)">
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Estructura:</strong> Contexto histórico-filosófico → Problema del texto en el sistema del autor → Desarrollo de la posición → Obras relacionadas → Conclusión.</p>
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Longitud ideal:</strong> 25-35 líneas. La más larga e importante.</p>
          <p style="padding:0.5rem 0.75rem;background:var(--teal-dim);border-left:3px solid var(--teal);border-radius:4px;color:var(--text2)">✅ <strong>Clave del éxito:</strong> Usa vocabulario técnico del autor constantemente. Cada párrafo debe conectar con el texto.</p>
        </div>
      </div>

      <!-- 2a -->
      <div style="background:var(--card);border:1px solid rgba(167,139,250,0.3);border-radius:var(--radius);padding:1.5rem;border-top:3px solid var(--purple)">
        <div style="display:flex;align-items:center;gap:0.75rem;margin-bottom:1rem">
          <div style="width:36px;height:36px;border-radius:50%;background:var(--purple-dim);border:2px solid var(--purple);display:flex;align-items:center;justify-content:center;font-weight:800;color:var(--purple);flex-shrink:0">2a</div>
          <div>
            <div style="font-weight:700">Relación con otro autor</div>
            <div style="font-size:0.75rem;color:var(--purple)">2 puntos · ~20 minutos</div>
          </div>
        </div>
        <div style="font-size:0.83rem;line-height:1.7;color:var(--text2)">
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Estructura:</strong> Introduce el tema → Posición del autor A → Posición del autor B → Semejanzas → Diferencias → Conclusión valorativa.</p>
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Pares más frecuentes:</strong> Platón–Aristóteles, Descartes–Hume, Kant–Hume, Marx–Hegel, Nietzsche–Platón.</p>
          <p style="padding:0.5rem 0.75rem;background:var(--red-dim);border-left:3px solid var(--red);border-radius:4px;color:var(--text2)">❌ <strong>Error frecuente:</strong> Exponer a los autores por separado sin compararlos. Siempre usa conectores: <em>"mientras que", "por el contrario", "ambos coinciden en"</em>.</p>
        </div>
      </div>

      <!-- 2b -->
      <div style="background:var(--card);border:1px solid rgba(224,92,92,0.3);border-radius:var(--radius);padding:1.5rem;border-top:3px solid var(--red)">
        <div style="display:flex;align-items:center;gap:0.75rem;margin-bottom:1rem">
          <div style="width:36px;height:36px;border-radius:50%;background:var(--red-dim);border:2px solid var(--red);display:flex;align-items:center;justify-content:center;font-weight:800;color:var(--red);flex-shrink:0">2b</div>
          <div>
            <div style="font-weight:700">Valoración personal razonada</div>
            <div style="font-size:0.75rem;color:var(--red)">2 puntos · ~15 minutos</div>
          </div>
        </div>
        <div style="font-size:0.83rem;line-height:1.7;color:var(--text2)">
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Estructura:</strong> Toma de postura clara → 2 argumentos propios con ejemplos actuales → Contraargumento y respuesta → Conclusión.</p>
          <p style="margin-bottom:0.5rem"><strong style="color:var(--text)">Frase de inicio:</strong> <em>"Desde mi punto de vista…"</em> o <em>"Considero que la posición de [autor] resulta [convincente/problemática] porque…"</em></p>
          <p style="padding:0.5rem 0.75rem;background:var(--teal-dim);border-left:3px solid var(--teal);border-radius:4px;color:var(--text2)">✅ <strong>Clave:</strong> No uses el espacio para repetir al autor. Es TU opinión argumentada. Conecta con problemas del mundo actual.</p>
        </div>
      </div>

      <!-- Distribución tiempo -->
      <div style="background:linear-gradient(135deg,var(--card),var(--card2));border:1px solid rgba(201,168,76,0.4);border-radius:var(--radius);padding:1.5rem">
        <div style="font-weight:700;margin-bottom:1rem;font-size:1rem">⏱️ Distribución del Tiempo (90 min)</div>
        <div style="font-size:0.83rem;display:flex;flex-direction:column;gap:0.5rem">
          <div style="display:flex;justify-content:space-between;align-items:center">
            <span>Leer y subrayar el texto</span>
            <span style="background:var(--gold-dim);color:var(--gold);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">10 min</span>
          </div>
          <div style="display:flex;justify-content:space-between;align-items:center">
            <span>1a · Definiciones</span>
            <span style="background:var(--gold-dim);color:var(--gold);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">15 min</span>
          </div>
          <div style="display:flex;justify-content:space-between;align-items:center">
            <span>1b · Idea y estructura</span>
            <span style="background:var(--teal-dim);color:var(--teal);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">15 min</span>
          </div>
          <div style="display:flex;justify-content:space-between;align-items:center">
            <span>1c · Posición filosófica</span>
            <span style="background:var(--blue-dim);color:var(--blue);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">20 min</span>
          </div>
          <div style="display:flex;justify-content:space-between;align-items:center">
            <span>2a · Relación autores</span>
            <span style="background:var(--purple-dim);color:var(--purple);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">20 min</span>
          </div>
          <div style="display:flex;justify-content:space-between;align-items:center">
            <span>2b · Valoración personal</span>
            <span style="background:var(--red-dim);color:var(--red);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">15 min</span>
          </div>
          <div style="display:flex;justify-content:space-between;align-items:center;border-top:1px solid var(--border);padding-top:0.5rem;margin-top:0.25rem">
            <span style="font-weight:700">Revisar y repasar</span>
            <span style="background:var(--card2);color:var(--text2);padding:2px 8px;border-radius:50px;font-weight:700;font-size:0.75rem">5 min</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- CALCULADORA DE NOTA -->
<section id="calculadora" style="background:var(--bg)">
  <div class="container" style="max-width:640px">
    <div class="section-label">Herramienta práctica</div>
    <h2 class="section-title">🧮 Calculadora de Nota PAU</h2>
    <p class="section-sub">Introduce tus puntuaciones en cada pregunta y calcula tu nota final al instante.</p>
    <div style="background:var(--card);border:1px solid var(--border);border-radius:20px;padding:2rem;margin-top:2rem">
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1.5rem">
        <div>
          <label style="display:block;font-size:0.78rem;font-weight:700;color:var(--text2);margin-bottom:0.4rem;text-transform:uppercase;letter-spacing:0.05em">1a · Definiciones <span style="color:var(--text3)">(0–2)</span></label>
          <input type="number" id="n1a" min="0" max="2" step="0.25" value="0" oninput="calcularNota()" style="width:100%;padding:0.65rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;outline:none;text-align:center">
        </div>
        <div>
          <label style="display:block;font-size:0.78rem;font-weight:700;color:var(--text2);margin-bottom:0.4rem;text-transform:uppercase;letter-spacing:0.05em">1b · Idea principal <span style="color:var(--text3)">(0–2)</span></label>
          <input type="number" id="n1b" min="0" max="2" step="0.25" value="0" oninput="calcularNota()" style="width:100%;padding:0.65rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;outline:none;text-align:center">
        </div>
        <div>
          <label style="display:block;font-size:0.78rem;font-weight:700;color:var(--text2);margin-bottom:0.4rem;text-transform:uppercase;letter-spacing:0.05em">1c · Posición filosófica <span style="color:var(--text3)">(0–2)</span></label>
          <input type="number" id="n1c" min="0" max="2" step="0.25" value="0" oninput="calcularNota()" style="width:100%;padding:0.65rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;outline:none;text-align:center">
        </div>
        <div>
          <label style="display:block;font-size:0.78rem;font-weight:700;color:var(--text2);margin-bottom:0.4rem;text-transform:uppercase;letter-spacing:0.05em">2a · Relación autores <span style="color:var(--text3)">(0–2)</span></label>
          <input type="number" id="n2a" min="0" max="2" step="0.25" value="0" oninput="calcularNota()" style="width:100%;padding:0.65rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;outline:none;text-align:center">
        </div>
        <div style="grid-column:span 2">
          <label style="display:block;font-size:0.78rem;font-weight:700;color:var(--text2);margin-bottom:0.4rem;text-transform:uppercase;letter-spacing:0.05em">2b · Valoración personal <span style="color:var(--text3)">(0–2)</span></label>
          <input type="number" id="n2b" min="0" max="2" step="0.25" value="0" oninput="calcularNota()" style="width:100%;padding:0.65rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;outline:none;text-align:center">
        </div>
      </div>
      <div id="resultadoCalc" style="text-align:center;padding:1.5rem;background:var(--bg3);border-radius:var(--radius-sm);border:2px solid var(--border)">
        <div style="font-size:0.78rem;color:var(--text3);margin-bottom:0.3rem;text-transform:uppercase;letter-spacing:0.05em">Tu nota en Filosofía</div>
        <div id="notaFinal" style="font-size:3.5rem;font-weight:900;font-family:var(--font-mono);color:var(--text3)">0.00</div>
        <div id="notaLabel" style="font-size:0.9rem;color:var(--text3);margin-top:0.25rem">Introduce tus puntuaciones</div>
        <div style="margin-top:1rem;font-size:0.78rem;color:var(--text3)">Recuerda: la nota de filosofía se pondera con el resto de asignaturas en la nota final de la PAU.</div>
      </div>
    </div>
  </div>
</section>

<!-- DATOS CURIOSOS -->
<section id="curiosidades" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">¿Lo sabías?</div>
    <h2 class="section-title">🤯 Datos Curiosos de los Filósofos</h2>
    <p class="section-sub">Lo que no viene en el libro de texto pero que hace que no se te olviden nunca. Además te sirven para enriquecer la valoración personal del examen.</p>
    <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1.25rem;margin-top:2rem" id="curiosidadesGrid"></div>
  </div>
</section>

<!-- MAPA CONCEPTUAL / RELACIONES -->
<section id="relaciones" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Pregunta 2a</div>
    <h2 class="section-title">🕸️ Mapa de Relaciones entre Autores</h2>
    <p class="section-sub">Los pares más frecuentes en la pregunta 2a del examen. Haz clic en cualquier par para ver semejanzas y diferencias.</p>
    <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:1rem;margin-top:2rem" id="relacionesGrid"></div>
  </div>
</section>

<!-- SIMULACRO -->
<section id="simulacro" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Examen completo</div>
    <h2 class="section-title">Simulacro de Examen PAU</h2>
    <p class="section-sub">90 minutos, condiciones reales. Corrección automática al terminar.</p>
    <div class="exam-container">
      <div class="exam-header-box">
        <div>
          <div style="font-size:0.72rem;color:var(--text3);margin-bottom:0.2rem;text-transform:uppercase;letter-spacing:0.08em">Tiempo restante</div>
          <div class="exam-timer" id="examTimer">90:00</div>
        </div>
        <div style="text-align:right">
          <div style="font-size:0.78rem;color:var(--text2);margin-bottom:0.4rem">Filosofía · PAU Andalucía 2026</div>
          <div style="display:flex;gap:0.5rem;flex-wrap:wrap;justify-content:flex-end">
            <span class="tag tag-gold">Platón — República</span>
            <button class="btn-primary" style="font-size:0.8rem;padding:0.45rem 1rem;border:none;cursor:pointer" id="startExam">▶ Iniciar</button>
          </div>
        </div>
      </div>
      <div style="background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.35rem;margin-bottom:1.35rem">
        <div style="font-size:0.7rem;font-weight:700;color:var(--gold);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.65rem">Texto — Platón, República VII, 514a–517a</div>
        <p style="font-size:0.875rem;color:var(--text2);line-height:1.75;font-style:italic">"Imagínate hombres que están en una morada subterránea [...] que no han visto nunca la luz del sol. [...] ¿Crees que semejantes hombres habrían visto otra cosa de sí mismos o de sus compañeros que las sombras proyectadas por el fuego sobre la parte de la caverna que está frente a ellos? [...] Y si pudieran hablar unos con otros, ¿no piensas que creerían estar nombrando objetos reales cuando nombraban lo que veían?"</p>
      </div>
      <div class="exam-section-title">CUESTIÓN 1a — Definición de términos (2 puntos)</div>
      <p style="font-size:0.83rem;color:var(--text2);margin-bottom:0.85rem">Define los términos <strong>sombras</strong> y <strong>luz del sol</strong> en el contexto del pensamiento platónico.</p>
      <textarea class="exam-textarea" placeholder="Escribe tu respuesta aquí..." id="resp1a" oninput="updateWC('wc1a',this.value)"></textarea>
      <div class="word-count" id="wc1a">0 palabras</div>
      <div class="exam-section-title">CUESTIÓN 1b — Idea principal y estructura (2 puntos)</div>
      <textarea class="exam-textarea" placeholder="Expón la idea principal del texto y su estructura argumentativa..." id="resp1b" oninput="updateWC('wc1b',this.value)"></textarea>
      <div class="word-count" id="wc1b">0 palabras</div>
      <div class="exam-section-title">CUESTIÓN 1c — Posición filosófica del autor (2 puntos)</div>
      <textarea class="exam-textarea" placeholder="Relaciona el texto con la filosofía de Platón..." id="resp1c" oninput="updateWC('wc1c',this.value)"></textarea>
      <div class="word-count" id="wc1c">0 palabras</div>
      <div class="exam-section-title">CUESTIÓN 2a — Relación con otro autor (2 puntos)</div>
      <textarea class="exam-textarea" placeholder="Relaciona con Aristóteles o Descartes..." id="resp2a" oninput="updateWC('wc2a',this.value)"></textarea>
      <div class="word-count" id="wc2a">0 palabras</div>
      <div class="exam-section-title">CUESTIÓN 2b — Valoración personal (2 puntos)</div>
      <textarea class="exam-textarea" placeholder="Tu valoración personal razonada..." id="resp2b" oninput="updateWC('wc2b',this.value)"></textarea>
      <div class="word-count" id="wc2b">0 palabras</div>
      <div style="text-align:center;margin-top:1.75rem">
        <button class="btn-primary" onclick="submitExam()" style="border:none;cursor:pointer">Entregar y ver corrección ✓</button>
      </div>
      <div id="examFeedback" style="display:none;margin-top:1.5rem"></div>
    </div>
  </div>
</section>

<!-- EXÁMENES PAU -->
<section id="examenes" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Exámenes reales corregidos</div>
    <h2 class="section-title">Exámenes PAU Andalucía — Corregidos</h2>
    <p class="section-sub">Exámenes oficiales desde 2015 hasta 2026 con orientación completa de respuesta.</p>
    <div style="background:linear-gradient(135deg,#1e1a0f,#2a2210);border:1px solid rgba(201,168,76,0.5);border-radius:20px;padding:2rem;margin:2.5rem 0 2rem;position:relative;overflow:hidden">
      <div style="position:absolute;top:14px;right:14px;background:var(--gold);color:#0d0f14;font-size:0.68rem;font-weight:800;padding:0.25rem 0.8rem;border-radius:50px;letter-spacing:0.08em">ESTE AÑO · 2026</div>
      <div style="font-size:0.72rem;color:var(--gold);font-weight:700;letter-spacing:0.1em;text-transform:uppercase;margin-bottom:0.65rem">PAU Andalucía — Junio 2026</div>
      <h3 style="font-size:1.25rem;font-weight:800;margin-bottom:0.45rem">Examen Oficial · Convocatoria Ordinaria</h3>
      <p style="font-size:0.85rem;color:var(--text2);margin-bottom:1.1rem">Opción A: <strong style="color:var(--gold)">Kant</strong> — Fundamentación de la Metafísica de las Costumbres &nbsp;|&nbsp; Opción B: <strong style="color:var(--gold)">Nietzsche</strong> — La Gaya Ciencia §125</p>
      <div id="examen2026" style="display:none">
        <div style="background:var(--card);border-radius:var(--radius);padding:1.35rem;margin-bottom:0.85rem;border:1px solid var(--border)">
          <h4 style="color:var(--gold);font-size:0.9rem;margin-bottom:0.65rem">📝 Orientación Opción A — Kant</h4>
          <p style="font-size:0.83rem;color:var(--text2);margin-bottom:0.6rem"><strong style="color:var(--text)">1a.</strong> <em>Humanidad</em>: la racionalidad y capacidad moral del ser humano, lo que nos hace dignos de respeto. <em>Fin en sí mismo</em>: el ser racional tiene valor intrínseco, no derivado de utilidad.</p>
          <p style="font-size:0.83rem;color:var(--text2);margin-bottom:0.6rem"><strong style="color:var(--text)">1b.</strong> Segunda formulación del imperativo categórico (fórmula de la humanidad). Estructura: obligación → ámbito → distinción fin/medio.</p>
          <p style="font-size:0.83rem;color:var(--text2);margin-bottom:0.6rem"><strong style="color:var(--text)">1c.</strong> Ética deontológica kantiana: ley moral formal, universal, incondicional. Autonomía moral y reino de los fines.</p>
          <p style="font-size:0.83rem;color:var(--text2)"><strong style="color:var(--text)">2b.</strong> Aplicar a problemas actuales: trata de seres humanos, explotación laboral, uso de datos personales. El principio kantiano en bioética y derechos humanos.</p>
        </div>
        <div style="background:var(--card);border-radius:var(--radius);padding:1.35rem;border:1px solid var(--border)">
          <h4 style="color:var(--teal);font-size:0.9rem;margin-bottom:0.65rem">📝 Orientación Opción B — Nietzsche</h4>
          <p style="font-size:0.83rem;color:var(--text2);margin-bottom:0.6rem"><strong style="color:var(--text)">1a.</strong> <em>Dios</em>: valores absolutos trascendentes de la civilización occidental. <em>Nihilismo</em>: situación en que los valores supremos pierden validez.</p>
          <p style="font-size:0.83rem;color:var(--text2);margin-bottom:0.6rem"><strong style="color:var(--text)">1b.</strong> El loco anuncia la muerte de Dios: el mayor acontecimiento de la modernidad. Estructura narrativa-profética.</p>
          <p style="font-size:0.83rem;color:var(--text2)"><strong style="color:var(--text)">2b.</strong> Relativismo moral actual, crisis de valores, fundamentalismos. ¿Hemos encontrado nuevos valores? El diagnóstico nietzscheano sigue siendo relevante.</p>
        </div>
      </div>
      <button onclick="toggleExamen('examen2026',this)" style="background:var(--gold);color:#0d0f14;border:none;padding:0.65rem 1.35rem;border-radius:var(--radius-sm);font-weight:700;font-size:0.85rem;cursor:pointer;margin-top:1rem">Ver corrección completa ↓</button>
    </div>
    <h3 style="font-size:1.05rem;font-weight:700;margin-bottom:1.35rem">Años anteriores</h3>
    <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(270px,1fr));gap:1.1rem" id="examenesGrid"></div>
  </div>
</section>

<!-- BANCO -->
<section id="banco" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Selectividad real</div>
    <h2 class="section-title">Banco de Preguntas PAU Andalucía</h2>
    <p class="section-sub">Preguntas reales ordenadas por autor, año y tipo con orientación de respuesta.</p>
    <div class="banco-search">
      <input class="search-input" placeholder="🔍 Buscar por autor, tema o concepto..." id="bancoSearch" oninput="filterBanco()">
      <select class="filter-select" id="bancoFilter" onchange="filterBanco()">
        <option value="all">Todos los autores</option>
        <option value="Platón">Platón</option>
        <option value="Aristóteles">Aristóteles</option>
        <option value="Descartes">Descartes</option>
        <option value="Hume">Hume</option>
        <option value="Kant">Kant</option>
        <option value="Nietzsche">Nietzsche</option>
        <option value="Marx">Marx</option>
      </select>
    </div>
    <div class="banco-list" id="bancoList"></div>
  </div>
</section>

<!-- PODCASTS -->
<!-- MIS VÍDEOS -->
<section id="mis-videos" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">FilosoFEANDO en vídeo</div>
    <h2 class="section-title">🎬 Mis Vídeos</h2>
    <p class="section-sub">Todo el contenido de TikTok e Instagram organizado por categorías.</p>
    <div style="display:flex;gap:0.5rem;flex-wrap:wrap;margin-top:1.5rem;margin-bottom:1.5rem" id="vTabBar">
      <button class="tab-btn" onclick="vFiltrar('todos',this)" style="background:var(--gold-dim);border-color:var(--gold);color:var(--gold)">Todos</button>
      <button class="tab-btn" onclick="vFiltrar('filosofo',this)">👤 Filósofos</button>
      <button class="tab-btn" onclick="vFiltrar('reflexion',this)">💭 Reflexión</button>
      <button class="tab-btn" onclick="vFiltrar('arte',this)">🎨 Arte</button>
      <button class="tab-btn" onclick="vFiltrar('web',this)">🌐 Mi Web</button>
      <button class="tab-btn" onclick="vFiltrar('tiktok',this)">TikTok</button>
      <button class="tab-btn" onclick="vFiltrar('instagram',this)">Instagram</button>
    </div>
    <div id="vAvatares" style="display:flex;gap:0.65rem;flex-wrap:wrap;margin-bottom:1.25rem"></div>
    <div id="vGrid" style="display:flex;flex-direction:column;gap:0.6rem"></div>
    <div style="text-align:center;margin-top:1.75rem;display:flex;gap:0.75rem;justify-content:center;flex-wrap:wrap">
      <a href="https://www.tiktok.com/@filosofeando_para_aproba" target="_blank" rel="noopener" style="display:flex;align-items:center;gap:0.5rem;padding:0.55rem 1.1rem;background:#010101;color:#fff;border-radius:50px;font-size:0.83rem;font-weight:700;text-decoration:none">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M19.59 6.69a4.83 4.83 0 01-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 01-2.88 2.5 2.89 2.89 0 01-2.89-2.89 2.89 2.89 0 012.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 00-.79-.05 6.34 6.34 0 00-6.34 6.34 6.34 6.34 0 006.34 6.34 6.34 6.34 0 006.33-6.34V8.69a8.17 8.17 0 004.77 1.52V6.75a4.85 4.85 0 01-1-.06z"/></svg>
        Seguir en TikTok
      </a>
      <a href="https://www.instagram.com/filosofeando_para_aprobar/" target="_blank" rel="noopener" style="display:flex;align-items:center;gap:0.5rem;padding:0.55rem 1.1rem;background:linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045);color:#fff;border-radius:50px;font-size:0.83rem;font-weight:700;text-decoration:none">
        <svg width="13" height="13" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
        Seguir en Instagram
      </a>
    </div>
  </div>
</section>

<section id="podcasts">
  <div class="container">
    <div class="section-label">Escucha y aprende</div>
    <h2 class="section-title">Podcasts de Filosofía</h2>
    <p class="section-sub">Los mejores podcasts en español para profundizar en los autores del currículo PAU mientras vas al instituto, haces deporte o te relajas.</p>
    <div class="podcasts-grid" id="podcastsGrid"></div>
  </div>
</section>

<!-- LIBROS -->
<section id="libros">
  <div class="container">
    <div class="section-label">Lecturas recomendadas</div>
    <h2 class="section-title">Biblioteca FilosoFEANDO</h2>
    <p class="section-sub">Libros seleccionados por nivel para entender a los grandes filósofos sin morir en el intento.</p>
    <div class="libros-tabs">
      <button class="tab-btn active" data-libfilter="all">Todos</button>
      <button class="tab-btn" data-libfilter="pau">Para la PAU</button>
      <button class="tab-btn" data-libfilter="divulgacion">Divulgación</button>
      <button class="tab-btn" data-libfilter="original">Obras originales</button>
    </div>
    <div class="libros-grid" id="librosGrid"></div>
  </div>
</section>

<!-- PROGRESO -->
<section id="progreso" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Mi estudio</div>
    <h2 class="section-title">Seguimiento del Progreso</h2>
    <p class="section-sub">Controla tu avance y mantén tu racha de estudio activa.</p>
    <div class="progreso-grid">
      <div class="progreso-card">
        <h3>Progreso Global <span id="fechaHoy"></span></h3>
        <div class="radial-wrap">
          <div class="radial-chart">
            <svg viewBox="0 0 120 120" width="130" height="130">
              <circle class="radial-bg" cx="60" cy="60" r="50"/>
              <circle class="radial-fill" id="radialFill" cx="60" cy="60" r="50" stroke-dasharray="314" stroke-dashoffset="220"/>
            </svg>
            <div class="radial-label">
              <div class="radial-pct" id="radialPct">30%</div>
              <div class="radial-sub">completado</div>
            </div>
          </div>
        </div>
        <div class="autor-progress-list" id="autorProgressList"></div>
      </div>
      <div class="progreso-card">
        <h3>Estadísticas</h3>
        <div style="display:grid;grid-template-columns:1fr 1fr;gap:0.85rem;margin-bottom:1.35rem">
          <div style="background:var(--card2);border-radius:var(--radius-sm);padding:0.9rem;text-align:center">
            <div style="font-family:var(--font-display);font-size:1.9rem;font-weight:800;color:var(--gold)">47</div>
            <div style="font-size:0.72rem;color:var(--text3);text-transform:uppercase;letter-spacing:0.06em">Flashcards</div>
          </div>
          <div style="background:var(--card2);border-radius:var(--radius-sm);padding:0.9rem;text-align:center">
            <div style="font-family:var(--font-display);font-size:1.9rem;font-weight:800;color:var(--teal)">73%</div>
            <div style="font-size:0.72rem;color:var(--text3);text-transform:uppercase;letter-spacing:0.06em">Aciertos test</div>
          </div>
          <div style="background:var(--card2);border-radius:var(--radius-sm);padding:0.9rem;text-align:center">
            <div style="font-family:var(--font-display);font-size:1.9rem;font-weight:800;color:var(--blue)">3</div>
            <div style="font-size:0.72rem;color:var(--text3);text-transform:uppercase;letter-spacing:0.06em">Simulacros</div>
          </div>
          <div style="background:var(--card2);border-radius:var(--radius-sm);padding:0.9rem;text-align:center">
            <div style="font-family:var(--font-display);font-size:1.9rem;font-weight:800;color:var(--red)">6🔥</div>
            <div style="font-size:0.72rem;color:var(--text3);text-transform:uppercase;letter-spacing:0.06em">Racha</div>
          </div>
        </div>
        <h4 style="font-size:0.82rem;font-weight:700;margin-bottom:0.75rem;color:var(--text2)">Racha semanal</h4>
        <div style="display:flex;gap:0.6rem;justify-content:center">
          <div class="streak-day done">L</div><div class="streak-day done">M</div><div class="streak-day done">X</div>
          <div class="streak-day done">J</div><div class="streak-day done">V</div><div class="streak-day today">S</div><div class="streak-day">D</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONSEJOS -->
<section id="consejos" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Consejos expertos</div>
    <h2 class="section-title">Cómo Sacar un 10 en la PAU</h2>
    <div class="consejos-grid">
      <div class="consejo-card reveal"><div class="consejo-num">1</div><h4>Domina el vocabulario técnico</h4><p>Usa siempre los términos filosóficos propios del autor. Los correctores valoran la precisión conceptual. Escribe «eudaimonia», «cogito», «imperativo categórico», no sus sinónimos vagos.</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">2</div><h4>Estructura cada respuesta</h4><p>Usa párrafos con introducción, desarrollo y conclusión. En la 1c: <strong>contexto histórico → tesis del autor → argumentos principales → conclusión</strong>. En la 2b: tesis propia → 2 argumentos → conclusión.</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">3</div><h4>Contextualiza siempre</h4><p>Sitúa al autor en su época, corriente filosófica y obra principal. Dos frases de contexto al inicio demuestran madurez intelectual y dan puntos extra.</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">4</div><h4>Prepara los 4 pares clave</h4><p>La pregunta 2a sale siempre. Memoriza: <strong>Platón-Aristóteles</strong> (mundo ideas vs. formas en materia), <strong>Descartes-Hume</strong> (razón vs. experiencia), <strong>Hume-Kant</strong> (escepticismo vs. crítica), <strong>Marx-Nietzsche</strong> (alienación social vs. valorativa).</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">5</div><h4>Construye tu valoración personal</h4><p>La 2b es TU oportunidad. Prepara 2-3 argumentos propios con ejemplos actuales (IA, redes sociales, política actual). Muestra que has pensado, no que has memorizado.</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">6</div><h4>Lee el texto 3 veces</h4><p><strong>1ª lectura:</strong> comprensión global. <strong>2ª lectura:</strong> subraya ideas clave y términos. <strong>3ª lectura:</strong> identifica la tesis y la estructura argumentativa. Dedica 10 minutos a esto, te ahorrará tiempo después.</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">7</div><h4>Gestiona el tiempo</h4><p>90 minutos divididos así: 10' leer → 15' definiciones → 15' idea principal → 20' posición filosófica → 20' relación autores → 15' valoración → 5' revisar. Nunca te saltes la revisión final.</p></div>
      <div class="consejo-card reveal"><div class="consejo-num">8</div><h4>Cuida la presentación</h4><p>Letra legible, párrafos diferenciados, sin tachones excesivos. Los correctores leen decenas de exámenes: una presentación clara predispone positivamente. Usa conectores: «en primer lugar», «sin embargo», «en conclusión».</p></div>
    </div>
    <div style="margin-top:2.5rem;padding:1.5rem;background:var(--card);border:1px solid rgba(224,92,92,0.3);border-radius:var(--radius);border-left:4px solid var(--red)">
      <div style="font-weight:800;font-size:1rem;margin-bottom:1rem;color:var(--red)">❌ Los 8 errores que más puntos te cuestan</div>
      <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:0.75rem">
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">1a ·</strong> Definir con sinónimos circulares («el cogito es el cogito»). Siempre aporte contenido filosófico real.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">1a ·</strong> Mezclar conceptos de distintos autores. El cogito es de Descartes, no de Platón.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">1b ·</strong> Resumir el texto en lugar de analizar su estructura lógica y argumento central.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">1c ·</strong> Copiar frases del texto en lugar de elaborar la posición filosófica completa del autor.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">2a ·</strong> Solo listar semejanzas sin explicar las diferencias, o viceversa. Siempre ambas partes.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">2a ·</strong> Relacionar autores que no tienen conexión temática real. Justifica siempre el nexo.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">2b ·</strong> Repetir lo que dijo el autor en lugar de dar TU valoración personal y argumentada.</div>
        <div style="font-size:0.82rem;color:var(--text2);padding:0.6rem 0.85rem;background:var(--red-dim);border-radius:8px;line-height:1.5"><strong style="color:var(--red)">General ·</strong> No repasar el examen los últimos 5 minutos. Siempre hay algo que mejorar.</div>
      </div>
    </div>
  </div>
</section>

<!-- PREMIUM -->
<section id="premium">
  <div class="container">
    <div style="text-align:center">
      <div class="section-label" style="display:inline-block">Próximamente</div>
      <h2 class="section-title" style="margin:0 auto">Planes de Acceso</h2>
      <p class="section-sub" style="margin:0 auto 2.5rem">La plataforma es <strong>gratis para siempre</strong>. Los planes premium desbloquean contenido extra y apoyan el proyecto.</p>
    </div>
    <div class="premium-grid">
      <div class="premium-card">
        <div class="plan-name">Gratuito</div>
        <div class="plan-price"><sup>€</sup>0<span>/mes</span></div>
        <div class="plan-desc">Todo lo esencial para aprobar</div>
        <ul class="plan-features">
          <li>6 autores completos</li><li>20 flashcards</li><li>Tests autocorregibles</li>
          <li>1 simulacro de examen</li><li>Banco PAU básico</li><li>Juegos filosóficos</li>
          <li class="no">Todos los autores</li><li class="no">Corrección con IA</li>
        </ul>
        <button class="btn-plan btn-plan-free" onclick="document.getElementById('autores').scrollIntoView({behavior:'smooth'})">Empezar gratis</button>
      </div>
      <div class="premium-card featured">
        <div class="plan-name">Premium</div>
        <div class="plan-price"><sup>€</sup>9<span>,99/mes</span></div>
        <div class="plan-desc">Acceso total para sacar un 10</div>
        <ul class="plan-features">
          <li>Todos los autores completos</li><li>500+ flashcards por tema</li><li>Tests ilimitados</li>
          <li>Simulacros ilimitados</li><li>Banco PAU completo 2010–2026</li>
          <li>Corrección con IA explicada</li><li>Comparativas y esquemas</li><li>Seguimiento avanzado</li>
        </ul>
        <a href="https://paypal.me/alvato/9.99" target="_blank" rel="noopener" class="btn-plan btn-plan-premium">
          Acceder con PayPal ✦
        </a>
      </div>
      <div class="premium-card">
        <div class="plan-name">Intensivo PAU</div>
        <div class="plan-price"><sup>€</sup>24<span>,99</span></div>
        <div class="plan-desc">Curso de 4 semanas con tutor</div>
        <ul class="plan-features">
          <li>Todo lo de Premium</li><li>4 clases en directo (Zoom)</li>
          <li>Corrección personalizada</li><li>Plan de estudio personalizado</li>
          <li>Grupo privado de Telegram</li><li>Garantía de nota o devolución</li>
          <li class="no">—</li><li class="no">—</li>
        </ul>
        <a href="https://paypal.me/alvato/24.99" target="_blank" rel="noopener" class="btn-plan btn-plan-free" style="display:block">
          Reservar con PayPal
        </a>
      </div>
    </div>
  </div>
</section>

<!-- COMMUNITY WIDGET -->
<section style="background:var(--bg2);padding:4rem 2rem">
  <div class="container">
    <div class="community-widget">
      <div style="font-size:3rem;margin-bottom:1rem;animation:float 3s ease infinite">🎓</div>
      <h3>¡Somos una comunidad de filósofos!</h3>
      <p>Esta plataforma es <strong style="color:var(--gold)">100% gratuita</strong> y la mantengo con mucho esfuerzo. Si te ayuda a preparar la PAU, apóyame siguiéndome en redes, compartiendo con tus compañeros y, si puedes, con una pequeña donación. ¡Juntos hacemos que la Filosofía mole!</p>
      <div class="community-btns">
        <a href="https://www.tiktok.com/@filosofeando_para_aproba" target="_blank" rel="noopener" class="btn-tiktok" style="font-size:0.95rem;padding:0.75rem 1.5rem">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M19.59 6.69a4.83 4.83 0 01-3.77-4.25V2h-3.45v13.67a2.89 2.89 0 01-2.88 2.5 2.89 2.89 0 01-2.89-2.89 2.89 2.89 0 012.89-2.89c.28 0 .54.04.79.1V9.01a6.33 6.33 0 00-.79-.05 6.34 6.34 0 00-6.34 6.34 6.34 6.34 0 006.34 6.34 6.34 6.34 0 006.33-6.34V8.69a8.17 8.17 0 004.77 1.52V6.75a4.85 4.85 0 01-1-.06z"/></svg>
          Seguir en TikTok · Dale like y comparte 🙏
        </a>
        <a href="https://www.instagram.com/filosofeando_para_aprobar/" target="_blank" rel="noopener" class="btn-instagram" style="font-size:0.95rem;padding:0.75rem 1.5rem">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          Seguir en Instagram · Comparte stories 📸
        </a>
        <a href="https://paypal.me/alvato" target="_blank" rel="noopener" class="btn-paypal" style="font-size:0.95rem;padding:0.75rem 1.5rem">
          <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M7.076 21.337H2.47a.641.641 0 0 1-.633-.74L4.944.901C5.026.382 5.474 0 5.998 0h7.46c2.57 0 4.578.543 5.69 1.81 1.01 1.15 1.304 2.42 1.012 4.287-.023.143-.047.288-.077.437-.983 5.05-4.349 6.797-8.647 6.797h-2.19c-.524 0-.968.382-1.05.9l-1.12 7.106zm14.146-14.42a3.35 3.35 0 0 0-.607-.541c-.013.076-.026.175-.041.254-.93 4.778-4.005 7.201-9.138 7.201h-2.19a.563.563 0 0 0-.556.479l-1.187 7.527h-.506l-.24 1.516a.56.56 0 0 0 .554.647h3.882c.46 0 .85-.334.922-.788.06-.26.76-4.852.816-5.09a.932.932 0 0 1 .923-.788h.58c3.76 0 6.705-1.528 7.565-5.946.36-1.847.174-3.388-.777-4.471z"/></svg>
          Donar con PayPal ❤️
        </a>
      </div>
      <div class="community-steps">
        <div class="community-step"><div class="community-step-icon">👍</div><p>Dale like a los vídeos para que lleguen a más estudiantes</p></div>
        <div class="community-step"><div class="community-step-icon">🔔</div><p>Activa las notificaciones para no perderte ningún vídeo nuevo</p></div>
        <div class="community-step"><div class="community-step-icon">📤</div><p>Comparte con tus compañeros de clase que estén preparando la PAU</p></div>
        <div class="community-step"><div class="community-step-icon">💬</div><p>Comenta tus dudas y las respondo en el próximo vídeo</p></div>
      </div>
    </div>
  </div>
</section>

<!-- SUGERENCIAS -->
<section id="sugerencias" style="background:var(--bg2)">
  <div class="container" style="max-width:680px">
    <div class="section-label">Tu opinión importa</div>
    <h2 class="section-title">💬 Sugerencias y Mejoras</h2>
    <p class="section-sub">¿Echas en falta algo? ¿Quieres que añada un autor, un juego, un examen resuelto? Cuéntamelo aquí y lo tendré en cuenta para las próximas actualizaciones.</p>

    <div style="background:var(--card);border:1px solid rgba(201,168,76,0.2);border-radius:20px;padding:2rem;margin-top:2rem">
      <!-- AVISO FORMSPREE -->
      <div id="formsprееAviso" style="background:var(--gold-dim);border:1px solid rgba(201,168,76,0.4);border-radius:var(--radius-sm);padding:1rem;margin-bottom:1.5rem;font-size:0.82rem;line-height:1.6">
        <strong style="color:var(--gold)">⚙️ Paso necesario (solo una vez):</strong><br>
      <form id="sugerenciasForm" action="https://formspree.io/f/xlgkgjer" method="POST" onsubmit="enviarSugerencia(event)">
        <!-- Tipo de sugerencia -->
        <div style="margin-bottom:1.25rem">
          <label style="display:block;font-size:0.82rem;font-weight:700;color:var(--text2);margin-bottom:0.6rem;text-transform:uppercase;letter-spacing:0.05em">¿Sobre qué es tu sugerencia?</label>
          <div style="display:flex;flex-wrap:wrap;gap:0.5rem">
            <label style="display:flex;align-items:center;gap:0.4rem;cursor:pointer">
              <input type="radio" name="tipo" value="Contenido/Temario" style="accent-color:var(--gold)" checked> <span style="font-size:0.85rem">📚 Contenido</span>
            </label>
            <label style="display:flex;align-items:center;gap:0.4rem;cursor:pointer">
              <input type="radio" name="tipo" value="Juegos" style="accent-color:var(--gold)"> <span style="font-size:0.85rem">🎮 Juegos</span>
            </label>
            <label style="display:flex;align-items:center;gap:0.4rem;cursor:pointer">
              <input type="radio" name="tipo" value="Exámenes resueltos" style="accent-color:var(--gold)"> <span style="font-size:0.85rem">📝 Exámenes</span>
            </label>
            <label style="display:flex;align-items:center;gap:0.4rem;cursor:pointer">
              <input type="radio" name="tipo" value="Diseño/Web" style="accent-color:var(--gold)"> <span style="font-size:0.85rem">🎨 Diseño</span>
            </label>
            <label style="display:flex;align-items:center;gap:0.4rem;cursor:pointer">
              <input type="radio" name="tipo" value="Otro" style="accent-color:var(--gold)"> <span style="font-size:0.85rem">💡 Otro</span>
            </label>
          </div>
        </div>

        <!-- Sugerencia -->
        <div style="margin-bottom:1.25rem">
          <label style="display:block;font-size:0.82rem;font-weight:700;color:var(--text2);margin-bottom:0.6rem;text-transform:uppercase;letter-spacing:0.05em">Tu sugerencia *</label>
          <textarea name="mensaje" required rows="4" placeholder="Ej: Me gustaría que añadieras un resumen de Ortega y Gasset, o un juego de completar frases célebres…" style="width:100%;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);padding:0.85rem;font-family:var(--font-body);font-size:0.9rem;resize:vertical;transition:border var(--transition);outline:none" onfocus="this.style.borderColor='var(--gold)'" onblur="this.style.borderColor='var(--border)'"></textarea>
        </div>

        <!-- Email opcional -->
        <div style="margin-bottom:1.5rem">
          <label style="display:block;font-size:0.82rem;font-weight:700;color:var(--text2);margin-bottom:0.6rem;text-transform:uppercase;letter-spacing:0.05em">Tu email <span style="font-weight:400;text-transform:none;color:var(--text3)">(opcional — para avisarte cuando lo añada)</span></label>
          <input type="email" name="email" placeholder="tucorreo@gmail.com" style="width:100%;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);padding:0.75rem 1rem;font-family:var(--font-body);font-size:0.9rem;outline:none;transition:border var(--transition)" onfocus="this.style.borderColor='var(--gold)'" onblur="this.style.borderColor='var(--border)'">
          <p style="font-size:0.75rem;color:var(--text3);margin-top:0.4rem">📌 Solo se usará para responderte. No se cede a terceros ni se usa para publicidad.</p>
        </div>

        <button type="submit" style="width:100%;padding:0.9rem;background:linear-gradient(135deg,var(--gold),#a8732e);color:#0d0f14;border:none;border-radius:var(--radius-sm);font-size:1rem;font-weight:800;cursor:pointer;transition:all var(--transition);letter-spacing:0.02em" onmouseover="this.style.transform='translateY(-2px)';this.style.boxShadow='0 6px 24px rgba(201,168,76,0.4)'" onmouseout="this.style.transform='none';this.style.boxShadow='none'">
          ✉️ Enviar sugerencia
        </button>
      </form>

      <!-- MENSAJE ÉXITO -->
      <div id="sugerenciasOk" style="display:none;text-align:center;padding:2rem 1rem">
        <div style="font-size:3rem;margin-bottom:0.75rem">🙏</div>
        <h3 style="margin-bottom:0.5rem;color:var(--gold)">¡Gracias por tu sugerencia!</h3>
        <p style="color:var(--text2);font-size:0.9rem;line-height:1.6">La he recibido y la tendré muy en cuenta para mejorar la plataforma.<br>Si dejaste tu email, te aviso cuando lo añada. ¡Sigue estudiando! 💪</p>
        <button onclick="document.getElementById('sugerenciasOk').style.display='none';document.getElementById('sugerenciasForm').style.display='block'" style="margin-top:1.25rem;background:var(--gold-dim);border:1px solid rgba(201,168,76,0.3);color:var(--gold);padding:0.55rem 1.25rem;border-radius:var(--radius-sm);font-size:0.85rem;font-weight:700;cursor:pointer">Enviar otra sugerencia</button>
      </div>
    </div>

    <!-- STATS motivacionales -->
    <div style="display:flex;gap:1rem;margin-top:1.5rem;flex-wrap:wrap">
      <div style="flex:1;min-width:140px;background:var(--card);border:1px solid var(--border);border-radius:var(--radius-sm);padding:1rem;text-align:center">
        <div style="font-size:1.5rem;font-weight:800;color:var(--gold)">100%</div>
        <div style="font-size:0.78rem;color:var(--text2)">Sugerencias leídas</div>
      </div>
      <div style="flex:1;min-width:140px;background:var(--card);border:1px solid var(--border);border-radius:var(--radius-sm);padding:1rem;text-align:center">
        <div style="font-size:1.5rem;font-weight:800;color:var(--teal)">48h</div>
        <div style="font-size:0.78rem;color:var(--text2)">Tiempo de respuesta máximo</div>
      </div>
      <div style="flex:1;min-width:140px;background:var(--card);border:1px solid var(--border);border-radius:var(--radius-sm);padding:1rem;text-align:center">
        <div style="font-size:1.5rem;font-weight:800;color:var(--purple)">♾️</div>
        <div style="font-size:0.78rem;color:var(--text2)">Mejoras planeadas</div>
      </div>
    </div>
  </div>
</section>

<!-- IA CORRECTORA -->
<section id="ia-correctora" style="background:var(--bg)">
  <div class="container" style="max-width:720px">
    <div class="section-label">Inteligencia Artificial</div>
    <h2 class="section-title">🤖 IA Correctora de Comentarios</h2>
    <p class="section-sub">Escribe tu respuesta a la pregunta 1c o 2b y la IA la analiza: conceptos, nota estimada y consejo.</p>
    <div style="background:var(--card);border:1px solid rgba(62,207,178,0.3);border-radius:20px;padding:1.75rem;margin-top:1.5rem">
      <div style="display:flex;gap:0.5rem;flex-wrap:wrap;margin-bottom:1rem">
        <button id="btn1c" onclick="iaSetTipo('1c')" style="padding:0.4rem 1rem;border-radius:50px;font-size:0.82rem;font-weight:700;cursor:pointer;background:var(--teal-dim);border:2px solid var(--teal);color:var(--teal)">1c · Posición filosófica</button>
        <button id="btn2b" onclick="iaSetTipo('2b')" style="padding:0.4rem 1rem;border-radius:50px;font-size:0.82rem;font-weight:700;cursor:pointer;background:var(--card2);border:2px solid var(--border);color:var(--text2)">2b · Valoración personal</button>
      </div>
      <select id="iaAutor" style="width:100%;padding:0.65rem 1rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-family:var(--font-body);font-size:0.9rem;outline:none;margin-bottom:1rem">
        <option>Platón</option><option>Aristóteles</option><option>Descartes</option>
        <option>Hume</option><option>Kant</option><option>Nietzsche</option><option>Marx</option>
      </select>
      <textarea id="iaResp" rows="7" placeholder="Escribe aquí tu respuesta completa (mínimo 20 palabras)…" style="width:100%;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);padding:0.85rem;font-family:var(--font-body);font-size:0.9rem;resize:vertical;outline:none;line-height:1.7;margin-bottom:1rem"></textarea>
      <button id="iaBtn" onclick="iaCorregir()" style="width:100%;padding:0.85rem;background:linear-gradient(135deg,var(--teal),#2a9d8f);color:#0d0f14;border:none;border-radius:var(--radius-sm);font-size:1rem;font-weight:800;cursor:pointer">🤖 Analizar con IA</button>
      <div id="iaResult" style="margin-top:1.25rem"></div>
    </div>
  </div>
</section>

<!-- COMPARADOR -->
<section id="comparador" style="background:var(--bg2)">
  <div class="container">
    <div class="section-label">Pregunta 2a</div>
    <h2 class="section-title">⚖️ Comparador de Autores</h2>
    <p class="section-sub">Genera una tabla comparativa al instante. Perfecta para preparar la pregunta 2a.</p>
    <div style="display:flex;gap:1rem;align-items:center;flex-wrap:wrap;margin-top:1.5rem;margin-bottom:1.5rem">
      <select id="comp1" style="flex:1;min-width:130px;padding:0.65rem 1rem;background:var(--card);border:2px solid #c9a84c;border-radius:var(--radius-sm);color:var(--text);font-family:var(--font-body);font-size:0.9rem;font-weight:600;outline:none">
        <option value="platon">Platón</option><option value="aristoteles">Aristóteles</option><option value="descartes">Descartes</option><option value="hume">Hume</option><option value="kant">Kant</option><option value="nietzsche">Nietzsche</option><option value="marx">Marx</option>
      </select>
      <span style="font-weight:700;color:var(--text3);font-size:1.25rem">VS</span>
      <select id="comp2" style="flex:1;min-width:130px;padding:0.65rem 1rem;background:var(--card);border:2px solid var(--teal);border-radius:var(--radius-sm);color:var(--text);font-family:var(--font-body);font-size:0.9rem;font-weight:600;outline:none">
        <option value="aristoteles">Aristóteles</option><option value="platon">Platón</option><option value="descartes">Descartes</option><option value="hume">Hume</option><option value="kant">Kant</option><option value="nietzsche">Nietzsche</option><option value="marx">Marx</option>
      </select>
      <button onclick="compGenerar()" style="padding:0.7rem 1.5rem;background:linear-gradient(135deg,#c9a84c,#a8732e);color:#0d0f14;border:none;border-radius:var(--radius-sm);font-weight:800;cursor:pointer">Comparar →</button>
    </div>
    <div id="compResult"></div>
  </div>
</section>

<!-- LOGROS -->
<section id="logros" style="background:var(--bg)">
  <div class="container">
    <div class="section-label">Gamificación</div>
    <h2 class="section-title">🏆 Logros y Nivel</h2>
    <p class="section-sub">Desbloquea logros estudiando. Cada acción te da XP.</p>
    <div style="background:var(--card);border:1px solid rgba(201,168,76,0.3);border-radius:var(--radius);padding:1.4rem;margin-top:1.5rem;margin-bottom:1.5rem;display:flex;align-items:center;gap:1.25rem;flex-wrap:wrap">
      <div style="width:64px;height:64px;border-radius:50%;background:var(--gold-dim);border:3px solid #c9a84c;display:flex;flex-direction:column;align-items:center;justify-content:center;flex-shrink:0">
        <div id="nivelNum" style="font-family:var(--font-mono);font-weight:900;font-size:1.4rem;color:#0d0f14;line-height:1">1</div>
        <div style="font-size:0.45rem;color:#0d0f14;font-weight:700;text-transform:uppercase">nivel</div>
      </div>
      <div style="flex:1;min-width:180px">
        <div style="display:flex;justify-content:space-between;margin-bottom:0.35rem">
          <strong id="nivelNombre" style="color:#c9a84c">Novato Filosófico</strong>
          <span id="nivelXP" style="font-size:0.78rem;color:var(--text3)">0 XP</span>
        </div>
        <div style="background:var(--bg3);border-radius:50px;height:7px;overflow:hidden">
          <div id="nivelBar" style="height:100%;background:linear-gradient(90deg,#c9a84c,#a8732e);border-radius:50px;width:0%;transition:width 1s ease"></div>
        </div>
        <div id="nivelProx" style="font-size:0.72rem;color:var(--text3);margin-top:0.3rem">Próximo: 50 XP</div>
      </div>
    </div>
    <div id="logrosGrid" style="display:grid;grid-template-columns:repeat(auto-fill,minmax(190px,1fr));gap:0.75rem"></div>
  </div>
</section>

<!-- COMUNIDAD -->
<section id="comunidad" style="background:var(--bg2)">
  <div class="container" style="max-width:680px">
    <div class="section-label">Entre estudiantes</div>
    <h2 class="section-title">🗣️ Comunidad FilosoFEANDO</h2>
    <p class="section-sub">Vota y ve qué piensan el resto de estudiantes.</p>
    <div id="comunidadGrid" style="display:grid;gap:1.1rem;margin-top:1.5rem"></div>
  </div>
</section>

<!-- CALCULADORA -->
<section id="calculadora" style="background:var(--bg)">
  <div class="container" style="max-width:580px">
    <div class="section-label">Herramienta</div>
    <h2 class="section-title">🧮 Calculadora de Nota PAU</h2>
    <p class="section-sub">Introduce tus puntuaciones y calcula tu nota al instante.</p>
    <div style="background:var(--card);border:1px solid var(--border);border-radius:20px;padding:1.75rem;margin-top:1.5rem">
      <div style="display:grid;grid-template-columns:1fr 1fr;gap:0.85rem;margin-bottom:1.25rem">
        <div><label style="display:block;font-size:0.73rem;font-weight:700;color:var(--text2);margin-bottom:0.35rem">1a · Definiciones (0–2)</label><input type="number" id="cn1a" min="0" max="2" step="0.25" value="0" oninput="calcNota()" style="width:100%;padding:0.6rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;text-align:center;outline:none"></div>
        <div><label style="display:block;font-size:0.73rem;font-weight:700;color:var(--text2);margin-bottom:0.35rem">1b · Idea principal (0–2)</label><input type="number" id="cn1b" min="0" max="2" step="0.25" value="0" oninput="calcNota()" style="width:100%;padding:0.6rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;text-align:center;outline:none"></div>
        <div><label style="display:block;font-size:0.73rem;font-weight:700;color:var(--text2);margin-bottom:0.35rem">1c · Posición (0–2)</label><input type="number" id="cn1c" min="0" max="2" step="0.25" value="0" oninput="calcNota()" style="width:100%;padding:0.6rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;text-align:center;outline:none"></div>
        <div><label style="display:block;font-size:0.73rem;font-weight:700;color:var(--text2);margin-bottom:0.35rem">2a · Relación autores (0–2)</label><input type="number" id="cn2a" min="0" max="2" step="0.25" value="0" oninput="calcNota()" style="width:100%;padding:0.6rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;text-align:center;outline:none"></div>
        <div style="grid-column:span 2"><label style="display:block;font-size:0.73rem;font-weight:700;color:var(--text2);margin-bottom:0.35rem">2b · Valoración (0–2)</label><input type="number" id="cn2b" min="0" max="2" step="0.25" value="0" oninput="calcNota()" style="width:100%;padding:0.6rem;background:var(--bg3);border:1px solid var(--border);border-radius:var(--radius-sm);color:var(--text);font-size:1rem;font-family:var(--font-mono);font-weight:700;text-align:center;outline:none"></div>
      </div>
      <div style="text-align:center;padding:1.25rem;background:var(--bg3);border-radius:var(--radius-sm)">
        <div id="cnFinal" style="font-size:3rem;font-weight:900;font-family:var(--font-mono);color:var(--text3)">0.00</div>
        <div id="cnLabel" style="font-size:0.85rem;color:var(--text3);margin-top:0.2rem">Introduce tus puntuaciones</div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-brand">📚 FilosoFEANDO</div>
  <p class="footer-sub">Plataforma educativa gratuita para la PAU de Filosofía · <span id="fechaFooter"></span><br>Adaptada al currículo de la Junta de Andalucía · Creada con ❤️ por un profesor de Bachillerato</p>
  <div class="footer-links">
    <a href="#pau-info">La PAU</a>
    <a href="#autores">Autores</a>
    <a href="#juegos">Juegos</a>
    <a href="#examenes">Exámenes</a>
    <a href="#podcasts">Podcasts</a>
    <a href="#libros">Libros</a>
    <a href="#sugerencias">💬 Sugerencias</a>
    <a href="#premium">Premium</a>
    <a href="https://www.tiktok.com/@filosofeando_para_aproba" target="_blank" rel="noopener" class="btn-tiktok" style="font-size:0.78rem;padding:0.35rem 0.85rem">TikTok</a>
    <a href="https://www.instagram.com/filosofeando_para_aprobar/" target="_blank" rel="noopener" class="btn-instagram" style="font-size:0.78rem;padding:0.35rem 0.85rem">Instagram</a>
    <a href="https://paypal.me/alvato" target="_blank" rel="noopener" class="btn-paypal" style="font-size:0.78rem;padding:0.35rem 0.85rem">Donar</a>
  </div>
</footer>

<script>
// ===== DATA AUTORES =====
const autoresData = [
  {id:'platon',nombre:'Platón',fechas:'427–347 a.C.',era:'Antigua',periodo:'antigua',desc:'Filósofo ateniense, discípulo de Sócrates. Fundador de la Academia y padre del idealismo filosófico occidental.',tags:['Idealismo','Metafísica','Política'],progreso:85,
   contexto:`<div class="content-block"><h4>Contexto Histórico-Filosófico</h4><p>Platón (427–347 a.C.) nace en Atenas durante el apogeo de la democracia ateniense. Testigo de la derrota en la Guerra del Peloponeso y, sobre todo, de la injusta condena y muerte de su maestro Sócrates (399 a.C.). Este hecho traumático marcará profundamente su pensamiento político y su desconfianza hacia la democracia. Fundó la Academia (388 a.C.), primera institución de educación superior de Occidente. Su pensamiento dialoga con los sofistas, los presocráticos y muy especialmente con el pitagorismo.</p></div>`,
   conocimiento:`<div class="content-block"><h4>Teoría del Conocimiento — La Línea Dividida</h4><ul><li><strong>Eikasía</strong> — Conjetura: sombras e imágenes. Nivel más bajo.</li><li><strong>Pistis</strong> — Creencia: objetos materiales percibidos.</li><li><strong>Dianoia</strong> — Pensamiento discursivo: matemáticas y geometría.</li><li><strong>Noesis</strong> — Intuición intelectual: contemplación directa de las Ideas. Nivel supremo.</li></ul></div><div class="content-block"><h4>El Mito de la Caverna</h4><p>Alegoría central de la República (Libro VII). Los prisioneros encadenados solo ven sombras (mundo sensible). El filósofo que asciende hacia la luz del sol (Bien supremo) alcanza el conocimiento verdadero y tiene el deber moral de regresar a gobernar.</p></div>`,
   realidad:`<div class="content-block"><h4>Teoría de las Ideas</h4><p>Dos mundos radicalmente distintos:</p></div><div class="concept-grid"><div class="concept-item"><div class="concept-term">Mundo Inteligible (topos noetos)</div><div class="concept-def">Mundo de las Ideas: eternas, inmutables, perfectas y universales. La Idea del Bien es la suprema que da ser y verdad a las demás.</div></div><div class="concept-item"><div class="concept-term">Mundo Sensible (topos horatos)</div><div class="concept-def">Mundo material percibido por los sentidos. Copia imperfecta y cambiante del mundo de las Ideas. Solo tiene ser derivado.</div></div></div>`,
   serhumano:`<div class="content-block"><h4>Dualismo Antropológico</h4><p>El ser humano es fundamentalmente su alma (psyche), prisionera en el cuerpo (soma sema: el cuerpo es tumba del alma). El alma preexiste al cuerpo y al encarnarse olvida las Ideas: el conocimiento es anamnesis (reminiscencia).</p></div><div class="content-block"><h4>Las tres partes del alma</h4><ul><li><strong>Alma racional (logistikon)</strong> — Inmortal; debe gobernar. Virtud: prudencia.</li><li><strong>Alma irascible (thymoeides)</strong> — Voluntad y valor. Virtud: fortaleza.</li><li><strong>Alma concupiscible (epithymetikon)</strong> — Deseos y apetitos. Virtud: templanza.</li></ul><p style="margin-top:0.6rem">La armonía de las tres bajo la razón produce la justicia en el individuo.</p></div>`,
   etica:`<div class="content-block"><h4>Ética Intelectualista y Política</h4><p>La ética platónica es intelectualista: el mal es ignorancia. El Estado ideal refleja la estructura del alma con tres clases: filósofos-reyes (prudencia), guardianes (fortaleza), productores (templanza). Critica la democracia por dar el poder a quienes no tienen conocimiento.</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Ideas (Eide)</div><div class="concept-def">Esencias eternas, inmutables, perfectas. Verdadera realidad. Arquetipos de las cosas sensibles.</div></div><div class="concept-item"><div class="concept-term">Anamnesis</div><div class="concept-def">Reminiscencia. El conocimiento como recuperación de lo que el alma vio antes de encarnarse.</div></div><div class="concept-item"><div class="concept-term">Demiurgo</div><div class="concept-def">Artesano divino que crea el mundo sensible imitando las Ideas eternas como modelo.</div></div><div class="concept-item"><div class="concept-term">Dialéctica</div><div class="concept-def">Método filosófico de ascenso desde las hipótesis hacia el Bien. Conocimiento más alto posible.</div></div><div class="concept-item"><div class="concept-term">Episteme / Doxa</div><div class="concept-def">Episteme: conocimiento verdadero de las Ideas. Doxa: opinión sobre el mundo sensible, no ciencia.</div></div><div class="concept-item"><div class="concept-term">Eros filosófico</div><div class="concept-def">Impulso amoroso que eleva el alma desde los cuerpos bellos hacia la Belleza en sí.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Platón</h4><p><strong>Ontología:</strong> Dos mundos: inteligible (Ideas eternas, verdaderas) y sensible (copia imperfecta). Idea del Bien como fundamento.</p><p style="margin-top:0.6rem"><strong>Gnoseología:</strong> Conocimiento verdadero (episteme) sobre Ideas. La alegoría de la caverna ilustra el ascenso filosófico. Anamnesis como mecanismo del conocimiento.</p><p style="margin-top:0.6rem"><strong>Antropología:</strong> Dualismo alma-cuerpo. Tres partes del alma. Virtud como armonía bajo la razón.</p><p style="margin-top:0.6rem"><strong>Ética y Política:</strong> Intelectualismo moral. Estado ideal con tres clases. Filósofos-reyes como gobernantes.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas Tipo PAU — Platón</h4></div><div class="banco-item" style="cursor:default;margin-bottom:0.65rem"><div class="banco-q">Define los términos <em>Idea</em> y <em>caverna</em> en el pensamiento de Platón. [PAU 2019]</div></div><div class="banco-item" style="cursor:default;margin-bottom:0.65rem"><div class="banco-q">Expón la teoría del conocimiento de Platón haciendo referencia a la alegoría de la caverna. [PAU 2018]</div></div><div class="banco-item" style="cursor:default"><div class="banco-q">Valora críticamente el planteamiento político de Platón en <em>La República</em> en relación con los valores democráticos actuales.</div></div>`,
   comentario:`<div class="content-block"><h4>Comentario de Texto Resuelto</h4><div style="background:var(--bg3);border-radius:8px;padding:0.9rem;margin-bottom:0.9rem;font-style:italic;font-size:0.85rem;color:var(--text2)">"Y si, después de contemplar el sol, volviera a la caverna y se sentase en el mismo lugar, tendría los ojos llenos de oscuridad." (República, 516e)</div><p style="font-size:0.85rem;color:var(--text2);margin-bottom:0.65rem"><strong style="color:var(--teal)">1a.</strong> <em>Sol</em>: simboliza la Idea del Bien, principio supremo del mundo inteligible. <em>Caverna</em>: el mundo sensible y la condición de ignorancia natural del ser humano.</p><p style="font-size:0.85rem;color:var(--text2);margin-bottom:0.65rem"><strong style="color:var(--teal)">1b.</strong> Contraste entre luz del conocimiento filosófico y oscuridad de la ignorancia. El filósofo que regresa experimenta desorientación: anticipa el deber del filósofo-rey.</p><p style="font-size:0.85rem;color:var(--text2)"><strong style="color:var(--teal)">1c.</strong> Enmarcado en la teoría de los dos mundos: caverna = doxa, sol = episteme. El ascenso es el proceso dialéctico hacia el Bien. El regreso conecta con la filosofía política: quien conoce el Bien debe gobernar.</p></div>`
  },
  {id:'aristoteles',nombre:'Aristóteles',fechas:'384–322 a.C.',era:'Antigua',periodo:'antigua',desc:'Discípulo de Platón y fundador del Liceo. El más enciclopédico de los filósofos griegos.',tags:['Metafísica','Empirismo','Ética'],progreso:60,
   contexto:`<div class="content-block"><h4>Contexto</h4><p>Aristóteles (384–322 a.C.) nace en Estagira. A los 17 años ingresa en la Academia de Platón donde permanece 20 años. Funda el Liceo en Atenas y es tutor de Alejandro Magno. Su pensamiento supone una crítica y superación del idealismo platónico desde dentro.</p></div>`,
   conocimiento:`<div class="content-block"><h4>Empirismo Aristotélico</h4><p>A diferencia de Platón, Aristóteles parte de la experiencia sensible. El conocimiento asciende desde los sentidos, por la memoria y experiencia, hasta el arte y la ciencia. Los universales no existen separados: están en las cosas y el entendimiento los abstrae.</p></div><div class="content-block"><h4>Lógica y Silogismo</h4><p>Aristóteles inventa la lógica formal. El silogismo es el razonamiento deductivo perfecto: de dos premisas se extrae necesariamente una conclusión.</p></div>`,
   realidad:`<div class="content-block"><h4>Crítica a Platón e Hilemorfismo</h4><p>Los universales no existen separados. La verdadera realidad es la sustancia individual concreta.</p></div><div class="concept-grid"><div class="concept-item"><div class="concept-term">Hilemorfismo</div><div class="concept-def">Toda sustancia está compuesta de materia (hyle) y forma (morphe). La forma es el principio activo; la materia es el substrato potencial.</div></div><div class="concept-item"><div class="concept-term">Acto y Potencia</div><div class="concept-def">Potencia: capacidad de ser algo. Acto: realización efectiva. El cambio es el paso de potencia a acto.</div></div><div class="concept-item"><div class="concept-term">Las Cuatro Causas</div><div class="concept-def">Material, formal, eficiente y final. La causa final (télos) es la más importante: todo tiende hacia su fin natural.</div></div><div class="concept-item"><div class="concept-term">Motor Inmóvil</div><div class="concept-def">Primer Motor que mueve sin ser movido. Acto puro sin potencia. Fundamento último del movimiento del cosmos.</div></div></div>`,
   serhumano:`<div class="content-block"><h4>Unidad Alma-Cuerpo</h4><p>Frente al dualismo platónico, Aristóteles defiende la unidad del ser humano. El alma es la forma del cuerpo, su principio vital. El ser humano es un animal racional y político por naturaleza (zoon politikon).</p></div>`,
   etica:`<div class="content-block"><h4>Ética de la Eudaimonia</h4><p>El fin último es la felicidad (eudaimonia): actividad del alma según la virtud. La virtud ética es un hábito adquirido que consiste en el término medio entre el exceso y el defecto. La prudencia (fronesis) nos permite encontrarlo.</p></div><div class="content-block"><h4>Política</h4><p>El ser humano es animal político por naturaleza. La polis es anterior al individuo. Clasifica los regímenes en rectos (monarquía, aristocracia, politeia) y desviados (tiranía, oligarquía, democracia). La politeia es el mejor régimen práctico.</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Sustancia (ousia)</div><div class="concept-def">Lo que existe por sí mismo. La sustancia individual concreta es la realidad primaria.</div></div><div class="concept-item"><div class="concept-term">Eudaimonia</div><div class="concept-def">Felicidad o florecimiento humano. Fin último de la vida. Actividad del alma conforme a la virtud.</div></div><div class="concept-item"><div class="concept-term">Fronesis</div><div class="concept-def">Prudencia. Virtud intelectual práctica para deliberar correctamente sobre el bien.</div></div><div class="concept-item"><div class="concept-term">Télos</div><div class="concept-def">Fin o finalidad. Todo ente natural tiene un fin hacia el que tiende por su propia naturaleza.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Aristóteles</h4><p>Critica la separación platónica de las Ideas. La verdadera realidad es la sustancia individual. Hilemorfismo (materia-forma), acto-potencia y cuatro causas explican la realidad y el cambio. Empirismo: conocimiento desde la experiencia sensible. Ética eudaimonista: virtud como término medio. Ser humano como animal político; polis como comunidad natural.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas PAU — Aristóteles</h4></div><div class="banco-item" style="cursor:default;margin-bottom:0.65rem"><div class="banco-q">Define <em>eudaimonia</em> y <em>virtud</em> en Aristóteles.</div></div><div class="banco-item" style="cursor:default"><div class="banco-q">Explica la crítica de Aristóteles a la teoría de las Ideas de Platón. [PAU 2021]</div></div>`,
   comentario:`<div class="content-block"><h4>Orientación — Aristóteles</h4><p style="font-size:0.875rem;color:var(--text2)">Aplica el mismo esquema: define términos técnicos (ousia, eudaimonia, polis...), expón la idea central relacionándola con su metafísica o ética, y relaciona con Platón como contraste.</p></div>`
  },
  {id:'descartes',nombre:'René Descartes',fechas:'1596–1650',era:'Moderna',periodo:'moderna',desc:'Padre del racionalismo moderno. El cogito y la duda metódica inauguran la filosofía moderna.',tags:['Racionalismo','Método','Dualismo'],progreso:40,
   contexto:`<div class="content-block"><h4>Contexto: La Revolución Científica</h4><p>Descartes (1596–1650) vive en plena Revolución Científica. Quiere construir una filosofía tan sólida como las matemáticas, capaz de fundamentar la nueva ciencia. Su método racionalista buscaba certezas absolutas frente al escepticismo pirrónico y el relativismo renacentista.</p></div>`,
   conocimiento:`<div class="content-block"><h4>Duda Metódica y Cogito</h4><p>Aplica la duda metódica: duda de todo lo que admita la menor posibilidad de ser falso (sentidos, mundo, matemáticas mediante el «genio maligno»). Al dudar de todo, descubre que no puede dudar de que está pensando: <em>cogito ergo sum</em> («pienso, luego existo»). Primera verdad indubitada.</p></div>`,
   realidad:`<div class="content-block"><h4>Tres Sustancias</h4><p>A partir del cogito demuestra la existencia de Dios y el mundo exterior. Establece tres sustancias: <strong>res cogitans</strong> (sustancia pensante: el yo), <strong>res extensa</strong> (sustancia extensa: los cuerpos) y <strong>Dios</strong> (sustancia infinita).</p></div>`,
   serhumano:`<div class="content-block"><h4>Dualismo Cartesiano</h4><p>El ser humano es la unión problemática de res cogitans y res extensa. Interactúan a través de la glándula pineal. Este dualismo radical genera el «problema mente-cuerpo» que intentarán resolver Malebranche, Spinoza y Leibniz.</p></div>`,
   etica:`<div class="content-block"><h4>Moral Provisional</h4><p>Propone una «moral provisional» para vivir mientras elabora su filosofía definitiva. Su ética aspira al dominio de las pasiones mediante la razón. En el Tratado de las pasiones elabora una psicología de las emociones.</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Cogito ergo sum</div><div class="concept-def">«Pienso, luego existo». Primera verdad indubitada. El acto de pensar prueba la existencia del yo pensante.</div></div><div class="concept-item"><div class="concept-term">Duda metódica</div><div class="concept-def">Procedimiento de dudar de todo lo que admite la menor duda para encontrar verdades absolutamente ciertas.</div></div><div class="concept-item"><div class="concept-term">Res cogitans / extensa</div><div class="concept-def">Sustancia pensante (mente) y sustancia extensa (cuerpo). Dualismo radical cartesiano.</div></div><div class="concept-item"><div class="concept-term">Ideas innatas</div><div class="concept-def">Ideas impresas en el alma sin provenir de la experiencia: Dios, yo, extensión. Base del racionalismo.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Descartes</h4><p>Inicia la filosofía moderna con el método de la duda. El cogito es la primera certeza. Demuestra a Dios y el mundo. Dualismo res cogitans / res extensa. Las ideas innatas son el fundamento del conocimiento racional. Funda el racionalismo: la razón, no los sentidos, es la fuente del conocimiento verdadero.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas PAU — Descartes</h4></div><div class="banco-item" style="cursor:default"><div class="banco-q">Define <em>cogito</em> y <em>duda metódica</em>. Expón el método cartesiano y sus reglas.</div></div>`,
   comentario:`<div class="content-block"><h4>Orientación — Descartes</h4><p style="font-size:0.875rem;color:var(--text2)">Textos frecuentes: Meditaciones Metafísicas o Discurso del Método. Localiza el cogito, la duda, las sustancias y la demostración de Dios. Relaciona con Hume (empirismo como crítica al racionalismo) o con Kant (síntesis).</p></div>`
  },
  {id:'hume',nombre:'David Hume',fechas:'1711–1776',era:'Moderna',periodo:'moderna',desc:'Máximo exponente del empirismo moderno y del escepticismo. Crítico radical del racionalismo y la metafísica.',tags:['Empirismo','Escepticismo','Causalidad'],progreso:55,
   contexto:`<div class="content-block"><h4>Contexto: La Ilustración Escocesa</h4><p>Hume (1711–1776) es el gran filósofo escocés de la Ilustración. Su pensamiento supone la radicalización del empirismo de Locke y Berkeley hasta posiciones escépticas que «despertaron a Kant de su sueño dogmático».</p></div>`,
   conocimiento:`<div class="content-block"><h4>Impresiones e Ideas</h4><p>Todo conocimiento deriva de la experiencia. Los contenidos mentales son: <strong>impresiones</strong> (percepciones directas, vivas) e <strong>ideas</strong> (copias debilitadas). No hay ideas innatas. Si una idea no puede rastrearse hasta una impresión, carece de significado.</p></div><div class="content-block"><h4>Crítica a la Causalidad</h4><p>La relación causa-efecto no se percibe: solo vemos conjunción constante de fenómenos. La idea de necesidad causal es una creencia (belief) fruto del hábito, no del razonamiento. Esta crítica impactó profundamente a Kant.</p></div>`,
   realidad:`<div class="content-block"><h4>Escepticismo</h4><p>No podemos conocer la sustancia, el yo como entidad permanente, ni la existencia de Dios mediante la razón. El yo no es más que un haz de percepciones sin sujeto permanente (bundle theory).</p></div>`,
   serhumano:`<div class="content-block"><h4>Bundle Theory del Yo</h4><p>No hay un yo sustancial: cuando introspeccionamos solo encontramos percepciones cambiantes. El yo es solo un haz o colección de percepciones.</p></div>`,
   etica:`<div class="content-block"><h4>Ética del Sentimiento</h4><p>La razón es esclava de las pasiones. Los juicios morales son expresiones de sentimientos de aprobación o desaprobación, no juicios racionales. La simpatía (sympathy) es el fundamento del juicio moral.</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Impresiones</div><div class="concept-def">Percepciones directas, vivas e inmediatas. Origen de todo conocimiento.</div></div><div class="concept-item"><div class="concept-term">Ideas</div><div class="concept-def">Copias debilitadas de las impresiones. Solo son válidas si se rastrean hasta una impresión.</div></div><div class="concept-item"><div class="concept-term">Conjunción constante</div><div class="concept-def">Lo que realmente observamos: A siempre seguido de B. No vemos necesidad causal, solo regularidad.</div></div><div class="concept-item"><div class="concept-term">Creencia (Belief)</div><div class="concept-def">La idea de causalidad formada por el hábito de observar conjunciones constantes, no razonamiento.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Hume</h4><p>Radicaliza el empirismo: todo conocimiento proviene de la experiencia (impresiones). No hay ideas innatas. Crítica a la causalidad: solo vemos conjunción constante. El yo es un haz de percepciones. La metafísica, teología y yo sustancial carecen de fundamento empírico. La moral se basa en el sentimiento, no en la razón.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas PAU — Hume</h4></div><div class="banco-item" style="cursor:default"><div class="banco-q">Explica la crítica de Hume al concepto de causalidad y sus consecuencias para la metafísica.</div></div>`,
   comentario:`<div class="content-block"><h4>Orientación — Hume</h4><p style="font-size:0.875rem;color:var(--text2)">Busca siempre: impresiones/ideas, crítica a la causalidad, escepticismo sobre el yo y Dios. Relaciona con Descartes (racionalismo vs empirismo) y con Kant (quien intenta superar el escepticismo humeano).</p></div>`
  },
  {id:'kant',nombre:'Immanuel Kant',fechas:'1724–1804',era:'Moderna',periodo:'moderna',desc:'El mayor filósofo de la Modernidad. Sintetizó racionalismo y empirismo, fundó la ética deontológica y el liberalismo político.',tags:['Criticismo','Imperativo','Ilustración'],progreso:70,
   contexto:`<div class="content-block"><h4>Contexto: La Ilustración Alemana</h4><p>Kant (1724–1804) es el filósofo de la Ilustración por excelencia. Su filosofía crítica responde tanto al dogmatismo racionalista (Descartes, Leibniz) como al escepticismo empirista (Hume). Sapere aude: «Atrévete a saber» es el lema ilustrado que él define.</p></div>`,
   conocimiento:`<div class="content-block"><h4>El Giro Copernicano</h4><p>No el conocimiento se adapta a los objetos, sino los objetos se adaptan a las formas del sujeto. La síntesis de intuiciones (sensibilidad: espacio y tiempo a priori) y conceptos (entendimiento: 12 categorías a priori) produce el conocimiento científico.</p></div>`,
   realidad:`<div class="content-block"><h4>Fenómeno y Noúmeno</h4><p>Conocemos los fenómenos (las cosas tal como se nos aparecen, filtradas por nuestras formas a priori), no los noúmenos (la cosa en sí). La metafísica tradicional fracasa porque pretende conocer más allá de la experiencia posible.</p></div>`,
   serhumano:`<div class="content-block"><h4>El Ser Humano como Fin en sí mismo</h4><p>El ser humano es racional y autónomo. Como ser racional pertenece al mundo inteligible de la libertad; como ser sensible al mundo natural. La dignidad humana consiste en ser fin en sí mismo y nunca solo medio.</p></div>`,
   etica:`<div class="content-block"><h4>El Imperativo Categórico</h4><ul><li><strong>Universal:</strong> «Obra solo según la máxima que puedas querer que sea ley universal»</li><li><strong>Humanidad:</strong> «Trata la humanidad siempre como fin, nunca solo como medio»</li><li><strong>Autonomía:</strong> «Obra como si fueras legislador en el reino de los fines»</li></ul></div><div class="content-block"><h4>La Paz Perpetua</h4><p>Defiende una federación de estados republicanos como condición para la paz duradera. Funda el cosmopolitismo moderno y el liberalismo político.</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Imperativo categórico</div><div class="concept-def">Mandato moral incondicional y universal de la razón práctica. Opuesto al imperativo hipotético.</div></div><div class="concept-item"><div class="concept-term">A priori / A posteriori</div><div class="concept-def">A priori: independiente de la experiencia. A posteriori: derivado de ella. Los juicios sintéticos a priori son la clave de la ciencia.</div></div><div class="concept-item"><div class="concept-term">Autonomía</div><div class="concept-def">Capacidad de la voluntad racional de darse a sí misma la ley moral. Fundamento de la dignidad humana.</div></div><div class="concept-item"><div class="concept-term">Noúmeno / Fenómeno</div><div class="concept-def">Fenómeno: la cosa tal como se nos aparece. Noúmeno: la cosa en sí, incognoscible para nuestra razón teórica.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Kant</h4><p>Sintetiza racionalismo y empirismo. Giro copernicano: el sujeto impone sus formas al objeto. Solo conocemos fenómenos, no noúmenos. La metafísica no es ciencia. El imperativo categórico es la ley moral universal e incondicional. El ser humano es autónomo y fin en sí mismo. Política: federación de repúblicas para la paz perpetua.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas PAU — Kant</h4></div><div class="banco-item" style="cursor:default;margin-bottom:0.65rem"><div class="banco-q">Explica el imperativo categórico de Kant. ¿En qué se diferencia del hipotético? [PAU 2023]</div></div><div class="banco-item" style="cursor:default"><div class="banco-q">Explica la distinción fenómeno / noúmeno y sus consecuencias para la metafísica.</div></div>`,
   comentario:`<div class="content-block"><h4>Orientación — Kant</h4><p style="font-size:0.875rem;color:var(--text2)">Identifica si el texto pertenece a la Crítica de la Razón Pura (gnoseología) o a la Fundamentación de la Metafísica de las Costumbres (ética). Busca palabras clave: a priori, imperativo, autonomía, fenómeno, noúmeno.</p></div>`
  },
  {id:'nietzsche',nombre:'Friedrich Nietzsche',fechas:'1844–1900',era:'Contemporánea',periodo:'contemporanea',desc:'Filósofo vitalista. Proclamó la muerte de Dios, el nihilismo y la voluntad de poder como filosofía de la vida.',tags:['Vitalismo','Nihilismo','Crítica'],progreso:45,
   contexto:`<div class="content-block"><h4>Contexto: Crisis de la Modernidad</h4><p>Nietzsche (1844–1900) vive en la segunda mitad del siglo XIX. Su filosofía es una crítica radical de toda la tradición occidental: Platón, el cristianismo y Kant. Se lo considera precursor de la posmodernidad.</p></div>`,
   conocimiento:`<div class="content-block"><h4>Perspectivismo</h4><p>No existe la verdad objetiva: toda verdad es una perspectiva, una interpretación desde un punto de vista vital. Los conceptos son metáforas que hemos olvidado que son metáforas. La ciencia y la metafísica son ficciones útiles, no verdades absolutas.</p></div>`,
   realidad:`<div class="content-block"><h4>Voluntad de Poder y Eterno Retorno</h4><p>La realidad es <strong>voluntad de poder</strong> (Wille zur Macht): impulso de vida, creatividad y superación. El <strong>eterno retorno</strong> es la idea de que todo vuelve a repetirse infinitamente: el gran experimento ético que pregunta si vivirías tu vida igual.</p></div>`,
   serhumano:`<div class="content-block"><h4>El Superhombre (Übermensch)</h4><p>El superhombre supera la moral del rebaño, crea sus propios valores más allá del bien y del mal, dice sí a la vida. No es el dominador: es el creador de nuevos valores tras la muerte de Dios.</p></div>`,
   etica:`<div class="content-block"><h4>Muerte de Dios y Transvaloración</h4><p>«Dios ha muerto»: colapso de los valores absolutos trascendentes. La moral cristiana es moral de esclavos (resentimiento). Nietzsche propone la <strong>transvaloración de todos los valores</strong>: reemplazar los valores nihilistas por valores vitales afirmativos. El amor fati es la actitud del superhombre ante la vida.</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Voluntad de poder</div><div class="concept-def">Principio fundamental de la vida: impulso creativo hacia el crecimiento y la superación, no hacia el dominio.</div></div><div class="concept-item"><div class="concept-term">Nihilismo</div><div class="concept-def">Los valores supremos se desvalorizan. Consecuencia de la muerte de Dios. Nietzsche quiere superarlo.</div></div><div class="concept-item"><div class="concept-term">Übermensch</div><div class="concept-def">Superhombre: ideal que crea sus propios valores, supera el nihilismo y dice sí a la vida con amor fati.</div></div><div class="concept-item"><div class="concept-term">Amor fati</div><div class="concept-def">Amor al destino: aceptación y amor de todo lo que ocurre, incluyendo el sufrimiento, sin resentimiento.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Nietzsche</h4><p>Critica toda la filosofía occidental como negación de la vida. «Dios ha muerto»: colapso de los valores absolutos. El nihilismo es la enfermedad de la modernidad. Voluntad de poder como principio vital creador. El superhombre crea nuevos valores. El eterno retorno es el gran experimento ético de la afirmación de la vida.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas PAU — Nietzsche</h4></div><div class="banco-item" style="cursor:default"><div class="banco-q">Explica qué significa «la muerte de Dios» en Nietzsche y sus consecuencias filosóficas. [PAU 2022]</div></div>`,
   comentario:`<div class="content-block"><h4>Orientación — Nietzsche</h4><p style="font-size:0.875rem;color:var(--text2)">Textos frecuentes: Así habló Zaratustra, Más allá del bien y del mal, La Gaya Ciencia. Busca: voluntad de poder, nihilismo, moral de esclavos/señores, transvaloración. Relaciona con Platón (crítica al mundo de los valores absolutos) o Marx.</p></div>`
  },
  {id:'marx',nombre:'Karl Marx',fechas:'1818–1883',era:'Contemporánea',periodo:'contemporanea',desc:'Filósofo, economista y revolucionario. Creador del materialismo histórico y la crítica al capitalismo.',tags:['Materialismo','Alienación','Revolución'],progreso:30,
   contexto:`<div class="content-block"><h4>Contexto: La Revolución Industrial</h4><p>Marx (1818–1883) vive en plena Revolución Industrial. Las condiciones de vida del proletariado son miserables. Su pensamiento dialoga críticamente con Hegel (invierte la dialéctica idealista), con los economistas clásicos (Smith, Ricardo) y con el socialismo utópico.</p></div>`,
   conocimiento:`<div class="content-block"><h4>Materialismo y Praxis</h4><p>«Los filósofos solo han interpretado el mundo de distintas maneras; de lo que se trata es de transformarlo» (Tesis sobre Feuerbach, XI). El conocimiento no es contemplativo sino práctico: la praxis (actividad transformadora) es el criterio de verdad.</p></div>`,
   realidad:`<div class="content-block"><h4>Materialismo Histórico</h4><p>Son las condiciones materiales de producción (infraestructura económica) las que determinan la superestructura ideológica, jurídica y política. La historia es la historia de la lucha de clases: cada modo de producción genera sus clases antagónicas.</p></div>`,
   serhumano:`<div class="content-block"><h4>Alienación</h4><p>El ser humano es esencialmente un ser productor (homo faber). En el capitalismo, el trabajador se aliena: se separa del producto de su trabajo, del proceso productivo, de su esencia genérica y de otros seres humanos. La revolución debe superar la alienación.</p></div>`,
   etica:`<div class="content-block"><h4>Crítica al Capitalismo y Comunismo</h4><p>La burguesía explota al proletariado apropiándose de la plusvalía (el valor generado por el trabajo no remunerado). El comunismo como sociedad sin clases superará la alienación y permitirá el pleno desarrollo humano: «De cada cual según sus capacidades, a cada cual según sus necesidades».</p></div>`,
   conceptos:`<div class="concept-grid"><div class="concept-item"><div class="concept-term">Alienación</div><div class="concept-def">Proceso por el que el trabajador se separa del producto de su trabajo, perdiendo su esencia humana creadora.</div></div><div class="concept-item"><div class="concept-term">Infraestructura</div><div class="concept-def">Base económica: fuerzas y relaciones de producción. Determina la superestructura ideológica y política.</div></div><div class="concept-item"><div class="concept-term">Plusvalía</div><div class="concept-def">Valor generado por el trabajador que se apropia el capitalista. Fundamento de la explotación.</div></div><div class="concept-item"><div class="concept-term">Praxis</div><div class="concept-def">Actividad práctica transformadora. El criterio de verdad y el fin de la filosofía marxista.</div></div></div>`,
   resumen:`<div class="content-block"><h4>📄 Resumen — Marx</h4><p>Invierte la dialéctica hegeliana: no el Espíritu sino la materia mueve la historia. Materialismo histórico: la economía determina la política y la ideología. La historia es lucha de clases. El capitalismo aliena al trabajador y genera plusvalía. La revolución proletaria conducirá al comunismo: sociedad sin clases que supera la alienación.</p></div>`,
   pau:`<div class="content-block"><h4>Preguntas PAU — Marx</h4></div><div class="banco-item" style="cursor:default"><div class="banco-q">Explica el concepto de alienación en Marx y su relación con el capitalismo.</div></div>`,
   comentario:`<div class="content-block"><h4>Orientación — Marx</h4><p style="font-size:0.875rem;color:var(--text2)">Textos frecuentes: Manuscritos Económico-Filosóficos, La Ideología Alemana, El Capital. Busca: alienación, plusvalía, lucha de clases, infraestructura/superestructura. Relaciona con Hegel (materialismo vs idealismo) o Nietzsche (crítica social desde ángulos distintos).</p></div>`
  }
];

// ===== FLASHCARDS =====
const flashcardsData = [
  {q:"¿Qué es la teoría de las Ideas de Platón?",a:"Las Ideas son esencias eternas, inmutables y perfectas que constituyen la verdadera realidad. El mundo sensible es copia imperfecta del mundo inteligible. El Bien es la Idea suprema."},
  {q:"¿Qué es el Mito de la Caverna?",a:"Alegoría platónica del ascenso del conocimiento. Prisioneros ven sombras (doxa). El filósofo que sale al sol (noesis) contempla el Bien y debe regresar a gobernar."},
  {q:"¿Qué es el cogito cartesiano?",a:"'Pienso, luego existo' (cogito ergo sum). Al dudar, piensa; al pensar, existe. Primera certeza indubitable y fundamento de la filosofía de Descartes."},
  {q:"¿Qué es el imperativo categórico de Kant?",a:"Mandato moral incondicional y universal: 'Obra solo según la máxima que puedas querer que se convierta en ley universal'. No depende de fines ni consecuencias."},
  {q:"¿Qué crítica hace Hume a la causalidad?",a:"No percibimos la necesidad causal: solo vemos conjunción constante de eventos. La idea de causa es una creencia fruto del hábito, no del razonamiento racional."},
  {q:"¿Qué es la voluntad de poder en Nietzsche?",a:"Principio fundamental de la vida: impulso creativo hacia el crecimiento y la superación. No es voluntad de dominar sino de crear y autoafirmarse vitalmente."},
  {q:"¿Qué diferencia hay entre fenómeno y noúmeno en Kant?",a:"Fenómeno: la cosa tal como se nos aparece, filtrada por nuestras formas a priori. Noúmeno: la cosa en sí, tal como es en sí misma, incognoscible para nosotros."},
  {q:"¿Qué es la anamnesis platónica?",a:"Teoría del conocimiento como reminiscencia. El alma, antes de encarnarse, contempló las Ideas. El aprendizaje es recuperar ese conocimiento olvidado al encarnarse."},
  {q:"¿Qué es la eudaimonia aristotélica?",a:"La felicidad o florecimiento humano: el fin último de la vida. Consiste en la actividad del alma conforme a la virtud más excelente a lo largo de una vida completa."},
  {q:"¿Qué es el hilemorfismo de Aristóteles?",a:"Toda sustancia está compuesta de materia (hyle: substrato potencial) y forma (morphe: principio activo que determina qué es la cosa). La forma es la esencia."},
  {q:"¿Qué es la alienación en Marx?",a:"El trabajador se separa del producto de su trabajo, del proceso productivo, de su esencia genérica y de otros seres humanos. El capitalismo produce esta separación sistemáticamente."},
  {q:"¿Qué es el giro copernicano de Kant?",a:"Revolución epistemológica: no el conocimiento se adapta a los objetos, sino los objetos se adaptan a las formas del sujeto. El sujeto construye activamente el conocimiento."},
  {q:"¿Qué significa 'la muerte de Dios' en Nietzsche?",a:"No es ateísmo sino el diagnóstico de que la cultura occidental ya no puede apoyarse en los valores absolutos trascendentes. El nihilismo es la consecuencia."},
  {q:"¿Qué es el materialismo histórico de Marx?",a:"Las condiciones materiales de producción (infraestructura económica) determinan la superestructura ideológica, jurídica y política. La historia es historia de la lucha de clases."},
  {q:"¿Qué son las impresiones e ideas en Hume?",a:"Impresiones: percepciones directas, vivas e inmediatas. Ideas: copias debilitadas de las impresiones. Todo conocimiento debe rastrearse hasta una impresión original."},
  {q:"¿Qué es el Übermensch nietzscheano?",a:"El superhombre: ideal del ser humano que supera la moral del rebaño, crea sus propios valores tras la muerte de Dios y dice sí a la vida con amor fati."},
  {q:"¿Qué es la virtud como término medio en Aristóteles?",a:"La virtud ética es el hábito de elegir el término medio entre el exceso y el defecto. Ej: el valor es el medio entre temeridad y cobardía."},
  {q:"¿Qué es la autonomía moral en Kant?",a:"La capacidad de la voluntad racional de darse a sí misma la ley moral, sin depender de factores externos. Fundamento de la dignidad humana y la libertad."},
  {q:"¿Qué es la plusvalía en Marx?",a:"Valor generado por el trabajador que el capitalista se apropia sin remunerar. Es el fundamento de la explotación capitalista y la fuente de acumulación del capital."},
  {q:"¿Qué es la dialéctica platónica?",a:"Método filosófico supremo de ascenso desde las hipótesis hacia el principio incondicionado (el Bien). El método propio del filósofo y el nivel más alto de conocimiento."}
];

// ===== QUIZ =====
const quizData = [
  {q:"Según Platón, ¿cuál es el nivel más alto de conocimiento en la teoría de la línea dividida?",opts:["Pistis (creencia)","Eikasía (conjetura)","Noesis (intuición intelectual)","Dianoia (pensamiento discursivo)"],correct:2,exp:"La noesis es la intuición directa de las Ideas y del Bien. Es el conocimiento filosófico supremo del filósofo-rey."},
  {q:"¿Qué primera certeza descubrió Descartes tras aplicar la duda metódica?",opts:["La existencia de Dios","La existencia del mundo exterior","Cogito ergo sum: 'Pienso, luego existo'","La inmortalidad del alma"],correct:2,exp:"Al dudar de todo, Descartes descubrió que no podía dudar de que estaba pensando. Este acto de pensar prueba su existencia."},
  {q:"Según Kant, ¿cuál describe correctamente el imperativo categórico?",opts:["Si quieres ser feliz, obra moralmente","Maximiza el bienestar general","Obra solo según la máxima que puedas querer que sea ley universal","Las consecuencias determinan el valor moral"],correct:2,exp:"El imperativo categórico es incondicional (no depende de fines) y universal. Es la ley moral racional para todos los seres racionales."},
  {q:"¿Qué crítica fundamental hace Hume al concepto de causalidad?",opts:["La causalidad es una Idea innata de la razón","Solo percibimos conjunción constante, no necesidad causal","Es una categoría a priori del entendimiento","La causa es siempre anterior al efecto"],correct:1,exp:"Hume muestra que jamás percibimos la 'fuerza' que une causa y efecto. Solo vemos que A siempre ha sido seguido de B."},
  {q:"¿Qué concepto usa Marx para describir la separación del trabajador de su trabajo?",opts:["Plusvalía","Praxis","Alienación","Infraestructura"],correct:2,exp:"La alienación describe cómo el trabajador capitalista se separa del producto de su trabajo, del proceso productivo y de su esencia humana creadora."},
  {q:"¿Qué es el hilemorfismo aristotélico?",opts:["La teoría de que solo existe la materia","La doctrina de que toda sustancia tiene materia y forma","La idea de que las Ideas son la verdadera realidad","La teoría del conocimiento empírico"],correct:1,exp:"El hilemorfismo sostiene que toda sustancia está compuesta de materia (potencia) y forma (acto), que son principios inseparables en la realidad concreta."}
];

// ===== JUEGO: ¿QUIÉN SOY? =====
const quienSoyData = [
  {filosofo:"Platón",pistas:["Nací en Atenas en el siglo V a.C.","Fui discípulo de Sócrates y maestro de Aristóteles","Fundé una famosa institución filosófica llamada la Academia","Escribí sobre una alegoría con prisioneros en una caverna"]},
  {filosofo:"Aristóteles",pistas:["Fui discípulo de Platón pero critiqué sus Ideas separadas","Fui tutor del hijo de Filipo II de Macedonia","Fundé el Liceo en Atenas","Inventé la lógica formal y el silogismo"]},
  {filosofo:"Descartes",pistas:["Soy conocido por una frase que comienza con 'Pienso...'","Dudo de todo metodicamente para encontrar una certeza","Dividí la realidad en dos sustancias radicalmente distintas","Soy considerado el padre de la filosofía moderna"]},
  {filosofo:"Kant",pistas:["Realicé un 'giro copernicano' en la filosofía","Formulé un imperativo que no admite excepciones","Hume me despertó de mi sueño dogmático","Nací y morí en Königsberg sin salir apenas de la ciudad"]},
  {filosofo:"Nietzsche",pistas:["Proclamé que Dios ha muerto en un famoso parágrafo","Propuse al superhombre como ideal filosófico","Critiqué la moral cristiana como moral de esclavos","El eterno retorno es uno de mis conceptos más enigmáticos"]},
  {filosofo:"Marx",pistas:["Junto con Engels escribí un célebre manifiesto","Analicé cómo el capitalista se apropia de la plusvalía","La historia para mí es la historia de la lucha de clases","Invertí la dialéctica hegeliana poniéndola sobre los pies"]},
];

// ===== WORDLE =====
const wordleWords = [
  {word:"IDEAS",hint:"Esencias eternas de Platón"},
  {word:"LOGOS",hint:"Razón y palabra en la filosofía griega"},
  {word:"EIDOS",hint:"Forma o esencia en griego"},
  {word:"NOMOS",hint:"Ley o costumbre. Opuesto a physis"},
  {word:"PHYSIS",hint:"Naturaleza. Opuesto a nomos (6 letras)"},
  {word:"ARCHE",hint:"Principio originario de los presocráticos"},
];

// ===== PAREJAS FILOSÓFICAS =====
const parejasData = [
  {concepto:"Cogito ergo sum",autor:"Descartes"},
  {concepto:"Imperativo categórico",autor:"Kant"},
  {concepto:"Voluntad de poder",autor:"Nietzsche"},
  {concepto:"Alegoría de la caverna",autor:"Platón"},
  {concepto:"Eudaimonia",autor:"Aristóteles"},
  {concepto:"Alienación",autor:"Marx"},
  {concepto:"Conjunción constante",autor:"Hume"},
  {concepto:"Amor fati",autor:"Nietzsche"},
];

// ===== PODCASTS =====
const podcastsData = [
  {nombre:"Historia de la Filosofía sin Cortes",plataforma:"Spotify / iVoox",icon:"🎙️",desc:"El podcast más completo en español. Recorre toda la historia del pensamiento desde los presocráticos hasta hoy, con episodios dedicados a cada autor del currículo PAU andaluz.",episodios:"200+ episodios",tags:["Todos los autores","Currículo PAU","Muy completo"],url:"https://open.spotify.com/show/2qdnBzFelPJJNXb3XQf7ky",color:"#1db954"},
  {nombre:"Filosofía de Bolsillo",plataforma:"Spotify / Apple Podcasts",icon:"🧠",desc:"Episodios cortos de 10-15 min perfectos para estudiar en el bus o antes de dormir. Cada episodio cubre un concepto o autor del temario de 2º de Bachillerato de forma clara y directa.",episodios:"120+ episodios",tags:["Breve","Bachillerato","Conceptos PAU"],url:"https://open.spotify.com/search/filosof%C3%ADa%20de%20bolsillo",color:"#1db954"},
  {nombre:"La Caverna de Platón",plataforma:"iVoox / YouTube",icon:"🏛️",desc:"Podcast especializado en filosofía griega clásica. Episodios en profundidad sobre Platón, Aristóteles y los presocráticos. El mejor recurso para los autores de la Antigüedad.",episodios:"80+ episodios",tags:["Antigua","Platón","Aristóteles"],url:"https://www.ivoox.com/podcast-caverna-platon_sq_f1424124_1.html",color:"#ff6b35"},
  {nombre:"Kant en 10 minutos",plataforma:"YouTube / iVoox",icon:"📚",desc:"Serie monográfica dedicada exclusivamente a Kant. Explica la Crítica de la Razón Pura, la Fundamentación y la Paz Perpetua de forma accesible para estudiantes de Bachillerato.",episodios:"30 episodios",tags:["Kant","Monográfico","Ética"],url:"https://www.youtube.com/results?search_query=kant+explicado+bachillerato",color:"#ff0000"},
  {nombre:"Marx Explicado",plataforma:"iVoox / Spotify",icon:"⚙️",desc:"Alienación, plusvalía, materialismo histórico y lucha de clases explicados con claridad. Perfectamente orientado al currículo PAU de Andalucía con ejemplos actuales.",episodios:"25 episodios",tags:["Marx","Economía","Contemporánea"],url:"https://open.spotify.com/search/marx%20filosofia%20explicado",color:"#e63946"},
  {nombre:"Nietzsche Desencadenado",plataforma:"Spotify / YouTube",icon:"⚡",desc:"Todo sobre Nietzsche: la muerte de Dios, el superhombre, la voluntad de poder y el eterno retorno. Incluye análisis de textos del examen PAU con ejemplos de respuestas.",episodios:"20 episodios",tags:["Nietzsche","Textos PAU","Voluntad de poder"],url:"https://open.spotify.com/search/nietzsche%20filosof%C3%ADa",color:"#f4a261"},
  {nombre:"Hume y el Empirismo",plataforma:"iVoox / Podcast",icon:"🔬",desc:"Análisis del pensamiento empirista de Hume: impresiones, ideas, causalidad e identidad personal. Contiene análisis de fragmentos del tipo que suele aparecer en la PAU.",episodios:"18 episodios",tags:["Hume","Empirismo","Causalidad"],url:"https://www.ivoox.com/buscar_sq_f_1.html?phps=hume+empirismo",color:"#457b9d"},
  {nombre:"Descartes y el Racionalismo",plataforma:"Spotify / YouTube",icon:"🔍",desc:"El método cartesiano, el cogito, las sustancias y la relación mente-cuerpo. Episodios especiales con textos del Discurso del Método comentados párrafo a párrafo.",episodios:"22 episodios",tags:["Descartes","Racionalismo","Cogito"],url:"https://open.spotify.com/search/descartes%20raz%C3%B3n%20filosof%C3%ADa",color:"#2a9d8f"},
  {nombre:"Filosofía Política: Platón a Marx",plataforma:"Spotify",icon:"🏛️",desc:"Recorre las grandes teorías políticas desde la ciudad ideal platónica hasta el comunismo de Marx. Fundamental para las preguntas de contextualización y comparación.",episodios:"35 episodios",tags:["Política","Platón","Marx","Comparativa"],url:"https://open.spotify.com/search/filosof%C3%ADa%20pol%C3%ADtica%20historia",color:"#1db954"},
  {nombre:"Ética: De Aristóteles a Kant",plataforma:"iVoox / Apple Podcasts",icon:"⚖️",desc:"Compara las grandes teorías éticas del currículo: la ética de la virtud aristotélica, el imperativo categórico kantiano y la crítica nietzscheana a la moral.",episodios:"28 episodios",tags:["Ética","Aristóteles","Kant","Comparativa"],url:"https://www.ivoox.com/buscar_sq_f_1.html?phps=etica+filosofia+bachillerato",color:"#e9c46a"},
  {nombre:"Filosofía y Actualidad",plataforma:"Spotify / iVoox",icon:"💡",desc:"Conecta los grandes temas filosóficos del currículo PAU con problemas del mundo actual: inteligencia artificial, democracia, sostenibilidad. Ideal para enriquecer respuestas.",episodios:"50+ episodios",tags:["Actualidad","Aplicación","Contextualización"],url:"https://open.spotify.com/search/filosof%C3%ADa%20actualidad%20podcast",color:"#6d6875"},
  {nombre:"PAU Filosofía: Guía Completa",plataforma:"YouTube",icon:"🎯",desc:"Canal de YouTube con videos específicos para cada pregunta de la PAU de Filosofía en Andalucía. Incluye simulacros, correcciones y trucos para sacar la máxima nota.",episodios:"40+ videos",tags:["PAU","Andalucía","Examen","Consejos"],url:"https://www.youtube.com/results?search_query=PAU+filosof%C3%ADa+andaluc%C3%ADa+2025",color:"#ff0000"},
];

// ===== LIBROS =====
const librosData = [
  // ORIGINALES
  {titulo:"La República",autor:"Platón",nivel:"original",cat:"original",emoji:"📜",color:"linear-gradient(135deg,#2a1a0e,#4a2e10)",desc:"La obra política y filosófica más importante de Platón. Contiene el mito de la caverna y la teoría del filósofo-rey. Imprescindible para la PAU."},
  {titulo:"Ética a Nicómaco",autor:"Aristóteles",nivel:"original",cat:"original",emoji:"⚖️",color:"linear-gradient(135deg,#0e1a2a,#102a4a)",desc:"Fundamento de la ética aristotélica: eudaimonía, virtud como término medio y la amistad. Libro I y X los más importantes para PAU."},
  {titulo:"Política",autor:"Aristóteles",nivel:"original",cat:"original",emoji:"🏛️",color:"linear-gradient(135deg,#0a1520,#0e2540)",desc:"El ser humano como animal político, los tipos de gobierno y la polis ideal. Complemento esencial a la Ética a Nicómaco para la PAU."},
  {titulo:"Discurso del Método",autor:"Descartes",nivel:"original",cat:"original",emoji:"🔍",color:"linear-gradient(135deg,#1a0e2a,#2e104a)",desc:"El texto más accesible de Descartes: el cogito y las cuatro reglas del método. Su brevedad lo hace ideal para leer completo antes del examen."},
  {titulo:"Meditaciones Metafísicas",autor:"Descartes",nivel:"original",cat:"original",emoji:"💭",color:"linear-gradient(135deg,#1e0a30,#320a50)",desc:"Las seis meditaciones que fundamentan el sistema cartesiano: duda, cogito, Dios como garante y el mundo exterior. Fundamental para entender la 2ª y 3ª Meditación."},
  {titulo:"Investigación sobre el entendimiento humano",autor:"Hume",nivel:"original",cat:"original",emoji:"🔬",color:"linear-gradient(135deg,#0a1e2e,#0e2840)",desc:"Versión más accesible del Tratado de Hume. Explica impresiones, ideas y la crítica a la causalidad y la inducción. Más recomendable que el Tratado para PAU."},
  {titulo:"Fundamentación de la Metafísica de las Costumbres",autor:"Kant",nivel:"original",cat:"original",emoji:"📐",color:"linear-gradient(135deg,#0e2a1a,#104a2e)",desc:"El imperativo categórico y la autonomía moral. Texto fundamental para la PAU de Kant. Las tres secciones explican la moralidad desde el sentido común hasta la metafísica."},
  {titulo:"¿Qué es la Ilustración?",autor:"Kant",nivel:"original",cat:"original",emoji:"💡",color:"linear-gradient(135deg,#0c2215,#0e3a20)",desc:"Breve pero esencial: la mayoría de edad, el Sapere aude y el uso público y privado de la razón. Texto corto que cae con frecuencia en la PAU de Andalucía."},
  {titulo:"Así habló Zaratustra",autor:"Nietzsche",nivel:"original",cat:"original",emoji:"⚡",color:"linear-gradient(135deg,#2a0e0e,#4a1010)",desc:"La obra más literaria de Nietzsche: el superhombre, el eterno retorno y el último hombre. La parábola de las tres transformaciones del espíritu es esencial."},
  {titulo:"La Gaya Ciencia",autor:"Nietzsche",nivel:"original",cat:"original",emoji:"🎭",color:"linear-gradient(135deg,#2a1a0e,#3a2010)",desc:"Donde Nietzsche proclama la muerte de Dios (parágrafo 125). También contiene la primera formulación del eterno retorno. Imprescindible para la PAU de Nietzsche."},
  {titulo:"Más allá del bien y del mal",autor:"Nietzsche",nivel:"original",cat:"original",emoji:"🦅",color:"linear-gradient(135deg,#250e0e,#400e0e)",desc:"La crítica a la moral de los esclavos y la voluntad de poder. Complemento perfecto a Zaratustra para entender la transvaloración de los valores."},
  {titulo:"Manifiesto Comunista",autor:"Marx y Engels",nivel:"original",cat:"original",emoji:"✊",color:"linear-gradient(135deg,#1a0e0e,#3a1010)",desc:"El texto político más influyente de Marx. Breve, directo y poderoso. Explica la lucha de clases, el materialismo histórico y el programa comunista."},
  {titulo:"Manuscritos Económico-Filosóficos de 1844",autor:"Marx",nivel:"original",cat:"original",emoji:"⚙️",color:"linear-gradient(135deg,#1e0a08,#380a08)",desc:"Donde Marx desarrolla el concepto de alienación. Texto frecuente en la PAU de Andalucía. Explica las cuatro formas de alienación del trabajo."},
  // PAU
  {titulo:"Historia de la Filosofía — 2º Bachillerato",autor:"Varios Editoriales",nivel:"basico",cat:"pau",emoji:"📖",color:"linear-gradient(135deg,#2a2a0e,#4a4a10)",desc:"El manual de referencia para preparar PAU. Elige la editorial adaptada al currículo andaluz (Anaya, SM, Santillana). Incluye textos comentados y orientaciones."},
  {titulo:"Comentario de textos filosóficos PAU Andalucía",autor:"VV.AA.",nivel:"basico",cat:"pau",emoji:"📝",color:"linear-gradient(135deg,#0e2a0e,#104a10)",desc:"Guía práctica con textos PAU reales y correcciones modelo. Analiza fragmentos de todos los autores del currículo andaluz con la estructura del examen."},
  {titulo:"Selectividad Filosofía: Exámenes Resueltos",autor:"VV.AA.",nivel:"basico",cat:"pau",emoji:"🎯",color:"linear-gradient(135deg,#1a2a0e,#2a4010)",desc:"Recopilación de exámenes resueltos de los últimos 10 años en Andalucía. Cada pregunta tiene respuesta modelo con la puntuación detallada."},
  {titulo:"La Filosofía Explicada a mi Perro",autor:"Jordi Pigem",nivel:"basico",cat:"pau",emoji:"🐕",color:"linear-gradient(135deg,#1e0a28,#320a40)",desc:"Introducción muy amena a los grandes temas filosóficos del currículo. Ideal para estudiantes que empiezan desde cero con Bachillerato."},
  // DIVULGACIÓN
  {titulo:"El mundo de Sofía",autor:"Jostein Gaarder",nivel:"basico",cat:"divulgacion",emoji:"🌍",color:"linear-gradient(135deg,#0e1a2a,#103040)",desc:"La mejor novela para iniciarse en la historia de la filosofía. Recorre a todos los filósofos del currículo de forma narrativa y apasionante."},
  {titulo:"Historia de la Filosofía sin Cortes",autor:"José Pablo García",nivel:"basico",cat:"divulgacion",emoji:"🎙️",color:"linear-gradient(135deg,#1a0a1a,#2a0a2a)",desc:"El libro del podcast más escuchado de filosofía en español. Accesible, riguroso y divertido. Perfecto como complemento al temario oficial."},
  {titulo:"Filosofía para Dummies",autor:"Martin Cohen",nivel:"basico",cat:"divulgacion",emoji:"🎯",color:"linear-gradient(135deg,#2a0e1a,#4a1030)",desc:"Introducción amena y accesible a los grandes filósofos y sus ideas. Sin tecnicismos pero sin simplificar los conceptos esenciales."},
  {titulo:"Historia de la Filosofía Occidental",autor:"Bertrand Russell",nivel:"medio",cat:"divulgacion",emoji:"🌐",color:"linear-gradient(135deg,#0e1a2a,#102040)",desc:"Visión panorámica y crítica de toda la historia de la filosofía occidental. Escrita con brillantez y humor. Referencia clásica para profundizar."},
  {titulo:"Así habló Zaratustra (edición comentada)",autor:"Nietzsche / VV.AA.",nivel:"medio",cat:"divulgacion",emoji:"📚",color:"linear-gradient(135deg,#2a1a00,#3a2800)",desc:"Edición académica con notas y comentarios que facilitan la comprensión. Imprescindible si el texto de Nietzsche va a caer en tu PAU."},
  {titulo:"¿Qué es filosofía?",autor:"Ortega y Gasset",nivel:"medio",cat:"divulgacion",emoji:"🏺",color:"linear-gradient(135deg,#0a1e1e,#0a2e2e)",desc:"Introducción magistral al quehacer filosófico. Aunque Ortega no está en todas las opciones PAU, este libro ayuda a entender la filosofía como actividad vital."},
  {titulo:"El malestar en la cultura",autor:"Freud",nivel:"avanzado",cat:"divulgacion",emoji:"🧠",color:"linear-gradient(135deg,#1e1a08,#2e2808)",desc:"Aunque no es del currículo PAU, aporta perspectiva sobre la crítica a la civilización que enriquece enormemente las respuestas de relación con Marx y Nietzsche."},
  {titulo:"Crítica de la Razón Pura (selección)",autor:"Kant",nivel:"avanzado",cat:"original",emoji:"🔭",color:"linear-gradient(135deg,#0e1e0e,#0e3020)",desc:"Selección de los pasajes más accesibles: Prólogo a la 2ª edición, Estética Trascendental y comienzo de la Analítica. Para quien quiera ir más allá del temario básico."},
];


// ===== BANCO =====
const bancoData = [
  {autor:"Platón",año:"2022",tipo:"Definición",q:"Define los términos 'episteme' y 'doxa' en el pensamiento de Platón.",resp:"Episteme (conocimiento) es el saber cierto sobre las Ideas eternas e inmutables: el verdadero conocimiento del filósofo. Doxa (opinión) es el conocimiento del mundo sensible, cambiante: mera opinión sobre las apariencias. Solo la episteme merece llamarse conocimiento."},
  {autor:"Platón",año:"2021",tipo:"Comentario",q:"Expón la idea principal del texto sobre el Mito de la Caverna y relaciona con la filosofía platónica.",resp:"La idea principal es el contraste entre ignorancia (caverna, sombras, mundo sensible) y conocimiento verdadero (salida al sol, Ideas). Ilustra: 1) Teoría de los dos mundos. 2) Proceso educativo dialéctico de ascenso hacia el Bien. 3) Deber del filósofo de gobernar."},
  {autor:"Platón",año:"2020",tipo:"Relación",q:"Relaciona el pensamiento de Platón con el de Aristóteles respecto a la realidad y el conocimiento.",resp:"Semejanzas: ambos buscan el conocimiento universal y dan importancia a la razón. Diferencias: Platón separa las Ideas del mundo sensible (dualismo), Aristóteles defiende que la forma está en la materia (hilemorfismo). En gnoseología: Platón parte de las Ideas, Aristóteles de la experiencia sensible."},
  {autor:"Descartes",año:"2019",tipo:"Definición",q:"Define 'duda metódica' y 'cogito' en el pensamiento de Descartes.",resp:"La duda metódica es el procedimiento de poner en duda todo lo que admita la menor posibilidad de ser falso. El cogito (cogito ergo sum) es la primera certeza: al dudar, pienso; al pensar, existo. Fundamento de toda su filosofía."},
  {autor:"Kant",año:"2023",tipo:"Comentario",q:"Explica el imperativo categórico y su relación con la ética kantiana.",resp:"El imperativo categórico es el principio supremo: mandato incondicional y universal. Formulación: 'Obra solo según la máxima que puedas querer que sea ley universal'. Base: autonomía del ser racional y su dignidad como fin en sí mismo. Se opone al imperativo hipotético (condicional, no moral)."},
  {autor:"Hume",año:"2021",tipo:"Relación",q:"Relaciona la crítica de Hume a la metafísica con el pensamiento de Descartes.",resp:"Descartes usa la razón para fundamentar la metafísica (yo, Dios, mundo). Hume destruye estas pretensiones: sin impresión, la idea carece de significado. No hay impresión del yo sustancial, ni de Dios como ser necesario, ni de la conexión causal necesaria. Hume critica el dogmatismo racionalista cartesiano."},
  {autor:"Nietzsche",año:"2022",tipo:"Comentario",q:"Explica qué significa 'la muerte de Dios' en Nietzsche y sus consecuencias.",resp:"«Dios ha muerto» no es ateísmo: significa que la cultura occidental ha perdido la capacidad de creer en los valores absolutos trascendentes. Consecuencias: nihilismo y necesidad de transvaloración. El superhombre asume la tarea creadora de nuevos valores vitales."},
  {autor:"Marx",año:"2020",tipo:"Relación",q:"Explica el materialismo histórico y relaciona con Hegel.",resp:"Marx parte de Hegel pero lo invierte: mientras Hegel pone la dialéctica en el Espíritu/Idea, Marx la lleva a la realidad material. El materialismo histórico sostiene que la infraestructura económica determina la superestructura. La historia es la historia de la lucha de clases."},
];

// ===== EXÁMENES =====
const examenesData = [
  {año:"2025",autor:"Platón / Marx",opcionA:"Platón — República",opcionB:"Marx — Manuscritos Económico-Filosóficos",corrA:"Términos: sombras (mundo sensible/doxa), sol (Idea del Bien/noesis). Idea: el ascenso filosófico del conocimiento. Relacionar con Aristóteles: crítica al mundo inteligible separado.",corrB:"Términos: alienación (el trabajador se separa del producto y su esencia), trabajo (actividad creadora esencial). Relacionar con Hegel: Marx invierte la dialéctica idealista.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2024",autor:"Kant / Nietzsche",opcionA:"Kant — Crítica de la Razón Práctica",opcionB:"Nietzsche — Más allá del bien y del mal",corrA:"Términos: autonomía (darse la ley a uno mismo), deber (necesidad de actuar por respeto a la ley moral). Relacionar con Hume: razón vs sentimiento como base moral.",corrB:"Términos: voluntad de poder, resentimiento, moral del rebaño. Relacionar con Platón: crítica a los valores absolutos del mundo inteligible.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2023",autor:"Descartes / Hume",opcionA:"Descartes — Meditaciones Metafísicas",opcionB:"Hume — Investigación sobre el entendimiento humano",corrA:"Términos: duda metódica, cogito, res cogitans. Relacionar con Platón: ambos priorizan el conocimiento racional.",corrB:"Términos: impresión, idea, conjunción constante. Relacionar con Descartes: empirismo vs racionalismo.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2022",autor:"Platón / Nietzsche",opcionA:"Platón — República (Libro IV)",opcionB:"Nietzsche — El nacimiento de la tragedia",corrA:"Términos: alma racional, justicia, virtud. Relacionar con Aristóteles: virtud como término medio vs virtud como armonía.",corrB:"Términos: dionisíaco (impulso vital), apolíneo (orden, apariencia). Relacionar con Platón: crítica a la supremacía de la razón.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2021",autor:"Aristóteles / Kant",opcionA:"Aristóteles — Ética a Nicómaco",opcionB:"Kant — Fundamentación de la Metafísica de las Costumbres",corrA:"Términos: eudaimonia, virtud, término medio. Relacionar con Platón: eudaimonia vs mundo de las Ideas.",corrB:"Términos: imperativo categórico, máxima, deber. Relacionar con Aristóteles: deontológica vs teleológica.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2020",autor:"Platón / Marx",opcionA:"Platón — Fedón",opcionB:"Marx — La ideología alemana",corrA:"Términos: alma, cuerpo, anamnesis. Relacionar con Aristóteles: alma como forma del cuerpo vs alma inmortal.",corrB:"Términos: infraestructura, superestructura, ideología. Relacionar con Hegel: materialismo vs idealismo.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2019",autor:"Descartes / Nietzsche",opcionA:"Descartes — Discurso del Método",opcionB:"Nietzsche — Así habló Zaratustra",corrA:"Términos: evidencia, análisis, síntesis. Relacionar con Hume: método racional vs método empírico.",corrB:"Términos: superhombre, voluntad de poder, eterno retorno. Relacionar con Kant: creación de valores vs universalidad moral.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2018",autor:"Platón / Hume",opcionA:"Platón — El Banquete",opcionB:"Hume — Tratado de la naturaleza humana",corrA:"Términos: eros, belleza, Bien. Relacionar con Aristóteles: amor como impulso vs amor como hábito.",corrB:"Términos: impresión, yo, haz de percepciones. Relacionar con Descartes: res cogitans vs yo como ficción.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2017",autor:"Aristóteles / Marx",opcionA:"Aristóteles — Política",opcionB:"Marx — El Capital",corrA:"Términos: polis, animal político, bien común. Relacionar con Platón: ciudad ideal vs ciudad natural.",corrB:"Términos: mercancía, plusvalía, fetichismo. Relacionar con Nietzsche: crítica a la sociedad burguesa.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2016",autor:"Kant / Platón",opcionA:"Kant — Crítica de la Razón Pura",opcionB:"Platón — República (Mito de la Caverna)",corrA:"Términos: a priori, síntesis, fenómeno. Relacionar con Hume: respuesta al escepticismo.",corrB:"Términos: caverna, sol, prisionero. Relacionar con Descartes: ascenso al conocimiento verdadero vs duda metódica.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
  {año:"2015",autor:"Hume / Nietzsche",opcionA:"Hume — Investigación sobre el entendimiento",opcionB:"Nietzsche — La Gaya Ciencia",corrA:"Términos: razón, creencia, costumbre. Relacionar con Kant: escepticismo humeano como punto de partida.",corrB:"Términos: muerte de Dios, nihilismo, transvaloración. Relacionar con Platón: destrucción de los valores absolutos.",url:"https://www.juntadeandalucia.es/educacion/portals/web/evaluacion-e-informes/pau"},
];

// ===== ORDENAR CRONOLÓGICO =====
const ordenarData = [
  {nombre:"Tales de Mileto",año:-624},
  {nombre:"Sócrates",año:-470},
  {nombre:"Platón",año:-427},
  {nombre:"Aristóteles",año:-384},
  {nombre:"Descartes",año:1596},
  {nombre:"Hume",año:1711},
  {nombre:"Kant",año:1724},
  {nombre:"Marx",año:1818},
  {nombre:"Nietzsche",año:1844},
  {nombre:"Ortega y Gasset",año:1883},
];

// ===== RENDER AUTORES =====
function renderAutores(filter='all') {
  const grid = document.getElementById('autoresGrid');
  grid.innerHTML = '';
  autoresData.filter(a => filter==='all' || a.periodo===filter).forEach(autor => {
    const card = document.createElement('div');
    card.className = 'autor-card reveal';
    card.innerHTML = `<div class="autor-era">${autor.era}</div><div class="autor-name">${autor.nombre}</div><div class="autor-dates">${autor.fechas}</div><div class="autor-desc">${autor.desc}</div><div class="autor-tags">${autor.tags.map(t=>`<span class="tag tag-gold">${t}</span>`).join('')}</div><div class="autor-progress"><div class="progress-bar"><div class="progress-fill" style="width:${autor.progreso}%"></div></div><span class="progress-label">${autor.progreso}%</span></div>`;
    card.addEventListener('click', () => openModal(autor));
    grid.appendChild(card);
  });
  observeReveal();
}

// ===== MODAL =====
function openModal(autor) {
  document.getElementById('modalEra').textContent = autor.era;
  document.getElementById('modalName').textContent = autor.nombre;
  document.getElementById('modalDates').textContent = autor.fechas;
  const sectionMap = {contexto:autor.contexto,conocimiento:autor.conocimiento,realidad:autor.realidad,'ser-humano':autor.serhumano,etica:autor.etica,conceptos:autor.conceptos,resumen:autor.resumen,pau:autor.pau,comentario:autor.comentario};
  const body = document.getElementById('modalBody');
  body.innerHTML = '';
  Object.entries(sectionMap).forEach(([key,content]) => {
    const div = document.createElement('div');
    div.className = 'modal-section'+(key==='contexto'?' active':'');
    div.dataset.section = key;
    div.innerHTML = content;
    body.appendChild(div);
  });
  document.getElementById('modalOverlay').classList.add('open');
  document.body.style.overflow = 'hidden';
  document.querySelectorAll('.modal-nav-btn').forEach(b => b.classList.toggle('active', b.dataset.section==='contexto'));
}
document.getElementById('modalClose').addEventListener('click', () => { document.getElementById('modalOverlay').classList.remove('open'); document.body.style.overflow=''; });
document.getElementById('modalOverlay').addEventListener('click', e => { if(e.target===e.currentTarget){ document.getElementById('modalOverlay').classList.remove('open'); document.body.style.overflow=''; }});
document.querySelectorAll('.modal-nav-btn').forEach(btn => {
  btn.addEventListener('click', () => {
    const s = btn.dataset.section;
    document.querySelectorAll('.modal-nav-btn').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    document.querySelectorAll('.modal-section').forEach(s2 => s2.classList.toggle('active', s2.dataset.section===s));
  });
});

// ===== TABS AUTORES =====
document.querySelectorAll('.tab-btn[data-filter]').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.tab-btn[data-filter]').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    renderAutores(btn.dataset.filter);
  });
});

// ===== TABS LIBROS =====
document.querySelectorAll('.tab-btn[data-libfilter]').forEach(btn => {
  btn.addEventListener('click', () => {
    document.querySelectorAll('.tab-btn[data-libfilter]').forEach(b => b.classList.remove('active'));
    btn.classList.add('active');
    renderLibros(btn.dataset.libfilter);
  });
});

// ===== FLASHCARDS =====
let fcIndex = 0;
function updateFC() {
  document.getElementById('fc-question').textContent = flashcardsData[fcIndex].q;
  document.getElementById('fc-answer').textContent = flashcardsData[fcIndex].a;
  document.getElementById('fcCount').textContent = `${fcIndex+1} / ${flashcardsData.length}`;
  document.getElementById('flashcard').classList.remove('flipped');
}
document.getElementById('flashcard').addEventListener('click', () => document.getElementById('flashcard').classList.toggle('flipped'));
document.getElementById('fcPrev').addEventListener('click', () => { fcIndex=(fcIndex-1+flashcardsData.length)%flashcardsData.length; updateFC(); });
document.getElementById('fcNext').addEventListener('click', () => { fcIndex=(fcIndex+1)%flashcardsData.length; updateFC(); });

// ===== QUIZ =====
function renderQuiz() {
  const container = document.getElementById('quizContainer');
  let html = quizData.map((q,qi) => `<div class="quiz-question"><div class="quiz-q-num">Pregunta ${qi+1} de ${quizData.length}</div><div class="quiz-q-text">${q.q}</div><div class="quiz-options">${q.opts.map((opt,oi) => `<button class="quiz-option" data-qi="${qi}" data-oi="${oi}" onclick="answerQuiz(this,${qi},${oi})">${opt}</button>`).join('')}</div><div class="quiz-explanation" id="exp-${qi}">${q.exp}</div></div>`).join('');
  html += `<div style="display:flex;justify-content:space-between;align-items:center;margin-top:1.5rem;flex-wrap:wrap;gap:0.75rem"><button class="btn-primary" onclick="resetQuiz()" style="border:none;cursor:pointer">↺ Reiniciar test</button><div style="font-size:0.83rem;color:var(--text3)" id="quizProgress">0 / ${quizData.length} respondidas</div></div><div class="quiz-score" id="quizScore"><div style="margin-bottom:0.4rem;font-size:0.83rem;color:var(--text3)">Puntuación final</div><div class="score-num" id="scoreNum">—</div><div style="font-size:0.875rem;color:var(--text2);margin-top:0.4rem" id="scoreFeedback"></div></div>`;
  container.innerHTML = html;
}
let quizAnswers = {};
function answerQuiz(btn, qi, oi) {
  if(quizAnswers[qi]!==undefined) return;
  quizAnswers[qi]=oi;
  const opts = document.querySelectorAll(`[data-qi="${qi}"]`);
  opts.forEach((o,i) => { o.disabled=true; if(i===quizData[qi].correct) o.classList.add('correct'); else if(i===oi) o.classList.add('wrong'); });
  document.getElementById(`exp-${qi}`).classList.add('show');
  const done = Object.keys(quizAnswers).length;
  document.getElementById('quizProgress').textContent = `${done} / ${quizData.length} respondidas`;
  if(done===quizData.length) {
    const score = Object.entries(quizAnswers).filter(([qi,oi]) => Number(oi)===quizData[qi].correct).length;
    const pct = Math.round(score/quizData.length*100);
    document.getElementById('quizScore').classList.add('show');
    document.getElementById('scoreNum').textContent = `${score}/${quizData.length}`;
    document.getElementById('scoreFeedback').textContent = pct>=80?'¡Excelente! Estás listo para la PAU 🎓':pct>=60?'Bien, repasa los temas fallados.':'Necesitas repasar más. ¡Tú puedes!';
  }
}
function resetQuiz() { quizAnswers={}; renderQuiz(); }

// ===== JUEGOS =====
let qgIndex=0, qgScore=0, qgPistaIndex=0, qgAnswered=false;
let parejasState={cards:[],flipped:[],matched:[],timer:0,interval:null};
let ordenarState={items:[],selected:null};

function showGame(type) {
  const zone = document.getElementById('gameZone');
  zone.style.display='block';
  zone.scrollIntoView({behavior:'smooth'});
  if(type==='quiensoy') renderQuienSoy();
  else if(type==='wordle') renderWordle();
  else if(type==='parejas') renderParejas();
  else if(type==='ordenar') renderOrdenar();
  else if(type==='ahorcado') renderAhorcado();
  else if(type==='verdadmentira') renderVerdadMentira();
  else if(type==='definicion') renderDefinicion();
  else if(type==='ruleta') renderRuleta();
}

// ===== AHORCADO =====
const ahorcadoPalabras = [
  {palabra:'DIALECTICA',pista:'Método de argumentación por contradicción (Platón, Hegel)'},
  {palabra:'EMPIRISMO',pista:'Corriente que defiende que el conocimiento viene de la experiencia'},
  {palabra:'RACIONALISMO',pista:'Corriente que defiende que la razón es fuente del conocimiento'},
  {palabra:'IMPERATIVO',pista:'Mandato moral incondicionado en Kant'},
  {palabra:'ALIENACION',pista:'Concepto clave en Marx: el trabajador pierde su esencia'},
  {palabra:'NIHILISMO',pista:'Filosofía que niega valores absolutos (relacionada con Nietzsche)'},
  {palabra:'EUDAIMONIA',pista:'Felicidad o florecimiento humano para Aristóteles'},
  {palabra:'METAFISICA',pista:'Rama de la filosofía que estudia la realidad más allá de lo físico'},
  {palabra:'ILUSTRACION',pista:'Movimiento cultural del siglo XVIII: mayoría de edad de la razón'},
  {palabra:'VOLUNTAD',pista:'Concepto central de Nietzsche: la __ de poder'},
];
let ahorcadoEstado = {};
function renderAhorcado() {
  const item = ahorcadoPalabras[Math.floor(Math.random()*ahorcadoPalabras.length)];
  ahorcadoEstado = {palabra:item.palabra, pista:item.pista, descubiertas:new Set(), errores:0, maxErrores:6, terminado:false};
  dibujarAhorcado();
}
function dibujarAhorcado() {
  const {palabra,pista,descubiertas,errores,maxErrores,terminado} = ahorcadoEstado;
  const letrasUsadas = [...descubiertas].join('');
  const letrasABC = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
  const partes = ['cabeza','cuerpo','brazo-izq','brazo-der','pierna-izq','pierna-der'];
  const svgPartes = [
    `<circle cx="50" cy="20" r="10" stroke="var(--red)" stroke-width="3" fill="none"/>`,
    `<line x1="50" y1="30" x2="50" y2="65" stroke="var(--red)" stroke-width="3"/>`,
    `<line x1="50" y1="38" x2="25" y2="55" stroke="var(--red)" stroke-width="3"/>`,
    `<line x1="50" y1="38" x2="75" y2="55" stroke="var(--red)" stroke-width="3"/>`,
    `<line x1="50" y1="65" x2="30" y2="90" stroke="var(--red)" stroke-width="3"/>`,
    `<line x1="50" y1="65" x2="70" y2="90" stroke="var(--red)" stroke-width="3"/>`,
  ];
  const displayPalabra = palabra.split('').map(l=>descubiertas.has(l)?`<span style="color:var(--gold);font-size:1.5rem;font-weight:800;font-family:var(--font-mono);border-bottom:3px solid var(--gold);padding:0 4px;margin:0 3px">${l}</span>`:`<span style="font-size:1.5rem;color:var(--text3);border-bottom:3px solid var(--border);padding:0 4px;margin:0 3px">_</span>`).join('');
  const ganado = palabra.split('').every(l=>descubiertas.has(l));
  const perdido = errores>=maxErrores;
  document.getElementById('gameZone').innerHTML = `
    <div class="quiz-game-container">
      <div class="qg-card" style="text-align:center">
        <div style="font-size:0.72rem;font-weight:700;color:var(--red);text-transform:uppercase;letter-spacing:0.08em;margin-bottom:0.5rem">🪢 FiloAhorcado — ${errores}/${maxErrores} errores</div>
        <div style="font-size:0.82rem;color:var(--text2);margin-bottom:1rem;font-style:italic">${pista}</div>
        <svg width="100" height="110" viewBox="0 0 100 110" style="margin:0 auto 1rem;display:block">
          <line x1="10" y1="105" x2="90" y2="105" stroke="var(--text3)" stroke-width="3"/>
          <line x1="30" y1="105" x2="30" y2="5" stroke="var(--text3)" stroke-width="3"/>
          <line x1="30" y1="5" x2="50" y2="5" stroke="var(--text3)" stroke-width="3"/>
          <line x1="50" y1="5" x2="50" y2="10" stroke="var(--text3)" stroke-width="3"/>
          ${svgPartes.slice(0,errores).join('')}
        </svg>
        <div style="margin-bottom:1.5rem;min-height:3rem;display:flex;flex-wrap:wrap;justify-content:center;gap:2px">${displayPalabra}</div>
        ${ganado?`<div style="font-size:1.5rem;margin-bottom:1rem">🎉 ¡Has ganado! La palabra era <strong style="color:var(--gold)">${palabra}</strong></div>`:''}
        ${perdido&&!ganado?`<div style="font-size:1.2rem;margin-bottom:1rem;color:var(--red)">💀 ¡Has perdido! Era: <strong>${palabra}</strong></div>`:''}
        ${(!ganado&&!perdido)?`<div style="display:flex;flex-wrap:wrap;gap:6px;justify-content:center;margin-bottom:1.25rem">${letrasABC.split('').map(l=>`<button onclick="letraAhorcado('${l}')" style="width:36px;height:36px;border-radius:6px;font-weight:700;font-size:0.85rem;cursor:pointer;border:none;background:${letrasUsadas.includes(l)?(palabra.includes(l)?'var(--teal)':'var(--bg3)'):'var(--card2)'};color:${letrasUsadas.includes(l)?(palabra.includes(l)?'#0d0f14':'var(--text3)'):'var(--text)'};pointer-events:${letrasUsadas.includes(l)?'none':'auto'}">${l}</button>`).join('')}</div>`:''}
        <button onclick="renderAhorcado()" style="background:var(--red-dim);border:1px solid rgba(224,92,92,0.3);color:var(--red);padding:0.5rem 1.25rem;border-radius:var(--radius-sm);font-size:0.82rem;font-weight:700;cursor:pointer">Nueva palabra 🔄</button>
      </div>
    </div>`;
}
function letraAhorcado(l) {
  if(ahorcadoEstado.terminado) return;
  ahorcadoEstado.descubiertas.add(l);
  if(!ahorcadoEstado.palabra.includes(l)) ahorcadoEstado.errores++;
  dibujarAhorcado();
}

// ===== VERDAD O MENTIRA =====
const verdadMentiraData = [
  {enunciado:'Platón escribió "La República" donde describe la ciudad ideal gobernada por filósofos.',respuesta:true},
  {enunciado:'Según Hume, las ideas preceden a las impresiones sensibles.',respuesta:false,explicacion:'Es al revés: las impresiones son primero, las ideas son copias de ellas.'},
  {enunciado:'El imperativo categórico de Kant dice: "Actúa solo según aquella máxima que puedas querer que sea ley universal."',respuesta:true},
  {enunciado:'Aristóteles fue discípulo de Sócrates directamente.',respuesta:false,explicacion:'Aristóteles fue discípulo de Platón, no de Sócrates.'},
  {enunciado:'Marx afirma que la religión es "el opio del pueblo".',respuesta:true},
  {enunciado:'Nietzsche proclama que "Dios ha muerto" en su obra "El capital".',respuesta:false,explicacion:'Lo proclama en "La gaya ciencia" y "Así habló Zaratustra". El capital es de Marx.'},
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
<script>
// ===== SUPRIMIR ERRORES EXTERNOS =====
window.addEventListener("error", function(e) {
  if (!e.filename || e.filename === "") { e.preventDefault(); return false; }
}, true);
window.onerror = function(msg, src) { if (!src || src === "") return true; };

// ===== FOTOS FILÓSOFOS =====
var FOTOS = {
  kant: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQADsDASIAAhEBAxEB/8QAGwAAAQUBAQAAAAAAAAAAAAAABQECAwQGBwD/xAAsEAACAQMDAwMCBwEAAAAAAAABAgMABBEFITEGElETQWEUIjJxgZGhscFS/8QAGAEAAwEBAAAAAAAAAAAAAAAAAgMEAAH/xAAdEQACAgMBAQEAAAAAAAAAAAAAAQIRAyExQRNR/9oADAMBAAIRAxEAPwDkmMcUnxT6IaPYieQzSDMcZGAeGPisZKyGz0ua67SQVUnYmiEvTcsMXrK3cmAc5rd6d05BcRLJMxJYBttgKmuemYyAsEjoMnG+1JeVWO+To5NeWkkDkMOKre1dMvekYEgdjIzyYz3HiufahatazshG2dqZGalwCeNx6V0pTmvR04jejFkkEZllVM4yefFa2KNLbToYAoDc5xz80B0WeGKVknAKvtg8Gjc0b9iIrg23qEIWI7jx/A/2gkHE6HoEgl06BhgkoKvzED2oZYRSwabFHbdveqAfFVLeG7+peSVpY8SEdvrdwZQPxDbbPipK2y3hbvJlFs5O4xXLep4wtwRncbn9a0+tJeyahcW5lZkQI0aep2AofxNtyQdsVluoIniniWRQrNGCQCdqdiVMVmdxAqc0pO9IBhiBS1QSHs4NENM1ARTKt07GHOx57T5x70ONMY71xqzqdOzs2l6kk0SSQOHjI2ZdwcVba6d2IRR81nuhY0vOl4/pADPaSP6qDkhjmi6usisO8ow/5ODUc40y+E1KNgLX7yKHU7GaQSRzAsjgjhD75G3OKxGu3bz30ju3cQxAPxWn6iSfuMk6uUTJWR2H9D3rDzMXkZj7mn416IzvwRDvTjzTEp9OJjxr3os0Zf8AYeafGmTlh9v91KSQK5YSj+kmha3e6FerdWMmG4dG3Vx4I/2tzcdY6DqljJd3EM1rqKLkRRNgyN8HGCPOQDXOpIu85TAPiowrI33AiuOKZk3HgeW41HW4J4+2SaTIIA2Ufmfigs8MlvO8FwhSRDgijPTnUlxpN3FHM7SWWcNGTso8j8vFP62ijGuF7YH6dolaM42AO4A/estaM3ewElOxSJTsCiBJwPivMKUU1jvsKEYRH7d/BqeJTJIqKO5mICjyahO+Pmn27srKynDKcg1mcJtW02ewkAuY1GfcHIo5p6yX2hzWl5A5eCAGJzsxjzlSPIU/wfigd/e3F8w+pfvCjA2qSLWL8zW7xuRLCO1Sq5Le2CPfbbFc3WwmleigY3icpIuGHIpCN+KvaniSZJ41IjkUbY/CRyv6VROc0Qs//9k=",
  nietzsche: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCAA1AFADASIAAhEBAxEB/8QAGwABAAIDAQEAAAAAAAAAAAAAAAYHAgQFAwj/xAAuEAABAwMDAgUDBAMAAAAAAAABAAIDBAURBhIhMUEHEyJRYRUygRQkQpFyobH/xAAUAQEAAAAAAAAAAAAAAAAAAAAA/8QAFBEBAAAAAAAAAAAAAAAAAAAAAP/aAAwDAQACEQMRAD8ApNERAWcEEtRM2GCN0kjjhrWjJKwUx0XpuW9Ub20shZNUSmFzh/Fgxx+Sefhvyg1KKxW6GmM10rWvk2nMETwCw59/5ce3+1zbvbIaWYuo5jLSudhjyQecZwcd+V9IWrwv0rbreynnt0dbNtAlqKglz3nvjngfAUV1X4UWh5P0maajjJ3mIepod0yM89EFCuBa4g9Qi6F/t0lpus9FMMOidgEdHDsfyFz0BERAREQFb3gvFVTGlNK1jIY5XGd7nDc/Lh6QM5x05wqhVi+EOoaWiu9Hbamne6eSpJpJmyYa1z2hpa8dxgcHsSgurXOpblYKTzbZZpK7Ddz5N2GM56fJUXm11qOl0wb9ctO+XHJL5UcLXEOwR9xBGQDhTa73SShge/axxx6d3QH3Pwqz1L4lVZf9MEFJLTmRv7mbLHOAGSdmeCT0+EFYa6ur7zeW1slL+me+EB0ec8gnuo6pX4iV0Vzu0FRSQtZTtp2ta5g4JySf+qKICIiAiIgLr6Qa92qrQYyARWwnJ/zC5C96KpfS1dPURu2uhkbICOxBzlB9QXqnjrJHtnqXwb24afYZ56qpr3pq00U1QZa51VJK8BhLBlzieGjByTn2Vz2ato7pQMiqDE/dHv2vxy3H3D455PZVjbbzo+2eIsscUDsGTFLWTS7mQSZ5AaR6QezskjI6IKknq37pYtmGBxwx5zt7f2tNb9/gFNe6+Frmva2oftc3oQTkEfghaCAiIgIiICzaB0REEhuVfVz2+wTuqHt8umfCwMcQRh5BOfkY/pTSPQFrrNAx3R0krbg6N87pySd3J4IyiIKuqWFpG524gDnHbC8ERAREQf/Z",
  kafka: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQADwDASIAAhEBAxEB/8QAGwAAAgIDAQAAAAAAAAAAAAAABAYBBQADBwL/xAAwEAACAQMCBAQFBAMBAAAAAAABAgMABBEFIQYSMUEUIlFxBxNhkcEjQlKBFTKx0f/EABQBAQAAAAAAAAAAAAAAAAAAAAD/xAAUEQEAAAAAAAAAAAAAAAAAAAAA/9oADAMBAAIRAxEAPwBvkPKCc1X3EuTjNE3Em5GarpTvigC1XULfTrN7q5YhF7DcsewFIeocY6hNITZj5EedgACcfUmo441Br/U/Bxn9G2OMDux6n8UBa6HcTpmWOUEf6qF6igKi4w1eNlZ5EdBuVZBvTDpnFNtqrrA6GG5YbL1VvY/ikPUbOSznKMrqB2I6fStFtM9vcRzxnzxsGHuKDp0hy2xzXnNaIrlLiCOdB5ZFDAeman5lA5XEuCTtQDzFnwASc1lxMckZoN5cHIJB9aCo4O0CG74svZryEvDDMww3QMd67RFbWyRoogRQo8vl6Uo3HDa6rJdPzpHcyBHbkyMnGMnHVsd61aHoWr6ffyNPfXXhQzARu5IIwcEZO1Bt430y2a0dTBGS3XyDJrhGr2ng72SNQeXO21P01nfazYT3095czXTTlRAjtyqu++3fp96VNesJtOdFuGJlXDkF8lf7oL+yQQWcMeT5Y1G/tW/nB7UBpiyixVpn5mclgT2HaiulAwzOcnehpWyete5mIzQ7MT3oGDhrVLhNQHzJSyiML5v4j/ym3Vr5fD/OjVpEVGLLHjJ27Zrm1kZjdxLbn9R3CLn1JxV1O5e3li8R4e4iJD88rdR6AGgVNG1eSwW6Z43gVWJQSbH+xS/ynXLye6u3bAcbD91etdmRJ5La3c3FzI255i3/AGqq1u3sLlgrc6Zw4HQn1FA1AqoCqAANgKwuPWgra7hulzC2SOqkbit2/pQXt1MqqXdgqgZJPQUv3vEKJ5bNC7fzcYH2qeJ7rlSO2U7t5m9u1Lb7CgudM1W5k1zTpJ525Eu4ThdgPOOwrrXGGjaXqOvpaNexWr3EvK3PjIbHN5R9d/TeuN8OLz8R6THjmzeRbDv5xT9xLc6XrPHFpNJOyc2pxqqg4SWIYXmz65H2NAfxjwzoPC3DVxe2CYmcfLiklbLSOepHqfbYAVxnFOfxI4rPE2uSfJkP+PtSY7VB0I7v7nH2ApOYYJoMVmQhkJUjuDijo9WulXBKv9WG9V5NZmgtdUn8VeSyk7FsL7DpQj+1e+XuanlFAZwwXTiOzuVjZ1tZVmcA/tUgn8ferH4kWyR66LqykHgphz2+DuM7kf0T+O1b/h9BBdXV/aSSLHcXNuFgZunMHDEe2BS3qczTzHLEopIQZyAM9vc70AfYbVjb1LHt27VBORQeTWVNeT1oP//Z",
  schopenhauer: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQAD8DASIAAhEBAxEB/8QAGwAAAQUBAQAAAAAAAAAAAAAABQACAwQGAQf/xAAvEAACAQMDAwMEAQMFAAAAAAABAgMABBEFEiEGMUETUWEicYGRoRQVMiM0UrHx/8QAFAEBAAAAAAAAAAAAAAAAAAAAAP/EABQRAQAAAAAAAAAAAAAAAAAAAAD/2gAMAwEAAhEDEQA/ACrlMnIFSLyoQKT7ADvTkAGOBwfNWoSY3EsYw0f1jHxQXbXp+4eF5nZUKjIU8k1H/bLl1IEYGOQxOB+KM32vQegnpsctwG9j7VPZAyRB2I3MM5NBnrfTJpldTsjYeHbFU76ynsiFuQqsfKndRnWbWKCRbxRIjBwJTGeCPcj8irtxEktoyODyuCzcUGFuQATkfag87sJHJ7UZmXAOaG3AXdjbmgOFGXyT8CpFldT9JKke1IuQmQe1Vndy5I7GgoalqEEepxLqEhigjXeW2Z3E4AwB9jWjh6u6djsIrn+sb+lyUEgjcgsO4HH27+9Z7VolBguJ1ZoslGcLkxnuD8+avdO6hp02mT2NvbzT3QlaR7YIysvbBLY2g4HftnigMxdRWFwrTWkzyxxqGaEp9WD5x5+1RS6ra3UG6AD1QoYpkggZIBI/FdE6TCFLOF9pXl2jCOB5Ujwc8YrOwajp1812mmNITBOwlDjBDHk45PGd380D72fBbPJPJoVNNzz+6tXTluSPiqUozg0GuEP08c5qPYA2MZPsKlWU4Cgc1heretoUguLHRHLzH6JLkD6VB4Ow+T89vagNy9R2F2+saVFcwxrbW4d5ZZAqSsGwyA/bAz7n2FUun7uys2kS6a3gkJP+59VXcfJJwPxmvKCuCAR9gRXrLX0djpbvrtk1tiEv6asHTfyNiZHGcAgZ8/FAT6n12LprQzcwoUvrgFLNGzlvdyDyVUds/FeU9N60+kal67hpIZRtnUHlhnOR8g8/uh95PLcS+pJv2gYRSxYIv/EE+KhQeaD1kXNvf2qzWNws0ZPJU9vgjwfg1DIv0jdkivN9Pv7rS7n17Z8EjDqf8XHsRW2s9es9RjVY39OdhzCx5GO+D2NAc6xvzadO3BVtkk2IVKnk57/wDXlsON+B3+K0PX2qG71BbOPiK2H1fLnv+hgfuswkhDLQdvVHqbfcc1qurdZN7oOi26SA+pCs0y85yo2j+d36rIztulJpxlZ0Te2diBFHsB/6aDhkIHbmuKcnPFJkYIsjf4twOabnigdI2aYhKnKkgjyK5SoCllH/AHC6kmu5OGcAsxxlmPj/ALrQw9OaG07gX1xLgEbNyqUPv2/g1krS7ktiPTYqN4b8iit1qCzSpLJJHJ7NJb4JH3FBS1nTJdOuMFvUgc/6coGN3wR4NDzU9zctKXVVVUYjgZxx9+1QUCPgZNKusVONoxxzTRQLNKlSoP/Z",
  maquiavelo: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQAD4DASIAAhEBAxEB/8QAHAAAAgIDAQEAAAAAAAAAAAAABAUDBgECBwAI/8QALBAAAgEDAwIFBAIDAAAAAAAAAQIDAAQRBRIxIUEGEyJRYRQycYEzwUKR4f/EABoBAAIDAQEAAAAAAAAAAAAAAAIEAAEDBQb/xAAhEQACAgICAgMBAAAAAAAAAAABAgADBBEhMRJBEyJRBf/aAAwDAQACEQMRAD8A4+OaJg6MCagVcnFFxL0FZsYwom6AtIDRcyRpGDI2Cf3UKLhgTXSdO0zwvJoVtcX6xi4WMCYNIwDORkbqWtsCa3NkUt1OewQJJGGjIYe4NektWORjFT29ubPXbiER7IZU3ogOcDtRcsYDEdqhb8lEEcGJWtwoO4mgnADYFOrpPScClEqbXNaIdwTMQISSR70dFET2qG1TnNMIQFPQ56VGMsDiaOgC8Yq6aZ4hddHhklnhUWsTQNG/LDptbHfjFUa8vIYTsJLP3Ve35oe31yWAzK1vFLBLjMUnuODkdc9aBqTYvUKu4I3Jj6wX6m/nupXbzXHpyfuHc4oiVMEmqjeaveXVykxcRGPpGsQ2hB8f9omLxBc5AuFSRe5A2mrNLdwGuUmNrpQFJJApROFLZBB+c1rqV357Dy2zHgYoJGI70aIQNyFhuMoG2jiipXWOFnX2yfiobWMySbQe9SasohsmUfcSBn3oTosBGKayVNh6EQnJJJ5JrUit6w3zTc500phpVn5/mu65QDb19zQNWjTYvK0iEkn17nHT3OP6rK5vFY5/PpFt3PQ5lceNoJWhfgdQfescUbqyAtvT/GggMjIqKdjcG+r4rCo69S0Q2M9lKXu4WjU/bu70Fr7b4eMYIIrq0eo6Xa2aJJax3JmIjEfTI9+p4ArkWvuDLJ5f8ZmYRnPKgnH9UpQ5sfZjz2CvHavUVDtWsqsrYZSG5wRg9ansZEjuopJQDGjqzblyMZGcjv8AivoBPD+gXemX1/cW0F5LNAWJmRPThcrjGdvbvmmLbvjI2Jy0rDDucC03T59QnEcK+nPqcj0oPmrf5KWlmsW8lEGzDGvSagohSKJFjRVAKqABnHxS+9vA3JJJOQD2rB3aw/gnoMfGrxVPOyYt1HbvkAIK45pXD9tb3t0ZZGUdBnr81DE2CetNIpCzj5Vy2W8ep0nVbn62CUz7Wl2Md4AB47454qk6+VDWyKAMITj8mrTFmYTOpGPpnJ/1VM1WXzrrKg4VAtLYw+00yj9IKDhT80+8KamILsWd3NJ9FN0MZkITd2yOMdv3SDacV4g44pt1DqQYjW5Rgwh2r3A+unS0uC9sHPl46dPb9cVFYsWZwxJ6Z6mhMGprQkTfkEVXiAuprVaxuBMzex4cOODz+agU4NHzruQqe9LwCDg1aniVkrqwke5//9k=",
  seneca: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCAA5AFADASIAAhEBAxEB/8QAHAAAAgIDAQEAAAAAAAAAAAAAAgYDBwABBQQI/8QAORAAAgEDAgMFAgsJAAAAAAAAAQIDAAQRBSEGEjETIkFRYTJxFDM0NTZScnN0gbIHI5GhscHR4fD/xAAWAQEBAQAAAAAAAAAAAAAAAAAAAQL/xAAaEQEBAAIDAAAAAAAAAAAAAAAAAQIREiEx/9oADAMBAAIRAxEAPwCqjWePpUvIDWcg8KqBBIUnwoVyemc1OkJcqg6scCu/p/D0zyIF3RgMsPHPlVk2F+O3kYZ5dvWhaFlGSNs1bMnBoSxP7hCSAobxz9albifQ/gM0h5FEWAwKncDpg1eITOXFGNwBiidOU1pemayMXOK2PWtisqjAMNREeO2K3gZoCd/Sg9ulmEXcZuA5jBwQhwSPIGrN0a/tYo4FtIUCKvM0p6jzGfzqq7PHbqDy4znBOM4p04WujPayLIkbQxNyyDJzg7CtYhufjbTbq5FnaSS86nc9n3QBuf5Uj8Ua9a6hHMttMGZz0C+Apnv5rCzRpol7pt2UNFHzBAQQAQOlIjTW02kw9vs8PcQIB3vQ/wAatRxSOaAn1qJcFd6OfZQo89xUQ6etYUa0Q61Gp3qTIzjFAZIVsGhcEnIqWRVz3hWwnaEJGGLHoAMk0EMMTyzpGgyzHAzTXwVJDFqc9pcd3touQAnAJz40OicHajciO7fEKBgQG9r/AFTBacNpbXnavEZH6yEnII6beVakoy80t5kuXFyyiPARBNyLv16DJNIM8bJIyFgwBIZs5yaYuIIdR029uIYrmWSBsFPcegpcmUtkuTzE7geFKjnueZic5GaHBzsa9otFPssc1E9pMrbIxHoKwqEEjxo1OSQaAqQSrKQfI7USjGMGgYOEtAl4k1WO1RikQXtJX+qv+auS04V03R7YfArSJHVcc5GWPvNIv7FPnG++4T9Rq2r72V99aiwnsk0nEcFhG4ReyMkgHTAPjXfls0FtJzL4e0o8K5Nn9LZfw/8AemO4+If3GraRW3H2mNHZ213EXaPtVRj559nekYabPJdmCJGkdWw2B0PjVr8W/R2z/Gxfqrx6N8t1b8VJ/Wr6hMj4eNj3rySNJuYFABzZ8qcNL4SlLm51JY3VwDyBcMPL3V4dd+XWv2RVhWXyNfuxS9EhB4z4ZjTRmNvDGMHmXYf9mqkkTkbcbZr6E4n+YZPyqg7745/tGs0f/9k=",
  wilde: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQADADASIAAhEBAxEB/8QAGwAAAwEAAwEAAAAAAAAAAAAABAUGAwECBwD/xAA0EAACAQMDAQUGBQQDAAAAAAABAgMABBEFEiEGEyIxQVEUMmFxgZEVI0KhsQfR4fBicrL/xAAXAQEBAQEAAAAAAAAAAAAAAAABAgAE/8QAGhEBAQEAAwEAAAAAAAAAAAAAAAERAiExQf/aAAwDAQACEQMRAD8A4QYxRCUOGGa3iauTHUKQVvEooeI1uZ4reMvPIsa+rHFbBohUrvjbXW3minRXhkV0YZBU5BFasODQyWA71ERUOuc0s6j1ttNt1htMe0yfqxnYP71caqJ5Fggkmkz2calmIGeBSZJo9e1eGzuZFSxK7+6+C/hhQfjmohtVvpd3tF1LIADgM5xXoXQkA0zpV7x413zr2ykDJCYwB9wT9acwE2sXqdP67awadJK1tDtZyZN+4HxUfLnjxzV9BPFdWyT27h4pF3Kw8xUPr1gj6a13cRxwRR2x3ke+ZONgx8TmqLo6e1n6dt1tHLdmCsgbxV/E/Tnj4VPLwp/Ub8QO0Dnsiy90nx/xSBo31Q3dzbr2ohUlye7sQHxwfpRnUVtLdaxFbAqpmcKrE5GT55+dUem9GX1m+2W7tbq2mjdZ+4Vc5Ugc+eOD9KqdQV5ncq52IOd3Cj1qng1yW703R9NswUmijEI2E95c5YsfQeP3qa1uC4sdSa1uSwnt1VW58DgHj9sV1sLlvbUiR+z7YlWbdgDd/A4Gav0LTr7VtLa2XSdOJ2xSl3MTDYWPPzPJzmsP6c3cltqrWpOYrlDkf8lGQf5qKmR4rlkkyHViGDeIIqq6Hnji1y134y25AT5Eg4/341NnRjjqiOSSaB02YWJj5gnHl48/tRmkdcanaaUIJbVbpbeJgCX2kr5ZPicfejNSMC2kE85gSOOMgybyxyScgjHvfAZpFfWRmtwwAtkxkDblyD6+Q+Q+9EZl1dbySGHUriczzzBS5A4KFFKnPryftSG2CLNIwywVDgEeZGKc6zNN+AaWEl/KKvbTAActEcoc/wDVx9qS28SOe+Ts8wPOrngaNI11IDIyllAGf1Nj1NPenLWafVLVbdGJV1ZmxwoBySTX2mPBAmdqKucBVAJJpp+KtGivH3McptP7/wC8VPKqhHqlxJqN8kaDMURxGhOM88n5n+KP1y7G1FUYDkgkHx4pdNsgcttywY8evNGazDm2Rx5P/IrMAsdtzpF9bS5IhljuVx6ZKN/6X7Uz0jTum5cjULq6g4G0qM5P0HFDdMWfbai8LSpGs8TxHefHcOMfEEA0deaesFh26ahBLgjKRsc/Y1rfgxld22m6Y7mylN5FK35G4e9/jNBXDyZDSvukc97+w+FbRIObu594jbFH6AVrptt7bqAMyhooxlwTj5CimP/Z",
  camus: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQAEMDASIAAhEBAxEB/8QAGwAAAQUBAQAAAAAAAAAAAAAABQADBAYHAgH/xAA0EAACAQMCBAQDCAEFAAAAAAABAgMABBEFEgYhMUETIlFhMoGhFBUjQnGRscHRB1JikuH/xAAUAQEAAAAAAAAAAAAAAAAAAAAA/8QAFBEBAAAAAAAAAAAAAAAAAAAAAP/aAAwDAQACEQMRAD8A9uABnbnl2rmKPdz9V/unLphtfAPLH815bMTGc46D+aA3w2BHfHsfDP8AVC+OeLbnTbr7BYkRyBA7zHmRnsB/dEdLfZd7jjG0inZ+D9O1yJb2/wDGE853kq+ML+Vf2H1oM0ueLNanH4moT7c58jbf4q0cAcWS3l0dK1CZpJGBaCVzknHMqT39RRex4F0O0nuFnDz+KMKkrY2D2I7+9UBNPXS/9RLG0spGaOO9QR7vi2k9/lmg1O9tfEu3kIzkD+Kj3n2aytmnuZEiiX4nc4Aqdqd9ZabbPd386Qxgcix5sfQDufask1jUrziW5a9nJjs4yRBBnko9T6n3/qgtTcYaSrEJHcSKOjhAAf3OaVUpbbyjlilQXm5Plce4pW5wvbotO3dsRuwMHcK48Mqo5elARtD5+RGSO1H4tVaEWUBt2aOVAqyr0DDlg1W4pfAV32/CjH6VP4G1CK701YLjYbi2feAxGcN3GffP70DN7r85vnKWYFqspiMoUyOzDryHQUG1xIYNZ0vX2tQyQ+UuSVw2SdzegC5HPlkipdtPbwy3yzwSJMZd8XjKAx588Y7dDmg/GPEEFvpy2pUSSTL+ICfye/6nH7UEXjKL704tcSzF7SGKMRYOV8wzy/WmbqO3tYFhgUbVGevU/wCKG6FA1/bRhpfCmC+Vs/GB0B+XepFy0kczRTD8ReRH+PagbVGZQQhPvtpUk+EUqDT9ZtFjeP8A58+VVzibxrSGCS2mkjLPtIB5HlnpRrV7lDOI5ZTJOBgrGcKG/Wq1qFyuoy28E5EKpJ5pGbl6enI/Sg40vULm4Z4rgKUCjLqvm5nAqNaTTaVqkV4hRzESrxjo6kncD8v2onqVlb6Npk/hTNLcTlT5gAUUE9vfrVba6LzKEBJcjAHUk9hQENf1zStPlnl0y2LXHhjJMaqke7mFO3v7e1Z9dXE9/O80zs7scu1XXVLO2tYRZIwlC5aWQj43J5n+vlVdWxzdvbqFSNGViVHUdRmgm6FK1tIvTAHwnlj9DVvjsrHV7i3a7kljTO15Isbl5e9VW7iFlaQzDDPKSFHTp3rmz8eaRXMzs2cHDYVT6D1NAXmsolmcWsreAGPh+L8RHYnFKpyxWrqGmJSTGGXPQjtSoHV0vXNLlkGq6fOYOYMsJEgB7HI7U3ZQ2897vE++3gQPcDHmDZICj3yM/pWtzjMmOg9c1U+JtNuby0v00eLwZufiBU2mdsDGG78j1oM74h1hLieTxGVuwJTYRQHT9W+y3Sy8iYgdg6gH1+tPanwrrFpkS6dfL06xFhz91zUTVOHdU0SNmurRnhxu8eLzoB7kcx88UBG41GKYKwkwhGGCtlv/ACoct6NkiwII1I7dT7k96BLOjN0+YNSlYFRt+poD0rtcWFu0jLFCsYWNfzy46n2XOak6aVQKrDB24RCPrTUEly+mWkMcYDbMK+B0BPc/Kn7KIW8zLkSzkcypyE/U9zQancaVpqSAeI8XlU7E08SAZUH4sc6VWm0jU2kO5FJ8NckjPalQB21RJ55IwjRToR+HOhQN67T3NRbiMy3GWWOMbxIA7HDnbjnzqwTQrIGjkRWj/wBrDI/agd5wnod2/iT6bC8gPJm3Ej60HULWqXGVmUSHOY1nJH/XNeytDITtYbmGMgDn7e9NQcPR2Uo+71tbSPGCYrYbyPTcTT33OmPNNOxznO4DP7CgzvjKCxs7xY9T0OzZZM+BPbuFYgYySOWDnt0p/R77hf7MI7jT9PFwv5XhQlx6ggfQ4qw8WcFrr00dz9umhnij2IGUMmM55jkfrVMm4D12yZmjtra6A5hoZcM3ybFAaOvcM3V42mSafAsSsUWQxBF+RByKgappuhwp4uj6ouSc+AWMm72DDp86r8mh6rAds2nXMb482Yjgj5cqk6Fpd7qGoLDaW8jMrDxhjAUZ6kmg3i1ObePGfhFKvLOKb7NHuKocfDjdj50qD//Z",
  montaigne: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQADsDASIAAhEBAxEB/8QAGwAAAQUBAQAAAAAAAAAAAAAABQIDBAYHAQD/xAA3EAACAQIFAQUGBQIHAAAAAAABAgMAEQQFEiExQQYTIlFhFDJxkaGxI0JSgcEz0QcVctLh8PH/xAAZAQADAQEBAAAAAAAAAAAAAAABAgMEAAX/xAAdEQACAgMBAQEAAAAAAAAAAAAAAQIRAyExBBJB/9oADAMBAAIRAxEAPwDO58ZL3snjPvHk+tRzipDyx+dKmsHfbqaYPoKUYdGKf9bfOutiG51Hc8XpmOMyOqILsxsAByat+B7C4qR4RM1i4u+nhfSknkjDoyi3wrIxchW1zb414zsd/wCat3aLsZFgcG02Flcuguyt1qlA2Fr3pYZI5FaOlFx6SUxUqW0uQPjUlMwmCga2+dD1O/FLFrU4BuRrs1/M03qrr++wP6jTZpgBrsiiy9ocIrC9mJA9QDatjhlIC+H4VjHZRRJn+EQsFDsVufVTWjHAFcJh8BNKzx94zPud/Ic8XPF68/1q5o0YuEztDMzYScFd9N7msdYjUwB21GtVxWFGX5RifaJg5Ksq2FrC2wqlZplDyQ4VMHCO8WK7Iq2Pp+9HzSUbQMsb2V4c804G24pkc2PNPDitpAYlGmRl8mP3pNKkF3cjc3NJt50xxoHZLJIUyI5gkHf4yRSyA/ltewHkfWhbYjNMTi+8mx0sWLjY6UEX4URH5T6/tR7/AA7zYf5eMNJpATw2A3t6VYMd2dyfNsWMXKGDEDvFSTSJB0uOp9axTdSdlVwqkWKx3aSFcDHDokU6cTiQ1408yPU9BVnkwmFyvLWWBQGVdmO5vbkmixOX5VhVhgWKKBBYIg2FVLtFnEXs+IhRryyIRHEBd2PA26Drc0kVbpLQW3+mbSsrzyOAAGckfOnFZdI8P1pCYeWRgscbOxNgqi5+VJBsLVuRIdjVRcgHUWO/JAv09acnjdk8drqB14+lKh0pKARfSCx+IH/JrxlLCzH1/iptuyiSoVCzZe6zxSOrruNJtfrvVggz7MfZNaSSWO1hhyxF+fdP/tVrEOWiXqRYfSp3GXL+G/vWsEdSOb7LtSNX056eieM2zHHY/CwEugeVbBgFvv8ApuSRRrMI8NkTYgFEkkSx1/mdmGwJ+G9V3srGJe0OGAjEaIDI1lA469T86kZtO+cZykCH+pLqPpf+y2Hzrmt0COw12Zw0axz5xjY9cpUtHYWK9Bp8iTsPID1oinZfLZQZMRhWkmclpGCjdid/rUmOJIsPHCq2RR3pHkqiyj+f2qcWdQBZuATv1IqP0xmY/r0yKTx4gaSpAlOo+8vh/wC/tXmicq2sEaWJtSSpdBb3kO3wrXQlnHOqMgWIuCL+VSpda5dHdWEZbrifDe3lyfjUVlKqduRfj6feuzOPZowq4cvfc6fFx9qFWBhXsoRho8yxdx4INCkebG396LdksL3082OlGxJRP5Py+9AcO7w5LoPvzzFm6bAWH3NXTJlTCZfDGylSsa3/ANR8TfSwqWS9jx0grBqxBxRXkkRL9AfqWoj3zL4Y1LqNg1uaD5Wzvg4kRAXm/EbUN97kAevJv0FEbS8FoQRt/UH+2ouIT//Z",
  spinoza: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCAA1AFADASIAAhEBAxEB/8QAGwAAAgIDAQAAAAAAAAAAAAAAAwQABgECBQf/xAArEAACAgEDBAIBAgcAAAAAAAABAgADEQQSIQUGMUFRYRMUMiJCcYGRscH/xAAYAQADAQEAAAAAAAAAAAAAAAABAgQAA//EAB0RAAICAgMBAAAAAAAAAAAAAAABAhEDMRIhQTL/2gAMAwEAAhEDEQA/APJFOIRGIBg1HmFRciIMboTCquRgzCKJhEfVakUVnjIEWwmGNanluRMBlb9rePmXXSdiJdUAGLXEZxnAzK53J25qeh2quqG1XGVI5GfiJHJCTpMeWOUVbOWRiCsXMlN24lGOeODMtOggueB9zRj5J8wreYNvBhAMr5h0EAvmMJ6gYUb2HYnHn1N+ku9Wq/LXs3qQQWGR/iA1WdyjHqM9FKrr1VwCG+YH8jLZftF17qtmhTVaVKa33bbLPxblH2ATwDOb3r1W3rHStt7UW2UvzZSpUZ9ggzq9v9QoPTxQtbWDLC1nXCgkk4z79RTvLU1npy6WqtK1J3ttHOcSKNLJVFclcLs80A2sCByPRh1YWfRgmyXIJJx9yDKn0Je0QolinMFjzG3GRmLsMf0gQWHRYwg8QajmGUTMyM3170BHkReqxqb0sA5U8iMPYta5Y4/7Guj6FupautGG1WOT9L8waXYTr9Mt0zK1r6ilKs7vxsDz9cGdyntrVdW0Day/dRphWfwIR/FZjwfpf9ztdudsdJpFepfQ12WZ3KbBuwPXHiWDrPUPx216SsKWZctn0JK2uXR2tuNM8B12ls02odHUjBi2M8AS6d03aXTVBbaRZa2dg8cfMpn5trbtqj6Eri21ZO+mGYHaM+cQLDiFWxbf2n+00fwZkEYHDkTfdtUnHgSSTegF9Ov6jUqLD5Mu/a9KbrDjl2CZ+ATiSSJk0NDZ6hoVAQYHHqV7WWs/WdQ58qCo+gBJJJls6+HkfcOst1nV9U1hwEcoo+AvAnLK+sySS5aJ2aAkNkHBENQ5tVt38p8ySQMKP//Z",
  marcoaurelio: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCABQAD0DASIAAhEBAxEB/8QAGgAAAgMBAQAAAAAAAAAAAAAABgcBAwUEAv/EADAQAAIBAwIEBQMEAwEBAAAAAAECAwQFEQAhBhIxQRMiUWFxBxSBIzJSkUKCobHw/8QAFwEAAwEAAAAAAAAAAAAAAAAAAAECA//EAB4RAAIDAAIDAQAAAAAAAAAAAAABAhEhEjEDIkJR/9oADAMBAAIRAxEAPwBI8upC59NWcup5cdNIqj3RUVRXVUVLSQvNPKwWONBksfQaK7d9MuI61VaSGCk5seWpkwwBOBlQCd+3rrc+mFBDDQPXmhnqrhUVS09II1xgDBYhjsN+p64B7aOJxxhBX+NT26Omo40kLJJUKjOx3JUZ69RnBG49NTyHQqLp9Nr/AECB4Yo61MlW+3JypHqGA/sZ0JywSQyNHNGyOpwysMEH3GnPTcXwtFUfeVFQJoMgFUH6hIJ5SAPMRjcgcvx10P8A1EtdPNSzXTxYWqopkjZolYc6MoZQ4P8AkAeuegx6aSkHEWvJqeXVuNRjVhR6xgDXtAMYbVRJ1GSdTRdja+nNwjpqWjamhkedfEiVS3KhfYnPU9GzkDAGe+im/X/iKSutix00FHSzwSTTTeH4u6ZygzjqAMd99LT6SVNUOLIoIJQFkhk5423WTCnAI9eumBWcbLDXCKa5lLSZwkcqW0hFboRz826jcZ+dZStYGHNxZabjX2Sn4jht0MFXQK61MMYMa1EB351C4OevfpocvtfHJwxXOscbMY/BlaJccvKyhVfBOSN8Nk9u+mDO0FDSvPBcCsc7gsWDyxAj/EkbhSeXPXGffGk5x3eTWMlIY4A6yM7vEMYGSoX36Bid98acdwTzQYEqtvjpqfKd9cwOOmpD41pQlIuHXXsIMZOphQu4VVLMTgADc6KrNwHfrtOiCiamhJ88s23IPXl/cf61LZaRmcJXB7bxDQ1UeVAkCEgdm8p+ev8AzTlqbyiVMVtoLVBOoiJgDxiNf3eZiCDuAeYjG/bbQTFwhFbqukt8hhepnUNmdPPu/KMIc4G2c53GiTjC0XO3VVsrqGaol8FGw5OQjHO4x28xGs3Kwopa6vXVVK4kpknq45Y50idv0ZInyxIOzZCgb++PdJzyNLK8shYs7FiT1JOmpw0DRyTy1VJySRsUwFJeR3P7QP5MSB/Wsq/cKeBW0FJURFppqmOArCfMCwHOB6hWYAf7aPHNWyZRdC8zjrqMjR9d/pjW0Qq5Y6pfAgXmVpEOG3xy5Hf8aAZI3jdkcFWU4IPY63TT6M2muw4+n9l++usVXNJIkML4CQw+LLO+D5ETG+xySdgPkablu4bo6N5paGimpKjmWNZpfJIC2VwCrYA37Y6a5uFobXwzY6i8sQtLEphh8PLNJhsYX+TM23uR6DbVtlVWzIJ7k6RzSTRSNSocpSoGBCe7YYFie/xrOUfVM0vSixWGzzul6pU8S4On6pml8Tz8pT/I52bO+240TVMy0lPBFI0UZYqHeZSOZcDmOBtzf8+dAxjWiu94o2iEsK1cjiMqGyHAkOAdicEnHflJ6jfsEtsNLHNTVs1JSN5XNPXsqc2f4tkD4OMf+RbWDqzetVNBVyNcJqSGMxSt9ose5HbmJ6Zx37Z9dY95o0N8tlTIgLRVEb838MyKqj225z/eim2TU09AiUUkchYAKEcMSP5HHb/7voD46vtJb7SrmY/f1FVHLDEu5WJGxlvTbJ+WPpoaxUFmvxTGJDUwR037givMXbrzrhQvTfqT8DfOlJxPwr99c5ayjl8PxpGLrJGdznqPn8aafHHMkFXUrJgAMsIDYwzeYtjuc8ig9sn10F+PJJK/naXKo4djgkMoO/5J0OTi7CrR0z1stwuFHBVxi30NqTNLRtjmklzyrIQNhudh6K3roksNbTz3i5UfOojihjLM5AHiOWJyfYFB+NA8vEtFfrHDOhWO6U/I0kWWAkZRglgAcjqQe2fbXJwLfhFxBcI6ymKioRmMRwQQOUBcH2/vVvslMO7lUwy3qZZmlRblDG6SxYzFNET5h7gEH4Vu2hDirh5qxDUuhp6xW8OZol8hb15e4I3GPx6a3+InWpiNTbwv3FMy1ECoAN16rj0IyP8AbXQt/pp6elnNOhpqmL9Obl2U/wAG9sYOD039NZybWlJJ4Le18N3eCsXxXqo4XBHNSDlZx6AjcfGNRdLSaWKcDx/DPMqtPkMSBuMHB698aNbnSW+rZnmCFVOGWcEoh9OYZeM+/mX3xrBu9hzEamktU60wjJLJULPEQO4ft+dTzbDiEt2uNVc7lS0sSv4bUpKsVK8waF2kx7AqBrIqoTb54YJG8wo4c5BG+CO/9fjXmnvb2astf3kZkMNM8yzsSdmhBxt8kemQD31Xf70OJKiC5pHNT+JAoxMwbPXoe43I/GnNfQL8P//Z",
  emerson: "data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wBDAAkGBwgHBgkIBwgKCgkLDRYPDQwMDRsUFRAWIB0iIiAdHx8kKDQsJCYxJx8fLT0tMTU3Ojo6Iys/RD84QzQ5Ojf/2wBDAQoKCg0MDRoPDxo3JR8lNzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzc3Nzf/wAARCAAtAFADASIAAhEBAxEB/8QAGgAAAgMBAQAAAAAAAAAAAAAABAUDBgcBAv/EADEQAAIBAwMDAwMDAgcAAAAAAAECAwAEEQUSITFBUQYTYQcUIjJxgRXBI0NScpGh4f/EABcBAQEBAQAAAAAAAAAAAAAAAAIDAQT/xAAgEQADAAIBBAMAAAAAAAAAAAAAAQIDESESIjFRMkFh/9oADAMBAAIRAxEAPwDNumOetF2yqy45714hj3DyfGaY2FozykNgJ5NZxo68eMieMxsVYHOBWnfTvTvsNEa9ghD3d4GbLcBUU4Az4JyT/FU2eFEHCgsAOTxir79PLi4lsnh3RPb20m2QgkSICCcf7c/3qGR7ngrc9KDfV2men9QW3sdWvVhuP1KqybC2OvHSsfvLWKK7uI4CHiSRlRt24FQeDnvxWy+oNRTT7aTVZNPhuUijMYJ/VIG4IDduPg5rIVgCjaq7AOiqOlZi8toGNPYuliXcpzx815MAwGU5JzjijrqNDGcHp3zXI0bC4/SB4ro3wUc8gOwAZz2qW3I35Jr3Om0qeCD3HeooVAYAZJz0otcAqQqxs/cIMZyQOmad2dvELYKzbWyDyc80q0mT2huLYOPFMFuSQoQ7iT4o1tlo1rZzUnEbKWdmdWBx3NA2Gs3mm3S3On3T21yOpXow8Edx8Gu3c8auxYOW/wBTDg/zSWRzIIpBgfkeB1xnipJtnNlydTLTrF96u1jT7rU7XTxb2Fqga89jciXRzy4UnBx1O3+c0n0TVor+N0kHt3Cc7c53D4q/fTj1jAkH9C1mVBFjFtLKfx2n/LYnt4/fFZV6002PQvVt7bWT4ginzCVbOFIDLz+xFOfQJyOH+FhePc2OxzXvZkAISuBxxSiy9QRSxr943tzDjhchh5+Kc293EUDRncmcZB4pPZ1TU14YLNEpjQDnntUMaCOdiw6Dmp/8WS5KQIzMTnCjkf8AlDzOF3/mmSO3OKf0Y2CQzdF3EfNObKRQbYRgMWdlYk9MDNVpDjJ+adaUxF4iHkEhh8fiw/tRv4slF8EutKqQOzAfsarcG5YXkydwbAz1x4p9rk7RyBVHA6fFV12d5pId+MncTjqTUsa7SN+Sa9zJYGaBzhcEMP8Av/ihr+9udbubq4vWVrmUiTKqACQuOg+BU8kX2sbxoxKOMOD3+fg0siZYpwI1IJGCSc5qiAzulPB7yrcOEViAz4ztHc/NbZe+gdFsNGWfR9SvJZbpY/tJZSjQzu3QKAAeR88VQ/o36UsfU/qOdNTLNbWcXvNABxMd2ApPYefNbH9WLW2b6e3wjgSMWYSaFVGFUqwGMDHGCRTc+jYemZ9YaFJdTR2txf2dsqnNxF+SOw5I4kxk9qQ63pFxptnLLNNZh4mIYifJHgbevPFLj6/9Ry2qW7X7+yihFTJIAAx3pLc6tc3lybm7Ec85IzLKu9j45JzW6Zasp//Z",
};

// ===== FRASE DEL DÍA =====
var FRASES = [
  {t:"La vida sin examen no merece la pena ser vivida.", a:"Sócrates"},
  {t:"Pienso, luego existo.", a:"Descartes"},
  {t:"El conocimiento es la única cosa que nadie puede quitarte.", a:"Platón"},
  {t:"Atrévete a saber. Ten el valor de usar tu propia razón.", a:"Kant"},
  {t:"Lo que no te destruye te hace más fuerte.", a:"Nietzsche"},
  {t:"El ser humano es por naturaleza un animal político.", a:"Aristóteles"},
  {t:"Solo sé que no sé nada.", a:"Sócrates"},
  {t:"Dios ha muerto. Nosotros lo hemos matado.", a:"Nietzsche"},
  {t:"La razón es y solo puede ser la esclava de las pasiones.", a:"Hume"},
  {t:"Quien tiene un porqué puede soportar casi cualquier cómo.", a:"Nietzsche"},
  {t:"Actúa solo según la máxima que puedas querer como ley universal.", a:"Kant"},
  {t:"La virtud es el término medio entre dos extremos viciosos.", a:"Aristóteles"},
  {t:"Si el mundo fuera claro, el arte no existiría.", a:"Camus"},
  {t:"El hombre está condenado a ser libre.", a:"Sartre"},
  {t:"El hombre sufre más por lo que imagina que por lo que ocurre.", a:"Montaigne"},
  {t:"Afronta cada lección como si fuera la última.", a:"Marco Aurelio"},
  {t:"El amor no es otra cosa que la alegría acompañada de una causa exterior.", a:"Spinoza"},
  {t:"Un libro debe ser el hacha que rompa el mar helado dentro de nosotros.", a:"Kafka"},
  {t:"La suerte se entrena. Prepárate para que la oportunidad te encuentre listo.", a:"Séneca"},
  {t:"No hay viento favorable para quien no sabe a dónde va.", a:"Séneca"},
  {t:"La educación es el arma más poderosa para cambiar el mundo.", a:"Mandela"},
  {t:"Un camino de mil millas comienza con un solo paso.", a:"Lao-Tse"},
  {t:"Somos lo que hacemos repetidamente. La excelencia es un hábito.", a:"Aristóteles"},
  {t:"Conocerte a ti mismo es el principio de toda sabiduría.", a:"Aristóteles"},
  {t:"La filosofía comienza con el asombro.", a:"Platón"},
  {t:"Los límites de mi lenguaje son los límites de mi mundo.", a:"Wittgenstein"},
  {t:"Todo lo real es racional; todo lo racional es real.", a:"Hegel"},
  {t:"La verdad es hija del tiempo, no de la autoridad.", a:"Francis Bacon"},
  {t:"El ignorante afirma, el sabio duda y reflexiona.", a:"Aristóteles"},
  {t:"La imaginación es más importante que el conocimiento.", a:"Einstein"},
  {t:"No hay camino hacia la paz; la paz es el camino.", a:"Gandhi"},
  {t:"Cada concepto que aprendes hoy es una herramienta para toda la vida.", a:"Anónimo"},
  {t:"Estudiar filosofía es aprender a dudar, a preguntar y a no conformarse.", a:"Anónimo"},
  {t:"La PAU no define quién eres, sino de lo que eres capaz.", a:"Anónimo"},
  {t:"El dolor de estudiar es temporal. El de no saber dura toda la vida.", a:"Anónimo"},
  {t:"Lo que sabemos es una gota; lo que ignoramos es un océano.", a:"Newton"},
  {t:"Nunca consideres el estudio como una obligación, sino como una oportunidad.", a:"Einstein"},
  {t:"Invertir en conocimiento paga siempre el mejor interés.", a:"Benjamin Franklin"},
  {t:"La angustia es el vértigo de la libertad.", a:"Kierkegaard"},
  {t:"Ante el absurdo, hay que imaginar a Sísifo feliz.", a:"Camus"},
  {t:"La vida es una constante oscilación entre el dolor y el aburrimiento.", a:"Schopenhauer"},
  {t:"La gente te amará como puede, no como quieres.", a:"Anónimo"},
  {t:"Haz hoy lo que otros no harán, y mañana tendrás lo que otros no tienen.", a:"Jerry Rice"},
  {t:"El hombre no está hecho para la derrota. Puede ser destruido, pero no derrotado.", a:"Hemingway"},
  {t:"Toda nuestra dignidad consiste en el pensamiento.", a:"Pascal"},
  {t:"El hombre es libre, pero en todas partes está encadenado.", a:"Rousseau"},
  {t:"Cometer un error y no corregirlo: eso sí es error.", a:"Confucio"},
  {t:"Cuida tus hábitos, pues se convertirán en carácter.", a:"Aristóteles"},
  {t:"El lenguaje es la casa del ser.", a:"Heidegger"},
];
var _fraseExtra = 0;

function mostrarFraseDia() {
  var hoy = new Date();
  var dia = Math.floor((hoy - new Date(hoy.getFullYear(), 0, 0)) / 864e5);
  var idx = (dia + _fraseExtra) % FRASES.length;
  var f = FRASES[idx];
  var dias = ["Domingo","Lunes","Martes","Miércoles","Jueves","Viernes","Sábado"];
  var meses = ["enero","febrero","marzo","abril","mayo","junio","julio","agosto","septiembre","octubre","noviembre","diciembre"];
  var lbl = document.getElementById("fraseLabel");
  var txt = document.getElementById("fraseTexto");
  var aut = document.getElementById("fraseAutorQ");
  if (lbl) lbl.textContent = dias[hoy.getDay()] + " " + hoy.getDate() + " de " + meses[hoy.getMonth()] + " · Frase del día";
  if (txt) {
    txt.style.opacity = "0";
    setTimeout(function() {
      txt.textContent = "\u201c" + f.t + "\u201d";
      if (aut) aut.textContent = "\u2014 " + f.a;
      txt.style.transition = "opacity 0.4s";
      txt.style.opacity = "1";
    }, 150);
  }
}
function siguienteFrase() {
  _fraseExtra = (_fraseExtra + 1) % FRASES.length;
  mostrarFraseDia();
}

// ===== BUSCADOR (FIX) =====
// Patch: replace toString bug with index-based approach
var _origBuscarFilo = window.buscarFilo;
window.buscarFilo = function(q) {
  var btn = document.getElementById("buscadorClear");
  var sugs = document.getElementById("sugerenciasRapidas");
  var res = document.getElementById("buscadorResultados");
  if (btn) btn.style.display = q ? "block" : "none";
  if (sugs) sugs.style.display = q ? "none" : "flex";
  if (!q.trim()) { if (res) res.innerHTML = ""; return; }
  var query = q.toLowerCase().trim();
  var results = [];
  if (typeof searchIndex !== "undefined") {
    for (var i = 0; i < searchIndex.length; i++) {
      var item = searchIndex[i];
      if ((item.titulo && item.titulo.toLowerCase().indexOf(query) >= 0) ||
          (item.subtitulo && item.subtitulo.toLowerCase().indexOf(query) >= 0) ||
          (item.texto && item.texto.toLowerCase().indexOf(query) >= 0)) {
        results.push({item: item, idx: i});
        if (results.length >= 8) break;
      }
    }
  }
  if (!results.length) {
    if (res) res.innerHTML = "<div style=\"text-align:center;padding:2rem;color:var(--text3)\"><div style=\"font-size:2rem;margin-bottom:0.5rem\">🔭</div><p>Sin resultados para <strong>" + q + "</strong>.</p></div>";
    return;
  }
  var html = results.map(function(r) {
    var item = r.item;
    var col = {autor:"var(--gold)",concepto:"var(--teal)",corriente:"var(--blue)",sección:"var(--purple)"}[item.tipo] || "var(--text2)";
    var bg = {autor:"var(--gold-dim)",concepto:"var(--teal-dim)",corriente:"var(--blue-dim)",sección:"var(--purple-dim)"}[item.tipo] || "var(--card2)";
    return "<div class=\"search-result\" onclick=\"searchIndex[" + r.idx + "].accion();document.getElementById('buscadorInput').blur();\">"
      + "<div class=\"search-result-icon\">" + (item.icon || "📖") + "</div>"
      + "<div class=\"search-result-body\">"
      + "<div class=\"search-result-title\">" + item.titulo + "</div>"
      + "<div class=\"search-result-subtitle\">" + item.subtitulo + "</div>"
      + "<div class=\"search-result-excerpt\">" + (item.texto || "").split(" ").slice(0,10).join(" ") + "…</div>"
      + "</div>"
      + "<span class=\"search-result-type\" style=\"background:" + bg + ";color:" + col + "\">" + item.tipo + "</span>"
      + "</div>";
  }).join("");
  if (res) res.innerHTML = html;
};

// ===== VÍDEOS =====
var VNOMBRES = {
  kant:"Kant", nietzsche:"Nietzsche", camus:"Camus", montaigne:"Montaigne",
  marcoaurelio:"Marco Aurelio", kafka:"Kafka", schopenhauer:"Schopenhauer",
  spinoza:"Spinoza", seneca:"Séneca", maquiavelo:"Maquiavelo", emerson:"Emerson", wilde:"Oscar Wilde"
};
var VCAT_COLOR = {filosofo:"#c9a84c", reflexion:"#a78bfa", arte:"#3ecfb2", web:"#5b8dee"};
var VCAT_LABEL = {filosofo:"👤 Filósofos", reflexion:"💭 Reflexión", arte:"🎨 Arte", web:"🌐 Mi Web"};
var VRED_BG = {tiktok:"#010101", instagram:"linear-gradient(135deg,#833ab4,#fd1d1d,#fcb045)"};

var VIDEOS = [
  {cat:"filosofo",autor:"kant",red:"tiktok",titulo:"Crítica de la Razón Pura — Kant",desc:"Fenómenos, noúmenos y estructuras a priori. Clave para la PAU.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648372615500926230"},
  {cat:"filosofo",autor:"nietzsche",red:"tiktok",titulo:"Nietzsche: los que bailaban eran vistos como locos",desc:"El pensamiento propio frente a la incomprensión social.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647500022803696918"},
  {cat:"filosofo",autor:"nietzsche",red:"tiktok",titulo:"¿Qué plantea Nietzsche sobre el cuerpo y el pensamiento?",desc:"El pensamiento como expresión de fuerzas fisiológicas e instintos.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648377661504507158"},
  {cat:"filosofo",autor:"nietzsche",red:"instagram",titulo:"Nietzsche: pensar por uno mismo aunque seas incomprendido",desc:"Gran parte de su obra cuestiona las normas sociales.",url:"https://www.instagram.com/reel/DZKY4iXMXwg/"},
  {cat:"filosofo",autor:"camus",red:"tiktok",titulo:"Albert Camus: Si el mundo fuera claro, el arte no existiría (P.1)",desc:"La filosofía del absurdo y el arte como respuesta.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647487188719963414"},
  {cat:"filosofo",autor:"camus",red:"tiktok",titulo:"Albert Camus: filosofía del absurdo (P.2)",desc:"Continuación: la creación como respuesta al absurdo.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647490855665716502"},
  {cat:"filosofo",autor:"camus",red:"tiktok",titulo:"Camus: ¿Es inmoral ser feliz en un mundo injusto?",desc:"Provocación filosófica perfecta para la valoración personal.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648378609928932630"},
  {cat:"filosofo",autor:"camus",red:"instagram",titulo:"Camus: el arte como respuesta al absurdo",desc:"Con contexto histórico y aplicación filosófica para la PAU.",url:"https://www.instagram.com/reel/DZLnE2Nsez4/"},
  {cat:"filosofo",autor:"montaigne",red:"tiktok",titulo:"Montaigne: El que teme sufrir, ya sufre el miedo (P.4)",desc:"La anticipación del sufrimiento y la mente humana.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647576623654505750"},
  {cat:"filosofo",autor:"montaigne",red:"tiktok",titulo:"Montaigne: El hombre sufre más por lo que imagina",desc:"Nuestros pensamientos nos causan más dolor que la realidad.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648247757530058006"},
  {cat:"filosofo",autor:"montaigne",red:"instagram",titulo:"Montaigne: El hombre sufre más por lo que imagina",desc:"Padre del ensayo moderno. Psicología filosófica avant la lettre.",url:"https://www.instagram.com/reel/DZPlBSLsDOm/"},
  {cat:"filosofo",autor:"montaigne",red:"instagram",titulo:"Montaigne: El que teme sufrir ya sufre el miedo",desc:"Sus escritos sobre el miedo y la naturaleza humana.",url:"https://www.instagram.com/reel/DZK7xGVM69R/"},
  {cat:"filosofo",autor:"marcoaurelio",red:"tiktok",titulo:"Marco Aurelio: Afronta cada lección como si fuera la última",desc:"Estoicismo puro: los obstáculos son parte del camino.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647523013545577750"},
  {cat:"filosofo",autor:"marcoaurelio",red:"instagram",titulo:"Marco Aurelio: estoicismo para la vida real",desc:"Las dificultades como oportunidades de crecimiento.",url:"https://www.instagram.com/reel/DZKizOOs8pY/"},
  {cat:"filosofo",autor:"kafka",red:"tiktok",titulo:"Kafka: Un libro debe ser el hacha que rompa el mar helado",desc:"La literatura no entretiene: transforma.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647628372041944342"},
  {cat:"filosofo",autor:"kafka",red:"tiktok",titulo:"Kafka: la historia de sus manuscritos condenados",desc:"Pidió que quemaran todo. Max Brod lo desobedeció.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648947714952088854"},
  {cat:"filosofo",autor:"kafka",red:"instagram",titulo:"Kafka: la historia de sus obras condenadas",desc:"Sin la traición de Max Brod no existiría La metamorfosis.",url:"https://www.instagram.com/reel/DZUa1R9sRoE/"},
  {cat:"filosofo",autor:"schopenhauer",red:"tiktok",titulo:"Schopenhauer: La vida oscila entre el dolor y el aburrimiento",desc:"El pesimismo filosófico y el deseo como sufrimiento.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647834158672153878"},
  {cat:"filosofo",autor:"schopenhauer",red:"instagram",titulo:"Schopenhauer y su caniche Atma",desc:"El destino baraja las cartas, pero nosotros las jugamos.",url:"https://www.instagram.com/reel/DZL3xEYiWu0/"},
  {cat:"filosofo",autor:"spinoza",red:"tiktok",titulo:"Spinoza: El amor es alegría acompañada de una causa exterior",desc:"La filosofía del amor según Spinoza.",url:"https://www.tiktok.com/@filosofeando_para_aproba/photo/7649118707922373910"},
  {cat:"filosofo",autor:"spinoza",red:"instagram",titulo:"Spinoza: el amor como forma de alegría",desc:"Una definición filosófica del amor que lo cambia todo.",url:"https://www.instagram.com/reel/DZVm4yHRHEe/"},
  {cat:"filosofo",autor:"seneca",red:"tiktok",titulo:"Séneca: la suerte se entrena",desc:"Prepárate para que la oportunidad te encuentre listo.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647863549770943766"},
  {cat:"filosofo",autor:"seneca",red:"instagram",titulo:"Séneca: prepárate para que la oportunidad te encuentre",desc:"Estoicismo aplicado a la vida cotidiana.",url:"https://www.instagram.com/reel/DZM45DSMlX3/"},
  {cat:"filosofo",autor:"maquiavelo",red:"instagram",titulo:"Maquiavelo: la astucia como virtud superior",desc:"Los seres humanos no actuamos por benevolencia sino por interés.",url:"https://www.instagram.com/reel/DZNI8vMMRYX/"},
  {cat:"filosofo",autor:"wilde",red:"instagram",titulo:"Oscar Wilde: el arte no debe copiar la realidad",desc:"Las artes se inspiran unas en otras, no en la vida.",url:"https://www.instagram.com/reel/DZNYTb0sywk/"},
  {cat:"reflexion",autor:"",red:"tiktok",titulo:"Reflexión P.1 — Filosofía para vivir",desc:"Reflexión sobre el pensamiento filosófico y la vida.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647361372505804054"},
  {cat:"reflexion",autor:"",red:"tiktok",titulo:"Heráclito y el cambio — Reflexión P.2",desc:"No puedes bañarte dos veces en el mismo río.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647348624413691158"},
  {cat:"reflexion",autor:"",red:"tiktok",titulo:"Tales de Mileto: la verdadera batalla es interior",desc:"Reconocer cuándo el ego nos gana es el primer paso.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647835017099431190"},
  {cat:"reflexion",autor:"",red:"tiktok",titulo:"Hemingway: el hombre no está hecho para la derrota",desc:"Un hombre puede ser destruido, pero no derrotado.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647933708355292438"},
  {cat:"reflexion",autor:"",red:"tiktok",titulo:"La noche no trae respuestas, solo preguntas",desc:"Los pensamientos que callamos durante el día.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648466200313236758"},
  {cat:"reflexion",autor:"",red:"instagram",titulo:"La tormenta siempre pasa — Nunca dejes de confiar en ti",desc:"La constancia y la disciplina te llevan a lo más alto.",url:"https://www.instagram.com/reel/DZTiqmNiBft/"},
  {cat:"reflexion",autor:"",red:"instagram",titulo:"La gente te amará como puede, no como quieres",desc:"El único amor a tu gusto es el que te brindes a ti mismo.",url:"https://www.instagram.com/reel/DZSfptrMQAq/"},
  {cat:"reflexion",autor:"",red:"instagram",titulo:"La noche no trae respuestas, solo preguntas",desc:"Reflexión nocturna sobre la introspección.",url:"https://www.instagram.com/reel/DZRFxuYCeCP/"},
  {cat:"arte",autor:"",red:"tiktok",titulo:"La Mona Lisa — ¿Por qué es tan famosa?",desc:"El sfumato, la sonrisa y el robo de 1911.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648341588166364438"},
  {cat:"arte",autor:"",red:"tiktok",titulo:"Salvator Mundi — Leonardo da Vinci",desc:"La esfera que no distorsiona. Simbolismo y percepción.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648107788752784662"},
  {cat:"arte",autor:"",red:"tiktok",titulo:"Daniel en el foso de los leones — Rubens",desc:"Tensión contenida: los leones no actúan.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647975213841288450"},
  {cat:"arte",autor:"",red:"instagram",titulo:"La Mona Lisa — Misterio y sfumato",desc:"La mirada que te sigue y el fondo irreal.",url:"https://www.instagram.com/reel/DZQPXxisxul/"},
  {cat:"arte",autor:"",red:"instagram",titulo:"Salvator Mundi — Simbolismo y percepción",desc:"Control, percepción y realidad en Da Vinci.",url:"https://www.instagram.com/reel/DZOmSxfi9Dk/"},
  {cat:"web",autor:"",red:"tiktok",titulo:"He creado la web de Filosofía que me habría ahorrado horas",desc:"Autores PAU, juegos, simulacros, flashcards. Todo gratis.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7647434603548003606"},
  {cat:"web",autor:"",red:"tiktok",titulo:"Plataforma GRATUITA PAU Filosofía Andalucía",desc:"Tests, flashcards, simulacros y exámenes anteriores.",url:"https://www.tiktok.com/@filosofeando_para_aproba/video/7648736661001784579"},
  {cat:"web",autor:"",red:"instagram",titulo:"Bienvenido a Filosofeando",desc:"Piensa menos como todos. Piensa más por ti mismo.",url:"https://www.instagram.com/p/DZJhNfcCSLP/"},
  {cat:"web",autor:"",red:"instagram",titulo:"Plataforma GRATUITA PAU Filosofía Andalucía",desc:"Tests, flashcards, simulacros y exámenes anteriores.",url:"https://www.instagram.com/reel/DZS9--pR7e4/"},
];

var _vFiltro = "todos";
var _vAutor = "";

function vFiltrar(f, btn) {
  _vFiltro = f;
  _vAutor = "";
  document.querySelectorAll("#vTabBar .tab-btn").forEach(function(b) {
    b.style.background = ""; b.style.borderColor = ""; b.style.color = "";
  });
  if (btn) { btn.style.background = "var(--gold-dim)"; btn.style.borderColor = "var(--gold)"; btn.style.color = "var(--gold)"; }
  vRenderAvatares();
  vRender();
}

function vFiltrarAutor(a) {
  _vAutor = _vAutor === a ? "" : a;
  vRenderAvatares();
  vRender();
}

function vRenderAvatares() {
  var el = document.getElementById("vAvatares");
  if (!el) return;
  var show = _vFiltro === "todos" || _vFiltro === "filosofo";
  el.style.display = show ? "flex" : "none";
  if (!show) return;
  var autores = [];
  for (var i = 0; i < VIDEOS.length; i++) {
    var v = VIDEOS[i];
    if (v.cat === "filosofo" && v.autor && autores.indexOf(v.autor) < 0) autores.push(v.autor);
  }
  el.innerHTML = autores.map(function(a) {
    var sel = _vAutor === a;
    var n = VNOMBRES[a] || a;
    var cnt = VIDEOS.filter(function(v) { return v.autor === a; }).length;
    var foto = FOTOS[a];
    var av = foto
      ? "<img src=\"" + foto + "\" alt=\"" + n + "\" style=\"width:100%;height:100%;object-fit:cover;border-radius:50%\" onerror=\"this.style.display='none'\">"
      : "<span style=\"font-weight:800;color:#c9a84c\">" + n[0] + "</span>";
    return "<button onclick=\"vFiltrarAutor('" + a + "')\" style=\"display:flex;flex-direction:column;align-items:center;gap:0.25rem;background:none;border:none;cursor:pointer;padding:0.2rem;opacity:" + (sel || !_vAutor ? 1 : 0.35) + "\">"
      + "<div style=\"width:46px;height:46px;border-radius:50%;overflow:hidden;border:2.5px solid " + (sel ? "#c9a84c" : "var(--border)") + ";display:flex;align-items:center;justify-content:center;background:var(--card2)\">" + av + "</div>"
      + "<span style=\"font-size:0.6rem;color:" + (sel ? "#c9a84c" : "var(--text3)") + ";font-weight:" + (sel ? 700 : 400) + ";max-width:52px;text-align:center;line-height:1.2\">" + n + "</span>"
      + "</button>";
  }).join("");
}

function vRender() {
  var el = document.getElementById("vGrid");
  if (!el) return;
  var lista = VIDEOS;
  if (_vFiltro === "filosofo") lista = lista.filter(function(v) { return v.cat === "filosofo"; });
  else if (_vFiltro === "reflexion") lista = lista.filter(function(v) { return v.cat === "reflexion"; });
  else if (_vFiltro === "arte") lista = lista.filter(function(v) { return v.cat === "arte"; });
  else if (_vFiltro === "web") lista = lista.filter(function(v) { return v.cat === "web"; });
  else if (_vFiltro === "tiktok") lista = lista.filter(function(v) { return v.red === "tiktok"; });
  else if (_vFiltro === "instagram") lista = lista.filter(function(v) { return v.red === "instagram"; });
  if (_vAutor) lista = lista.filter(function(v) { return v.autor === _vAutor; });
  if (!lista.length) { el.innerHTML = "<p style=\"text-align:center;color:var(--text3);padding:1.5rem\">Sin vídeos para este filtro.</p>"; return; }

  var cats = _vFiltro === "todos" ? ["filosofo","reflexion","arte","web"] : [_vFiltro.replace("tiktok","mix").replace("instagram","mix")];
  var html = "";
  cats.forEach(function(cat) {
    var items = lista.filter(function(v) { return _vFiltro === "todos" ? v.cat === cat : true; });
    if (_vFiltro !== "todos") items = lista;
    if (!items.length) return;
    var col = VCAT_COLOR[cat] || "#c9a84c";
    if (_vFiltro === "todos") {
      html += "<div style=\"display:flex;align-items:center;gap:0.5rem;margin:1rem 0 0.5rem\">"
        + "<span style=\"width:12px;height:2px;background:" + col + ";display:block;border-radius:2px\"></span>"
        + "<span style=\"font-size:0.68rem;font-weight:800;text-transform:uppercase;letter-spacing:0.09em;color:" + col + "\">" + (VCAT_LABEL[cat] || cat) + "</span>"
        + "<span style=\"flex:1;height:1px;background:var(--border);display:block\"></span>"
        + "<span style=\"font-size:0.68rem;color:var(--text3)\">" + items.length + " vídeos</span></div>";
    }
    items.forEach(function(v) {
      var col2 = VCAT_COLOR[v.cat] || "#c9a84c";
      var foto = FOTOS[v.autor];
      var nom = VNOMBRES[v.autor] || (v.cat === "reflexion" ? "Reflexión" : v.cat === "arte" ? "Arte" : "Mi Web");
      var av = foto
        ? "<img src=\"" + foto + "\" alt=\"" + nom + "\" style=\"width:100%;height:100%;object-fit:cover;border-radius:50%\" onerror=\"this.style.display='none'\">"
        : "<span style=\"font-size:0.9rem\">" + (v.cat==="reflexion" ? "💭" : v.cat==="arte" ? "🎨" : "🌐") + "</span>";
      var rbg = VRED_BG[v.red] || "#010101";
      var rl = v.red === "tiktok" ? "TikTok" : "IG";
      html += "<a href=\"" + v.url + "\" target=\"_blank\" rel=\"noopener\" "
        + "style=\"display:flex;gap:0.85rem;align-items:center;background:var(--card);border:1px solid var(--border);border-left:3px solid " + col2 + ";border-radius:var(--radius-sm);padding:0.85rem;text-decoration:none;color:inherit;transition:transform 0.18s\" "
        + "onmouseover=\"this.style.transform='translateX(3px)'\" onmouseout=\"this.style.transform=''\"> "
        + "<div style=\"width:38px;height:38px;border-radius:50%;overflow:hidden;flex-shrink:0;border:1.5px solid " + col2 + "55;display:flex;align-items:center;justify-content:center;background:var(--bg3)\">" + av + "</div>"
        + "<div style=\"flex:1;min-width:0\">"
        + "<div style=\"display:flex;align-items:center;gap:0.35rem;margin-bottom:0.2rem\">"
        + "<span style=\"font-size:0.64rem;font-weight:700;color:" + col2 + "\">" + nom + "</span>"
        + "<span style=\"font-size:0.62rem;font-weight:700;padding:1px 6px;border-radius:50px;background:" + rbg + ";color:#fff\">" + rl + "</span>"
        + "</div>"
        + "<div style=\"font-weight:600;font-size:0.84rem;line-height:1.35;overflow:hidden;white-space:nowrap;text-overflow:ellipsis\">" + v.titulo + "</div>"
        + "<div style=\"font-size:0.75rem;color:var(--text3);overflow:hidden;white-space:nowrap;text-overflow:ellipsis;margin-top:0.12rem\">" + v.desc + "</div>"
        + "</div><span style=\"flex-shrink:0;color:" + col2 + ";font-size:0.8rem\">▶</span></a>";
    });
    if (_vFiltro !== "todos") return;
  });
  el.innerHTML = html;
}

// ===== PROGRESO =====
var STO = {
  get: function(k) { try { return JSON.parse(localStorage.getItem("filo_" + k)); } catch(e) { return null; } },
  set: function(k, v) { localStorage.setItem("filo_" + k, JSON.stringify(v)); }
};
function getProg() { return STO.get("prog") || {tests:0,notas:[],juegos:0,autores:[],dias:[],xp:0,iaUsos:0}; }
function saveProg(p) { STO.set("prog", p); }

function addXP(n, msg) {
  var p = getProg(); p.xp = (p.xp || 0) + n; saveProg(p);
  renderNivel(p.xp);
  var t = document.createElement("div");
  t.textContent = "+" + n + " XP · " + msg;
  t.style.cssText = "position:fixed;bottom:6rem;left:50%;transform:translateX(-50%);background:#c9a84c;color:#0d0f14;padding:0.4rem 1.2rem;border-radius:50px;font-weight:700;font-size:0.8rem;z-index:900;pointer-events:none";
  document.body.appendChild(t);
  setTimeout(function() { t.remove(); }, 2000);
}

function registrarDia() {
  var p = getProg(), hoy = new Date().toDateString();
  if (!p.dias) p.dias = [];
  if (p.dias.indexOf(hoy) < 0) { p.dias.push(hoy); saveProg(p); addXP(10, "Día de estudio"); }
}

function calcRacha(dias) {
  if (!dias || !dias.length) return 0;
  var sorted = dias.map(function(d) { return new Date(d); }).sort(function(a,b) { return b-a; });
  var hoy = new Date(); hoy.setHours(0,0,0,0);
  var ayer = new Date(hoy); ayer.setDate(ayer.getDate()-1);
  if (sorted[0].toDateString() !== hoy.toDateString() && sorted[0].toDateString() !== ayer.toDateString()) return 0;
  var racha = 1;
  for (var i = 1; i < sorted.length; i++) {
    if (Math.round((sorted[i-1]-sorted[i])/864e5) === 1) racha++;
    else break;
  }
  return racha;
}

var NIVELES = [
  {min:0,max:50,num:1,n:"Novato Filosófico"},
  {min:50,max:150,num:2,n:"Aprendiz de Sócrates"},
  {min:150,max:300,num:3,n:"Discípulo de Platón"},
  {min:300,max:500,num:5,n:"Seguidor de Aristóteles"},
  {min:500,max:800,num:8,n:"Racionalista Cartesiano"},
  {min:800,max:1200,num:12,n:"Escéptico de Hume"},
  {min:1200,max:1800,num:18,n:"Kantiano Crítico"},
  {min:1800,max:2500,num:25,n:"Sócrates"},
  {min:2500,max:4000,num:35,n:"Aristóteles"},
  {min:4000,max:1e9,num:50,n:"Filósofo Supremo"},
];
function renderNivel(xp) {
  var nv = NIVELES[0];
  for (var i = 0; i < NIVELES.length; i++) { if (xp >= NIVELES[i].min && xp < NIVELES[i].max) { nv = NIVELES[i]; break; } }
  var next = NIVELES[NIVELES.indexOf(nv)+1];
  var pct = next ? Math.round((xp-nv.min)/(next.min-nv.min)*100) : 100;
  var g = function(id) { return document.getElementById(id); };
  if (g("nivelNum")) g("nivelNum").textContent = nv.num;
  if (g("nivelNombre")) g("nivelNombre").textContent = nv.n;
  if (g("nivelXP")) g("nivelXP").textContent = xp + " XP";
  if (g("nivelBar")) g("nivelBar").style.width = pct + "%";
  if (g("nivelProx")) g("nivelProx").textContent = next ? "Próximo: " + next.n + " (" + next.min + " XP)" : "🏆 Nivel máximo";
}

// ===== LOGROS =====
var LOGROS = [
  {id:"d1",i:"🎯",n:"Primer día",d:"Visita la web",check:function(p){return (p.dias||[]).length>=1;},xp:10},
  {id:"a1",i:"📚",n:"Primer autor",d:"Estudia un autor PAU",check:function(p){return (p.autores||[]).length>=1;},xp:30},
  {id:"a7",i:"🌍",n:"Currículo completo",d:"Estudia los 7 autores",check:function(p){return (p.autores||[]).length>=7;},xp:300},
  {id:"r3",i:"🔥",n:"3 días seguidos",d:"Racha de 3 días",check:function(p){return calcRacha(p.dias||[])>=3;},xp:60},
  {id:"r7",i:"💪",n:"Semana filosófica",d:"Racha de 7 días",check:function(p){return calcRacha(p.dias||[])>=7;},xp:150},
  {id:"ia1",i:"🤖",n:"Amigo de la IA",d:"Usa el corrector de IA",check:function(p){return (p.iaUsos||0)>=1;},xp:40},
];

function verificarLogros(p) {
  var desbloqueados = STO.get("logros") || [];
  LOGROS.forEach(function(l) {
    if (desbloqueados.indexOf(l.id) < 0 && l.check(p)) {
      desbloqueados.push(l.id);
      STO.set("logros", desbloqueados);
      addXP(l.xp, "🏆 " + l.n);
      var t = document.createElement("div");
      t.innerHTML = "<div style=\"font-size:1.4rem\">" + l.i + "</div><div><strong>¡Logro!</strong><br><span style=\"font-size:0.75rem\">" + l.n + "</span></div>";
      t.style.cssText = "position:fixed;top:80px;right:1rem;background:var(--card);border:2px solid #c9a84c;border-radius:12px;padding:0.75rem 1rem;display:flex;gap:0.65rem;align-items:center;z-index:901;box-shadow:0 8px 32px rgba(0,0,0,0.4);max-width:230px";
      document.body.appendChild(t);
      setTimeout(function() { t.remove(); }, 4000);
    }
  });
  renderLogros();
}

function renderLogros() {
  var grid = document.getElementById("logrosGrid");
  if (!grid) return;
  var desbloqueados = STO.get("logros") || [];
  grid.innerHTML = LOGROS.map(function(l) {
    var ok = desbloqueados.indexOf(l.id) >= 0;
    return "<div style=\"background:var(--card);border:1px solid " + (ok ? "rgba(201,168,76,0.5)" : "var(--border)") + ";border-radius:var(--radius-sm);padding:0.85rem;display:flex;gap:0.65rem;align-items:center;opacity:" + (ok ? 1 : 0.4) + "\">"
      + "<div style=\"font-size:1.4rem;filter:" + (ok ? "none" : "grayscale(1)") + "\">" + l.i + "</div>"
      + "<div><div style=\"font-weight:700;font-size:0.82rem;color:" + (ok ? "#c9a84c" : "var(--text)") + "\">" + l.n + "</div>"
      + "<div style=\"font-size:0.72rem;color:var(--text3)\">" + l.d + "</div>"
      + "<div style=\"font-size:0.68rem;color:var(--text3);margin-top:0.15rem\">+" + l.xp + " XP · " + (ok ? "✅ Desbloqueado" : "🔒 Bloqueado") + "</div></div></div>";
  }).join("");
}

// ===== IA CORRECTORA =====
var _iaTipo = "1c";
function iaSetTipo(t) {
  _iaTipo = t;
  var b1 = document.getElementById("btn1c");
  var b2 = document.getElementById("btn2b");
  if (b1) { b1.style.background = t==="1c" ? "var(--teal-dim)" : "var(--card2)"; b1.style.borderColor = t==="1c" ? "var(--teal)" : "var(--border)"; b1.style.color = t==="1c" ? "var(--teal)" : "var(--text2)"; }
  if (b2) { b2.style.background = t==="2b" ? "var(--teal-dim)" : "var(--card2)"; b2.style.borderColor = t==="2b" ? "var(--teal)" : "var(--border)"; b2.style.color = t==="2b" ? "var(--teal)" : "var(--text2)"; }
}

async function iaCorregir() {
  var autor = (document.getElementById("iaAutor") || {}).value || "Kant";
  var resp = ((document.getElementById("iaResp") || {}).value || "").trim();
  var btn = document.getElementById("iaBtn");
  var res = document.getElementById("iaResult");
  if (resp.split(/\s+/).filter(Boolean).length < 20) {
    if (res) res.innerHTML = "<div style=\"background:var(--red-dim);border:1px solid var(--red);border-radius:var(--radius-sm);padding:0.75rem;color:var(--red)\">✍️ Escribe al menos 20 palabras.</div>";
    return;
  }
  if (btn) { btn.textContent = "⏳ Analizando…"; btn.disabled = true; }
  if (res) res.innerHTML = "<div style=\"text-align:center;padding:1.5rem;color:var(--text3)\">🤖 Analizando tu respuesta…</div>";
  var prompt = "Eres profesor de filosofía PAU Andalucía. El alumno responde a la pregunta " + (_iaTipo === "1c" ? "1c (posición filosófica)" : "2b (valoración personal)") + " sobre " + autor + ".\n\nRESPUESTA: \"" + resp + "\"\n\nDevuelve SOLO JSON sin markdown:\n{\"notaEstimada\":0.0,\"correctos\":[\"...\"],\"mejoras\":[\"...\"],\"estructuraOk\":true,\"vocabularioOk\":true,\"consejo\":\"...\"}";
  try {
    var r = await fetch("https://api.anthropic.com/v1/messages", {
      method: "POST",
      headers: {"Content-Type": "application/json"},
      body: JSON.stringify({model:"claude-sonnet-4-20250514",max_tokens:800,messages:[{role:"user",content:prompt}]})
    });
    var data = await r.json();
    var text = data.content.map(function(i) { return i.text || ""; }).join("").replace(/```json|```/g,"").trim();
    var j = JSON.parse(text);
    var nc = j.notaEstimada >= 1.5 ? "var(--teal)" : j.notaEstimada >= 1 ? "#c9a84c" : "var(--red)";
    if (res) res.innerHTML = "<div style=\"display:grid;gap:0.85rem\">"
      + "<div style=\"background:var(--bg3);border-radius:var(--radius-sm);padding:1rem;display:flex;align-items:center;gap:1rem\">"
      + "<div style=\"text-align:center\"><div style=\"font-size:2.5rem;font-weight:900;color:" + nc + "\">" + j.notaEstimada + "</div><div style=\"font-size:0.68rem;color:var(--text3)\">de 2 pts</div></div>"
      + "<div><div style=\"display:flex;gap:0.4rem;margin-bottom:0.3rem\">"
      + "<span style=\"font-size:0.68rem;font-weight:700;padding:2px 7px;border-radius:50px;background:" + (j.estructuraOk ? "var(--teal-dim)" : "var(--red-dim)") + ";color:" + (j.estructuraOk ? "var(--teal)" : "var(--red)") + "\">" + (j.estructuraOk ? "✅" : "❌") + " Estructura</span>"
      + "<span style=\"font-size:0.68rem;font-weight:700;padding:2px 7px;border-radius:50px;background:" + (j.vocabularioOk ? "var(--teal-dim)" : "var(--red-dim)") + ";color:" + (j.vocabularioOk ? "var(--teal)" : "var(--red)") + "\">" + (j.vocabularioOk ? "✅" : "❌") + " Vocabulario</span>"
      + "</div></div></div>"
      + "<div style=\"background:var(--teal-dim);border:1px solid var(--teal);border-radius:var(--radius-sm);padding:0.85rem\"><div style=\"font-weight:700;color:var(--teal);margin-bottom:0.4rem;font-size:0.82rem\">✅ Bien desarrollado</div><ul style=\"margin:0;padding-left:1.1rem;font-size:0.8rem;color:var(--text2);line-height:1.8\">" + j.correctos.map(function(x) { return "<li>" + x + "</li>"; }).join("") + "</ul></div>"
      + "<div style=\"background:var(--gold-dim);border:1px solid rgba(201,168,76,0.4);border-radius:var(--radius-sm);padding:0.85rem\"><div style=\"font-weight:700;color:#c9a84c;margin-bottom:0.4rem;font-size:0.82rem\">⚠️ Puedes mejorar</div><ul style=\"margin:0;padding-left:1.1rem;font-size:0.8rem;color:var(--text2);line-height:1.8\">" + j.mejoras.map(function(x) { return "<li>" + x + "</li>"; }).join("") + "</ul></div>"
      + "<div style=\"background:var(--blue-dim);border:1px solid var(--blue);border-radius:var(--radius-sm);padding:0.85rem\"><div style=\"font-weight:700;color:var(--blue);margin-bottom:0.3rem;font-size:0.82rem\">💡 Consejo</div><p style=\"font-size:0.82rem;color:var(--text2);line-height:1.55;margin:0\">" + j.consejo + "</p></div></div>";
    var p = getProg(); p.iaUsos = (p.iaUsos||0)+1; saveProg(p); verificarLogros(p); addXP(15,"Corrección con IA");
  } catch(e) {
    if (res) res.innerHTML = "<div style=\"background:var(--red-dim);border:1px solid var(--red);border-radius:var(--radius-sm);padding:0.85rem;color:var(--red)\">❌ Error al conectar. Inténtalo de nuevo.</div>";
  }
  if (btn) { btn.textContent = "🤖 Analizar con IA"; btn.disabled = false; }
}

// ===== COMPARADOR =====
var COMP = {
  platon:{n:"Platón",c:"#c9a84c",t:{Realidad:"Dualismo: mundo sensible (apariencias) y mundo inteligible (Ideas verdaderas).",Conocimiento:"Reminiscencia: conocer es recordar las Ideas. Doxa (opinión) vs episteme (ciencia).",Ética:"Virtud como armonía del alma bajo la razón. Bien supremo como fin último.",Política:"Aristocracia gobernada por filósofos-reyes que conocen el Bien.",Ser_humano:"Alma inmortal atrapada en el cuerpo. Tres partes: racional, irascible, concupiscible."}},
  aristoteles:{n:"Aristóteles",c:"#3ecfb2",t:{Realidad:"Hilemorfismo: materia y forma inseparables en la sustancia individual concreta.",Conocimiento:"Parte de la experiencia sensible. Abstracción de universales desde los particulares.",Ética:"Eudaimonía: virtud como término medio. Felicidad como fin supremo de la vida.",Política:"Animal político por naturaleza. La polis necesaria para el desarrollo humano.",Ser_humano:"Animal racional. El alma es la forma del cuerpo, no sustancia separada."}},
  descartes:{n:"Descartes",c:"#5b8dee",t:{Realidad:"Dualismo: res cogitans (mente) y res extensa (cuerpo). Dios como garante.",Conocimiento:"Duda metódica → cogito ergo sum. Ideas claras y distintas garantizadas por Dios.",Ética:"Dominio de las pasiones por la razón. Generosidad como virtud principal.",Política:"No desarrolló filosofía política sistemática. Prima el orden racional.",Ser_humano:"Res cogitans: ser pensante. El cuerpo es máquina; la mente, sustancia inmaterial."}},
  hume:{n:"Hume",c:"#a78bfa",t:{Realidad:"Solo podemos conocer nuestras percepciones. Escepticismo sobre el exterior y el yo.",Conocimiento:"Impresiones → ideas. Causalidad: hábito mental, no razón. Guillotina de Hume.",Ética:"Moral basada en el sentimiento. La razón es esclava de las pasiones.",Política:"Convencionalismo: las instituciones son convenciones útiles, no naturales.",Ser_humano:"El yo es un haz de percepciones. No hay identidad personal sustancial."}},
  kant:{n:"Kant",c:"#3ecfb2",t:{Realidad:"Fenómeno (lo que conocemos) vs noúmeno (cosa en sí, incognoscible). Giro copernicano.",Conocimiento:"Síntesis de intuiciones a priori (espacio/tiempo) y categorías del entendimiento.",Ética:"Imperativo categórico: actúa según la máxima que puedas querer como ley universal.",Política:"Paz perpetua mediante federación de repúblicas. Uso público de la razón.",Ser_humano:"Ser racional y autónomo. Fin en sí mismo, nunca solo medio."}},
  nietzsche:{n:"Nietzsche",c:"#e05c5c",t:{Realidad:"No hay mundos verdaderos: solo interpretaciones. Crítica radical al platonismo.",Conocimiento:"Perspectivismo: no hay verdad objetiva, solo perspectivas al servicio de la vida.",Ética:"Transvaloración: moral de señores (afirmación) vs moral de esclavos (resentimiento).",Política:"Crítica al Estado, al nacionalismo y a la democracia igualitaria.",Ser_humano:"Ser que puede superarse: del último hombre al superhombre. Voluntad de poder."}},
  marx:{n:"Marx",c:"#e05c5c",t:{Realidad:"Materialismo: la realidad material (economía) determina la conciencia.",Conocimiento:"La ideología distorsiona el conocimiento para servir a la clase dominante.",Ética:"Moral burguesa es ideología. La praxis revolucionaria transforma el mundo.",Política:"Materialismo histórico: historia = lucha de clases. Estado = instrumento burgués.",Ser_humano:"Ser social y productor. Alienación separa al trabajador de su esencia creadora."}}
};

function compGenerar() {
  var k1 = (document.getElementById("comp1") || {}).value || "platon";
  var k2 = (document.getElementById("comp2") || {}).value || "aristoteles";
  var res = document.getElementById("compResult");
  if (!res) return;
  if (k1 === k2) { res.innerHTML = "<p style=\"color:var(--text3);text-align:center;padding:1rem\">Selecciona dos autores distintos.</p>"; return; }
  var d1 = COMP[k1], d2 = COMP[k2];
  var temas = Object.keys(d1.t);
  var html = "<div style=\"overflow-x:auto\"><table style=\"width:100%;border-collapse:collapse;font-size:0.8rem\">"
    + "<thead><tr>"
    + "<th style=\"background:var(--card);border:1px solid var(--border);padding:0.65rem 0.85rem;text-align:left;color:var(--text3);font-size:0.7rem;text-transform:uppercase;width:12%\">Tema</th>"
    + "<th style=\"background:var(--card);border:1px solid var(--border);padding:0.65rem 0.85rem;text-align:left;color:" + d1.c + "\">⚖️ " + d1.n + "</th>"
    + "<th style=\"background:var(--card);border:1px solid var(--border);padding:0.65rem 0.85rem;text-align:left;color:" + d2.c + "\">⚖️ " + d2.n + "</th>"
    + "</tr></thead><tbody>";
  temas.forEach(function(t, i) {
    html += "<tr style=\"background:" + (i%2===0 ? "var(--bg3)" : "var(--card)") + "\">"
      + "<td style=\"border:1px solid var(--border);padding:0.65rem 0.85rem;font-weight:700;color:var(--text2);white-space:nowrap\">" + t.replace("_"," ") + "</td>"
      + "<td style=\"border:1px solid var(--border);border-left:3px solid " + d1.c + ";padding:0.65rem 0.85rem;line-height:1.55\">" + d1.t[t] + "</td>"
      + "<td style=\"border:1px solid var(--border);border-left:3px solid " + d2.c + ";padding:0.65rem 0.85rem;line-height:1.55\">" + d2.t[t] + "</td>"
      + "</tr>";
  });
  html += "</tbody></table></div>"
    + "<div style=\"margin-top:0.85rem;background:var(--gold-dim);border:1px solid rgba(201,168,76,0.3);border-radius:var(--radius-sm);padding:0.85rem;font-size:0.8rem;color:var(--text2)\">"
    + "💡 <strong style=\"color:#c9a84c\">Para la 2a:</strong> <em>\"mientras " + d1.n + " defiende…, " + d2.n + " sostiene por el contrario…\"</em>, <em>\"ambos coinciden en…, sin embargo difieren en…\"</em></div>";
  res.innerHTML = html;
}

// ===== CALCULADORA =====
function calcNota() {
  var ids = ["cn1a","cn1b","cn1c","cn2a","cn2b"];
  var total = 0;
  for (var i = 0; i < ids.length; i++) {
    var el = document.getElementById(ids[i]);
    if (el) total += Math.min(2, Math.max(0, parseFloat(el.value) || 0));
  }
  var nota = Math.min(10, total);
  var ef = document.getElementById("cnFinal");
  var el2 = document.getElementById("cnLabel");
  if (ef) {
    ef.textContent = nota.toFixed(2);
    ef.style.color = nota>=9 ? "#c9a84c" : nota>=7 ? "var(--teal)" : nota>=5 ? "var(--blue)" : "var(--red)";
  }
  if (el2) el2.textContent = nota>=9 ? "🏆 Sobresaliente" : nota>=7 ? "👏 Notable" : nota>=5 ? "✅ Aprobado" : nota>=3 ? "⚠️ Cerca" : "❌ Suspendido";
}

// ===== COMUNIDAD =====
var ENCUESTAS = [
  {id:"dif",q:"¿Qué autor te cuesta más?",ops:["Kant","Platón","Nietzsche","Hume","Marx","Descartes","Aristóteles"]},
  {id:"preg",q:"¿Qué pregunta es más difícil?",ops:["1a Definiciones","1b Idea principal","1c Posición filosófica","2a Relación autores","2b Valoración personal"]},
  {id:"cnd",q:"¿Cuándo empezaste a estudiar?",ops:["Más de 3 meses antes","1-3 meses antes","1 mes antes","2 semanas antes","La noche anterior 😅"]},
];

function renderComunidad() {
  var grid = document.getElementById("comunidadGrid");
  if (!grid) return;
  grid.innerHTML = ENCUESTAS.map(function(e) {
    var votos = STO.get("v_" + e.id) || {};
    var votado = STO.get("vt_" + e.id);
    var total = Object.values(votos).reduce(function(a,b) { return a+b; }, 0) || 1;
    return "<div style=\"background:var(--card);border:1px solid var(--border);border-radius:var(--radius);padding:1.25rem\">"
      + "<h3 style=\"font-size:0.9rem;font-weight:700;margin-bottom:0.85rem\">🗳️ " + e.q + "</h3>"
      + "<div style=\"display:flex;flex-direction:column;gap:0.5rem\">"
      + e.ops.map(function(op) {
          var v = votos[op] || 0;
          var pct = Math.round(v/total*100);
          var sel = votado === op;
          return "<div><div style=\"display:flex;justify-content:space-between;margin-bottom:0.2rem;font-size:0.8rem\">"
            + "<button onclick=\"votar('" + e.id + "','" + op + "')\" style=\"background:none;border:none;color:" + (sel ? "#c9a84c" : "var(--text2)") + ";cursor:pointer;font-size:0.8rem;text-align:left;font-family:var(--font-body);font-weight:" + (sel ? 700 : 400) + ";padding:0\">" + (sel ? "✓ " : "") + op + "</button>"
            + (votado ? "<span style=\"color:var(--text3)\">" + pct + "%</span>" : "")
            + "</div>"
            + (votado ? "<div style=\"background:var(--bg3);border-radius:50px;height:4px;overflow:hidden\"><div style=\"height:100%;background:" + (sel ? "#c9a84c" : "var(--teal)") + ";border-radius:50px;width:" + pct + "%;transition:width 0.6s\"></div></div>" : "")
            + "</div>";
        }).join("")
      + "</div>"
      + (!votado ? "<p style=\"font-size:0.7rem;color:var(--text3);margin-top:0.65rem\">Vota para ver resultados</p>" : "<p style=\"font-size:0.7rem;color:var(--text3);margin-top:0.5rem\">" + total + " votos</p>")
      + "</div>";
  }).join("");
}

function votar(id, op) {
  if (STO.get("vt_" + id)) return;
  var votos = STO.get("v_" + id) || {};
  votos[op] = (votos[op] || 0) + 1;
  STO.set("v_" + id, votos);
  STO.set("vt_" + id, op);
  addXP(5, "Voto en comunidad");
  renderComunidad();
}

// ===== FRASE DEL DÍA HTML =====
document.addEventListener("DOMContentLoaded", function() {
  // Frase del día: insertar antes del social banner
  var banner = document.querySelector(".social-banner, #mis-videos");
  if (banner) {
    var fd = document.createElement("div");
    fd.style.cssText = "background:var(--bg2);border-bottom:1px solid var(--border);padding:0.9rem 1.25rem";
    fd.innerHTML = "<div style=\"max-width:860px;margin:0 auto;display:flex;align-items:center;gap:1rem;flex-wrap:wrap\">"
      + "<div style=\"width:38px;height:38px;border-radius:50%;background:var(--gold-dim);border:2px solid rgba(201,168,76,0.35);display:flex;align-items:center;justify-content:center;font-size:1.1rem;flex-shrink:0\">💭</div>"
      + "<div style=\"flex:1;min-width:180px\">"
      + "<div id=\"fraseLabel\" style=\"font-size:0.62rem;font-weight:700;text-transform:uppercase;letter-spacing:0.1em;color:#c9a84c;margin-bottom:0.15rem\">Frase del día</div>"
      + "<div id=\"fraseTexto\" style=\"font-size:0.88rem;line-height:1.5;color:var(--text);font-style:italic\"></div>"
      + "<div id=\"fraseAutorQ\" style=\"font-size:0.73rem;color:var(--text3);margin-top:0.15rem;font-weight:600\"></div></div>"
      + "<button onclick=\"siguienteFrase()\" style=\"flex-shrink:0;background:var(--card);border:1px solid var(--border);color:var(--text3);width:32px;height:32px;border-radius:50%;font-size:0.95rem;cursor:pointer\" title=\"Otra frase\">↻</button></div>";
    banner.parentNode.insertBefore(fd, banner);
  }
  mostrarFraseDia();

  // Init vídeos
  vRenderAvatares();
  vRender();

  // Init demás secciones
  renderLogros();
  renderComunidad();
  compGenerar();

  // Progreso
  registrarDia();
  var p = getProg();
  renderNivel(p.xp || 0);
  verificarLogros(p);
});
</script>

</body>
</html>
