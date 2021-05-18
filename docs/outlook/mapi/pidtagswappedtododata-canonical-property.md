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
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359136"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="641e5-103">PidTagSwappedToDoData (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="641e5-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="641e5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="641e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="641e5-105">Verwaltet einen zweiten Satz von Eigenschaftswerten, die sich nicht auf den gekennzeichneten Status des Message-Objekts auswirken.</span><span class="sxs-lookup"><span data-stu-id="641e5-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="641e5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="641e5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="641e5-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="641e5-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="641e5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="641e5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="641e5-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="641e5-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="641e5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="641e5-110">Data type:</span></span>  <br/> |<span data-ttu-id="641e5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="641e5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="641e5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="641e5-112">Area:</span></span>  <br/> |<span data-ttu-id="641e5-113">MAPI nicht durchlässig</span><span class="sxs-lookup"><span data-stu-id="641e5-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="641e5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="641e5-114">Remarks</span></span>

<span data-ttu-id="641e5-115">Als sekundärer Flagspeicherort, wenn Absenderflags oder Absendererinnerungen unterstützt werden, bietet diese Struktur einen Speicherort, an dem alle Eigenschaften im Zusammenhang mit dem Informational Flagging Protocol gespeichert werden, die in Absenderflags unterstützt werden, sowie alle Eigenschaften im Zusammenhang mit dem Reminder Einstellungen Protocol, die in Absendererinnerungen unterstützt werden, ohne das Absenderkennzeichen oder die Absendererinnerungsinformationen den Empfängern einer Nachricht verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="641e5-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="641e5-116">Auf ähnliche Weise bietet diese Struktur einen Speicherort zum Speichern aller Eigenschaften im Zusammenhang mit dem Informational Flagging Protocol, die in Empfängerflags und Eigenschaften im Zusammenhang mit dem Reminder Einstellungen Protocol unterstützt werden, die in Empfängererinnerungen für eine zuvor gesendete Nachricht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="641e5-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="641e5-117">Weitere Informationen zu dieser Eigenschaft finden Sie [unter [MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="641e5-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="641e5-118">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="641e5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="641e5-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="641e5-119">Protocol specifications</span></span>

<span data-ttu-id="641e5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="641e5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="641e5-121">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="641e5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="641e5-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="641e5-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="641e5-123">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Kennzeichnung an.</span><span class="sxs-lookup"><span data-stu-id="641e5-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="641e5-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="641e5-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="641e5-125">Gibt die Eigenschaften und das Interaktionsmodell für E-Mail- und andere Objekterinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="641e5-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="641e5-126">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="641e5-126">Header files</span></span>

<span data-ttu-id="641e5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="641e5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="641e5-128">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="641e5-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="641e5-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="641e5-129">Mapitags.h</span></span>
  
> <span data-ttu-id="641e5-130">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="641e5-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="641e5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="641e5-131">See also</span></span>



[<span data-ttu-id="641e5-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="641e5-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="641e5-133">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="641e5-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="641e5-134">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="641e5-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="641e5-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="641e5-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

