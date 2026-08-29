# Election-Polls-Scraper-Philippines-Poland
Ce projet consiste à collecter, nettoyer et analyser des données de sondages électoraux pour dix élections aux Philippines (présidentielles 2010, 2016, 2022) et en Pologne (législatives 2001, 2005, 2007, 2011, 2015, 2019, 2023), via web scraping de Wikipédia (BeautifulSoup) puis traitement avec pandas.

Les tableaux de sondages sont extraits automatiquement pour chaque élection, fusionnés, nettoyés (gestion des colonnes fusionnées, harmonisation des noms de colonnes) puis restructurés du format large au format long afin d'associer, pour chaque sondage et chaque candidat/parti, une prédiction et le résultat final. Une orientation politique (gauche, centre, droite, extrême droite, etc.) est ensuite attribuée à chaque candidat via un dictionnaire d'affiliations politiques construit manuellement.

Une détection d'outliers par score Z (seuil de 3 écarts-types) est appliquée sur les colonnes numériques, et les données standardisées sont exportées en fichiers Excel par élection. Les dates de sondage sont nettoyées et uniformisées (extraction et reconstruction du format date), et les valeurs manquantes sont traitées.

Enfin, le projet propose un tableau de bord interactif développé avec Streamlit, permettant de sélectionner un pays et une année d'élection, de filtrer les sondages sur une période donnée, de visualiser l'évolution des prédictions de chaque candidat/parti dans le temps (avec zoom ajustable sur l'axe Y), d'afficher des statistiques descriptives et de télécharger les données filtrées au format CSV.
