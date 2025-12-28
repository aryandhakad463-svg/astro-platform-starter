<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>ARW Study</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; background: #f4f6f8; }
    header { background: #1e293b; color: white; padding: 15px; text-align: center; }
    .container { padding: 20px; }
    .card { background: white; padding: 20px; margin-bottom: 15px; border-radius: 10px; box-shadow: 0 4px 10px rgba(0,0,0,0.1); }
    button { padding: 10px 15px; border: none; border-radius: 8px; background: #2563eb; color: white; cursor: pointer; }
    button:hover { background: #1d4ed8; }
    .hidden { display: none; }
    .whatsapp { position: fixed; bottom: 20px; right: 20px; background: #25D366; color: white; padding: 12px 16px; border-radius: 50px; text-decoration: none; font-weight: bold; }
  </style>
</head>
<body><header>
  <h1>ARW Study</h1>
  <p>Smart Study for NEET | JEE | Board</p>
</header><div class="container">  <!-- Mode Selection -->  <div id="modes" class="card">
    <h2>Select Mode / मोड चुनें</h2>
    <button onclick="openMode('neet')">NEET</button>
    <button onclick="openMode('jee')">JEE</button>
    <button onclick="openMode('board')">BOARD</button>
  </div>  <!-- NEET -->  <div id="neet" class="card hidden">
    <h2>NEET Mode</h2>
    <button onclick="openPlan('neet20')">20 Din Challenge</button>
    <button onclick="openPlan('neet8')">Daily 8 Hour Study</button>
    <button onclick="openPlan('neetSyl')">NEET Syllabus</button>
  </div>  <!-- JEE -->  <div id="jee" class="card hidden">
    <h2>JEE Mode</h2>
    <button onclick="openPlan('jee20')">20 Din Challenge</button>
    <button onclick="openPlan('jee8')">Daily 8 Hour Study</button>
    <button onclick="openPlan('jeeSyl')">JEE Syllabus</button>
  </div>  <!-- Board -->  <div id="board" class="card hidden">
    <h2>Board Mode</h2>
    <button onclick="openPlan('board20')">20 Din Challenge</button>
    <button onclick="openPlan('board8')">Daily 8 Hour Study</button>
    <button onclick="openPlan('boardSyl')">Board Syllabus</button>
  </div>  <!-- Plan -->  <div id="plan" class="card hidden">
    <h2 id="planTitle"></h2>
    <p>Topic select karo. Time ke andar complete nahi hua to topic lock ho jayega (demo).</p>
    <ul>
      <li>Topic 1</li>
      <li>Topic 2</li>
      <li>Topic 3</li>
    </ul>
    <button onclick="goBack()">Back</button>
  </div></div><a class="whatsapp" href="https://wa.me/91XXXXXXXXXX" target="_blank">WhatsApp</a>

<script>
  function openMode(mode) {
    document.getElementById('modes').classList.add('hidden');
    document.getElementById(mode).classList.remove('hidden');
  }

  function openPlan(plan) {
    document.querySelectorAll('.card').forEach(c => c.classList.add('hidden'));
    document.getElementById('plan').classList.remove('hidden');
    document.getElementById('planTitle').innerText = plan + ' Plan';
  }

  function goBack() {
    location.reload();
  }
</script></body>
</html>
