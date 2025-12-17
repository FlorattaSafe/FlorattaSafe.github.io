# FlorattaSafe.github.io
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Floratta Safe</title>

  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Poppins:wght@400;600&display=swap" rel="stylesheet" />

  <style>
    /* ================= PALETA ================= */
    :root {
      --rosa: #f4b6c2;
      --verde-musgo: #4b6043;
      --branco: #fff;
      --cinza-claro: #f9f9f9;
    }

    /* ================= RESET ================= */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: var(--cinza-claro);
      color: var(--verde-musgo);
      line-height: 1.6;
    }

    /* ================= NAV ================= */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background-color: var(--rosa);
      display: flex;
      justify-content: center;
      gap: 20px;
      padding: 10px;
      z-index: 1000;
      box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    }

    nav a {
      color: var(--verde-musgo);
      text-decoration: none;
      font-weight: 600;
    }

    nav a:hover {
      color: var(--branco);
    }

    /* ================= HEADER ================= */
    header {
      margin-top: 60px;
      background-color: var(--verde-musgo);
      color: var(--branco);
      padding: 20px 40px;
      text-align: center;
    }

    .header-content {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .logo {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      border: 3px solid var(--rosa);
      object-fit: cover;
    }

    header h1 {
      font-family: 'Playfair Display', serif;
      font-size: 2.5rem;
    }

    .titulo p {
      font-style: italic;
    }

    /* ================= SEÇÕES ================= */
    section {
      padding: 80px 15% 50px;
      background-color: var(--branco);
      margin: 30px auto;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    section h2 {
      font-family: 'Playfair Display', serif;
      border-bottom: 3px solid var(--rosa);
      margin-bottom: 20px;
      display: inline-block;
    }

    section p {
      text-align: justify;
    }

    /* ================= EQUIPE ================= */
    .equipe {
      display: flex;
      gap: 30px;
      flex-wrap: wrap;
      justify-content: center;
      margin-top: 30px;
    }

    .membro {
      background-color: var(--cinza-claro);
      border-radius: 10px;
      padding: 20px;
      text-align: center;
      width: 220px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.1);
    }

    .membro img {
      width: 90px;
      height: 100px;
      border-radius: 50%;
      border: 3px solid var(--rosa);
      object-fit: cover;
      margin-bottom: 10px;
    }

    /* ================= TABELA ================= */
    table {
      width: 100%;
      border-collapse: collapse;
      margin-bottom: 20px;
      font-size: 0.95rem;
    }

    caption {
      font-weight: 600;
      margin-bottom: 10px;
      font-family: 'Playfair Display', serif;
    }

    th, td {
      border: 1px solid #e5e5e5;
      padding: 12px;
      text-align: left;
    }

    thead {
      background-color: var(--rosa);
    }

    tbody tr:nth-child(even) {
      background-color: var(--cinza-claro);
    }

    /* ================= FOOTER ================= */
    footer {
      background-color: var(--verde-musgo);
      color: var(--branco);
      text-align: center;
      padding: 20px;
      margin-top: 40px;
    }

    /* ================= RESPONSIVO ================= */
    @media (max-width: 768px) {
      section {
        padding: 60px 10%;
      }

      .equipe {
        flex-direction: column;
        align-items: center;
      }

      .header-content {
        flex-direction: column;
      }
    }

    /* ================= PRODUTO CARROSSEL ================= */
    .carrossel-container {
      position: relative;
      max-width: 840px;
      margin: 40px auto 0;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .carrossel-wrapper {
      overflow: hidden;
      flex: 1;
      border-radius: 16px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
    }

    .carrossel {
      display: flex;
      transition: transform 0.5s ease;
      gap: 20px;
      padding: 20px;
    }

    .carrossel-card {
      flex: 0 0 260px;
      background-color: var(--cinza-claro);
      border-radius: 16px;
      overflow: hidden;
      box-shadow: 0 10px 25px rgba(0,0,0,0.15);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      cursor: grab;
    }

    .carrossel-card:hover {
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0,0,0,0.25);
    }

    .carrossel-card img {
      width: 100%;
      height: 260px;
      object-fit: cover;
    }

    .produto-info {
      padding: 15px;
      text-align: center;
    }

    .produto-info h3 {
      margin-bottom: 8px;
      font-family: 'Playfair Display', serif;
    }

    /* Botões */
    .btn {
      background-color: var(--rosa);
      border: none;
      color: var(--verde-musgo);
      font-size: 2rem;
      padding: 10px 14px;
      border-radius: 50%;
      cursor: pointer;
      transition: background-color 0.3s ease;
      user-select: none;
      flex-shrink: 0;
    }

    .btn:hover {
      background-color: var(--verde-musgo);
      color: var(--branco);
    }

    /* RESPONSIVO CARROSSEL */
    @media (max-width: 768px) {
      .carrossel-card {
        flex: 0 0 220px;
      }

      .carrossel-container {
        max-width: 100%;
        padding: 0 10px;
      }
    }
  </style>
</head>

<body>
  <nav>
    <a href="#inicio">Início</a>
    <a href="#sobre">Sobre</a>
    <a href="#historia">História</a>
    <a href="#equipe">Equipe</a>
    <a href="#ingredientes">Ingredientes</a>
    <a href="#produto">Produto</a>
    <a href="#preco">Preço</a>
    <a href="#sustentabilidade">Sustentabilidade</a>
    <a href="#contato">Contato</a>
  </nav>

  <header>
    <div class="header-content">
      <img src="logo.jpeg" alt="Logo Floratta Safe" class="logo" />
      <div class="titulo">
        <h1>Floratta Safe</h1>
        <p>O ar que protege: respire proteção, espalhe cuidado.</p>
      </div>
    </div>
  </header>

  <section id="inicio">
    <h2>Bem-vindo(a)</h2>
    <p>
      Olá, a Floratta Safe é uma startup dedicada a proteger o ar, você e sua família contra os insetos que os rodeiam. Nosso repelente foi desenvolvido para atender a todos os públicos, desde os mais jovens até os mais experientes. Para sua formulação, utilizamos óleos e extratos de plantas retirados diretamente da natureza, sempre com respeito ao meio ambiente e com o propósito de aproximá-lo cada vez mais de quem faz uso do produto.
    </p>
  </section>

  <section id="sobre">
    <h2>Sobre</h2>
    <p>
      Nós somos a <strong>Floratta Safe</strong>. Criamos um repelente natural, ecológico e seguro para todos os públicos, com um diferencial inovador: ele pode ser aplicado diretamente no ar-condicionado. Assim, o ar que refresca também protege. Sem cheiro forte, sem química nociva — apenas natureza e tecnologia trabalhando juntas. <strong>Floratta Safe: o ar que protege você e o planeta.</strong> Vivemos em um mundo onde o conforto e a saúde devem andar juntos. A Floratta Safe nasceu com a missão de proteger as pessoas de forma natural, sem prejudicar o meio ambiente. Desenvolvemos um repelente 100% natural, livre de substâncias químicas agressivas, que alia bem-estar, sustentabilidade e inovação. Nosso produto transforma o ar em um escudo invisível contra mosquitos e insetos, sendo ideal para casas, escolas, hospitais, escritórios e veículos, garantindo proteção contínua para crianças, adultos e animais de estimação. Com tecnologia sustentável e ingredientes de origem vegetal, a Floratta Safe une ciência, natureza e inovação para oferecer um novo conceito em repelência ambiental. <strong>Respire proteção, espalhe cuidado.</strong>
    </p>
  </section>

  <section id="historia">
    <h2>Nossa História</h2>
    <p>
      A ideia inicial de criar um repelente natural surgiu a partir da observação do nosso cotidiano, especialmente de como bueiros e canais abertos podem comprometer a saúde da população. Em nosso município, há um grande desafio relacionado à saúde pública, e a população, sobretudo a de baixa renda, sofre intensamente com os efeitos dos insetos que impactam negativamente a vida dos cidadãos.  

      Essa iniciativa foi ainda mais fortalecida graças ao projeto Ceará Científico, no qual grande parte da equipe participou de um grupo cujo tema era: “Como os agrotóxicos interferem na vida dos indivíduos”. A partir dessa experiência, tornou-se evidente que não apenas os agrotóxicos são prejudiciais à sociedade, mas também o uso de produtos químicos comumente presentes no cotidiano dos cidadãos representa riscos à saúde.  

      Um exemplo claro disso é o uso de repelentes, que muitas vezes passam despercebidos. Por serem comercializados como itens de proteção familiar, não recebem a devida atenção quanto à sua composição química e, consequentemente, não são vistos como nocivos à saúde.  

      Diante dessa realidade, tivemos a iniciativa de desenvolver um produto acessível à população de menor poder aquisitivo, capaz de afastar os insetos sem agredir a saúde de quem o utiliza. 
    </p>
  </section>

  <section id="equipe">
    <h2>Equipe</h2>
    <div class="equipe">
      <div class="membro">
        <img src="Jessica.jpeg" alt="Foto de Jéssica Magalhães" />
        <h3>Jéssica Magalhães</h3>
        <p>CEO</p>
      </div>

      <div class="membro">
        <img src="isabelle.jpeg" alt="Foto de Isabelle Farias" />
        <h3>Isabelle Farias</h3>
        <p>Pesquisadora de Ingredientes Naturais e Responsável pelo Controle de Qualidade</p>
      </div>

      <div class="membro">
        <img src="clara.jpeg" alt="Foto de Clara Gonçalves" />
        <h3>Clara Gonçalves</h3>
        <p>Pesquisadora de Ingredientes Naturais</p>
      </div>

      <div class="membro">
        <img src="julia.jpeg" alt="Foto de Júlia Torres" />
        <h3>Júlia Torres</h3>
        <p>Pesquisadora de Ingredientes Naturais e Responsável pelo Controle de Qualidade</p>
      </div>

      <div class="membro">
        <img src="roberta.jpeg" alt="Foto de Roberta Viana" />
        <h3>Roberta Viana</h3>
        <p>Marketing</p>
      </div>

      <div class="membro">
        <img src="rangel.jpg" alt="Foto de Rangel Araújo" />
        <h3>Rangel Araújo</h3>
        <p>Produção do Produto</p>
      </div>
    </div>
  </section>

  <section id="ingredientes">
    <h2>Ingredientes</h2>
    <p>
      Nosso produto é elaborado com ingredientes naturais, como a citronela e o cravo-da-índia. Além de ser livre de parabenos e não testado em animais, foi desenvolvido com o propósito de oferecer eficácia aliada a um aroma agradável, sempre em harmonia com a natureza.  

      Os componentes utilizados são tradicionalmente aplicados na aromaterapia e em tratamentos naturais, contribuindo para afastar insetos de forma segura e eficaz.  
    </p>
  </section>

  <section id="produto">
    <h2>Produto</h2>
    <p>
      Repelente em <strong>Spray</strong> e <strong>Creme</strong>, nossa fórmula combina eficácia de um repelente com a hidratação da pele. 
      Desenvolvido com ingredientes naturais como <strong>citronela</strong> e <strong>cravo-da-índia</strong>, oferece proteção contínua e segura.
A Floratta Safe oferece um repelente natural que garante proteção para você e sua família nos momentos em que mais precisam. Se busca praticidade e rapidez, o repelente em spray é a escolha ideal: fácil de aplicar e altamente eficaz.  

Mas, se prefere um cuidado mais completo, que além de proteger contra os insetos também hidrata a pele, o nosso creme repelente é perfeito para você.  

E, quando está no conforto da sua casa e deseja manter o ambiente livre de insetos sem precisar aplicar nada diretamente na pele, o nosso filtro para ar-condicionado é a solução mais indicada.  

De uma forma ou de outra, o melhor para você e sua família está nos produtos Floratta Safe: proteção eficaz, cuidado com o bem-estar e compromisso com a sustentabilidade do meio ambiente. 
    </p>

    <div class="carrossel-container">
      <button class="btn prev">&#10094;</button>

      <div class="carrossel-wrapper">
        <div class="carrossel">
          <div class="carrossel-card">
            <img src="spray.jpeg" alt="Spray Natural Floratta Safe" />
            <div class="produto-info">
              <h3>Spray Natural</h3>
              <p>Proteção ambiental com aplicação no ar-condicionado.</p>
            </div>
          </div>

          <div class="carrossel-card">
            <img src="creme.jpeg" alt="Creme Natural Floratta Safe" />
            <div class="produto-info">
              <h3>Creme Hidratante</h3>
              <p>Repelência eficaz com cuidado para a pele.</p>
            </div>
          </div>

          <div class="carrossel-card">
            <img src="difusor.jpeg" alt="Difusor Floratta Safe" />
            <div class="produto-info">
              <h3>Difusor de Ar</h3>
              <p>Aromaterapia contínua e proteção natural.</p>
            </div>
          </div>
        </div>
      </div>

      <button class="btn next">&#10095;</button>
    </div>
  </section>

  <section id="preco">
    <h2>Preço</h2>

    <table>
      <caption>Produtos Unitários</caption>
      <thead>
        <tr>
          <th>Produto</th>
          <th>Foco Principal</th>
          <th>Preço Unitário</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Home Spray Protetor/Aromatizador (200ml)</td>
          <td>Perfumação instantânea e defesa natural do ambiente</td>
          <td>R$ 29,90</td>
        </tr>
        <tr>
          <td>Creme Hidratante Terapêutico (150g)</td>
          <td>Cuidado corporal profundo e efeitos terapêuticos na pele</td>
          <td>R$ 34,90</td>
        </tr>
        <tr>
          <td>Difusor de Ar Condicionado</td>
          <td>Aromaterapia contínua e discreta em pequenos espaços</td>
          <td>R$ 39,90</td>
        </tr>
      </tbody>
    </table>
  </section>

  <section id="sustentabilidade">
    <h2>Sustentabilidade</h2>
    <p>
      Nossa fórmula é baseada em ingredientes de origem vegetal, como a citronela e o cravo-da-índia, conhecidos por suas propriedades repelentes naturais e pelo baixo impacto ecológico. Esses ativos substituem o uso de substâncias químicas agressivas, reduzindo riscos à saúde humana, aos animais e ao meio ambiente. Além disso, são biodegradáveis e não contaminam o ar, o solo ou a água.
      Um dos grandes diferenciais da Floratta Safe é a aplicação do repelente diretamente no ar-condicionado, transformando o ar em um meio de proteção contínua contra insetos. Essa tecnologia permite uma dispersão uniforme, evitando o uso excessivo de sprays no ambiente e diminuindo o desperdício de produto. Dessa forma, promovemos um consumo mais consciente e eficiente.
      Na Floratta Safe, sustentabilidade não é apenas um conceito, mas um valor essencial. Cada produto é desenvolvido para garantir proteção eficaz, bem-estar e harmonia com a natureza, reforçando nosso propósito de criar soluções que cuidam das pessoas hoje sem comprometer o futuro do planeta.
    </p>
  </section>

  <section id="contato">
    <
  <section id="contato">
    <h2>Contato</h2>
    <p>Quer saber mais? Entre em contato conosco:</p>
    <ul>
      <li>Email: contato@florattasafe.com.br</li>
      <li>Telefone: (85) 99999-9999</li>
      <li>Endereço: Rua da Natureza, 123, Fortaleza - CE</li>
    </ul>
  </section>

  <footer>
    <p>&copy; 2025 Floratta Safe. Todos os direitos reservados.</p>
  </footer>

  <script>
    const carrossel = document.querySelector('.carrossel');
    const btnPrev = document.querySelector('.btn.prev');
    const btnNext = document.querySelector('.btn.next');

    let scrollAmount = 0;
    const cardWidth = 280; // Largura total aproximada do card + gap (260 + 20)

    btnNext.addEventListener('click', () => {
      if(scrollAmount <= carrossel.scrollWidth - carrossel.clientWidth - cardWidth){
        scrollAmount += cardWidth;
        carrossel.style.transform = `translateX(-${scrollAmount}px)`;
      }
    });

    btnPrev.addEventListener('click', () => {
      if(scrollAmount > 0){
        scrollAmount -= cardWidth;
        carrossel.style.transform = `translateX(-${scrollAmount}px)`;
      }
    });
  </script>
</body>
</html>
