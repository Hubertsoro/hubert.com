<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hubert.com - Vente et Réparation</title>
    <style>
        :root {
            --primary-color: #2c3e50;
            --secondary-color: #e74c3c;
            --accent-color: #3498db;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --success-color: #27ae60;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary-color);
            color: white;
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: white;
            text-decoration: none;
        }
        
        .logo span {
            color: var(--secondary-color);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }
        
        nav ul li a:hover {
            color: var(--secondary-color);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url('https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: white;
            padding: 0.8rem 1.5rem;
            border: none;
            border-radius: 4px;
            font-size: 1rem;
            cursor: pointer;
            text-decoration: none;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #c0392b;
        }
        
        /* Section Styles */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            color: var(--primary-color);
        }
        
        .section-title h2 {
            font-size: 2.2rem;
            margin-bottom: 0.5rem;
        }
        
        .section-title p {
            color: #777;
        }
        
        /* Products Section */
        .products {
            background-color: white;
        }
        
        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
        }
        
        .product-card {
            background-color: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
        }
        
        .product-img {
            height: 200px;
            background-color: #f5f5f5;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow: hidden;
        }
        
        .product-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .product-card:hover .product-img img {
            transform: scale(1.05);
        }
        
        .product-info {
            padding: 1.5rem;
        }
        
        .product-info h3 {
            margin-bottom: 0.5rem;
            color: var(--dark-color);
        }
        
        .product-price {
            font-size: 1.2rem;
            font-weight: bold;
            color: var(--secondary-color);
            margin-bottom: 1rem;
        }
        
        /* Services Section */
        .services {
            background-color: var(--light-color);
        }
        
        .service-cards {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            text-align: center;
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--accent-color);
            margin-bottom: 1rem;
        }
        
        /* Repair Form */
        .repair-form {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            margin: 0 auto;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        textarea.form-control {
            min-height: 120px;
            resize: vertical;
        }
        
        /* Admin Panel */
        .admin-panel {
            background-color: var(--light-color);
            padding: 2rem;
            border-radius: 8px;
            margin-top: 2rem;
            display: none;
        }
        
        .admin-section {
            margin-bottom: 2rem;
        }
        
        .admin-section h3 {
            margin-bottom: 1rem;
            color: var(--primary-color);
            border-bottom: 2px solid var(--accent-color);
            padding-bottom: 0.5rem;
        }
        
        .product-list, .repair-list {
            background-color: white;
            border-radius: 8px;
            padding: 1rem;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .list-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1rem;
            border-bottom: 1px solid #eee;
        }
        
        .list-item:last-child {
            border-bottom: none;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-section h3 {
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .footer-section p, .footer-section a {
            margin-bottom: 0.8rem;
            display: block;
            color: #ccc;
            text-decoration: none;
        }
        
        .footer-section a:hover {
            color: white;
        }
        
        .social-links a {
            display: inline-block;
            margin-right: 1rem;
            font-size: 1.2rem;
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid #4a5568;
            color: #ccc;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
                justify-content: center;
            }
            
            nav ul li {
                margin: 0 0.5rem;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-content">
            <a href="#" class="logo">HUBERT<span>.COM</span></a>
            <nav>
                <ul>
                    <li><a href="#accueil">Accueil</a></li>
                    <li><a href="#produits">Produits</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#reparation">Réparation</a></li>
                    <li><a href="#contact">Contact</a></li>
                    <li><a href="#" onclick="toggleAdmin()">Admin</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="accueil">
        <div class="container">
            <h1>Vente en ligne & Services de Réparation</h1>
            <p>Découvrez nos produits de qualité et profitez de nos services de réparation experts pour tous vos appareils.</p>
            <a href="#produits" class="btn">Découvrir nos produits</a>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="produits">
        <div class="container">
            <div class="section-title">
                <h2>Nos Produits</h2>
                <p>Découvrez notre sélection de produits de qualité</p>
            </div>
            
            <div class="product-grid">
                <!-- Product 1 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Casque Audio">
                    </div>
                    <div class="product-info">
                        <h3>Casque Audio Premium</h3>
                        <p>Casque sans fil avec annulation de bruit</p>
                        <div class="product-price">129,99 €</div>
                        <a href="#" class="btn">Ajouter au panier</a>
                    </div>
                </div>
                
                <!-- Product 2 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1526170375885-4d8ecf77b99f?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Appareil Photo">
                    </div>
                    <div class="product-info">
                        <h3>Appareil Photo Numerique</h3>
                        <p>24.2MP, 4K Video, Ecran Tactile</p>
                        <div class="product-price">499,99 €</div>
                        <a href="#" class="btn">Ajouter au panier</a>
                    </div>
                </div>
                
                <!-- Product 3 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1585298723682-7115561c51b7?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Enceinte Bluetooth">
                    </div>
                    <div class="product-info">
                        <h3>Enceinte Bluetooth</h3>
                        <p>SoundBoost, 20W, Résistante à l'eau</p>
                        <div class="product-price">89,99 €</div>
                        <a href="#" class="btn">Ajouter au panier</a>
                    </div>
                </div>
                
                <!-- Product 4 -->
                <div class="product-card">
                    <div class="product-img">
                        <img src="https://images.unsplash.com/photo-1504274066651-8d31a536b11a?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="Montre Connectée">
                    </div>
                    <div class="product-info">
                        <h3>Montre Connectée Fitness</h3>
                        <p>Suivi activité, Rythme cardiaque, Étanche</p>
                        <div class="product-price">159,99 €</div>
                        <a href="#" class="btn">Ajouter au panier</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Nos Services</h2>
                <p>Des services de qualité pour tous vos besoins</p>
            </div>
            
            <div class="service-cards">
                <div class="service-card">
                    <div class="service-icon">🔧</div>
                    <h3>Réparation Express</h3>
                    <p>Réparation rapide de tous vos appareils électroniques avec une garantie de 6 mois sur les interventions.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">📱</div>
                    <h3>Réparation Smartphone</h3>
                    <p>Écrans cassés, batteries défectueuses, problèmes de logiciel - nous réparons tout type de smartphone.</p>
                </div>
                
                <div class="service-card">
                    <div class="service-icon">💻</div>
                    <h3>Réparation Ordinateur</h3>
                    <p>Nettoyage, upgrade, réparation de matériel et assistance logicielle pour ordinateurs portables et fixes.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Repair Section -->
    <section class="repair" id="reparation">
        <div class="container">
            <div class="section-title">
                <h2>Demande de Réparation</h2>
                <p>Remplissez le formulaire pour une demande de réparation</p>
            </div>
            
            <form class="repair-form" id="repairForm">
                <div class="form-group">
                    <label for="name">Nom complet</label>
                    <input type="text" id="name" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="email">Adresse email</label>
                    <input type="email" id="email" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="phone">Numéro de téléphone</label>
                    <input type="tel" id="phone" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="deviceType">Type d'appareil</label>
                    <select id="deviceType" class="form-control" required>
                        <option value="">Sélectionnez un type</option>
                        <option value="smartphone">Smartphone</option>
                        <option value="laptop">Ordinateur portable</option>
                        <option value="desktop">Ordinateur de bureau</option>
                        <option value="tablet">Tablette</option>
                        <option value="other">Autre</option>
                    </select>
                </div>
                
                <div class="form-group">
                    <label for="brand">Marque</label>
                    <input type="text" id="brand" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="model">Modèle</label>
                    <input type="text" id="model" class="form-control" required>
                </div>
                
                <div class="form-group">
                    <label for="problem">Description du problème</label>
                    <textarea id="problem" class="form-control" required></textarea>
                </div>
                
                <button type="submit" class="btn">Soumettre la demande</button>
            </form>
        </div>
    </section>

    <!-- Admin Panel -->
    <section class="admin" id="admin">
        <div class="container">
            <div class="admin-panel" id="adminPanel">
                <h2>Panel d'Administration Hubert.com</h2>
                
                <div class="admin-section">
                    <h3>Gestion des Produits</h3>
                    <div class="product-list">
                        <div class="list-item">
                            <div>
                                <h4>Casque Audio Premium</h4>
                                <p>Stock: 15 | Prix: 129,99 €</p>
                            </div>
                            <div>
                                <button class="btn">Modifier</button>
                                <button class="btn" style="background-color: #e74c3c;">Supprimer</button>
                            </div>
                        </div>
                        
                        <div class="list-item">
                            <div>
                                <h4>Appareil Photo Numerique</h4>
                                <p>Stock: 8 | Prix: 499,99 €</p>
                            </div>
                            <div>
                                <button class="btn">Modifier</button>
                                <button class="btn" style="background-color: #e74c3c;">Supprimer</button>
                            </div>
                        </div>
                    </div>
                    <button class="btn" style="margin-top: 1rem;">Ajouter un produit</button>
                </div>
                
                <div class="admin-section">
                    <h3>Demandes de Réparation</h3>
                    <div class="repair-list">
                        <div class="list-item">
                            <div>
                                <h4>Jean Dupont - Smartphone Samsung</h4>
                                <p>Écran cassé | Reçu le: 12/05/2023</p>
                            </div>
                            <div>
                                <button class="btn">Marquer comme réparé</button>
                            </div>
                        </div>
                        
                        <div class="list-item">
                            <div>
                                <h4>Marie Martin - Ordinateur Dell</h4>
                                <p>Problème de démarrage | Reçu le: 10/05/2023</p>
                            </div>
                            <div>
                                <button class="btn">Marquer comme réparé</button>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="admin-section">
                    <h3>Statistiques</h3>
                    <div style="background-color: white; padding: 1rem; border-radius: 8px;">
                        <p>Produits vendus ce mois: 42</p>
                        <p>Réparations effectuées ce mois: 28</p>
                        <p>Chiffre d'affaires ce mois: 8 542,50 €</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>À propos de Hubert.com</h3>
                    <p>Votre spécialiste en vente de produits électroniques et services de réparation depuis 2010.</p>
                </div>
                
                <div class="footer-section">
                    <h3>Contactez-nous</h3>
                    <p>📱 +33 1 23 45 67 89</p>
                    <p>✉️ contact@hubert.com</p>
                    <p>🏠 123 Rue du Commerce, 75000 Paris</p>
                </div>
                
                <div class="footer-section">
                    <h3>Liens rapides</h3>
                    <a href="#accueil">Accueil</a>
                    <a href="#produits">Produits</a>
                    <a href="#services">Services</a>
                    <a href="#reparation">Réparation</a>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 Hubert.com - Tous droits réservés</p>
            </div>
        </div>
    </footer>

    <script>
        // Toggle Admin Panel
        function toggleAdmin() {
            const adminPanel = document.getElementById('adminPanel');
            if (adminPanel.style.display === 'block') {
                adminPanel.style.display = 'none';
            } else {
                adminPanel.style.display = 'block';
                window.scrollTo({ top: document.getElementById('admin').offsetTop, behavior: 'smooth' });
            }
        }
        
        // Repair Form Submission
        document.getElementById('repairForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Votre demande de réparation a été envoyée avec succès! Nous vous contacterons dans les 24h.');
            this.reset();
        });
        
        // Simple Cart Functionality
        const addToCartButtons = document.querySelectorAll('.product-card .btn');
        addToCartButtons.forEach(button => {
            button.addEventListener('click', function(e) {
                e.preventDefault();
                const productName = this.parentElement.querySelector('h3').textContent;
                alert(`${productName} a été ajouté à votre panier!`);
            });
        });
    </script>
</body>
</html>
