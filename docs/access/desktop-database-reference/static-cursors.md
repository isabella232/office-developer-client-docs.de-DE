---
title: Statische Cursor (Access Desktop Database Reference)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2eb019a6fc960d58771ff5ab0de7dca547c55f1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308540"
---
# <a name="static-cursors"></a><span data-ttu-id="73abd-102">Statischer Cursor</span><span class="sxs-lookup"><span data-stu-id="73abd-102">Static cursors</span></span>


<span data-ttu-id="73abd-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="73abd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="73abd-p101">Der statische Cursor zeigt das Resultset so wie beim ersten Öffnen des Cursors an. Je nach Implementierung sind statische Cursor entweder schreibgeschützt oder weisen Lese-/Schreibzugriff auf und ermöglichen den Bildlauf vorwärts und rückwärts. Änderungen an der Mitgliedschaft, der Reihenfolge oder den Werten des Resultsets nach dem Öffnen des Cursors werden gewöhnlich nicht vom Cursor erkannt. Statische Cursor erkennen möglicherweise eigene Aktualisier-, Lösch- und Einfügevorgänge, obwohl sie dies nicht müssen.</span><span class="sxs-lookup"><span data-stu-id="73abd-p101">The static cursor always displays the result set as it was when the cursor was first opened. Depending on implementation, static cursors are either read-only or read/write and provide forward and backward scrolling. The static cursor does not usually detect changes made to the membership, order, or values of the result set after the cursor is opened. Static cursors may detect their own updates, deletes, and inserts, although they are not required to do so.</span></span>

<span data-ttu-id="73abd-p102">Andere Aktualisier-, Lösch- und Einfügevorgänge werden von statischen Cursorn niemals erkannt. Angenommen, ein statischer Cursor ruft eine Zeile ab, und eine andere Anwendung aktualisiert dann diese Zeile. Falls die Anwendung die Zeile erneut vom statischen Cursor abruft, sind die Werte unverändert, trotz der Änderungen durch die andere Anwendung. Alle Bildlaufarten werden unterstützt, aber Lesezeichen werden von Anbietern unterstützt, oder auch nicht.</span><span class="sxs-lookup"><span data-stu-id="73abd-p102">Static cursors never detect other updates, deletes, and inserts. For example, suppose a static cursor fetches a row, and another application then updates that row. If the application refetches the row from the static cursor, the values it sees are unchanged, despite the changes made by the other application. All types of scrolling are supported, but providers may or may not support bookmarks.</span></span>

<span data-ttu-id="73abd-p103">Wenn Ihre Anwendung Datenänderungen nicht erkennen muss und ein Bildlauf erforderlich ist, ist der statische Cursor optimal geeignet. Verwenden Sie **adOpenStatic** für **CursorTypeEnum**, um anzuzeigen, dass Sie einen statischen Cursor in ADO verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="73abd-p103">If your application does not need to detect data changes and requires scrolling, the static cursor is the best choice. Use the **adOpenStatic** **CursorTypeEnum** to indicate that you want to use a static cursor in ADO.</span></span>

