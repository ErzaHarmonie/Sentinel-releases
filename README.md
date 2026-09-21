# Sentinel pour Windows

<p align="center"><img src="https://github.com/ErzaHarmonie/Sentinel-releases/releases/latest/download/sentinel-logo.png" alt="Logo Sentinel" width="360"></p>

Sentinel aide à comprendre l’état de son PC : mesures matérielles locales, apprentissage du profil de la machine et actions de maintenance contrôlées. Une mesure absente reste **Indisponible**.

## Télécharger

**[Télécharger Sentinel 2.4.3](https://github.com/ErzaHarmonie/Sentinel-releases/releases/download/v2.4.3/Sentinel-2.4.3-Setup.exe)**

Les installateurs et les notes de version sont disponibles dans les [versions publiées](https://github.com/ErzaHarmonie/Sentinel-releases/releases). Plateforme : Windows 10 (18362 ou plus récent) et Windows 11, x64.

Le paquet inclut le runtime .NET. Les informations sur les composants tiers et le pilote optionnel de mesure matérielle sont présentées dans l’installateur.

## IA locale, même sans NPU

Depuis la version 2.4.0, Sentinel choisit automatiquement un moteur pour analyser le profil du PC : NPU compatible, puis GPU DirectML, puis CPU. L’application vérifie le moteur effectivement utilisé et le résultat avant de les afficher. La disponibilité de l’accélération dépend du matériel et de ses pilotes.

Les calculs restent sur votre PC. Dans **IA locale**, utilisez **Analyser mon PC** ; lorsque le suivi IA est activé, le choix du moteur est également automatique. Le diagnostic du NPU reste accessible séparément.

## Mises à jour

Après l’installation de Sentinel 2.4.3, ouvrez **Paramètres → Vérifier les mises à jour**. Vous choisissez le téléchargement et l’installation ; Sentinel vérifie la signature EdDSA du fichier reçu. La recherche n’envoie ni vos mesures matérielles ni votre profil appris.

**Si vous utilisez 2.4.2 ou une version antérieure, installez manuellement la 2.4.3 une fois.** La clé de signature historique a été remplacée : cette installation adopte la nouvelle clé pour les mises à jour suivantes. Les anciennes versions peuvent encore indiquer que la 2.4.1 est la dernière version. Fermez Sentinel avant de lancer l’installateur. Les données locales existantes sont conservées. La relance après installation reste manuelle.

Depuis la version 2.4.0, un résumé court présente les nouveautés au premier lancement de chaque nouvelle version. Cliquez sur **Compris** pour le fermer ; il reste consultable dans **À propos → Nouveautés de cette version**.

Le nouveau flux public est [appcast-v2.xml](https://github.com/ErzaHarmonie/Sentinel-releases/releases/latest/download/appcast-v2.xml). L’ancien fichier `appcast.xml` reste disponible avec la version 2.4.1 pour les anciens clients. La signature de mise à jour ne constitue pas une signature Authenticode de l’éditeur Windows.

Ce dépôt est consacré à la distribution : installateurs, visuels et notes de version. Le code source de Sentinel est conservé séparément.
