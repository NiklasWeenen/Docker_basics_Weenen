Standard-Netzwerkverhalten:
Docker Compose erstellt automatisch ein eigenes Bridge-Netzwerk, in dem sich alle Container über Servicenamen erreichen.

Benutzerdefiniertes Netzwerk:
Unter networks: definieren und im Service mit networks: referenzieren.

Netzwerkmodi:
bridge (Standard), host (Container nutzt Host-Netzwerk), none. Host-Modus ist gut für hohe Performance oder spezielle Netzwerkzugriffe.

Netzwerke bei Beenden:
docker-compose stop lässt Netzwerke bestehen, docker-compose down löscht standardmäßig erstellte Netzwerke.

Kommunikation zwischen Projekten:
Durch gemeinsame externe Netzwerke, die in beiden Projekten verwendet werden.

Aliase:
Alternative Namen für Container im Netzwerk, definiert unter networks.<netwerk>.aliases.

IP-Vergabe:
Standard: dynamisch. Statisch durch IPAM-Konfiguration und ipv4_address in benutzerdefinierten Netzwerken möglich.
