---
title: RDS-Lernprogramm (Visual J++)
TOCTitle: RDS Tutorial (Visual J++)
ms:assetid: b5679bfe-e830-05df-8a1c-0744c96abe90
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249870(v=office.15)
ms:contentKeyID: 48547248
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15eadc36079faa529585e539b67eb0da246cf4bc
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474235"
---
# <a name="rds-tutorial-visual-j"></a>RDS-Lernprogramm (Visual J++)


**Betrifft**: Access 2013 | Office 2013

ADO/WFC entspricht insofern, als das [RDS.DataControl](datacontrol-object-rds.md)-Objekt nicht implementiert wird, nicht vollständig dem RDS-Objektmodell. ADO/WFC implementiert lediglich die clientseitige Klasse [RDS.DataSpace](dataspace-object-rds.md).

Die **DataSpace** -Klasse implementiert eine [CreateObject](createobject-method-rds.md)-Methode, die wiederum ein [ObjectProxy](https://msdn.microsoft.com/library/jj249624\(v=office.15\))-Objekt zurückgibt. Die **DataSpace** -Klasse implementiert auch die [InternetTimeout](internettimeout-property-rds.md)-Eigenschaft.

Die ObjectProxy-Klasse implementiert die call-Methode, die jedes beliebige serverseitige Geschäftsobjekt aufrufen kann.

**Dies ist der Anfang des Lernprogramms.**

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

**Dies ist das Ende des Lernprogramms.**

