---
title: Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 213e405718d50369367d439457e8026d4ef71242
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937505"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="64e1e-102">Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen</span><span class="sxs-lookup"><span data-stu-id="64e1e-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="64e1e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64e1e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64e1e-104">Das anonyme Webserverkonto (IUSR\_*ComputerName*) der lokalen Gruppe Gäste auf dem Webservercomputer Verwendung von RDS hinzugefügt werden müssen</span><span class="sxs-lookup"><span data-stu-id="64e1e-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="64e1e-105">**So erteilen einem Webservercomputer Gastberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="64e1e-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="64e1e-106">Klicken Sie auf dem Microsoft Windows 2000 Server-Computer auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Computerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="64e1e-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="64e1e-107">Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="64e1e-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="64e1e-p101">Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="64e1e-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="64e1e-110">Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="64e1e-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="64e1e-111">Wenn das anonyme Webserverkonto in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** nicht angezeigt wird, geben Sie deren Namen (IUSR\_*ComputerName*) in der unteren leer Feld, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="64e1e-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="64e1e-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="64e1e-112">Click **OK**.</span></span>

