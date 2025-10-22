<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>FoodieFiesta Delight - Menu Restaurant</title>
  <link rel="icon" href="images/logo.png" type="image/png" />
  
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  
  <!-- Feather Icons -->
  <script src="https://unpkg.com/feather-icons"></script>

  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#FF6B6B',
            secondary: '#4ECDC4',
          },
        },
      },
    };
  </script>
</head>

<body class="bg-gray-50">
  <!-- Navbar -->
  <custom-navbar></custom-navbar>

  <!-- Contenu principal -->
  <main class="container mx-auto px-4 py-8">
    <div class="text-center mb-12">
      <h1 class="text-4xl font-bold text-primary mb-4">Notre Menu Délicieux</h1>
      <p class="text-gray-600 max-w-2xl mx-auto">
        Découvrez nos plats savoureux et commandez en un clic !
      </p>
    </div>

    <!-- Grille des catégories -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

      <!-- Plats du Jour -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden transition-transform duration-300 hover:scale-105">
        <div class="bg-primary p-6">
          <h2 class="text-white text-xl font-bold">Plats du Jour</h2>
        </div>
        <div class="p-6">
          <p class="text-gray-600 mb-4">Découvrez nos spécialités quotidiennes</p>
          <a href="plats-du-jour.html" class="inline-flex items-center px-4 py-2 bg-secondary text-white rounded-lg hover:bg-opacity-90 transition">
            <span>Voir les plats</span>
            <i data-feather="arrow-right" class="ml-2"></i>
          </a>
        </div>
      </div>

      <!-- Sandwich -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden transition-transform duration-300 hover:scale-105">
        <div class="bg-primary p-6">
          <h2 class="text-white text-xl font-bold">Nos Sandwichs</h2>
        </div>
        <div class="p-6">
          <p class="text-gray-600 mb-4">Des sandwichs frais et savoureux</p>
          <a href="sandwich.html" class="inline-flex items-center px-4 py-2 bg-secondary text-white rounded-lg hover:bg-opacity-90 transition">
            <span>Voir les options</span>
            <i data-feather="arrow-right" class="ml-2"></i>
          </a>
        </div>
      </div>

      <!-- Shawarmas -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden transition-transform duration-300 hover:scale-105">
        <div class="bg-primary p-6">
          <h2 class="text-white text-xl font-bold">Nos Shawarmas</h2>
        </div>
        <div class="p-6">
          <p class="text-gray-600 mb-4">Shawarmas préparés avec soin</p>
          <a href="shawarma.html" class="inline-flex items-center px-4 py-2 bg-secondary text-white rounded-lg hover:bg-opacity-90 transition">
            <span>Voir les options</span>
            <i data-feather="arrow-right" class="ml-2"></i>
          </a>
        </div>
      </div>

      <!-- Tacos -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden transition-transform duration-300 hover:scale-105">
        <div class="bg-primary p-6">
          <h2 class="text-white text-xl font-bold">Nos Tacos</h2>
        </div>
        <div class="p-6">
          <p class="text-gray-600 mb-4">Tacos gourmands à savourer</p>
          <a href="tacos.html" class="inline-flex items-center px-4 py-2 bg-secondary text-white rounded-lg hover:bg-opacity-90 transition">
            <span>Voir les options</span>
            <i data-feather="arrow-right" class="ml-2"></i>
          </a>
        </div>
      </div>

      <!-- Burgers -->
      <div class="bg-white rounded-lg shadow-lg overflow-hidden transition-transform duration-300 hover:scale-105">
        <div class="bg-primary p-6">
          <h2 class="text-white text-xl font-bold">Nos Burgers</h2>
        </div>
        <div class="p-6">
          <p class="text-gray-600 mb-4">Burgers juteux et copieux</p>
          <a href="burger.html" class="inline-flex items-center px-4 py-2 bg-secondary text-white rounded-lg hover:bg-opacity-90 transition">
            <span>Voir les options</span>
            <i data-feather="arrow-right" class="ml-2"></i>
          </a>
        </div>
      </div>

    </div>
  </main>

  <!-- Footer -->
  <custom-footer></custom-footer>

  <!-- Scripts -->
  <script src="components/navbar.js"></script>
  <script src="components/footer.js"></script>
  <script src="script.js"></script>
  <script>
    feather.replace();
  </script>
</body>
</html>
