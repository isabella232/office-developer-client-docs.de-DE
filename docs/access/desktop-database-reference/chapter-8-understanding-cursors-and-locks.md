---
title: 'Kapitel 8: Grundlegendes zu Cursorn und Sperren'
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4b98952e64eac3c35ed67f50e50776c08e594474
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869085"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="b4ede-102">Kapitel 8: Grundlegendes zu Cursorn und Sperren</span><span class="sxs-lookup"><span data-stu-id="b4ede-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="b4ede-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4ede-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4ede-p101">Sie sollten unbedingt die Funktionsweise von Cursorn kennen, damit Sie den optimalen und effizientesten Cursortyp für die Datenzugriffsanforderungen einer Anwendung auswählen können. Durch eine nicht optimale Cursorkonfiguration können Datenzugriffsvorgänge extrem langsam werden.</span><span class="sxs-lookup"><span data-stu-id="b4ede-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="b4ede-106">Viele Funktionen des **Recordset** -ADO-Objekts werden durch den Cursortyp und die Cursorplatzierung sowie durch den Sperrtyp bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b4ede-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="b4ede-107">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="b4ede-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="b4ede-108">Was ist ein Cursor?</span><span class="sxs-lookup"><span data-stu-id="b4ede-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

- [<span data-ttu-id="b4ede-109">Bedeutung der Cursorplatzierung</span><span class="sxs-lookup"><span data-stu-id="b4ede-109">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

- [<span data-ttu-id="b4ede-110">Microsoft Cursor Service für OLE DB</span><span class="sxs-lookup"><span data-stu-id="b4ede-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

- [<span data-ttu-id="b4ede-111">Verwenden der CacheSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b4ede-111">Using CacheSize</span></span>](using-cachesize.md)

- [<span data-ttu-id="b4ede-112">Merkmale von Cursorn und Sperren</span><span class="sxs-lookup"><span data-stu-id="b4ede-112">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

- [<span data-ttu-id="b4ede-113">Types of Cursors (ADO)</span><span class="sxs-lookup"><span data-stu-id="b4ede-113">Types of Cursors (ADO)</span></span>](types-of-cursors.md)

- [<span data-ttu-id="b4ede-114">What is a Lock? (ADO)</span><span class="sxs-lookup"><span data-stu-id="b4ede-114">What is a Lock? (ADO)</span></span>](what-is-a-lock.md)

