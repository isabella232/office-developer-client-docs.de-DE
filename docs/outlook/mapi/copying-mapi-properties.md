---
title: Kopieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415047"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="4a385-103">Kopieren von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4a385-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="4a385-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a385-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a385-105">Clients und Dienstanbieter können eine oder mehrere Eigenschaften eines Objekts mit den folgenden **IMAPIProp-Methoden** und -API-Funktionen kopieren:</span><span class="sxs-lookup"><span data-stu-id="4a385-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="4a385-106">Die [IMAPIProp::CopyTo-Methode](imapiprop-copyto.md) kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, optional ohne ausgewählte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4a385-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="4a385-107">**CopyTo wird** zum Kopieren oder Verschieben eines beliebigen Objekttyps verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a385-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="4a385-108">Die [IMAPIProp::CopyProps-Methode](imapiprop-copyprops.md) kopiert ausgewählte Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="4a385-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="4a385-109">**CopyProps wird** hauptsächlich für Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="4a385-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="4a385-110">Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder einer Antwort erstellt, übernimmt **CopyProps** das Kopieren der entsprechenden Eigenschaften aus der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="4a385-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="4a385-111">Die [PropCopyMore-Funktion](propcopymore.md) kopiert einen einzelnen Eigenschaftswert von einem Speicherort an einen anderen.</span><span class="sxs-lookup"><span data-stu-id="4a385-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="4a385-112">Verwenden **Sie PropCopyMore** mit Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="4a385-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="4a385-113">Beim Kopieren eines Werts nach dem anderen ist es möglich, viele kleine Speicherblöcke zuzuordnen und das Fragmentieren des Arbeitsspeichers zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="4a385-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="4a385-114">Die [ScCopyProps-Funktion](sccopyprops.md) kopiert Eigenschaftswerte in Massen.</span><span class="sxs-lookup"><span data-stu-id="4a385-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="4a385-115">**ScCopyProps kann** Eigenschaftswerte kopieren, die aus nicht zusammensistenten Speicherblöcken erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4a385-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="4a385-116">Es wird ein neues Eigenschaftenarray zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4a385-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="4a385-117">Wenn das von **ScCopyProps** zurückgegebene Eigenschaftenarray auf dem Datenträger gespeichert werden soll, passen Sie die Zeiger mit der [ScRelocProps-Funktion](screlocprops.md) an.</span><span class="sxs-lookup"><span data-stu-id="4a385-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="4a385-118">**ScRelocProps** sollte zweimal aufgerufen werden. einmal, um die Adressen anzupassen, bevor der Datenvorgang geschrieben wird, und dann erneut während des Lesevorgangs.</span><span class="sxs-lookup"><span data-stu-id="4a385-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="4a385-119">Die **ScRelocProps-Funktion** geht davon aus, dass das Eigenschaftswertarray ursprünglich in einer einzigen Zuordnung zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="4a385-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="4a385-120">Die in der vorherigen Liste beschriebenen API-Funktionen kopieren Eigenschaften im Arbeitsspeicher und nicht von einem Objekt in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a385-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="4a385-121">Diese Funktionen werden derzeit unterstützt, werden jedoch möglicherweise in einer zukünftigen Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4a385-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4a385-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a385-122">See also</span></span>



[<span data-ttu-id="4a385-123">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4a385-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

