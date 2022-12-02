# Fehler

## Startup Error


1. **Primary sendet SNRM Befehl** !!kommt nicht an!!
2. Timeout 
3. Primary sendete SNRM Befehl erneut !!retransmission!!
4. Secondary sendet UA
5. Primary sendet I Block ...
6. ...

## Startup Response Error

1. Primary sendet SNRM Befehl
2. **Secondary sendet UA** !!kommt nicht an!!
3. Timeout 
4. Primary sendete SNRM Befehl erneut
5. Secondary sendet UA !!retransmission!!
5. Primary sendet I Block ...
6. ...


## Primary poll frame Error (Verbindung besteht bereits)

1. Primary sendet I Block (Ns = 0, Nr = 0)
2. Primary sendet I Block (Ns = 1, Nr = 0)
3. **Primary sendet I Block (Ns = 2, Nr = 0) PBit gesetzt**
4. Timeout
5. Primary sendet RR Nr = 0 (hat ja noch keine Pakete von Secondary empfangen) PBit gesetzt
6. Secondary sendet I Frame(Ns = 0, Nr = 2)
7. Secondary senet I Frame(Ns = 1 , Nr = 2)
8. Primary sendet I Block erneut (Ns = 2, Nr = 2) !!retransmission!!
9. ...

## Primary Information error

1. Primary sendet I Block (Ns = 0, Nr = 0)
2. **Primary sendet I Block (Ns = 1, Nr = 0)** !!kommt nicht an!!
3. Primary sendet I Block (Ns = 2, Nr = 0) PBit gesetzt
4. Secondary sendet I Block (Ns = 0, Nr = 1) !!Der 3. I BLock der Primary wird verworfen, da der 2. auch fehlt!!
5. Secondary sendet I Block ( Ns = 1, Nr = 1) P/F BIt gesetzt. 
6. Primary sendet I BLock (Ns = 2, Nr = 2) !!retransmission!!
7. ...


## Fehler beim I Block übertragen

1. Primary sendet I Block (Ns = 0, Nr = 0)
2. Primary sendet I Block (Ns = 1, Nr = 0)

3. Primary sendet I Block (Ns = 2, Nr = 0) P Bit
4. **Secondary sendet I Block (Ns = 0, Nr  = 3)** !!kommt nicht an!!
5. Secondaray sendet I Block (Ns = 1, Nr = 3)

6. Nun gibt es 2 Möglichkeiten
    6. a) Primary sendet RR0 mit Pbit
    7. a) Secondary sendet I Blöcke erneut
    6. b) Primary sendet normale I Blöcke erhöhrt aber Nr nicht --> Nr = 0. Nach Window werden die Blöcke erneut angefordert.
    7. b) secondary sendet I Blöcke erneut





 