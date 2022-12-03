# WEP – Wired Equivalent Privacy

## WEP

Wired Equivalent Privacy

## WEP Eigenschaften

- Symmetrisch mit 40 oder 104 Bit Schlüssel, RC4
- Schlüssel ergänzt um einmaligen Initialisierungsvektor (24 Bit)
- Pseudozufälliger Keystream => Xor Data
- Integrität: CRC
- Authentizität: Keine oder Challenge-Response mit PSK (Pre-Shared Key)

## WEP Angriffe

- Replay, Initialization Vector (IV) zu kurz, Schlüssel berechnbar (SNAP 0xAAAA03)
- Brute Force
