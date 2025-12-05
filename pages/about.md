---
layout: page
permalink: /about.html
title: "Profil Technique"
description: "Ingénieur Logiciel & DevOps - Approche, Compétences et Philosophie."
header-img: 
last-updated: 2025-12-05
---

<div class="about-container mt-2">
    <div class="row align-items-center mb-5">
        <div class="col-lg-5 mb-4 mb-lg-0 text-center">
            <div class="profile-wrapper animate__animated animate__fadeInLeft">
                <div class="profile-card">
                    <img src="{{ site.baseurl }}/assets/img/{{ site.profile_image }}" 
                         alt="Henri Bikouri - Portrait Ingénieur" 
                         class="profile-img img-fluid shadow-lg"
                         style="border-radius: 20px; border: 4px solid white;">
                    <div class="floating-badge badge-top-right">
                        <i class="fas fa-terminal"></i> Backend
                    </div>
                    <div class="floating-badge badge-bottom-left">
                        <i class="fas fa-cloud"></i> DevOps
                    </div>
                </div>
            </div>
        </div>
        <div class="col-lg-7">
            <div class="terminal-window shadow-sm animate__animated animate__fadeInRight">
                <div class="terminal-header">
                    <span class="terminal-dot red"></span>
                    <span class="terminal-dot yellow"></span>
                    <span class="terminal-dot green"></span>
                    <span class="terminal-title">root@henri-bikouri:~/bio</span>
                </div>
                <div class="terminal-body">
                    <p class="console-text">
                        <span class="prompt">$</span> init_profile --verbose
                    </p>
                    <h2 class="font-weight-bold mb-3 text-white">Henri Bikouri</h2>
                    <p class="lead text-light opacity-75">
                        {{ site.description }}
                    </p>
                    <hr style="border-color: rgba(255,255,255,0.1);">
                    <p class="text-light small mt-3">
                        <span class="prompt">root@henri:~#</span> cat mission.log<br>
                        <span class="text-success">>></span> "Concevoir des architectures résilientes."<br>
                        <span class="text-success">>></span> "Automatiser l'impossible."<br>
                        <span class="text-success">>></span> "Transformer le code en valeur."
                    </p>
                    <div class="mt-4">
                        <a href="{{ site.baseurl }}/assets/pdf/CV_HENRI_BIKOURI.pdf" target="_blank" class="btn btn-sm btn-outline-success font-weight-bold" style="border-radius: 0;">
                            <i class="fas fa-download mr-2"></i> wget cv_henri.pdf
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div class="row mb-5 text-center animate__animated animate__fadeInUp" style="animation-delay: 0.3s;">
        <div class="col-md-4 mb-3">
            <div class="p-3 shadow-sm bg-white rounded">
                <h2 class="font-weight-bold display-4" style="color: #149f98;">3+</h2>
                <p class="text-muted text-uppercase small letter-spacing-2">Années d'Expérience</p>
            </div>
        </div>
        <div class="col-md-4 mb-3">
            <div class="p-3 shadow-sm bg-white rounded">
                <h2 class="font-weight-bold display-4" style="color: #149f98;">15+</h2>
                <p class="text-muted text-uppercase small letter-spacing-2">Projets Déployés</p>
            </div>
        </div>
        <div class="col-md-4 mb-3">
            <div class="p-3 shadow-sm bg-white rounded">
                <h2 class="font-weight-bold display-4" style="color: #149f98;">100%</h2>
                <p class="text-muted text-uppercase small letter-spacing-2">Commitment</p>
            </div>
        </div>
    </div>
    <div class="row mb-5">
        <div class="col-12">
            <h3 class="font-weight-bold mb-4 border-left pl-3" style="border-color: #149f98 !important; border-width: 5px !important;">
                Architecture & Philosophie
            </h3>
            <div class="accordion custom-accordion shadow-sm" id="accordionSkills">
                <div class="card border-0 mb-1">
                    <div class="card-header bg-white p-0" id="headingOne">
                        <h2 class="mb-0">
                            <button class="btn btn-link btn-block text-left font-weight-bold text-dark d-flex justify-content-between align-items-center p-4" type="button" data-toggle="collapse" data-target="#collapseOne" aria-expanded="true" aria-controls="collapseOne">
                                <span><i class="fas fa-cogs mr-3" style="color: #149f98;"></i> Ingénierie Système & DevOps</span>
                                <i class="fas fa-chevron-down text-muted"></i>
                            </button>
                        </h2>
                    </div>
                    <div id="collapseOne" class="collapse show" aria-labelledby="headingOne" data-parent="#accordionSkills">
                        <div class="card-body bg-light text-muted pl-5">
                            Mon terrain de jeu favori. Je maîtrise la chaîne CI/CD complète, de la conteneurisation (Docker, K8s) à l'orchestration cloud. Mon objectif : réduire le "Time-to-Market" sans sacrifier la stabilité.
                        </div>
                    </div>
                </div>
                <div class="card border-0 mb-1">
                    <div class="card-header bg-white p-0" id="headingTwo">
                        <h2 class="mb-0">
                            <button class="btn btn-link btn-block text-left collapsed font-weight-bold text-dark d-flex justify-content-between align-items-center p-4" type="button" data-toggle="collapse" data-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
                                <span><i class="fas fa-code-branch mr-3" style="color: #149f98;"></i> Développement Backend</span>
                                <i class="fas fa-chevron-down text-muted"></i>
                            </button>
                        </h2>
                    </div>
                    <div id="collapseTwo" class="collapse" aria-labelledby="headingTwo" data-parent="#accordionSkills">
                        <div class="card-body bg-light text-muted pl-5">
                            Architecture Microservices ou Monolithe modulaire ? Le choix dépend du besoin. Je conçois des APIs RESTful et GraphQL robustes, sécurisées et documentées, prêtes à scaler.
                        </div>
                    </div>
                </div>
                <div class="card border-0 mb-1">
                    <div class="card-header bg-white p-0" id="headingThree">
                        <h2 class="mb-0">
                            <button class="btn btn-link btn-block text-left collapsed font-weight-bold text-dark d-flex justify-content-between align-items-center p-4" type="button" data-toggle="collapse" data-target="#collapseThree" aria-expanded="false" aria-controls="collapseThree">
                                <span><i class="fas fa-lightbulb mr-3" style="color: #149f98;"></i> Innovation & Veille</span>
                                <i class="fas fa-chevron-down text-muted"></i>
                            </button>
                        </h2>
                    </div>
                    <div id="collapseThree" class="collapse" aria-labelledby="headingThree" data-parent="#accordionSkills">
                        <div class="card-body bg-light text-muted pl-5">
                            L'ingénierie est un apprentissage constant. Je surveille activement les tendances (AI, Cloud Native) pour proposer des solutions pérennes et non juste "à la mode".
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </div>

</div>