---
title: Erforderliche Anbieter für die Datenstrukturierung
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41b8c7b34aa8a0da7a360dbdca5b396bb9f2b4b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475770"
---
# <a name="required-providers-for-data-shaping"></a>Erforderliche Anbieter für die Datenstrukturierung


**Betrifft**: Access 2013 | Office 2013

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

