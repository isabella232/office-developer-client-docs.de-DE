---
title: 'Schritt 3: Abrufen eines Recordset-Objekts durch den Server (RDS-Lernprogramm)'
TOCTitle: 'Step 3: Server Obtains a Recordset (RDS Tutorial)'
ms:assetid: fadb6a9b-ed44-264f-22fd-26b121f98040
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250282(v=office.15)
ms:contentKeyID: 48548856
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ddd306e95ccf9ed68848b516c6d23d45286edf63
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25943836"
---
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a>Schritt 3: Server erhält ein Recordset-Objekt (RDS-Lernprogramm)

**Betrifft**: Access 2013, Office 2013

Das Serverprogramm verwendet die Verbindungszeichenfolge und den Befehlstext, um die gewünschten Zeilen in der Datenquelle abzufragen. In der Regel wird ADO zum Abrufen dieses **Recordset** -Objekts verwendet, obwohl auch andere Datenzugriffsschnittstellen verwendet werden könnten (z. B. OLE DB).

Ein benutzerdefiniertes Serverprogramm kann folgendermaßen aussehen:

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

