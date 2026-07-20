<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Premio a la Innovación 2025-2026 — Formulario de Evaluación</title>
<style>
*{box-sizing:border-box;margin:0;padding:0}
body{font-family:-apple-system,BlinkMacSystemFont,'Segoe UI',sans-serif;background:#f0f4f8;min-height:100vh;padding:2rem 1rem;color:#1a1a1a}
.wrap{max-width:720px;margin:0 auto}
.header{background:#0a4d7c;border-radius:14px;padding:1.4rem 1.75rem;margin-bottom:1.5rem;display:flex;align-items:center;justify-content:space-between}
.header h1{color:#ffffff;font-size:17px;font-weight:700}
.header p{color:#ffffff;font-size:12px;margin-top:3px}
.header-logo{color:#ffffff;font-size:13px;font-weight:700;opacity:.85}
.step-bar{display:flex;gap:6px;margin-bottom:1.5rem}
.step{flex:1;height:5px;border-radius:3px;background:#dde3ec;transition:background .3s}
.step.done{background:#0a4d7c}
.step.active{background:#1a7db5}
.card{background:#fff;border:1px solid #e2e8f0;border-radius:12px;padding:1.25rem 1.5rem;margin-bottom:1rem}
.lbl{font-size:11px;font-weight:700;letter-spacing:.08em;text-transform:uppercase;color:#888;margin-bottom:6px}
input[type=text],select,textarea{width:100%;font-size:14px;padding:9px 11px;border:1px solid #cbd5e1;border-radius:8px;background:#f8fafc;color:#1a1a1a;outline:none;font-family:inherit}
input[type=text]:focus,select:focus,textarea:focus{border-color:#1a7db5;background:#fff}
textarea{resize:vertical;min-height:72px}
.brief-toggle{width:100%;display:flex;align-items:center;justify-content:space-between;background:#fff;border:1px solid #bfdbfe;border-radius:10px;padding:12px 16px;cursor:pointer;margin-bottom:10px;transition:background .15s}
.brief-toggle:hover{background:#f0f7ff}
.brief-toggle-left{display:flex;align-items:center;gap:8px}
.brief-toggle-title{font-size:13px;font-weight:700;color:#0a4d7c}
.brief-toggle-sub{font-size:11px;color:#64748b;margin-top:1px}
.brief-arrow{font-size:14px;color:#0a4d7c;transition:transform .25s}
.brief-arrow.open{transform:rotate(180deg)}
.brief-body{background:#fff;border:1px solid #bfdbfe;border-radius:10px;padding:0;margin-bottom:14px;overflow:hidden;max-height:0;transition:max-height .35s ease,padding .25s}
.brief-body.open{max-height:900px;padding:16px}
.brief-grid{display:grid;grid-template-columns:1fr 1fr 1fr;gap:10px}
.brief-col{background:#f8fafc;border:1px solid #e2e8f0;border-radius:8px;padding:10px 12px}
.brief-col-title{font-size:10px;font-weight:700;letter-spacing:.07em;text-transform:uppercase;color:#888;margin-bottom:8px}
.brief-col-title.blue{color:#1a7db5}
.brief-col-title.green{color:#16a34a}
.brief-col-title.teal{color:#0d9488}
.brief-info{font-size:11px;color:#334155;margin-bottom:5px;line-height:1.5}
.brief-info b{color:#0a4d7c;font-weight:700}
.brief-divider{border:none;border-top:1px solid #e2e8f0;margin:8px 0}
.brief-bullet{font-size:11px;color:#334155;margin-bottom:5px;padding-left:10px;position:relative;line-height:1.5}
.brief-bullet::befoe{content:'•';position:absolute;left:0;color:#0a4d7c}
.brief-impact{font-size:11px;color:#334155;margin-bottom:5px;padding-left:14px;position:relative;line-height:1.5}
.brief-impact::befoe{content:'→';position:absolute;left:0;color:#0a4d7c;font-weight:700}
.brief-tag{display:inline-block;font-size:10px;padding:2px 8px;border-radius:20px;font-weight:700;margin-bottom:3px}
.tag-blue{background:#dbeafe;color:#1e40af}
.tag-green{background:#dcfce7;color:#166534}
.bloque-hdr{display:flex;align-items:center;gap:8px;padding:10px 14px;border-radius:8px;margin-bottom:12px}
.bh-imp{background:#dbeafe;border-left:3px solid #1a7db5}
.bh-ot{background:#dcfce7;border-left:3px solid #16a34a}
.bh-title{font-size:13px;font-weight:700;color:#1e3a5f}
.bh-title.green{color:#14532d}
.bh-sub{font-size:11px;color:#555;margin-top:1px}
.crit{border:1px solid #e2e8f0;border-radius:10px;margin-bottom:10px;overflow:hidden;background:#fff}
.crit-head{padding:.9rem 1.25rem .5rem}
.crit-name{font-size:13px;font-weight:700;color:#1a1a1a}
.crit-peso{font-size:11px;font-weight:700;color:#1a7db5;background:#dbeafe;padding:2px 8px;border-radius:20px;display:inline-block;margin-top:4px}
.crit-desc{font-size:12px;color:#555;margin-top:6px;line-height:1.55}
.opt-table{display:grid;grid-template-columns:1fr 1fr 1fr;border-top:1px solid #e2e8f0}
.opt{cursor:pointer;padding:10px 8px 12px;text-align:center;transition:background .15s;border-right:1px solid #e2e8f0}
.opt:last-child{border-right:none}
.opt-pts{font-size:20px;font-weight:800;color:#aaa;display:block}
.opt-lbl{font-size:10px;font-weight:700;letter-spacing:.06em;color:#aaa;display:block;margin-top:1px}
.opt-hint{font-size:10px;color:#bbb;display:block;margin-top:5px;line-height:1.4;padding:0 4px}
.opt:hover{background:#f0f7ff}
.opt:hover .opt-pts,.opt:hover .opt-lbl{color:#0a4d7c}
.opt.s0{background:#fef2f2}.opt.s0 .opt-pts,.opt.s0 .opt-lbl{color:#dc2626}.opt.s0 .opt-hint{color:#f87171}
.opt.s50{background:#fffbeb}.opt.s50 .opt-pts,.opt.s50 .opt-lbl{color:#d97706}.opt.s50 .opt-hint{color:#fbbf24}
.opt.s100{background:#eff6ff}.opt.s100 .opt-pts,.opt.s100 .opt-lbl{color:#0a4d7c}.opt.s100 .opt-hint{color:#60a5fa}
.crit-comment{padding:.5rem 1.25rem .9rem}
.crit-comment textarea{height:44px;font-size:12px;border-color:#e2e8f0;resize:none}
.score-box{background:linear-gradient(135deg,#0a4d7c,#1a7db5);border-radius:12px;padding:1.1rem 1.4rem;margin-bottom:1rem;display:flex;align-items:center;gap:16px}
.score-num{font-size:42px;font-weight:800;color:#fff;min-width:72px;line-height:1}
.score-right{flex:1}
.score-bar-wrap{height:8px;background:rgba(255,255,255,.25);border-radius:4px;overflow:hidden;margin-bottom:6px}
.score-bar{height:100%;background:#fff;border-radius:4px;transition:width .5s}
.score-sub{font-size:11px;color:rgba(255,255,255,.75)}
.fr{display:flex;gap:8px;margin-top:8px}
.fb{flex:1;padding:12px;border-radius:8px;border:1px solid #cbd5e1;background:#f8fafc;color:#555;font-size:13px;font-weight:700;cursor:pointer;text-align:center;transition:all .15s}
.fb:hover{border-color:#1a7db5;color:#0a4d7c;background:#eff6ff}
.fb.fsi{background:#eff6ff;border-color:#1a7db5;color:#0a4d7c}
.fb.fno{background:#fef2f2;border-color:#fca5a5;color:#dc2626}
.fb.ftv{background:#fffbeb;border-color:#fcd34d;color:#d97706}
.nr{display:flex;gap:10px;margin-top:1rem}
.bp{flex:1;padding:13px;border-radius:8px;border:none;background:#0a4d7c;color:#fff;font-size:14px;font-weight:700;cursor:pointer}
.bp:hover{background:#083d63}
.bs{padding:13px 22px;border-radius:8px;border:1px solid #cbd5e1;background:#f8fafc;color:#555;font-size:14px;cursor:pointer}
.bs:hover{background:#e2e8f0}
.sc{background:#fff;border:1px solid #e2e8f0;border-radius:12px;padding:2.5rem;text-align:center}
.si{width:56px;height:56px;border-radius:50%;background:#dbeafe;display:flex;align-items:center;justify-content:center;margin:0 auto 1rem;font-size:28px}
.hidden{display:none}
.pt{display:inline-flex;align-items:center;gap:5px;background:#fff;border:1px solid #e2e8f0;border-radius:20px;padding:4px 14px;font-size:12px;color:#555;margin-bottom:14px;font-weight:600}
.ib{background:#f0f7ff;border:1px solid #bfdbfe;border-radius:8px;padding:10px 14px;font-size:12px;color:#334155;line-height:1.6;margin-bottom:16px}
.ib strong{color:#0a4d7c}
.res-row{display:flex;align-items:flex-start;justify-content:space-between;gap:8px;padding:6px 0;border-bottom:1px solid #f1f5f9;font-size:13px}
.res-row:last-child{border-bottom:none}
.res-name{color:#555;flex:1}
.res-lbl{font-size:11px;padding:2px 8px;border-radius:20px;font-weight:700;white-space:nowrap}
.rl0{background:#fef2f2;color:#dc2626}
.rl50{background:#fffbeb;color:#d97706}
.rl100{background:#eff6ff;color:#0a4d7c}
</style>
</head>
<body>
<div class="wrap">
  <div class="header">
    <div><h1>Premio a la Innovación 2025-2026</h1><p>Formulario de evaluación — uso exclusivo evaluadores</p></div>
    <div class="header-logo">ARS Primera</div>
  </div>
  <div class="step-bar">
    <div class="step active" id="s1"></div>
    <div class="step" id="s2"></div>
    <div class="step" id="s3"></div>
  </div>

  <div id="p1">
    <div class="card"><div class="lbl">Nombre del Evaluado</div><input type="text" id="ev" placeholder="Ingresa tu código de evaluación" onblur="markEvaluatedOptions()"></div>
    <div class="card"><div class="lbl">Solución a Evaluar</div>
      <select id="sol">
        <option value="">Selecciona una solución...</option>
        <option>Conciliacion Web</option>
        <option>Procesamiento Masivo de Reclamaciones Medicas</option>
        <option>Implementacion del Bot Vera para PSS</option>
        <option>Cuidados Paliativos Siempre Juntos Adulto</option>
        <option>Motor Tarifario</option>
        <option>Gestion Agil de Altas Medicas</option>
        <option>Calculadora de Oxigeno</option>
        <option>Proceso de Suspension Dependientes Adicionales</option>
        <option>ARI (Asistente de Respuestas para Intermediarios)</option>
        <option>Autorizaciones Agiles</option>
        <option>Anomatrace 1.0</option>
        <option>Automatizacion y Gestion de Solicitudes de Contrataciones de PSS</option>
      </select>
    </div>
    <div id="eval-banner" style="display:none;background:#f0fdf4;border:1px solid #bbf7d0;border-radius:10px;padding:10px 14px;margin-bottom:1rem;font-size:12px;color:#166534;line-height:1.8"></div>
    <div class="nr"><button class="bp" onclick="goTo(2)">Continuar</button></div>
  </div>

  <div id="p2" class="hidden">
    <div class="pt">Solución: <span id="pt1"></span></div>
    <div class="brief-toggle" onclick="toggleBrief()">
      <div class="brief-toggle-left">
        <span>📋</span>
        <div>
          <div class="brief-toggle-title">Ver Brief de la Solución</div>
          <div class="brief-toggle-sub">Antes / Después / Impacto — clic para expandir</div>
        </div>
      </div>
      <span class="brief-arrow" id="brief-arrow">▼</span>
    </div>
    <div class="brief-body" id="brief-body">
      <div class="brief-grid">
        <div class="brief-col">
          <div class="brief-col-title blue">📊 Información</div>
          <div id="b-info"></div>
        </div>
        <div class="brief-col" style="grid-column:span 2">
          <div class="brief-col-title" style="color:#dc5a30">📈 Antes</div>
          <div id="b-antes"></div>
          <hr class="brief-divider">
          <div class="brief-col-title green">💡 Después</div>
          <div id="b-despues"></div>
        </div>
      </div>
      <div style="margin-top:10px;background:#f8fafc;border:1px solid #e2e8f0;border-radius:8px;padding:10px 12px">
        <div class="brief-col-title teal">🎯 Impacto</div>
        <div id="b-impacto" style="display:grid;grid-template-columns:1fr 1fr;gap:4px 16px"></div>
      </div>
    </div>
    <div class="ib"><strong>Criterio único: IMPACTO</strong> — Desagregado en 4 dimensiones (90%) + 2 criterios de contexto (10%). Selecciona <strong>Bajo (0)</strong>, <strong>Medio (50)</strong> o <strong>Alto (100)</strong> for each.</div>
    <div class="bloque-hdr bh-imp"><div><div class="bh-title">🎯 IMPACTO — 90%</div><div class="bh-sub">4 dimensiones de 22.5% cada una</div></div></div>
    <div id="ci"></div>
    <div class="bloque-hdr bh-ot" style="margin-top:8px"><div><div class="bh-title green">🧩 OTROS CRITERIOS — 10%</div><div class="bh-sub">2 criterios de contexto de 5% cada uno</div></div></div>
    <div id="co"></div>
    <div class="score-box">
      <div><div style="font-size:11px;color:rgba(255,255,255,.65);font-weight:700;letter-spacing:.06em;text-transform:uppercase;margin-bottom:4px">Total Score</div><div class="score-num" id="sdn">—</div></div>
      <div class="score-right"><div class="score-bar-wrap"><div class="score-bar" id="sbr" style="width:0%"></div></div><div class="score-sub" id="sbdt">Score all criteria to see the result</div></div>
      <div style="text-align:right;color:rgba(255,255,255,.6)"><div style="font-size:10px;margin-bottom:2px">Máximo</div><div style="font-size:18px;font-weight:800;color:#fff">100</div></div>
    </div>
    <div class="nr"><button class="bs" onclick="goTo(1)">Atrás</button><button class="bp" onclick="goTo(3)">Continuar</button></div>
  </div>

  <div id="p3" class="hidden">
    <div class="pt">Solución: <span id="pt2"></span></div>
    <div class="card"><div class="lbl" style="margin-bottom:6px">Comentario</div><textarea id="ft" placeholder="Escribe tu comentario general sobre esta solución..."></textarea></div>
    <div class="card">
      <div class="lbl" style="margin-bottom:8px">¿Recomiendas este proyecto como finalista?</div>
      <div class="fr">
        <div class="fb" id="fsi" onclick="sf('si')">Sí</div>
        <div class="fb" id="ftv" onclick="sf('talvez')">Tal vez</div>
        <div class="fb" id="fno" onclick="sf('no')">No</div>
      </div>
    </div>
    <div class="nr"><button class="bs" onclick="goTo(2)">Atrás</button><button class="bp" onclick="sub()">Enviar Evaluación</button></div>
  </div>

  <div id="p4" class="hidden">
    <div class="sc">
      <div class="si">✓</div>
      <div style="font-size:18px;font-weight:700;color:#1a1a1a;margin-bottom:6px">Evaluación Enviada</div>
      <div style="font-size:13px;color:#555;margin-bottom:1.5rem" id="cm"></div>
      <div style="background:#f8fafc;border:1px solid #e2e8f0;border-radius:10px;padding:1.25rem;text-align:left;margin-bottom:1.5rem">
        <div style="font-size:11px;color:#888;text-transform:uppercase;letter-spacing:.08em;font-weight:700;margin-bottom:12px">Resumen de Evaluación</div>
        <div id="res"></div>
        <div style="margin-top:12px;padding-top:12px;border-top:1px solid #e2e8f0">
          <div style="font-size:13px;color:#555" id="r-comment"></div>
          <div style="font-size:13px;color:#555;margin-top:4px"><b>Finalista:</b> <span id="r-fin"></span></div>
        </div>
        <div style="margin-top:14px;padding-top:12px;border-top:2px solid #0a4d7c;display:flex;align-items:center;justify-content:space-between">
          <div style="font-size:13px;font-weight:700;color:#555">Total Score</div>
          <div style="font-size:28px;font-weight:800;color:#0a4d7c" id="r-total"></div>
        </div>
      </div>
      <button class="bp" onclick="rst()" style="max-width:240px;margin:0 auto;display:block">Evaluar Otra Solución</button>
    </div>
  </div>
</div>

<script>
var EVALUADORES = {
  'ARS-001': 'Vilma Linnet Breton',
  'ARS-002': 'Magda Rosanna Sánchez',
  'ARS-003': 'Sarah Mercedes Herrera',
  'ARS-004': 'Ramón Gómez',
  'ARS-007': 'Denis Alexandra Pérez',
  'ARS-008': 'Juan Alfredo de la Cruz',
  'ARS-009': 'Teresalina Páez',
  'ARS-010': 'Jean Paul Quiroz',
  'ARS-011': 'Sandra Jacobo',
};

var BRIEFS = {
  'Conciliacion Web':{
    postulante:'Angel Bladimir Pinales',
    area:'Servicio y Operaciones',
    categoria:'Procesos y Eficiencia',
    tipo:'Disruptiva',
    equipo:'Angel Bladimir Pinales, Victor Morillo, Jose Manuel Perez, Deborah Tirado',
    antes:[
      'Proceso completamente manual y reactivo con alta friccion entre las partes.',
      'Casos con antiguedad mayor a 360 dias escalados obligatoriamente al comite para aprobacion de pago.',
      'Escasa visibilidad del estado de cada conciliacion para el PSS y para las areas internas.',
      'Reprocesos, retrasos y dependencia total de intervenciones manuales para avanzar cada caso.',
      'Modelo de aproximadamente 8 a 10 pasos manuales.'
    ],
    despues:[
      'Conciliacion Web: el PSS gestiona, el comite solo interviene en excepciones. Flujo digital de 3 a 4 pasos.',
      'Plataforma digital donde el PSS gestiona sus propias conciliaciones de forma autonoma. El PSS carga directamente la conciliacion en la Oficina Virtual (OFV).',
      'Trazabilidad completa del proceso de punta a punta sin intervencion manual en casos estandar.',
      'El comite queda reservado exclusivamente para casos excepcionales fuera de los parametros definidos.',
      'Informacion confiable en tiempo real para la toma de decisiones de todas las areas involucradas.'
    ],
    impacto:[
      'Reduccion del 58% en la cantidad de conciliaciones procesadas en 2025 vs 2024 y 101% desde el ano 2025.',
      'Costo evitable estimado (2025): RD$257 millones. Equivalente al 1.05% de la siniestralidad.',
      'Migracion del 94% de las conciliaciones a la web.'
    ]
  },
  'Procesamiento Masivo de Reclamaciones Medicas':{
    postulante:'Katherine Torres Ventura',
    area:'Servicio y Operaciones',
    categoria:'Procesos y Eficiencia',
    tipo:'Disruptiva',
    equipo:'Katherine Torres, Jose Ventura, Victor Morillo, Jose Manuel Perez, Angel Pinales',
    antes:[
      '"El procesador era el humano — siempre"',
      'Cada reclamacion requeria validacion y gestion manual por parte del equipo.',
      'Tiempos prolongados de gestion y alta carga administrativa por volumen.',
      'Riesgo de inconsistencias por dependencia total de la intervencion humana.',
      'Sin capacidad de escalar el volumen sin aumentar proporcionalmente el equipo.'
    ],
    despues:[
      'El procesador es el sistema — el equipo gestiona excepciones.',
      '70% de las reclamaciones procesadas de forma masiva y desasistida.',
      'El sistema valida, procesa y gestiona sin intervencion humana en casos estandar.',
      'El equipo reenfocado en supervision, monitoreo y gestion de excepciones.',
      'Modelo escalable: mas volumen sin incremento proporcional de estructura.'
    ],
    impacto:[
      'Ahorro anual: RD$10.6MM (gastos en nomina).',
      '+25% eficiencia operativa.',
      '70% procesadas masivamente (+535k reclamos/mes).',
      'Pasamos de 160 a 132 personas, alcanzando mayor eficiencia operativa.'
    ]
  },
  'Implementacion del Bot Vera para PSS':{
    postulante:'Maria Fernanda Ortiz e Isabel Brito',
    area:'Gestion de Redes',
    categoria:'Experiencia del cliente',
    tipo:'Disruptiva',
    equipo:'Maria Fernanda Ortiz e Isabel Brito',
    antes:[
      'Predominio de canales tradicionales (correo electronico y CAC) para gestion de solicitudes.',
      'Accesibilidad limitada para los diferentes perfiles y necesidades de los prestadores.',
      'Tecnologias y canales de comunicacion directa enfocados en el afiliado, no en el prestador.',
      'Tiempos de respuesta prolongados y mayor carga operativa para las areas internas.',
      'Experiencia del prestador fragmentada, con alta dependencia de intervencion humana.'
    ],
    despues:[
      'Vera: Nueva asistente virtual, exclusiva para prestadores de ARS Primera.',
      'Consolidacion de un canal digital especializado que unifica consultas, solicitudes e informacion en tiempo real.',
      'Reduccion de tiempos de respuesta con atencion inmediata, personalizada y disponible 24/7.',
      'Incremento de la adopcion de canales digitales, disminuyendo dependencia de llamadas y CAC.',
      'Fortalecimiento de la autogestion de los Prestadores con mayor autonomia y trazabilidad.'
    ],
    impacto:[
      '44% de traccion — superando la meta inicial del 25%. Nueva meta 60% para finales del 2026.',
      '644 PSS activos en el canal desde el lanzamiento en Noviembre 2025.',
      'Adopcion del PSS: 7% al cierre Junio 2026, meta proyectada 8% para Noviembre 2026.',
      'Vera gestiono 4,218 solicitudes en los primeros seis meses de 2026, equivalente al 69% del volumen del mismo periodo de 2025.'
    ]
  },
  'Cuidados Paliativos Siempre Juntos Adulto':{
    postulante:'Ruth Perez Gonzalez',
    area:'Gestion de Redes',
    categoria:'Experiencia del cliente',
    tipo:'Disruptiva',
    equipo:'Ruth Perez Gonzalez, Giselle Pena, Johanna Reynoso, Dulsinea Perez',
    antes:[
      'Pacientes con enfermedades avanzadas e incurables enfrentaban necesidades complejas mas alla de la atencion medica tradicional.',
      'El manejo del dolor, control de sintomas y acompanamiento emocional no estaban centralizados ni contaban con un modelo especializado.',
      'La coordinacion de servicios requeria atencion integral y continua que no siempre existia.',
      'Alta carga para pacientes y familias en etapa de alta vulnerabilidad fisica y emocional.',
      'Atencion en la ultima etapa de la vida en centros hospitalarios con altos costos de bolsillos para los afiliados.'
    ],
    despues:[
      'Se implemento el programa Cuidados Paliativos Siempre Juntos Adulto, orientado a brindar atencion integral a pacientes con enfermedades avanzadas y a sus familias.',
      'Incorpora la metodologia internacional NEWPALEX®, basada en mas de 200 estandares de calidad y mejora continua.',
      'Equipo dedicado brinda manejo especializado del dolor, apoyo emocional, acompanamiento psicologico y coordinacion de servicios.',
      'Atencion centrada en la calidad de vida, la dignidad y el bienestar del paciente.',
      'Acompanamiento a familiares mediante apoyo al duelo durante un mes posterior al fallecimiento.',
      'Atencion especializada directamente desde el domicilio.'
    ],
    impacto:[
      'Control del dolor: 87.4%.',
      'Ahorro economico: RD$152.6 MM (Oct-2024 - Sept 2025).',
      'Cantidad de pacientes: 1,572 a junio 2026.',
      'Reduccion hospitalizaciones: 66.3%.',
      'Reduccion de uso de emergencias: 64.6%.',
      'Satisfaccion: 97.9% (Meta >95%).',
      'Atencion domiciliaria de la poblacion: 86.1%.'
    ]
  },
  'Motor Tarifario':{
    postulante:'Randy de Jesus Polanco Fernandez, Jose Gabriel Matos Parra',
    area:'Gestion de Redes e Inteligencia PDSS',
    categoria:'Procesos y Eficiencia',
    tipo:'Disruptiva',
    equipo:'Randy Polanco, Magda Sanchez, Jose Gabriel Matos, Alfonso Then',
    antes:[
      '"Sin referente interno: el PSS ponia el precio, la ARS negociaba desde debilidad."',
      'Gestion financiera de procedimientos de alto costo sin metodologia estandarizada de valoracion.',
      'Variabilidad en criterios entre areas: autorizaciones, auditoria y reclamaciones con montos distintos.',
      'La tarifa la definia el PSS — la ARS aceptaba o negociaba sin un instrumento propio de referencia.',
      'Construir un paquete de cobertura tomaba hasta 3 semanas por la fragmentacion del proceso.'
    ],
    despues:[
      '"Motor Tarifario: la ARS define el valor, el PSS negocia desde un referente."',
      'Herramienta analitica y operativa que paquetiza coberturas de alta complejidad y calcula una tarifa propia por procedimiento.',
      'Calculo automatico de tarifa propia por procedimiento segun contrato y parametros clinicos.',
      'Transicion hacia modalidad de pago por paquete con criterios estandarizados y auditables.',
      'La ARS paso de reaccionar a la tarifa del PSS a tener su propio instrumento de valoracion.'
    ],
    impacto:[
      'RD$30,955,278.90 de costo evitado real y auditado entre marzo 2024 y junio 2026.',
      '3,199 eventos contratados con tarifa propia en 11 prestadores.',
      'En el 100% de las negociaciones el motor cerro por debajo de lo solicitado por el prestador, con reduccion promedio del 20.7%.',
      'Eficiencia operativa: Antes 3 semanas para construir un paquete, ahora 5 minutos.'
    ]
  },
  'Gestion Agil de Altas Medicas':{
    postulante:'Hilda Martinez',
    area:'Gestion Medica',
    categoria:'Procesos y Eficiencia',
    tipo:'Distinta',
    equipo:'Hilda Martinez y Wendy Arias',
    antes:[
      'El PSS dependia del CAC para cerrar cualquier cuenta clinica, incluso las de baja complejidad que no requerian intervencion humana.',
      'Demoras para PSS y afiliados por cuello de botella en el canal asistido, afectando la eficiencia operativa y la experiencia del afiliado.',
      'El CAC no podia enfocarse en gestiones criticas por el volumen de solicitudes simples.'
    ],
    despues:[
      'WEBSALUD ARS Primera: Modulo integrado en el canal de Autorizaciones Medicas en Linea.',
      'El PSS cierra en linea sus cuentas de baja complejidad sin intervencion del CAC.',
      'El sistema valida y procesa la transaccion automaticamente.',
      'El CAC queda disponible para gestionar casos de mayor complejidad.'
    ],
    impacto:[
      '169 PSS adoptaron el canal desde el lanzamiento.',
      '19,552 transacciones exitosas procesadas de forma autonoma (Abril 2025 - Junio 2026), correspondientes al 23% del total.',
      '19.5% de reduccion de llamadas al CAC.',
      'El tiempo promedio de cierre de cuenta se redujo en un 58.3%: De 7.2 min a solo 3 minutos.'
    ]
  },
  'Calculadora de Oxigeno':{
    postulante:'Jose Rafael Silie',
    area:'Gestion de Redes',
    categoria:'Procesos y Eficiencia',
    tipo:'Distinta',
    equipo:'Jose Rafael Silie, Alfonso Then, Maria Fernanda Ortiz',
    antes:[
      'Calculo manual, tres areas, un mismo error.',
      'Calculo de cobertura de oxigeno realizado manualmente en el cierre de cada cuenta clinica.',
      'Diferencias frecuentes entre Autorizaciones, Auditoria Medica y Reclamaciones por variacion en los montos calculados.',
      'Glosas, ajustes y pagos incompletos que retrasaban el pago al PSS e incrementaban sus cuentas por cobrar.',
      'Alta carga operativa por reprocesos.'
    ],
    despues:[
      'Calculadora de oxigeno: un codigo, un calculo, cero diferencias.',
      'Modulo automatico en Infoplan activado al digitar el codigo de cobertura 1083.',
      'Seleccion del tipo de contrato (Litro o Monto) y calculo automatico segun tarifa contratada.',
      'Validacion de campos obligatorios y confirmacion antes de aplicar el cierre de cuenta.',
      'Valores transferidos directo a la cuenta clinica y almacenados en cubos de costo medico.'
    ],
    impacto:[
      'Glosas codigo 1083: $2,459,658 (2024) → $371,357 (2025). Reduccion del 85%.',
      'Reduccion de errores en un 20%.',
      'Reduccion del 6% entre el margen de lo reclamado vs lo pagado 2024 vs 2025.'
    ]
  },
  'Proceso de Suspension Dependientes Adicionales':{
    postulante:'Andres Michel Gonzalez Amador',
    area:'Servicio y Operaciones',
    categoria:'Procesos y Eficiencia',
    tipo:'Distinta',
    equipo:'Augusto Mejia, Andres Gonzalez, Edwin Figueroa, Tito Mendez',
    antes:[
      'Una sola validacion: el proceso validaba la notificacion inicial del titular, pero no verificaba la recepcion efectiva del pago.',
      '~1,200 dependientes permanecian activos sin cobertura vigente.',
      'Consumos indebidos por parte de afiliados sin pago.',
      'La organizacion absorbia el costo sin control posterior.'
    ],
    despues:[
      'Doble validacion automatica: sin pago confirmado, sin cobertura. Automatizacion total del proceso.',
      'Suspension automatica ejecutada posterior a fecha limite TSS.',
      'Validacion mensual del estado de dependientes adicionales.',
      'Suspension al segundo corte si no hay confirmacion.',
      'Reactivacion automatica inmediata al recibir el pago.'
    ],
    impacto:[
      'Perdidas evitadas: RD$12.9MM (3 meses: junio a agosto 2025).',
      'Proyeccion anual: ~RD$51.6MM en riesgo financiero bajo control.',
      'Eficiencia mensual: ~1,200 dependientes gestionados de forma correcta.'
    ]
  },
  'ARI (Asistente de Respuestas para Intermediarios)':{
    postulante:'Minerva Frias Sosa',
    area:'Servicio y Operaciones',
    categoria:'Experiencia del cliente',
    tipo:'Disruptiva',
    equipo:'Minerva Frias Sosa, Luis Alejandro Troncoso Martinez, Monnavel Carvajal Sanchez, Carlos Daniel Feliz Javiera',
    antes:[
      'Los intermediarios gestionaban un alto volumen de consultas criticas a traves de canales asistidos como correos y visitas presenciales.',
      'Este modelo generaba tiempos de respuesta prolongados y reprocesos operativos.',
      'Generaba friccion en la experiencia y desgaste en la relacion comercial.'
    ],
    despues:[
      'Se implemento ARI, un asistente conversacional inteligente disenado especificamente para intermediarios, integrado a WhatsApp.',
      'Permite consultar la cartera de clientes, validar vigencias y planes, gestionar inclusiones y realizar consultas operativas sin intervencion humana.',
      'Combina procesamiento de lenguaje natural, flujos guiados y consumo de APIs internas.',
      'Ofrece una experiencia simple, uniforme y segura, disponible las 24 horas.'
    ],
    impacto:[
      'Gestion de 658 transacciones entre abril y diciembre de 2025, de las cuales el 82% fueron resueltas sin intervencion humana.',
      '402 usuarios unicos utilizaron la solucion durante el periodo comprendido entre abril y diciembre de 2025.',
      'Incremento de 19 puntos porcentuales en el NPS: de 35% (abril 2025) a 54% (abril 2026).',
      'Incremento de 10 puntos porcentuales en el CSAT: de 77% (abril 2025) a 87% (abril 2026).'
    ]
  },
  'Autorizaciones Agiles':{
    postulante:'Carlos Daniel Feliz Javier',
    area:'Servicio y Operaciones',
    categoria:'Experiencia del cliente',
    tipo:'Disruptiva',
    equipo:'Luis Troncoso, Carlos Feliz, Monnavel Carvajal, Minerva Frias',
    antes:[
      'Largos tiempos de espera: tiempos prolongados por parte del afiliado en canales tradicionales.',
      'Procesos Manuales: multiples validaciones y alta dependencia de intervencion humana.',
      'Saturacion Operativa: reprocesos constantes que afectan al equipo interno tecnico.',
      'Ineficiencia: friccion historica en el flujo de aprobacion medica.'
    ],
    despues:[
      'Se evoluciono de un proceso analogico y burocratico a una experiencia agil centrada en el afiliado, impulsada por Inteligencia Artificial y asistencia virtual.',
      'Canal de acceso: digital nativo, automatizado (WhatsApp PILI), en lugar de presencial o call center limitado.',
      'Carga del afiliado: sin friccion desde casa, eliminando traslados.',
      'Auditoria medica: IA Alfred con reglas 100% consistentes, sustituyendo el proceso manual sujeto a errores.'
    ],
    impacto:[
      '80% Reduccion en tiempo de procesamiento: de 4:37 horas a un promedio de 56 minutos.',
      'Estimacion de ahorros: RD$2,886,109 (Nov. 2024 a May. 2026).',
      '90% de NPS promedio sostenido.',
      '85% de Satisfaccion.'
    ]
  },
  'Anomatrace 1.0':{
    postulante:'Jose Gabriel Matos Parra',
    area:'Inteligencia PDSS',
    categoria:'Procesos y Eficiencia',
    tipo:'Disruptiva',
    equipo:'Jose Gabriel Matos Parra, Bellalina Rojas',
    antes:[
      'Gestion inicial de senales anomalas mediante archivos Excel, caso por caso.',
      'Proceso descentralizado, sin trazabilidad estructurada.',
      'Limitada visibilidad sobre el estado y gestion de los casos.',
      'Ausencia de monitoreo continuo y retroalimentacion oportuna a las areas.',
      'Modelo reactivo: el riesgo se identificaba despues de ocurrido el dano.'
    ],
    despues:[
      'AnomaTrace 1.0 — Torre de Control del Fraude.',
      'Aplicativo especializado que centraliza todas las senales de alerta en un unico entorno.',
      'Torre de Control con dashboard Power BI: seguimiento, cancelados, ahorro y productividad por analista.',
      'Blacklist activa de PSS con fraude confirmado que bloquea pagos futuros de forma automatica.',
      'Equipo dedicado al seguimiento de anomalias con metricas de rendimiento individual.'
    ],
    impacto:[
      'Fraude evitado de mas de RD$3MM de un total de RD$9MM detectado durante el periodo 2024-2025.',
      'Anomatrace permitio la cancelacion de 69 prestadores por fraude: ahorro estimado de RD$8MM anuales y ahorro acumulado de mas de RD$32MM.',
      '+760 PSS en lista negra con fraude confirmado y +96 PSS con carta compromiso.',
      'Incremento total de 1,200-1,400% en las reclamaciones diarias validadas por analista.'
    ]
  },
  'Automatizacion y Gestion de Solicitudes de Contrataciones de PSS':{
    postulante:'Luis Guillermo Gomez Cossio',
    area:'Gestion de Redes',
    categoria:'Procesos y Eficiencia',
    tipo:'Distinta',
    equipo:'Luis Guillermo Gomez Cossio',
    antes:[
      'Contratacion PSS: correos, Excel y sin visibilidad.',
      'Proceso de contratacion gestionado por correos electronicos y controles manuales dispersos con trazabilidad limitada.',
      'Sin visibilidad del estado de cada solicitud para el PSS ni para las areas internas.',
      'Reprocesos y duplicidad de notificaciones por falta de estandarizacion.',
      'Experiencia del prestador fragmentada con tiempos de respuesta prolongados.'
    ],
    despues:[
      'Flujo digital centralizado con Power Automate.',
      'Flujo digital que recibe, clasifica y asigna solicitudes automaticamente segun tipo de PSS y zona.',
      'Notificaciones automaticas a PSS y areas internas en cada cambio de estatus.',
      'Seguimiento de SLA en tiempo real con control de responsables por etapa.',
      'Coordinacion automatica entre todas las areas del proceso: evaluacion, tarificacion, Riesgo, capacitacion y cierre.'
    ],
    impacto:[
      '1,181 solicitudes digitalizadas.',
      'Tiempo promedio: antes 36 dias lab. Ahora el 25% ha cerrado en ≤4 dias lab y el 75% en ≤30 dias lab.',
      '57 PSS incorporados en 30 provincias y 53 especialidades.',
      'KPI propios del flujo: SLA al cierre 47%, media 24 dias lab., 25% cierres en ≤5 dias.'
    ]
  }
};

var C=[
  {id:'mag',g:'i',n:'Magnitud del Impacto',p:22.5,d:'How significant is the impact generated for the business (savings, revenue, time, satisfaction, costs, experience).',b:'Marginal or hard-to-sustain impact; effect limited to a single task or process.',m:'Moderate and verifiable impact on a relevant indicator or process.',a:'Substantial and demonstrable impact on one or more key business indicators.'},
  {id:'rel',g:'i',n:'Relevancia del Impacto para el Negocio',p:22.5,d:'How strategic is the impact and its alignment with key business priorities or challenges.',b:'Impact disconnected from current strategic priorities.',m:'Impact related to at least one relevant business priority or challenge.',a:'Impact directly aligned with critical strategic business priorities.'},
  {id:'esc',g:'i',n:'Scalability o Reach',p:22.5,d:'The potential of the initiative to expand or replicate across other areas, processes, markets, o clients.',b:'Solución acotada a un caso único, sin potencial claro de réplica.',m:'Solution replicable with moderate adjustments in other areas or similar processes.',a:'Highly scalable or directly replicable solution across multiple areas, markets, o clients.'},
  {id:'cua',g:'i',n:'Impacto Cualitativo',p:22.5,d:'Positive changes beyond quantifiable results (capabilities, culture, learning, reputation, collaboration).',b:'Sin evidencia de cambios cualitativos relevantes.',m:'Evidence of some positive qualitative change (learning, collaboration, etc.).',a:'Cambios cualitativos claros y significativos en varias dimensiones.'},
  {id:'ali',g:'o',n:'Alineación Estratégica',p:5,d:'Degree of alignment of the initiative with the declared strategy, values, o challenges of the organization.',b:'Little or no connection with the organizational strategy.',m:'Conexión parcial con algún pilar estratégico.',a:'Strong connection and coherence with the organizational strategy.'},
  {id:'inn',g:'o',n:'Nivel de Innovación',p:5,d:'Degree of novelty of the solution for the organization, industry, o market in its approach, technology, o model.',b:'Known or previously applied solution, with no novel elements.',m:'Solution with novel adaptations or improvements on something existing.',a:'Clearly novel or disruptive solution for the organization or sector.'}
];

var sc={};
C.forEach(function(c){sc[c.id]=null;});
var fin='', briefOpen=false;

function checkCode(){
  var code = document.getElementById('ev').value.trim().toUpperCase();
  var nameEl = document.getElementById('evaluator-name');
  var errorEl = document.getElementById('code-error');
  if(code.length === 0){nameEl.style.display='none';errorEl.style.display='none';return;}
  if(EVALUADORES[code]){
    nameEl.style.display='block';
    nameEl.innerHTML='✅ Bienvenido/a, <b>'+EVALUADORES[code]+'</b>';
    errorEl.style.display='none';
    markEvaluatedOptions();
  } else {
    nameEl.style.display='none';
    errorEl.style.display='block';
  }
}
function getKey(){
  var name=document.getElementById('ev').value.trim().toUpperCase();
  return 'evaluated_'+name;
}
function getEvaluated(){
  try{return JSON.parse(localStorage.getItem(getKey())||'[]');}catch(e){return[];}
}
function saveEvaluated(sol){
  var ev=getEvaluated();
  if(ev.indexOf(sol)===-1){ev.push(sol);localStorage.setItem(getKey(),JSON.stringify(ev));}
}
function markEvaluatedOptions(){
  var name=document.getElementById('ev').value.trim().toUpperCase();
  if(!name)return;
  var done=getEvaluated();
  var opts=document.querySelectorAll('#sol option');
  opts.forEach(function(o){
    if(done.indexOf(o.value)!==-1){o.text=o.value+' ✓';o.style.color='#16a34a';}
    else{o.text=o.value.replace(' ✓','');o.style.color='';}
  });
  var banner=document.getElementById('eval-banner');
  if(done.length>0){
    banner.style.display='block';
    banner.innerHTML='<b>Ya evaluadas ('+done.length+'):</b> '+done.map(function(s){return '<span style="display:inline-block;background:#dcfce7;color:#166534;border-radius:20px;padding:2px 10px;font-size:11px;font-weight:700;margin:2px 3px">'+s+' ✓</span>';}).join('');
  }else{banner.style.display='none';}
}
function toggleBrief(){
  briefOpen=!briefOpen;
  document.getElementById('brief-body').classList.toggle('open',briefOpen);
  document.getElementById('brief-arrow').classList.toggle('open',briefOpen);
}
function loadBrief(sol){
  var b=BRIEFS[sol];
  if(!b){document.getElementById('b-info').innerHTML='<div class="brief-info">Brief no disponible para esta solución.</div>';return;}
  document.getElementById('b-info').innerHTML=
    '<div class="brief-info"><b>Postulante:</b> '+b.postulante+'</div>'+
    '<div class="brief-info"><b>Área:</b> '+b.area+'</div>'+
    '<div class="brief-info"><b>Categoría:</b> '+b.categoria+'</div>'+
    '<div class="brief-info"><b>Tipo:</b> <span class="brief-tag '+(b.tipo==='Disruptiva'?'tag-green':'tag-blue')+'">'+b.tipo+'</span></div>'+
    '<hr class="brief-divider">'+
    '<div class="brief-info"><b>Equipo:</b> '+b.equipo+'</div>';
  document.getElementById('b-antes').innerHTML=b.antes.map(function(t){return '<div class="brief-bullet">'+t+'</div>';}).join('');
  document.getElementById('b-despues').innerHTML=b.despues.map(function(t){return '<div class="brief-bullet">'+t+'</div>';}).join('');
  document.getElementById('b-impacto').innerHTML=b.impacto.map(function(t){return '<div class="brief-impact">'+t+'</div>';}).join('');
}
function build(){
  ['i','o'].forEach(function(g){
    var el=document.getElementById('c'+g);el.innerHTML='';
    C.filter(function(c){return c.g===g;}).forEach(function(c){
      var div=document.createElement('div');div.className='crit';
      var opts=[0,50,100].map(function(v){
        var lbl=v===0?'BAJO':v===50?'MEDIO':'ALTO';
        var hint=v===0?c.b:v===50?c.m:c.a;
        var sel=sc[c.id]===v?' s'+v:'';
        return '<div class="opt'+sel+'" onclick="pick(\''+c.id+'\','+v+',this)" data-v="'+v+'"><span class="opt-pts">'+v+'</span><span class="opt-lbl">'+lbl+'</span><span class="opt-hint">'+hint+'</span></div>';
      }).join('');
      div.innerHTML='<div class="crit-head"><div class="crit-name">'+c.n+'</div><span class="crit-peso">'+c.p+'%</span><div class="crit-desc">'+c.d+'</div></div><div class="opt-table">'+opts+'</div><div class="crit-comment"><textarea id="t'+c.id+'" placeholder="Comentario opcional..."></textarea></div>';
      el.appendChild(div);
    });
  });
}
function pick(id,v,el){
  sc[id]=v;
  el.parentElement.querySelectorAll('.opt').forEach(function(b){b.className='opt'+(parseInt(b.dataset.v)===v?' s'+v:'');});
  upd();
}
function upd(){
  var done=C.every(function(c){return sc[c.id]!==null;});
  if(!done){document.getElementById('sdn').textContent='—';document.getElementById('sbr').style.width='0%';document.getElementById('sbdt').textContent='Score all criteria to see the result';return;}
  var t=0;C.forEach(function(c){t+=sc[c.id]*(c.p/100);});
  t=Math.round(t*10)/10;
  document.getElementById('sdn').textContent=t.toFixed(1);
  document.getElementById('sbr').style.width=t+'%';
  var imp=Math.round(C.filter(function(c){return c.g==='i';}).reduce(function(a,c){return a+sc[c.id]*(c.p/100);},0)*10)/10;
  var ot=Math.round(C.filter(function(c){return c.g==='o';}).reduce(function(a,c){return a+sc[c.id]*(c.p/100);},0)*10)/10;
  document.getElementById('sbdt').textContent='Impacto: '+imp.toFixed(1)+' pts · Otros criterios: '+ot.toFixed(1)+' pts';
}
function goTo(pg){
  if(pg===2){
    var e=document.getElementById('ev').value.trim();
    var s=document.getElementById('sol').value;
    if(!e||!s){alert('Por favor ingresa tu nombre y selecciona una solución para continuar.');return;}
    var key='evaluated_'+e.toLowerCase().split(' ').join('_');
    var done=JSON.parse(localStorage.getItem(key)||'[]');
    if(done.indexOf(s)!==-1){alert('Ya evaluaste esta solución. Por favor selecciona una diferente.');return;}
    document.getElementById('pt1').textContent=s;
    document.getElementById('pt2').textContent=s;
    loadBrief(s);build();upd();
  }
  if(pg===3){
    if(C.some(function(c){return sc[c.id]===null;})){alert('Please score all criteria to continue.');return;}
  }
  [1,2,3,4].forEach(function(p){document.getElementById('p'+p).classList.add('hidden');});
  document.getElementById('p'+pg).classList.remove('hidden');
  ['s1','s2','s3'].forEach(function(s,i){
    document.getElementById(s).className='step'+(i+1<pg?' done':i+1===pg?' active':'');
  });
}
function sf(v){
  fin=v;
  document.getElementById('fsi').className='fb'+(v==='si'?' fsi':'');
  document.getElementById('ftv').className='fb'+(v==='talvez'?' ftv':'');
  document.getElementById('fno').className='fb'+(v==='no'?' fno':'');
}
var POWER_AUTOMATE_URL = 'https://default379ca0ae251a416188ebe6cf903ae1.a6.environment.api.powerplatform.com:443/powerautomate/automations/direct/workflows/bb43e54e7cbe4b3793122e8482244ede/triggers/manual/paths/invoke?api-version=1&sp=%2Ftriggers%2Fmanual%2Frun&sv=1.0&sig=xUpN5EFFl36qy6nSKIdjPdNBjBWxYgT3-ZVcqrS-LMU';

function sub(){
  if(!fin){alert('Por favor indica si recomiendas este proyecto como finalista.');return;}
  var comentario=document.getElementById('ft').value.trim();
  if(!comentario){alert('El comentario es obligatorio.');return;}
  var sol=document.getElementById('sol').value;
  var e=document.getElementById('ev').value;
  var t=0;C.forEach(function(c){t+=sc[c.id]*(c.p/100);});
  t=(Math.round(t*10)/10).toFixed(1);

  var payload={
    Evaluador:e,
    Solucion:sol,
    Comentario:comentario,
    Finalista:{si:'Si',no:'No',talvez:'Tal vez'}[fin],
    Total:parseFloat(t),
    Fecha:new Date().toISOString()
  };
  C.forEach(function(c){
    payload[c.id+'_puntaje']=sc[c.id];
    payload[c.id+'_comentario']=document.getElementById('t'+c.id)?document.getElementById('t'+c.id).value.trim():'';
  });

  var btn=document.querySelector('#p3 .bp');
  if(btn){btn.disabled=true;btn.textContent='Enviando...';}

  fetch(POWER_AUTOMATE_URL,{
    method:'POST',
    headers:{'Content-Type':'application/json'},
    body:JSON.stringify(payload)
  }).then(function(r){
    if(!r.ok){throw new Error('HTTP '+r.status);}
    finalizeSubmit(sol,e,t,comentario);
  }).catch(function(err){
    if(btn){btn.disabled=false;btn.textContent='Enviar Evaluación';}
    alert('No se pudo guardar la evaluación en el servidor. Revisa tu conexión e intenta de nuevo.\n('+err.message+')');
  });
}

function finalizeSubmit(sol,e,t,comentario){
  saveEvaluated(sol);
  document.getElementById('cm').textContent='Evaluación de "'+sol+'" enviada por '+e+'.';
  var resEl=document.getElementById('res');resEl.innerHTML='';
  C.forEach(function(c){
    var l=sc[c.id]===0?'Bajo':sc[c.id]===50?'Medio':'Alto';
    var cls=sc[c.id]===0?'rl0':sc[c.id]===50?'rl50':'rl100';
    var com=document.getElementById('t'+c.id)?document.getElementById('t'+c.id).value:'';
    var row=document.createElement('div');row.className='res-row';
    row.innerHTML='<span class="res-name">'+c.n+(com?'<br><span style="font-size:11px;color:#888;font-style:italic">'+com+'</span>':'')+'</span><span class="res-lbl '+cls+'">'+l+'</span><span style="font-weight:700;color:#0a4d7c;min-width:40px;text-align:right">'+sc[c.id]+' pts</span>';
    resEl.appendChild(row);
  });
  document.getElementById('r-total').textContent=t+' / 100';
  document.getElementById('r-comment').textContent=comentario;
  document.getElementById('r-fin').textContent={si:'Sí',no:'No',talvez:'Tal vez'}[fin];
  [1,2,3].forEach(function(p){document.getElementById('p'+p).classList.add('hidden');});
  document.getElementById('p4').classList.remove('hidden');
  ['s1','s2','s3'].forEach(function(s){document.getElementById(s).className='step done';});
}
function rst(){
  C.forEach(function(c){sc[c.id]=null;});fin='';briefOpen=false;
  document.getElementById('brief-body').classList.remove('open');
  document.getElementById('brief-arrow').classList.remove('open');
  document.getElementById('ev').value='';
  document.getElementById('sol').value='';
  document.getElementById('ft').value='';
  markEvaluatedOptions();
  goTo(1);
}
</script>
</body>
</html>
