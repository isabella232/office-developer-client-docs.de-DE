---
title: Vorwärtscursor
TOCTitle: Forward-Only Cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 176dc9fe3820b88ddaf0bd27feb4aacbbcb311cc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886284"
---
# <a name="forward-only-cursors"></a><span data-ttu-id="f67c6-102">Vorwärtscursor</span><span class="sxs-lookup"><span data-stu-id="f67c6-102">Forward-Only Cursors</span></span>


<span data-ttu-id="f67c6-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f67c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f67c6-p101">Der typische Standardcursortyp, der so genannte Vorwärtscursor (oder Cursor ohne Bildlauf), kann im Resultset nur vorwärts navigieren. Der Bildlauf (die Möglichkeit, im Resultset vorwärts und rückwärts zu navigieren) wird von diesem Cursortyp nicht unterstützt. Es können vielmehr nur Zeilen vom Anfang bis zum Ende des Resultsets abgerufen werden. Bei einigen Vorwärtscursorn (z. B. bei der SQL Server-Cursorbibliothek), werden alle Einfügungs-, Aktualisierungs- und Löschanweisungen des aktuellen Benutzers (oder anderer Benutzer), die Zeilen im Resultset betreffen, beim Abrufen der Zeilen angezeigt. Für den Cursor ist kein Bildlauf rückwärts möglich, weshalb Änderungen, die nach dem Abrufen von Zeilen in der Datenbank an diesen vorgenommen werden, mit diesem Cursor nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f67c6-p101">The typical default cursor type, called a forward-only (or non-scrollable) cursor, can move only forward through the result set. A forward-only cursor does not support scrolling (the ability to move forward and backward in the result set); it only supports fetching rows from the start to the end of the result set. With some forward-only cursors (such as with the SQL Server cursor library), all insert, update, and delete statements made by the current user (or committed by other users) that affect rows in the result set are visible as the rows are fetched. Because the cursor cannot be scrolled backward, however, changes made to rows in the database after the row was fetched are not visible through the cursor.</span></span>

<span data-ttu-id="f67c6-p102">Nachdem die Daten für die aktuelle Zeile verarbeitet wurden, gibt der Vorwärtscursor die Ressourcen frei, mit denen diese Daten gespeichert wurden. Vorwärtscursor sind standardmäßig dynamisch, weshalb alle Änderungen beim Verarbeiten der aktuellen Zeile erkannt werden. Dadurch kann der Cursor schneller geöffnet werden, und im Resultset können Aktualisierungen an den zugrunde liegenden Tabellen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f67c6-p102">After the data for the current row is processed, the forward-only cursor releases the resources that were used to hold that data. Forward-only cursors are dynamic by default, meaning that all changes are detected as the current row is processed. This provides faster cursor opening and enables the result set to display updates made to the underlying tables.</span></span>

<span data-ttu-id="f67c6-p103">Der Bildlauf rückwärts wird zwar von Vorwärtscursorn nicht unterstützt, aber die Anwendung kann wieder an den Anfang des Resultsets zurückgesetzt werden, indem der Cursor geschlossen und erneut geöffnet wird. Dies ist eine effiziente Arbeitsweise für kleine Datenmengen. Als Alternative könnte die Anwendung das Resultset einmal lesen, die Daten lokal zwischenspeichern und dann den lokalen Datencache durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="f67c6-p103">While forward-only cursors do not support backward scrolling, your application can return to the beginning of the result set by closing and reopening the cursor. This is an effective way to work with small amounts of data. As an alternative, your application could read the result set once, cache the data locally, and then browse the local data cache.</span></span>

<span data-ttu-id="f67c6-p104">Wenn für die Anwendung kein Bildlauf im Resultset erforderlich ist, ist der Vorwärtscursor optimal geeignet, um Daten schnell und mit dem geringsten Arbeitsaufwand abzurufen. Verwenden Sie **adOpenForwardOnly** für **CursorTypeEnum**, um anzugeben, dass Sie einen Vorwärtscursor in ADO verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="f67c6-p104">If your application does not require scrolling through the result set, the forward-only cursor is the best way to retrieve data quickly with the least amount of overhead. Use the **adOpenForwardOnly** **CursorTypeEnum** to indicate that you want to use a forward-only cursor in ADO.</span></span>

