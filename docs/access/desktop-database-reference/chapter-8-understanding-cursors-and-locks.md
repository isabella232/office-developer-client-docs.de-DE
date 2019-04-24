---
title: 'Kapitel 8: Grundlegendes zu Cursorn und Sperren'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3075c0c9bd8267f6b30773a846523172eb2ef603
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296416"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="0abb9-102">Kapitel 8: Grundlegendes zu Cursorn und Sperren</span><span class="sxs-lookup"><span data-stu-id="0abb9-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="0abb9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0abb9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0abb9-p101">Sie sollten unbedingt die Funktionsweise von Cursorn kennen, damit Sie den optimalen und effizientesten Cursortyp für die Datenzugriffsanforderungen einer Anwendung auswählen können. Durch eine nicht optimale Cursorkonfiguration können Datenzugriffsvorgänge extrem langsam werden.</span><span class="sxs-lookup"><span data-stu-id="0abb9-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="0abb9-106">Viele Funktionen des **Recordset** -ADO-Objekts werden durch den Cursortyp und die Cursorplatzierung sowie durch den Sperrtyp bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0abb9-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="0abb9-107">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="0abb9-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="0abb9-108">Was ist ein Cursor?</span><span class="sxs-lookup"><span data-stu-id="0abb9-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="0abb9-109">Bedeutung der Cursorposition</span><span class="sxs-lookup"><span data-stu-id="0abb9-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="0abb9-110">Microsoft Cursor Service für OLE DB</span><span class="sxs-lookup"><span data-stu-id="0abb9-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="0abb9-111">Verwenden der CacheSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0abb9-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="0abb9-112">Cursor- und Sperrenmerkmale</span><span class="sxs-lookup"><span data-stu-id="0abb9-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="0abb9-113">Cursortypen (ADO)</span><span class="sxs-lookup"><span data-stu-id="0abb9-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="0abb9-114">Was ist eine Sperre? ADO</span><span class="sxs-lookup"><span data-stu-id="0abb9-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

