---
title: Visual J++ (Access PC-Datenbank-Referenz)
TOCTitle: Visual J++
ms:assetid: 5c05db85-cdf2-9a73-fbc5-3dbfa6752376
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249320(v=office.15)
ms:contentKeyID: 48545079
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d40a820b5ee3bd6e5c423cbb963a4514d4ff40e1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874545"
---
# <a name="visual-j"></a><span data-ttu-id="57fca-102">Visual J++</span><span class="sxs-lookup"><span data-stu-id="57fca-102">Visual J++</span></span>


<span data-ttu-id="57fca-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57fca-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57fca-104">Dieses kurze Microsoft Visual J++-Beispiel zeigt, wie Sie einem bestimmten Ereignis Ihre eigene Funktion zuordnen können.</span><span class="sxs-lookup"><span data-stu-id="57fca-104">This short Microsoft Visual J++ example shows how you can associate your own function with a particular event.</span></span>

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

<span data-ttu-id="57fca-105">Zunächst wird die Klasse-Methode *OnConnectionComplete* erstellen ein neues **ConnectionEventHandler** -Objekt, und weisen die *OnConnectComplete* -Funktion, um das Objekt dem **ConnectionComplete** -Ereignis zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="57fca-105">First, the class method *onConnectionComplete* is associated with the **ConnectionComplete** event by creating a new **ConnectionEventHandler** object and assigning the *onConnectComplete* function to the object.</span></span>

<span data-ttu-id="57fca-106">Die *main* -Funktion wird dann ein **Connection** -Objekt erstellt und ermöglicht die Ereignisbehandlung durch Aufrufen der **AddOnConnectComplete** -Methode und durch Übergeben der Adresse der *Handler* -Funktion.</span><span class="sxs-lookup"><span data-stu-id="57fca-106">The *main* function then creates a **Connection** object and enables event handling by calling the **addOnConnectComplete** method and passing it the address of the *handler* function.</span></span>

