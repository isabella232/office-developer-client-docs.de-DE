---
title: Cursortypen (Access PC-Datenbank-Referenz)
TOCTitle: Types of Cursors
ms:assetid: 589f3755-3cf5-9470-bd66-8e8afa218fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249299(v=office.15)
ms:contentKeyID: 48544996
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6493d746f43ac8d923e5b1b9d6dcd3de44b411ec
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717573"
---
# <a name="types-of-cursors"></a><span data-ttu-id="ce0da-102">Cursortypen</span><span class="sxs-lookup"><span data-stu-id="ce0da-102">Types of cursors</span></span>


<span data-ttu-id="ce0da-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ce0da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ce0da-p101">Als Faustregel gilt, dass Ihre Anwendung den einfachsten Cursor verwenden sollte, der den erforderlichen Datenzugriff ermöglicht. Jedes zusätzliche Cursormerkmal (Vorwärtscursor, schreibgeschützter Cursor, statischer Cursor, Bildlaufcursor, ungepufferter Cursor) hat einen Preis - in Bezug auf Clientarbeitsspeicher, Netzwerklast oder Leistung. In vielen Fällen generieren die Standardcursoroptionen einen komplexeren Cursor, als tatsächlich von der Anwendung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="ce0da-p101">As a general rule, your application should use the simplest cursor that provides the required data access. Each additional cursor characteristic beyond the basics (forward-only, read-only, static, scrolling, unbuffered) has a price — in client memory, network load, or performance. In many cases, the default cursor options generate a more complex cursor than your application actually needs.</span></span>

<span data-ttu-id="ce0da-107">Die Auswahl des Cursortyps hängt davon ab, wie das Resultset von der Anwendung verwendet wird, sowie von mehreren Designaspekten wie z. B. der Größe des Resultsets, dem Prozentsatz der wahrscheinlich verwendeten Daten, der Empfindlichkeit gegenüber Datenänderungen sowie den Leistungsanforderungen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ce0da-107">Your choice of cursor type depends on how your application uses the result set and also on several design considerations, including the size of the result set, the percentage of the data likely to be used, sensitivity to data changes, and application performance requirements.</span></span>

<span data-ttu-id="ce0da-108">Im einfachsten Fall hängt die Cursorauswahl davon ab, ob Sie die Daten ändern oder einfach anzeigen müssen:</span><span class="sxs-lookup"><span data-stu-id="ce0da-108">At its most basic, your cursor choice depends on whether you need to change or simply view the data:</span></span>

  - <span data-ttu-id="ce0da-109">Wenn Sie keine Daten ändern, sondern lediglich einen Bildlauf in Resultsets ausführen müssen, verwenden Sie einen [Vorwärtscursor](forward-only-cursors.md) oder einen [statischen](static-cursors.md) Cursor.</span><span class="sxs-lookup"><span data-stu-id="ce0da-109">If you just need to scroll through a set of results, but not change data, use a [forward-only](forward-only-cursors.md) or [static](static-cursors.md) cursor.</span></span>

  - <span data-ttu-id="ce0da-110">Wenn ein umfangreiches Resultset vorliegt und nur ein paar Zeilen ausgewählt werden müssen, verwenden Sie einen [Keyset](keyset-cursors.md)cursor.</span><span class="sxs-lookup"><span data-stu-id="ce0da-110">If you have a large result set and need to select just a few rows, use a [keyset](keyset-cursors.md) cursor.</span></span>

  - <span data-ttu-id="ce0da-111">Wenn Sie für ein Resultset neueste Hinzufügungen, Änderungen und Löschvorgänge von allen gleichzeitigen Benutzern synchronisieren möchten, verwenden Sie einen [dynamischen](dynamic-cursors.md) Cursor.</span><span class="sxs-lookup"><span data-stu-id="ce0da-111">If you want to synchronize a result set with recent adds, changes, and deletes by all concurrent users, use a [dynamic](dynamic-cursors.md) cursor.</span></span>

<span data-ttu-id="ce0da-112">Alle Cursortypen unterscheiden sich zwar voneinander. Sie sollten jedoch beachten, dass diese Cursortypen weniger unterschiedliche Ausprägungen darstellen, als einfach das Ergebnis sich überschneidender Merkmale und Optionen sind.</span><span class="sxs-lookup"><span data-stu-id="ce0da-112">Although each cursor type seems to be distinct, keep in mind that these cursor types are not so much different varieties as simply the result of overlapping characteristics and options.</span></span>

