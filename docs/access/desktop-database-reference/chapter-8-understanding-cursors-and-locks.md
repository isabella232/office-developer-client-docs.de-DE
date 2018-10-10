---
title: 'Kapitel 8: Grundlegendes zu Cursorn und Sperren'
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99f363522874f01268f4c1a64515bf6f2cdd6336
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473608"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="b475f-102">Kapitel 8: Grundlegendes zu Cursorn und Sperren</span><span class="sxs-lookup"><span data-stu-id="b475f-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="b475f-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b475f-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b475f-p101">Sie sollten unbedingt die Funktionsweise von Cursorn kennen, damit Sie den optimalen und effizientesten Cursortyp für die Datenzugriffsanforderungen einer Anwendung auswählen können. Durch eine nicht optimale Cursorkonfiguration können Datenzugriffsvorgänge extrem langsam werden.</span><span class="sxs-lookup"><span data-stu-id="b475f-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="b475f-106">Viele Funktionen des **Recordset** -ADO-Objekts werden durch den Cursortyp und die Cursorplatzierung sowie durch den Sperrtyp bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b475f-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="b475f-107">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="b475f-107">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="b475f-108">Was ist ein Cursor?</span><span class="sxs-lookup"><span data-stu-id="b475f-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

  - [<span data-ttu-id="b475f-109">Cursortypen</span><span class="sxs-lookup"><span data-stu-id="b475f-109">Types of Cursors</span></span>](types-of-cursors.md)

  - [<span data-ttu-id="b475f-110">Bedeutung der Cursorplatzierung</span><span class="sxs-lookup"><span data-stu-id="b475f-110">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

  - [<span data-ttu-id="b475f-111">Microsoft Cursor Service für OLE DB</span><span class="sxs-lookup"><span data-stu-id="b475f-111">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

  - [<span data-ttu-id="b475f-112">Was ist eine Sperre?</span><span class="sxs-lookup"><span data-stu-id="b475f-112">What is a Lock?</span></span>](what-is-a-lock.md)

  - [<span data-ttu-id="b475f-113">Verwenden der CacheSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b475f-113">Using CacheSize</span></span>](using-cachesize.md)

  - [<span data-ttu-id="b475f-114">Merkmale von Cursorn und Sperren</span><span class="sxs-lookup"><span data-stu-id="b475f-114">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

