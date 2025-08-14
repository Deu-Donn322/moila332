Bot d'Interprétation Biblique des Rêves

Ce projet est un bot Telegram qui interprète les rêves des utilisateurs à partir d'une perspective biblique, en s'inspirant des Écritures et des symboles spirituels. Il fournit des analyses détaillées, des versets d'encouragement, des prières personnalisées, et des conseils spirituels pour aider les utilisateurs à discerner le message divin derrière leurs rêves.

Fonctionnalités





Interprétation universelle : Analyse tout type de rêve, même sans symboles prédéfinis, en se basant sur le contexte, les émotions, et une approche narrative.



Symboles bibliques : Détecte des symboles comme l'eau, la mort, la maladie, le feu, etc., avec des interprétations variées et non répétitives.



Émotions détectées : Identifie des émotions (peur, tristesse, espoir, etc.) pour personnaliser les prières et conseils.



Historique : Stocke les rêves et leurs interprétations dans une base SQLite avec pagination.



Anti-répétition : Utilise un système de sélection non répétitive pour éviter les redondances dans les réponses.



Interface utilisateur : Commandes Telegram et boutons interactifs pour une expérience fluide.

Prérequis





Python 3.8 ou supérieur



Compte Telegram avec un token de bot (obtenu via BotFather)



Bibliothèques listées dans requirements.txt

Installation





Cloner le dépôt :

git clone <URL_DU_DÉPÔT>
cd dreambot



Créer un environnement virtuel (optionnel, mais recommandé) :

python -m venv venv
source venv/bin/activate  # Sur Windows : venv\Scripts\activate



Installer les dépendances :

pip install -r requirements.txt



Configurer le token Telegram :





Remplacez la variable token dans dreambot.py par votre propre token Telegram :

token = "VOTRE_TOKEN_ICI"



Le token actuel dans le code est spécifique à l'utilisateur et doit être sécurisé.



Lancer le bot :

python dreambot.py

Utilisation





Démarrer le bot :





Envoyez /start sur Telegram pour voir le menu principal avec des boutons interactifs.



Commandes disponibles :





/start : Affiche le message de bienvenue et le menu.



/aide : Fournit des instructions sur l'utilisation du bot.



/versets : Propose un verset biblique d'encouragement.



/prieres : Offre une prière adaptée au contexte.



/historique [page] : Affiche l'historique des rêves (ex. : /historique 2 pour la page 2).



Boutons interactifs : "Interpréter un rêve", "Versets d'encouragement", "Prières spéciales", "Mon historique", "Aide".



Envoyer un rêve :





Cliquez sur "Interpréter un rêve" ou envoyez directement une description (ex. : "J'ai rêvé que j'étais atteint d'un cancer et que je vais bientôt mourir").



Incluez des détails (émotions, lieux, objets, personnes) pour une interprétation plus riche.



Le bot vérifie si le message est un rêve (mots comme "rêve", "songe", etc.). Sinon, il suggère de reformuler.

Exemple d'interprétation

Rêve soumis : "J'ai rêvé que j'étais atteint d'un cancer et que je vais bientôt mourir."

Réponse du bot (extrait) :

🌟 INTERPRÉTATION BIBLIQUE DE VOTRE RÊVE 🌟

📅 Analyse: 14/08/2025 17:35

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📖 Résumé du rêve:
J'ai rêvé que j'étais atteint d'un cancer et que je vais bientôt mourir.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🌙 Message spirituel:
Même dans les rêves troublants, Dieu offre espoir, guérison et direction. Confiez-vous à Lui.

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔍 Symboles bibliques identifiés:
• MALADIE
  Signification: La maladie, comme le cancer, peut symboliser une lutte spirituelle ou une affliction qui ronge l'âme...
  📖 Verset: Psaumes 103:3
  🙏 Prière: Seigneur, guéris toutes mes maladies...

• MORT
  Signification: La mort dans un rêve peut symboliser la fin d'un cycle de vie...
  📖 Verset: Jean 11:25-26
  🙏 Prière: Jésus, tu es la résurrection et la vie...

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
💭 Analyse contextuelle:
Ce rêve semble tisser une histoire spirituelle riche, où la *maladie* et la *mort* révèlent un message divin. Il peut indiquer une période de transition ou de confrontation avec des craintes profondes. Dieu vous invite à Lui confier vos peurs et à chercher Sa paix...

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🌟 Interprétation générale:
Ce rêve pourrait signaler un besoin de guérison émotionnelle ou spirituelle...

📖 Verset d'encouragement:
Psaumes 103:2-3
Que mon âme bénisse l'Éternel! ... Qui guérit toutes tes maladies.

🙏 Prière personnalisée:
Seigneur, face à la peur de la mort, rappelle-moi que tu es la résurrection...

💡 Conseils spirituels:
• Confiez vos peurs de maladie ou de mort à Dieu...
• Cherchez la guérison spirituelle et physique par la foi...

🕊️ Conclusion:
Dieu est votre guérisseur et votre refuge; confiez-Lui vos craintes...

Structure du projet





dreambot.py : Code principal du bot, incluant la logique d'interprétation, la gestion de la base de données, et les handlers Telegram.



requirements.txt : Liste des dépendances Python.



dreambot.db : Base de données SQLite (créée automatiquement) pour stocker les rêves et les sélections non répétitives.

Déploiement

Pour déployer le bot sur un serveur (ex. : Heroku, AWS, ou un VPS) :





Configurez un environnement avec Python et les dépendances.



Sécurisez le token Telegram (utilisez des variables d'environnement).



Assurez-vous que le bot peut écrire dans le répertoire pour la base SQLite (dreambot.db).



Lancez dreambot.py en mode production (ex. : avec gunicorn ou un service systemd).

Contribuer





Forkez le dépôt.



Ajoutez de nouveaux symboles, versets, ou prières dans SYMBOLS, VERSETS_ENCOURAGEMENT, ou PRIERE_PAR_EMOTION.



Testez localement avant de soumettre une pull request.



Respectez le style de code Python (PEP 8).

Avertissement





Ce bot fournit des interprétations spirituelles basées sur une perspective biblique. Il ne remplace pas un conseil pastoral ou professionnel.



Les rêves sont subjectifs; les utilisateurs doivent discerner les interprétations avec prière et sagesse.

Licence

Ce projet est sous licence MIT. Voir le fichier LICENSE (à créer si nécessaire).



Développé avec ❤️ pour aider les âmes à entendre la voix de Dieu à travers leurs rêves.
