---
title: Erforderliche Anbieter für Datenmodellierung
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3de8c0731a7133cb053c715ef3a2254a0cdae9e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576933"
---
# <a name="required-providers-for-data-shaping"></a>Erforderliche Anbieter für Datenmodellierung

**Gilt für**: Access 2013, Office 2013

Für die Datenstrukturierung sind normalerweise zwei Anbieter erforderlich. Vom Dienstanbieter ([Datenstrukturierungsdienst für OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md)) wird die Datenstrukturierungsfunktionalität bereitgestellt, und von einem Datenanbieter, wie z. B. dem OLE DB-Anbieter für SQL Server, werden Zeilen mit Daten zum Auffüllen des geformten [Recordset](recordset-object-ado.md)-Objekts bereitgestellt.

Der Name des Dienstanbieters (MSDataShape) kann als Wert der [Provider](provider-property-ado.md)-Eigenschaft des [Connection](connection-object-ado.md)-Objekts oder des Verbindungszeichenfolgen-Schlüsselworts "Provider=MSDataShape;" angegeben werden.

Der Name des Datenproviders kann als Wert der dynamischen **Data Provider**-Eigenschaft angegeben werden, die vom Datenstrukturierungsdienst für OLE DB der [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts oder zum Verbindungszeichenfolgen-Schlüsselwort "**Data Provider=**_provider_" hinzugefügt wird.

Wenn das **Recordset**-Objekt nicht aufgefüllt wird (z. B. bei einem erstellten **Recordset**-Objekt, in dem Spalten mit dem NEW-Schlüsselwort erstellt werden), ist kein Datenprovider erforderlich. Geben Sie in diesem Fall **"Data Provider=none;"** an.

## <a name="example"></a>Beispiel

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

