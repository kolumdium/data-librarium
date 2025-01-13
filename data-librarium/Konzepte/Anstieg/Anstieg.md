# Anstieg

Damit der Roboter Routen effizient und sicher planen kann, müssen genaue Daten über den Anstieg der Fahrbahn erfasst werden. Der **Neigungswinkel** beeinflusst maßgeblich, welche Strecken der Roboter bewältigen kann, ohne dabei seine **Motorleistung** zu überschreiten.

Zudem spielen die **Traglast** und der **Schwerpunkt** eine wichtige Rolle. Auf geneigten Strecken verschiebt sich das Gleichgewicht des Roboters, wodurch das Risiko eines **Umkippens** steigt, insbesondere bei Lastentransporten. Durch präzise Anstiegsdaten kann der Roboter vorab bewerten, ob eine geplante Route stabil und sicher bleibt oder alternative Wege gewählt werden müssen.

Darüber hinaus beeinflussen diese Daten den **Energieverbrauch**. Steigungen erfordern mehr Leistung und verkürzen die Batterielaufzeit. Eine genaue Einschätzung des Anstiegs ermöglicht dem Roboter, den Energiebedarf der geplanten Route besser zu kalkulieren und den Betrieb effizienter zu gestalten.

## Szenarien

1.  Lieferroboter
	1. Differenzieller Antrieb
	2. ca. 80 x 60 cm 
	3. Sensoren
		1. Lidar
			1. vorn
			2. hinten
		2. Stereokameras
			1. Front
			2. Seite
			3. Hinten
		3. GPS
		4. IMU
		5. Odometry
2.  Lastenrad
	1. Ackerman Steuerung
	2. ca. 2,5 x 1,0 m
	3. Sensoren
		1. Kameras vorne
		2. Lidar 

## Steckbrief
### [[Szenario-abhängige Parameter]]

| Anforderungen                                                          | [[Szenario 1]]                                                     | [[Szenario 2]]                                 |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------ | ---------------------------------------------- |
| [[Temporale Aufloesung]]                                               | Bei Begin der Planung                                              | Bei Begin der Planung                          |
| [[Kritikalitaet der TA]]                                                | gering[^1]                                                         | gering[^1]                                     |
| [[Lokale Aufloesung]]                                                   | max. Wert zwischen Hauseingängen                                   | $m^2$                                          |
| [[Kritikalitaet der LA]]                                                | hoch                                                               | hoch                                           |
| [[Datenquellen]]                                                       | [[Berechnung#GPS\|GPS]], IMU, Lidar + IMU, Community, [[Kataster]] | GPS, IMU, Lidar + IMU, Community, Kataster     |
| [[Generierende Sensoren]]                                              |                                                                    |                                                |
| [[Generierende Verarbeitungen]]                                        | [[Berechnung]]                                                     | Berechnung                                     |
| [[Weiterfuehrende Verarbeitung fuer]]                                    | Energieaufwand, Geschwindigkeit, Routenplanung                     | Energieaufwand, Geschwindigkeit, Routenplanung |
| [[Relevanz der Vollstaendigkeit]]                                       | Fehlen könnte zur Neuplanung führen                                | Fehlen könnte zur Neuplanung führen            |
| [[Relevanz der Richtigkeit]]                                           | Falsche Angaben könnten zur Neuplanung führen                      | Falsche Angaben könnten zur Neuplanung führen  |
| [[Operationale Wichtigkeit]] (ist das nicht die Summe der Relevanzen?) |                                                                    |                                                |
| Zeitverlust durch Fehlerhafte Angaben                                  | gering                                                             | gering                                         |
| Zeitverlust durch Schätzen                                             | gering                                                             | gering                                         |
|                                                                        |                                                                    |                                                |
[^1]: Anstieg ändert sich nur selten

### Richtgrößen
float 32 


## Detaillierte Antworten