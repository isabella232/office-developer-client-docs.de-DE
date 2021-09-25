---
title: Visual J++ (Access-Desktopdatenbankreferenz)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 93952438594d87e9985d44f22ca4e071a974e5f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572529"
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

