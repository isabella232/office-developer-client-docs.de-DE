---
title: Gewähren einem Webservercomputer Gastberechtigungen; RDS-Gastberechtigungen
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1f127e4ea9393d3b461e9b7da2901df554ee36b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947210"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="2708c-102">Gewähren einem Webservercomputer Gastberechtigungen; RDS-Gastberechtigungen</span><span class="sxs-lookup"><span data-stu-id="2708c-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="2708c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2708c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2708c-104">Das anonyme Webserverkonto (IUSR\_*ComputerName*) der lokalen Gruppe Gäste auf dem Webservercomputer Verwendung von RDS hinzugefügt werden müssen</span><span class="sxs-lookup"><span data-stu-id="2708c-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="2708c-105">**So erteilen einem Webservercomputer Gastberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="2708c-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="2708c-106">Klicken Sie auf dem Microsoft Windows 2000 Server-Computer auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Computerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="2708c-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="2708c-107">Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="2708c-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="2708c-p101">Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="2708c-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="2708c-110">Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2708c-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="2708c-111">Wenn das anonyme Webserverkonto in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** nicht angezeigt wird, geben Sie deren Namen (IUSR\_*ComputerName*) in der unteren leer Feld, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="2708c-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="2708c-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2708c-112">Click **OK**.</span></span>

