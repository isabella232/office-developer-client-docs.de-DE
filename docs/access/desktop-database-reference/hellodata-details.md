---
title: Informationen zu HelloData (Access PC-Datenbank-Referenz)
TOCTitle: HelloData Details
ms:assetid: db51e15c-1b5b-c64a-2f84-34dd0e78c6cf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250105(v=office.15)
ms:contentKeyID: 48548103
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c25197f0a8a45487f93f56543f73a2beeea062ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603155"
---
# <a name="hellodata-details"></a>Informationen zu HelloData


**Betrifft**: Access 2013 | Office 2013

Mit der Anwendung HelloData werden die grundlegenden Vorgänge einer typischen ADO-Anwendung ausgeführt: Abrufen, Überprüfen, Bearbeiten und Aktualisieren von Daten. Klicken Sie beim Starten der Anwendung auf die erste Schaltfläche (Daten abrufen). Damit wird die GetData()-Subroutine ausgeführt.

## <a name="getdata"></a>GetData

GetData Fügt eine gültige Verbindungszeichenfolge in einer Variablen auf Modulebene *m\_sConnStr*. Weitere Informationen zu Verbindungszeichenfolgen finden Sie unter [Erstellen der Verbindungszeichenfolge](creating-the-connection-string.md).

Weisen Sie eine Fehlerbehandlungsroutine mithilfe der Visual Basic-Anweisung **OnError** zu. Weitere Informationen zur Fehlerbehandlung in ADO finden Sie in [Kapitel 6: Fehlerbehandlung](chapter-6-error-handling.md). Ein neues **Connection**-Objekt wird erstellt, und die **CursorLocation**-Eigenschaft wird auf **adUseClient** festgelegt, da mit dem HelloData-Beispiel eine *getrennte Datensatzgruppe* erstellt wird. Das bedeutet, dass die physikalische Verbindung nach dem Abrufen der Daten aus der Datenquelle unterbrochen wird. Sie können jedoch weiterhin mit den Daten arbeiten, da diese lokal im **Recordset**-Objekt zwischengespeichert sind.

Weisen Sie nach dem Öffnen der Verbindung einer Variablen (sSQL) eine SQL-Zeichenfolge zu. Instanziieren Sie ein neues **Recordset** -Objekt m\_oRecordset1. Öffnen Sie in der nächsten Codezeile das **Recordset-Objekt** über das vorhandene **Connection**, übergeben. Öffnen Sie in der nächsten Codezeile das **Recordset-Objekt** über das vorhandene **Connection**, sSQL als die Quelle des **Recordset-Objekts**übergeben. Unterstützen Sie ADO festlegen, dass die SQL-Zeichenfolge, die Sie als Quelle für das **Recordset-Objekt** übergeben haben Textdefinition eines Befehls, indem Sie **AdCmdText** im letzten Arguments an das **Recordset** **Open** -Methode übergeben wird. Diese Zeile auch die **LockType** und **CursorType** zugeordnete **Recordset-Objekt**.

<<<<<<< HEAD die nächste Codezeile wird die **MarshalOptions** -Eigenschaft **AdMarshalModifiedOnly**gleich. **MarshalOptions** gibt an, welche Datensätze auf die mittlere Ebene (oder den Webserver) gemarshallt werden müssen. Weitere Informationen zum Marshalling finden Sie in der Dokumentation zu COM. Wenn eine clientseitige Cursor **AdMarshalModifiedOnly** mit ([CursorLocation](cursorlocation-property-ado.md) = **AdUseClient**), nur die Datensätze, die auf dem Client geändert wurden in der mittleren Ebene zurückgeschrieben werden. Wenn **MarshalOptions** auf **adMarshalModifiedOnly** festgelegt wird, wird möglicherweise die Leistung verbessert, da weniger Zeilen gemarshallt werden müssen.
=== Die nächste Codezeile wird die **MarshalOptions** -Eigenschaft gleich **AdMarshalModifiedOnly**. **MarshalOptions** gibt an, welche Datensätze in der mittleren Ebene (oder Webserver) gemarshallt werden sollen. Weitere Informationen zum Marshalling finden Sie in der Dokumentation zu COM. Wenn eine clientseitige Cursor **AdMarshalModifiedOnly** mit ([CursorLocation](cursorlocation-property-ado.md) = **AdUseClient**), nur die Datensätze, die auf dem Client geändert wurden in der mittleren Ebene zurückgeschrieben werden. Wenn **MarshalOptions** auf **adMarshalModifiedOnly** festgelegt wird, wird möglicherweise die Leistung verbessert, da weniger Zeilen gemarshallt werden müssen.
>>>>>>> master

Trennen Sie anschließend das **Recordset** -Objekt, indem Sie die zugehörige **ActiveConnection** -Eigenschaft auf **Nothing** setzen. Weitere Informationen finden Sie unter [Trennen und Wiederherstellen der Verbindung für das Recordset-Objekt](disconnecting-and-reconnecting-the-recordset.md) in "Kapitel 5: Aktualisieren und Speichern von Daten".

Schließen Sie die Verbindung mit der Datenquelle, und löschen Sie das vorhandene **Connection** -Objekt. Damit geben Sie die von diesem Objekt belegten Ressourcen frei.

In einem letzten Schritt wird das **Recordset** -Objekt als **DataSource** für Microsoft DataBound-Rastersteuerelement auf dem Formular festgelegt, sodass die Daten aus dem **Recordset** -Objekt problemlos auf dem Formular angezeigt werden können.

Klicken Sie auf die zweite Schaltfläche (Daten prüfen). Die ExamineData-Subroutine wird ausgeführt.

## <a name="examinedata"></a>ExamineData

ExamineData verwendet verschiedene Methoden und Eigenschaften des Recordset-Objekts zum Anzeigen von Informationen zu den Daten im Recordset-Objekt. Die Subroutine meldet die Anzahl von Datensätzen mithilfe der RecordCount-Eigenschaft. Sie führt das Recordset-Objekt in Schleifen aus und druckt den Wert der AbsolutePosition-Eigenschaft in das Anzeigetextfeld auf dem Formular. Zudem wird beim Ausführen der Schleife der Wert der Bookmark-Eigenschaft für den dritten Datensatz für die spätere Verwendung in eine Variable vom Typ Variant (vBookmark) eingefügt.

Die Routine kehrt mithilfe der zuvor gespeicherten Textmarkenvariablen direkt zum dritten Datensatz zurück. Die Routine ruft die WalkFields-Subroutine auf, die die Fields-Auflistung des Recordset-Objekts in Schleifen ausführt und Informationen zu jedem Field-Eintrag in der Auflistung anzeigt.

Abschließend verwendet die ExamineData-Subroutine die Filter-Eigenschaft des Recordset-Objekts, um nur nach den Datensätzen zu suchen, deren CategoryId-Wert gleich 2 ist. Das Ergebnis dieses Filters wird auf dem Anzeigeraster des Formulars sofort angezeigt.

Weitere Informationen zu der in der ExamineData-Subroutine dargestellten Funktionalität finden Sie in Kapitel 3: Untersuchen von Daten.

Klicken Sie nun auf die dritte Schaltfläche (Daten bearbeiten). Damit wird die EditData-Subroutine ausgeführt.

## <a name="editdata"></a>EditData

Wenn der Code mit der Ausführung der EditData-Subroutine beginnt, wird das Recordset-Objekt noch nach Einträgen gefiltert, deren CategoryId-Wert gleich 2 ist. Daher werden nur die Elemente angezeigt, die diesem Filterkriterium entsprechen. Die Subroutine führt zunächst das Recordset-Objekt in Schleifen aus und erhöht den Preis der im Recordset-Objekt angezeigten Elemente um 10 %. Der Wert des Price-Felds wird geändert, indem die Value-Eigenschaft für das Feld auf einen neuen gültigen Betrag gesetzt wird.

Beachten Sie, dass das Recordset-Objekt von der Datenquelle getrennt ist. Die in der EditData-Subroutine vorgenommenen Änderungen werden nur für die lokal zwischengespeicherte Kopie der Daten übernommen. Weitere Informationen finden Sie in Kapitel 4: Bearbeiten von Daten.

Die Änderungen werden in der Datenquelle erst übernommen, wenn Sie auf die vierte Schaltfläche (Daten aktualisieren) klicken. Die UpdateData-Subroutine wird ausgeführt.

## <a name="updatedata"></a>UpdateData

UpdateData entfernt zuerst den Filter, der an das **Recordset**angewendet wurde. Der Code entfernt und als **DataSource** für das Microsoft Bound DataGrid auf dem Formular zurückgesetzt, sodass das ungefilterte **Recordset-Objekt** im Raster angezeigt wird.

Der Code überprüft als Nächstes, ob Sie sich im **Recordset** -Objekt mithilfe der **Supports** -Methode mit dem **adMovePrevious** -Argument zurück bewegen können.

Die Routine kehrt mit der **MoveFirst** -Methode zum ersten Datensatz zurück und zeigt den ursprünglichen und aktuellen Wert des Felds an. Hierzu werden die Eigenschaften **OriginalValue** und **Value** des **Field** -Objekts verwendet. Diese Eigenschaften werden zusammen mit der **UnderlyingValue** -Eigenschaft (hier nicht verwendet) in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md) beschrieben.

Im nächsten Schritt wird ein neues **Connection** -Objekt erstellt und verwendet, um mit der Datenquelle erneut eine Verbindung herzustellen. Sie verbinden das **Recordset** -Objekt erneut mit der Datenquelle, indem Sie das neue **Connection** -Objekt als **ActiveConnection** für das **Recordset** -Objekt festlegen. Um die Aktualisierungen an den Server zu senden, ruft der Code **UpdateBatch** auf dem **Recordset** -Objekt auf.

Wenn die Batchaktualisierung erfolgreich ist, handelt es sich bei eine Variablen auf Modulebene Kennzeichnung, auf True festgelegt ist. Dadurch werden Sie später auf, um alle Änderungen an der Datenbank bereinigen daran erinnern.

In einem letzten Schritt kehrt der Code zum ersten Datensatz im **Recordset** -Objekt zurück und zeigt den ursprünglichen und aktuellen Wert an. Diese beiden Werte sind nach dem Aufruf von **UpdateBatch** identisch.

Ausführlichere Informationen zum Aktualisieren von Daten sowie Anweisungen zur Vorgehensweise, wenn Daten auf dem Server geändert werden, während das **Recordset** -Objekt getrennt ist, finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

## <a name="formunload"></a>Formular\_entladen

Das Formular\_Unload-Unterroutine ist aus verschiedenen Gründen zu wichtig. Erste, da dies ein Beispiel für Formular ist\_Unload bereinigt die Änderungen an der Datenbank vor dem Beenden der Anwendung. Zweitens zeigt den Code, wie ein Befehl direkt über ein geöffnetes **Connection** -Objekt mithilfe der **Execute** -Methode ausgeführt werden kann. Abschließend wird ein Beispiel für die Ausführung einer Abfrage nicht Zeile zurückgibt (eine Aktualisierungsabfrage) für die Datenquelle.

