---
<<<<<<< HEAD-Titel: Verwenden von ActiveX Data-Objekte TOCTitle: Verwenden von ActiveX Data Objects Ms:assetid: 64055c45-7a27-2296-468a-015362898329 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) Ms:contentKeyID: 48545279 ms.date: 09/18/2015 === Titel: Verwenden von ActiveX Data-Objekte TOCTitle: Verwendung ActiveX Data Objects Beschreibung: Microsoft Access enthält drei-Objektmodellen verwendet bei der Erstellung, warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.
MS:AssetId: 64055c45-7a27-2296-468a-015362898329 Ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) Ms:contentKeyID: 48545279 ms.date: 10/16/2018
>>>>>>> Master-Shape Mtps_version: Office. 15 f1_keywords:
- vbaac10.chm5285627 f1_categories:
- Office.Version=v15
---

<<<<<<< Kopf
# <a name="using-activex-data-objects"></a>Verwenden von ActiveX Data Objects (ADO)


**Betrifft**: Access 2013 | Office 2013

<a name="microsoft-access-provides-three-object-models-to-use-in-the-creation-maintaining-and-managing-of-your-access-databases-and-their-related-data-by-using-visual-basic"></a>Microsoft Access enthält drei Objektmodelle, die Sie beim Erstellen, Warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mit Visual Basic verwenden können.
=======
# <a name="use-activex-data-objects"></a>Verwenden von ActiveX Data Objects

**Betrifft**: Access 2013 | Office 2013

Microsoft Access enthält drei Objektmodelle, verwenden Sie bei der Erstellung, warten und Verwalten Ihrer Access-Datenbanken und der zugehörigen Daten mithilfe von Visual Basic.
>>>>>>> master

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data-Objekte (ADO)

ADO enthält die Objekte, die zum Erstellen, Pflegen und Löschen von Datensätzen in einer bestimmten Datenquelle erforderlich sind.

<<<<<<< Kopf
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext. for DDL and Security (ADOX)

ADOX stellt die DDL (Data Definition Language)-Objekte bereit, die zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den zum Verwalten der Zugriffsrechte benötigten Objekten erforderlich sind.

**Microsoft Jet and Replication Objects 2.5 Library (JRO)**

<a name="since-ado-objects-were-designed-to-work-with-many-databases-in-addition-to-microsoft-jet-databases-functionality-specific-to-jet-was-broken-out-into-the-jro-library"></a>Da ADO-Objekte für die Zusammenarbeit mit vielen Datenbanken neben den Microsoft Jet-Datenbanken konzipiert wurden, wurde die Jet-spezifische Funktionalität in die JRO-Bibliothek verlagert.
=======
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO Ext Sicherheit (ADOX)

ADOX stellt die Datendefinitionssprache (Data Definition Language, DDL)-Objekte, die erforderlich sind, zum Erstellen einer neuen Datenbank und der darin enthaltenen Objekte zusätzlich zu den zum Verwalten der Sicherheit bereit.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet and Replication Objects 2.5-Bibliothek (JRO)

Da ADO-Objekte für die Arbeit mit vielen Datenbanken neben den Microsoft Jet-Datenbanken konzipiert wurden, wurde die Jet-spezifische Funktionalität in die JRO-Bibliothek verlagert.
>>>>>>> master

Die folgende Liste listet die von jedem der neuen Objektmodelle bereitgestellten Funktionen im Vergleich zu DAO auf.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Funktion</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
<<<<<<< Kopf (nur des MDB)</p></th>
=== (Nur MDBs)</p></th>
>>>>>>> master
</tr>
</thead>
<tbody>
<tr class="odd">
<<<<<<< Kopf
<td><p>Erstellen von Datensatzgruppen</p></td>
=======
<td><p>Erstellen von Datensatzgruppen.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Bearbeiten von Starteigenschaften</p></td>
=======
<td><p>Bearbeiten von Starteigenschaften.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Unterstützung von ANSI92 SQL***</p></td>
=======
<td><p>Unterstützung von ANSI92 SQL.* **</p></td>
>>>>>>>Master-Shape
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Erstellen von Tabellen</p></td>
=======
<td><p>Erstellen von Tabellen.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Erstellen einer neuen Datenbank</p></td>
=======
<td><p>Erstellen Sie neue Datenbank.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Bearbeiten vorhandener Tabelleneigenschaften</p></td>
=======
<td><p>Bearbeiten Sie vorhandener Tabelleneigenschaften.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Erstellen von Tabellenbeziehungen</p></td>
=======
<td><p>Erstellen von tabellenbeziehungen.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Bearbeiten von Sicherheitseinstellungen</p></td>
=======
<td><p>Bearbeiten von Sicherheitseinstellungen.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Unterstützung des Attributs Compression für Spaltendaten</p></td>
=======
<td><p>Unterstützung des Attributs Compression für Spaltendaten.</p></td>
>>>>>>>Master-Shape
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Bearbeiten gespeicherter SQL-Standardabfragen oder -ansichten</p></td>
=======
<td><p>Bearbeiten Sie gespeicherter SQL-Standardabfragen oder-Ansichten.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Erstellen permanenter Abfragen, auf die nur über Code zugegriffen werden kann</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Erstellen von Abfragen, auf die über Datenbankcontainer/UI und Code zugegriffen werden kann</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Komprimieren/Verschlüsseln von Datenbanken</p></td>
=======
<td><p>Codieren Sie komprimieren/Datenbank.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Aktualisieren des Cachespeichers</p></td>
=======
<td><p>Aktualisieren des Cachespeichers.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Datenbank replizierbar machen</p></td>
=======
<td><p>Machen Sie Datenbank replizierbar.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Erstellen von Datenbankreplikaten</p></td>
=======
<td><p>Erstellen von Datenbankreplikaten.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Synchronisieren von Replikaten</p></td>
=======
<td><p>Synchronisieren von Replikaten.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Bearbeiten von Datenbankeigenschaften</p></td>
=======
<td><p>Bearbeiten von Datenbankeigenschaften.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< Kopf
<td><p>Erstellen benutzerdefinierter Datenbankeigenschaften</p></td>
=======
<td><p>Erstellen Sie benutzerdefinierter Datenbankeigenschaften.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< Kopf
<td><p>Bearbeiten von Tabellenspalteneigenschaften</p></td>
=======
<td><p>Bearbeiten von Tabellenspalteneigenschaften.</p></td>
>>>>>>>Master-Shape
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Nur verfügbar beim Arbeiten mit Microsoft Access-Datenbanken. Zukünftige Versionen des SQL-Providers stellen diese Funktionalität möglicherweise auch in Microsoft Access-Projekten (ADP) bereit.

\*\* Nur verfügbar beim Arbeiten mit Access-Projekten.

<<<<<<< HEAD \* \* \* , obwohl das Access-Datenbankmodul ANSI 92 SQL unterstützt es ist noch nicht vollständig ANSI92-kompatibel.

1Verweist mithilfe des **Connection** -Objekts auf Datenbank

2Verweist mithilfe des **Catalog** -Objekts auf Datenbank

3Verweist mithilfe des **Replica** -Objekts auf Datenbank

4Verweist mithilfe des **JetEngine** -Objekts auf Datenbank


> [!NOTE]
> <a name="punlike-dao-ado-and-adox-objects-can-perform-the-marked-actions-in-databases-other-then-jet-as-long-as-the-provider-for-those-databases-supports-that-actionp"></a><P>[!HINWEIS] Im Gegensatz zu DAO können ADO- and ADOX-Objekte die gekennzeichneten Aktionen in anderen Datenbanken als Jet-Datenbanken ausführen, sofern der Provider für diese Datenbanken die betreffende Aktion unterstützt.</P>
=======
\*\*\*Obwohl das Access-Datenbankmodul ANSI 92 SQL unterstützt werden, ist es noch nicht vollständig ANSI92-kompatibel.

1 verwendet **Connection** -Objekts auf Datenbank.

2 verwendet **Catalog** -Objekts auf Datenbank.

3 verwendet **Replikat** -Objekts auf Datenbank.

4 verwendet **JetEngine** -Objekts auf Datenbank.


> [!NOTE]
> Im Gegensatz zu DAO können ADO- and ADOX-Objekte die gekennzeichneten Aktionen in Datenbanken als Jet ausführen, solange der Provider für diese Datenbanken die betreffende Aktion unterstützt.
>>>>>>> master


