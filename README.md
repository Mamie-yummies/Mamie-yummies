<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Menu Yummies</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="icon" href="logo.png" type="image/png" />
</head>
<body class="bg-gray-50 font-sans">

  <!-- Header -->
  <header class="bg-purple-600 text-white p-4 flex items-center justify-between">
    <div class="flex items-center gap-2">
      <img src="logo.png" alt="Logo" class="h-12 w-12 object-contain">
      <h1 class="text-2xl font-bold">Yummies Menu</h1>
    </div>
  </header>

  <main class="p-4 max-w-3xl mx-auto">

    <!-- Families -->
    <div class="space-y-4">
      
      <!-- Plat du jour -->
      <div>
        <button onclick="toggleSection('platDuJour')" class="w-full text-left p-4 bg-purple-200 font-semibold rounded hover:bg-purple-300">
          Plat du jour
        </button>
        <div id="platDuJour" class="hidden mt-2 space-y-2">
          <div>
            <button onclick="toggleSection('lundi')" class="w-full text-left p-2 bg-purple-100 rounded hover:bg-purple-200">Lundi</button>
            <div id="lundi" class="hidden p-2 pl-4 space-y-1">
              <p>Yassa poulet : 3000f</p>
              <p>Fakoye : 3000f</p>
            </div>
          </div>
          <div>
            <button onclick="toggleSection('mardi')" class="w-full text-left p-2 bg-purple-100 rounded hover:bg-purple-200">Mardi</button>
            <div id="mardi" class="hidden p-2 pl-4 space-y-1">
              <p>Maffé : 3000f</p>
              <p>Thiep poisson ou poulet : 3000f</p>
            </div>
          </div>
          <div>
            <button onclick="toggleSection('mercredi')" class="w-full text-left p-2 bg-purple-100 rounded hover:bg-purple-200">Mercredi</button>
            <div id="mercredi" class="hidden p-2 pl-4 space-y-1">
              <p>Saga saga : 3000f</p>
              <p>Sauce tomate : 3000f</p>
            </div>
          </div>
          <div>
            <button onclick="toggleSection('jeudi')" class="w-full text-left p-2 bg-purple-100 rounded hover:bg-purple-200">Jeudi</button>
            <div id="jeudi" class="hidden p-2 pl-4 space-y-1">
              <p>Woudjila : 3000f</p>
              <p>Atieké : 3000f</p>
            </div>
          </div>
          <div>
            <button onclick="toggleSection('vendredi')" class="w-full text-left p-2 bg-purple-100 rounded hover:bg-purple-200">Vendredi</button>
            <div id="vendredi" class="hidden p-2 pl-4 space-y-1">
              <p>Tôt : 3000f</p>
              <p>Thiep poisson ou poulet : 3000f</p>
            </div>
          </div>
          <a href="https://wa.me/22372910000" target="_blank" class="mt-2 inline-block bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">Commander sur WhatsApp</a>
        </div>
      </div>

      <!-- Sandwich -->
      <div>
        <button onclick="toggleSection('sandwich')" class="w-full text-left p-4 bg-purple-200 font-semibold rounded hover:bg-purple-300">
          Nos Sandwich
        </button>
        <div id="sandwich" class="hidden mt-2 p-2 pl-4 space-y-1">
          <p>Sandwich viande haché : 1000f</p>
          <p>Sandwich poulet : 2000f</p>
          <p>Sandwich Thon : 2000f</p>
          <p>Sandwich foie : 2000f</p>
          <p>Sandwich rognon : 2000f</p>
          <p>Sandwich Steak : 1500f</p>
          <a href="https://wa.me/22372910000" target="_blank" class="mt-2 inline-block bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">Commander sur WhatsApp</a>
        </div>
      </div>

      <!-- Shawarma -->
      <div>
        <button onclick="toggleSection('shawarma')" class="w-full text-left p-4 bg-purple-200 font-semibold rounded hover:bg-purple-300">
          Nos Shawarmas
        </button>
        <div id="shawarma" class="hidden mt-2 p-2 pl-4 space-y-1">
          <p>Shawarma poulet : 2500f</p>
          <p>Shawarma BŒUF : 2000f</p>
          <a href="https://wa.me/22372910000" target="_blank" class="mt-2 inline-block bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">Commander sur WhatsApp</a>
        </div>
      </div>

      <!-- Tacos -->
      <div>
        <button onclick="toggleSection('tacos')" class="w-full text-left p-4 bg-purple-200 font-semibold rounded hover:bg-purple-300">
          Nos Tacos
        </button>
        <div id="tacos" class="hidden mt-2 p-2 pl-4 space-y-1">
          <p>Tacos viande : 2500f</p>
          <p>Le régal : 3500f</p>
          <p>Tacos yummies : 4500f</p>
          <a href="https://wa.me/22372910000" target="_blank" class="mt-2 inline-block bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">Commander sur WhatsApp</a>
        </div>
      </div>

      <!-- Burger -->
      <div>
        <button onclick="toggleSection('burger')" class="w-full text-left p-4 bg-purple-200 font-semibold rounded hover:bg-purple-300">
          Nos Burger
        </button>
        <div id="burger" class="hidden mt-2 p-2 pl-4 space-y-1">
          <p>Burger smile : 3000f</p>
          <p>Burger chicken Masala : 3000f</p>
          <p>Burger yummies : 4000f</p>
          <a href="https://wa.me/22372910000" target="_blank" class="mt-2 inline-block bg-green-500 text-white px-4 py-2 rounded hover:bg-green-600">Commander sur WhatsApp</a>
        </div>
      </div>

    </div>
  </main>

  <script>
    function toggleSection(id) {
      const section = document.getElementById(id);
      section.classList.toggle('hidden');
    }
  </script>
</body>
</html>
