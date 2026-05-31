# MisteryA Match System (MMS)

Fork de [MatchZy](https://github.com/shobhit-pathak/MatchZy) adapté pour MisteryA Esport.

MMS est un plugin CS2 (CounterStrikeSharp) pour gérer les pratiques, scrims et matchs compétitifs de MisteryA.

## Fonctionnalités

- Mode Practice avec `.bot`, `.spawn`, `.ctspawn`, `.tspawn`, `.nobots`, `.rethrow`, `.last`, `.timer`, `.clear`, `.exitprac` et bien d'autres commandes
- Support BO1/BO3/BO5 avec système de veto intégré
- Configuration et verrouillage des joueurs dans leur équipe
- Round couteau (logique : équipe avec le plus de joueurs gagne ; en cas d'égalité, avantage HP ; sinon aléatoire)
- Enregistrement automatique des démos (demo recording start/stop)
- Upload automatique des démos en fin de map sur URL configurée
- Whitelist joueurs
- Système de coaching
- Rapport de dégâts après chaque round
- Restauration de round (backup système Valve)
- Système d'administration avec commandes admin
- Statistiques en base de données SQLite (MySQL supporté) + export CSV

## Branding MisteryA

- Préfixe chat : `[MMS]` (rouge)
- Préfixe admin : `[ADMIN]` (gold)
- Hostname : `MisteryA | {TEAM1} vs {TEAM2}`

## Différences avec MatchZy upstream

| Fonctionnalité | MatchZy | MMS |
|---|---|---|
| Branding | MatchZy / WD- | MisteryA / c3drick0s |
| Get5 / G5API | ✅ Supporté | ❌ Retiré |
| Création match panel web | ✅ Supporté | ❌ Retiré |

## Installation

1. Installer [Metamod](https://www.sourcemm.net/) et [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp)
2. Télécharger la dernière release depuis [Releases](https://github.com/c3drick0s/MisteryA-Match-System/releases)
3. Copier `MMS.dll` dans `addons/counterstrikesharp/plugins/MMS/`

## Roadmap

- **MMS Stat v1** — collecte des statistiques en fin de match (Kills, Deaths, ADR, HS%, Clutchs...)
- **MMS Stat v2** — statistiques avancées (Opening Kills, Trades, Flash Assists, KAST, Impact Score)
- **MMS Live** — panel web temps réel via WebSocket
- **MMS Tournament** — projet indépendant (BO3/BO5, brackets, tournois)

## Crédits

- [MatchZy](https://github.com/shobhit-pathak/MatchZy) par WD- — base technique du projet
- [CounterStrikeSharp](https://github.com/roflmuffin/CounterStrikeSharp/) par roflmuffin

## Licence

MIT