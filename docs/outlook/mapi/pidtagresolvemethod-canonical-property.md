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
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331402"
---
# <a name="pidtagresolvemethod-canonical-property"></a><span data-ttu-id="5e5fa-103">PidTagResolveMethod (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="5e5fa-103">PidTagResolveMethod Canonical Property</span></span>

  
  
<span data-ttu-id="5e5fa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e5fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e5fa-105">Enthält den Konfliktauflösungswert eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-105">Contains a folder's conflict resolution value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e5fa-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5e5fa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e5fa-107">PR_RESOLVE_METHOD</span><span class="sxs-lookup"><span data-stu-id="5e5fa-107">PR_RESOLVE_METHOD</span></span>  <br/> |
|<span data-ttu-id="5e5fa-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5e5fa-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e5fa-109">0x3FE7</span><span class="sxs-lookup"><span data-stu-id="5e5fa-109">0x3FE7</span></span>  <br/> |
|<span data-ttu-id="5e5fa-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5e5fa-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e5fa-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5e5fa-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5e5fa-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5e5fa-112">Area:</span></span>  <br/> |<span data-ttu-id="5e5fa-113">MAPI-Status</span><span class="sxs-lookup"><span data-stu-id="5e5fa-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e5fa-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5e5fa-114">Remarks</span></span>

<span data-ttu-id="5e5fa-115">Diese Eigenschaft für den Ordner, der die Konfliktlösungsnachricht enthält, gibt an, wie der Konflikt gelöst werden soll.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-115">This property on the folder containing the conflict resolution message will indicate how to resolve the conflict.</span></span> <span data-ttu-id="5e5fa-116">Diese Eigenschaft ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-116">This property is not required.</span></span> <span data-ttu-id="5e5fa-117">Wenn sie jedoch festgelegt ist, dürfen keine anderen Kennzeichen als die folgenden vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="5e5fa-117">However, if it is set, flags other than the following must not be present:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e5fa-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="5e5fa-118">RESOLVE_METHOD_DEFAULT (0x00000000)</span></span>  <br/> |<span data-ttu-id="5e5fa-119">Nachricht zur Konfliktlösung sollte generiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-119">Conflict resolve message should be generated.</span></span>  <br/> |
|<span data-ttu-id="5e5fa-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="5e5fa-120">RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)</span></span>  <br/> |<span data-ttu-id="5e5fa-121">Überschreiben Sie die Zielnachricht, und aktuelle Änderungen werden angewendet.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-121">Overwrite target message with current changes being applied.</span></span>  <br/> |
|<span data-ttu-id="5e5fa-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="5e5fa-122">RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)</span></span>  <br/> |<span data-ttu-id="5e5fa-123">Senden Sie keine Konfliktbenachrichtigung, wenn Sie eine Konfliktlösungsnachricht im öffentlichen Ordner generieren.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-123">Do not send conflict notification message when generating conflict resolve message in public folder.</span></span>  <br/> |
   
<span data-ttu-id="5e5fa-124">Ein Client oder Server darf keine Konfliktlösungsnachricht für zugeordnete Nachrichten generieren.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-124">A client or server must not generate a conflict resolve message for associated messages.</span></span> <span data-ttu-id="5e5fa-125">Diese Nachrichten müssen mithilfe RESOLVE_METHOD_LAST_WRITER_WINS **aufgelöst** werden.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-125">These messages must be resolved by using **RESOLVE_METHOD_LAST_WRITER_WINS** semantics.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e5fa-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5e5fa-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e5fa-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5e5fa-127">Protocol specifications</span></span>

<span data-ttu-id="5e5fa-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e5fa-128">[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e5fa-129">Behandelt die Synchronisierung von Messagingobjektdaten zwischen einem Server und einem Client.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-129">Handles synchronizing messaging object data between a server and a client.</span></span>
    
<span data-ttu-id="5e5fa-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e5fa-130">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e5fa-131">Definiert die grundlegenden Datenstrukturen, die in Remotevorgängen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-131">Defines the basic data structures that are used in remote operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e5fa-132">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="5e5fa-132">Header files</span></span>

<span data-ttu-id="5e5fa-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5e5fa-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e5fa-134">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e5fa-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="5e5fa-135">Mapitags.h</span></span>
  
> <span data-ttu-id="5e5fa-136">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5e5fa-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e5fa-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e5fa-137">See also</span></span>



[<span data-ttu-id="5e5fa-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5e5fa-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e5fa-139">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="5e5fa-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e5fa-140">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5e5fa-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e5fa-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5e5fa-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

