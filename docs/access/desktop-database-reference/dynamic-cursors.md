---
title: Dynamische Cursor (Access Desktop Database Reference)
TOCTitle: Dynamic cursors
ms:assetid: ae599d86-6b89-6103-fda1-c899a6138e1d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249823(v=office.15)
ms:contentKeyID: 48547068
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ee81b2bd0e7d40b3a426c6416111d21e2ec760c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293637"
---
# <a name="dynamic-cursors"></a><span data-ttu-id="62ec1-102">Dynamischer Cursor</span><span class="sxs-lookup"><span data-stu-id="62ec1-102">Dynamic cursors</span></span>


<span data-ttu-id="62ec1-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="62ec1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="62ec1-p101">Dynamische Cursor erkennen alle Änderungen, die an den Zeilen im Resultset vorgenommen werden, unabhängig davon, ob die Änderungen innerhalb des Cursors oder durch andere Benutzer außerhalb des Cursors vorgenommen werden. Alle Einfügungs-, Aktualisierungs- und Löschanweisungen aller Benutzer sind über den Cursor sichtbar. Der dynamische Cursor kann alle Änderungen, die an den Zeilen, der Reihenfolge und den Werten im Resultset nach dem Öffnen des Cursors vorgenommen werden, erkennen. Aktualisierungen außerhalb des Cursors sind erst nach einem Commit sichtbar (außer für die Transaktionsisolationsstufe des Cursors ist "uncommitted" festgelegt).</span><span class="sxs-lookup"><span data-stu-id="62ec1-p101">Dynamic cursors detect all changes made to the rows in the result set, regardless of whether the changes occur from inside the cursor or by other users outside the cursor. All insert, update, and delete statements made by all users are visible through the cursor. The dynamic cursor can detect any changes made to the rows, order, and values in the result set after the cursor is opened. Updates made outside the cursor are not visible until they are committed (unless the cursor transaction isolation level is set to "uncommitted").</span></span>

<span data-ttu-id="62ec1-p102">Angenommen, ein dynamischer Cursor ruft zwei Zeilen und eine andere Anwendung ab und aktualisiert die eine Zeile und löscht die andere Zeile. Falls der dynamische Cursor dann diese Zeilen abruft, wird die gelöschte Zeile nicht gefunden, aber die neuen Werte für die aktualisierte Zeile werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="62ec1-p102">For example, suppose a dynamic cursor fetches two rows and another application, and then updates one of those rows and deletes the other. If the dynamic cursor then fetches those rows, it will not find the deleted row, but it will display the new values for the updated row.</span></span>

<span data-ttu-id="62ec1-p103">Der dynamische Cursor ist gut geeignet, falls die Anwendung alle gleichzeitigen Aktualisierungen, die von anderen Benutzern vorgenommen werden, erkennen muss. Verwenden Sie **adOpenDynamic** für **CursorTypeEnum**, um anzugeben, dass Sie einen dynamischen Cursor in ADO verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="62ec1-p103">The dynamic cursor is a good choice if your application must detect all concurrent updates made by other users. Use the **adOpenDynamic** **CursorTypeEnum** to indicate that you want to use a dynamic cursor in ADO.</span></span>

<span data-ttu-id="62ec1-112">[Vorwärtscursor](forward-only-cursors.md) | [Statische Cursor](static-cursors.md) | [Keysetcursor](keyset-cursors.md)</span><span class="sxs-lookup"><span data-stu-id="62ec1-112">[Forward-Only Cursors](forward-only-cursors.md) | [Static Cursors](static-cursors.md) | [Keyset Cursors](keyset-cursors.md)</span></span>

