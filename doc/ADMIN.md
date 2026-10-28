## Operation

* The game server is a small Node.js service (`systemctl status __APP__`). Logs are in `/var/log/__APP__/__APP__.log`.
* Game rooms are kept in `__DATA_DIR__/rooms.json` (saved every 30 seconds and when the service stops). Rooms without players are removed from memory after 30 minutes.
* Online play needs a WebSocket connection through the web server. If it does not connect, check that the app is reachable through its URL and not through a different host name.
* No accounts: anyone who knows a room code can join it. Use the access setting of the app in the YunoHost admin if the game should only be open to your users.
