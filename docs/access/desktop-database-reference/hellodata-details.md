---
title: HelloData Details (Access Desktop Database Reference)
TOCTitle: HelloData details
ms:assetid: db51e15c-1b5b-c64a-2f84-34dd0e78c6cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250105(v=office.15)
ms:contentKeyID: 48548103
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 78b04b74d4e2b8d9c215235d6e7ccebed4fa2ef2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291999"
---
# <a name="hellodata-details"></a>HelloData-Details


**Gilt für**: Access 2013, Office 2013

The HelloData application steps through the basic operations of a typical ADO application: getting, examining, editing, and updating data. When you start the application, click the first button, **Get Data**. This will run the GetData() subroutine.

## <a name="getdata"></a>GetData

GetData platziert eine gültige Verbindungszeichenfolge in eine Variable auf Modulebene, *m\_sConnStr*. For more information about connection strings, see [Creating the Connection String](creating-the-connection-string.md).

Weisen Sie eine Fehlerbehandlungsroutine mithilfe der Visual Basic-Anweisung **OnError** zu. Weitere Informationen zur Fehlerbehandlung in ADO finden Sie in [Kapitel 6: Fehlerbehandlung](chapter-6-error-handling.md). Ein neues **Connection**-Objekt wird erstellt, und die **CursorLocation**-Eigenschaft wird auf **adUseClient** festgelegt, da mit dem HelloData-Beispiel eine *getrennte Datensatzgruppe* erstellt wird. Das bedeutet, dass die physikalische Verbindung nach dem Abrufen der Daten aus der Datenquelle unterbrochen wird. Sie können jedoch weiterhin mit den Daten arbeiten, da diese lokal im **Recordset**-Objekt zwischengespeichert sind.

Weisen Sie nach dem Öffnen der Verbindung einer Variablen (sSQL) eine SQL-Zeichenfolge zu. Instanziieren Sie dann ein neues **Recordset** -Objekt\_, m oRecordset1. Öffnen Sie in der nächsten Codezeile das **Recordset** -Objekt über die vorhandene **Verbindung**, und übergeben Sie es. Öffnen Sie in der nächsten Codezeile das **Recordset** -Objekt über die vorhandene **Verbindung**, und übergeben Sie SSQL als Quelle des **Recordset-Objekts**. Sie unterstützen ADO bei der Bestimmung, dass die SQL-Zeichenfolge, die Sie als Quelle für das **Recordset** -Objekt übergeben haben, eine Textdefinition eines Befehls ist, indem Sie **adCmdText** im letzten Argument an die **Open** -Methode des **Recordset-Objekts** übergeben. In dieser Position werden auch die mit dem **Recordset**verknüpften **LockType** -und **CursorType** -Datensätze festgelegt.

Mit der nächsten Codezeile wird die **MarshalOptions** -Eigenschaft mit **adMarshalModifiedOnly** gleichgesetzt. **MarshalOptions** gibt an, welche Datensätze auf die mittlere Ebene (oder den Webserver) gemarshallt werden sollen. Weitere Informationen zum Marshalling finden Sie in der Dokumentation zu COM. Bei Verwendung von **adMarshalModifiedOnly** mit einem clientseitigen Cursor ([CursorLocation](cursorlocation-property-ado.md) = **adUseClient**) werden nur Datensätze, die auf dem Client geändert wurden, in die mittlere Ebene zurückgeschrieben. Wenn **MarshalOptions** auf **adMarshalModifiedOnly** festgelegt wird, wird möglicherweise die Leistung verbessert, da weniger Zeilen gemarshallt werden müssen.

Trennen Sie anschließend das **Recordset** -Objekt, indem Sie die zugehörige **ActiveConnection** -Eigenschaft auf **Nothing** setzen. Weitere Informationen finden Sie unter [Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt](disconnecting-and-reconnecting-the-recordset.md) in "Kapitel 5: Aktualisieren und Speichern von Daten".

Schließen Sie die Verbindung mit der Datenquelle, und löschen Sie das vorhandene **Connection** -Objekt. Damit geben Sie die von diesem Objekt belegten Ressourcen frei.

In einem letzten Schritt wird das **Recordset**-Objekt als **DataSource** für Microsoft DataBound-Rastersteuerelement auf dem Formular festgelegt, sodass die Daten aus dem **Recordset**-Objekt problemlos auf dem Formular angezeigt werden können.

Click the second button, **Examine Data**. This runs the ExamineData subroutine.

## <a name="examinedata"></a>ExamineData

ExamineData uses various methods and properties of the **Recordset** object to display information about the data in the **Recordset**. It reports the number of records by using the **RecordCount** property. It loops through the **Recordset** and prints the value of the **AbsolutePosition** property in the display text box on the form. Auch in der Schleife wird der Wert der **Bookmark** -Eigenschaft für den dritten Datensatz in einer Variant-Variable, *vBookmark*, zur späteren Verwendung eingefügt.

The routine navigates directly back to the third record using the bookmark variable that it stored earlier. The routine calls the WalkFields subroutine, which loops through the **Fields** collection of the **Recordset** and displays details about each **Field** in the collection.

Finally, ExamineData uses the **Filter** property of the **Recordset** to screen for only those records with a CategoryId equal to 2. The result of applying this filter is immediately visible in the display grid on the form.

For more information about the functionality shown in the ExamineData subroutine, see [Chapter 3: Examining Data](chapter-3-examining-data.md).

Next, click the third button, **Edit Data**. This will run the EditData subroutine.

## <a name="editdata"></a>EditData

When the code enters the EditData subroutine, the **Recordset** is still filtered on CategoryId equal to 2, so only those items that meet the filter criteria are visible. It first loops through the **Recordset** and increases the price of each visible item in the **Recordset** by 10 percent. The value of the **Price** field is changed by setting the **Value** property for that field equal to a new, valid amount.

Remember that the **Recordset** is disconnected from the data source. The changes made in EditData are made only to the locally cached copy of the data. For more information, see [Chapter 4: Editing Data](chapter-4-editing-data.md).

The changes will not be made on the data source until you click the fourth button, **Update Data**. This will run the UpdateData subroutine.

## <a name="updatedata"></a>UpdateData

UpdateData first removes the filter that has been applied to the **Recordset**. Der Code entfernt und setzt als **DataSource** für das Microsoft Bound-DataGrid auf dem Formular zurück, sodass das ungefilterte **Recordset** -Objekt im Raster angezeigt wird.

Der Code überprüft als Nächstes, ob Sie sich im **Recordset**-Objekt mithilfe der **Supports**-Methode mit dem **adMovePrevious**-Argument zurück bewegen können.

Die Routine kehrt mit der **MoveFirst**-Methode zum ersten Datensatz zurück und zeigt den ursprünglichen und aktuellen Wert des Felds an. Hierzu werden die Eigenschaften **OriginalValue** und **Value** des **Field**-Objekts verwendet. Diese Eigenschaften werden zusammen mit der **UnderlyingValue**-Eigenschaft (hier nicht verwendet) in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md) beschrieben.

Im nächsten Schritt wird ein neues **Connection**-Objekt erstellt und verwendet, um mit der Datenquelle erneut eine Verbindung herzustellen. Sie verbinden das **Recordset**-Objekt erneut mit der Datenquelle, indem Sie das neue **Connection**-Objekt als **ActiveConnection** für das **Recordset**-Objekt festlegen. Um die Aktualisierungen an den Server zu senden, ruft der Code **UpdateBatch** auf dem **Recordset**-Objekt auf.

Wenn die Batchaktualisierung erfolgreich ist, wird eine Flag-Variable auf Modulebene auf true festgelegt. Damit werden Sie später daran erinnert, alle an der Datenbank vorgenommenen Änderungen zu bereinigen.

In einem letzten Schritt kehrt der Code zum ersten Datensatz im **Recordset** -Objekt zurück und zeigt den ursprünglichen und aktuellen Wert an. Diese beiden Werte sind nach dem Aufruf von **UpdateBatch** identisch.

Ausführlichere Informationen zum Aktualisieren von Daten sowie Anweisungen zur Vorgehensweise, wenn Daten auf dem Server geändert werden, während das **Recordset** -Objekt getrennt ist, finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

## <a name="formunload"></a>Formular\_entladen

Die unter\_Routine für das Entladen von Formularen ist aus verschiedenen Gründen wichtig. Da es sich um eine Beispielanwendung handelt,\_werden die Änderungen an der Datenbank bereinigt, bevor die Anwendung beendet wird. Second, the code shows how a command can be executed directly from an open **Connection** object using the **Execute** method. Schließlich zeigt es ein Beispiel für das Ausführen einer nicht Zeilen übergebenen Abfrage (eine Aktualisierungsabfrage) für die Datenquelle.

