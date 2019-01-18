---
title: 'Alternativen: Verwenden von SQL-Anweisungen'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 185f5c1eb7e11a9425ff6cc4a16f1387424f3219
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711350"
---
# <a name="alternatives-using-sql-statements"></a>Alternativen: Verwenden von SQL-Anweisungen


**Betrifft**: Access 2013, Office 2013

ADO ermöglicht alternativ zu den integrierten Eigenschaften und Methoden auch die Verwendung von Befehlen zum Bearbeiten von Daten. In Abhängigkeit von Ihrem Anbieter könnten alle in diesem Kapitel beschriebenen Vorgänge auch durch Übergeben von Befehlen an die Datenquelle ausgeführt werden. Beispielsweise können mit UPDATE-SQL-Anweisungen Daten geändert werden, ohne dass die **Value** -Eigenschaft eines **Field** -Objekts verwendet wird. Anstelle der **AddNew** -Methode von ADO können einer Datenquelle mit INSERT-SQL-Anweisungen neue Datensätze hinzugefügt werden. Weitere Informationen zu SQL oder zur Datenbearbeitungssprache Ihres Anbieters finden Sie in der Dokumentation Ihrer Datenquelle.

Beispielsweise können Sie wie im folgenden Code veranschaulicht eine SQL-Zeichenfolge, die eine DELETE-Anweisung enthält, an eine Datenbank übergeben:

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

