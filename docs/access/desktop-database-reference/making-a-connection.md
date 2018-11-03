---
title: Herstellen einer Verbindung
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0335c4bbc0d1240d6d4ca53ceacf47bf44fce67d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945887"
---
# <a name="making-a-connection"></a>Herstellen einer Verbindung

**Betrifft**: Access 2013, Office 2013

Zum Herstellen einer Verbindung mit einer Datenquelle müssen Sie eine *Verbindungszeichenfolge* angeben, deren Parameter je nach Anbieter und Datenquelle variieren können. Weitere Informationen finden Sie unter [Erstellen der Verbindungszeichenfolge](creating-the-connection-string.md).

ADO öffnet eine Verbindung in der Regel mithilfe der **Open** -Methode des **Connection** -Objekts. Die Syntax für die **Open** -Methode ist im Folgenden dargestellt:

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Alternativ können Sie den Kurzbefehl **Recordset.Open** verwenden, um eine implizite Verbindung zu öffnen und einen Befehl für diese Verbindung in einem Schritt auszustellen. Zu diesem Zweck in eine gültige Verbindungszeichenfolge als *ActiveConnection* -Argument an die **Open** -Methode übergeben. Es folgt die Syntax für die verschiedenen Methoden in Visual Basic:

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!HINWEIS] Wann sollten Sie ein **Connection** -Objekt und wann den Kurzbefehl **Recordset.Open** verwenden? Verwenden Sie das **Connection** -Objekt, falls Sie mehrere **Recordset** -Objekte öffnen möchten, oder wenn Sie mehrere Befehle ausführen. Mit dem Kurzbefehl **Recordset.Open** wird von ADO weiterhin implizit eine Verbindung erstellt.


