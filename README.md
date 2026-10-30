# Zurich: law history in git

The law of the canton of Zurich (Kanton Zürich, Switzerland) as a git history: one file per article, one commit per amending act on the day it took effect, and the amending act as the commit's author. `git blame` names the act behind every paragraph; `git log` lists every change to an article; checking out a date gives the text in force that day.

It follows the shared design of [lexifina/global-law](https://github.com/lexifina/global-law), which places it at `ch-zh/`. The federal law is in [lexifina/switzerland-law](https://github.com/lexifina/switzerland-law).

The text is in German, the canton's official language, exactly as the canton publishes it.

## What this repository holds

589 acts with 1743 versions so far: the cantonal constitution, then the cantonal laws (Gesetze) in force and the ordinances (Verordnungen and Reglemente) in force, in the order of the Zürcher Loseblattsammlung (LS), added in parts. Decrees, intercantonal agreements and repealed acts are not included yet. Laws whose PDF layout the parser does not yet read letter for letter are left out until it does: LS 170.1, LS 171.1, LS 415.11, LS 554.5, LS 724.1, LS 730.1, LS 851.1.

| Folder | Act | Versions | History |
| --- | --- | ---: | --- |
| `ls-101/` | Verfassung des Kantons Zürich (LS 101) | 8 | as enacted, then each Nachtrag: 1 January 2006 to 1 July 2024 |
| `ls-131-1/` | Gemeindegesetz (GG) (LS 131.1) | 6 | as enacted, then each Nachtrag: 1 January 2018 to 1 April 2026 |
| `ls-132-1/` | Finanzausgleichsgesetz (FAG) (LS 132.1) | 1 | as enacted1 January 2012 |
| `ls-132-2/` | Staatsbeitragsgesetz (LS 132.2) | 7 | oldest version available, then each Nachtrag: 1 January 2006 to 1 January 2021 |
| `ls-141-1/` | Kantonales Bürgerrechtsgesetz (KBüG) (LS 141.1) | 1 | as enacted1 July 2023 |
| `ls-142-1/` | Gesetz über das Meldewesen und die Einwohnerregister (MERG) (LS 142.1) | 2 | as enacted, then each Nachtrag: 1 January 2016 to 1 April 2018 |
| `ls-161/` | Gesetz über die politischen Rechte (GPR) (LS 161) | 17 | as enacted, then each Nachtrag: 1 January 2005 to 1 July 2026 |
| `ls-170-4/` | Gesetz über die Information und den Datenschutz (IDG) (LS 170.4) | 11 | oldest version available, then each Nachtrag: 1 June 2007 to 1 May 2024 |
| `ls-170-5/` | Publikationsgesetz (PublG) (LS 170.5) | 2 | as enacted, then each Nachtrag: 1 January 2018 to 1 May 2020 |
| `ls-170-6/` | Archivgesetz (LS 170.6) | 1 | one version (the oldest available)15 January 2014 |
| `ls-172-1/` | Gesetz über die Organisation des Regierungsrates und der kantonalen Verwaltung (OG RR) (LS 172.1) | 7 | as enacted, then each Nachtrag: 1 September 2007 to 1 January 2022 |
| `ls-172-71/` | Gesetz über die Auslagerung von Informatikdienstleistungen (LS 172.71) | 1 | one version (the oldest available)1 October 2008 |
| `ls-173-1/` | Bezirksverwaltungsgesetz (BezVG) (LS 173.1) | 9 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2023 |
| `ls-175-2/` | Verwaltungsrechtspflegegesetz (VRG) (LS 175.2) | 17 | oldest version available, then each Nachtrag: 1 July 2010 to 1 July 2026 |
| `ls-177-10/` | Personalgesetz (PG) (LS 177.10) | 9 | oldest version available, then each Nachtrag: 1 May 2007 to 1 August 2024 |
| `ls-177-12/` | Gesetz über das Schlichtungsverfahren für Streitigkeiten nach Gleichstellungsgesetz in öffentlich-rechtlichen Arbeitsverhältnissen (LS 177.12) | 1 | as enacted1 January 2011 |
| `ls-177-201-1/` | Gesetz über die Verselbstständigung der Versicherungskasse für das Staatspersonal (LS 177.201.1) | 2 | as enacted, then each Nachtrag: 1 May 2007 to 1 December 2009 |
| `ls-180-1/` | Kirchengesetz (KiG) (LS 180.1) | 3 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2021 |
| `ls-184-1/` | Gesetz über die anerkannten jüdischen Gemeinden (GjG) (LS 184.1) | 2 | as enacted, then each Nachtrag: 1 January 2008 to 1 January 2021 |
| `ls-211-1/` | Gesetz über die Gerichts- und Behördenorganisation im Zivil- und Strafprozess (GOG) (LS 211.1) | 18 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2026 |
| `ls-212-81/` | Gesetz über das Sozialversicherungsgericht (GSVGer) (LS 212.81) | 9 | oldest version available, then each Nachtrag: 1 January 2005 to 1 July 2025 |
| `ls-215-1/` | Anwaltsgesetz (LS 215.1) | 4 | as enacted, then each Nachtrag: 1 January 2005 to 1 January 2011 |
| `ls-230/` | Einführungsgesetz zum Schweizerischen Zivilgesetzbuch (EG ZGB) (LS 230) | 22 | oldest version available, then each Nachtrag: 1 May 2006 to 1 June 2026 |
| `ls-232-3/` | Einführungsgesetz zum Kindes- und Erwachsenenschutzrecht (EG KESR) (LS 232.3) | 7 | oldest version available, then each Nachtrag: 19 October 2012 to 1 January 2022 |
| `ls-234-1/` | Einführungsgesetz zum Bundesgesetz über den Erwerb von Grundstücken durch Personen im Ausland (EG BewG) (LS 234.1) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2011 |
| `ls-242/` | Notariatsgesetz (NotG) (LS 242) | 5 | oldest version available, then each Nachtrag: 1 January 2008 to 1 January 2017 |
| `ls-281/` | Einführungsgesetz zum Bundesgesetz über Schuldbetreibung und Konkurs (EG SchKG) (LS 281) | 9 | oldest version available, then each Nachtrag: 1 January 2015 to 1 September 2026 |
| `ls-312/` | Gesetz betreffend die Ordnungsstrafen (LS 312) | 1 | as enacted30 October 1866 |
| `ls-331/` | Straf- und Justizvollzugsgesetz (StJVG) (LS 331) | 8 | as enacted, then each Nachtrag: 1 January 2007 to 1 June 2020 |
| `ls-341/` | Einführungsgesetz zum Opferhilfegesetz (EG OHG) (LS 341) | 4 | oldest version available, then each Nachtrag: 1 January 2008 to 1 April 2024 |
| `ls-351/` | Gewaltschutzgesetz (GSG) (LS 351) | 7 | as enacted, then each Nachtrag: 1 April 2007 to 1 January 2025 |
| `ls-410-1/` | Bildungsgesetz (BiG) (LS 410.1) | 5 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2021 |
| `ls-410-6/` | Musikschulgesetz (MuSG) (LS 410.6) | 1 | as enacted1 January 2023 |
| `ls-410-9/` | Gesetz über den Lehrmittelverlag (LMVG) (LS 410.9) | 1 | one version (the oldest available)23 February 2018 |
| `ls-412-31/` | Lehrpersonalgesetz (LPG) (LS 412.31) | 15 | oldest version available, then each Nachtrag: 21 August 2006 to 1 October 2022 |
| `ls-412-41/` | Gesetz über das Zentrum für Gehör und Sprache (LS 412.41) | 3 | as enacted, then each Nachtrag: 1 January 2009 to 1 January 2018 |
| `ls-412-100/` | Volksschulgesetz (VSG) (LS 412.100) | 11 | oldest version available, then each Nachtrag: 1 January 2014 to 1 August 2024 |
| `ls-413-21/` | Mittelschulgesetz (MSG) (LS 413.21) | 10 | oldest version available, then each Nachtrag: 1 March 2011 to 1 April 2026 |
| `ls-413-31/` | Einführungsgesetz zum Berufsbildungsgesetz (EG BBG) (LS 413.31) | 8 | as enacted, then each Nachtrag: 1 January 2011 to 1 April 2026 |
| `ls-414-10/` | Fachhochschulgesetz (FaHG) (LS 414.10) | 6 | oldest version available, then each Nachtrag: 1 July 2010 to 1 August 2024 |
| `ls-414-41/` | Gesetz über die Pädagogische Hochschule (PHG) (LS 414.41) | 9 | oldest version available, then each Nachtrag: 21 August 2006 to 1 August 2024 |
| `ls-431-1/` | Statistikgesetz (StatG) (LS 431.1) | 1 | as enacted1 January 2016 |
| `ls-440-1/` | Kulturförderungsgesetz (KFG) (LS 440.1) | 1 | one version (the oldest available)1 January 2012 |
| `ls-440-2/` | Opernhausgesetz (OpHG) (LS 440.2) | 2 | as enacted, then each Nachtrag: 1 January 2012 to 1 July 2016 |
| `ls-520/` | Bevölkerungsschutzgesetz (BSG) (LS 520) | 2 | as enacted, then each Nachtrag: 1 July 2008 to 1 January 2022 |
| `ls-522/` | Zivilschutzgesetz (ZSG) (LS 522) | 4 | as enacted, then each Nachtrag: 1 August 2007 to 1 January 2018 |
| `ls-550-1/` | Polizeigesetz (PolG) (LS 550.1) | 14 | as enacted, then each Nachtrag: 1 July 2009 to 1 January 2026 |
| `ls-551-1/` | Polizeiorganisationsgesetz (POG) (LS 551.1) | 10 | as enacted, then each Nachtrag: 1 January 2006 to 1 August 2022 |
| `ls-551-4/` | Gesetz für ein Polizei- und Justizzentrum Zürich (LS 551.4) | 2 | as enacted, then each Nachtrag: 1 April 2004 to 1 April 2019 |
| `ls-553/` | Einführungsgesetz zum Bundesgesetz über Geldspiele (EG BGS) (LS 553) | 1 | as enacted1 January 2022 |
| `ls-554-1/` | Kantonales Tierschutzgesetz (LS 554.1) | 4 | oldest version available, then each Nachtrag: 1 January 2007 to 1 June 2018 |
| `ls-611/` | Gesetz über Controlling und Rechnungslegung (CRG) (LS 611) | 12 | as enacted, then each Nachtrag: 1 April 2008 to 1 July 2022 |
| `ls-612/` | Lotteriefondsgesetz (LFG) (LS 612) | 1 | as enacted1 January 2021 |
| `ls-614/` | Finanzkontrollgesetz (FKG) (LS 614) | 8 | oldest version available, then each Nachtrag: 1 April 2008 to 1 May 2024 |
| `ls-631-1/` | Steuergesetz (StG) (LS 631.1) | 24 | oldest version available, then each Nachtrag: 1 January 2004 to 26 March 2026 |
| `ls-632-1/` | Erbschafts- und Schenkungssteuergesetz (ESchG) (LS 632.1) | 5 | oldest version available, then each Nachtrag: 1 January 2007 to 1 January 2011 |
| `ls-700-1/` | Planungs- und Baugesetz (PBG) (LS 700.1) | 14 | oldest version available, then each Nachtrag: 1 July 2014 to 1 August 2026 |
| `ls-700-9/` | Mehrwertausgleichsgesetz (MAG) (LS 700.9) | 2 | as enacted, then each Nachtrag: 1 January 2021 to 1 August 2026 |
| `ls-702-21/` | Natur- und Heimatschutzfondsgesetz (NHFG) (LS 702.21) | 2 | oldest version available, then each Nachtrag: 1 January 2005 to 1 October 2021 |
| `ls-704-1/` | Kantonales Geoinformationsgesetz (KGeoIG) (LS 704.1) | 3 | as enacted, then each Nachtrag: 1 November 2012 to 1 May 2022 |
| `ls-712-1/` | Abfallgesetz (AbfG) (LS 712.1) | 4 | oldest version available, then each Nachtrag: 1 April 2004 to 1 July 2014 |
| `ls-722-1/` | Strassengesetz (StrG) (LS 722.1) | 9 | oldest version available, then each Nachtrag: 1 January 2012 to 1 June 2026 |
| `ls-722-2/` | Einführungsgesetz zum Nationalstrassengesetz (EG NSG) (LS 722.2) | 4 | oldest version available, then each Nachtrag: 1 January 2008 to 1 January 2018 |
| `ls-725-1/` | Gesetz über die Nutzung des Untergrundes (GNU) (LS 725.1) | 1 | as enacted1 July 2023 |
| `ls-732-1/` | Gesetz betreffend die Elektrizitätswerke des Kantons Zürich (EKZ-Gesetz) (LS 732.1) | 5 | oldest version available, then each Nachtrag: 20 May 2007 to 1 February 2026 |
| `ls-740-1/` | Gesetz über den öffentlichen Personenverkehr (PVG) (LS 740.1) | 3 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2026 |
| `ls-741-1/` | Verkehrsabgabengesetz (VAG) (LS 741.1) | 5 | oldest version available, then each Nachtrag: 1 January 2007 to 1 January 2019 |
| `ls-747-1/` | Einführungsgesetz zum Bundesgesetz über die Binnenschiffahrt (LS 747.1) | 1 | one version (the oldest available)1 July 2003 |
| `ls-747-12/` | Gesetz über die Besteuerung der Schiffe (Schiffssteuergesetz) (LS 747.12) | 2 | oldest version available, then each Nachtrag: 1 July 2003 to 1 January 2007 |
| `ls-748-1/` | Gesetz über den Flughafen Zürich (Flughafengesetz) (LS 748.1) | 3 | oldest version available, then each Nachtrag: 1 May 2007 to 1 March 2018 |
| `ls-748-3/` | Flughafenfondsgesetz (LS 748.3) | 1 | one version (the oldest available)1 July 2010 |
| `ls-781/` | Gesetz betreffend die Abtretung von Privatrechten (LS 781) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-810-1/` | Gesundheitsgesetz (GesG) (LS 810.1) | 13 | as enacted, then each Nachtrag: 1 July 2008 to 1 January 2026 |
| `ls-810-4/` | Gesetz über die Verselbstständigung der Kantonsapotheke Zürich (VKG) (LS 810.4) | 1 | as enacted1 May 2023 |
| `ls-811-4/` | Einführungsgesetz zum Bundesgesetz über die Förderung der Ausbildung im Bereich der Pflege (EG Ausbildungsfördergesetz Pflege) (LS 811.4) | 1 | one version (the oldest available)21 February 2025 |
| `ls-813-13/` | Patientinnen- und Patientengesetz (LS 813.13) | 6 | as enacted, then each Nachtrag: 1 January 2005 to 15 January 2014 |
| `ls-813-15/` | Gesetz über das Universitätsspital Zürich (USZG) (LS 813.15) | 7 | as enacted, then each Nachtrag: 1 January 2007 to 1 January 2024 |
| `ls-813-16/` | Gesetz über das Kantonsspital Winterthur (KSWG) (LS 813.16) | 7 | as enacted, then each Nachtrag: 1 January 2007 to 1 January 2023 |
| `ls-813-17/` | Gesetz über die Psychiatrische Universitätsklinik Zürich (PUKG) (LS 813.17) | 2 | as enacted, then each Nachtrag: 1 January 2018 to 1 January 2023 |
| `ls-813-18/` | Gesetz über die Integrierte Psychiatrie Winterthur &#8211; Zürcher Unterland (ipwG) (LS 813.18) | 2 | oldest version available, then each Nachtrag: 25 January 2019 to 1 January 2023 |
| `ls-813-20/` | Spitalplanungs- und -finanzierungsgesetz (SPFG) (LS 813.20) | 6 | as enacted, then each Nachtrag: 1 January 2012 to 1 January 2023 |
| `ls-818-16/` | Gesetz über die finanzielle Unterstützung der privaten institutionellen familienergänzenden Kinderbetreuung aufgrund der Coronapandemie (GUpfK) (LS 818.16) | 1 | as enacted1 March 2022 |
| `ls-818-17/` | Gesetz über die finanzielle Unterstützung der öffentlich-rechtlichen institutionellen familienergänzenden Kinderbetreuung aufgrund der Coronapandemie (GUöfK) (LS 818.17) | 1 | one version (the oldest available)25 March 2022 |
| `ls-818-41/` | Krebsregistergesetz (KreReG) (LS 818.41) | 1 | as enacted1 January 2017 |
| `ls-821-5/` | Gesetz über das kantonale Einigungsamt (LS 821.5) | 1 | one version (the oldest available)1 January 2011 |
| `ls-822-4/` | Ruhetags- und Ladenöffnungsgesetz (LS 822.4) | 1 | as enacted1 May 2004 |
| `ls-831-1/` | Einführungsgesetz zu den Bundesgesetzen über die Alters- und Hinterlassenenversicherung und die Invalidenversicherung (EG AHVG/IVG) (LS 831.1) | 2 | oldest version available, then each Nachtrag: 1 January 2008 to 1 January 2018 |
| `ls-831-3/` | Zusatzleistungsgesetz (ZLG) (LS 831.3) | 13 | oldest version available, then each Nachtrag: 1 January 2004 to 1 June 2026 |
| `ls-831-5/` | Gesetz über den selbstbestimmten Leistungsbezug durch Menschen mit Behinderung (Selbstbestimmungsgesetz, SLBG) (LS 831.5) | 1 | as enacted1 January 2024 |
| `ls-832-01/` | Einführungsgesetz zum Krankenversicherungsgesetz (EG KVG) (LS 832.01) | 3 | as enacted, then each Nachtrag: 1 April 2020 to 1 October 2023 |
| `ls-833-1/` | Gesetz über die BVG- und Stiftungsaufsicht (BSAG) (LS 833.1) | 1 | one version (the oldest available)1 October 2025 |
| `ls-836-1/` | Einführungsgesetz zum Bundesgesetz über die Familienzulagen (EG FamZG) (LS 836.1) | 4 | as enacted, then each Nachtrag: 1 July 2009 to 1 January 2025 |
| `ls-837-1/` | Einführungsgesetz zum Arbeitslosenversicherungsgesetz (EG AVIG) (LS 837.1) | 3 | oldest version available, then each Nachtrag: 1 June 2005 to 1 July 2013 |
| `ls-841/` | Gesetz über die Wohnbau- und Wohneigentumsförderung (WBFG) (LS 841) | 3 | as enacted, then each Nachtrag: 1 July 2005 to 1 June 2026 |
| `ls-852-1/` | Kinder- und Jugendhilfegesetz (KJHG) (LS 852.1) | 5 | as enacted, then each Nachtrag: 1 January 2012 to 1 August 2020 |
| `ls-852-2/` | Kinder- und Jugendheimgesetz (KJG) (LS 852.2) | 2 | as enacted, then each Nachtrag: 1 January 2022 to 1 January 2025 |
| `ls-855-1/` | Pflegegesetz (LS 855.1) | 3 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2024 |
| `ls-855-2/` | Gesetz über den Transport von mobilitätsbehinderten Personen (TMG) (LS 855.2) | 4 | as enacted, then each Nachtrag: 1 January 2008 to 1 January 2024 |
| `ls-861-1/` | Gesetz über die Feuerpolizei und das Feuerwehrwesen (FFG) (LS 861.1) | 5 | oldest version available, then each Nachtrag: 24 September 1978 to 1 July 2011 |
| `ls-862-1/` | Gesetz über die Gebäudeversicherung (GebVG) (LS 862.1) | 3 | oldest version available, then each Nachtrag: 1 July 2011 to 1 April 2020 |
| `ls-910-1/` | Landwirtschaftsgesetz (LG) (LS 910.1) | 10 | oldest version available, then each Nachtrag: 1 January 2005 to 1 July 2026 |
| `ls-916-21/` | Kantonales Tierseuchengesetz (KTSG) (LS 916.21) | 1 | as enacted1 January 2014 |
| `ls-921-1/` | Kantonales Waldgesetz (LS 921.1) | 3 | oldest version available, then each Nachtrag: 1 January 2007 to 1 January 2018 |
| `ls-922-1/` | Kantonales Jagdgesetz (JG) (LS 922.1) | 1 | as enacted1 January 2023 |
| `ls-923-1/` | Gesetz über die Fischerei (LS 923.1) | 3 | oldest version available, then each Nachtrag: 1 January 2007 to 1 January 2013 |
| `ls-930-1/` | Standortförderungs- und Unternehmensentlastungsgesetz (SFUEG) (LS 930.1) | 1 | as enacted1 July 2026 |
| `ls-935-11/` | Gastgewerbegesetz (LS 935.11) | 2 | oldest version available, then each Nachtrag: 1 May 2010 to 1 January 2018 |
| `ls-935-21/` | Gesetz über den Jugendschutz bei öffentlichen Filmvorführungen und Trägermedien (JFTG) (LS 935.21) | 1 | as enacted1 July 2019 |
| `ls-935-31/` | Gesetz über die Märkte und das Reisendengewerbe (LS 935.31) | 2 | as enacted, then each Nachtrag: 1 July 2007 to 1 January 2012 |
| `ls-935-32/` | Gesetz über das Unterhaltungsgewerbe (LS 935.32) | 2 | oldest version available, then each Nachtrag: 1 January 2007 to 1 January 2022 |
| `ls-935-41/` | Gesetz über die Geschäftsagenten, Liegenschaftenvermittler und Privatdetektive (LS 935.41) | 1 | one version (the oldest available)1 July 2010 |
| `ls-935-51/` | Gesetz über den Personentransport mit Taxis und Limousinen (PTLG) (LS 935.51) | 1 | as enacted1 January 2024 |
| `ls-951-1/` | Kantonalbankgesetz (ZKBG) (LS 951.1) | 9 | oldest version available, then each Nachtrag: 1 January 2005 to 1 January 2025 |
| `ls-131-3/` | Verordnung des Obergerichts über die Beglaubigungen durch die Gemeindeammänner (LS 131.3) | 1 | one version (the oldest available)1 January 2011 |
| `ls-131-11/` | Gemeindeverordnung (VGG) (LS 131.11) | 10 | as enacted, then each Nachtrag: 1 January 2018 to 1 August 2026 |
| `ls-132-11/` | Finanzausgleichsverordnung (FAV) (LS 132.11) | 7 | as enacted, then each Nachtrag: 1 January 2012 to 1 July 2026 |
| `ls-132-21/` | Staatsbeitragsverordnung (StBV) (LS 132.21) | 3 | oldest version available, then each Nachtrag: 1 January 2005 to 1 January 2012 |
| `ls-141-11/` | Kantonale Bürgerrechtsverordnung (KBüV) (LS 141.11) | 1 | as enacted1 July 2023 |
| `ls-142-20/` | Verordnung über die Zuständigkeiten im Ausländerrecht (VZA) (LS 142.20) | 6 | as enacted, then each Nachtrag: 1 December 2011 to 1 January 2024 |
| `ls-142-31/` | Verordnung über die Härtefallkommission (LS 142.31) | 1 | as enacted1 September 2009 |
| `ls-142-51/` | Verordnung über das elektronische Archiv des Migrationsamtes (ELARV) (LS 142.51) | 4 | as enacted, then each Nachtrag: 1 October 2004 to 1 November 2022 |
| `ls-143-2/` | Kantonale Ausweisverordnung (LS 143.2) | 2 | as enacted, then each Nachtrag: 1 March 2010 to 1 March 2012 |
| `ls-161-1/` | Verordnung über die politischen Rechte (VPR) (LS 161.1) | 13 | as enacted, then each Nachtrag: 1 January 2005 to 1 July 2026 |
| `ls-170-8/` | Verordnung über die Informationsverwaltung und -sicherheit (IVSV) (LS 170.8) | 1 | as enacted1 January 2020 |
| `ls-170-41/` | Verordnung über die Information und den Datenschutz (IDV) (LS 170.41) | 3 | as enacted, then each Nachtrag: 1 October 2008 to 24 January 2020 |
| `ls-170-51/` | Publikationsverordnung (PublV) (LS 170.51) | 3 | as enacted, then each Nachtrag: 1 January 2018 to 1 January 2025 |
| `ls-170-61/` | Archivverordnung (LS 170.61) | 3 | oldest version available, then each Nachtrag: 15 January 2014 to 1 January 2020 |
| `ls-171-3/` | Verordnung über die Parlamentsdienste (VoPD) (LS 171.3) | 1 | as enacted1 May 2020 |
| `ls-171-11/` | Kantonsratsreglement (KRR) (LS 171.11) | 3 | as enacted, then each Nachtrag: 1 May 2020 to 1 July 2026 |
| `ls-171-21/` | Entschädigungsverordnung des Kantonsrates (EVKR) (LS 171.21) | 1 | one version (the oldest available)23 April 2021 |
| `ls-171-41/` | Verordnung über das kantonale Jugendparlament (VJP) (LS 171.41) | 3 | as enacted, then each Nachtrag: 1 May 2017 to 1 June 2022 |
| `ls-171-51/` | Reglement des Kantonsrates über den Zürcher Zukunftspreis (RZZP) (LS 171.51) | 1 | as enacted1 May 2024 |
| `ls-172-4/` | Verordnung zum Bundesgesetz über die wirtschaftliche Landesversorgung (WLV) (LS 172.4) | 3 | as enacted, then each Nachtrag: 1 March 2011 to 1 October 2024 |
| `ls-172-5/` | Verordnung über die strategische Führung und den Einsatz der kantonalen Führungsorganisation (KFOV) (LS 172.5) | 4 | as enacted, then each Nachtrag: 1 April 2011 to 1 June 2025 |
| `ls-172-8/` | Integrationsverordnung (LS 172.8) | 1 | as enacted1 November 2006 |
| `ls-172-11/` | Verordnung über die Organisation des Regierungsrates und der kantonalen Verwaltung (VOG RR) (LS 172.11) | 31 | as enacted, then each Nachtrag: 1 September 2007 to 1 July 2026 |
| `ls-172-15/` | Verordnung über das Rekursverfahren vor dem Regierungsrat (LS 172.15) | 1 | one version (the oldest available)1 September 2007 |
| `ls-172-16/` | Rechtsetzungsverordnung (RSV) (LS 172.16) | 3 | oldest version available, then each Nachtrag: 1 January 2016 to 1 September 2023 |
| `ls-172-110-2/` | Organisationsverordnung der Sicherheitsdirektion (OV DS) (LS 172.110.2) | 4 | as enacted, then each Nachtrag: 1 January 2013 to 1 January 2018 |
| `ls-172-110-3/` | Organisationsverordnung der Finanzdirektion (OV FD) (LS 172.110.3) | 8 | as enacted, then each Nachtrag: 1 April 2016 to 1 July 2026 |
| `ls-172-110-4/` | Organisationsverordnung der Volkswirtschaftsdirektion (OV VD) (LS 172.110.4) | 5 | as enacted, then each Nachtrag: 1 May 2010 to 26 January 2024 |
| `ls-172-110-5/` | Organisationsverordnung der Gesundheitsdirektion (OV GD) (LS 172.110.5) | 4 | oldest version available, then each Nachtrag: 21 February 2022 to 1 June 2024 |
| `ls-172-110-6/` | Organisationsverordnung der Bildungsdirektion (OV BI) (LS 172.110.6) | 2 | as enacted, then each Nachtrag: 1 February 2023 to 1 November 2025 |
| `ls-172-110-7/` | Organisationsverordnung der Baudirektion (BDOV) (LS 172.110.7) | 5 | as enacted, then each Nachtrag: 1 October 2012 to 1 July 2025 |
| `ls-172-110-11/` | Verordnung über die Datenbearbeitung der Direktion der Justiz und des Innern (LS 172.110.11) | 2 | as enacted, then each Nachtrag: 1 July 2016 to 1 April 2020 |
| `ls-172-311/` | Verordnung über die Kantonale Drucksachen- und Materialzentrale (KDMZ) (LS 172.311) | 1 | one version (the oldest available)1 July 2003 |
| `ls-173-42/` | Verordnung über den Aufbau des Bezirksgerichts Dietikon (LS 173.42) | 1 | as enacted1 February 2008 |
| `ls-175-21/` | Organisationsverordnung des Verwaltungsgerichts (OV VGr) (LS 175.21) | 3 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2026 |
| `ls-175-211/` | Verordnung über die Kanzlei des Verwaltungsgerichts (LS 175.211) | 1 | as enacted1 January 2011 |
| `ls-175-252/` | Gebührenverordnung des Verwaltungsgerichts (GebV VGr) (LS 175.252) | 1 | as enacted1 June 2019 |
| `ls-176-5/` | Verordnung über die Beteiligung der Gemeinden an den Kosten der Ombudsperson (LS 176.5) | 2 | as enacted, then each Nachtrag: 1 January 2012 to 1 July 2018 |
| `ls-177-115/` | Verordnung über die Nutzung von Internet und E-Mail (LS 177.115) | 2 | as enacted, then each Nachtrag: 1 October 2003 to 1 January 2026 |
| `ls-180-11/` | Verordnung zum Kirchengesetz und zum Gesetz über die anerkannten jüdischen Gemeinden (LS 180.11) | 3 | as enacted, then each Nachtrag: 1 January 2010 to 1 July 2012 |
| `ls-181-13/` | Finanzverordnung der Evangelisch-reformierten Landeskirche des Kantons Zürich (LS 181.13) | 2 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-181-15/` | Verordnung über das Mitgliederregister (MRVO) (LS 181.15) | 2 | as enacted, then each Nachtrag: 1 January 2020 to 1 November 2020 |
| `ls-181-17/` | Verordnung über die religionspädagogischen Module (rpg-Verordnung) (LS 181.17) | 3 | as enacted, then each Nachtrag: 1 May 2008 to 1 August 2022 |
| `ls-181-19/` | Verordnung über die Aufsicht über kirchliche Stiftungen (StAVO) (LS 181.19) | 1 | as enacted1 January 2021 |
| `ls-181-20/` | Verordnung über die Wahl der Kirchensynode (Synodalwahlverordnung) (LS 181.20) | 3 | as enacted, then each Nachtrag: 1 July 2010 to 1 August 2025 |
| `ls-181-25/` | Verordnung über die Entschädigungen an Mitglieder landeskirchlicher Behörden, Organe und Kommissionen (Entschädigungsverordnung) (LS 181.25) | 6 | as enacted, then each Nachtrag: 15 June 2007 to 1 January 2024 |
| `ls-181-40/` | Personalverordnung der Evangelisch-reformierten Landeskirche des Kantons Zürich (LS 181.40) | 7 | as enacted, then each Nachtrag: 1 January 2012 to 1 January 2026 |
| `ls-181-43/` | Verordnung über die Aufsicht und die Visitation in den Kirchgemeinden (LS 181.43) | 4 | as enacted, then each Nachtrag: 1 July 2011 to 1 June 2026 |
| `ls-181-44/` | Verordnung über das Kirchgemeindearchiv, das Pfarrarchiv und die kirchlichen Register (Archiv- und Registerverordnung, ARVO) (LS 181.44) | 1 | as enacted1 July 2026 |
| `ls-181-50/` | Verordnung über die Seelsorge in Institutionen (SIVO) (LS 181.50) | 1 | as enacted1 September 2016 |
| `ls-181-131/` | Vollzugsverordnung zur Finanzverordnung (LS 181.131) | 13 | as enacted, then each Nachtrag: 1 January 2011 to 1 March 2026 |
| `ls-181-221/` | Verordnung über die Organisation der Gesamtkirchlichen Dienste (VO GKD) (LS 181.221) | 2 | as enacted, then each Nachtrag: 1 October 2021 to 1 February 2022 |
| `ls-181-222/` | Verordnung über die Konferenz der Dekaninnen und Dekane (DeKVO) (LS 181.222) | 1 | as enacted1 March 2023 |
| `ls-181-402/` | Verordnung über das Pfarramt in der Landeskirche (LS 181.402) | 8 | as enacted, then each Nachtrag: 1 January 2015 to 1 June 2026 |
| `ls-181-412/` | Verordnung über den Quereinstieg ins Pfarramt (Quest-Verordnung, QuestV) (LS 181.412) | 2 | oldest version available, then each Nachtrag: 25 April 2024 to 1 November 2024 |
| `ls-181-416/` | Rekursverordnung (RVO) (LS 181.416) | 1 | one version (the oldest available)25 April 2024 |
| `ls-182-14/` | Verordnung über das Register der Mitglieder und weiterer Personen der Römisch-katholischen Körperschaft des Kantons Zürich (RMVO) (LS 182.14) | 1 | one version (the oldest available)25 May 2022 |
| `ls-182-15/` | Entschädigungsreglement der Römisch-katholischen Körperschaft des Kantons Zürich (Entschädigungsreglement, ER) (LS 182.15) | 6 | as enacted, then each Nachtrag: 1 January 2010 to 1 July 2023 |
| `ls-182-22/` | Reglement über die Wahl der Pfarrer und Pfarreibeauftragten (RWPP) (LS 182.22) | 1 | as enacted1 January 2024 |
| `ls-182-23/` | Reglement über die Organisation, die Aufgaben und Kompetenzen der Personalkommission sowie die Delegation von Aufgaben und Kompetenzen an einzelne Kaderangestellte der Römisch-katholischen Körperschaft des Kantons Zürich (Personalreglement des Synodalrates) (LS 182.23) | 1 | as enacted1 April 2020 |
| `ls-182-33/` | Verordnung der römisch-katholischen Körperschaft des Kantons Zürich über die Beiträge an die Finanzierung regionaler Jugendseelsorger (LS 182.33) | 1 | as enacted12 June 1987 |
| `ls-182-34/` | Verordnung der römisch-katholischen Körperschaft des Kantons Zürich über die Finanzierung der Migrantenseelsorge (LS 182.34) | 2 | as enacted, then each Nachtrag: 1 January 2006 to 31 December 2012 |
| `ls-182-42/` | Reglement über den Einsatz der Informatikmittel in der Römisch-katholischen Körperschaft des Kantons Zürich (ICT-Reglement) (LS 182.42) | 1 | as enacted1 October 2025 |
| `ls-182-43/` | Reglement über die Entbindung vom Seelsorgegeheimnis (LS 182.43) | 1 | as enacted1 March 2021 |
| `ls-182-51/` | Reglement über Organisation und Verfahren der Rekurskommission der Römisch-katholischen Körperschaft des Kantons Zürich (LS 182.51) | 3 | as enacted, then each Nachtrag: 1 January 2010 to 1 July 2021 |
| `ls-182-60/` | Reglement der Römisch-katholischen Körperschaft des Kantons Zürich über die Kirchgemeinden (KGR) (Kirchgemeindereglement) (LS 182.60) | 3 | as enacted, then each Nachtrag: 1 January 2018 to 1 April 2026 |
| `ls-182-63/` | Reglement über den Finanzhaushalt der römisch-katholischen Kirchgemeinden im Kanton Zürich (FKG) (Finanzreglement der Kirchgemeinden) (LS 182.63) | 1 | as enacted1 January 2019 |
| `ls-183-15/` | Personalreglement der Christkatholischen Kirchgemeinde Zürich (LS 183.15) | 1 | one version (the oldest available)25 July 2022 |
| `ls-211-11/` | Gebührenverordnung des Obergerichts (GebV OG) (LS 211.11) | 1 | as enacted1 January 2011 |
| `ls-211-12/` | Verordnung der obersten kantonalen Gerichte über die Entschädigung der Zeugen und Zeuginnen, Auskunftspersonen und Sachverständigen (Entschädigungsverordnung der obersten Gerichte) (LS 211.12) | 1 | one version (the oldest available)1 January 2011 |
| `ls-211-13/` | Verordnung des Obergerichtes über die Verwaltung von Depositen, Kautionen und Effekten (LS 211.13) | 2 | oldest version available, then each Nachtrag: 1 October 2003 to 1 January 2011 |
| `ls-211-14/` | Verordnung des Obergerichts über das Rechnungswesen der Bezirksgerichte und des Obergerichts sowie über das zentrale Inkasso (LS 211.14) | 3 | as enacted, then each Nachtrag: 1 July 2003 to 1 January 2011 |
| `ls-211-16/` | Verordnung der obersten kantonalen Gerichte über die Archivierung von Verfahrensakten (Archivverordnung der obersten Gerichte) (LS 211.16) | 2 | oldest version available, then each Nachtrag: 1 October 2003 to 1 January 2011 |
| `ls-211-17/` | Sprachdienstleistungsverordnung (SDV) (LS 211.17) | 3 | as enacted, then each Nachtrag: 1 July 2019 to 1 June 2024 |
| `ls-211-21/` | Vollzugsverordnung der obersten kantonalen Gerichte zum Personalgesetz (LS 211.21) | 3 | oldest version available, then each Nachtrag: 1 October 2003 to 1 January 2011 |
| `ls-211-22/` | Verordnung der obersten kantonalen Gerichte über die Nutzung von Internet und E-Mail (LS 211.22) | 1 | as enacted1 July 2004 |
| `ls-211-23/` | Verordnung der obersten kantonalen Gerichte über die Gerichtsauditoren und Gerichtsauditorinnen (LS 211.23) | 2 | oldest version available, then each Nachtrag: 1 October 2003 to 1 January 2011 |
| `ls-211-25/` | Verordnung über das Mitspracherecht des Personals der Gerichte und Notariate (LS 211.25) | 1 | one version (the oldest available)1 January 2011 |
| `ls-211-56/` | Verordnung über den Vollzug der Zwangsmassnahmen im Ausländerrecht (VVZMA) (LS 211.56) | 5 | oldest version available, then each Nachtrag: 1 January 2007 to 1 February 2026 |
| `ls-211-112/` | Verordnung über das Inkasso von Gebühren und Kosten (LS 211.112) | 2 | as enacted, then each Nachtrag: 1 July 2007 to 1 January 2011 |
| `ls-212-51/` | Verordnung über die Organisation des Obergerichts (LS 212.51) | 2 | as enacted, then each Nachtrag: 1 January 2011 to 1 March 2022 |
| `ls-212-511/` | Verordnung über die Organisation und Geschäftsführung der Obergerichtskanzlei (LS 212.511) | 1 | as enacted1 January 2011 |
| `ls-212-513/` | Akturierungsverordnung (LS 212.513) | 1 | as enacted1 January 2011 |
| `ls-212-811/` | Verordnung über die Organisation und den Geschäftsgang des Sozialversicherungsgerichts (OrgV SVGer) (LS 212.811) | 3 | as enacted, then each Nachtrag: 1 April 2005 to 1 January 2022 |
| `ls-212-812/` | Verordnung über die Gebühren, Kosten und Entschädigungen vor dem Sozialversicherungsgericht (GebV SVGer) (LS 212.812) | 2 | as enacted, then each Nachtrag: 1 July 2011 to 1 January 2022 |
| `ls-212-814/` | Verordnung über das Schiedsgericht in Sozialversicherungsstreitigkeiten (SGVo) (LS 212.814) | 1 | as enacted1 April 2005 |
| `ls-213-21/` | Verordnung über die Organisation der Oberstaatsanwaltschaft und der Staatsanwaltschaften (VOSTA) (LS 213.21) | 4 | as enacted, then each Nachtrag: 1 January 2005 to 1 April 2026 |
| `ls-213-23/` | Verordnung über das Wahlfähigkeitszeugnis für Staatsanwältinnen und Staatsanwälte (LS 213.23) | 3 | as enacted, then each Nachtrag: 1 January 2006 to 1 January 2011 |
| `ls-213-27/` | Verordnung zum Bundesgesetz über die Teilung eingezogener Vermögenswerte (VO TEVG) (LS 213.27) | 1 | as enacted1 April 2012 |
| `ls-213-231/` | Reglement der Direktion der Justiz und des Innern über die Organisation und die Tätigkeit der Prüfungskommission für die Staatsanwaltschaften (LS 213.231) | 3 | as enacted, then each Nachtrag: 1 February 2006 to 1 March 2021 |
| `ls-215-2/` | Verordnung des Obergerichts über die Aufsichtskommission über die Anwältinnen und Anwälte (LS 215.2) | 2 | as enacted, then each Nachtrag: 1 January 2005 to 1 October 2026 |
| `ls-215-3/` | Verordnung über die Anwaltsgebühren (AnwGebV) (LS 215.3) | 2 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2015 |
| `ls-215-11/` | Verordnung des Obergerichts über die Fähigkeitsprüfung für den Anwaltsberuf (LS 215.11) | 2 | as enacted, then each Nachtrag: 1 January 2007 to 1 September 2013 |
| `ls-215-12/` | Verordnung des Obergerichts über die Gebühren, Kosten und Entschädigungen gemäss Anwaltsgesetz (LS 215.12) | 1 | as enacted1 January 2007 |
| `ls-215-21/` | Verordnung des Obergerichts über die Durchführung der Wahl der durch die Anwaltschaft zu wählenden Mitglieder und Ersatzmitglieder der Aufsichtskommission (LS 215.21) | 2 | as enacted, then each Nachtrag: 1 January 2005 to 1 January 2011 |
| `ls-215-22/` | Verordnung des Obergerichts über die Entschädigung der Mitglieder der Aufsichtskommission (LS 215.22) | 1 | as enacted1 January 2005 |
| `ls-215-111/` | Verordnung des Obergerichts über die Entschädigung der Mitglieder der Anwaltsprüfungskommission (LS 215.111) | 2 | as enacted, then each Nachtrag: 1 January 2007 to 1 October 2024 |
| `ls-230-5/` | Verordnung über die elektronische Überwachung zum Schutz gewaltbetroffener Personen (VeÜ) (LS 230.5) | 1 | as enacted1 January 2022 |
| `ls-230-31/` | Vollziehungsverordnung zum Bundesgesetz über Voraussetzungen und Verfahren bei Sterilisationen (LS 230.31) | 1 | as enacted1 January 2013 |
| `ls-231-1/` | Kantonale Zivilstandsverordnung (ZVO) (LS 231.1) | 16 | as enacted, then each Nachtrag: 1 January 2005 to 1 January 2025 |
| `ls-232-32/` | Verordnung über den elektronischen Zugriff der Kindes- und Erwachsenenschutzbehörden auf die Einwohnerregister (LS 232.32) | 1 | as enacted1 April 2013 |
| `ls-232-35/` | Verordnung über Entschädigung und Spesenersatz bei Beistandschaften (ESBV) (LS 232.35) | 1 | as enacted1 January 2013 |
| `ls-232-351/` | Verordnung über die Entschädigung der Fachärztinnen und Fachärzte bei der fürsorgerischen Unterbringung freiwillig Eingetretener (LS 232.351) | 1 | as enacted1 March 2017 |
| `ls-234-3/` | Verordnung über die Meldestelle für gefundene Tiere (LS 234.3) | 1 | as enacted1 May 2005 |
| `ls-234-12/` | Verordnung zum Einführungsgesetz zum Bundesgesetz über den Erwerb von Grundstücken durch Personen im Ausland (VBewG) (LS 234.12) | 2 | as enacted, then each Nachtrag: 1 July 2010 to 1 January 2018 |
| `ls-235-15/` | Verordnung des Obergerichts über das Verfahren bei freiwilligen öffentlichen Versteigerungen (LS 235.15) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 24 May 2019 |
| `ls-242-1/` | Verordnung über den Erwerb des Wahlfähigkeitszeugnisses für Notarinnen und Notare (NotPV) (LS 242.1) | 1 | as enacted1 January 2014 |
| `ls-242-2/` | Verordnung des Obergerichtes über die Geschäftsführung der Notariate (Notariatsverordnung) (LS 242.2) | 4 | oldest version available, then each Nachtrag: 1 January 2007 to 1 July 2016 |
| `ls-242-25/` | Verordnung über die Notariatsverwaltung (Notariatsverwaltungsverordnung) (LS 242.25) | 3 | oldest version available, then each Nachtrag: 1 January 2011 to 1 July 2016 |
| `ls-242-26/` | Verordnung des Obergerichts über die Rechnungs- und Kassenführung im Notariatswesen (Rechnungswesenverordnung) (LS 242.26) | 2 | oldest version available, then each Nachtrag: 1 October 2003 to 1 July 2016 |
| `ls-243/` | Notariatsgebührenverordnung (NotGebV) (LS 243) | 5 | as enacted, then each Nachtrag: 1 July 2009 to 1 January 2024 |
| `ls-252/` | Verordnung des Obergerichtes über die Geschäftsführung der Grundbuchämter und die Einführung des eidgenössischen Grundbuches (Kantonale Grundbuchverordnung) (LS 252) | 5 | oldest version available, then each Nachtrag: 1 January 2005 to 1 December 2024 |
| `ls-281-1/` | Verordnung über die Betreibungs- und Gemeindeammannämter (VBG) (LS 281.1) | 2 | as enacted, then each Nachtrag: 1 July 2010 to 1 January 2011 |
| `ls-281-2/` | Verordnung des Obergerichtes über die Geschäftsführung der Konkursämter (Kantonale Konkursverordnung) (LS 281.2) | 3 | oldest version available, then each Nachtrag: 1 July 2004 to 1 January 2011 |
| `ls-281-11/` | Verordnung über die Gebühren der Gemeindeammannämter (GebV GA) (LS 281.11) | 1 | one version (the oldest available)24 May 2019 |
| `ls-281-51/` | Verordnung des Obergerichts über den Wahlfähigkeitsausweis für Betreibungsbeamtinnen und Betreibungsbeamte (LS 281.51) | 2 | as enacted, then each Nachtrag: 1 January 2009 to 1 January 2016 |
| `ls-315-1/` | Verordnung über die Kommission zur Bekämpfung von Menschenhandel (Runder Tisch Menschenhandel, VRTM) (LS 315.1) | 1 | as enacted1 January 2022 |
| `ls-321-1/` | Verordnung über die Zuständigkeit der Gemeinden im Übertretungsstrafrecht (LS 321.1) | 4 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2016 |
| `ls-321-2/` | Kantonale Ordnungsbussenverordnung (KOBV) (LS 321.2) | 4 | as enacted, then each Nachtrag: 1 January 2020 to 1 June 2025 |
| `ls-321-3/` | Verordnung über den Einsatz des Einzelgerichts als Zwangsmassnahmengericht in Haftsachen (Haftrichterverordnung) (LS 321.3) | 1 | as enacted1 January 2011 |
| `ls-321-4/` | Verordnung über psychiatrische und psychologische Gutachten in Straf- und Zivilverfahren (PPGV) (LS 321.4) | 5 | as enacted, then each Nachtrag: 1 March 2011 to 1 June 2026 |
| `ls-321-5/` | DNA-Verordnung (DNAV) (LS 321.5) | 4 | as enacted, then each Nachtrag: 1 July 2005 to 1 October 2024 |
| `ls-321-6/` | Verordnung über die Mediation im Jugendstrafverfahren (LS 321.6) | 1 | as enacted1 January 2011 |
| `ls-322/` | Verordnung über die Jugendstrafrechtspflege (JStV) (LS 322) | 4 | as enacted, then each Nachtrag: 1 January 2007 to 1 January 2013 |
| `ls-323-1/` | Verordnung über die Gebühren, Auslagen und Entschädigungen der Strafverfolgungsbehörden (GebV StrV) (LS 323.1) | 4 | as enacted, then each Nachtrag: 1 January 2011 to 1 November 2018 |
| `ls-326/` | Reglement für das Kriminalistische Institut des Kantons Zürich (LS 326) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2022 |
| `ls-331-1/` | Justizvollzugsverordnung (JVV) (LS 331.1) | 13 | as enacted, then each Nachtrag: 1 January 2007 to 1 July 2025 |
| `ls-331-5/` | Kantonale Verordnung über das Strafregister-Informationssystem VOSTRA (KStReV) (LS 331.5) | 1 | as enacted1 October 2024 |
| `ls-341-1/` | Kantonale Opferhilfeverordnung (KOHV) (LS 341.1) | 2 | as enacted, then each Nachtrag: 1 July 2013 to 1 April 2024 |
| `ls-410-5/` | Reglement der EDK über die Anerkennung von gymnasialen Maturitätszeugnissen (Maturitätsanerkennungsreglement, MAR) (LS 410.5) | 1 | one version (the oldest available)25 April 2025 |
| `ls-410-8/` | Verordnung über das Sportamt und die Sportkommission (LS 410.8) | 3 | oldest version available, then each Nachtrag: 1 May 2006 to 1 January 2013 |
| `ls-410-11/` | Synodalverordnung (LS 410.11) | 5 | as enacted, then each Nachtrag: 15 June 2004 to 1 August 2017 |
| `ls-410-61/` | Musikschulverordnung (MuSV) (LS 410.61) | 1 | as enacted1 January 2023 |
| `ls-412-14/` | Lehrmittelverordnung für die Volksschule (LS 412.14) | 1 | as enacted1 November 2014 |
| `ls-412-101/` | Volksschulverordnung (VSV) (LS 412.101) | 9 | oldest version available, then each Nachtrag: 1 August 2012 to 1 August 2026 |
| `ls-412-101-3/` | Reglement über die Aufnahme von Schülerinnen und Schülern in fremdsprachige Schulen (LS 412.101.3) | 1 | as enacted18 August 2014 |
| `ls-412-101-6/` | Reglement über die Aufsicht über den Privatunterricht (LS 412.101.6) | 1 | as enacted17 August 2009 |
| `ls-412-101-21/` | Reglement über die Zugriffsrechte und die Datensicherheit der Daten der schulpsychologischen Dienste (LS 412.101.21) | 1 | as enacted1 January 2017 |
| `ls-412-103/` | Verordnung über die sonderpädagogischen Massnahmen (VSM) (LS 412.103) | 12 | as enacted, then each Nachtrag: 18 August 2008 to 1 August 2026 |
| `ls-412-104/` | Verordnung über Schulversuche an der Volksschule (LS 412.104) | 2 | as enacted, then each Nachtrag: 1 September 2007 to 1 August 2012 |
| `ls-412-105/` | Finanzverordnung zum Volksschulgesetz (LS 412.105) | 9 | as enacted, then each Nachtrag: 1 January 2008 to 1 January 2022 |
| `ls-412-106/` | Verordnung über die Finanzierung der Sonderschulung (VFiSo) (LS 412.106) | 1 | as enacted1 January 2022 |
| `ls-412-106-1/` | Verordnung über die Aufsicht über die Sonderschulung (LS 412.106.1) | 1 | as enacted1 January 2022 |
| `ls-412-107/` | Spitalschulverordnung (SpiV) (LS 412.107) | 1 | as enacted1 January 2022 |
| `ls-412-107-1/` | Verordnung über die Aufsicht über die Spitalschulen (LS 412.107.1) | 1 | as enacted1 January 2022 |
| `ls-412-121-31/` | Reglement über die Ausstellung der Schulzeugnisse (Zeugnisreglement) (LS 412.121.31) | 6 | as enacted, then each Nachtrag: 16 August 2008 to 19 August 2019 |
| `ls-412-138-1/` | Reglement über den Abschluss Sekundarstufe I für Erwachsene (LS 412.138.1) | 4 | as enacted, then each Nachtrag: 1 January 2004 to 1 January 2022 |
| `ls-412-141/` | Verordnung über den Lehrmittelverlag (LS 412.141) | 1 | one version (the oldest available)1 November 2014 |
| `ls-412-411/` | Personalreglement für das Zentrum für Gehör und Sprache (LS 412.411) | 1 | as enacted1 January 2012 |
| `ls-412-412/` | Finanzreglement für das Zentrum für Gehör und Sprache (LS 412.412) | 2 | as enacted, then each Nachtrag: 1 January 2012 to 1 January 2022 |
| `ls-413-51/` | Verordnung über die Schulen im Gesundheitswesen (LS 413.51) | 2 | oldest version available, then each Nachtrag: 1 October 2003 to 1 March 2005 |
| `ls-413-112-5/` | Reglement über die Ausrichtung von Entschädigungen für die Mitwirkung bei Aufnahme- und Abschlussprüfungen an kantonalen Mittelschulen und kantonalen und beitragsberechtigten Berufsmaturitätsschulen (LS 413.112.5) | 5 | as enacted, then each Nachtrag: 1 May 2005 to 1 February 2024 |
| `ls-413-113/` | Verordnung über die Schulgelder an den kantonalen Mittelschulen (LS 413.113) | 2 | as enacted, then each Nachtrag: 16 August 2004 to 1 August 2012 |
| `ls-413-116-1/` | Verordnung über abweichende Aufbewahrungsfristen im Bereich der Sekundarstufe II und der Tertiärstufe B (LS 413.116.1) | 2 | as enacted, then each Nachtrag: 1 January 2017 to 1 June 2025 |
| `ls-413-211/` | Mittelschulverordnung (MSV) (LS 413.211) | 6 | oldest version available, then each Nachtrag: 19 August 2013 to 1 August 2026 |
| `ls-413-211-1/` | Disziplinarreglement der Mittelschulen (LS 413.211.1) | 2 | as enacted, then each Nachtrag: 1 August 2015 to 25 September 2020 |
| `ls-413-211-2/` | Reglement betreffend Unterricht an den kantonalen Gymnasien (Unterrichtsreglement) (LS 413.211.2) | 1 | as enacted1 August 2023 |
| `ls-413-212/` | Verordnung über Subventionen an nichtstaatliche Mittelschulen (LS 413.212) | 1 | one version (the oldest available)1 July 2003 |
| `ls-413-232/` | Reglement für Sprachaufenthalte von Schülerinnen und Schülern der kantonalen Mittelschulen (Sprachaufenthaltsreglement) (LS 413.232) | 1 | as enacted1 February 2012 |
| `ls-413-250-1/` | Reglement für die Aufnahme in die Gymnasien mit Anschluss an die 6. Klasse der Primarschule (LS 413.250.1) | 4 | as enacted, then each Nachtrag: 1 March 2010 to 1 August 2022 |
| `ls-413-250-2/` | Verordnung über die Aufnahme in die Maturitätsschulen im Anschluss an die Sekundarstufe und nach Abschluss der beruflichen Grundbildung (VAM) (LS 413.250.2) | 3 | as enacted, then each Nachtrag: 1 August 2022 to 1 January 2026 |
| `ls-413-250-9/` | Aufnahmereglement für die Kantonale Maturitätsschule für Erwachsene (LS 413.250.9) | 5 | as enacted, then each Nachtrag: 1 March 2010 to 1 March 2026 |
| `ls-413-250-33/` | Reglement für die Aufnahme in die K+S-Klassen am Mathematisch-Naturwissenschaftlichen Gymnasium Rämibühl Zürich mit Anschluss an die 6. Klasse der Primarstufe (LS 413.250.33) | 2 | as enacted, then each Nachtrag: 1 April 2012 to 1 August 2022 |
| `ls-413-251-1/` | Promotionsreglement für die Gymnasien des Kantons Zürich (LS 413.251.1) | 2 | oldest version available, then each Nachtrag: 20 August 2012 to 1 August 2022 |
| `ls-413-251-2/` | Promotionsreglement für die Kantonale Maturitätsschule für Erwachsene (LS 413.251.2) | 3 | oldest version available, then each Nachtrag: 18 August 2008 to 1 August 2022 |
| `ls-413-251-5/` | Promotionsreglement für die kantonalen Handelsmittelschulen (LS 413.251.5) | 4 | as enacted, then each Nachtrag: 21 August 1995 to 1 August 2022 |
| `ls-413-251-8/` | Promotionsreglement für das schweizerisch-italienische Liceo artistico (Kunstgymnasium) Zürich (LS 413.251.8) | 2 | oldest version available, then each Nachtrag: 20 August 2012 to 1 August 2022 |
| `ls-413-251-15/` | Promotionsreglement für die K+S Klassen am Mathematisch-Naturwissenschaftlichen Gymnasium Rämibühl Zürich (LS 413.251.15) | 2 | as enacted, then each Nachtrag: 20 August 2012 to 1 August 2022 |
| `ls-413-251-51/` | Promotionsreglement für die kantonalen Informatikmittelschulen an Handelsmittelschulen (LS 413.251.51) | 3 | as enacted, then each Nachtrag: 19 August 2013 to 1 August 2022 |
| `ls-413-252-1/` | Reglement für die Maturitätsprüfungen an den Gymnasien des Kantons Zürich (LS 413.252.1) | 4 | oldest version available, then each Nachtrag: 22 August 2011 to 25 April 2024 |
| `ls-413-252-4/` | Prüfungsreglement für die Fachmittelschulen des Kantons Zürich (LS 413.252.4) | 6 | as enacted, then each Nachtrag: 20 August 2007 to 1 August 2024 |
| `ls-413-252-8/` | Reglement für die Maturitätsprüfungen des schweizerisch-italienischen Liceo artistico (Kunstgymnasium) Zürich (LS 413.252.8) | 3 | oldest version available, then each Nachtrag: 20 August 2012 to 1 August 2023 |
| `ls-413-311/` | Verordnung zum EG BBG (VEG BBG) (LS 413.311) | 5 | oldest version available, then each Nachtrag: 16 August 2009 to 1 April 2026 |
| `ls-413-311-1/` | Verordnung über die Zulassungsvoraussetzungen und die Abschlussbeurteilung der Berufsvorbereitungsjahre (ZABV) (LS 413.311.1) | 1 | as enacted1 August 2024 |
| `ls-413-311-5/` | Verordnung über die Anforderungen an Lehrpersonen in Berufsvorbereitungsjahren (ALBV) (LS 413.311.5) | 2 | as enacted, then each Nachtrag: 18 August 2014 to 1 August 2024 |
| `ls-413-312/` | Verordnung über die Finanzierung von Leistungen der Berufsbildung (VFin BBG) (LS 413.312) | 11 | as enacted, then each Nachtrag: 1 January 2011 to 1 September 2025 |
| `ls-413-313/` | Verordnung über den Berufsbildungsfonds (VBBF) (LS 413.313) | 2 | as enacted, then each Nachtrag: 1 January 2011 to 1 July 2018 |
| `ls-413-319/` | Verordnung über die Berufs-, Studien- und Laufbahnberatung (V BSLB) (LS 413.319) | 8 | as enacted, then each Nachtrag: 1 March 2014 to 1 July 2026 |
| `ls-413-322/` | Disziplinarreglement Berufsbildung (LS 413.322) | 1 | as enacted1 August 2015 |
| `ls-413-323/` | Disziplinarreglement Berufsvorbereitungsjahr (LS 413.323) | 1 | as enacted1 August 2015 |
| `ls-413-325/` | Reglement über die Qualifikationsverfahren der beruflichen Grundbildung (RQV BBG) (LS 413.325) | 1 | as enacted1 February 2014 |
| `ls-413-325-1/` | Reglement über die Entschädigung von Mitwirkenden bei Qualifikationsverfahren der Berufsbildung (ERQV) (LS 413.325.1) | 1 | as enacted1 January 2024 |
| `ls-413-326/` | Berufsmaturitätsreglement (BMR) (LS 413.326) | 5 | as enacted, then each Nachtrag: 1 January 2015 to 1 August 2026 |
| `ls-413-412/` | Verordnung über die Lehrpersonen der Hauswirtschaftskurse an Mittelschulen (VLHM) (LS 413.412) | 3 | as enacted, then each Nachtrag: 1 March 2011 to 1 August 2026 |
| `ls-414-20/` | Gebührenverordnung der Zürcher Fachhochschulen (GVF) (LS 414.20) | 7 | as enacted, then each Nachtrag: 1 August 2008 to 1 August 2024 |
| `ls-414-101/` | Verordnung zum Fachhochschulgesetz (VFaHG) (LS 414.101) | 2 | as enacted, then each Nachtrag: 1 August 2009 to 1 August 2024 |
| `ls-414-102/` | Finanzverordnung der Zürcher Fachhochschulen (FVF) (LS 414.102) | 2 | as enacted, then each Nachtrag: 1 January 2012 to 1 August 2024 |
| `ls-414-112/` | Personalverordnung der Zürcher Fachhochschulen (PVF) (LS 414.112) | 1 | as enacted1 August 2024 |
| `ls-414-113/` | Organisationsreglement des Fachhochschulrats der Zürcher Fachhochschule (LS 414.113) | 1 | as enacted1 October 2009 |
| `ls-414-254/` | Professurenreglement der Zürcher Hochschule für Angewandte Wissenschaften (LS 414.254) | 1 | one version (the oldest available)20 December 2024 |
| `ls-414-264/` | Professurenreglement der Zürcher Hochschule der Künste (LS 414.264) | 1 | one version (the oldest available)25 September 2024 |
| `ls-414-412-1/` | Reglement zum Aufnahme- und Immatrikulationsverfahren an der Pädagogischen Hochschule Zürich (LS 414.412.1) | 1 | one version (the oldest available)26 January 2026 |
| `ls-414-416-3/` | Verordnung über die Berufseinführung der Lehrpersonen der Volksschule (BLVV) (LS 414.416.3) | 1 | as enacted1 August 2023 |
| `ls-414-417/` | Reglement über die Erweiterungsstudien an der Pädagogischen Hochschule Zürich (LS 414.417) | 1 | as enacted1 September 2026 |
| `ls-414-422-1/` | Reglement zum Joint Degree Masterstudiengang Fachdidaktik Naturwissenschaften an der Pädagogischen Hochschule Zürich, an der Philosophischen Fakultät der Universität Zürich und am Departement Geistes-, Sozial- und Staatswissenschaften der Eidgenössischen Technischen Hochschule Zürich (LS 414.422.1) | 1 | as enacted1 June 2026 |
| `ls-414-422-2/` | Reglement über den Joint Degree Masterstudiengang Fachdidaktik Schulsprache Deutsch an der Pädagogischen Hochschule Zürich und an der Universität Zürich (LS 414.422.2) | 1 | as enacted1 June 2025 |
| `ls-414-422-3/` | Reglement zum Joint Degree Masterstudiengang Fachdidaktik Mathematik an der Pädagogischen Hochschule Zürich und am Departement Geistes-, Sozial- und Staatswissenschaften an der Eidgenössischen Technischen Hochschule Zürich (LS 414.422.3) | 1 | as enacted1 September 2024 |
| `ls-414-422-4/` | Reglement zum Joint Degree Masterstudiengang Fachdidaktik Künste an der Pädagogischen Hochschule Zürich und der Zürcher Hochschule der Künste (LS 414.422.4) | 2 | oldest version available, then each Nachtrag: 23 February 2018 to 1 September 2022 |
| `ls-414-422-5/` | Reglement zum Joint Degree Masterstudiengang Fachdidaktik Ethik, Religionen, Gemeinschaft an der Pädagogischen Hochschule Zürich und an der Universität Zürich (LS 414.422.5) | 1 | as enacted1 March 2024 |
| `ls-414-424/` | Professurenreglement der Pädagogischen Hochschule Zürich (LS 414.424) | 1 | one version (the oldest available)25 September 2024 |
| `ls-415-16/` | Verordnung über die Forschung und Lehre der Universität im Gesundheitsbereich (VüFL) (LS 415.16) | 3 | as enacted, then each Nachtrag: 1 January 2004 to 1 January 2023 |
| `ls-415-21/` | Personalverordnung der Universität Zürich (PVO-UZH) (LS 415.21) | 5 | as enacted, then each Nachtrag: 1 April 2015 to 1 August 2025 |
| `ls-415-23/` | Rahmenverordnung über die Habilitation an der Universität Zürich (RVO Habil) (LS 415.23) | 1 | as enacted1 April 2020 |
| `ls-415-24/` | Rahmenverordnung über die Titularprofessur an der Universität Zürich (RVO TP) (LS 415.24) | 1 | as enacted1 April 2020 |
| `ls-415-27/` | Verordnung über den Umgang mit wissenschaftlichem Fehlverhalten an der Universität Zürich (Integritätsverordnung) (LS 415.27) | 1 | as enacted1 September 2020 |
| `ls-415-31/` | Verordnung über die Zulassung zum Studium an der Universität Zürich (VZS) (LS 415.31) | 2 | as enacted, then each Nachtrag: 1 February 2019 to 1 August 2022 |
| `ls-415-33/` | Disziplinarverordnung der Universität Zürich (LS 415.33) | 1 | as enacted1 June 2022 |
| `ls-415-60/` | Rahmenverordnung über die Weiterbildung an der Universität Zürich (RVO WB) (LS 415.60) | 1 | as enacted1 December 2020 |
| `ls-415-111-2/` | Reglement für die Wahl der Delegierten der Stände in die Organe und weitere Gremien der Universität Zürich (Wahlreglement) (LS 415.111.2) | 3 | as enacted, then each Nachtrag: 1 April 2020 to 1 January 2022 |
| `ls-415-111-3/` | Organisationsreglement der Erweiterten Universitätsleitung (OrgR EUL) (LS 415.111.3) | 3 | as enacted, then each Nachtrag: 1 August 2022 to 1 October 2026 |
| `ls-415-111-4/` | Organisationsreglement des Senats der Universität Zürich (OrgR Senat) (LS 415.111.4) | 1 | as enacted1 April 2025 |
| `ls-415-111-7/` | Verordnung über Organisation und Verfahren der Rekurskommission der Zürcher Hochschulen (VoRK) (LS 415.111.7) | 1 | as enacted1 August 2024 |
| `ls-415-112/` | Finanzreglement der Universität Zürich (LS 415.112) | 3 | as enacted, then each Nachtrag: 1 January 2010 to 1 January 2025 |
| `ls-415-113/` | Verordnung über die Einwerbung und Entgegennahme von Spenden und Sponsoringbeiträgen (Fundraising) der Universität Zürich (LS 415.113) | 1 | as enacted1 February 2019 |
| `ls-415-114/` | Verordnung über die Verleihung der Würde eines Ehrendoktorats durch die Erweiterte Universitätsleitung (LS 415.114) | 1 | as enacted1 January 2018 |
| `ls-415-115/` | Evaluationsreglement der Universität Zürich (LS 415.115) | 1 | as enacted1 August 2018 |
| `ls-415-116/` | Reglement zum Schutz vor sexueller Belästigung an der Universität Zürich (LS 415.116) | 1 | as enacted1 May 2007 |
| `ls-415-117/` | Immobilienverordnung der Universität Zürich (ImV UZH) (LS 415.117) | 1 | one version (the oldest available)22 February 2019 |
| `ls-415-117-1/` | Reglement über die Zuständigkeiten im Immobilienwesen der Universität Zürich (LS 415.117.1) | 2 | oldest version available, then each Nachtrag: 22 February 2019 to 1 March 2021 |
| `ls-415-121/` | Reglement über die Beurteilung von Lehrveranstaltungen durch die Studierenden an der Universität Zürich (LS 415.121) | 2 | as enacted, then each Nachtrag: 14 September 2009 to 1 February 2014 |
| `ls-415-212/` | Reglement über die Arbeitszeit und die Lohnzuschläge der klinisch tätigen Oberärztinnen und Oberärzte und Assistenzärztinnen und Assistenzärzte der Vetsuisse-Fakultät der Universität Zürich (LS 415.212) | 3 | oldest version available, then each Nachtrag: 19 December 2017 to 1 January 2021 |
| `ls-415-213/` | Reglement über die Entschädigung von Pikettdienst in besonderen Organisationseinheiten an der Universität Zürich (REP-UZH) (LS 415.213) | 1 | as enacted1 January 2022 |
| `ls-415-215/` | Reglement über die Funktionszulagen für Professorinnen und Professoren der Universität Zürich (LS 415.215) | 1 | as enacted1 October 2020 |
| `ls-415-215-3/` | Reglement über die leistungsabhängige Entschädigung für die Führung von vorwiegend dienstleistungserbringenden Organisationseinheiten an der Medizinischen Fakultät der Universität Zürich (LS 415.215.3) | 1 | one version (the oldest available)1 April 2003 |
| `ls-415-311/` | Verordnung über die Aufnahmeprüfung an die Universität Zürich (LS 415.311) | 1 | as enacted1 February 2021 |
| `ls-415-321/` | Verordnung über die Studiengebühren an der Universität Zürich (LS 415.321) | 2 | as enacted, then each Nachtrag: 1 August 2022 to 1 January 2025 |
| `ls-415-322/` | Verordnung über die zusätzliche Studiengebühr von ausländischen Studierenden an der Universität (LS 415.322) | 1 | one version (the oldest available)18 May 2012 |
| `ls-415-401/` | Organisationsreglement der Theologischen Fakultät der Universität Zürich (OrgR ThF) (LS 415.401) | 1 | as enacted1 July 2021 |
| `ls-415-403-1/` | Verordnung über die Promotion an der Theologischen und Religionswissenschaftlichen Fakultät der Universität Zürich (Promotionsverordnung) (LS 415.403.1) | 2 | as enacted, then each Nachtrag: 1 April 2010 to 1 August 2024 |
| `ls-415-405-1/` | Rahmenverordnung über die Bachelor- und Masterstudiengänge an der Theologischen und Religionswissenschaftlichen Fakultät der Universität Zürich (RVO TRF) (LS 415.405.1) | 3 | as enacted, then each Nachtrag: 1 August 2019 to 25 July 2024 |
| `ls-415-405-6/` | Rahmenverordnung für die Joint Degree Master-Studiengänge der Theologischen Fakultät der Universität Zürich in in- und ausländischen Partnerfakultäten (LS 415.405.6) | 1 | as enacted1 June 2010 |
| `ls-415-405-71/` | Rahmenverordnung über den Joint Degree Bachelorstudiengang in Sustainability an der Theologischen und Religionswissenschaftlichen Fakultät der Universität Zürich und den beteiligten Partneruniversitäten der Hochschulallianz Una Europa (RVO JD Sustainability TRF) (LS 415.405.71) | 1 | as enacted1 August 2025 |
| `ls-415-409/` | Verordnung über die Titularprofessur an der Theologischen Fakultät der Universität Zürich (TPV ThF) (LS 415.409) | 1 | as enacted1 May 2022 |
| `ls-415-411/` | Organisationsreglement der Rechtswissenschaftlichen Fakultät der Universität Zürich (OrgR RWF) (LS 415.411) | 2 | as enacted, then each Nachtrag: 1 February 2023 to 1 August 2025 |
| `ls-415-413/` | Verordnung über die Promotion zur Doktorin / zum Doktor der Rechtswissenschaft (Dr. iur.) an der Rechtswissenschaftlichen Fakultät der Universität Zürich (Promotionsverordnung) (LS 415.413) | 4 | as enacted, then each Nachtrag: 1 August 2009 to 1 August 2026 |
| `ls-415-415-1/` | Rahmenverordnung über den Bachelor- und den Masterstudiengang an der Rechtswissenschaftlichen Fakultät der Universität Zürich (RVO RWF) (LS 415.415.1) | 2 | as enacted, then each Nachtrag: 1 August 2021 to 1 August 2022 |
| `ls-415-415-7/` | Rahmenverordnung für die Double Degree Masterstudiengänge der Rechtswissenschaftlichen Fakultät der Universität Zürich und der ausländischen Partnerfakultäten (RVO DD RWF) (LS 415.415.7) | 1 | as enacted1 August 2021 |
| `ls-415-415-61/` | Rahmenverordnung für den zweisprachigen Joint Degree Masterstudiengang in Rechtswissenschaft der Fakultät der Rechts-, Kriminal- und Verwaltungswissenschaften der Universität Lausanne und der Rechtswissenschaftlichen Fakultät der Universität Zürich (RVO JD RWF) (LS 415.415.61) | 1 | as enacted1 August 2021 |
| `ls-415-416-3/` | Verordnung über die Weiterbildungsstudiengänge CAS und LL.M. im Bereich des Internationalen Wirtschaftsrechts an der Rechtswissenschaftlichen Fakultät der Universität Zürich (LS 415.416.3) | 1 | as enacted1 March 2019 |
| `ls-415-419/` | Verordnung über die Titularprofessur an der Rechtswissenschaftlichen Fakultät der Universität Zürich (TPV RWF) (LS 415.419) | 1 | as enacted1 February 2021 |
| `ls-415-421/` | Organisationsreglement der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (OrgR WWF) (LS 415.421) | 2 | as enacted, then each Nachtrag: 1 April 2021 to 1 October 2024 |
| `ls-415-423-11/` | Rahmenverordnung über die Bachelor- und Masterstudiengänge an der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (RVO WWF) (LS 415.423.11) | 1 | as enacted1 August 2022 |
| `ls-415-423-13/` | Promotionsverordnung über das Doktorat in Wirtschaftswissenschaften an der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (LS 415.423.13) | 1 | as enacted1 February 2013 |
| `ls-415-423-23/` | Promotionsverordnung über das Doktorat in Informatik an der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (LS 415.423.23) | 2 | as enacted, then each Nachtrag: 1 February 2009 to 1 May 2012 |
| `ls-415-423-33/` | Promotionsverordnung über das Doktorat in Neuroökonomie an der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (LS 415.423.33) | 2 | as enacted, then each Nachtrag: 1 January 2011 to 1 May 2012 |
| `ls-415-423-61/` | Rahmenverordnung über den Joint Degree Masterstudiengang «Quantitative Finance» an der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich und am Departement Mathematik der ETH Zürich (RVO MSc QF UZH ETH Zürich) (LS 415.423.61) | 1 | as enacted1 August 2022 |
| `ls-415-429/` | Verordnung über die Titularprofessur an der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (TPV WWF) (LS 415.429) | 1 | as enacted1 April 2021 |
| `ls-415-431/` | Organisationsreglement der Medizinischen Fakultät der Universität Zürich (OrgR MeF) (LS 415.431) | 1 | as enacted1 August 2021 |
| `ls-415-432/` | Verordnung über die Zulassungsbeschränkungen zu den medizinischen Studiengängen der Universität Zürich (VZMS) (LS 415.432) | 2 | as enacted, then each Nachtrag: 15 May 2020 to 1 February 2021 |
| `ls-415-433-1/` | Verordnung über die Promotion zur Doktorin oder zum Doktor der Medizin, der Zahnmedizin und der Chiropraktischen Medizin an der Medizinischen Fakultät der Universität Zürich (Promotionsverordnung Dr. med. / Dr. med. dent. / Dr. med. chiro.) (LS 415.433.1) | 2 | as enacted, then each Nachtrag: 1 August 2015 to 1 September 2020 |
| `ls-415-433-3/` | Verordnung über die Promotion zum Doctor scientiarum medicarum oder zum Doctor scientiarum medicarum dentium an der Medizinischen Fakultät der Universität Zürich (PromVO Dr. sc. med. / Dr. sc. med. dent.) (LS 415.433.3) | 2 | as enacted, then each Nachtrag: 1 February 2022 to 1 February 2026 |
| `ls-415-433-5/` | Rahmenverordnung über die Bachelor- und Masterstudiengänge an der Medizinischen Fakultät der Universität Zürich (RVO MeF) (LS 415.433.5) | 2 | as enacted, then each Nachtrag: 1 August 2020 to 1 August 2022 |
| `ls-415-433-91/` | Rahmenverordnung über den Joint Degree Masterstudiengang in Humanmedizin «Joint Medical Master» an der School of Medicine der Universität St. Gallen HSG und an der Medizinischen Fakultät der Universität Zürich (RVO JMM-HSG/UZH) (LS 415.433.91) | 1 | as enacted1 August 2020 |
| `ls-415-433-92/` | Rahmenverordnung über den Joint Degree Masterstudiengang in Humanmedizin «Joint Medical Master» am Departement Gesundheitswissenschaften und Medizin der Universität Luzern und an der Medizinischen Fakultät der Universität Zürich (RVO JMM-UniLU/UZH) (LS 415.433.92) | 1 | as enacted1 August 2020 |
| `ls-415-434/` | Verordnung über die Titularprofessur an der Medizinischen Fakultät der Universität Zürich (TPV MeF) (LS 415.434) | 2 | as enacted, then each Nachtrag: 1 July 2021 to 26 March 2024 |
| `ls-415-436/` | Reglement über die Verleihung des Titels «Klinische Dozentin» oder «Klinischer Dozent» an der Medizinischen Fakultät der Universität Zürich (LS 415.436) | 1 | as enacted1 August 2023 |
| `ls-415-437/` | Verordnung über das Zentrum für Zahnmedizin der Universität Zürich (V-ZZM) (LS 415.437) | 2 | as enacted, then each Nachtrag: 1 August 2023 to 26 January 2026 |
| `ls-415-439/` | Verordnung über das Institut für Rechtsmedizin der Universität Zürich (V-IRM) (LS 415.439) | 2 | as enacted, then each Nachtrag: 1 August 2025 to 26 January 2026 |
| `ls-415-439-1/` | Gebührenverordnung für das Institut für Medizinische Genetik der Universität Zürich (LS 415.439.1) | 1 | as enacted1 April 2020 |
| `ls-415-439-2/` | Gebührenverordnung der Institute für Medizinische Mikrobiologie und für Medizinische Virologie der Universität Zürich (LS 415.439.2) | 2 | as enacted, then each Nachtrag: 1 May 2014 to 24 July 2020 |
| `ls-415-439-3/` | Gebührenverordnung des Instituts für Rechtsmedizin der Universität Zürich (LS 415.439.3) | 1 | one version (the oldest available)1 October 2013 |
| `ls-415-439-4/` | Gebührenverordnung für das Zentrum für Reisemedizin am Institut für Epidemiologie, Biostatistik und Prävention der Universität Zürich (LS 415.439.4) | 1 | as enacted1 April 2020 |
| `ls-415-439-5/` | Gebührenverordnung für das Zentrum für Zahnmedizin der Universität Zürich (LS 415.439.5) | 1 | as enacted1 December 2018 |
| `ls-415-439-6/` | Gebührenverordnung für das Psychotherapeutische Zentrum des Psychologischen Instituts der Universität Zürich (LS 415.439.6) | 1 | as enacted1 January 2025 |
| `ls-415-441/` | Organisationsreglement der Vetsuisse-Fakultät der Universität Zürich (OrgR VSF) (LS 415.441) | 2 | as enacted, then each Nachtrag: 1 July 2022 to 1 November 2023 |
| `ls-415-443-1/` | Verordnung über die Promotion zum Doctor scientiarum medicarum veterinariarum (Dr. sc. med. vet.) an der Vetsuisse-Fakultät der Universität Zürich (Promotionsverordnung) (LS 415.443.1) | 1 | as enacted1 August 2017 |
| `ls-415-446/` | Verordnung über die Titularprofessur an der Vetsuisse-Fakultät der Universität Zürich (TPV VSF) (LS 415.446) | 1 | one version (the oldest available)24 September 2021 |
| `ls-415-447/` | Verordnung über das Tierspital der Vetsuisse-Fakultät der Universität Zürich (Tierspitalverordnung) (LS 415.447) | 1 | as enacted1 July 2019 |
| `ls-415-451/` | Organisationsreglement der Philosophischen Fakultät der Universität Zürich (OrgR PhF) (LS 415.451) | 2 | as enacted, then each Nachtrag: 1 August 2024 to 1 August 2025 |
| `ls-415-452/` | Verordnung über die Promotion an der Philosophischen Fakultät der Universität Zürich (PromVO PhF) (LS 415.452) | 1 | one version (the oldest available)1 January 2019 |
| `ls-415-455-1/` | Rahmenverordnung über die Bachelor- und Masterstudiengänge an der Philosophischen Fakultät der Universität Zürich (RVO PhF) (LS 415.455.1) | 3 | as enacted, then each Nachtrag: 1 August 2019 to 1 August 2025 |
| `ls-415-455-9/` | Rahmenverordnung über die Double Degree Masterstudiengänge an der Philosophischen Fakultät der Universität Zürichund an den ausländischen Partnerhochschulen (RVO DD PhF) (LS 415.455.9) | 1 | as enacted1 August 2026 |
| `ls-415-455-51/` | Rahmenverordnung über den hochschulübergreifenden Masterstudiengang «Filmwissenschaft» an der Philosophischen Fakultät der Universität Zürich (LS 415.455.51) | 1 | as enacted1 December 2013 |
| `ls-415-455-81/` | Rahmenverordnung über den Joint Degree Masterstudiengang «Comparative and International Studies» am Departement Geistes-, Sozial- und Staatswissenschaften der ETH Zürich und an der Philosophischen Fakultät der Universität Zürich (LS 415.455.81) | 1 | one version (the oldest available)20 October 2016 |
| `ls-415-455-82/` | Rahmenverordnung zum Joint Degree Masterstudiengang «Fachdidaktik Naturwissenschaften» an der Pädagogischen Hochschule Zürich, an der Philosophischen Fakultät der Universität Zürich und am Departement Geistes-, Sozial- und Staatswissenschaften der Eidgenössischen Technischen Hochschule Zürich (LS 415.455.82) | 1 | as enacted1 September 2011 |
| `ls-415-455-83/` | Rahmenverordnung zum Joint Degree Masterstudiengang «Fachdidaktik Schulsprache Deutsch» an der Pädagogischen Hochschule Zürich und an der Philosophischen Fakultät der Universität Zürich (LS 415.455.83) | 1 | as enacted1 August 2012 |
| `ls-415-455-84/` | Rahmenverordnung über den Joint Degree Masterstudiengang Fachdidaktik Ethik, Religionen, Gemeinschaft an der Pädagogischen Hochschule Zürich und an der Philosophischen Fakultät der Universität Zürich (RVO JD ERG PhF) (LS 415.455.84) | 1 | as enacted1 August 2024 |
| `ls-415-456-1/` | Rahmenverordnung über das «Lehrdiplom für Maturitätsschulen» an der Philosophischen Fakultät der Universität Zürich (RVO LfM) (LS 415.456.1) | 2 | as enacted, then each Nachtrag: 1 August 2021 to 1 February 2025 |
| `ls-415-456-2/` | Verordnung über die Organisation der Zusammenarbeit in der Lehrerinnen- und Lehrerbildung für Maturitätsschulen an der Universität Zürich (Organisationsverordnung LLBM) (LS 415.456.2) | 1 | one version (the oldest available)20 October 2016 |
| `ls-415-456-21/` | Reglement über die Entschädigung von Leistungen im Rahmen der Lehrerinnen- und Lehrerbildung für Maturitätsschulen (Entschädigungsreglement LLBM) (LS 415.456.21) | 1 | one version (the oldest available)20 October 2016 |
| `ls-415-459/` | Verordnung über die Titularprofessur an der Philosophischen Fakultät der Universität Zürich (TPV PhF) (LS 415.459) | 1 | as enacted1 April 2021 |
| `ls-415-461/` | Organisationsreglement der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich (OrgR MNF) (LS 415.461) | 1 | as enacted1 October 2025 |
| `ls-415-462/` | Rahmenverordnung für das Studium in den Bachelor- und Masterstudiengängen der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich (LS 415.462) | 2 | as enacted, then each Nachtrag: 1 August 2021 to 1 August 2022 |
| `ls-415-462-51/` | Rahmenverordnung über den Joint Degree Masterstudiengang «Neural Systems and Computation» an der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich und am Departement Informationstechnologie und Elektrotechnik der ETH Zürich (LS 415.462.51) | 1 | as enacted1 June 2014 |
| `ls-415-462-52/` | Rahmenverordnung über den Joint Degree Masterstudiengang «Computational Biology and Bioinformatics» am Departement Biosysteme der ETH Zürich und an der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich sowie an der Philosophisch-Naturwissenschaftlichen Fakultät der Universität Basel (LS 415.462.52) | 1 | one version (the oldest available)19 September 2017 |
| `ls-415-462-53/` | Rahmenverordnung über den Joint Degree Masterstudiengang in Interdisciplinary Brain Sciences an der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich und am Departement Gesundheitswissenschaften und Technologie der Eidgenössischen Technischen Hochschule Zürich (RVO UZH/ETH Zürich Joint MSc in Interdisciplinary Brain Sciences) (LS 415.462.53) | 1 | as enacted1 August 2022 |
| `ls-415-463/` | Verordnung über die Promotion an der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich (Promotionsverordnung) (LS 415.463) | 3 | as enacted, then each Nachtrag: 2 May 2011 to 1 January 2024 |
| `ls-415-463-1/` | Verordnung über die Promotion im gemeinsamen Doktorat der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich und der Eidgenössischen Technischen Hochschule Zürich (PromVO MNF ETHZ) (LS 415.463.1) | 1 | as enacted1 August 2019 |
| `ls-415-468/` | Verordnung über die Titularprofessur an der Mathematisch-naturwissenschaftlichen Fakultät der Universität Zürich (TPV MNF) (LS 415.468) | 1 | as enacted1 October 2021 |
| `ls-415-618/` | Verordnung über den Weiterbildungsstudiengang DAS in Psychotraumatologie an der Medizinischen Fakultät der Universität Zürich (LS 415.618) | 1 | as enacted1 June 2014 |
| `ls-415-621/` | Verordnung über die Weiterbildungsstudiengänge CAS, DAS und Executive Master in Arts Administration an der Philosophischen und der Wirtschaftswissenschaftlichen Fakultät der Universität Zürich (LS 415.621) | 1 | one version (the oldest available)19 December 2017 |
| `ls-415-629/` | Verordnung über die Weiterbildungsstudiengänge CAS, DAS und MAS in Parodontologie an der Medizinischen Fakultät der Universität Zürich (LS 415.629) | 1 | one version (the oldest available)24 May 2019 |
| `ls-415-634/` | Verordnung über den Weiterbildungsstudiengang DAS in Kognitiv-verhaltenstherapeutischer Supervision an der Philosophischen Fakultät der Universität Zürich (LS 415.634) | 1 | as enacted1 January 2019 |
| `ls-415-635/` | Verordnung über die Weiterbildungsstudiengänge CAS, DAS und Master in Public Health an den Medizinischen Fakultäten der Universitäten Basel, Bern und Zürich (LS 415.635) | 3 | as enacted, then each Nachtrag: 1 June 2011 to 1 June 2017 |
| `ls-415-638/` | Verordnung über die Weiterbildungsstudiengänge CAS, DAS und Executive Master in Art Market Studies an der Philosophischen Fakultät der Universität Zürich (LS 415.638) | 2 | as enacted, then each Nachtrag: 1 September 2011 to 1 July 2015 |
| `ls-415-644/` | Verordnung über die Weiterbildungsstudiengänge CAS in Organizational Health Development sowie CAS, DAS und MAS in Work + Health an der Medizinischen Fakultät der Universität Zürich und der Faculté de biologie et de médecine der Universität Lausanne (LS 415.644) | 1 | as enacted1 April 2015 |
| `ls-416-1/` | Verordnung über die Ausbildungsbeiträge (VAB) (LS 416.1) | 1 | as enacted1 January 2021 |
| `ls-431-11/` | Verordnung über das Amt für Statistik und Daten (VASD) (LS 431.11) | 1 | as enacted1 July 2026 |
| `ls-432-22/` | Bibliotheksförderungsverordnung (BFV) (LS 432.22) | 3 | as enacted, then each Nachtrag: 1 November 2011 to 1 January 2026 |
| `ls-440-11/` | Kulturförderungsverordnung (KFV) (LS 440.11) | 3 | as enacted, then each Nachtrag: 1 July 2010 to 1 July 2016 |
| `ls-522-1/` | Kantonale Zivilschutzverordnung (KZV) (LS 522.1) | 2 | as enacted, then each Nachtrag: 1 November 2008 to 1 January 2012 |
| `ls-528-1/` | Verordnung über den ABC-Schutz (ABCV) (LS 528.1) | 2 | as enacted, then each Nachtrag: 1 June 2025 to 1 June 2026 |
| `ls-550-12/` | Verordnung über die polizeiliche Überprüfung von Neuzuzugsmeldungen (VpÜN) (LS 550.12) | 1 | as enacted1 April 2018 |
| `ls-551-2/` | Kantonale Verordnung über Massnahmen zur Unterstützung der Sicherheit von Minderheiten mit besonderen Schutzbedürfnissen (KVSMS) (LS 551.2) | 2 | as enacted, then each Nachtrag: 1 October 2022 to 25 April 2024 |
| `ls-551-11/` | Kantonspolizeiverordnung (KapoV) (LS 551.11) | 14 | oldest version available, then each Nachtrag: 1 May 2006 to 1 July 2026 |
| `ls-551-12/` | Reglement über die Beförderungen bei der Kantonspolizei (LS 551.12) | 3 | oldest version available, then each Nachtrag: 1 May 2006 to 1 March 2011 |
| `ls-551-61/` | Organisationsreglement des Forensischen Instituts Zürich (LS 551.61) | 1 | as enacted1 January 2022 |
| `ls-551-64/` | Finanzreglement des Forensischen Instituts Zürich (LS 551.64) | 1 | as enacted1 January 2022 |
| `ls-551-65/` | Personalreglement des Forensischen Instituts Zürich (LS 551.65) | 1 | as enacted1 January 2022 |
| `ls-551-101/` | Verordnung über die kriminalpolizeiliche Aufgabenteilung (LS 551.101) | 1 | as enacted1 January 2006 |
| `ls-551-102/` | Verordnung über die Entschädigung für gemeindepolizeiliche Aufgaben (VEGPA) (LS 551.102) | 3 | as enacted, then each Nachtrag: 1 January 2006 to 1 July 2026 |
| `ls-551-103/` | Verordnung über das Polizei-Informationssystem POLIS (POLIS-Verordnung) (LS 551.103) | 7 | as enacted, then each Nachtrag: 1 January 2006 to 1 January 2022 |
| `ls-551-112/` | Verordnung über die erkennungsdienstliche Behandlung von Personen (LS 551.112) | 2 | as enacted, then each Nachtrag: 1 January 2006 to 1 January 2022 |
| `ls-551-191/` | Verordnung zum Vollzug der Massnahmen gegen Gewalt anlässlich von Sportveranstaltungen (LS 551.191) | 1 | as enacted1 August 2013 |
| `ls-552-1/` | Waffenverordnung (WafVO) (LS 552.1) | 3 | oldest version available, then each Nachtrag: 1 May 2006 to 1 January 2020 |
| `ls-552-5/` | Kantonale Sprengstoffverordnung (KSprstV) (LS 552.5) | 3 | as enacted, then each Nachtrag: 1 March 2011 to 1 January 2024 |
| `ls-553-1/` | Kantonale Geldspielverordnung (KGSV) (LS 553.1) | 1 | as enacted1 January 2022 |
| `ls-554-11/` | Kantonale Tierschutzverordnung (KTSchV) (LS 554.11) | 3 | oldest version available, then each Nachtrag: 1 January 2005 to 1 June 2018 |
| `ls-554-51/` | Hundeverordnung (HuV) (LS 554.51) | 4 | as enacted, then each Nachtrag: 1 January 2010 to 1 June 2025 |
| `ls-611-1/` | Rechnungslegungsverordnung (RLV) (LS 611.1) | 6 | oldest version available, then each Nachtrag: 1 April 2008 to 1 January 2022 |
| `ls-611-2/` | Finanzcontrollingverordnung (FCV) (LS 611.2) | 15 | as enacted, then each Nachtrag: 1 April 2008 to 1 January 2023 |
| `ls-612-1/` | Verordnung über den Gemeinnützigen Fonds (VGF) (LS 612.1) | 1 | as enacted1 January 2021 |
| `ls-612-2/` | Sportfondsverordnung (SfV) (LS 612.2) | 1 | as enacted1 January 2021 |
| `ls-612-3/` | Kulturfondsverordnung (KufV) (LS 612.3) | 1 | one version (the oldest available)26 February 2021 |
| `ls-612-4/` | Denkmalpflegefondsverordnung (DPFV) (LS 612.4) | 1 | as enacted1 March 2022 |
| `ls-631-11/` | Verordnung zum Steuergesetz (StV) (LS 631.11) | 5 | oldest version available, then each Nachtrag: 1 August 2010 to 1 February 2020 |
| `ls-631-19/` | Verordnung über den Vollzug des Unternehmenssteuerreformgesetzes II des Bundes (LS 631.19) | 1 | as enacted1 January 2011 |
| `ls-631-41/` | Verordnung über die Quellensteuer für ausländische Arbeitnehmer (Quellensteuerverordnung I) (LS 631.41) | 3 | oldest version available, then each Nachtrag: 1 August 2010 to 1 January 2021 |
| `ls-631-42/` | Verordnung über die Quellensteuer für natürliche und juristische Personen ohne steuerrechtlichen Wohnsitz oder Aufenthalt in der Schweiz (Quellensteuerverordnung II) (LS 631.42) | 4 | as enacted, then each Nachtrag: 1 January 1995 to 1 January 2021 |
| `ls-631-43/` | Verordnung über die elektronische Einreichung von Quellensteuerdaten (LS 631.43) | 1 | as enacted1 January 2015 |
| `ls-631-51/` | Verordnung über die Organisation des kantonalen Steueramtes (OV KStA) (LS 631.51) | 1 | as enacted1 June 2024 |
| `ls-631-121/` | Verordnung über die elektronische Einreichung der Steuererklärung (LS 631.121) | 3 | oldest version available, then each Nachtrag: 1 January 2012 to 1 July 2025 |
| `ls-631-122/` | Verordnung über die elektronische Zustellung von Verfügungen und Rechnungen (LS 631.122) | 1 | as enacted1 December 2012 |
| `ls-631-421/` | Verordnung der Finanzdirektion über die Tarife für quellensteuerpflichtige Arbeitnehmerinnen und Arbeitnehmer (LS 631.421) | 3 | as enacted, then each Nachtrag: 1 January 2021 to 26 January 2026 |
| `ls-631-423/` | Verordnung der Finanzdirektion über die Steuerfreibeträge von quellensteuerpflichtigen Personen ohne steuerrechtlichen Wohnsitz oder Aufenthalt in der Schweiz (LS 631.423) | 1 | as enacted1 January 2021 |
| `ls-631-424/` | Verordnung über die Bezugsprovision im Quellensteuerverfahren (LS 631.424) | 1 | as enacted1 January 2021 |
| `ls-632-11/` | Verordnung zum Erbschafts- und Schenkungssteuergesetz (LS 632.11) | 1 | one version (the oldest available)1 August 2010 |
| `ls-634-1/` | Verordnung über die Durchführung des Bundesgesetzes über die direkte Bundessteuer (LS 634.1) | 6 | oldest version available, then each Nachtrag: 1 August 2010 to 1 June 2024 |
| `ls-634-2/` | Verordnung über die Rückerstattung der Verrechnungssteuer (LS 634.2) | 4 | oldest version available, then each Nachtrag: 1 August 2010 to 1 January 2017 |
| `ls-634-3/` | Verordnung über die Durchführung der Anrechnung ausländischer Quellensteuern (LS 634.3) | 4 | oldest version available, then each Nachtrag: 1 July 2004 to 1 January 2020 |
| `ls-634-5/` | Kantonale Verordnung über die Wehrpflichtersatzabgabe (KWPEV) (LS 634.5) | 2 | as enacted, then each Nachtrag: 1 July 2004 to 1 July 2010 |
| `ls-634-41/` | Verordnung über die Rückerstattung des zusätzlichen Steuerrückbehaltes auf Dividenden und Zinsen von amerikanischen Gesellschaften und Obligationenschuldnern (LS 634.41) | 1 | one version (the oldest available)1 January 2014 |
| `ls-700-2/` | Allgemeine Bauverordnung (ABV) (LS 700.2) | 5 | oldest version available, then each Nachtrag: 1 January 2004 to 1 December 2024 |
| `ls-700-3/` | Sondergebrauchsverordnung (SGV) (LS 700.3) | 3 | oldest version available, then each Nachtrag: 1 November 2011 to 1 April 2019 |
| `ls-700-5/` | Verordnung über den Bahntransport von Aushub und Gesteinskörnung (BTV) (LS 700.5) | 1 | as enacted1 July 2021 |
| `ls-700-7/` | Organisationsverordnung des Baurekursgerichts (OV BRG) (LS 700.7) | 1 | as enacted1 January 2011 |
| `ls-700-8/` | Verordnung über den preisgünstigen Wohnraum (PWV) (LS 700.8) | 2 | as enacted, then each Nachtrag: 1 November 2019 to 1 February 2022 |
| `ls-700-22/` | Besondere Bauverordnung II (BBV II) (LS 700.22) | 2 | oldest version available, then each Nachtrag: 1 November 2009 to 14 May 2019 |
| `ls-700-91/` | Mehrwertausgleichsverordnung (MAV) (LS 700.91) | 1 | as enacted1 January 2021 |
| `ls-701-12/` | Verordnung über die Darstellung von Nutzungsplänen (VDNP) (LS 701.12) | 3 | as enacted, then each Nachtrag: 1 August 2016 to 1 December 2024 |
| `ls-701-13/` | Quartierplanverordnung (QPV) (LS 701.13) | 3 | oldest version available, then each Nachtrag: 1 January 2011 to 1 June 2026 |
| `ls-702-12/` | Verordnung über den Pflanzenschutz (LS 702.12) | 1 | one version (the oldest available)1 November 2011 |
| `ls-702-13/` | Verordnung zum Schutze der einheimischen Tier- und Pflanzenwelt (LS 702.13) | 1 | one version (the oldest available)1 November 2011 |
| `ls-702-15/` | Pilzschutzverordnung (LS 702.15) | 2 | oldest version available, then each Nachtrag: 15 May 2006 to 1 November 2011 |
| `ls-702-111/` | Verordnung über die Sachverständigenkommissionen gemäss § 216 PBG (VSVK) (LS 702.111) | 5 | oldest version available, then each Nachtrag: 18 February 2005 to 1 October 2026 |
| `ls-702-332/` | Verordnung zum Schutze des Landschaftsbildes am Albispass (LS 702.332) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-411/` | Verordnung zum Schutze des Landschaftsbildes beim Wehrmännerdenkmal Forch (LS 702.411) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-422/` | Verordnung zum Schutze des Lützelsees, des Seeweidsees und des Uetzikerrietes (LS 702.422) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-541/` | Verordnung zum Schutze des Orts- und Landschaftsbildes Ellikon am Rhein (LS 702.541) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-581/` | Verordnung zum Schutze des Landschaftsbildes beim Rheinfall (LS 702.581) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-615/` | Verordnung zum Schutze des Eigentales (LS 702.615) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-625/` | Verordnung zum Schutze des Bachsertales (LS 702.625) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-651/` | Verordnung zum Schutze des Neeracherriedes (LS 702.651) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-702-665/` | Verordnung zum Schutze des Orts- und Landschaftsbildes von Regensberg (LS 702.665) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 January 2018 |
| `ls-704-11/` | Kantonale Geoinformationsverordnung (KGeoIV) (LS 704.11) | 8 | as enacted, then each Nachtrag: 1 November 2012 to 1 June 2026 |
| `ls-704-12/` | Kantonale Verordnung über die amtliche Vermessung (KVAV) (LS 704.12) | 2 | as enacted, then each Nachtrag: 1 November 2012 to 1 January 2018 |
| `ls-704-13/` | Kantonale Verordnung über den Kataster der öffentlich-rechtlichen Eigentumsbeschränkungen (KÖREBKV) (LS 704.13) | 2 | as enacted, then each Nachtrag: 1 November 2012 to 1 January 2018 |
| `ls-704-14/` | Leitungskatasterverordnung (LKV) (LS 704.14) | 1 | as enacted1 May 2022 |
| `ls-704-15/` | Gebührenverordnung für Geodaten (GebV GeoD) (LS 704.15) | 1 | as enacted1 January 2018 |
| `ls-704-16/` | Verordnung über das Gebäude- und Wohnungsregister und die Datenlogistik (GWDV) (LS 704.16) | 2 | oldest version available, then each Nachtrag: 17 April 2014 to 1 February 2022 |
| `ls-710-2/` | Gebührenverordnung zum Vollzug des Umweltrechts (GebV UR) (LS 710.2) | 1 | one version (the oldest available)1 November 2011 |
| `ls-710-3/` | Verordnung über allgemeine und Wohnhygiene (LS 710.3) | 1 | one version (the oldest available)1 November 2011 |
| `ls-710-5/` | Einführungsverordnung über die Umweltverträglichkeitsprüfung (EV UVP) (LS 710.5) | 1 | as enacted1 January 2012 |
| `ls-710-6/` | Verordnung über den Vollzug der Störfallverordnung (LS 710.6) | 1 | one version (the oldest available)1 January 2012 |
| `ls-712-11/` | Abfallverordnung (AbfV) (LS 712.11) | 2 | oldest version available, then each Nachtrag: 25 January 2014 to 1 June 2018 |
| `ls-712-12/` | Deponienachsorgeverordnung (DeNaV) (LS 712.12) | 1 | as enacted1 January 2020 |
| `ls-712-41/` | Sonderabfall-Abgabeverordnung (LS 712.41) | 3 | oldest version available, then each Nachtrag: 1 July 2003 to 1 November 2011 |
| `ls-713-12/` | SMOG-Verordnung (LS 713.12) | 2 | as enacted, then each Nachtrag: 1 January 2007 to 1 November 2011 |
| `ls-715-1/` | Verordnung über den Vollzug der Chemikaliengesetzgebung (VVChem) (LS 715.1) | 5 | as enacted, then each Nachtrag: 1 July 2007 to 1 January 2024 |
| `ls-720-11/` | Submissionsverordnung (SVO) (LS 720.11) | 2 | as enacted, then each Nachtrag: 1 October 2023 to 1 January 2026 |
| `ls-721-1/` | Immobilienverordnung (ImV) (LS 721.1) | 3 | oldest version available, then each Nachtrag: 22 February 2019 to 1 January 2024 |
| `ls-722-11/` | Verordnung über die Beiträge an den Unterhalt der Gemeindestrassen (VBUG) (LS 722.11) | 1 | as enacted1 June 2022 |
| `ls-722-61/` | Verordnung über das Gesamtverkehrsmodell (GVMV) (LS 722.61) | 2 | as enacted, then each Nachtrag: 1 August 2015 to 1 January 2021 |
| `ls-725-11/` | Verordnung über die Nutzung des Untergrundes (VNU) (LS 725.11) | 1 | as enacted1 July 2023 |
| `ls-730-11/` | Energieverordnung (EnerV) (LS 730.11) | 2 | oldest version available, then each Nachtrag: 1 November 2011 to 1 June 2013 |
| `ls-732-11/` | Verordnung über die Organisation und Verwaltung der Elektrizitätswerke des Kantons Zürich (EKZ-Verordnung) (LS 732.11) | 2 | oldest version available, then each Nachtrag: 1 July 2019 to 1 October 2025 |
| `ls-740-3/` | Verordnung über das Angebot im öffentlichen Personenverkehr (Angebotsverordnung) (LS 740.3) | 2 | oldest version available, then each Nachtrag: 1 March 2009 to 1 July 2017 |
| `ls-740-4/` | Geschäftsreglement des Verkehrsverbundes des Kantons Zürich (GR-ZVV) (LS 740.4) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 September 2019 |
| `ls-740-7/` | Verordnung über die Beteiligung der Gemeinden an der Einlage des Kantons in den Bahninfrastrukturfonds des Bundes (VB BIF) (LS 740.7) | 1 | as enacted1 January 2019 |
| `ls-740-35/` | Fahrplanverfahrensverordnung (FVV) (LS 740.35) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 April 2025 |
| `ls-741-2/` | Kantonale Signalisationsverordnung (KSigV) (LS 741.2) | 5 | oldest version available, then each Nachtrag: 1 May 2006 to 1 June 2026 |
| `ls-741-4/` | Verordnung über die Bezeichnung der für den Vollzug der ARV 1 und ARV 2 zuständigen Behörden (LS 741.4) | 2 | oldest version available, then each Nachtrag: 1 May 2006 to 1 July 2010 |
| `ls-743-2/` | Einführungsverordnung zur Seilbahnverordnung (ESebV) (LS 743.2) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2021 |
| `ls-744-11/` | Kantonale Personenbeförderungsverordnung (KPBV) (LS 744.11) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2021 |
| `ls-747-4/` | Schiffsstationierungsverordnung (SchSV) (LS 747.4) | 5 | oldest version available, then each Nachtrag: 1 May 2006 to 1 June 2026 |
| `ls-747-121/` | Schiffssteuerverordnung (LS 747.121) | 2 | oldest version available, then each Nachtrag: 1 July 2003 to 1 July 2010 |
| `ls-748-2/` | Verordnung zum Luftfahrtrecht des Bundes (VLB) (LS 748.2) | 2 | as enacted, then each Nachtrag: 1 July 2012 to 1 January 2021 |
| `ls-748-15/` | Verordnung zum Zürcher Fluglärm-Index (ZFI-VO) (LS 748.15) | 2 | oldest version available, then each Nachtrag: 1 March 2012 to 1 January 2021 |
| `ls-754-2/` | Verordnung über die Top Level Domain «.zuerich» (TLDV) (LS 754.2) | 1 | as enacted1 January 2021 |
| `ls-781-1/` | Verordnung betreffend das Administrativverfahren bei Abtretung von Privatrechten (LS 781.1) | 2 | as enacted, then each Nachtrag: 6 March 1880 to 1 January 2018 |
| `ls-781-2/` | Verordnung über das Verfahren der Schätzungskommissionen in Abtretungsstreitigkeiten (LS 781.2) | 1 | one version (the oldest available)1 January 2011 |
| `ls-810-11/` | Verordnung über die Bezirksärztinnen und Bezirksärzte (VBÄ) (LS 810.11) | 1 | as enacted1 June 2026 |
| `ls-811-11/` | Verordnung über die universitären Medizinalberufe (MedBV) (LS 811.11) | 7 | as enacted, then each Nachtrag: 1 July 2008 to 1 January 2025 |
| `ls-811-21/` | Verordnung über die nichtuniversitären Medizinalberufe (nuMedBV) (LS 811.21) | 1 | as enacted1 March 2011 |
| `ls-811-41/` | Verordnung zum EG Ausbildungsfördergesetz Pflege (VEG AFP) (LS 811.41) | 1 | one version (the oldest available)21 February 2025 |
| `ls-811-42/` | Verordnung über Förderbeiträge an Auszubildende im Bereich der Pflege (VFAP) (LS 811.42) | 1 | one version (the oldest available)21 February 2025 |
| `ls-811-43/` | Einführungsverordnung zum Bundesgesetz über die Förderung der Ausbildung im Bereich der Pflege für die Institutionen des Gesundheitswesens (EV Ausbildungsfördergesetz Pflege für die Institutionen des Gesundheitswesens, EV APIG) (LS 811.43) | 1 | as enacted1 April 2025 |
| `ls-811-61/` | Verordnung über die psychologischen Psychotherapeutinnen und -therapeuten (PPsyV) (LS 811.61) | 1 | as enacted1 May 2014 |
| `ls-812-1/` | Heilmittelverordnung (HMV) (LS 812.1) | 1 | as enacted1 July 2023 |
| `ls-812-4/` | Verordnung über die Kantonale Ethikkommission (KEKV) (LS 812.4) | 1 | as enacted1 October 2021 |
| `ls-813-11/` | Verordnung über die kantonalen psychiatrischen Spitäler (VPS) (LS 813.11) | 1 | as enacted1 January 2010 |
| `ls-813-12/` | Verordnung über die Spitalräte (SRV) (LS 813.12) | 1 | one version (the oldest available)21 February 2022 |
| `ls-813-31/` | Verordnung über das Rettungswesen (RWV) (LS 813.31) | 2 | as enacted, then each Nachtrag: 1 July 2018 to 1 August 2019 |
| `ls-813-42/` | Spitalärzteverordnung (LS 813.42) | 1 | as enacted1 January 2010 |
| `ls-813-111/` | Verordnung über Leistungen und Gebühren der kantonalen Spitäler (Taxordnung) (LS 813.111) | 2 | as enacted, then each Nachtrag: 1 January 2005 to 1 January 2008 |
| `ls-813-152/` | Personalreglement des Universitätsspitals Zürich (PR-USZ) (LS 813.152) | 7 | as enacted, then each Nachtrag: 1 February 2009 to 1 March 2026 |
| `ls-813-155-1/` | Vollzugsverordnung zur Taxordnung des Universitätsspitals Zürich (VVO TO USZ) (LS 813.155.1) | 1 | as enacted1 August 2024 |
| `ls-813-162/` | Personalreglement des Kantonsspitals Winterthur (PR-KSW) (LS 813.162) | 5 | as enacted, then each Nachtrag: 1 September 2010 to 1 January 2025 |
| `ls-813-163/` | Finanzreglement des Kantonsspitals Winterthur (FinReg-KSW) (LS 813.163) | 1 | as enacted1 September 2010 |
| `ls-813-172/` | Personalreglement der Psychiatrischen Universitätsklinik Zürich (PR-PUK) (LS 813.172) | 3 | as enacted, then each Nachtrag: 1 January 2023 to 1 May 2025 |
| `ls-813-182/` | Personalreglement der Integrierten Psychiatrie Winterthur &#8211; Zürcher Unterland (PR-ipw) (LS 813.182) | 2 | oldest version available, then each Nachtrag: 23 September 2022 to 1 October 2025 |
| `ls-813-205/` | Verordnung über die Umwandlung von Investitionsbeiträgen an Spitäler (InUV) (LS 813.205) | 1 | as enacted1 January 2012 |
| `ls-813-206/` | Verordnung zur Förderung ambulanter Behandlungen (LS 813.206) | 2 | as enacted, then each Nachtrag: 1 January 2018 to 1 January 2019 |
| `ls-813-211/` | Wohnsitzprüfungsverordnung (WPV) (LS 813.211) | 5 | as enacted, then each Nachtrag: 1 May 2014 to 1 July 2026 |
| `ls-817-1/` | Vollzugsverordnung zur Lebensmittel- und Gebrauchsgegenständegesetzgebung (VVLG) (LS 817.1) | 1 | as enacted1 January 2020 |
| `ls-818-11/` | Vollzugsverordnung zur eidgenössischen Epidemiengesetzgebung (VV EpiG) (LS 818.11) | 2 | oldest version available, then each Nachtrag: 1 January 2011 to 1 August 2020 |
| `ls-818-15/` | Rahmenverordnung über die Durchführung von Online-Prüfungen an der Universität Zürich während der Covid-19-Pandemie (Covid-19-RVO Online-Prüfungen) (LS 818.15) | 2 | as enacted, then each Nachtrag: 1 January 2021 to 1 February 2022 |
| `ls-818-22/` | Verordnung über die Schul- und Volkszahnpflege (VSVZ) (LS 818.22) | 1 | one version (the oldest available)1 January 2012 |
| `ls-818-25/` | Verordnung über die Bekämpfung des Suchtmittelmissbrauchs (LS 818.25) | 1 | as enacted1 July 2008 |
| `ls-818-32/` | Vollzugsverordnung zur Tabakproduktegesetzgebung (VV TPG) (LS 818.32) | 1 | as enacted1 November 2025 |
| `ls-818-61/` | Bestattungsverordnung (BesV) (LS 818.61) | 2 | as enacted, then each Nachtrag: 1 January 2016 to 1 December 2017 |
| `ls-821-11/` | Vollzugsverordnung über die Allgemeinverbindlicherklärung von Gesamtarbeitsverträgen (LS 821.11) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2024 |
| `ls-822-1/` | Verordnung zum Arbeitsgesetz (LS 822.1) | 2 | oldest version available, then each Nachtrag: 1 July 2010 to 1 January 2024 |
| `ls-822-41/` | Verordnung zum Ruhetags- und Ladenöffnungsgesetz (LS 822.41) | 1 | one version (the oldest available)1 March 2015 |
| `ls-823-44/` | Vollzugsverordnung zum Bundesgesetz gegen die Schwarzarbeit (VVSA) (LS 823.44) | 2 | as enacted, then each Nachtrag: 1 January 2008 to 1 January 2024 |
| `ls-831-31/` | Zusatzleistungsverordnung (ZLV) (LS 831.31) | 9 | as enacted, then each Nachtrag: 1 January 2008 to 1 January 2025 |
| `ls-831-51/` | Verordnung über den selbstbestimmten Leistungsbezug durch Menschen mit Behinderung (Selbstbestimmungsverordnung, SLBV) (LS 831.51) | 2 | as enacted, then each Nachtrag: 1 January 2024 to 1 January 2026 |
| `ls-832-1/` | Verordnung zum EG KVG (VEG KVG) (LS 832.1) | 1 | one version (the oldest available)9 April 2020 |
| `ls-832-21/` | Vollzugsverordnung zur Bundesgesetzgebung über die Unfallversicherung (VV UVG) (LS 832.21) | 2 | as enacted, then each Nachtrag: 1 January 2011 to 1 January 2024 |
| `ls-836-11/` | Verordnung zum EG FamZG (LS 836.11) | 4 | as enacted, then each Nachtrag: 1 July 2009 to 1 January 2021 |
| `ls-837-11/` | Verordnung zum Einführungsgesetz zum Arbeitslosenversicherungsgesetz (VO EG AVIG) (LS 837.11) | 2 | as enacted, then each Nachtrag: 1 July 2013 to 1 January 2024 |
| `ls-837-15/` | Verordnung über die Übertragung von Aufgaben der Kantonalen Amtsstelle an die Regionalen Arbeitsvermittlungszentren und an die Logistik-Stelle für arbeitsmarktliche Massnahmen (Delegationsverordnung AVIG; DVO AVIG) (LS 837.15) | 1 | as enacted1 January 2007 |
| `ls-851-11/` | Verordnung zum Sozialhilfegesetz (SHV) (LS 851.11) | 22 | oldest version available, then each Nachtrag: 1 April 2005 to 1 January 2026 |
| `ls-851-13/` | Asylfürsorgeverordnung (AfV) (LS 851.13) | 9 | as enacted, then each Nachtrag: 1 July 2005 to 1 January 2025 |
| `ls-851-14/` | Verordnung über die Gewährung von Nothilfe an Personen ohne Aufenthaltsrecht (Nothilfeverordnung) (LS 851.14) | 3 | as enacted, then each Nachtrag: 1 January 2008 to 9 April 2020 |
| `ls-852-12/` | Verordnung über die sonderpädagogischen Massnahmen im Vor- und Nachschulbereich (SPMV) (LS 852.12) | 10 | as enacted, then each Nachtrag: 1 January 2012 to 26 January 2026 |
| `ls-852-13/` | Verordnung über die Alimentenhilfe (AlimV) (LS 852.13) | 6 | as enacted, then each Nachtrag: 1 January 2013 to 1 October 2025 |
| `ls-852-14/` | Verordnung über die Tagesfamilien und Kindertagesstätten (V TaK) (LS 852.14) | 2 | as enacted, then each Nachtrag: 1 August 2020 to 1 January 2025 |
| `ls-852-17/` | Verordnung über die Kindesschutzkommission (VKSK) (LS 852.17) | 1 | as enacted1 July 2012 |
| `ls-852-22/` | Verordnung über abweichende Aufbewahrungsfristen im Bereich der ergänzenden Hilfen zur Erziehung (LS 852.22) | 1 | as enacted1 June 2025 |
| `ls-855-11/` | Verordnung über die Pflegeversorgung (LS 855.11) | 2 | as enacted, then each Nachtrag: 1 March 2011 to 1 July 2013 |
| `ls-855-12/` | Verordnung über die Ausbildungspflicht in der Langzeitpflege (ALV) (LS 855.12) | 2 | oldest version available, then each Nachtrag: 22 February 2019 to 1 January 2022 |
| `ls-855-21/` | Verordnung über den Transport von mobilitätsbehinderten Personen (TMV) (LS 855.21) | 6 | as enacted, then each Nachtrag: 1 January 2008 to 1 January 2024 |
| `ls-857-5/` | Verordnung zur Bundesgesetzgebung über die Schwangerschaftsberatungsstellen (LS 857.5) | 1 | one version (the oldest available)1 January 2011 |
| `ls-857-6/` | Verordnung zum Bundesgesetz über genetische Untersuchungen beim Menschen (LS 857.6) | 2 | as enacted, then each Nachtrag: 1 April 2007 to 1 January 2011 |
| `ls-861-2/` | Feuerwehrverordnung (LS 861.2) | 2 | as enacted, then each Nachtrag: 1 June 2009 to 1 April 2018 |
| `ls-861-21/` | Verordnung über die Subventionen der Gebäudeversicherung an den Brandschutz (VSGB) (LS 861.21) | 6 | oldest version available, then each Nachtrag: 1 January 2004 to 1 April 2020 |
| `ls-862-111/` | Geschäftsreglement für die Gebäudeversicherung (LS 862.111) | 1 | one version (the oldest available)31 May 2009 |
| `ls-901-21/` | Verordnung zum Gesetz über die steuerbegünstigten Arbeitsbeschaffungsreserven (LS 901.21) | 1 | one version (the oldest available)1 October 2003 |
| `ls-910-11/` | Landwirtschaftsverordnung (LV) (LS 910.11) | 1 | as enacted1 January 2020 |
| `ls-915-11/` | Landwirtschaftliche Bildungsverordnung (LBV) (LS 915.11) | 2 | oldest version available, then each Nachtrag: 15 May 2006 to 1 November 2011 |
| `ls-916-22/` | Kantonale Tierseuchenverordnung (KTSV) (LS 916.22) | 1 | as enacted1 January 2014 |
| `ls-921-11/` | Kantonale Waldverordnung (KWaV) (LS 921.11) | 2 | oldest version available, then each Nachtrag: 1 April 2013 to 1 January 2023 |
| `ls-922-11/` | Kantonale Jagdverordnung (JV) (LS 922.11) | 2 | as enacted, then each Nachtrag: 1 January 2023 to 1 September 2025 |
| `ls-923-11/` | Fischereiverordnung (LS 923.11) | 2 | as enacted, then each Nachtrag: 1 January 2009 to 1 November 2012 |
| `ls-935-12/` | Verordnung zum Gastgewerbegesetz (LS 935.12) | 2 | oldest version available, then each Nachtrag: 1 May 2010 to 26 January 2018 |
| `ls-935-22/` | Verordnung über den Jugendschutz bei öffentlichen Filmvorführungen und Trägermedien (JFTV) (LS 935.22) | 1 | as enacted1 July 2019 |
| `ls-935-511/` | Verordnung über den Personentransport mit Taxis und Limousinen (PTLV) (LS 935.511) | 2 | as enacted, then each Nachtrag: 1 January 2024 to 1 June 2025 |
| `ls-935-512/` | Reglement über die Vorgaben zur kantonalen Taxilampe (LS 935.512) | 1 | as enacted1 January 2024 |
| `ls-935-513/` | Reglement über die Vorgaben zur kantonalen Limousinenplakette (LS 935.513) | 1 | as enacted1 January 2024 |
| `ls-941-1/` | Verordnung über das Messwesen (LS 941.1) | 4 | oldest version available, then each Nachtrag: 1 May 2006 to 1 November 2018 |
| `ls-951-11/` | Reglement über die Vorbereitung der Wahl neuer Mitglieder des Bankrates und des Bankpräsidiums der Zürcher Kantonalbank (LS 951.11) | 1 | as enacted1 June 2022 |
| `ls-951-12/` | Reglement über die Entschädigungen der Mitglieder des Bankrates der Zürcher Kantonalbank (LS 951.12) | 1 | as enacted1 January 2005 |
| `ls-951-14/` | Reglement über die Entschädigung der Staatsgarantie durch die Zürcher Kantonalbank (LS 951.14) | 1 | one version (the oldest available)19 October 2015 |
| `ls-954-2/` | Verordnung zum Konsumkreditgesetz (LS 954.2) | 2 | as enacted, then each Nachtrag: 1 July 2004 to 1 January 2024 |
| `ls-954-3/` | Verordnung über die Pfandleiher (LS 954.3) | 2 | oldest version available, then each Nachtrag: 1 May 2006 to 1 July 2010 |

## Source

The Zürcher Loseblattsammlung (LS) in ZH-Lex, the canton's collection of its law in force, at <https://www.zh.ch/de/politik-staat/gesetze-beschluesse/gesetzessammlung.html>. For each act ZH-Lex lists every Nachtrag (each reissue of the act after an amendment) with its date and links the Nachtrag's text as a PDF. The endnotes of each PDF name, for every amended provision, the amending act, its entry in the Official Compilation (OS) and the day it took effect.

## Dates

- Each commit is dated at **noon, Europe/Zurich, on the day ZH-Lex gives for the Nachtrag**, which is the day the amendments it incorporates took effect. The decision date of each amending act is the `Enacted:` trailer.
- An act's first commit is the oldest Nachtrag of the act in force today. It is credited to the act as enacted when it is the act's first Nachtrag and dated the day the act took effect; otherwise it is the "oldest version available".
- `--before="YYYY-MM-DD"` alone uses your clock's time of day; use `T23:59:59Z` or `tools/on.py`.

## Files

`<act>/art-005.md` is Art. 5 (or § 5), `art-005a.md` Art. 5a; the first line holds the article's margin title. `ingress.md` holds the title, date and preamble; `gliederung.md` the section headings; `abschnitt-*.md` text printed under a heading with no article (such as transitional provisions of an amendment). One paragraph or list item per line. Note references, running heads, page numbers and the endnotes are left out.

## How it is checked

- Every version of every act is read back from git on the day it took effect and on the day before (`tools/check_repo.py`); both must match `corpus.json`.
- The letters and digits of every version equal those of the text layer of that Nachtrag's PDF (read span by span, less running heads, page numbers, note references and endnotes).
- Health checks: no merge commits, commit dates never go backwards, nothing dated in the future, and every commit's trailers parse.

## What "author" means

The author of a commit is the amending act, named by its entry in the Official Compilation (`OS <volume>, <page>`), with an e-mail address that cannot exist (`<act key>@zh.ch.invalid`). A change is credited to the act named in the endnote of the changed provision; where no endnote of that provision names an act taking effect in that window, every act whose endnote gives an in-force day in the window is named; where there is none, the change is unexplained and committed by the publisher. The committer is always Lexifina.

## Limits

This is not an official publication; the binding text is the one in the canton's official publications. The history starts with the oldest Nachtrag ZH-Lex links as a PDF for the act in force today, so older versions of an act (before a total revision, such as the constitution of 1869) are not included. Only the acts listed above are included.
