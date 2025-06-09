<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sakura Delícias - Doces Orientais Premium</title>
  <style>
    :root {
      --primary: #FFB7B2; /* Rosa pastel */
      --primary-dark: #FF9AA2; /* Rosa mais escuro */
      --secondary: #FFDAC1; /* Pêssego pastel */
      --light: #FFF9FB; /* Branco rosado */
      --dark: #6B5B95; /* Roxo suave */
      --gray: #E2F0CB; /* Verde menta pastel */
    }
    
    @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700&family=Noto+Sans+JP:wght@400;700&display=swap');
    
    body {
      font-family: 'Montserrat', 'Noto Sans JP', sans-serif;
      margin: 0;
      padding: 0;
      background-color: var(--light);
      color: var(--dark);
      line-height: 1.6;
    }
    
    header {
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      color: white;
      padding: 3rem 0;
      text-align: center;
      box-shadow: 0 4px 12px rgba(0,0,0,0.1);
      position: relative;
      overflow: hidden;
    }
    
    .header-content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
      position: relative;
      z-index: 2;
    }
    
    h1 {
      margin: 0;
      font-size: 3rem;
      font-weight: 700;
      text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
      letter-spacing: 2px;
      color: var(--dark);
    }
    
    .tagline {
      font-size: 1.3rem;
      margin-top: 1rem;
      font-weight: 300;
      max-width: 800px;
      margin-left: auto;
      margin-right: auto;
      color: var(--dark);
    }
    
    .container {
      max-width: 1200px;
      margin: 3rem auto;
      padding: 0 20px;
    }
    
    .section-title {
      text-align: center;
      margin-bottom: 3rem;
      color: var(--primary-dark);
      position: relative;
      font-size: 2rem;
    }
    
    .section-title:after {
      content: '';
      display: block;
      width: 100px;
      height: 4px;
      background: var(--secondary);
      margin: 1rem auto;
    }
    
    .destaque {
      background-color: white;
      border-radius: 15px;
      padding: 2rem;
      margin-bottom: 3rem;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
      display: flex;
      flex-direction: column;
      align-items: center;
      text-align: center;
    }
    
    .destaque-icon {
      font-size: 3rem;
      color: var(--primary-dark);
      margin-bottom: 1rem;
    }
    
    .produtos {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 2rem;
      padding: 1rem 0;
    }
    
    .produto {
      background-color: white;
      border-radius: 15px;
      overflow: hidden;
      box-shadow: 0 5px 15px rgba(0,0,0,0.08);
      transition: transform 0.3s ease, box-shadow 0.3s ease;
      position: relative;
    }
    
    .produto:hover {
      transform: translateY(-10px);
      box-shadow: 0 15px 30px rgba(0,0,0,0.1);
    }
    
    .produto-badge {
      position: absolute;
      top: 15px;
      right: 15px;
      background-color: var(--secondary);
      color: var(--dark);
      padding: 0.3rem 0.8rem;
      border-radius: 50px;
      font-size: 0.8rem;
      font-weight: 600;
      z-index: 2;
    }
    
    .produto-img {
      width: 100%;
      height: 250px;
      object-fit: cover;
      border-bottom: 1px solid var(--gray);
      transition: transform 0.5s ease;
    }
    
    .produto:hover .produto-img {
      transform: scale(1.05);
    }
    
    .produto-info {
      padding: 1.5rem;
      text-align: center;
    }
    
    .produto h3 {
      margin: 0 0 0.5rem;
      font-size: 1.5rem;
      color: var(--primary-dark);
    }
    
    .produto p {
      margin: 0.5rem 0;
      color: #888;
      min-height: 60px;
    }
    
    .preco {
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--primary-dark);
      margin: 1rem 0;
    }
    
    .btn-comprar {
      background: var(--primary-dark);
      color: white;
      padding: 1rem 2rem;
      border: none;
      border-radius: 50px;
      cursor: pointer;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-size: 1rem;
      transition: all 0.3s ease;
      display: inline-block;
      margin-top: 0.5rem;
      width: 100%;
    }
    
    .btn-comprar:hover {
      background: var(--dark);
      transform: translateY(-2px);
      box-shadow: 0 5px 15px rgba(107, 91, 149, 0.3);
    }
    
    .sobre-nos {
      background-color: white;
      border-radius: 15px;
      padding: 3rem;
      margin: 3rem 0;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    }
    
    .sobre-nos h2 {
      color: var(--primary-dark);
      text-align: center;
      margin-bottom: 2rem;
    }
    
    .qualidades {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
      margin-top: 2rem;
    }
    
    .qualidade {
      text-align: center;
      padding: 1.5rem;
      border-radius: 10px;
      background-color: var(--light);
    }
    
    .qualidade i {
      font-size: 2.5rem;
      color: var(--primary-dark);
      margin-bottom: 1rem;
      display: block;
    }
    
    .depoimentos {
      margin: 4rem 0;
    }
    
    .depoimento-cards {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }
    
    .depoimento-card {
      background-color: white;
      border-radius: 15px;
      padding: 2rem;
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    }
    
    .depoimento-texto {
      font-style: italic;
      margin-bottom: 1rem;
      color: #666;
    }
    
    .depoimento-autor {
      font-weight: 600;
      color: var(--primary-dark);
    }
    
    .estrelas {
      color: var(--secondary);
      margin-top: 0.5rem;
    }
    
    footer {
      background: linear-gradient(135deg, var(--primary), var(--primary-dark));
      color: white;
      padding: 3rem 0 2rem;
      margin-top: 3rem;
    }
    
    .footer-content {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 20px;
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 2rem;
    }
    
    .footer-col h3 {
      font-size: 1.3rem;
      margin-bottom: 1.5rem;
      position: relative;
      padding-bottom: 0.5rem;
    }
    
    .footer-col h3:after {
      content: '';
      position: absolute;
      left: 0;
      bottom: 0;
      width: 50px;
      height: 2px;
      background: var(--secondary);
    }
    
    .footer-links {
      list-style: none;
      padding: 0;
    }
    
    .footer-links li {
      margin-bottom: 0.8rem;
    }
    
    .footer-links a {
      color: white;
      text-decoration: none;
      transition: all 0.3s ease;
      display: inline-block;
    }
    
    .footer-links a:hover {
      transform: translateX(5px);
      opacity: 0.8;
    }
    
    .social-links {
      display: flex;
      gap: 1rem;
      margin-top: 1rem;
    }
    
    .social-links a {
      color: white;
      font-size: 1.5rem;
      transition: transform 0.3s ease;
    }
    
    .social-links a:hover {
      transform: translateY(-5px);
    }
    
    .copyright {
      text-align: center;
      margin-top: 3rem;
      padding-top: 1.5rem;
      border-top: 1px solid rgba(255,255,255,0.2);
      font-size: 0.9rem;
      opacity: 0.8;
    }
    
    /* Elementos orientais */
    .sakura-decoration {
      position: absolute;
      opacity: 0.2;
      z-index: 1;
      color: var(--primary-dark);
    }
    
    .sakura-1 {
      top: 20px;
      left: 5%;
      font-size: 8rem;
      transform: rotate(-15deg);
    }
    
    .sakura-2 {
      bottom: 30px;
      right: 10%;
      font-size: 6rem;
      transform: rotate(25deg);
    }
    
    @media (max-width: 768px) {
      .produtos {
        grid-template-columns: 1fr;
      }
      
      h1 {
        font-size: 2.5rem;
      }
      
      .sobre-nos {
        padding: 2rem 1rem;
      }
      
      .sakura-decoration {
        display: none;
      }
    }
  </style>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>

  <header>
    <div class="sakura-decoration sakura-1">
      <i class="fas fa-spa"></i>
    </div>
    <div class="sakura-decoration sakura-2">
      <i class="fas fa-spa"></i>
    </div>
    <div class="header-content">
      <h1>Sakura Delícias</h1>
      <p class="tagline">Doces Orientais Premium - Autênticos sabores da Ásia</p>
    </div>
  </header>

  <main class="container">
    <section class="destaque">
      <div class="destaque-icon">
        <i class="fas fa-umbrella-beach"></i>
      </div>
      <h2>Autenticidade Oriental</h2>
      <p>Nossos doces são preparados seguindo receitas tradicionais japonesas e chinesas, com ingredientes importados diretamente da Ásia. Cada doce é uma experiência cultural que transporta você para as ruas de Tóquio ou os mercados de Pequim.</p>
    </section>
    
    <h2 class="section-title">Nossas Delícias Orientais</h2>
    
    <div class="produtos">
      <!-- Dorayaki Premium -->
      <div class="produto">
        <span class="produto-badge">Mais vendido</span>
        <img src="doorayakiii.jfif" alt="Dorayaki Premium" class="produto-img">
        <div class="produto-info">
          <h3>Dorayaki Premium</h3>
          <p>Os famosos panquecas japonesas recheadas com anko cremoso. Nosso diferencial: massa extra fofinha e recheio generoso. O preferido do Doraemon!</p>
          <p class="preco">R$ 7,00</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <!-- Mochi Tradicional -->
      <div class="produto">
        <span class="produto-badge">Novidade</span>
        <img src="gheia.jpm.jfif" alt="Mochi Tradicional" class="produto-img">
        <div class="produto-info">
          <h3>Mochi Tradicional</h3>
          <p>O clássico japonês! Massa de arroz glutinoso macia e elástica recheada com anko (pasta de feijão vermelho doce). Disponível também nas versões matcha e chocolate.</p>
          <p class="preco">R$ 4,50</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <!-- Mooncake Premium -->
      <div class="produto">
        <span class="produto-badge">Destaque</span>
        <img src="Caramel+Almond+Mooncake-2.jpg" alt="Mooncake Premium" class="produto-img">
        <div class="produto-info">
          <h3>Mooncake Premium</h3>
          <p>O tradicional bolo lunar chinês em versão sofisticada. Massa macia envolve recheios como lótus, gema de ovo salgada e nozes. Edição especial para o Festival da Lua.</p>
          <p class="preco">R$ 12,00</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <div class="produto">
        <span class="produto-badge">Exclusivo</span>
        <img src="taiyaki..jpeg" alt="Taiyaki" class="produto-img">
        <div class="produto-info">
          <h3>Taiyaki Crocante</h3>
          <p>Peixinho japonês com massa crocante por fora e macia por dentro. Recheios: chocolate belga, creme de matcha ou doce de feijão tradicional. Feito na hora!</p>
          <p class="preco">R$ 8,50</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <div class="produto">
        <span class="produto-badge">Sem glúten</span>
        <img src="tango..webp" alt="Dango" class="produto-img">
        <div class="produto-info">
          <h3>Dango Tricolor</h3>
          <p>Bolinhas de mochi em espetinhos, no tradicional estilo hanami dango (rosa, branco e verde). Sabor suave e textura perfeita para acompanhar chá verde.</p>
          <p class="preco">R$ 6,00</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <div class="produto">
        <span class="produto-badge">Festival</span>
        <img src="yakitori.jfif" alt="Yakitori Doce" class="produto-img">
        <div class="produto-info">
          <h3>Yakitori Doce</h3>
          <p>Versão doce do tradicional espetinho japonês. Massa de bolinho frito com cobertura de mel e gergelim. Perfeito para festivais e comemorações.</p>
          <p class="preco">R$ 5,50</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <div class="produto">
        <span class="produto-badge">Tradicional</span>
        <img src="manju..jfif" alt="Manju" class="produto-img">
        <div class="produto-info">
          <h3>Manju Japonês</h3>
          <p>Bolinhos cozidos no vapor com massa macia e recheio de feijão doce. Versões com massa de chá verde ou sakura (flor de cerejeira). Autêntico sabor de Kyoto.</p>
          <p class="preco">R$ 3,50</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
      
      <div class="produto">
        <span class="produto-badge">Sazonal</span>
        <img src="sakuura.mochi.jfif" alt="Sakura Mochi" class="produto-img">
        <div class="produto-info">
          <h3>Sakura Mochi</h3>
          <p>Edição especial de primavera! Mochi cor-de-rosa envolto em folha de cerejeira. Sabor delicado e apresentação que homenageia a florada das cerejeiras.</p>
          <p class="preco">R$ 5,00</p>
          <button class="btn-comprar">Comprar agora</button>
        </div>
      </div>
    </div>
    
    <section class="sobre-nos">
      <h2>Sobre a Sakura Delícias</h2>
      <p>Fundada por uma família nipo-brasileira, a Sakura Delícias nasceu da paixão por compartilhar os autênticos sabores doces do Oriente. Com mais de 15 anos de experiência na confeitaria japonesa, nosso mestre confeiteiro traz técnicas tradicionais combinadas com toques contemporâneos.</p>
      
      <div class="qualidades">
        <div class="qualidade">
          <i class="fas fa-fan"></i>
          <h3>Tradição Japonesa</h3>
          <p>Receitas autênticas passadas por gerações, preparadas com técnicas tradicionais e respeito à cultura oriental.</p>
        </div>
        
        <div class="qualidade">
          <i class="fas fa-seedling"></i>
          <h3>Ingredientes Importados</h3>
          <p>Utilizamos ingredientes premium importados diretamente do Japão e China para garantir o sabor original.</p>
        </div>
        
        <div class="qualidade">
          <i class="fas fa-heart"></i>
          <h3>Artesanal</h3>
          <p>Cada doce é preparado manualmente com atenção aos detalhes, garantindo qualidade e apresentação impecáveis.</p>
        </div>
        
        <div class="qualidade">
          <i class="fas fa-calendar-alt"></i>
          <h3>Festivais Temáticos</h3>
          <p>Doces especiais para cada estação e celebrações do calendário oriental como Hanami, Festival da Lua e Ano Novo Chinês.</p>
        </div>
      </div>
    </section>
    
    <section class="depoimentos">
      <h2 class="section-title">O que dizem nossos clientes</h2>
      
      <div class="depoimento-cards">
        <div class="depoimento-card">
          <div class="depoimento-texto">
            "Os mochis da Sakura Delícias são os mais autênticos que já comi fora do Japão! A textura da massa é perfeita e o recheio tem o equilíbrio ideal de doçura."
          </div>
          <div class="depoimento-autor">- Takashi M.</div>
          <div class="estrelas">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
          </div>
        </div>
        
        <div class="depoimento-card">
          <div class="depoimento-texto">
            "Compro mensalmente os mooncakes para presentear meus clientes asiáticos. Eles sempre elogiam a autenticidade e qualidade, dizendo que parece feito em casa!"
          </div>
          <div class="depoimento-autor">- Luana C.</div>
          <div class="estrelas">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
          </div>
        </div>
        
        <div class="depoimento-card">
          <div class="depoimento-texto">
            "Meus filhos adoram o taiyaki crocante! Levamos toda semana depois da aula de japonês. Já experimentamos todos os recheios e o de matcha é nosso favorito."
          </div>
          <div class="depoimento-autor">- Ana Paula R.</div>
          <div class="estrelas">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star-half-alt"></i>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="footer-content">
      <div class="footer-col">
        <h3>Sakura Delícias</h3>
        <p>Doces Orientais Premium - Autênticos sabores da Ásia no Brasil desde 2010.</p>
        <div class="social-links">
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-facebook"></i></a>
          <a href="#"><i class="fab fa-whatsapp"></i></a>
        </div>
      </div>
      
      <div class="footer-col">
        <h3>Links Rápidos</h3>
        <ul class="footer-links">
          <li><a href="#">Home</a></li>
          <li><a href="#">Produtos</a></li>
          <li><a href="#">Sobre Nós</a></li>
          <li><a href="#">Festivais</a></li>
          <li><a href="#">Contato</a></li>
        </ul>
      </div>
      
      <div class="footer-col">
        <h3>Contato</h3>
        <ul class="footer-links">
          <li><i class="fas fa-map-marker-alt"></i> Rua das Cerejeiras, 456 - Liberdade</li>
          <li><i class="fas fa-phone"></i> (11) 98765-4321</li>
          <li><i class="fas fa-envelope"></i> contato@sakuradelicias.com</li>
          <li><i class="fas fa-clock"></i> Ter-Dom: 10h-20h | Seg: fechado</li>
        </ul>
      </div>
    </div>
    
    <div class="copyright">
      &copy; 2025 Sakura Delícias - Todos os direitos reservados | さくらデリシアス
    </div>
  </footer>

</body>
</html>
