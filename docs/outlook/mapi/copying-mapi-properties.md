---
title: Kopieren der MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 556ea9faedf0d9a02b0cff1bb2f1750289cc4d1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565081"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="9aebb-103">Kopieren der MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9aebb-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="9aebb-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9aebb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9aebb-105">Clients und -Dienstanbieter können eine oder mehrere der Eigenschaften eines Objekts mit dem folgenden **IMAPIProp** Methoden und API-Funktionen kopieren:</span><span class="sxs-lookup"><span data-stu-id="9aebb-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="9aebb-106">Die [IMAPIProp::CopyTo](imapiprop-copyto.md) -Methode kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, optional Ausschließen von ausgewählten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9aebb-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="9aebb-107">**CopyTo** dient zum Kopieren oder verschieben jeden Objekttyp.</span><span class="sxs-lookup"><span data-stu-id="9aebb-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="9aebb-108">Die [IMAPIProp::CopyProps](imapiprop-copyprops.md) -Methode kopiert die ausgewählte Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="9aebb-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="9aebb-109">**CopyProps** wird hauptsächlich mit Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="9aebb-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="9aebb-110">Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder eine Antwort, die **CopyProps** Handles kopieren die entsprechenden Eigenschaften aus der ursprünglichen Nachricht erstellt.</span><span class="sxs-lookup"><span data-stu-id="9aebb-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="9aebb-111">Die [PropCopyMore](propcopymore.md) -Funktion kopiert einen einzelnen Eigenschaftswert von einem Speicherort in einen anderen.</span><span class="sxs-lookup"><span data-stu-id="9aebb-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="9aebb-112">Verwenden Sie **PropCopyMore** mit Bedacht vor.</span><span class="sxs-lookup"><span data-stu-id="9aebb-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="9aebb-113">Es ist möglich – Wenn Sie einen Wert zu einem Zeitpunkt kopieren – reservieren viele kleine Blöcke mit Speicher und Arbeitsspeicher zum fragmentieren verursachen.</span><span class="sxs-lookup"><span data-stu-id="9aebb-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="9aebb-114">Die Funktion [ScCopyProps](sccopyprops.md) kopiert Eigenschaftswerte in einer Sammeloperation.</span><span class="sxs-lookup"><span data-stu-id="9aebb-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="9aebb-115">**ScCopyProps** können Eigenschaftswerte, die erstellt wurden aus getrennten Blöcke des Arbeitsspeichers kopieren.</span><span class="sxs-lookup"><span data-stu-id="9aebb-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="9aebb-116">Es gibt ein neue Eigenschaftenarray zurück.</span><span class="sxs-lookup"><span data-stu-id="9aebb-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="9aebb-117">Ist das Array-Eigenschaft zurückgegebene **ScCopyProps** , auf dem Datenträger gespeichert werden sollen, verwenden Sie die [ScRelocProps](screlocprops.md) -Funktion, um den Zeiger anzupassen.</span><span class="sxs-lookup"><span data-stu-id="9aebb-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="9aebb-118">**ScRelocProps** sollte zweimal aufgerufen werden. einmal, um die Adressen vor dem Schreiben des Datenvorgangs anpassen und dann erneut bei der Lesevorgang.</span><span class="sxs-lookup"><span data-stu-id="9aebb-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="9aebb-119">Die Funktion **ScRelocProps** wird vorausgesetzt, dass das Array-Eigenschaft Wert in einer einzelnen Verteilung ursprünglich belegt wurde.</span><span class="sxs-lookup"><span data-stu-id="9aebb-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="9aebb-120">Die API-Funktionen in der vorherigen Liste Kopie Eigenschaften im Arbeitsspeicher und nicht von einem Objekt in ein anderes Objekt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9aebb-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="9aebb-121">Diese Funktionen werden derzeit unterstützt, jedoch möglicherweise nicht in einer zukünftigen Version unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9aebb-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9aebb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9aebb-122">See also</span></span>



[<span data-ttu-id="9aebb-123">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9aebb-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

