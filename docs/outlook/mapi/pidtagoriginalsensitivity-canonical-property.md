---
title: PidTagOriginalSensitivity (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSensitivity
api_type:
- COM
ms.assetid: 70a87cf8-2011-4669-90fd-2711c3352e30
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e712a4cc49541ee4330f479d7a03af323bdbc887
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390079"
---
# <a name="pidtagoriginalsensitivity-canonical-property"></a><span data-ttu-id="895fe-103">PidTagOriginalSensitivity (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="895fe-103">PidTagOriginalSensitivity Canonical Property</span></span>

  
  
<span data-ttu-id="895fe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="895fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="895fe-105">Enthält die vom Absender der ersten Version einer Nachricht zugewiesen Vertraulichkeitsstufe d. h., die Nachricht vor dem weitergeleitet oder darauf geantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="895fe-105">Contains the sensitivity value assigned by the sender of the first version of a message that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="895fe-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="895fe-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="895fe-107">PR_ORIGINAL_SENSITIVITY</span><span class="sxs-lookup"><span data-stu-id="895fe-107">PR_ORIGINAL_SENSITIVITY</span></span>  <br/> |
|<span data-ttu-id="895fe-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="895fe-108">Identifier:</span></span>  <br/> |<span data-ttu-id="895fe-109">0x002E</span><span class="sxs-lookup"><span data-stu-id="895fe-109">0x002E</span></span>  <br/> |
|<span data-ttu-id="895fe-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="895fe-110">Data type:</span></span>  <br/> |<span data-ttu-id="895fe-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="895fe-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="895fe-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="895fe-112">Area:</span></span>  <br/> |<span data-ttu-id="895fe-113">Allgemeine messaging</span><span class="sxs-lookup"><span data-stu-id="895fe-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="895fe-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="895fe-114">Remarks</span></span>

<span data-ttu-id="895fe-115">Eine Clientanwendung sollte diese Eigenschaft auf denselben Wert festgelegt wie die **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))-Eigenschaft, wenn die Nachricht wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="895fe-115">A client application should set this property to the same value as the **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) property when the message is first submitted.</span></span> <span data-ttu-id="895fe-116">Es sollte niemals später geändert werden.</span><span class="sxs-lookup"><span data-stu-id="895fe-116">It should never be changed subsequently.</span></span>
  
<span data-ttu-id="895fe-117">Diese Eigenschaft wird von der Adressbuchhierarchie verwendet, um die Vertraulichkeit auf kopierten Einträge zu schützen.</span><span class="sxs-lookup"><span data-stu-id="895fe-117">This property is used by the transport provider to protect the sensitivity on copied entries.</span></span> <span data-ttu-id="895fe-118">Sie können sie beispielsweise zum Blockieren der Änderung von der Text der ursprünglichen Nachricht in einer Weiterleitung des oder der Antwort auf eine Nachricht, die ursprünglich **SENSITIVITY_PRIVATE**gekennzeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="895fe-118">It enables it, for example, to block modification of the original message text in a forward of or reply to a message that was originally marked **SENSITIVITY_PRIVATE**.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="895fe-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="895fe-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="895fe-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="895fe-120">Protocol specifications</span></span>

<span data-ttu-id="895fe-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="895fe-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="895fe-122">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="895fe-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="895fe-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="895fe-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="895fe-124">Gibt die Eigenschaften und Operationen, die für Objekte, die e-Mail-Nachricht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="895fe-124">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="895fe-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="895fe-125">Header files</span></span>

<span data-ttu-id="895fe-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="895fe-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="895fe-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="895fe-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="895fe-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="895fe-128">Mapitags.h</span></span>
  
> <span data-ttu-id="895fe-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="895fe-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="895fe-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="895fe-130">See also</span></span>



[<span data-ttu-id="895fe-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="895fe-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="895fe-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="895fe-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="895fe-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="895fe-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="895fe-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="895fe-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

