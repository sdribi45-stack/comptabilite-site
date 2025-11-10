# comptabilite-site
"Site web de comptabilité et facturation"
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Comptabilité & Facturation Pro</title>
    <style>
        :root {
            --primary: #2c3e50;
            --secondary: #3498db;
            --accent: #e74c3c;
            --light: #ecf0f1;
            --dark: #2c3e50;
            --success: #2ecc71;
            --warning: #f39c12;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header Styles */
        header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
        }
        
        .logo span {
            color: var(--secondary);
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
            color: var(--secondary);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary) 0%, var(--secondary) 100%);
            color: white;
            padding: 5rem 0;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
        }
        
        .btn:hover {
            background-color: #c0392b;
        }
        
        /* Services Section */
        .services {
            padding: 5rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: #666;
            max-width: 600px;
            margin: 0 auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--secondary);
            margin-bottom: 1rem;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        /* Client Area */
        .client-area {
            background-color: var(--light);
            padding: 5rem 0;
        }
        
        .client-login {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            max-width: 500px;
            margin: 0 auto;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }
        
        .client-login h3 {
            text-align: center;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-group input {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        /* Admin Login */
        .admin-login {
            background: var(--primary);
            color: white;
            padding: 2rem;
            border-radius: 8px;
            max-width: 400px;
            margin: 2rem auto 0;
        }
        
        .admin-login h3 {
            text-align: center;
            margin-bottom: 1.5rem;
        }
        
        .admin-login .btn {
            background-color: var(--secondary);
        }
        
        .admin-login .btn:hover {
            background-color: #2980b9;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .footer-column h4 {
            margin-bottom: 1.5rem;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 0.8rem;
        }
        
        .footer-column ul li a {
            color: #bbb;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 2rem;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: #bbb;
            font-size: 0.9rem;
        }
        
        /* Admin Interface Styles */
        .admin-interface {
            display: none;
            background-color: #f8f9fa;
            min-height: 100vh;
        }
        
        .admin-header {
            background-color: var(--primary);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        .admin-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .admin-nav ul {
            display: flex;
            list-style: none;
        }
        
        .admin-nav ul li {
            margin-left: 1.5rem;
        }
        
        .admin-nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
        }
        
        .admin-main {
            padding: 2rem 0;
        }
        
        .dashboard-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-bottom: 2rem;
        }
        
        .dashboard-card {
            background: white;
            border-radius: 8px;
            padding: 1.5rem;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        
        .dashboard-card h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--primary);
        }
        
        .dashboard-card .value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--secondary);
        }
        
        .admin-table {
            background: white;
            border-radius: 8px;
            overflow: hidden;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        th, td {
            padding: 1rem;
            text-align: left;
            border-bottom: 1px solid #eee;
        }
        
        th {
            background-color: var(--light);
            font-weight: 600;
            color: var(--primary);
        }
        
        .status-pending {
            color: var(--warning);
            font-weight: 600;
        }
        
        .status-paid {
            color: var(--success);
            font-weight: 600;
        }
        
        /* Login Modal */
        .login-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            z-index: 1000;
            justify-content: center;
            align-items: center;
        }
        
        .modal-content {
            background: white;
            border-radius: 8px;
            padding: 2rem;
            width: 100%;
            max-width: 400px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .modal-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .modal-header h3 {
            color: var(--primary);
        }
        
        .close-modal {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #999;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .header-content, .admin-nav {
                flex-direction: column;
            }
            
            nav ul {
                margin-top: 1rem;
            }
            
            nav ul li {
                margin: 0 0.5rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
            
            .services-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Client Interface -->
    <div id="client-interface">
        <header>
            <div class="container header-content">
                <div class="logo">Compta<span>Pro</span></div>
                <nav>
                    <ul>
                        <li><a href="#accueil">Accueil</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#contact">Contact</a></li>
                        <li><a href="#" id="client-login-link">Espace Client</a></li>
                    </ul>
                </nav>
            </div>
        </header>

        <section class="hero" id="accueil">
            <div class="container">
                <h1>Solutions de Comptabilité et Facturation</h1>
                <p>Simplifiez votre gestion financière avec nos services professionnels de comptabilité et de facturation. Gagnez du temps et concentrez-vous sur votre activité.</p>
                <a href="#services" class="btn">Découvrir nos services</a>
            </div>
        </section>

        <section class="services" id="services">
            <div class="container">
                <div class="section-title">
                    <h2>Nos Services</h2>
                    <p>Nous offrons une gamme complète de services pour répondre à tous vos besoins en comptabilité et facturation.</p>
                </div>
                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">📊</div>
                        <h3>Comptabilité Générale</h3>
                        <p>Gestion complète de votre comptabilité avec des rapports détaillés et conformes aux normes en vigueur.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">🧾</div>
                        <h3>Facturation Électronique</h3>
                        <p>Création, envoi et suivi de vos factures électroniques avec un système automatisé et sécurisé.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">💰</div>
                        <h3>Gestion de Trésorerie</h3>
                        <p>Suivi de vos flux financiers, prévisions de trésorerie et optimisation de votre gestion financière.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">📈</div>
                        <h3>Reporting Financier</h3>
                        <p>Analyses détaillées et tableaux de bord pour une vision claire de la santé financière de votre entreprise.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">🔒</div>
                        <h3>Conformité Fiscale</h3>
                        <p>Assistance pour vos déclarations fiscales et respect des obligations légales en matière de comptabilité.</p>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">👥</div>
                        <h3>Conseil Financier</h3>
                        <p>Accompagnement personnalisé pour optimiser votre stratégie financière et prendre les bonnes décisions.</p>
                    </div>
                </div>
            </div>
        </section>

        <section class="client-area">
            <div class="container">
                <div class="section-title">
                    <h2>Espace Client</h2>
                    <p>Accédez à votre espace personnel pour consulter vos documents et suivre votre situation financière.</p>
                </div>
                <div class="client-login">
                    <h3>Connexion Client</h3>
                    <div class="form-group">
                        <label for="client-email">Email</label>
                        <input type="email" id="client-email" placeholder="votre@email.com">
                    </div>
                    <div class="form-group">
                        <label for="client-password">Mot de passe</label>
                        <input type="password" id="client-password" placeholder="Votre mot de passe">
                    </div>
                    <button class="btn" style="width: 100%;">Se connecter</button>
                    <p style="text-align: center; margin-top: 1rem;"><a href="#" style="color: var(--secondary);">Mot de passe oublié ?</a></p>
                </div>
                
                <div class="admin-login">
                    <h3>Accès Administrateur</h3>
                    <p style="text-align: center; margin-bottom: 1rem;">Accès réservé au personnel autorisé</p>
                    <button class="btn" id="admin-login-btn" style="width: 100%;">Connexion Admin</button>
                </div>
            </div>
        </section>

        <footer id="contact">
            <div class="container">
                <div class="footer-content">
                    <div class="footer-column">
                        <h4>ComptaPro</h4>
                        <p>Votre partenaire de confiance pour tous vos besoins en comptabilité et facturation.</p>
                    </div>
                    <div class="footer-column">
                        <h4>Liens Rapides</h4>
                        <ul>
                            <li><a href="#accueil">Accueil</a></li>
                            <li><a href="#services">Services</a></li>
                            <li><a href="#contact">Contact</a></li>
                            <li><a href="#">Espace Client</a></li>
                        </ul>
                    </div>
                    <div class="footer-column">
                        <h4>Services</h4>
                        <ul>
                            <li><a href="#">Comptabilité Générale</a></li>
                            <li><a href="#">Facturation</a></li>
                            <li><a href="#">Gestion de Trésorerie</a></li>
                            <li><a href="#">Conseil Financier</a></li>
                        </ul>
                    </div>
                    <div class="footer-column">
                        <h4>Contact</h4>
                        <ul>
                            <li>📞 +33 1 23 45 67 89</li>
                            <li>✉️ contact@comptapro.fr</li>
                            <li>📍 123 Rue des Comptables, 75000 Paris</li>
                        </ul>
                    </div>
                </div>
                <div class="copyright">
                    <p>&copy; 2023 ComptaPro. Tous droits réservés.</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- Admin Interface (hidden by default) -->
    <div id="admin-interface" class="admin-interface">
        <header class="admin-header">
            <div class="container admin-nav">
                <div class="logo">Compta<span>Pro</span> Admin</div>
                <nav>
                    <ul>
                        <li><a href="#" class="admin-nav-link" data-section="dashboard">Tableau de bord</a></li>
                        <li><a href="#" class="admin-nav-link" data-section="clients">Clients</a></li>
                        <li><a href="#" class="admin-nav-link" data-section="invoices">Factures</a></li>
                        <li><a href="#" class="admin-nav-link" data-section="reports">Rapports</a></li>
                        <li><a href="#" id="admin-logout">Déconnexion</a></li>
                    </ul>
                </nav>
            </div>
        </header>

        <main class="admin-main">
            <div class="container">
                <!-- Dashboard Section -->
                <div id="dashboard-section" class="admin-section">
                    <h2>Tableau de Bord</h2>
                    <div class="dashboard-cards">
                        <div class="dashboard-card">
                            <h3>Clients Actifs</h3>
                            <div class="value">42</div>
                        </div>
                        <div class="dashboard-card">
                            <h3>Factures ce mois</h3>
                            <div class="value">128</div>
                        </div>
                        <div class="dashboard-card">
                            <h3>Chiffre d'affaires</h3>
                            <div class="value">€84,520</div>
                        </div>
                        <div class="dashboard-card">
                            <h3>Factures en attente</h3>
                            <div class="value">18</div>
                        </div>
                    </div>
                    
                    <h3 style="margin-bottom: 1rem;">Factures Récentes</h3>
                    <div class="admin-table">
                        <table>
                            <thead>
                                <tr>
                                    <th>N° Facture</th>
                                    <th>Client</th>
                                    <th>Date</th>
                                    <th>Montant</th>
                                    <th>Statut</th>
                                </tr>
                            </thead>
                            <tbody>
                                <tr>
                                    <td>INV-2023-0456</td>
                                    <td>Entreprise A</td>
                                    <td>15/10/2023</td>
                                    <td>€2,450.00</td>
                                    <td class="status-paid">Payée</td>
                                </tr>
                                <tr>
                                    <td>INV-2023-0457</td>
                                    <td>Entreprise B</td>
                                    <td>16/10/2023</td>
                                    <td>€1,890.50</td>
                                    <td class="status-pending">En attente</td>
                                </tr>
                                <tr>
                                    <td>INV-2023-0458</td>
                                    <td>Entreprise C</td>
                                    <td>17/10/2023</td>
                                    <td>€3,210.00</td>
                                    <td class="status-paid">Payée</td>
                                </tr>
                                <tr>
                                    <td>INV-2023-0459</td>
                                    <td>Entreprise D</td>
                                    <td>18/10/2023</td>
                                    <td>€1,575.75</td>
                                    <td class="status-pending">En attente</td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
                
                <!-- Clients Section -->
                <div id="clients-section" class="admin-section" style="display: none;">
                    <h2>Gestion des Clients</h2>
                    <p>Interface de gestion des clients à développer...</p>
                </div>
                
                <!-- Invoices Section -->
                <div id="invoices-section" class="admin-section" style="display: none;">
                    <h2>Gestion des Factures</h2>
                    <p>Interface de gestion des factures à développer...</p>
                </div>
                
                <!-- Reports Section -->
                <div id="reports-section" class="admin-section" style="display: none;">
                    <h2>Rapports Financiers</h2>
                    <p>Interface des rapports financiers à développer...</p>
                </div>
            </div>
        </main>
    </div>

    <!-- Admin Login Modal -->
    <div id="admin-login-modal" class="login-modal">
        <div class="modal-content">
            <div class="modal-header">
                <h3>Connexion Administrateur</h3>
                <button class="close-modal">&times;</button>
            </div>
            <div class="form-group">
                <label for="admin-username">Nom d'utilisateur</label>
                <input type="text" id="admin-username" placeholder="Votre nom d'utilisateur">
            </div>
            <div class="form-group">
                <label for="admin-password">Mot de passe</label>
                <input type="password" id="admin-password" placeholder="Votre mot de passe">
            </div>
            <button class="btn" id="admin-login-submit" style="width: 100%;">Se connecter</button>
        </div>
    </div>

    <script>
        // DOM Elements
        const clientInterface = document.getElementById('client-interface');
        const adminInterface = document.getElementById('admin-interface');
        const adminLoginBtn = document.getElementById('admin-login-btn');
        const adminLoginModal = document.getElementById('admin-login-modal');
        const closeModal = document.querySelector('.close-modal');
        const adminLoginSubmit = document.getElementById('admin-login-submit');
        const adminLogout = document.getElementById('admin-logout');
        const adminNavLinks = document.querySelectorAll('.admin-nav-link');
        const adminSections = document.querySelectorAll('.admin-section');

        // Show admin login modal
        adminLoginBtn.addEventListener('click', () => {
            adminLoginModal.style.display = 'flex';
        });

        // Close modal
        closeModal.addEventListener('click', () => {
            adminLoginModal.style.display = 'none';
        });

        // Admin login
        adminLoginSubmit.addEventListener('click', () => {
            const username = document.getElementById('admin-username').value;
            const password = document.getElementById('admin-password').value;
            
            // Simple authentication (in a real app, this would be handled server-side)
            if (username === 'admin' && password === 'admin123') {
                clientInterface.style.display = 'none';
                adminInterface.style.display = 'block';
                adminLoginModal.style.display = 'none';
            } else {
                alert('Identifiants incorrects. Utilisez "admin" et "admin123" pour tester.');
            }
        });

        // Admin logout
        adminLogout.addEventListener('click', () => {
            adminInterface.style.display = 'none';
            clientInterface.style.display = 'block';
        });

        // Admin navigation
        adminNavLinks.forEach(link => {
            link.addEventListener('click', (e) => {
                e.preventDefault();
                const targetSection = link.getAttribute('data-section');
                
                // Hide all sections
                adminSections.forEach(section => {
                    section.style.display = 'none';
                });
                
                // Show target section
                document.getElementById(`${targetSection}-section`).style.display = 'block';
            });
        });

        // Close modal when clicking outside
        window.addEventListener('click', (e) => {
            if (e.target === adminLoginModal) {
                adminLoginModal.style.display = 'none';
            }
        });
    </script>
</body>
</html> 
# Site de Comptabilité et Facturation

Site web professionnel pour services de comptabilité et facturation.

## Accès Admin
- Nom d'utilisateur: admin
- Mot de passe: admin123
