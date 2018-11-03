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
# <a name="step-3-server-obtains-a-recordset-rds-tutorial"></a><span data-ttu-id="b5993-102">Schritt 3: Server erhält ein Recordset-Objekt (RDS-Lernprogramm)</span><span class="sxs-lookup"><span data-stu-id="b5993-102">Step 3: Server obtains a Recordset (RDS Tutorial)</span></span>

<span data-ttu-id="b5993-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b5993-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b5993-p101">Das Serverprogramm verwendet die Verbindungszeichenfolge und den Befehlstext, um die gewünschten Zeilen in der Datenquelle abzufragen. In der Regel wird ADO zum Abrufen dieses **Recordset** -Objekts verwendet, obwohl auch andere Datenzugriffsschnittstellen verwendet werden könnten (z. B. OLE DB).</span><span class="sxs-lookup"><span data-stu-id="b5993-p101">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="b5993-106">Ein benutzerdefiniertes Serverprogramm kann folgendermaßen aussehen:</span><span class="sxs-lookup"><span data-stu-id="b5993-106">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

