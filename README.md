# esp32_cyd_mqtt-telegram
Esp32 CYD Board MQTT/Telegram
# ESP32 MQTT Monitor mit Telegram-Integration

## Beschreibung

Dieses Projekt verbindet einen ESP32-Mikrocontroller mit einem TFT-Display, um Nachrichten von verschiedenen Quellen anzuzeigen:

1. MQTT-Nachrichten von zwei konfigurierbaren Topics
2. Telegram-Nachrichten über einen Telegram-Bot

Das Display zeigt die drei Nachrichtenkanäle gleichzeitig an und aktualisiert sie in Echtzeit. Die Statusleiste am unteren Bildschirmrand zeigt den aktuellen Verbindungsstatus für WLAN, MQTT und Telegram.

## Funktionen

- **MQTT-Integration**: Abonniert zwei konfigurierbare MQTT-Topics
- **Telegram-Bot-Integration**: Ermöglicht das Senden von Nachrichten über einen Telegram-Bot
- **Übersichtliches Display-Layout**: Zeigt alle drei Nachrichtenquellen gleichzeitig an
- **Statusanzeige**: WLAN-, MQTT- und Telegram-Verbindungsstatus
- **Benutzerautentifizierung**: Nur autorisierte Telegram-Benutzer können Nachrichten senden
- **Animierte Benutzeroberfläche**: Ansprechende Animationen beim Start und bei Statusänderungen

## Telegram-Befehle

Der Telegram-Bot unterstützt folgende Befehle:
- `/status` - Zeigt den aktuellen Systemstatus an
- `/hilfe` oder `/help` - Zeigt eine Liste der verfügbaren Befehle
- `/nachricht <text>` - Sendet einen Text an das Display

## Technische Details

- **Hardware**: ESP32 mit TFT-Display (TFT_eSPI-Bibliothek)
- **Netzwerk**: WLAN-Verbindung und MQTT-Client
- **Zeit**: NTP-Synchronisation für genaue Zeitstempel
- **Bibliotheken**: WiFi, PubSubClient, TFT_eSPI, UniversalTelegramBot, ArduinoJson
- **Speicher**: Feste Nachrichtenslots für optimale Anzeige und Organisation

## Installation

1. Installiere die erforderlichen Bibliotheken in der Arduino IDE
2. Konfiguriere deine WLAN-, MQTT- und Telegram-Bot-Einstellungen im Code
3. Trage deine Telegram-Chat-ID bei `ALLOWED_USERS` ein
4. Kompiliere und lade den Code auf deinen ESP32

## Anpassungen

Der Code kann einfach angepasst werden, um:
- Die Anzahl und Namen der MQTT-Topics zu ändern
- Das Display-Layout anzupassen
- Weitere Telegram-Befehle hinzuzufügen
- Die Farbgebung zu personalisieren

## Integration mit Node-RED

Das Projekt lässt sich leicht mit Node-RED integrieren, um:
- MQTT-Nachrichten an die konfigurierten Topics zu senden
- Telegram-Nachrichten über die Telegram-API zu versenden
