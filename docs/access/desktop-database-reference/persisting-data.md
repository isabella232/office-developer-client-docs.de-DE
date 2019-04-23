---
title: Persisting Data (Access-Desktop-Daten Bankreferenz)
TOCTitle: Persisting data
ms:assetid: cb8a32f7-2cdc-26ed-c6d4-dd93c1ac37ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250010(v=office.15)
ms:contentKeyID: 48547715
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f5788216a20e62cfc39fd2081f4f672bc4f9b808
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287601"
---
# <a name="persisting-data"></a>Speichern von Daten


**Gilt für**: Access 2013, Office 2013

Tragbare Computer (z. B. Laptops) haben Anwendungen erforderlich gemacht, die online und offline ausgeführt werden können. ADO unterstützt dies nun, indem der Entwickler ein Clientcursor- **Recordset** auf einem Datenträger speichern und später erneut laden kann.

Für dieses Feature gibt es verschiedene Einsatzmöglichkeiten:

- **Unterwegs:** Wenn Sie mit der Anwendung unterwegs sind, müssen unbedingt Änderungen vorgenommen und neue Datensätze hinzugefügt werden können, die dann später erneut mit der Datenbank verbunden werden können und für die ein Commit ausgeführt werden kann.

- **Selten aktualisierte Lookuptabellen:** Bei einer Anwendung werden Tabellen oft zum Nachschlagen verwendet, z. B. Steuertabellen. Sie werden selten aktualisiert und sind schreibgeschützt. Anstatt diese Daten bei jedem Start der Anwendung erneut vom Server einzulesen, kann die Anwendung die Daten einfach von einem lokal gespeicherten **Recordset** -Objekt laden.

Verwenden Sie in ADO zum Speichern und Laden von **Recordset** -Objekten die Methoden **Recordset.Save** und **Recordset.Open(,,,,adCmdFile)** im **Recordset** -Objekt von ADO.

Sie können die **Save** -Methode des **Recordset** -Objekts zum Speichern des **Recordset** -Objekts von ADO in einer Datei auf einem Datenträger verwenden. (Ein **Recordset** -Objekt kann auch in einem **Stream** -Objekt von ADO gespeichert werden. **Stream** -Objekte werden weiter unten in diesem Handbuch behandelt.) Später können Sie mit der **Open** -Methode das **Recordset** -Objekt erneut öffnen, wenn Sie es benötigen. Standardmäßig speichert ADO das **Recordset** -Objekt im systemeigenen Microsoft Advanced Data TableGram-Format (ADTG). Dieses binäre Format wird mithilfe des **adPersistADTG** -Werts für **PersistFormatEnum** angegeben. Alternativ können Sie das **Recordset** -Objekt stattdessen mithilfe von **adPersistXML** im XML-Format speichern. Weitere Informationen zum Speichern von Datensätzen im XML-Format finden Sie unter [Speichern von Datensätzen im XML-Format](persisting-records-in-xml-format.md).

Die **Save** -Methode weist die folgende Syntax auf:

`recordset.Save Destination, PersistFormat`

Wenn Sie das **Recordset**-Objekt das erste Mal speichern, können Sie optional das *Ziel* angeben. Wenn Sie das *Ziel* auslassen, wird eine neue Datei erstellt, deren Namen auf den Wert der [Source](source-property-ado-recordset.md)-Eigenschaft des **Recordset**-Objekts festgelegt ist.

Lassen Sie das *Ziel* aus, wenn Sie anschließend **Save** nach dem ersten Speichern aufrufen, da ansonsten ein Laufzeitfehler generiert wird. Wenn Sie danach **Save** mit einem neuen *Ziel* aufrufen, wird das **Recordset**-Objekt im neuen Ziel gespeichert. Das neue Ziel und das ursprüngliche Ziel sind jedoch beide geöffnet.

Mit **Save** wird das **Recordset**-Objekt oder das *Ziel* nicht geschlossen, weshalb Sie weiter mit dem **Recordset**-Objekt arbeiten und die neuesten Änderungen speichern können. Das *Ziel* bleibt so lange geöffnet, bis das **Recordset**-Objekt geschlossen wird. In dieser Zeit können andere Anwendungen das *Ziel* lesen, aber nicht in dieses schreiben.

Aus Sicherheitsgründen gestattet die **Save** -Methode nur die Verwendung niedriger und benutzerdefinierter Sicherheitseinstellungen in einem von Microsoft Internet Explorer ausgeführten Skript. Ausführlichere Erläuterungen zu Sicherheitsproblemen finden Sie unter "ADO- und RDS-Sicherheitsprobleme in Microsoft Internet Explorer" (in englischer Sprache) im Abschnitt "ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles".

Wenn die **Save** -Methode während eines asynchronen Abruf-, Ausführungs- oder Aktualisierungsvorgangs des **Recordset** -Objekts aufgerufen wird, wartet die **Save** -Methode, bis der asynchrone Vorgang abgeschlossen ist.

Datensätze werden ab der ersten Zeile des **Recordset** -Objekts gespeichert. Wenn die **Save** -Methode abgeschlossen ist, wird die erste Zeile des **Recordset** -Objekts zur aktuellen Zeile.

Legen Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft mithilfe von **Save** auf **adUseClient** fest, um optimale Ergebnisse zu erzielen. Wenn Ihr Anbieter nicht die gesamte zum Speichern von **Recordset** -Objekten erforderliche Funktionalität unterstützt, bietet der Cursordienst diese Funktionalität.

Wenn ein **Recordset** -Objekt gespeichert wird, während die **CursorLocation** -Eigenschaft auf **adUseServer** festgelegt ist, sind die Aktualisierungsmöglichkeiten für das **Recordset** -Objekt eingeschränkt. Normalerweise ist nur das Aktualisieren, Einfügen und Löschen für eine einzelne Tabelle zulässig (in Abhängig von der Providerfunktionalität). Die [Resync](resync-method-ado.md)-Methode ist in dieser Konfiguration ebenfalls nicht verfügbar.

Für den *Ziel*-Parameter ist jedes Objekt zulässig, das die OLE DB-Schnittstelle **IStream** unterstützt. Deshalb können Sie ein **Recordset**-Objekt direkt im **Response**-Objekt von ASP speichern.

Im folgenden Beispiel wird mit den Methoden **Save** und **Open** ein **Recordset**-Objekt gespeichert und später erneut geöffnet:

```vb 
 
'BeginPersist 
 conn.ConnectionString = _ 
 "Provider='SQLOLEDB';Data Source='MySqlServer';" _ 
 & "Integrated Security='SSPI';Initial Catalog='pubs'" 
 conn.Open 
 
 conn.Execute "create table testtable (dbkey int " & _ 
 "primary key, field1 char(10))" 
 conn.Execute "insert into testtable values (1, 'string1')" 
 
 Set rst.ActiveConnection = conn 
 rst.CursorLocation = adUseClient 
 
 rst.Open "select * from testtable", conn, adOpenStatic, _ 
 adLockBatchOptimistic 
 
 'Change the row on the client 
 rst!field1 = "NewValue" 
 
 'Save to a file--the .dat extension is an example; choose 
 'your own extension. The changes will be saved in the file 
 'as well as the original data. 
 MyFile = Dir("c:\temp\temptbl.dat") 
 If MyFile <> "" Then 
 Kill "c:\temp\temptbl.dat" 
 End If 
 
 rst.Save "c:\temp\temptbl.dat", adPersistADTG 
 rst.Close 
 Set rst = Nothing 
 
 'Now reload the data from the file 
 Set rst = New ADODB.Recordset 
 rst.Open "c:\temp\temptbl.dat", , adOpenStatic, _ 
 adLockBatchOptimistic, adCmdFile 
 
 Debug.Print "After Loading the file from disk" 
 Debug.Print " Current Edited Value: " & rst!field1.Value 
 Debug.Print " Value Before Editing: " & rst!field1.OriginalValue 
 
 'Note that you can reconnect to a connection and 
 'submit the changes to the data source 
 Set rst.ActiveConnection = conn 
 rst.UpdateBatch 
'EndPersist 
```

Dieser Abschnitt enthält die folgenden Themen:

- [Weitere Informationen zur Daten Satz Persistenz](more-about-recordset-persistence.md)

- [Speichern von geFilterten und hierarchischen Recordsets](persisting-filtered-and-hierarchical-recordsets.md)

- [Speichern von Datensätzen im XML-Format (ADO)](persisting-records-in-xml-format.md)
