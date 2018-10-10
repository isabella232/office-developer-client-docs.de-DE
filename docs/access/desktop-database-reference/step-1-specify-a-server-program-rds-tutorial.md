---
title: 'Schritt 1: Angeben eines Serverprogramms (RDS-Lernprogramm)'
TOCTitle: 'Step 1: Specify a Server Program (RDS Tutorial)'
ms:assetid: e6c2c624-d9bc-c899-60bc-e80a67ce8596
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250172(v=office.15)
ms:contentKeyID: 48548389
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 89aa87aa63a3d8bfdeb291f78d6525f51c4262b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472618"
---
# <a name="step-1-specify-a-server-program-rds-tutorial"></a><span data-ttu-id="89420-102">Schritt 1: Angeben eines Serverprogramms (RDS-Lernprogramm)</span><span class="sxs-lookup"><span data-stu-id="89420-102">Step 1: Specify a Server Program (RDS Tutorial)</span></span>


<span data-ttu-id="89420-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="89420-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="89420-p101">Verwenden Sie ganz allgemein die [CreateObject](createobject-method-rds.md)-Methode des [RDS.DataSpace](dataspace-object-rds.md)-Objekts zum Angeben des Standardserverprogramms, [RDSServer.DataFactory](datafactory-object-rdsserver.md), oder Ihres eigenen benutzerdefinierten Serverprogramms (Geschäftsobjekt). Ein Serverprogramm wird auf dem Server instanziiert, und ein Verweis auf das Serverprogramm bzw. den *Proxy* wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89420-p101">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="89420-106">In diesem Lernprogramm wird das Standardserverprogramm verwendet:</span><span class="sxs-lookup"><span data-stu-id="89420-106">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

