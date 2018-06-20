---
title: IEnumFBBlock
manager: soliver
ms.date: 12/08/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fad9c0fd-b523-db98-ee0d-78aad5914ff2
ms.openlocfilehash: 536c19aa314db9fca39298536c12464e71a71407
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790970"
---
# <a name="ienumfbblock"></a><span data-ttu-id="68c65-102">IEnumFBBlock</span><span class="sxs-lookup"><span data-stu-id="68c65-102">IEnumFBBlock</span></span>

<span data-ttu-id="68c65-103">Unterstützt den Zugriff auf und das Aufzählen von Datenblöcke Frei/Gebucht-Informationen für einen Benutzer innerhalb eines Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="68c65-103">Supports accessing and enumerating free/busy blocks of data for a user within a time range.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="68c65-104">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="68c65-104">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68c65-105">Erbt:</span><span class="sxs-lookup"><span data-stu-id="68c65-105">Inherits from:</span></span>  <br/> |[<span data-ttu-id="68c65-106">IUnknown</span><span class="sxs-lookup"><span data-stu-id="68c65-106">IUnknown</span></span>](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="68c65-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="68c65-107">Provided by:</span></span>  <br/> |<span data-ttu-id="68c65-108">Frei/Gebucht-Anbieter</span><span class="sxs-lookup"><span data-stu-id="68c65-108">Free/busy provider</span></span>  <br/> |
|<span data-ttu-id="68c65-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="68c65-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="68c65-110">**IEnumFBBlock**</span><span class="sxs-lookup"><span data-stu-id="68c65-110">**IEnumFBBlock**</span></span> <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="68c65-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="68c65-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="68c65-112">Nächste</span><span class="sxs-lookup"><span data-stu-id="68c65-112">Next</span></span>](ienumfbblock-next.md) <br/> |<span data-ttu-id="68c65-113">Ruft die Anzahl der nächste angegebene Blöcke mit Frei/Gebucht-Daten in eine Enumeration.</span><span class="sxs-lookup"><span data-stu-id="68c65-113">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>  <br/> |
|[<span data-ttu-id="68c65-114">Überspringen</span><span class="sxs-lookup"><span data-stu-id="68c65-114">Skip</span></span>](ienumfbblock-skip.md) <br/> |<span data-ttu-id="68c65-115">Überspringt eine angegebene Anzahl von Blöcken des Frei/Gebucht-Daten.</span><span class="sxs-lookup"><span data-stu-id="68c65-115">Skips a specified number of blocks of free/busy data.</span></span>  <br/> |
|[<span data-ttu-id="68c65-116">Reset</span><span class="sxs-lookup"><span data-stu-id="68c65-116">Reset</span></span>](ienumfbblock-reset.md) <br/> |<span data-ttu-id="68c65-117">Setzt den Enumerator durch Festlegen des Cursors an den Anfang zurück.</span><span class="sxs-lookup"><span data-stu-id="68c65-117">Resets the enumerator by setting the cursor to the beginning.</span></span>  <br/> |
|[<span data-ttu-id="68c65-118">Clone</span><span class="sxs-lookup"><span data-stu-id="68c65-118">Clone</span></span>](ienumfbblock-clone.md) <br/> |<span data-ttu-id="68c65-119">Erstellt eine Kopie der Enumerator, verwenden die gleichen zeitliche Beschränkung jedoch festlegen des Cursors an den Anfang des den Enumerator.</span><span class="sxs-lookup"><span data-stu-id="68c65-119">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>  <br/> |
|[<span data-ttu-id="68c65-120">Einschränken</span><span class="sxs-lookup"><span data-stu-id="68c65-120">Restrict</span></span>](ienumfbblock-restrict.md) <br/> |<span data-ttu-id="68c65-121">Legt eine Beschränkung auf die Enumeration, die einen angegebenen Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="68c65-121">Restricts the enumeration to a specified time period.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68c65-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68c65-122">Remarks</span></span>

<span data-ttu-id="68c65-123">Eine Enumeration enthält Frei/Gebucht-Blöcke mit Daten, die nicht rechtzeitig überlappen.</span><span class="sxs-lookup"><span data-stu-id="68c65-123">An enumeration contains free/busy blocks of data that do not overlap in time.</span></span> <span data-ttu-id="68c65-124">Wenn sich überschneidenden Elemente in einem Kalender sind, verbindet Outlook diese Elemente um Frei/Gebucht-Blöcke übereinander in der angegebenen Reihenfolge der Priorität-Enumeration bilden: Abwesenheits, gebucht, mit Vorbehalt.</span><span class="sxs-lookup"><span data-stu-id="68c65-124">When there are overlapping items on a calendar, Outlook merges these items to form non-overlapping free/busy blocks in the enumeration based on this order of precedence: out-of-office, busy, tentative.</span></span>
  
<span data-ttu-id="68c65-125">Ein Anbieter Frei/Gebucht-Informationen ruft diese Schnittstelle und die für einen Zeitraum für einen Benutzer über [IFreeBusyData](ifreebusydata.md)-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="68c65-125">A free/busy provider obtains this interface and the enumeration for a time range for a user through [IFreeBusyData](ifreebusydata.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68c65-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68c65-126">See also</span></span>

- [<span data-ttu-id="68c65-127">Über die Frei/Gebucht-API</span><span class="sxs-lookup"><span data-stu-id="68c65-127">About the Free/Busy API</span></span>](about-the-free-busy-api.md)  
- [<span data-ttu-id="68c65-128">Konstanten (Frei/Gebucht-API)</span><span class="sxs-lookup"><span data-stu-id="68c65-128">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="68c65-129">IFreeBusyData</span><span class="sxs-lookup"><span data-stu-id="68c65-129">IFreeBusyData</span></span>](ifreebusydata.md)

