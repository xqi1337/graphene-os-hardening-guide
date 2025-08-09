---
title: 'GrapheneOS Hardening-Guide'
description: 'Umfassende Anleitung zur sicheren Einrichtung von GrapheneOS auf Pixel-Geräten'
tags: ['IT', 'Sicherheit', 'GrapheneOS', 'Mobiles', 'Privacy']
---

## GrapheneOS

Da es in diesem Bereich immer noch viele falsche Informationen gibt, wie Anohandys am besten einzurichten sind, werde ich hier eine kleine Anleitung raushauen, wie es am besten gemacht wird.

Da **Fraud** auch in DE immer heißer wird, und sich viele durch ihre **Anohandys** busten lassen, sichert euch lieber dreifach ab.

In meinen Augen eignet sich am besten als Anohandy ein **Google Pixel**. Ich nutze das 7 Pro, aber das 6A tut es auch. **iPhones** bitte nur das Neuste und kein **FaceID**, **16 Zeichen Passwort** und **iCloud Backup deaktivieren**. Aber mit iPhones habe ich persönlich zu wenig Erfahrung gemacht, um dazu etwas sagen zu können.

---

## Was benötigen wir?

- **Passendes Pixel**, das von **GrapheneOS** unterstützt wird. Die Liste dafür findet ihr hier: *Liste der Geräte*. Ich empfehle die Pixels unter dem 6er, aber nicht mehr.

- **Windows Laptop**

- **USB-C Kabel**

- **Internet**

- **APKs**, die verlinkt sind.

**Optional, aber macht das Gerät sicherer:**

- **E-SIM**

---

## Wie kaufe ich das Gerät?

Am besten über **KAZA**, ein gebrauchtes. Bitte niemals eine **SIM** in das Gerät stecken, die über euch läuft. Ansonsten im Laden geht natürlich auch.

---

## Was sind die Vorteile von **GrapheneOS**?

- **Keine Google Dienste** und die dazugehörigen **Backdoors**

- **Mehr 0Day Patches**

- **Verstärkter Bootloader**

- **Auto Reboot**

- **Bessere E-SIM Funktionalität**

Und vieles mehr. Einfach hier einlesen: **Features von GrapheneOS**

---

## Wie installiere ich **GrapheneOS**?

### Vorbereitungen:

a. Lade die nötigen Tools für deinen Computer herunter:  
```bash
https://developer.android.com/studio/releases/platform-tools
```

b. Schalte die **Entwickleroptionen** auf deinem Handy ein:

- Öffne die **Einstellungen**-App  
- Tippe auf **„Über das Telefon“**  
- Finde die **„Build-Nummer“** und tippe **7-mal** drauf, um die Entwickleroptionen freizuschalten  
- Gehe zurück zu den **Einstellungen** und wähle **„Entwickleroptionen“**  
- Aktiviere **„USB-Debugging“** und **„OEM-Entsperrung“**

---

### GrapheneOS Webinstaller:  
**DIESER FUNKTIONIERT NUR MIT CHROME oder CHROMIUM-BASIERTEN BROWSERN!**

1. **Bootloader entsperren:**  
Klicke auf **„Unlock Bootloader“**, wähle dein Pixel aus.  

Das Gerät wird neustarten und sich komplett resetten. Mit den Lautstärketasten die Bestätigung auswählen.

2. **ROM herunterladen:**  
Klicke auf **„Download Release“**.  
Warte, bis der blaue Balken vollständig geladen ist.

3. **Flashen:**  
Klicke auf **„Flash Release“**. Das Gerät rebootet automatisch mehrmals.  
Bitte währenddessen nichts am Phone machen, einfach liegen lassen.  
Danach **nicht einrichten!**

4. **Bootloader sperren:**  
Auf **„Lock Bootloader“** klicken. Das ist extrem wichtig!  
Das Gerät ist sonst genauso unsicher wie ein **Schweizer Käse** mit offenem Bootloader.

---

## Einrichtung nach der Installation

Richte dein **Phone** so ein, wie du es normalerweise machen würdest.  

Verwende **KEINEN Fingerabdruck**!  
Ein **Passwort** von mindestens **16 Zeichen** sollte genutzt werden – die gleiche Sicherheit wie bei der **HDD-Verschlüsselung**.

---

## Aktiviert folgende Optionen:

### Entwicklereinstellungen:

- **Sensoren deaktivieren:**  
*Entwickleroptionen aktivieren + Sensoren deaktivieren*  
*Schaltet Kamera, Mikrofone, Bewegungssensoren uvm. aus* **WICHTIG!!**

- **Wi-Fi automatisch ausschalten:**  
*Netzwerk & Internet → WLAN → Netzwerkpräferenzen → WLAN automatisch ausschalten (2. Option)*  
*Empfohlen: 1-3 Stunden*

- **Bluetooth Timeout:**  
*Verbundene Geräte → Bluetooth Timeout*  
*Empfohlen: 15 Sekunden*

- **Auto Reboot:**  
*Sicherheit → Auto Reboot*  
*Empfohlen: 30 Minuten*  
**EXTREM WICHTIG!**  
*Verhindert, dass im Unlock-Mode die Entschlüsselungs-Keys aus dem RAM ausgelesen werden.*

- **Native Code Debugging:**  
*Sicherheit → Native Code Debugging*  
*Alle Logs ausschalten*

---

## Installiere folgende Apps auf deinem Hauptprofil:

- **F-Droid Store** (Download)  
- **Aurora Store** (bei F-Droid) – sichere & anonyme Alternative zum Google Play Store  
- **Sentry** (bei F-Droid) – nach Installation Geräte-Owner-Permission geben (`„TURN ON“`)  
- **Wasted** (bei F-Droid) – starten, aktivieren, Rechte erlauben, **Wipe Data** & **Wipe eSIM** aktivieren, Tile entfernen, neues Tile aktivieren.  
- **LockUp** (APK hier) – installieren, aktivieren, erkennt UFED-Attacken (z.B. Cellebrite), resettet das Gerät automatisch.

> **Hinweis:**  
Google-Dienste sollten nur in einem **gesonderten Profil** installiert werden. Dank GrapheneOS könnt ihr beliebig viele Profile anlegen, die extra verstärkt sind.

---

## Verhalten mit einem Anohandy

- Es wird geloggt, **über welche IMEI** sich die SIM ins Netz einwählt.  
**KEINE RL-regged SIMs** im Handy verwenden!!

- Bei ländlicher Umgebung: **Nicht Zuhause nutzen**.  
In Neuköllner Plattenbauten ist das egal.

- Gerät **nicht eingeschaltet** mitführen, besonders wenn ihr ein **RL-Handy** dabei habt.  
**IMMER ausschalten!**  
Andernfalls kann mithilfe der Funkmasten ein **Bewegungsprofil** erstellt werden.

- Nicht über Nacht eingeschaltet lassen.  
Glaubt mir, wenn euch das SEK die Türe eintreten lässt, ist es zu spät.

- **E-SIMs verwenden!**  
Können nicht entfernt werden, und ihr könnt mit **Wasted** aus der Ferne resetten.

- **E-SIMs regelmäßig changen**

- **Nicht rooten!**

- Trotz **anosim VPN** verwenden (z.B. Mullvad, Perfect Privacy).

- Apps nur die notwendigsten Rechte geben, Netzwerkrechte entziehen, wenn nicht genutzt.

---

## **Sicherheits-Tools & Maßnahmen**

### Fail2Ban mit Termux:

```bash
pkg install fail2ban openssh
echo -e "[sshd]\nenabled=true
port=8022
logpath=/data/data/com.termux/files/usr/var/log/sshd.log
findtime=600
maxretry=4
bantime=28800" > $PREFIX/etc/fail2ban/jail.local
sv-enable fail2ban
```

### iptables Rate-Limiter:

```bash
iptables -A INPUT -p tcp --dport 5555 -m state --state NEW -m recent --set
iptables -A INPUT -p tcp --dport 5555 -m state --state NEW -m recent \
        --update --seconds 60 --hitcount 4 -j DROP
```

### Device Brute-Force Schutz (DeviceOwner erforderlich):

```kotlin
class BruteForceGuard : DeviceAdminReceiver() {
    override fun onEnabled(context: Context, intent: Intent) {
        val dpm = context.getSystemService(DevicePolicyManager::class.java)
        dpm.setMaximumFailedPasswordsForWipe(componentName, 10)
    }
}
```

### ADB-over-Wi-Fi temporär (rootfrei):

```bash
#!/data/data/com.termux/files/usr/bin/bash
# save as adb-temp.sh && chmod +x adb-temp.sh
timeout=${1:-300}  # Standard: 5 Minuten

adb tcpip 5555
echo "[*] ADB-Wi-Fi läuft $timeout s ..."
sleep "$timeout"
adb kill-server
echo "[*] ADB-Wi-Fi deaktiviert."
```

### Geo-Fence: Biometrie zu Hause an, unterwegs aus (Tasker + Termux):

```bash
# Toggle-Funktion:
cmd=$1  # "enable" | "disable"
if [ "$cmd" = "disable" ]; then
  settings put secure lock_screen_lock_after_timeout 0
  locksettings set-disabled true
else
  settings put secure lock_screen_lock_after_timeout 5000
  locksettings set-disabled false
fi
```

---

## Quellen & Weiterführende Links

- [Android 11 DP2 Wireless ADB Debugging](https://9to5google.com/2020/03/18/android-11-dp2-wireless-adb-debugging/)
- [Android Sicherheit Bulletins](https://source.android.com/docs/security/bulletin/android-15?hl=de)

---
