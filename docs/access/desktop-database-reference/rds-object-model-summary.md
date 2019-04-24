---
title: Zusammenfassung des RDS-Objektmodells
TOCTitle: RDS object model summary
ms:assetid: 0355d62a-dabb-8643-5c43-1e98ccf7f3b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248800(v=office.15)
ms:contentKeyID: 48542981
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33cbdc6de644592d87b7d49e65a5c5674ad94d5b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300875"
---
# <a name="rds-object-model-summary"></a><span data-ttu-id="19f47-102">Zusammenfassung des RDS-Objektmodells</span><span class="sxs-lookup"><span data-stu-id="19f47-102">RDS object model summary</span></span>


<span data-ttu-id="19f47-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19f47-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="19f47-104">Objekt</span><span class="sxs-lookup"><span data-stu-id="19f47-104">Object</span></span></p></th>
<th><p><span data-ttu-id="19f47-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19f47-105">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="19f47-106"><a href="dataspace-object-rds.md">RDS. DataSpace</a></span><span class="sxs-lookup"><span data-stu-id="19f47-106"><a href="dataspace-object-rds.md">RDS.DataSpace</a></span></span></p></td>
<td><p><span data-ttu-id="19f47-p101">Dieses Objekt enthält eine Methode zum Abrufen eines Serverproxys. Der Proxy kann das Standardserverprogramm oder ein benutzerdefiniertes Serverprogramm (Geschäftsobjekt) sein. Das Serverprogramm kann im Internet, in einem Intranet oder in einem lokalen Netzwerk aufgerufen werden oder eine lokale Dynamic Link Library sein.</span><span class="sxs-lookup"><span data-stu-id="19f47-p101">This object contains a method to obtain a server proxy. The proxy may be the default or a custom server program (business object). The server program may be invoked on the Internet, an intranet, a local area network, or be a local dynamic-link library.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="19f47-110"><a href="datafactory-object-rdsserver.md">RDSServer. dataFactory</a></span><span class="sxs-lookup"><span data-stu-id="19f47-110"><a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a></span></span></p></td>
<td><p><span data-ttu-id="19f47-p102">Durch dieses Objekt wird das Standardserverprogramm dargestellt und das Standardverhalten für RDS-Datenabrufe und -aktualisierungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="19f47-p102">This object represents the default server program. It executes the default RDS data retrieval and update behavior.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="19f47-113"><a href="datacontrol-object-rds.md">RDS. DataControl</a></span><span class="sxs-lookup"><span data-stu-id="19f47-113"><a href="datacontrol-object-rds.md">RDS.DataControl</a></span></span></p></td>
<td><p><span data-ttu-id="19f47-114">Durch dieses Objekt können die Objekte <strong>RDS.DataSpace</strong> und <strong>RDSServer.DataFactory</strong> automatisch aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="19f47-114">This object can automatically invoke the <strong>RDS.DataSpace</strong> and <strong>RDSServer.DataFactory</strong> objects.</span></span> <span data-ttu-id="19f47-115">Verwenden Sie dieses Objekt zum Aufrufen des Standardverhaltens für RDS-Datenabrufe oder -aktualisierungen.</span><span class="sxs-lookup"><span data-stu-id="19f47-115">Use this object to invoke the default RDS data retrieval or update behavior.</span></span> <span data-ttu-id="19f47-116">Durch dieses Objekt wird außerdem die Möglichkeit bereitgestellt, durch visuelle Steuerelemente auf das zurückgegebene <strong>Recordset</strong>-Objekt zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="19f47-116">This object also provides the means for visual controls to access the returned <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

