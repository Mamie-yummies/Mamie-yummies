## Hi there 👋

<!--
**Mamie-yummies/Mamie-yummies** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ..
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Menu Yummies</title>
  <link rel="icon" href="logo.png" type="image/png">
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-white text-gray-800 font-sans">

  <header class="bg-purple-700 text-white p-4 flex items-center">
    <img src="logo.png" alt="Logo" class="h-12 mr-4">
    <h1 class="text-2xl font-bold">Cherry's Yummies</h1>
  </header>

  <main class="p-4 max-w-3xl mx-auto">

    <!-- Familles -->
    <h2 class="text-xl font-bold mb-4">Nos Menus</h2>
    <div id="menu-families" class="grid grid-cols-2 gap-4 mb-6">
      <button class="family-btn bg-purple-200 hover:bg-purple-300 p-3 rounded" data-family="plats-jour">Plat du jour</button>
      <button class="family-btn bg-purple-200 hover:bg-purple-300 p-3 rounded" data-family="sandwich">Sandwichs</button>
      <button class="family-btn bg-purple-200 hover:bg-purple-300 p-3 rounded" data-family="shawarma">Shawarmas</button>
      <button class="family-btn bg-purple-200 hover:bg-purple-300 p-3 rounded" data-family="tacos">Tacos</button>
      <button class="family-btn bg-purple-200 hover:bg-purple-300 p-3 rounded" data-family="burger">Burgers</button>
    </div>

    <!-- Contenu des menus -->
    <div id="menu-content"></div>

  </main>

<script>
const menuData = {
  "plats-jour": {
    "Lundi": [
      {name: "Yassa poulet", price: 3000},
      {name: "Fakoye", price: 3000}
    ],
    "Mardi": [
      {name: "Maffé", price: 3000},
      {name: "Thiep poisson ou poulet", price: 3000}
    ],
    "Mercredi": [
      {name: "Saga saga", price: 3000},
      {name: "Sauce tomate", price: 3000}
    ],
    "Jeudi": [
      {name: "Woudjila", price: 3000},
      {name: "Atieké", price: 3000}
    ],
    "Vendredi": [
      {name: "Tôt", price: 3000},
      {name: "Tiep poisson ou poulet", price: 3000}
    ]
  },
  "sandwich": [
    {name: "Sandwich viande haché", price: 1000},
    {name: "Sandwich poulet", price: 2000},
    {name: "Sandwich Thon", price: 2000},
    {name: "Sandwich foie", price: 2000},
    {name: "Sandwich rognon", price: 2000},
    {name: "Sandwich Steak", price: 1500}
  ],
  "shawarma": [
    {name: "Shawarma poulet", price: 2500},
    {name: "Shawarma BŒUF", price: 2000}
  ],
  "tacos": [
    {name: "Tacos viande", price: 2500},
    {name: "Le régal", price: 3500},
    {name: "Tacos yummies", price: 4500}
  ],
  "burger": [
    {name: "Burger smile", price: 3000},
    {name: "Burger chicken Masala", price: 3000},
    {name: "Burger yummies", price: 4000}
  ]
};

const menuContent = document.getElementById('menu-content');

function showFamily(family) {
  menuContent.innerHTML = ''; // clear previous content
  if(family === "plats-jour") {
    // Affiche les jours
    Object.keys(menuData[family]).forEach(day => {
      const dayBtn = document.createElement('button');
      dayBtn.textContent = day;
      dayBtn.className = "bg-purple-100 hover:bg-purple-200 p-2 m-1 rounded";
      dayBtn.onclick = () => showPlatsDuJour(day);
      menuContent.appendChild(dayBtn);
    });
  } else {
    menuData[family].forEach(item => {
      menuContent.appendChild(createPlatElement(item));
    });
  }
}

function showPlatsDuJour(day) {
  menuContent.innerHTML = `<h3 class="text-lg font-bold mb-2">${day}</h3>`;
  menuData['plats-jour'][day].forEach(item => {
    menuContent.appendChild(createPlatElement(item));
  });
}

function createPlatElement(item) {
  const div = document.createElement('div');
  div.className = "border p-3 mb-2 rounded flex justify-between items-center";
  div.innerHTML = `
    <span>${item.name} - ${item.price} F CFA</span>
    <button class="bg-green-500 text-white px-3 py-1 rounded hover:bg-green-600"
      onclick="passerCommande('${item.name}', ${item.price})">Commander</button>
  `;
  return div;
}

function passerCommande(plat, price) {
  const livraison = confirm("Voulez-vous que la commande soit livrée ? Cliquez 'Annuler' si vous souhaitez manger sur place.");
  let message = `Bonjour, je souhaite commander: ${plat} pour ${price} F CFA.`;
  if(livraison){
    const location = prompt("Veuillez envoyer votre emplacement pour la livraison (adresse ou description) :");
    if(location) {
      message += ` Livraison à : ${location}`;
    }
  }
  // Ouvre WhatsApp avec le message
  const whatsappNumber = "72910000";
  const url = `https://wa.me/${whatsappNumber}?text=${encodeURIComponent(message)}`;
  window.open(url, '_blank');
}

// Event listeners
document.querySelectorAll('.family-btn').forEach(btn => {
  btn.addEventListener('click', () => showFamily(btn.dataset.family));
});
</script>

</body>
</html>
