---
title: Kanonische Pidtagresourcepath (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 32d150e508f5c208e15d5ee5f0b8c800a1e597f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330170"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="0cef5-103">Kanonische Pidtagresourcepath (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0cef5-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="0cef5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0cef5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0cef5-105">Enthält einen Pfad zum Server des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="0cef5-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0cef5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0cef5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0cef5-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="0cef5-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="0cef5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0cef5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0cef5-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="0cef5-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="0cef5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0cef5-110">Data type:</span></span>  <br/> |<span data-ttu-id="0cef5-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0cef5-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0cef5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0cef5-112">Area:</span></span>  <br/> |<span data-ttu-id="0cef5-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="0cef5-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cef5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cef5-114">Remarks</span></span>

<span data-ttu-id="0cef5-115">Der in diesen Eigenschaften enthaltene Pfad stellt den vorgeschlagenen Pfad dar, in dem der Benutzer Ressourcen finden kann.</span><span class="sxs-lookup"><span data-stu-id="0cef5-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="0cef5-116">Die Definition dieser Eigenschaften ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0cef5-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="0cef5-117">Eine Planungsanwendung verwendet diese Eigenschaften zum Beispiel, um den vorgeschlagenen Speicherort für die Planungs Anwendungsdateien anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0cef5-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="0cef5-118">Das Messaging-Benutzerprofil stellt diese Eigenschaften als Bequemlichkeit bereit, sodass eine Clientanwendung den Messagingbenutzer nicht für einen Netzwerkpfad oder Netzlaufwerkbuchstaben auffordern muss.</span><span class="sxs-lookup"><span data-stu-id="0cef5-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="0cef5-119">MAPI funktioniert nur mit Dateinamen im ANSI-Zeichensatz (American National Standards Institute).</span><span class="sxs-lookup"><span data-stu-id="0cef5-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="0cef5-120">Anwendungen, die Dateinamen in einem OEM-Zeichensatz (Original Equipment Manufacturer) verwenden, müssen Sie vor dem Aufrufen von MAPI in ANSI konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0cef5-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0cef5-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0cef5-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0cef5-122">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="0cef5-122">Header files</span></span>

<span data-ttu-id="0cef5-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0cef5-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="0cef5-124">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="0cef5-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="0cef5-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0cef5-125">Mapitags.h</span></span>
  
> <span data-ttu-id="0cef5-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="0cef5-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0cef5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0cef5-127">See also</span></span>



[<span data-ttu-id="0cef5-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0cef5-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0cef5-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0cef5-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0cef5-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0cef5-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0cef5-131">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0cef5-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

