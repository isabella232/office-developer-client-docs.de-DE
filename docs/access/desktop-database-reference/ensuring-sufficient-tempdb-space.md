---
title: Sicherstellen von ausreichend Speicherplatz für TempDB
TOCTitle: Ensuring Sufficient TempDB Space
ms:assetid: 2729c118-ec8b-1fcb-4a90-56b57823b24c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249034(v=office.15)
ms:contentKeyID: 48543830
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b08980b7bb852a497ea339f4c43d439ac16a7e5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885766"
---
# <a name="ensuring-sufficient-tempdb-space"></a><span data-ttu-id="1bf4b-102">Sicherstellen von ausreichend Speicherplatz für TempDB</span><span class="sxs-lookup"><span data-stu-id="1bf4b-102">Ensuring Sufficient TempDB Space</span></span>


<span data-ttu-id="1bf4b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1bf4b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1bf4b-p101">Falls bei der Bearbeitung von [Recordset](recordset-object-ado.md)-Objekten, die Verarbeitungskapazitäten von Microsoft SQL Server 6.5 benötigen, Fehler auftreten, müssen Sie möglicherweise TempDB vergrößern. (Einige Abfragen erfordern temporäre Verarbeitungskapazitäten. Eine Abfrage mit einer ORDER BY-Klausel erfordert z. B. eine Sortierung des **Recordset** -Objekts, was temporären Speicherplatz in Anspruch nimmt.)</span><span class="sxs-lookup"><span data-stu-id="1bf4b-p101">If errors occur while handling [Recordset](recordset-object-ado.md) objects that need processing space on Microsoft SQL Server 6.5, you may need to increase the size of the TempDB. (Some queries require temporary processing space; for example, a query with an ORDER BY clause requires a sort of the **Recordset**, which requires some temporary space.)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1bf4b-106">[!WICHTIG] Lesen Sie dieses Verfahren zuerst durch, bevor Sie die Aktionen ausführen, da ein Medium schwer wieder zu verkleinern ist, nachdem es vergrößert wurde.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-106">Read through this procedure before performing the actions because it isn't as easy to shrink a device once it is expanded.</span></span>

> [!NOTE]
> <span data-ttu-id="1bf4b-p102">[!HINWEIS] In Microsoft SQL Server 7.0 oder höher ist TempDB standardmäßig so eingerichtet, dass eine automatische Vergrößerung stattfindet. Dieses Verfahren ist deshalb möglicherweise nur bei Servern erforderlich, auf denen niedrigere Versionen als 7.0 ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-p102">By default in Microsoft SQL Server 7.0 and later, TempDB is set to automatically grow as needed. Therefore, this procedure may only be necessary on servers running versions earlier than 7.0.</span></span>



<span data-ttu-id="1bf4b-109">**So vergrößern Sie den Speicherplatz von TempDB in SQL Server 6.5**</span><span class="sxs-lookup"><span data-stu-id="1bf4b-109">**To increase the TempDB space on SQL Server 6.5**</span></span>

1.  <span data-ttu-id="1bf4b-110">Starten Sie Microsoft® SQL Server Enterprise Manager, erweitern Sie die Struktur für den Server, und erweitern Sie dann die Struktur der Datenbankmedien.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-110">Start Microsoft® SQL Server Enterprise Manager, open the tree for the Server, and then open the Database Devices tree.</span></span>

2.  <span data-ttu-id="1bf4b-p103">Wählen Sie ein (physisches) Medium zum Vergrößern aus, z. B. Master, und doppelklicken Sie auf das Medium, um das Dialogfeld **Datenbankmedium bearbeiten** zu öffnen. Dieses Dialogfeld zeigt, wie viel Speicherplatz die aktuellen Datenbanken belegen.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-p103">Select a (physical) device to expand, such as Master, and double-click the device to open the **Edit Database Device** dialog box. This dialog box shows how much space the current databases are using.</span></span>

3.  <span data-ttu-id="1bf4b-113">Erweitern Sie im Feld **Größe** das Medium auf die gewünschte Größe (z. B. 50 MB Festplattenspeicher).</span><span class="sxs-lookup"><span data-stu-id="1bf4b-113">In the **Size** box, increase the device to the desired amount (for example, 50 megabytes (MB) of hard disk space).</span></span>

4.  <span data-ttu-id="1bf4b-114">Klicken Sie auf **Jetzt ändern**, um den Speicherplatz zu vergrößern, den die (logische) TempDB maximal belegen kann.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-114">Click **Change Now** to increase the amount of space to which the (logical) TempDB can expand.</span></span>

5.  <span data-ttu-id="1bf4b-p104">Erweitern Sie die Struktur der Datenbanken auf dem Server, und doppelklicken Sie auf **TempDB**, um das Dialogfeld **Datenbank bearbeiten** zu öffnen. Auf der Registerkarte **Datenbank** wird der Speicherplatz aufgeführt, der aktuell für TempDB reserviert ist (**Datengröße**). Standardmäßig sind das 2 MB.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-p104">Open the Databases tree on the server, and then double-click **TempDB** to open the **Edit Database** dialog box. The **Database** tab lists the amount of space currently allocated to TempDB (**Data Size**). By default, this is 2 MB.</span></span>

6.  <span data-ttu-id="1bf4b-p105">Klicken Sie in der Gruppe **Größe** auf **Vergrößern**. Das Diagramm zeigt den verfügbaren und den reservierten Speicherplatz aller physischen Medien an. Die braunen Balken stellen den verfügbaren Speicherplatz dar.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-p105">Under the **Size** group, click **Expand**. The graphs show the available and allocated space on each of the physical devices. The bars in maroon color represent available space.</span></span>

7.  <span data-ttu-id="1bf4b-121">Wählen Sie ein Protokollmedium aus, z. B. **Master**, um den verfügbaren Speicherplatz im Feld **Größe (MB)** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-121">Select a **Log Device**, such as Master, to display the available size in the **Size (MB)** box.</span></span>

8.  <span data-ttu-id="1bf4b-p106">Klicken Sie auf **Jetzt erweitern**, um diesen Speicherplatz für die TempDB-Datenbank zu reservieren. Das Dialogfeld **Datenbank bearbeiten** zeigt die neu reservierte Größe für TempDB an.</span><span class="sxs-lookup"><span data-stu-id="1bf4b-p106">Click **Expand Now** to allocate that space to the TempDB database. The **Edit Database** dialog box displays the new allocated size for TempDB.</span></span>

<span data-ttu-id="1bf4b-124">Weitere Informationen zu diesem Thema finden Sie in der Hilfe zu Microsoft SQL Server Enterprise Manager unter Datenbank vergrößern (Dialogfeld).</span><span class="sxs-lookup"><span data-stu-id="1bf4b-124">For more information about this topic, search the Microsoft SQL Server Enterprise Manager Help file for "Expand Database dialog box."</span></span>

