---
title: 'Kapitel 8: Grundlegendes zu Cursorn und Sperren für Websitesammlungen'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3ca76b5635e057251aff845ecf45146e6e0d89a6
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936939"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="b88ae-102">Kapitel 8: Grundlegendes zu Cursorn und Sperren für Websitesammlungen</span><span class="sxs-lookup"><span data-stu-id="b88ae-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="b88ae-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b88ae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b88ae-p101">Sie sollten unbedingt die Funktionsweise von Cursorn kennen, damit Sie den optimalen und effizientesten Cursortyp für die Datenzugriffsanforderungen einer Anwendung auswählen können. Durch eine nicht optimale Cursorkonfiguration können Datenzugriffsvorgänge extrem langsam werden.</span><span class="sxs-lookup"><span data-stu-id="b88ae-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="b88ae-106">Viele Funktionen des **Recordset** -ADO-Objekts werden durch den Cursortyp und die Cursorplatzierung sowie durch den Sperrtyp bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b88ae-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="b88ae-107">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="b88ae-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="b88ae-108">Was ist ein Cursor?</span><span class="sxs-lookup"><span data-stu-id="b88ae-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="b88ae-109">Die Bedeutung der cursorplatzierung</span><span class="sxs-lookup"><span data-stu-id="b88ae-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="b88ae-110">Microsoft Cursor Service für OLE DB</span><span class="sxs-lookup"><span data-stu-id="b88ae-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="b88ae-111">Verwenden der CacheSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b88ae-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="b88ae-112">Merkmale von Cursorn und Sperren</span><span class="sxs-lookup"><span data-stu-id="b88ae-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="b88ae-113">Cursortypen (ADO)</span><span class="sxs-lookup"><span data-stu-id="b88ae-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="b88ae-114">Was ist eine Sperre? (ADO)</span><span class="sxs-lookup"><span data-stu-id="b88ae-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

