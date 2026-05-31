# Configuration

Tous les fichiers de configuration de MMS se trouvent dans `csgo/cfg/MatchZy`.

## Créer des admins

Deux méthodes disponibles :

**1. Via le système admin de CounterStrikeSharp**

Ajouter une entrée dans `/addons/counterstrikesharp/configs/admins.json` :

```json
{
  "c3drick0s": {
    "identity": "76561198154367261",
    "flags": ["@css/root"]
  },
  "Autre admin": {
    "identity": "SteamID2",
    "flags": ["@css/config", "@css/rcon"]
  }
}
```

Permissions par flag :
- `@css/root` : accès à toutes les commandes admin
- `@css/config` : commandes de configuration
- `@custom/prac` : commandes practice
- `@css/map` : changement de map et toggle practice
- `@css/rcon` : commandes RCON via `!rcon`
- `@css/chat` : messages admin via `!asay`

**2. Via le fichier `admins.json` de MMS**

Dans `csgo/cfg/MatchZy/admins.json` (créé automatiquement au premier chargement) :

```json
{
  "76561198154367261": "",
  "<autre_steam_id>": ""
}
```

## ConVars (config.cfg)

Le fichier `csgo/cfg/MatchZy/config.cfg` est exécuté à chaque chargement du plugin. Pour recharger : `exec MatchZy/config.cfg`.

#### `matchzy_knife_enabled_default`
Active le round couteau par défaut. Peut être togglé par un admin avec `.roundknife`.<br>**`Default: true`**

#### `matchzy_minimum_ready_required`
Nombre minimum de joueurs prêts pour démarrer. Si 0, tous les joueurs connectés doivent être prêts.<br>**`Default: 2`**

#### `matchzy_stop_command_available`
Active la commande `.stop` pour restaurer le backup du round en cours.<br>**`Default: false`**

#### `matchzy_stop_command_no_damage`
Désactive `.stop` si un joueur a infligé des dégâts à l'équipe adverse.<br>**`Default: false`**

#### `matchzy_pause_after_restore`
Met le match en pause après une restauration de round.<br>**`Default: true`**

#### `matchzy_whitelist_enabled_default`
Active la whitelist joueurs par défaut. Peut être togglée avec `.whitelist`.<br>**`Default: false`**

#### `matchzy_kick_when_no_match_loaded`
Expulse tous les clients si aucun match n'est chargé via `matchzy_loadmatch`.<br>**`Default: false`**

#### `matchzy_demo_path`
Dossier de sauvegarde des démos. Ne doit pas commencer par `/` et doit se terminer par `/`.<br>**`Default: MatchZy/`**

#### `matchzy_demo_name_format`
Format du nom des démos. Variables disponibles : `{TIME}`, `{MATCH_ID}`, `{MAP}`, `{MAPNUMBER}`, `{TEAM1}`, `{TEAM2}`. Ne pas inclure `.dem`.<br>**`Default: "{TIME}_{MATCH_ID}_{MAP}_{TEAM1}_vs_{TEAM2}"`**

#### `matchzy_demo_upload_url`
URL d'upload automatique de la démo en fin de map.<br>**`Default: ""`**

#### `matchzy_chat_prefix`
Préfixe chat MMS. Couleurs disponibles : `{Default}`, `{Red}`, `{Green}`, `{Gold}`, `{Blue}`, etc. Toujours terminer par `{Default}`.<br>**`Default: [{Red}MMS{Default}]`**

#### `matchzy_admin_chat_prefix`
Préfixe chat pour les messages admin via `.asay`.<br>**`Default: [{Gold}ADMIN{Default}]`**

#### `matchzy_chat_messages_timer_delay`
Délai en secondes entre les messages de rappel MMS (non prêt, pause, etc.).<br>**`Default: 13`**

#### `matchzy_playout_enabled_default`
Active le playout (tous les rounds joués peu importe le score). Utile en scrim.<br>**`Default: false`**

#### `matchzy_reset_cvars_on_series_end`
Restaure les CVars de la config match à la fin de la série.<br>**`Default: true`**

#### `matchzy_use_pause_command_for_tactical_pause`
Utilise `.pause` comme pause tactique.<br>**`Default: false`**

#### `matchzy_autostart_mode`
Mode au démarrage : `0` = aucun, `1` = match, `2` = practice.<br>**`Default: 1`**

#### `matchzy_save_nades_as_global_enabled`
Sauvegarde les nades en global (partagées entre tous les joueurs).<br>**`Default: false`**

#### `matchzy_allow_force_ready`
Autorise la commande `!forceready`.<br>**`Default: true`**

#### `matchzy_max_saved_last_grenades`
Nombre maximum de grenades sauvegardées dans l'historique par joueur/map. `0` = illimité.<br>**`Default: 512`**

#### `matchzy_smoke_color_enabled`
Colorie les smokes avec la couleur d'équipe du joueur (radar).<br>**`Default: false`**

#### `matchzy_everyone_is_admin`
Donne les permissions admin à tous les joueurs.<br>**`Default: false`**

#### `matchzy_show_credits_on_match_start`
Affiche le message MisteryA Match System au démarrage du match.<br>**`Default: true`**

#### `matchzy_hostname_format`
Format du hostname serveur. Variables : `{TIME}`, `{MATCH_ID}`, `{MAP}`, `{MAPNUMBER}`, `{TEAM1}`, `{TEAM2}`, `{TEAM1_SCORE}`, `{TEAM2_SCORE}`. Mettre `""` pour désactiver.<br>**`Default: MisteryA | {TEAM1} vs {TEAM2}`**

#### `matchzy_match_start_message`
Message affiché au démarrage du match. Utiliser `$$$` pour sauter une ligne. Mettre `""` pour désactiver.<br>**`Default: ""`**

#### `matchzy_loadbackup`
Charge un backup depuis un fichier. Relatif à `csgo/MatchZyDataBackup/`.

#### `matchzy_loadbackup_url`
Charge un backup depuis une URL HTTP(S) GET.

#### `matchzy_remote_backup_url`
URL d'envoi automatique des backups en HTTP POST.

#### `matchzy_remote_backup_header_key`
Clé du header HTTP pour les requêtes de backup.<br>**`Default: "Authorization"`**

#### `matchzy_remote_backup_header_value`
Valeur du header HTTP pour les requêtes de backup.<br>**`Default: ""`**

#### `matchzy_enable_damage_report`
Affiche le rapport de dégâts après chaque round.<br>**`Default: true`**

#### `matchzy_addplayer <steam64> <team1|team2|spec> [name]`
Ajoute un joueur par SteamID64 à l'équipe indiquée.

#### `matchzy_removeplayer <steam64>`
Retire un joueur de toutes les équipes.

## CFGs Warmup / Knife / Live / Practice

Dans `csgo/cfg/MatchZy` : `warmup.cfg`, `knife.cfg`, `live.cfg`, `prac.cfg`. Exécutés automatiquement à chaque phase. Modifier selon les besoins. Ajouter `live_override.cfg` pour surcharger `live.cfg` sans le modifier.

## Whitelist joueurs

Dans `csgo/cfg/MatchZy/whitelist.cfg`, ajouter les SteamID64 :