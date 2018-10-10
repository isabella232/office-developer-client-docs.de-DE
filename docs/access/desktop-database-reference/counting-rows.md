---
title: Zählen von Zeilen (Access PC-Datenbank-Referenz)
TOCTitle: Counting Rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 93a583ef0a8f0ef287835eebdd9d68cf726a19df
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475024"
---
# <a name="counting-rows"></a>Zählen von Zeilen


**Betrifft**: Access 2013 | Office 2013

Die **RecordCount** -Eigenschaft gibt einen Wert vom Datentyp **Long** für die Anzahl von Datensätzen im **Recordset** -Objekt zurück. Mithilfe der **RecordCount** -Eigenschaft stellen Sie die Anzahl der Datensätze im **Recordset** -Objekt fest. Diese Eigenschaft gibt -1 zurück, wenn ADO die Anzahl von Datensätzen nicht bestimmen kann, oder wenn **RecordCount** vom Anbieter oder Cursortyp nicht unterstützt wird. Ein Fehler wird gemeldet, wenn die **RecordCount** -Eigenschaft für ein geschlossenes **Recordset** -Objekt gelesen wird.

Die **RecordCount** -Eigenschaft hängt von der Funktionalität des Anbieters und vom Cursortyp ab. Mit der **RecordCount** -Eigenschaft wird -1 für einen Vorwärtscursor, die tatsächliche Anzahl für einen statischen Cursor oder einen Keysetcursor, und je nach Datenquelle -1 oder die tatsächliche Anzahl für einen dynamischen Cursor zurückgegeben.

Im Beispiel **Recordset** eingeführt in [Untersuchen von Daten](chapter-3-examining-data.md) würde – 1 zurück, da ein Vorwärtscursor geöffnet wurde. Für die Verwendung der **RecordCount** -Eigenschaft müssten Sie das **Recordset** -Objekt mit einem leistungsfähigeren Cursor (statischer Cursor oder Keysetcursor) öffnen.

Es kann vorkommen, dass der Anbieter oder Cursor den Wert für die **RecordCount** -Eigenschaft nur bereitstellen kann, wenn zuerst alle Datensätze von der Datenquelle abgerufen werden. Rufen Sie die **MoveLast** -Methode des **Recordset** -Objekts vor **RecordCount** auf, um diese Art von Abrufen zu erzwingen.

Angenommen, Sie müssten die Codezeile, mit der die **Open** -Methode des **Recordset** -Objekts aufgerufen wird, durch folgenden Code ersetzen:

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

In diesem Fall könnten Sie die **RecordCount** -Eigenschaft verwenden, weil [RecordCount](microsoft-ole-db-provider-for-sql-server.md) von statischen Cursorn mit dem **Microsoft OLE DB-Anbieter für SQL Server** unterstützt werden. Beispielsweise würde der folgende Code die von dem Befehl zurückgegebene Anzahl von Datensätzen im Debugfenster ausgeben, vorausgesetzt die **RecordCount** -Eigenschaft wird vom Cursor unterstützt:

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

Von da an sollten diese leistungsfähigeren (aber teureren) Cursor- und Sperrtypeinstellungen verwendet werden.

