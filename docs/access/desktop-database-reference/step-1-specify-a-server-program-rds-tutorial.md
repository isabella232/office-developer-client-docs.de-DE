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
# <a name="step-1-specify-a-server-program-rds-tutorial"></a>Schritt 1: Angeben eines Serverprogramms (RDS-Lernprogramm)


**Betrifft**: Access 2013 | Office 2013

Verwenden Sie ganz allgemein die [CreateObject](createobject-method-rds.md)-Methode des [RDS.DataSpace](dataspace-object-rds.md)-Objekts zum Angeben des Standardserverprogramms, [RDSServer.DataFactory](datafactory-object-rdsserver.md), oder Ihres eigenen benutzerdefinierten Serverprogramms (Geschäftsobjekt). Ein Serverprogramm wird auf dem Server instanziiert, und ein Verweis auf das Serverprogramm bzw. den *Proxy* wird zurückgegeben.

In diesem Lernprogramm wird das Standardserverprogramm verwendet:

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
```

