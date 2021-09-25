---
title: ADO-Aufzählungskonstanten
TOCTitle: ADO enumerated constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: bef40c027c85621005d02ab16b9606b9784368a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553417"
---
# <a name="ado-enumerated-constants"></a>ADO-Aufzählungskonstanten

**Gilt für**: Access 2013, Office 2013

Zur Unterstützung beim Debuggen wird in den ADO-Aufzählungen für jede Konstante ein Wert aufgelistet. Dieser Wert ist jedoch lediglich ein Hinweis und kann zwischen ADO-Versionen geändert werden. Der Code sollte nur vom Namen, nicht vom tatsächlichen Wert, der einzelnen aufgezählten Konstanten abhängen.

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Aufzählungskonstante</th>
<th>Beschreibung</th>
</tr>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Für ein <strong>Recordset</strong>-RDS-Objekt wird die Ausführungspriorität des asynchronen Threads angegeben, durch den Daten abgerufen werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Es wird angegeben, wann durch den <strong>MSDataShape</strong>-Anbieter aggregierte und berechnete Spalten in einem hierarchischen <strong>Recordset</strong> erneut berechnet werden.</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Es wird angegeben, welche Felder zum Erkennen von Konflikten während einer optimistischen Aktualisierung einer Zeile der Datenquelle mit einem <strong>Recordset</strong>-Objekt verwendet werden können.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Es wird angegeben, ob auf die <strong>UpdateBatch</strong>-Methode eine implizite <strong>Resync</strong>-Methodenoperation folgt, und es wird ggf. der Umfang der Operation angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Es wird angegeben, welche Datensätze von einer Operation betroffen sind.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Eine Textmarke wird angegeben, die anzeigt, wo die Operation beginnen soll.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Es wird angegeben, wie ein Befehlsargument interpretiert werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Die relative Position zweier Datensätze, die von Textmarken dargestellt werden, wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Die verfügbaren Berechtigungen zum Ändern von Daten in einem <strong>Connection</strong>-Objekt, zum Öffnen eines <strong>Record</strong>-Objekts oder zum Angeben von Werten für die <strong>Mode</strong>-Eigenschaft der Objekte <strong>Record</strong> und <strong>Stream</strong> werden angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Es wird angegeben, ob die <strong>Open</strong>-Methode eines <strong>Connection</strong>-Objekts zurückgegeben werden soll, nachdem (synchron) oder bevor (asynchron) die Verbindung hergestellt wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Es wird angegeben, ob ein Dialog angezeigt werden soll, der zur Eingabe fehlender Parameter auffordert, wenn eine Verbindung mit einer ODBC-Datenquelle geöffnet wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p>Das Verhalten der <strong>CopyRecord</strong>-Methode wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>Der Speicherort des Cursormoduls wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p>Es wird angegeben, auf welche Funktionalität die <strong>Supports</strong>-Methode getestet werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Der Typ des Cursors wird angegeben, der in einem <strong>Recordset</strong>-Objekt verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Der Datentyp eines <strong>Field</strong>-Objekts, eines <strong>Parameter</strong>-Objekts oder eines <strong>Property</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Der Bearbeitungsstatus eines Datensatzes wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Der Typ eines ADO-Laufzeitfehlers wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Der Grund für das Auftreten eines Ereignisses wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>Der aktuelle Status der Ausführung eines Ereignisses wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>Es wird angegeben, wie ein Befehl von einem Anbieter ausgeführt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p>Die speziellen Felder werden angegeben, auf die in der <strong>Field</strong>-Auflistung eines <strong>Record</strong>-Objekts verwiesen wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Eines oder mehrere Attribute eines <strong>Field</strong>-Objekts werden angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Der Status eines <strong>Field</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Die Gruppe der zu filternden Datensätze aus einem <strong>Recordset</strong>-Objekt wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Es wird angegeben, wie viele Datensätze aus einem <strong>Recordset</strong>-Objekt abgerufen werden sollen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Die Transaktionsisolationsstufe für ein <strong>Connection</strong>-Objekt wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Es wird das Zeichen angegeben, das als Zeilentrennzeichen in <strong>Stream</strong>-Textobjekten verwendet wird.</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Es wird der Typ der Sperrung angegeben, die während der Bearbeitung für Datensätze festgelegt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptionsEnum</a></p></td>
<td><p>Es wird angegeben, welche Datensätze an den Server zurückgegeben werden sollen.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Das Verhalten der <strong>MoveRecord</strong>-Methode des <strong>Record</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Es wird angegeben, ob ein Objekt geöffnet oder geschlossen ist, eine Verbindung mit einer Datenquelle herstellt, einen Befehl ausführt oder Daten abruft.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Die Attribute eines <strong>Parameter</strong>-Objekts werden angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Es wird angegeben, ob das <strong>Parameter</strong>-Objekt einen Eingabeparameter und/oder einen Ausgabeparameter darstellt oder ob der Parameter der Rückgabewert aus einer gespeicherten Prozedur ist.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Es wird das Format angegeben, in dem ein <strong>Recordset</strong>-Objekt gespeichert werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Die aktuelle Position des Datensatzzeigers innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Die Attribute eines <strong>Property</strong>-Objekts werden angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Die <strong>Open</strong>-Methode des <strong>Record</strong>-Objekts wird angegeben, sowie ob ein vorhandenes <strong>Record</strong>-Objekt geöffnet werden soll oder ob ein neues <strong>Record</strong>-Objekt erstellt werden soll.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Optionen für das Öffnen eines <strong>Record</strong>-Objekts werden angegeben. Diese Werte können mithilfe eines OR-Operators kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Der Status eines Datensatzes in Bezug auf Batchaktualisierungen und andere Mengenoperationen wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Der Typ eines <strong>Record</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Es wird angegeben, ob zugrunde liegende Werte durch einen Aufruf von <strong>Resync</strong> überschrieben werden.</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Gibt an, ob eine Datei erstellt oder gespeichert werden sollte, wenn die Speicherung in einem <strong>Stream</strong>-Objekt erfolgt. Die Werte können mit einem AND-Operator kombiniert werden.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Der Typ des <strong>Recordset</strong>-Schemaobjekts wird angegeben, das von der <strong>OpenSchema</strong>-Methode abgerufen wird. Die Richtung einer Datensatzsuche innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Die Richtung einer Datensatzsuche innerhalb eines <strong>Recordset</strong>-Objekts wird angegeben. Der Typ des auszuführenden <strong>Seek</strong>-Vorgangs wird angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Der Typ des auszuführenden <strong>Seek</strong>-Vorgangs wird angegeben. Optionen für das Öffnen eines <strong>Stream</strong>-Objekts werden angegeben. Die Werte können mit einem AND-Operator kombiniert werden.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Optionen für das Öffnen eines <strong>Stream</strong>-Objekts werden angegeben. Die Werte können mit einem AND-Operator kombiniert werden. Es wird angegeben, ob der gesamte Datenstrom oder die nächste Zeile aus einem <strong>Stream</strong>-Objekt gelesen werden soll.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Es wird angegeben, ob der gesamte Datenstrom oder die nächste Zeile aus einem <strong>Stream</strong>-Objekt gelesen werden soll. Der Typ der in einem <strong>Stream</strong>-Objekt gespeicherten Daten wird angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Der Typ der in einem <strong>Stream</strong>-Objekt gespeicherten Daten wird angegeben. Es wird angegeben, ob ein Zeilentrennzeichen an die Zeichenfolge angefügt wird, die in ein <strong>Stream</strong>-Objekt geschrieben wird.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Es wird angegeben, ob ein Zeilentrennzeichen an die Zeichenfolge angefügt wird, die in ein <strong>Stream</strong>-Objekt geschrieben wird. Das Format beim Abrufen eines <strong>Recordset</strong>-Objekts wird als Zeichenfolge angegeben.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Das Format beim Abrufen eines <strong>Recordset</strong>-Objekts wird als Zeichenfolge angegeben. Die Transaktionsattribute eines <strong>Connection</strong>-Objekts werden angegeben.</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Gibt die Transaktionsattribute eines <strong>Connection</strong>-Objekts an.</p></td>
</tr>
</tbody>
</table>

