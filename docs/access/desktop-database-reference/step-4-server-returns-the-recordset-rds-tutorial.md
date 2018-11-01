---
title: 'Schritt 4: Zurückgeben des Recordset-Objekts durch den Server (RDS-Lernprogramm)'
TOCTitle: 'Step 4: Server Returns the Recordset (RDS Tutorial)'
ms:assetid: 4503151d-de8b-98d1-1aa8-11f1b6e6b55c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249209(v=office.15)
ms:contentKeyID: 48544542
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1c7aaaa556d11fc3c457c89a35edb1240628aa9e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868623"
---
# <a name="step-4-server-returns-the-recordset-rds-tutorial"></a>Step 4: Server Returns the Recordset (RDS Tutorial)


**Betrifft**: Access 2013, Office 2013

RDS konvertiert das abgerufene **Recordset**-Objekt in eine Form, die zurück an den Client gesendet werden kann (d. h. das **Recordset**-Objekt wird *gemarshallt*). In welcher Form das Objekt genau konvertiert und gesendet wird, hängt davon ab, ob sich der Server im Internet, dem Intranet oder einem LAN befindet oder ob es sich um eine DLL handelt. Diese Details ist jedoch nicht wichtig. Entscheidend ist, dass RDS das **Recordset**-Objekt zurück an den Client sendet.

Auf dem Client wird ein **Recordset** -Objekt an eine lokale Variable zurückgegeben und dieser Variablen zugewiesen.

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

