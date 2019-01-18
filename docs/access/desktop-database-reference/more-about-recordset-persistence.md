---
title: Weitere Informationen zur Recordset-Speicherung
TOCTitle: More about Recordset persistence
ms:assetid: f3248de7-6eef-1dd0-ff96-557b411789e7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250232(v=office.15)
ms:contentKeyID: 48548666
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 194dcf3826409c91f8d046b39b9009b43aee5477
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717608"
---
# <a name="more-about-recordset-persistence"></a>Weitere Informationen zur Recordset-Speicherung

**Betrifft**: Access 2013, Office 2013

Das ADO-Recordset-Objekt unterstützt das Speichern von Inhalt für ein **Recordset** -Objekt mithilfe der [Save](save-method-ado.md) -Methode in einer Datei. Die permanent gespeicherte Datei kann auf einem lokalen Laufwerk, Netzwerkserver oder als URL auf einer Website vorhanden. Die Datei kann später mit der [Open](open-method-ado-recordset.md) -Methode entweder des **Recordset** -Objekts oder die [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) -Methode des [Connection](connection-object-ado.md) -Objekts wiederhergestellt werden.

Außerdem wird durch die [GetString](getstring-method-ado.md)-Methode ein **Recordset** -Objekt in ein Formular konvertiert, dessen Spalten und Zeilen durch die von Ihnen angegebenen Zeichen getrennt sind.

Beginnen Sie, ein **Recordset** permanent zu machen, indem Sie es in ein Formular konvertieren, das in einer Datei gespeichert werden kann. **Recordset** -Objekte können im proprietären ADTG-Format (Advanced Data TableGram) oder im offenen XML-Format (Extensible Markup Language) gespeichert werden. ADTG-Beispiele werden weiter unten gezeigt. Weitere Informationen zur XML-Permanenz finden Sie unter [Speichern von Datensätzen im XML-Format](persisting-records-in-xml-format.md).

Speichern Sie alle ausstehenden Änderungen der permanenten Datei. Dadurch können Sie eine Abfrage ausgeben, von der ein **Recordset** -Objekt zurückgegeben wird und das **Recordset** bearbeitet und zusammen mit den ausstehenden Änderungen gespeichert wird. Später wird das **Recordset** wiederhergestellt, und dann wird die Datenquelle mit den gespeicherten ausstehenden Änderungen aktualisiert.

Weitere Informationen zum permanenten Speichern von **Stream** -Objekten finden Sie unter [Datenströme und Permanenz](streams-and-persistence.md) in Kapitel 10.

Ein Beispiel für die **Recordset** -Permanenz finden Sie unter [Speicherszenario für XML-Recordset](xml-recordset-persistence-scenario.md).

## <a name="example"></a>Beispiel

**Speichern eines Recordsets:**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Save "c:\yourFile.adtg", adPersistADTG 
```

**Öffnen einer permanenten Datei mit "Recordset.Open":**

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg", "Provider='MSPersist'",,,adCmdFile
```

Wenn das **Recordset** nicht über eine aktive Verbindung verfügt, können Sie optional alle Standardeinstellungen akzeptieren und einfach folgenden Code schreiben:

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "c:\yourFile.adtg" 
```

**Öffnen einer permanenten Datei mit "Connection.Execute":**

```vb 
 
Dim conn as New ADODB.Connection 
Dim rs as ADODB.Recordset 
conn.Open "Provider='MSPersist'" 
Set rs = conn.execute("c:\yourFile.adtg") 
```

**Öffnen einer permanenten Datei mit "RDS.DataControl":**

In diesem Fall ist die **Server** -Eigenschaft nicht festgelegt.

```vb 
 
Dim dc as New RDS.DataControl 
dc.Connection = "Provider='MSPersist'" 
dc.SQL = "c:\yourFile.adtg" 
dc.Refresh
```

