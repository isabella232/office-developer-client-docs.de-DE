---
title: 'Schritt 4: Zurückgeben des Recordset-Objekts durch den Server (RDS-Lernprogramm)'
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41fd4a1aabda0887d265e3aa0ec9201b1abbbde7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475763"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a><span data-ttu-id="0a83d-102">Schritt 4: Zurückgeben des Recordset-Objekts durch den Server (RDS-Lernprogramm)</span><span class="sxs-lookup"><span data-stu-id="0a83d-102">Step 4: Server Returns the Recordset (RDS Tutorial)</span></span>


<span data-ttu-id="0a83d-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a83d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0a83d-p101">RDS konvertiert das abgerufene **Recordset**-Objekt in eine Form, die zurück an den Client gesendet werden kann (d. h. das **Recordset**-Objekt wird *gemarshallt*). In welcher Form das Objekt genau konvertiert und gesendet wird, hängt davon ab, ob sich der Server im Internet, dem Intranet oder einem LAN befindet oder ob es sich um eine DLL handelt. Diese Details ist jedoch nicht wichtig. Entscheidend ist, dass RDS das **Recordset**-Objekt zurück an den Client sendet.</span><span class="sxs-lookup"><span data-stu-id="0a83d-p101">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**). The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="0a83d-107">Auf dem Client wird ein **Recordset** -Objekt an eine lokale Variable zurückgegeben und dieser Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0a83d-107">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

