<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV - TARIK MERRAS</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #2E86C1;
            --primary-dark: #1A5276;
            --secondary: #5D6D7E;
            --light: #F8F9F9;
            --dark: #283747;
            --success: #28B463;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background-color: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            position: relative;
        }
        
        .floating-bg {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at 70% 30%, rgba(46, 134, 193, 0.1) 0%, transparent 40%);
            z-index: -1;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
            animation: fadeIn 1s ease-in-out;
            position: relative;
            padding-bottom: 20px;
        }
        
        header::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 25%;
            width: 50%;
            height: 3px;
            background: linear-gradient(90deg, transparent, var(--primary), transparent);
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 5px solid white;
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }
        
        .profile-img:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(46, 134, 193, 0.3);
        }
        
        h1 {
            color: var(--primary);
            font-size: 2.5rem;
            margin-bottom: 5px;
            text-shadow: 1px 1px 3px rgba(0,0,0,0.1);
        }
        
        .subtitle {
            color: var(--secondary);
            font-weight: 400;
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
        }
        
        .subtitle::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 100%;
            height: 2px;
            background: var(--primary);
            transform: scaleX(0);
            transition: transform 0.3s ease;
        }
        
        .subtitle:hover::after {
            transform: scaleX(1);
        }
        
        .contact-info {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 15px;
            background: white;
            border-radius: 30px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
            transition: all 0.3s ease;
        }
        
        .contact-item:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .contact-item i {
            color: var(--primary);
            font-size: 1.2rem;
            min-width: 20px;
        }
        
        section {
            background: white;
            padding: 30px;
            margin-bottom: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            animation: slideUp 0.8s ease-in-out;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }
        
        section:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        
        section::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: linear-gradient(to bottom, var(--primary), var(--primary-dark));
        }
        
        h2 {
            color: var(--primary-dark);
            border-bottom: 2px solid #eee;
            padding-bottom: 10px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
            font-size: 1.5rem;
        }
        
        h2 i {
            font-size: 1.5rem;
            width: 40px;
            height: 40px;
            background: rgba(46, 134, 193, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s ease;
        }
        
        section:hover h2 i {
            background: rgba(46, 134, 193, 0.2);
            transform: rotate(10deg);
        }
        
        .timeline {
            position: relative;
            padding-left: 30px;
        }
        
        .timeline-item {
            position: relative;
            padding-bottom: 25px;
            margin-bottom: 25px;
        }
        
        .timeline-item:last-child {
            margin-bottom: 0;
            padding-bottom: 0;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -25px;
            top: 5px;
            width: 15px;
            height: 15px;
            border-radius: 50%;
            background: white;
            border: 3px solid var(--primary);
            z-index: 1;
            transition: all 0.3s ease;
        }
        
        .timeline-item:hover::before {
            transform: scale(1.2);
            background: var(--primary);
        }
        
        .timeline-item::after {
            content: '';
            position: absolute;
            left: -18px;
            top: 20px;
            bottom: -5px;
            width: 2px;
            background: var(--secondary);
            opacity: 0.3;
        }
        
        .timeline-item:last-child::after {
            display: none;
        }
        
        .timeline-date {
            font-weight: 600;
            color: var(--primary);
            margin-bottom: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .timeline-date i {
            font-size: 1rem;
        }
        
        .timeline-title {
            font-weight: 600;
            margin-bottom: 8px;
            font-size: 1.2rem;
            color: var(--dark);
        }
        
        .timeline-subtitle {
            color: var(--secondary);
            font-style: italic;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .timeline-subtitle i {
            font-size: 0.9rem;
            color: var(--primary);
        }
        
        ul {
            padding-left: 20px;
            margin-top: 10px;
        }
        
        li {
            margin-bottom: 10px;
            position: relative;
            padding-left: 25px;
            list-style-type: none;
        }
        
        li::before {
            content: '\f00c';
            font-family: 'Font Awesome 6 Free';
            font-weight: 900;
            position: absolute;
            left: 0;
            top: 2px;
            color: var(--success);
        }
        
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            gap: 20px;
        }
        
        .skill-category {
            margin-bottom: 20px;
        }
        
        .skill-category h4 {
            margin-bottom: 15px;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
            padding-bottom: 5px;
            border-bottom: 1px dashed #eee;
        }
        
        .skill-category h4 i {
            font-size: 1.2rem;
        }
        
        .skill-item {
            display: flex;
            align-items: center;
            margin-bottom: 12px;
            padding: 8px 12px;
            background: rgba(46, 134, 193, 0.05);
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        .skill-item:hover {
            background: rgba(46, 134, 193, 0.1);
            transform: translateX(5px);
        }
        
        .skill-item i {
            color: var(--primary);
            margin-right: 10px;
            width: 20px;
            text-align: center;
            font-size: 1.1rem;
        }
        
        .skill-name {
            flex: 1;
        }
        
        .skill-level {
            height: 5px;
            background: rgba(46, 134, 193, 0.2);
            border-radius: 5px;
            margin-top: 5px;
            overflow: hidden;
        }
        
        .skill-level-bar {
            height: 100%;
            background: var(--primary);
            border-radius: 5px;
        }
        
        .references {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .reference-item {
            background: white;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            border-left: 3px solid var(--primary);
        }
        
        .reference-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
        }
        
        .reference-name {
            font-weight: 600;
            color: var(--primary-dark);
            margin-bottom: 5px;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .reference-name i {
            color: var(--primary);
        }
        
        .reference-title {
            font-style: italic;
            margin-bottom: 10px;
            color: var(--secondary);
        }
        
        .reference-contact {
            display: flex;
            align-items: center;
            gap: 8px;
            color: var(--dark);
        }
        
        footer {
            text-align: center;
            padding: 20px;
            color: var(--secondary);
            font-size: 0.9rem;
        }
        
        footer a {
            color: var(--primary);
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        footer a:hover {
            color: var(--primary-dark);
            text-decoration: underline;
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0;
                transform: translateY(30px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            section {
                padding: 20px;
            }
            
            .skills-container {
                grid-template-columns: 1fr;
            }
            
            .references {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .contact-item {
                padding: 6px 12px;
                font-size: 0.9rem;
            }
        }
        
        @media (max-width: 480px) {
            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 10px;
            }
            
            .timeline {
                padding-left: 20px;
            }
            
            .timeline-item::before {
                left: -22px;
                width: 12px;
                height: 12px;
            }
        }
        
        /* Ajouts pour la carte */
        .map-container {
            margin-top: 20px;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        
        .map-container iframe {
            width: 100%;
            height: 300px;
            border: 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="floating-bg"></div>
        
        <header>
            
            <h1>TARIK MERRAS</h1>
            <p class="subtitle">Technicien Spécialisé en Systèmes et Réseaux Informatiques</p>
            
            <div class="contact-info">
                <div class="contact-item">
                    <i class="fas fa-map-marker-alt"></i>
                    <span>92 Loi Tarik Boufkrane, Meknès</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-envelope"></i>
                    <span>tarikmerras20@gmail.com</span>
                </div>
                <div class="contact-item">
                    <i class="fas fa-phone"></i>
                    <span>+212 693 044430</span>
                </div>
                <div class="contact-item">
                    <i class="fab fa-linkedin"></i>
                    <span>linkedin.com/in/tarikmerras</span>
                </div>
            </div>
            
            <!-- Ajout de la carte Google Maps -->
            <div class="map-container">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3306.125837764745!2d-5.547403684784092!3d33.88113598064235!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xda0759b1f9a6a49%3A0x9e8c7c3b3b3b3b3b!2sBoufekrane%2C%20Mekn%C3%A8s%2C%20Maroc!5e0!3m2!1sfr!2sfr!4v1620000000000!5m2!1sfr!2sfr" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </header>
        
        <section>
            <h2><i class="fas fa-user-tie"></i> Profil Professionnel</h2>
            <p>Technicien stagiaire en <strong>Infrastructure Digitale (Systèmes & Réseaux)</strong> avec une expérience pratique dans la résolution de problèmes réseau pour l'OPPPT. Compétences en administration <strong>Windows/Linux</strong>, virtualisation (<strong>Proxmox/VMware</strong>), sécurité réseau (<strong>pfSense</strong>), et outils de surveillance (<strong>Zabbix, Nagios</strong>). Rigoureux et motivé pour progresser dans le domaine.</p>
            
            <div style="margin-top: 20px; display: flex; flex-wrap: wrap; gap: 10px;">
                <span style="padding: 5px 12px; background: rgba(46, 134, 193, 0.1); border-radius: 20px; font-size: 0.8rem; color: var(--primary-dark);">
                    <i class="fas fa-shield-alt"></i> Sécurité Réseau
                </span>
                <span style="padding: 5px 12px; background: rgba(46, 134, 193, 0.1); border-radius: 20px; font-size: 0.8rem; color: var(--primary-dark);">
                    <i class="fas fa-server"></i> Virtualisation
                </span>
                <span style="padding: 5px 12px; background: rgba(46, 134, 193, 0.1); border-radius: 20px; font-size: 0.8rem; color: var(--primary-dark);">
                    <i class="fas fa-network-wired"></i> Infrastructure
                </span>
            </div>
        </section>
        
        <section>
            <h2><i class="fas fa-graduation-cap"></i> Formation</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date"><i class="far fa-calendar-alt"></i> 2023 – 2025</div>
                    <h3 class="timeline-title">Technicien Spécialisé en Systèmes & Réseaux Informatiques</h3>
                    <p class="timeline-subtitle"><i class="fas fa-university"></i> ISTA Bab Tizimi</p>
                    <ul>
                        <li>Spécialisation en Infrastructure Digitale (option Systèmes et Réseaux)</li>
                        <li>Projets pratiques sur les réseaux Cisco et la sécurité informatique</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-date"><i class="far fa-calendar-alt"></i> 2024 – 2025</div>
                    <h3 class="timeline-title">Formation en Test d'Intrusion en Cybersécurité</h3>
                    <p class="timeline-subtitle"><i class="fas fa-university"></i> ISTA Bab Tizimi</p>
                    <ul>
                        <li>Apprentissage des techniques de pentesting</li>
                        <li>Sécurisation des systèmes d'information</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-date"><i class="far fa-calendar-alt"></i> 2022 – 2023</div>
                    <h3 class="timeline-title">Option Mathématiques et Applications</h3>
                    <p class="timeline-subtitle"><i class="fas fa-university"></i> Faculté des Sciences</p>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-date"><i class="far fa-calendar-alt"></i> 2021 – 2022</div>
                    <h3 class="timeline-title">Baccalauréat Sciences et Technologies Électriques</h3>
                    <p class="timeline-subtitle"><i class="fas fa-school"></i> Lycée Moulay Ismail</p>
                </div>
            </div>
        </section>
        
        <section>
            <h2><i class="fas fa-briefcase"></i> Expérience Professionnelle</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-date"><i class="far fa-calendar-alt"></i> 2023 – 2025</div>
                    <h3 class="timeline-title">Technicien Réseau</h3>
                    <p class="timeline-subtitle"><i class="fas fa-building"></i> CELUIE Informatique – ISTA Bab Tizimi, Meknès</p>
                    <ul>
                        <li>Surveillance et optimisation du <strong>réseau local</strong> (Cisco, HP, Ruijie)</li>
                        <li>Installation/config de <strong>pfSense</strong> (NAT, VPN, VLANs) et virtualisation <strong>Proxmox VE</strong></li>
                        <li>Résolution d'incidents complexes dans les établissements <strong>OPPPT</strong></li>
                        <li>Audit réseau et sécurisation avec <strong>Zabbix/Nagios</strong></li>
                        <li>Réparation de switches défectueux et restauration des fonctionnalités réseau</li>
                        <li>Création et gestion de VLANs pour la segmentation réseau</li>
                        <li>Mise en œuvre de stratégies de sauvegarde pour serveurs virtualisés</li>
                    </ul>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-date"><i class="far fa-calendar-alt"></i> 2025</div>
                    <h3 class="timeline-title">Stage - Technicien Systèmes & Réseaux</h3>
                    <p class="timeline-subtitle"><i class="fas fa-building"></i> Municipalité de Boufekrane</p>
                    <ul>
                        <li>Déploiement d'un réseau local sécurisé (Wi-Fi/câblé)</li>
                        <li>Gestion du parc informatique via <strong>GLPI</strong></li>
                        <li>Installation et configuration de <strong>Proxmox VE</strong></li>
                        <li>Déploiement et configuration du pare-feu <strong>pfSense</strong></li>
                        <li>Mise en œuvre de politiques de filtrage des sites web</li>
                    </ul>
                </div>
            </div>
        </section>
        
        <section>
            <h2><i class="fas fa-laptop-code"></i> Compétences Techniques</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h4><i class="fas fa-network-wired"></i> Réseaux</h4>
                    <div class="skill-item">
                        <i class="fab fa-cisco"></i>
                        <div>
                            <div class="skill-name">Cisco CCNA</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 85%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-fire"></i>
                        <div>
                            <div class="skill-name">pfSense</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 80%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-project-diagram"></i>
                        <div>
                            <div class="skill-name">VLANs/VPN</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 75%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-chart-line"></i>
                        <div>
                            <div class="skill-name">Zabbix/Nagios</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 70%"></div></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4><i class="fas fa-server"></i> Systèmes</h4>
                    <div class="skill-item">
                        <i class="fab fa-windows"></i>
                        <div>
                            <div class="skill-name">Windows Server</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 80%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fab fa-linux"></i>
                        <div>
                            <div class="skill-name">Linux (Admin)</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 75%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-cube"></i>
                        <div>
                            <div class="skill-name">Proxmox VE</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 70%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-boxes"></i>
                        <div>
                            <div class="skill-name">VirtualBox/VMware</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 65%"></div></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4><i class="fas fa-shield-alt"></i> Sécurité</h4>
                    <div class="skill-item">
                        <i class="fas fa-lock"></i>
                        <div>
                            <div class="skill-name">Cybersécurité</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 75%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-filter"></i>
                        <div>
                            <div class="skill-name">Filtrage Web</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 70%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-search"></i>
                        <div>
                            <div class="skill-name">Audits réseau</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 65%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-tasks"></i>
                        <div>
                            <div class="skill-name">GLPI</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 60%"></div></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h4><i class="fas fa-language"></i> Langues</h4>
                    <div class="skill-item">
                        <i class="fas fa-check"></i>
                        <div>
                            <div class="skill-name">Arabe (Natif)</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 100%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-check"></i>
                        <div>
                            <div class="skill-name">Français (Courant)</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 90%"></div></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <i class="fas fa-check"></i>
                        <div>
                            <div class="skill-name">Anglais (Technique)</div>
                            <div class="skill-level"><div class="skill-level-bar" style="width: 70%"></div></div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <section>
    <h2><i class="fas fa-certificate"></i> Certifications</h2>
    <div style="display: grid; grid-template-columns: repeat(auto-fill, minmax(300px, 1fr)); gap: 20px;">
        <!-- Certification Cisco 1 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #1BA0D1; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Cisco_logo_blue_2016.svg/1200px-Cisco_logo_blue_2016.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Networking Basics</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Cisco Networking Academy</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/NetworkingBasicsUpdate20250620-27-78v9yv.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Cisco 2 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #1BA0D1; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Cisco_logo_blue_2016.svg/1200px-Cisco_logo_blue_2016.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Network Defense</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Cisco Networking Academy</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/NetworkDefenseUpdate20250620-28-ztefgg.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Cisco 3 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #1BA0D1; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Cisco_logo_blue_2016.svg/1200px-Cisco_logo_blue_2016.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Introduction to Cybersecurity</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Cisco Networking Academy</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Mai 2024</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/Introduction_to_Cybersecurity_certificate_2003101900272-ofppt-edu-ma_132df137-ccd3-49d9-8384-e2aabfd66a5c.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Cisco 4 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #1BA0D1; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Cisco_logo_blue_2016.svg/1200px-Cisco_logo_blue_2016.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Ethical Hacker</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Cisco Networking Academy</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/EthicalHackerUpdate20250620-27-2ee8d1.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Cisco 5 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #1BA0D1; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Cisco_logo_blue_2016.svg/1200px-Cisco_logo_blue_2016.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Introduction to IoT</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Cisco Networking Academy</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Mai 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/IntrotoIoTUpdate20250620-27-2xhtad.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Cisco 6 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #1BA0D1; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Cisco_logo_blue_2016.svg/1200px-Cisco_logo_blue_2016.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Introduction to Data Science</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Cisco Networking Academy</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Mai 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/IntrotoDataScienceUpdate20250620-27-qbtbr4.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Microsoft 1 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #0078D4; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Microsoft_logo_%282012%29.svg/2560px-Microsoft_logo_%282012%29.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Décrire les composants d'Azure</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Microsoft Learn</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/Succ%C3%A8s%20-%20tarikmerras-6925%20_%20Microsoft%20Learn.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification Microsoft 2 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #0078D4; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/96/Microsoft_logo_%282012%29.svg/2560px-Microsoft_logo_%282012%29.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Describe cloud computing</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">Microsoft Learn</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/Achievements%20-%20tarikmerras-6925%20_%20Microsoft%20Learn.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification HP 1 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #0096D6; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/HP_logo_2012.svg/1200px-HP_logo_2012.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">AI for Beginners</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">HP LIFE</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/certificate-1.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>

        <!-- Certification HP 2 -->
        <div style="background: rgba(46, 134, 193, 0.05); padding: 15px; border-radius: 8px; border-left: 3px solid #0096D6; position: relative;">
            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 10px;">
                <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/ad/HP_logo_2012.svg/1200px-HP_logo_2012.svg.png" style="width: 40px; height: auto;">
                <h4 style="color: var(--primary-dark); margin: 0;">Business Email</h4>
            </div>
            <p style="color: var(--secondary); font-size: 0.9rem; margin-bottom: 10px;">HP LIFE</p>
            <p style="color: var(--secondary); font-size: 0.8rem;"><i class="far fa-calendar-alt"></i> Juin 2025</p>
            <a href="https://github.com/tarikmr/IDOSR/raw/7bd66ef527cf11b2bd9737386c9ff3e70581c542/certificate.pdf" 
               style="position: absolute; top: 15px; right: 15px; color: var(--primary);" 
               title="Voir le certificat" 
               target="_blank">
               <i class="fas fa-external-link-alt"></i>
            </a>
        </div>
    </div>
</section>
        
        <section>
            <h2><i class="fas fa-users"></i> Références</h2>
            <div class="references">
                <div class="reference-item">
                    <div class="reference-name"><i class="fas fa-user-tie"></i> Dr. Ali Sadiqui</div>
                    <div class="reference-title">Formateur en Réseaux & Sécurité Informatique</div>
                    <div class="reference-contact"><i class="fas fa-phone"></i> +212 667 392228</div>
                </div>
                
                <div class="reference-item">
                    <div class="reference-name"><i class="fas fa-user-tie"></i> Moulay Rachid Filali</div>
                    <div class="reference-title">Formateur Animateur</div>
                    <div class="reference-contact"><i class="fas fa-phone"></i> +212 718 691553</div>
                </div>
                
                <div class="reference-item">
                    <div class="reference-name"><i class="fas fa-user-tie"></i> M. Abdeslam Saber</div>
                    <div class="reference-title">Formateur en Réseaux Informatiques</div>
                    <div class="reference-contact"><i class="fas fa-phone"></i> +212 663 444684</div>
                </div>
            </div>
        </section>
        
        <footer>
            <p>© 2025 TARIK MERRAS - Tous droits réservés | <a href="#" id="print-btn"><i class="fas fa-print"></i> Imprimer</a></p>
        </footer>
    </div>
    
    <script>
        // Animation au défilement
        document.addEventListener('DOMContentLoaded', function() {
            const sections = document.querySelectorAll('section');
            const contactItems = document.querySelectorAll('.contact-item');
            const skillItems = document.querySelectorAll('.skill-item');
            const timelineItems = document.querySelectorAll('.timeline-item');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.opacity = 1;
                        entry.target.style.transform = 'translateY(0)';
                    }
                });
            }, { threshold: 0.1 });
            
            sections.forEach(section => {
                section.style.opacity = 0;
                section.style.transform = 'translateY(30px)';
                section.style.transition = 'all 0.6s ease-out';
                observer.observe(section);
            });
            
            // Animation des éléments de contact
            contactItems.forEach((item, index) => {
                item.style.transition = `all 0.4s ease-out ${index * 0.1}s`;
                item.style.opacity = 0;
                item.style.transform = 'translateY(20px)';
                
                setTimeout(() => {
                    item.style.opacity = 1;
                    item.style.transform = 'translateY(0)';
                }, 500 + index * 100);
            });
            
            // Animation des compétences
            skillItems.forEach((item, index) => {
                item.style.transition = `all 0.4s ease-out ${index * 0.05}s`;
            });
            
            // Animation des éléments de timeline
            timelineItems.forEach((item, index) => {
                item.style.transition = `all 0.4s ease-out ${index * 0.1}s`;
            });
            
            // Bouton d'impression
            document.getElementById('print-btn').addEventListener('click', function(e) {
                e.preventDefault();
                window.print();
            });
        });
        
        // Effet de survol sur les icônes de section
        document.querySelectorAll('h2 i').forEach(icon => {
            icon.addEventListener('mouseenter', function() {
                this.style.animation = 'pulse 0.5s ease';
            });
            
            icon.addEventListener('mouseleave', function() {
                this.style.animation = '';
            });
        });
    </script>
</body>
</html>
