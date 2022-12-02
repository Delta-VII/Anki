# Verbindungsaufbau Normal Response Mode und nur Secondary sendet

Window Size w = 2
Wenn P/F signalisiert Ende der Übertragung und fordert eine unmittelbare Antwort.
Nach erreichen der Window Size wird das P Bit gesetzt. (oder am Ende einer Übertragung)

1. Primary sendet SNRM Befehl
2. Secondary antwortet mit UA Befehl
3. Primary sendet RR (0,P) --> Nr = 0 da nichts empfangen und Ns = 0  da keine I Blöcke gesendet.
4. Secondary sendet I Blöcke und beginnt bei Ns = 0 und Nr = 0

# Verbindungsaufbau Normal Response Mode und nur Primary sendet

Window Size w = 2
Wenn P/F signalisiert Ende der Übertragung und fordert eine unmittelbare Antwort.
Nach erreichen der Window Size wird das P Bit gesetzt. (oder am Ende einer Übertragung)

1. Primary sendet SNRM Befehl
2. Secondary antwortet mit UA Befehl
3. Primary sendet I Blöcke (bis zu Ns = w), dann PBit um Bestätigung einzuholen
4. Secondary sendet RR (2,F) (Ns = 0 und Nr = 2)
5. Primary sendet weiter mit I (Ns=2 und Nr= 0)

# Beide Seiten senden (Verbindung bereits aufgebaut)

Window Size w = 3
Wenn P/F signalisiert Ende der Übertragung und fordert eine unmittelbare Antwort.
Nach erreichen der Window Size wird das P Bit gesetzt. (oder am Ende einer Übertragung)

1. Primary sendet I Block (Ns = 0, Nr = 0)
2. Primary sendet I Block (Ns = 1, Nr = 0)
3. Primary sendet I Block (Ns = 2, Nr = 0) P/F Bit gesetzt.
4. Secondary sendet I Block (Ns= 0, Nr = 3) (Es wurden 3 Blöcke von Primary empfangen)
5. Secondary sendet I Block (Ns=1, Nr=3) 
6. Primary sendet I Block (Ns = 3, Nr = 2)
7. Primary sendet I Block (Ns = 4, Nr = 2) P/F Bit gesetzt
8. Secondary sendet I Block (Ns=2, Nr=5) P/F Bit gesetzt
9. Primary sendet I Block (Ns=5, Nr = 3)
10. ...

# Disconnect 

1. Primary sendet DISC mit P Bit
2. Secondary sendet UA

oder

1. Secondary sendet DM
2. Primary sendet SNRM
3. Secondary sendet UA
