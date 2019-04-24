---
title: Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen
TOCTitle: Granting guest privileges to a web server computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8c0ee29125bf06ef51d1ac511838bdd09231e1a6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292125"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="66cf3-102">Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen</span><span class="sxs-lookup"><span data-stu-id="66cf3-102">Granting guest privileges to a web server computer; RDS guest privileges</span></span>

<span data-ttu-id="66cf3-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="66cf3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="66cf3-104">Das anonyme Webserverkonto (IUSR\_*Computername*) muss der lokalen Gruppe "Gäste" auf dem Webservercomputer hinzugefügt werden, um RDS verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="66cf3-104">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="66cf3-105">**So gewähren Sie einem Webservercomputer Gastberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="66cf3-105">**To grant guest privileges to a web server computer**</span></span>

1.  <span data-ttu-id="66cf3-106">Klicken Sie auf dem Computer mit Microsoft Windows 2000-Server auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Computerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-106">On your Microsoft Windows 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="66cf3-107">Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-107">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="66cf3-p101">Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="66cf3-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="66cf3-110">Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-110">In the **Guests Properties** dialog box, click **Add**.</span></span>

5.  <span data-ttu-id="66cf3-111">Wenn das anonyme Webserverkonto nicht in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** angezeigt wird, geben Sie den Namen (IUSR\_*Computer*Name) in das untere leere Feld ein, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-111">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>

6.  <span data-ttu-id="66cf3-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="66cf3-112">Click **OK**.</span></span>

