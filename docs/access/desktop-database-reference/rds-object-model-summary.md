---
title: RDS-Objektmodell (Zusammenfassung)
TOCTitle: RDS Object Model Summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4afb0309018b12267f29c23bcde740fdb5a9664e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474548"
---
# <a name="rds-object-model-summary"></a>RDS-Objektmodell (Zusammenfassung)


**Betrifft**: Access 2013 | Office 2013

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objekt</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="dataspace-object-rds.md">RDS. DataSpace</a></p></td>
<td><p>Dieses Objekt enthält eine Methode zum Abrufen eines Serverproxys. Der Proxy kann das Standardserverprogramm oder ein benutzerdefiniertes Serverprogramm (Geschäftsobjekt) sein. Das Serverprogramm kann im Internet, in einem Intranet oder in einem lokalen Netzwerk aufgerufen werden oder eine lokale Dynamic Link Library sein.</p></td>
</tr>
<tr class="even">
<td><p><a href="datafactory-object-rdsserver.md">"RDSServer.DataFactory"</a></p></td>
<td><p>Durch dieses Objekt wird das Standardserverprogramm dargestellt und das Standardverhalten für RDS-Datenabrufe und -aktualisierungen ausgeführt.</p></td>
</tr>
<tr class="odd">
<td><p><a href="datacontrol-object-rds.md">RDS. DataControl</a></p></td>
<td><p>Durch dieses Objekt können die Objekte <strong>RDS.DataSpace</strong> und <strong>RDSServer.DataFactory</strong> automatisch aufgerufen werden.
 Verwenden Sie dieses Objekt zum Aufrufen des Standardverhaltens für RDS-Datenabrufe oder -aktualisierungen. Durch dieses Objekt wird außerdem die Möglichkeit bereitgestellt, durch visuelle Steuerelemente auf das zurückgegebene <strong>Recordset</strong>-Objekt zuzugreifen.</p></td>
</tr>
</tbody>
</table>

