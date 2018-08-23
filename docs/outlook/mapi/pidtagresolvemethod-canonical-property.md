---
title: PidTagResolveMethod (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e67cbb113899487f489ef7235d92d1adfcb76163
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563639"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="43fe8-103">PidTagResolveMethod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="43fe8-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="43fe8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43fe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43fe8-105">Enthält einen Ordner Konflikt Lösung Wert.</span><span class="sxs-lookup"><span data-stu-id="43fe8-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43fe8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="43fe8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="43fe8-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="43fe8-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="43fe8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="43fe8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="43fe8-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="43fe8-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="43fe8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="43fe8-110">Data type:</span></span>  <br/> |<span data-ttu-id="43fe8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="43fe8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="43fe8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="43fe8-112">Area:</span></span>  <br/> |<span data-ttu-id="43fe8-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="43fe8-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="43fe8-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="43fe8-114">Remarks</span></span>

<span data-ttu-id="43fe8-115">Diese Eigenschaft auf den Ordner mit den Konflikt Lösung Nachricht wird anzugeben, wie den Konflikt zu lösen.</span><span class="sxs-lookup"><span data-stu-id="43fe8-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="43fe8-116">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="43fe8-116">This property is not required.</span></span> <span data-ttu-id="43fe8-117">Jedoch ist festgelegt, müssen als den folgenden Kennzeichen nicht vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="43fe8-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43fe8-118">RESOLVE_METHOD_DEFAULT (0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="43fe8-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="43fe8-119">Konflikt zu lösen, dass die Nachricht generiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="43fe8-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="43fe8-120">RESOLVE_METHOD_LAST_WRITER_WINS (0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="43fe8-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="43fe8-121">Überschreiben Sie Zielnachricht mit aktuellen Änderungen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="43fe8-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="43fe8-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0 X 00000002)</span><span class="sxs-lookup"><span data-stu-id="43fe8-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="43fe8-123">Senden Sie Conflict-Benachrichtigung nicht beim Generieren von Konflikt beheben Nachricht im öffentlichen Ordner.</span><span class="sxs-lookup"><span data-stu-id="43fe8-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="43fe8-124">Ein Client oder Server muss eine Nachricht an Konflikt auflösen zugeordneten Nachrichten nicht generiert werden.</span><span class="sxs-lookup"><span data-stu-id="43fe8-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="43fe8-125">Diese Nachrichten müssen mit **RESOLVE_METHOD_LAST_WRITER_WINS** Semantik aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="43fe8-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="43fe8-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43fe8-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="43fe8-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="43fe8-127">Protocol specifications</span></span>

<span data-ttu-id="43fe8-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43fe8-128">[[MS-OXCSYNC]](http://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43fe8-129">Synchronisieren von messaging Objektdaten zwischen einem Server und einem Client behandelt.</span><span class="sxs-lookup"><span data-stu-id="43fe8-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="43fe8-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="43fe8-130">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="43fe8-131">Definiert die grundlegende Datenstrukturen, die verwendet werden remote-Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="43fe8-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="43fe8-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="43fe8-132">Header files</span></span>

<span data-ttu-id="43fe8-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="43fe8-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="43fe8-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="43fe8-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="43fe8-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="43fe8-135">Mapitags.h</span></span>
  
> <span data-ttu-id="43fe8-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="43fe8-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43fe8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43fe8-137">See also</span></span>



[<span data-ttu-id="43fe8-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43fe8-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="43fe8-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43fe8-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="43fe8-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="43fe8-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="43fe8-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="43fe8-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

