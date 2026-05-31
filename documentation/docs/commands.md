# Commandes

La plupart des commandes peuvent aussi être utilisées avec le préfixe `!` au lieu de `.` (exemple : `!ready`)

## Commandes joueurs

- `.ready` Marque le joueur comme prêt (alias : `.r`)
- `.unready` Marque le joueur comme non prêt (alias : `.ur`, `.notready`)
- `.pause` Met le match en pause en freezetime (tactique ou normale, selon `matchzy_use_pause_command_for_tactical_pause`)
- `.tech` Met le match en pause en freezetime
- `.unpause` Demande la reprise du match (les deux équipes doivent taper `.unpause`)
- `.stay` Reste du même côté après le round couteau
- `.switch` / `.swap` Change de côté après le round couteau
- `.stop` Restaure le backup du round en cours (les deux équipes doivent taper `.stop`)
- `.tac` Lance un timeout tactique
- `.coach <side>` Commence à coacher le côté indiqué. Exemple : `.coach t`
- `.uncoach` Quitte le slot de coach

## Commandes practice

- `.spawn <numéro>` Téléporte au spawn compétitif demandé (même équipe)
- `.ctspawn <numéro>` Téléporte au spawn CT demandé (alias : `.cts`)
- `.tspawn <numéro>` Téléporte au spawn T demandé (alias : `.ts`)
- `.bestspawn` Téléporte au spawn le plus proche de ta position
- `.worstspawn` Téléporte au spawn le plus éloigné de ta position
- `.bestctspawn` Téléporte au spawn CT le plus proche
- `.worstctspawn` Téléporte au spawn CT le plus éloigné
- `.besttspawn` Téléporte au spawn T le plus proche
- `.worsttspawn` Téléporte au spawn T le plus éloigné
- `.showspawns` Affiche tous les spawns compétitifs
- `.hidespawns` Cache les spawns affichés
- `.bot` Ajoute un bot à ta position actuelle
- `.crouchbot` Ajoute un bot accroupi à ta position (alias : `.cbot`)
- `.boost` Ajoute un bot et te booste dessus
- `.crouchboost` Ajoute un bot accroupi et te booste dessus
- `.ct` / `.t` / `.spec` Change d'équipe
- `.fas` / `.watchme` Force tous les joueurs en spectateur sauf toi
- `.nobots` Supprime tous les bots
- `.clear` Supprime toutes les smokes, molotovs et incendiaires actifs
- `.fastforward` Avance le temps serveur à 20 secondes (alias : `.ff`)
- `.noflash` Active/désactive l'immunité aux flashbangs (alias : `.noblind`)
- `.dryrun` Active le mode dry-run (alias : `.dry`)
- `.god` Active le mode dieu
- `.solid` Active/désactive `mp_solid_teammates`
- `.impacts` Active/désactive `sv_showimpacts`
- `.traj` Active/désactive `sv_grenade_trajectory_prac_pipreview` (alias : `.pip`)
- `.break` Casse toutes les entités destructibles (vitres, portes, ventilations...)
- `.timer` Lance un chronomètre, tape `.timer` à nouveau pour l'arrêter
- `.savenade <nom> <description optionnelle>` Sauvegarde un lineup (alias : `.sn`)
- `.loadnade <nom>` Charge un lineup (alias : `.ln`)
- `.deletenade <nom>` Supprime un lineup (alias : `.dn`)
- `.importnade <code>` Importe un lineup via son code (alias : `.in`)
- `.listnades <filtre optionnel>` Liste les lineups sauvegardés (alias : `.lin`)
- `.rethrow` Relance ta dernière grenade (alias : `.rt`)
- `.last` Téléporte à l'endroit depuis lequel tu as lancé ta dernière grenade
- `.back <numéro>` Téléporte à la position indiquée dans ton historique de grenades
- `.delay <secondes>` Ajoute un délai à ta dernière grenade (utilisé avec `.rethrow` / `.throwindex`)
- `.throwindex <index>` Relance la grenade à l'index indiqué. Exemple : `.throwindex 1 2`
- `.lastindex` Affiche l'index de ta dernière grenade lancée
- `.rethrowsmoke` Relance ta dernière smoke
- `.rethrownade` Relance ta dernière HE
- `.rethrowflash` Relance ta dernière flash
- `.rethrowmolotov` Relance ta dernière molotov
- `.rethrowdecoy` Relance ton dernier decoy

## Commandes admin

- `.start` Force le démarrage du match
- `.restart` Force le redémarrage du match (alias : `.endmatch`, `.forceend`)
- `.forcepause` Met le match en pause côté admin (alias : `.fp`)
- `.forceunpause` Force la reprise du match (alias : `.fup`)
- `.forceready` Force l'équipe du joueur comme prête
- `.restore <round>` Restaure le backup du round indiqué
- `.skipveto` / `.sv` Passe la phase de veto
- `.roundknife` / `.rk` Active/désactive le round couteau
- `.playout` Active/désactive le playout (tous les rounds joués peu importe le score, utile en scrim)
- `.whitelist` Active/désactive la whitelist joueurs
- `.readyrequired <nombre>` Définit le nombre de joueurs prêts requis pour démarrer
- `.settings` Affiche les paramètres actuels du match
- `.map <mapname>` Change la map
- `.asay <message>` Envoie un message admin dans le chat général
- `.reload_admins` Recharge les admins depuis `admins.json`
- `.team1 <nom>` Définit le nom de l'équipe 1 (CT par défaut)
- `.team2 <nom>` Définit le nom de l'équipe 2 (T par défaut)
- `.prac` Lance le mode practice (alias : `.tactics`)
- `.exitprac` Quitte le mode practice et revient en mode match
- `.rcon <commande>` Envoie une commande au serveur