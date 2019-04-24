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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333075"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="2a15a-103">Kopieren von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2a15a-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="2a15a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a15a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a15a-105">Clients und Dienstanbieter können eine oder mehrere Eigenschaften eines Objekts mit den folgenden **IMAPIProp** -Methoden und API-Funktionen kopieren:</span><span class="sxs-lookup"><span data-stu-id="2a15a-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="2a15a-106">Die [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Methode kopiert alle Eigenschaften eines Objekts in ein anderes Objekt, wobei optional ausgewählte Eigenschaften ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2a15a-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="2a15a-107">**CopyTo** wird zum Kopieren oder bewegen eines beliebigen Objekttyps verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a15a-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="2a15a-108">Die [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Methode kopiert die ausgewählten Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="2a15a-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="2a15a-109">**CopyProps** wird hauptsächlich mit Nachrichten verwendet.</span><span class="sxs-lookup"><span data-stu-id="2a15a-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="2a15a-110">Wenn ein Client eine weitergeleitete Kopie einer Nachricht oder einer Antwort erstellt, verarbeitet **CopyProps** das Kopieren der entsprechenden Eigenschaften aus der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2a15a-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="2a15a-111">Die [PropCopyMore](propcopymore.md) -Funktion kopiert einen einzelnen Eigenschaftswert von einem Speicherort an einen anderen.</span><span class="sxs-lookup"><span data-stu-id="2a15a-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="2a15a-112">Verwenden Sie **PropCopyMore** mit Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="2a15a-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="2a15a-113">Es ist möglich, wenn Sie einen Wert gleichzeitig kopieren, um viele kleine Speicherblöcke zuzuweisen und Speicher Fragmente zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="2a15a-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="2a15a-114">Die [ScCopyProps](sccopyprops.md) -Funktion kopiert Eigenschaftswerte in Massen.</span><span class="sxs-lookup"><span data-stu-id="2a15a-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="2a15a-115">**ScCopyProps** können Eigenschaftswerte kopieren, die aus unzusammenhängenden Speicherblöcken erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2a15a-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="2a15a-116">Es wird ein neues Eigenschaftenarray zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2a15a-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="2a15a-117">Wenn das von **ScCopyProps** zurückgegebene Eigenschaftenarray auf dem Datenträger gespeichert werden soll, verwenden Sie die [ScRelocProps](screlocprops.md) -Funktion, um die Zeiger anzupassen.</span><span class="sxs-lookup"><span data-stu-id="2a15a-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="2a15a-118">**ScRelocProps** sollte zweimal aufgerufen werden; einmal, um die Adressen vor dem Schreiben des Datenvorgangs und dann erneut während des Lesevorgangs anzupassen.</span><span class="sxs-lookup"><span data-stu-id="2a15a-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="2a15a-119">Die **ScRelocProps** -Funktion geht davon aus, dass das Eigenschafts Wertarray ursprünglich in einer einzelnen Zuordnung zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="2a15a-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="2a15a-120">Die in der obigen Liste beschriebenen API-Funktionen kopieren die Eigenschaften im Arbeitsspeicher und nicht von einem Objekt zu einem anderen Objekt.</span><span class="sxs-lookup"><span data-stu-id="2a15a-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="2a15a-121">Diese Funktionen werden derzeit unterstützt, werden jedoch in zukünftigen Versionen möglicherweise nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2a15a-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a15a-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a15a-122">See also</span></span>



[<span data-ttu-id="2a15a-123">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2a15a-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

