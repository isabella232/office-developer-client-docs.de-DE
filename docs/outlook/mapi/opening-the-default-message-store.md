---
title: Öffnen eines Standardnachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 670fb896-9aaf-4a96-83f7-76237409e956
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d8e620516e2b3e61cd07f3a08af989cc4ed5b61e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436027"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="767c6-103">Öffnen eines Standardnachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="767c6-103">Opening the default message store</span></span>

<span data-ttu-id="767c6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="767c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="767c6-105">In einer bestimmten Sitzung fungiert ein Nachrichtenspeicher als Standardnachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="767c6-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="767c6-106">Ein Standardnachrichtenspeicher hat die folgenden Merkmale:</span><span class="sxs-lookup"><span data-stu-id="767c6-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="767c6-107">Die **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) -Eigenschaft ist auf TRUE festgelegt.</span><span class="sxs-lookup"><span data-stu-id="767c6-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="767c6-108">Das STATUS_DEFAULT_STORE wird in der **eigenschaft PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="767c6-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="767c6-109">MAPI erstellt automatisch die IPM-Unterstruktur und die Stammordner für Suchergebnisse, allgemeine Ansichten und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="767c6-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="767c6-110">Weitere Informationen zu diesen Ordnern finden Sie unter [IPM Subtree](ipm-subtree.md) und [MAPI Special Folders](mapi-special-folders.md).</span><span class="sxs-lookup"><span data-stu-id="767c6-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="767c6-111">Zum Abrufen der Eintrags-ID für den Standardnachrichtenspeicher müssen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) aufrufen, um die Nachrichtenspeichertabelle zu öffnen und eine entsprechende Einschränkung in einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="767c6-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="767c6-112">**HrQueryAllRows** gibt einen Zeilensatz mit der zeile zurück, die den Standardnachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="767c6-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="767c6-113">Die Einschränkung, die Sie an **HrQueryAllRows übergeben,** kann in einem der folgenden Formen bestehen:</span><span class="sxs-lookup"><span data-stu-id="767c6-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="767c6-114">Eine **AND-Einschränkung,** die eine **SAndRestriction-Struktur** verwendet, um zu kombinieren:</span><span class="sxs-lookup"><span data-stu-id="767c6-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="767c6-115">Es gibt eine Einschränkung, die eine **SExistRestriction-Struktur** verwendet, um das Vorhandensein der PR_DEFAULT_STORE **zu** testen.</span><span class="sxs-lookup"><span data-stu-id="767c6-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="767c6-116">Eine Eigenschaftseinschränkung, die eine [SPropertyRestriction-Struktur](spropertyrestriction.md) verwendet, um den TRUE-Wert in der PR_DEFAULT_STORE **zu** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="767c6-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="767c6-117">Eine Bitmaskeneinschränkung, die eine [SBitMaskRestriction-Struktur](sbitmaskrestriction.md) zum Anwenden von STATUS_DEFAULT_STORE als Maske auf die PR_RESOURCE_FLAGS **verwendet.**</span><span class="sxs-lookup"><span data-stu-id="767c6-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="767c6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="767c6-118">See also</span></span>

- [<span data-ttu-id="767c6-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="767c6-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="767c6-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="767c6-120">SAndRestriction</span></span>](sandrestriction.md)

