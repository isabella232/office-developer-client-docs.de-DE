---
title: PidTagSwappedToDoData (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8086bc3ea35fdbb4e0f7758b7931e305259a3a9e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578668"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="fafe4-103">PidTagSwappedToDoData (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="fafe4-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="fafe4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fafe4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fafe4-105">Verwaltet einen zweiten Satz von Eigenschaftswerten, die keine Auswirkung auf die gekennzeichneten Zustand des Message-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fafe4-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fafe4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="fafe4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fafe4-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="fafe4-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="fafe4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="fafe4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fafe4-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="fafe4-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="fafe4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="fafe4-110">Data type:</span></span>  <br/> |<span data-ttu-id="fafe4-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fafe4-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fafe4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="fafe4-112">Area:</span></span>  <br/> |<span data-ttu-id="fafe4-113">MAPI Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="fafe4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fafe4-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fafe4-114">Remarks</span></span>

<span data-ttu-id="fafe4-115">Als den Speicherort des sekundären Flag fungiert, wenn Flags Absender oder Absender Erinnerungen unterstützt werden, enthält diese Struktur einen Speicherort zum Speichern aller Eigenschaften sich auf das Informationszwecken kennzeichnen Protokoll beziehen, die in den Absender Flags unterstützt werden, und alle Eigenschaften für das Reminder-Einstellungen-Protokoll, die in Absender Erinnerungen unterstützt werden, ohne das Flag Absender oder Absender Erinnerungsinformationen an die Empfänger einer Nachricht verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="fafe4-116">In ähnlicher Weise stellt diese Struktur einen Speicherort zum Speichern aller die Eigenschaften für das Informationszwecken Protokoll kennzeichnen, die in den Empfänger Flags unterstützt werden und Eigenschaften für das Protokoll der Erinnerung Einstellungen, die im Empfänger unterstützt werden Erinnerungen für eine zuvor gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="fafe4-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="fafe4-117">Weitere Informationen zu dieser Eigenschaft finden Sie unter [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="fafe4-117">For more information about this property, see [[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fafe4-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fafe4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fafe4-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="fafe4-119">Protocol specifications</span></span>

<span data-ttu-id="fafe4-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fafe4-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fafe4-121">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fafe4-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fafe4-122">[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fafe4-123">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="fafe4-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fafe4-124">[[MS-OXORMDR]](http://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fafe4-125">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fafe4-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="fafe4-126">Header files</span></span>

<span data-ttu-id="fafe4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fafe4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="fafe4-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="fafe4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="fafe4-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fafe4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="fafe4-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="fafe4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fafe4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fafe4-131">See also</span></span>



[<span data-ttu-id="fafe4-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fafe4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fafe4-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fafe4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fafe4-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="fafe4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fafe4-135">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="fafe4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

