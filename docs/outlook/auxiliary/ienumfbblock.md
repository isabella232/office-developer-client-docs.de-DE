---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 2b37aa2000218acc0663ee8e2db12f01b93c0663
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317626"
---
# <a name="ienumfbblock"></a><span data-ttu-id="f5908-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="f5908-102">IEnumFBBlock</span></span>

<span data-ttu-id="f5908-103">Unterstützt den Zugriff auf und das Aufzählen von Frei/Gebucht-Datenblöcken für einen Benutzer innerhalb eines Zeitbereichs.</span><span class="sxs-lookup"><span data-stu-id="f5908-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f5908-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f5908-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f5908-105">Erbt von:</span><span class="sxs-lookup"><span data-stu-id="f5908-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="f5908-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5908-106">IUnknown</span></span>](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="f5908-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="f5908-107">Provided by:</span></span>  <br/> |<span data-ttu-id="f5908-108">Frei/Gebucht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="f5908-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="f5908-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="f5908-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f5908-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="f5908-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f5908-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="f5908-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f5908-112">Next</span><span class="sxs-lookup"><span data-stu-id="f5908-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="f5908-113">Ruft die nächste angegebene Anzahl von Blöcken von Frei/Gebucht-Daten in einer Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="f5908-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="f5908-114">Skip</span><span class="sxs-lookup"><span data-stu-id="f5908-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="f5908-115">Überspringt eine angegebene Anzahl von Blöcken von Frei/Gebucht-Daten.</span><span class="sxs-lookup"><span data-stu-id="f5908-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="f5908-116">Reset</span><span class="sxs-lookup"><span data-stu-id="f5908-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="f5908-117">Setzt den Enumerationszähler zurück, indem der Cursor auf den Anfang gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f5908-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="f5908-118">Clone</span><span class="sxs-lookup"><span data-stu-id="f5908-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="f5908-119">Erstellt eine Kopie des Enumerators mit der gleichen Zeiteinschränkung, legt den Cursor jedoch auf den Anfang des Enumerationsgeräts.</span><span class="sxs-lookup"><span data-stu-id="f5908-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="f5908-120">Restrict</span><span class="sxs-lookup"><span data-stu-id="f5908-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="f5908-121">Schränkt die Enumeration auf einen angegebenen Zeitraum ein.</span><span class="sxs-lookup"><span data-stu-id="f5908-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5908-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f5908-122">Remarks</span></span>

<span data-ttu-id="f5908-123">Eine Enumeration enthält Frei/Gebucht-Blöcke von Daten, die nicht zeitlich überlappen.</span><span class="sxs-lookup"><span data-stu-id="f5908-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="f5908-124">Wenn in einem Kalender überlappende Elemente enthalten sind, führt Outlook diese Elemente zu nicht überlappenden Frei/Gebucht-Blöcken in der Enumeration basierend auf dieser Rangfolge zusammen: out-of-office, busy, tentative.</span><span class="sxs-lookup"><span data-stu-id="f5908-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="f5908-125">Ein Frei/Gebucht-Anbieter ruft diese Schnittstelle und die Enumeration für einen Zeitraum für einen Benutzer über [IFreeBusyData ab.](ifreebusydata.md)</span><span class="sxs-lookup"><span data-stu-id="f5908-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f5908-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5908-126">See also</span></span>

- [<span data-ttu-id="f5908-127">Informationen zur Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="f5908-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="f5908-128">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="f5908-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="f5908-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="f5908-129">IFreeBusyData</span></span>](ifreebusydata.md)

