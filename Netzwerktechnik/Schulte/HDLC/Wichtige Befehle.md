# Wichtige Befehle

## SNRM
Set Normal Response Mode

Setzt die Secondary Station in NRM für Information Trans-
fer (Poll Bit an), Zähler werden auf 0 gesetzt.

Die Antwort ist UA.

## SABM
Set Asynchronous Balanced Mode

Mit SABM leitet eine Station den Aufbau einer gesicherten
Verbindung ein.
Die Antwort ist UA.
## DISC

Disconnect

Mit DISC beendet eine Station eine bestehende Verbindung.
Die Antwort ist UA oder DM (Disconnect Mode).

Die DM-Antwort ist zu verwenden, um einen Status zu mel-
den, bei dem die Sekundär-/Kombistation logisch von der

Datenverbindung getrennt ist und per Systemdefinition im
NDM oder ADM ist.

## UA
Unnumbered Ack
Bestätigung auf SNRM, SABM und DISC
## UI
Unnumbered Information
Zur Übertragung von Informationen ohne Sequenz-Nummer
## RNR
Receive Not Ready
Mit RNR kann eine Station der anderen anzeigen, dass sie

zurzeit keine Datenblöcke annehmen kann. Mit dem Emp-
fangsfolgenummernzähler (N(R)) können die bis zu diesem

Zeitpunkt richtig empfangenen Blöcke quittiert werden.
## RR 

Receive Ready
Mit RR zeigt eine Station ihre Bereitschaft an, weitere I-
Blöcke zu empfangen. Die RR-Meldung wird auch zur Quit-
tierung richtig empfangener I-Blöcke verwendet, wenn die

quittierende Station selbst keine I-Blöcke zu senden hat.
## REJ
Reject
Mit REJ kann eine Station von ihrer Partnerstation die Wie-
derholung von I-Blöcken ab der im N(R) enthaltenen Block-
nummer anfordern. REJ wird gesendet, wenn ein Block mit

falscher Folgenummer empfangen wird.
