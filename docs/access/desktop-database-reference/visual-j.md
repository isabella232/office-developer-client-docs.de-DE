---
title: Visual J++ (Access Desktop Database Reference)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: da13ae0f10e2338b961f2f12686bd378580a69d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311333"
---
# <a name="visual-j"></a>Visual J++


**Gilt für**: Access 2013, Office 2013

Dieses kurze Microsoft Visual J++-Beispiel zeigt, wie Sie einem bestimmten Ereignis Ihre eigene Funktion zuordnen können.

```java 
 
// BeginEventExampleVJ 
import com.ms.wfc.data.*; 
 
public class EventExampleVJ 
{ 
 ConnectionEventHandler handler = new ConnectionEventHandler(this,"onConnectComplete"); 
 
 public void onConnectComplete(Object sender,ConnectionEvent e) 
 { 
 if (e.adStatus == AdoEnums.EventStatus.ERRORSOCCURRED) 
 System.out.println("Connection failed"); 
 else 
 System.out.println("Connection completed"); 
 return; 
 } 
 
 public static void main (String[] args) 
 { 
 EventExampleVJ Class1 = new EventExampleVJ(); 
 Connection conn = new Connection(); 
 
 conn.addOnConnectComplete(Class1.handler); // Enable event support. 
 conn.open("DSN=Pubs"); 
 conn.close(); 
 conn.removeOnConnectComplete(Class1.handler); // Disable event support. 
 } 
} 
// EndEventExampleVJ 
```

Zunächst wird die *onConnectionComplete*-Klassenmethode dem **ConnectionComplete**-Ereignis zugeordnet, indem ein neues **ConnectionEventHandler**-Objekt erstellt und die *onConnectComplete*-Funktion diesem Objekt zugewiesen wird.

Die *main*-Funktion erstellt dann ein **Connection**-Objekt und ermöglicht die Ereignisbehandlung durch Aufrufen der **addOnConnectComplete**-Methode und durch Übergeben der Adresse der *handler*-Funktion.

