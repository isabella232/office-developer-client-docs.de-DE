---
title: Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen
TOCTitle: Granting Guest Privileges to a Web Server Computer; RDS guest privileges
ms:assetid: 4ec9c05b-36f6-de22-b848-0cb8573f9dd1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249254(v=office.15)
ms:contentKeyID: 48544766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bee4c05e3adc0fa3ad722b5c82c63f315860e12c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604113"
---
# <a name="granting-guest-privileges-to-a-web-server-computer-rds-guest-privileges"></a><span data-ttu-id="6a5b5-102">Gewähren von Gastberechtigungen für einen Webservercomputer; RDS-Gastberechtigungen</span><span class="sxs-lookup"><span data-stu-id="6a5b5-102">Granting Guest Privileges to a Web Server Computer; RDS guest privileges</span></span> 


<span data-ttu-id="6a5b5-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a5b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6a5b5-104"><<<<<<< HEAD-das anonyme Webserverkonto (IUSR\_*ComputerName*) der lokalen Gruppe Gäste auf dem Webservercomputer Verwendung von RDS hinzugefügt werden müssen</span><span class="sxs-lookup"><span data-stu-id="6a5b5-104"><<<<<<< HEAD The anonymous Web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the Web server computer to use RDS.</span></span>

<a name="to-grant-guest-privileges-to-a-web-server-computer"></a><span data-ttu-id="6a5b5-105">**So gewähren Sie einem Webservercomputer Gastberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-105">**To grant guest privileges to a Web server computer**</span></span>
=======
<span data-ttu-id="6a5b5-106">Das anonyme Webserverkonto (IUSR\_*ComputerName*) der lokalen Gruppe Gäste auf dem Webservercomputer Verwendung von RDS hinzugefügt werden müssen</span><span class="sxs-lookup"><span data-stu-id="6a5b5-106">The anonymous web server account (IUSR\_*ComputerName*) must be added to the Guests local group on the web server computer to use RDS.</span></span>

<span data-ttu-id="6a5b5-107">**So erteilen einem Webservercomputer Gastberechtigungen**</span><span class="sxs-lookup"><span data-stu-id="6a5b5-107">**To grant guest privileges to a web server computer**</span></span>
>>>>>>> <span data-ttu-id="6a5b5-108">master</span><span class="sxs-lookup"><span data-stu-id="6a5b5-108">master</span></span>

1.  <span data-ttu-id="6a5b5-109">Klicken Sie auf dem Computer unter Microsoft Windows® 2000 Server auf **Start**, zeigen Sie auf **Programme**, zeigen Sie auf **Verwaltung**, und klicken Sie dann auf **Computerverwaltung**.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-109">On your Microsoft Windows® 2000 Server computer, click **Start**, point to **Programs**, point to **Administrative Tools**, and then click **Computer Management**.</span></span>

2.  <span data-ttu-id="6a5b5-110">Klicken Sie in der Konsolenstruktur in **Lokale Benutzer und Gruppen** auf **Gruppen**.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-110">In the console tree, in **Local Users and Groups**, click **Groups**.</span></span>

3.  <span data-ttu-id="6a5b5-p101">Wählen Sie die lokale Gruppe **Gäste** aus. Wählen Sie im Menü **Aktion** die Option **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-p101">Select the **Guests** local group. From the **Action** menu, choose **Properties**.</span></span>

4.  <span data-ttu-id="6a5b5-113">Klicken Sie im Dialogfeld **Eigenschaften von Gäste** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-113">In the **Guests Properties** dialog box, click **Add**.</span></span>

<span data-ttu-id="6a5b5-114"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="6a5b5-114"><<<<<<< HEAD</span></span>
5.  <span data-ttu-id="6a5b5-115">Wenn das anonyme Webserverkonto in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** nicht angezeigt wird, geben Sie deren Namen (IUSR\_*ComputerName*) in der unteren leer Feld, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-115">If the anonymous Web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>
=======
5.  <span data-ttu-id="6a5b5-116">Wenn das anonyme Webserverkonto in der Liste im Dialogfeld **Benutzer oder Gruppen auswählen** nicht angezeigt wird, geben Sie deren Namen (IUSR\_*ComputerName*) in der unteren leer Feld, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-116">If the anonymous web server account does not appear in the list in the **Select Users or Groups** dialog box, type its name (IUSR\_*ComputerName*) into the bottom blank box, and then click **Add**.</span></span>
>>>>>>> <span data-ttu-id="6a5b5-117">master</span><span class="sxs-lookup"><span data-stu-id="6a5b5-117">master</span></span>

6.  <span data-ttu-id="6a5b5-118">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a5b5-118">Click **OK**.</span></span>

