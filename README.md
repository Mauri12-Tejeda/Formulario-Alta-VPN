

<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Solicitud de Alta de VPN</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Libre+Franklin:wght@500;700&display=swap" rel="stylesheet">
  <style>
    * { box-sizing: border-box; }
    body { margin: 0; background: #f3f5f8; font-family: Inter, sans-serif; }

    .sheet {
      width: 210mm; min-height: 297mm; margin: 12mm auto; background: #fff; padding: 11mm;
      border: 2px solid #1a1a1a; border-radius: 8px; box-shadow: 0 10px 30px rgba(0,0,0,.12);
    }

    .header-wrap { border: 1.6px solid #343a40; border-radius: 6px; overflow: hidden; }
    .header { display: grid; grid-template-columns: 170px 1fr; align-items: center; }
    .logo-column { border-right: 1.6px solid #343a40; padding: 8px; display: grid; grid-template-columns: 1fr 1fr; gap: 8px; }
    .logo { height: 44px; border: 1.2px solid #343a40; border-radius: 4px; display: flex; align-items: center; justify-content: center; font-size: 10px; }
    .title-column { text-align: center; padding: 16px 8px; }
    .title-main { font-family: "Libre Franklin", Inter, sans-serif; font-weight: 700; font-size: 20px; }
    .title-sub { margin-top: 4px; font-weight: 600; font-size: 14px; }

    .bar-box { margin-top: 8mm; border: 1.4px solid #343a40; border-radius: 6px; overflow: hidden; }
    .bar { display: grid; grid-template-columns: auto 1fr; }
    .bar-label { padding: 6px 10px; background: #e9eef6; font-weight: 700; border-right: 1.4px solid #343a40; }
    .bar-fill { background: #fff; }

    table.grid { width: 100%; border-collapse: collapse; }
    table.grid th, table.grid td { border: 1px solid #343a40; padding: 6px 7px; font-size: 12.2px; }
    table.grid th { background: #f0f3f8; text-align: left; font-weight: 600; }

    .input-line { width: 100%; border: none; border-bottom: 1px dashed #7e8790; padding: 2px 0; font: inherit; outline: none; }
    input[type="date"] { width: 100%; border: none; font: inherit; }

    .check { position: relative; display: flex; align-items: center; gap: 6px; cursor: pointer; }
    .check input {
      appearance: none;
       width: 14px;
       height: 14px;
       border: 1.4px solid #343a40;
       border-radius: 2px;
       margin: 0;
       cursor: pointer;
      }
    .check input:checked {
      background-color: #0067c6;
    }


    textarea { width: 100%; border: none; border-top: 1px dashed #7e8790; padding: 8px 6px; min-height: 28mm; font: inherit; resize: none; }

    .toolbar { position: sticky; bottom: 0; display: flex; gap: 8px; justify-content: center; width: 210mm; margin: 0 auto; padding: 10px 0 18px; }
    .btn { background: #0067c6; color: #fff; border: 0; border-radius: 10px; padding: 10px 14px; font-weight: 700; cursor: pointer; }

    @media print { .toolbar { display: none !important; } }
  </style>
</head>
<body>
  <div class="toolbar">
    <button id="btnPdf" class="btn">Convertir a PDF</button>
    <button id="btnClear" class="btn" style="background:#6c757d;">Limpiar Formulario</button>
  </div>

  <section id="documento" class="sheet">
    <!-- Encabezado principal -->
    <div class="header-wrap">
      <div class="header">
        <div class="logo-column">
          <div class="logo">Buenos Aires Ciudad</div>
          <div class="logo">BA</div>
        </div>
        <div class="title-column">
          <div class="title-main">Seguridad Informática</div>
          <div class="title-sub">Ministerio de Seguridad - CABA</div>
        </div>
      </div>
    </div>

    <!-- Solicitud de alta de VPN -->
    <div class="bar-box">
      <div class="bar">
        <div class="bar-label">SOLICITUD DE ALTA DE VPN</div>
        <div class="bar-fill"></div>
      </div>
      <table class="grid">
        <tr>
          <th>Fecha de Solicitud:</th>
          <td><input type="date"></td>
          <th>Referido a CCOO:</th>
          <td><input class="input-line" type="text"></td>
        </tr>
      </table>
    </div>

    <!-- Datos del solicitante -->
    <div class="bar-box">
      <div class="bar">
        <div class="bar-label">DATOS DEL SOLICITANTE</div>
        <div class="bar-fill"></div>
      </div>
      <table class="grid">
        <tr>
          <th>Apellido y Nombre</th>
          <td colspan="3"><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>Usuario de Dominio</th>
          <td><input class="input-line" type="text"></td>
          <th>Nº de CUIL</th>
          <td><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>Cargo</th>
          <td><input class="input-line" type="text"></td>
          <th>LP Nº</th>
          <td><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>División / Departamento</th>
          <td colspan="3"><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>Dependencia</th>
          <td colspan="3"><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>Calle</th>
          <td><input class="input-line" type="text"></td>
          <th>Nº</th>
          <td><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>E‑Mail</th>
          <td><input class="input-line" type="email"></td>
          <th>Teléfono / Interno</th>
          <td><input class="input-line" type="text"></td>
        </tr>
      </table>
    </div>

    <!-- Sistemas/Servidores -->
   <!-- Sistemas/Servidores -->
<div class="bar-box">
  <div class="bar">
    <div class="bar-label">SISTEMAS O SERVIDORES A LOS CUALES ACCEDERÁ A TRAVÉS DE LA VPN</div>
    <div class="bar-fill"></div>
  </div>
  <div class="checks">
    <label class="check">
      <input type="checkbox"><span class="box"></span>
      <span>Servicios Policiales <span class="hint">(SIRHU, SILOL, SMLAM, SIGET, SIGENO, SIFOR, CREA, GAP, etc.)</span></span>
    </label>
    <label class="check">
      <input type="checkbox"><span class="box"></span>
      <span>Servicios ASI <span class="hint">(SADE, SIGAF, SIGAFWEB, BAC, etc.)</span></span>
    </label>
    <label class="check">
      <input type="checkbox"><span class="box"></span>
      <span>SISEP</span>
    </label>
    <label class="check">
      <input type="checkbox"><span class="box"></span>
      <span>Cámaras ULTRA-IP</span>
    </label>
    <label class="check">
      <input type="checkbox"><span class="box"></span>
      <span>Carpeta Compartida</span>
    </label>
    <label class="check">
      <input type="checkbox"><span class="box"></span>
      <span>Otros</span>
    </label>
  </div>
  <table class="grid notes">
    <tr><th>Detalle adicional (URLs / Servidores / Observaciones)</th></tr>
    <tr><td><textarea></textarea></td></tr>
  </table>
</div>


    <!-- Responsable de la dependencia -->
    <div class="bar-box">
      <div class="bar">
        <div class="bar-label">RESPONSABLE DE LA DEPENDENCIA</div>
        <div class="bar-fill"></div>
      </div>
      <table class="grid">
        <tr>
          <th>Apellido y Nombre</th>
          <td colspan="3"><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>Cargo</th>
          <td><input class="input-line" type="text"></td>
          <th>LP</th>
          <td><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>División / Departamento</th>
          <td colspan="3"><input class="input-line" type="text"></td>
        </tr>
        <tr>
          <th>E‑Mail</th>
          <td><input class="input-line" type="email"></td>
          <th>Teléfono / Interno</th>
          <td><input class="input-line" type="text"></td>
        </tr>
      </table>
    </div>
  </section>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.9.3/html2pdf.bundle.min.js"></script>
  <script>
    document.getElementById('btnPdf').addEventListener('click', () => {
      const el = document.getElementById('documento');
      const opt = {
        margin: 0,
        filename: 'Solicitud_Alta_VPN.pdf',
        image: { type: 'jpeg', quality: 0.98 },
        html2canvas: { scale: 2, useCORS: true },
        jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait' }
      };
      html2pdf().set(opt).from(el).save();
    });

    document.getElementById('btnClear').addEventListener('click', () => {
      document.querySelectorAll('input, textarea').forEach(el => {
        if(el.type === 'checkbox' || el.type === 'radio') {
          el.checked = false;
        } else {
          el.value = '';
        }
      });
    });
  </script>
</body>
</html>
