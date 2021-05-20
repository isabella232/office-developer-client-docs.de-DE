---
title: PidTagResourcePath (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429859"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="7a693-103">PidTagResourcePath (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7a693-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="7a693-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a693-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a693-105">Enthält einen Pfad zum Server des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="7a693-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7a693-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7a693-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7a693-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="7a693-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="7a693-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7a693-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7a693-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="7a693-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="7a693-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7a693-110">Data type:</span></span>  <br/> |<span data-ttu-id="7a693-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7a693-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="7a693-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7a693-112">Area:</span></span>  <br/> |<span data-ttu-id="7a693-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="7a693-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a693-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7a693-114">Remarks</span></span>

<span data-ttu-id="7a693-115">Der in diesen Eigenschaften enthaltene Pfad stellt den vorgeschlagenen Pfad dar, in dem der Benutzer Ressourcen finden kann.</span><span class="sxs-lookup"><span data-stu-id="7a693-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="7a693-116">Die Definition dieser Eigenschaften ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="7a693-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="7a693-117">Beispielsweise verwendet eine Planungsanwendung diese Eigenschaften, um den vorgeschlagenen Speicherort für die Planungsanwendungsdateien anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7a693-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="7a693-118">Das Messagingbenutzerprofil bietet diese Eigenschaften als Komfort, sodass eine Clientanwendung den Messagingbenutzer nicht zur Eingabe eines Netzwerkpfads oder Eines Netzlaufwerkbuchstabens anfordern muss.</span><span class="sxs-lookup"><span data-stu-id="7a693-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="7a693-119">MAPI kann nur mit Dateinamen im Zeichensatz American National Standards Institute (ANSI) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a693-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="7a693-120">Anwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="7a693-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7a693-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a693-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="7a693-122">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7a693-122">Header files</span></span>

<span data-ttu-id="7a693-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7a693-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="7a693-124">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7a693-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="7a693-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7a693-125">Mapitags.h</span></span>
  
> <span data-ttu-id="7a693-126">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7a693-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7a693-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a693-127">See also</span></span>



[<span data-ttu-id="7a693-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7a693-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7a693-129">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7a693-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7a693-130">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7a693-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7a693-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7a693-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

