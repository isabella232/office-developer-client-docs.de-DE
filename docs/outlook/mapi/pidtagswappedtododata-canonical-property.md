---
title: Kanonische Pidtagswappedtododata (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359136"
---
# <a name="pidtagswappedtododata-canonical-property"></a><span data-ttu-id="b2348-103">Kanonische Pidtagswappedtododata (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b2348-103">PidTagSwappedToDoData Canonical Property</span></span>

  
  
<span data-ttu-id="b2348-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2348-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2348-105">Verwaltet einen zweiten Satz von Eigenschaftswerten, die sich nicht auf den gekennzeichneten Status des Message-Objekts auswirken.</span><span class="sxs-lookup"><span data-stu-id="b2348-105">Maintains a second set of property values that do not affect the flagged state of the Message object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b2348-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b2348-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b2348-107">PR_SWAPPED_TODO_DATA</span><span class="sxs-lookup"><span data-stu-id="b2348-107">PR_SWAPPED_TODO_DATA</span></span>  <br/> |
|<span data-ttu-id="b2348-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b2348-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b2348-109">0x0E2D</span><span class="sxs-lookup"><span data-stu-id="b2348-109">0x0E2D</span></span>  <br/> |
|<span data-ttu-id="b2348-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b2348-110">Data type:</span></span>  <br/> |<span data-ttu-id="b2348-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="b2348-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="b2348-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b2348-112">Area:</span></span>  <br/> |<span data-ttu-id="b2348-113">Nicht transmitable MAPI</span><span class="sxs-lookup"><span data-stu-id="b2348-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2348-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b2348-114">Remarks</span></span>

<span data-ttu-id="b2348-115">Als sekundäres Flag-Speicherplatz fungieren wenn Absender Kennzeichen oder Absender Erinnerungen unterstützt werden, bietet diese Struktur einen Speicherort, an dem alle Eigenschaften im Zusammenhang mit dem Informations Protokoll, das in Absender-Flags unterstützt wird, gespeichert werden, und alle Eigenschaften im Zusammenhang mit dem Protokoll für Erinnerungseinstellungen, die in Absender Erinnerungen unterstützt werden, ohne die Absender Kennzeichnung oder Absender Erinnerungsinformationen an die Empfänger einer Nachricht zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="b2348-115">Acting as the secondary flag storage location if sender flags or sender reminders are supported, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in sender flags, and all properties relating to the Reminder Settings Protocol that are supported in sender reminders without exposing the sender flag or sender reminder information to the recipients of a message.</span></span>
  
<span data-ttu-id="b2348-116">Entsprechend bietet diese Struktur einen Speicherort für alle Eigenschaften im Zusammenhang mit dem Informations Protokoll, die in Empfänger Kennzeichen und Eigenschaften in Bezug auf das Protokoll für Erinnerungseinstellungen unterstützt werden, das im Empfänger unterstützt wird. Erinnerungen für eine zuvor gesendete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="b2348-116">Similarly, this structure provides a location in which to store all of the properties relating to the Informational Flagging Protocol that are supported in recipient flags and properties relating to the Reminder Settings Protocol that are supported in recipient reminders on a previously sent message.</span></span>
  
<span data-ttu-id="b2348-117">Weitere Informationen zu dieser Eigenschaft finden Sie unter [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b2348-117">For more information about this property, see [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b2348-118">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2348-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b2348-119">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b2348-119">Protocol specifications</span></span>

<span data-ttu-id="b2348-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2348-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2348-121">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b2348-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b2348-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2348-122">[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2348-123">Gibt die Eigenschaften und Vorgänge im Zusammenhang mit der Markierung an.</span><span class="sxs-lookup"><span data-stu-id="b2348-123">Specifies the properties and operations related to flagging.</span></span>
    
<span data-ttu-id="b2348-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b2348-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b2348-125">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="b2348-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b2348-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="b2348-126">Header files</span></span>

<span data-ttu-id="b2348-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b2348-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b2348-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="b2348-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b2348-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b2348-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b2348-130">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b2348-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b2348-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2348-131">See also</span></span>



[<span data-ttu-id="b2348-132">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2348-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b2348-133">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2348-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b2348-134">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b2348-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b2348-135">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b2348-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

