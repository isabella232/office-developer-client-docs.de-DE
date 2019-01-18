---
title: Erforderliche Anbieter für Datenmodellierung
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706674"
---
# <a name="required-providers-for-data-shaping"></a>Erforderliche Anbieter für Datenmodellierung

**Betrifft**: Access 2013, Office 2013

Für die Datenstrukturierung sind normalerweise zwei Anbieter erforderlich. Vom Dienstanbieter ([Datenstrukturierungsdienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)) wird die Datenstrukturierungsfunktionalität bereitgestellt, und von einem Datenanbieter, wie z. B. dem OLE DB-Anbieter für SQL Server, werden Zeilen mit Daten zum Auffüllen des geformten [Recordset](recordset-object-ado.md)-Objekts bereitgestellt.

Der Name des Dienstanbieters (MSDataShape) kann als Wert der [Provider](connection-object-ado.md)-Eigenschaft des [Connection](provider-property-ado.md)-Objekts oder des Verbindungszeichenfolgen-Schlüsselworts "Provider=MSDataShape;" angegeben werden.

Der Name des Datenanbieters angegeben werden kann, als der Wert der dynamischen **Datenanbieter** -Eigenschaft, die der [Properties](properties-collection-ado.md) -Auflistung des **Connection** -Objekts vom Data Shaping Dienst für OLE DB oder des Verbindungszeichenfolgen-Schlüsselworts hinzugefügt wird "* *Data Provider = *** Anbieter*".

Wenn das **Recordset**-Objekt nicht aufgefüllt wird (z. B. bei einem erstellten **Recordset**-Objekt, in dem Spalten mit dem NEW-Schlüsselwort erstellt werden), ist kein Datenprovider erforderlich. Geben Sie in diesem Fall **"Data Provider=none;"** an.

## <a name="example"></a>Beispiel

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

