---
title: Kanonische Pidlidreminderset (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidReminderSet
api_type:
- COM
ms.assetid: 06b7792c-1b43-4e20-9a3b-44f2664b2125
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335154"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="12732-103">Kanonische Pidlidreminderset (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="12732-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="12732-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12732-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12732-105">Gibt an, ob eine Erinnerung für das Objekt festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="12732-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="12732-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="12732-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="12732-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="12732-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="12732-108">Eigenschaftensatz:</span><span class="sxs-lookup"><span data-stu-id="12732-108">Property set:</span></span>  <br/> |<span data-ttu-id="12732-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="12732-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="12732-110">Long-ID (Deckel):</span><span class="sxs-lookup"><span data-stu-id="12732-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="12732-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="12732-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="12732-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="12732-112">Data type:</span></span>  <br/> |<span data-ttu-id="12732-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="12732-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="12732-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="12732-114">Area:</span></span>  <br/> |<span data-ttu-id="12732-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="12732-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12732-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12732-116">Remarks</span></span>

<span data-ttu-id="12732-117">Wenn für ein wiederkehrendes Calendar-Objekt diese Eigenschaft auf TRUE festgelegt ist, kann der Client diesen Wert für Ausnahmen außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="12732-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="12732-118">Wenn diese Eigenschaft für ein wiederkehrendes Kalenderobjekt auf FALSE festgelegt ist, werden Erinnerungen für die gesamte Datenreihe deaktiviert, einschließlich Ausnahmen.</span><span class="sxs-lookup"><span data-stu-id="12732-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="12732-119">Bei Objekten mit wiederkehrenden Aufgaben kann diese Eigenschaft nicht durch Ausnahmen außer Kraft gesetzt werden (Weitere Informationen finden Sie unter [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) und [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="12732-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="12732-120">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="12732-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="12732-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="12732-121">Protocol specifications</span></span>

<span data-ttu-id="12732-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12732-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12732-123">Stellt Eigenschaftensatz Definitionen und Verweise auf zugehörige Exchange Server-Protokollspezifikationen bereit.</span><span class="sxs-lookup"><span data-stu-id="12732-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="12732-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="12732-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="12732-125">Gibt die Eigenschaften und das Interaktionsmodell für e-Mails und andere Objekt Erinnerungen an.</span><span class="sxs-lookup"><span data-stu-id="12732-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="12732-126">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="12732-126">Header files</span></span>

<span data-ttu-id="12732-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="12732-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="12732-128">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="12732-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="12732-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12732-129">See also</span></span>



[<span data-ttu-id="12732-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12732-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="12732-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="12732-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="12732-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="12732-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="12732-133">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="12732-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

