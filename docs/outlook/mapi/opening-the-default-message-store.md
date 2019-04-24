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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348601"
---
# <a name="opening-the-default-message-store"></a><span data-ttu-id="bb732-103">Öffnen eines Standardnachrichtenspeichers</span><span class="sxs-lookup"><span data-stu-id="bb732-103">Opening the default message store</span></span>

<span data-ttu-id="bb732-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb732-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb732-105">In einer bestimmten Sitzung fungiert ein Nachrichtenspeicher als Standardnachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="bb732-105">In any particular session, one message store acts as the default message store.</span></span> <span data-ttu-id="bb732-106">Ein Standardnachrichtenspeicher weist die folgenden Merkmale auf:</span><span class="sxs-lookup"><span data-stu-id="bb732-106">A default message store has the following characteristics:</span></span>
  
- <span data-ttu-id="bb732-107">Die **PR_DEFAULT_STORE** ([pidtagdefaultstore (](pidtagdefaultstore-canonical-property.md))-Eigenschaft ist auf true festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bb732-107">The **PR_DEFAULT_STORE** ([PidTagDefaultStore](pidtagdefaultstore-canonical-property.md)) property is set to TRUE.</span></span>
    
- <span data-ttu-id="bb732-108">Das STATUS_DEFAULT_STORE-Flag wird in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bb732-108">The STATUS_DEFAULT_STORE flag is set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="bb732-109">MAPI erstellt automatisch die IPM-Unterstruktur und die Stammordner für Suchergebnisse, allgemeine Ansichten und persönliche Ansichten, wenn der Nachrichtenspeicher geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bb732-109">MAPI automatically creates the IPM subtree and the root folders for search-results, common views and personal views when the message store is opened.</span></span> <span data-ttu-id="bb732-110">Weitere Informationen zu diesen Ordnern finden Sie unter " [IPM subtree](ipm-subtree.md) " und " [MAPI Special Folders](mapi-special-folders.md)".</span><span class="sxs-lookup"><span data-stu-id="bb732-110">For more information about these folders, see [IPM Subtree](ipm-subtree.md) and [MAPI Special Folders](mapi-special-folders.md).</span></span> 
    
<span data-ttu-id="bb732-111">Zum Abrufen der Eintrags-ID für den standardmäßigen Nachrichtenspeicher müssen Sie [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) aufrufen, um die Nachrichtenspeichertabelle zu öffnen und bei einem Aufruf von [HrQueryAllRows](hrqueryallrows.md)eine entsprechende Einschränkung anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="bb732-111">To retrieve the entry identifier for the default message store, you must call [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) to open the message store table and apply an appropriate restriction in a call to [HrQueryAllRows](hrqueryallrows.md).</span></span> <span data-ttu-id="bb732-112">**HrQueryAllRows** gibt einen Zeilensatz mit der eine Zeile zurück, die den Standardnachrichtenspeicher darstellt.</span><span class="sxs-lookup"><span data-stu-id="bb732-112">**HrQueryAllRows** will return a row set with the one row that represents the default message store.</span></span> <span data-ttu-id="bb732-113">Die an **HrQueryAllRows** übergebene Einschränkung kann eines der folgenden Formen annehmen:</span><span class="sxs-lookup"><span data-stu-id="bb732-113">The restriction that you pass to **HrQueryAllRows** can take on one of the following forms:</span></span> 
  
1. <span data-ttu-id="bb732-114">Eine **und-** Einschränkung, die eine **SAndRestriction** -Struktur kombiniert:</span><span class="sxs-lookup"><span data-stu-id="bb732-114">An **AND** restriction that uses an **SAndRestriction** structure to combine:</span></span> 
    
   - <span data-ttu-id="bb732-115">Eine EXISTS-Einschränkung, die eine **SExistRestriction** -Struktur verwendet, um das vorhanden sein der **PR_DEFAULT_STORE** -Eigenschaft zu testen.</span><span class="sxs-lookup"><span data-stu-id="bb732-115">An exists restriction that uses an **SExistRestriction** structure to test for the existence of the **PR_DEFAULT_STORE** property.</span></span> 
    
   - <span data-ttu-id="bb732-116">Eine Eigenschaftseinschränkung, die eine [SPropertyRestriction](spropertyrestriction.md) -Struktur verwendet, um den true-Wert in der **PR_DEFAULT_STORE** -Eigenschaft zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="bb732-116">A property restriction that uses an [SPropertyRestriction](spropertyrestriction.md) structure to check for the TRUE value in the **PR_DEFAULT_STORE** property.</span></span> 
    
2. <span data-ttu-id="bb732-117">Eine Bitmasken Einschränkung, die eine [SBitMaskRestriction](sbitmaskrestriction.md) -Struktur zum Anwenden von STATUS_DEFAULT_STORE als Maske für die **PR_RESOURCE_FLAGS** -Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="bb732-117">A bitmask restriction that uses an [SBitMaskRestriction](sbitmaskrestriction.md) structure for applying STATUS_DEFAULT_STORE as a mask against the **PR_RESOURCE_FLAGS** property.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="bb732-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb732-118">See also</span></span>

- [<span data-ttu-id="bb732-119">SExistRestriction</span><span class="sxs-lookup"><span data-stu-id="bb732-119">SExistRestriction</span></span>](sexistrestriction.md)
- [<span data-ttu-id="bb732-120">SAndRestriction</span><span class="sxs-lookup"><span data-stu-id="bb732-120">SAndRestriction</span></span>](sandrestriction.md)

