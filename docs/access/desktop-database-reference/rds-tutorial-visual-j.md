---
title: RDS-Lernprogramm (Visual J++)
TOCTitle: RDS Tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6b01809cd17c9c1a5c1a73a5765bb8808692e4c2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877919"
---
# <a name="rds-tutorial-visual-j"></a><span data-ttu-id="cb4fc-102">RDS-Lernprogramm (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="cb4fc-102">RDS Tutorial (Visual J++)</span></span>


<span data-ttu-id="cb4fc-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb4fc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb4fc-p101">ADO/WFC entspricht insofern, als das [RDS.DataControl](datacontrol-object-rds.md)-Objekt nicht implementiert wird, nicht vollständig dem RDS-Objektmodell. ADO/WFC implementiert lediglich die clientseitige Klasse [RDS.DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="cb4fc-p101">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="cb4fc-p102">Die **DataSpace** -Klasse implementiert eine [CreateObject](createobject-method-rds.md)-Methode, die wiederum ein [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\))-Objekt zurückgibt. Die **DataSpace** -Klasse implementiert auch die [InternetTimeout](internettimeout-property-rds.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cb4fc-p102">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\)) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="cb4fc-108">Die ObjectProxy-Klasse implementiert die call-Methode, die jedes beliebige serverseitige Geschäftsobjekt aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="cb4fc-108">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

<span data-ttu-id="cb4fc-109">**Dies ist der Anfang des Lernprogramms.**</span><span class="sxs-lookup"><span data-stu-id="cb4fc-109">**This is the beginning of the tutorial.**</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```

<span data-ttu-id="cb4fc-110">**Dies ist das Ende des Lernprogramms.**</span><span class="sxs-lookup"><span data-stu-id="cb4fc-110">**This is the end of the tutorial.**</span></span>

