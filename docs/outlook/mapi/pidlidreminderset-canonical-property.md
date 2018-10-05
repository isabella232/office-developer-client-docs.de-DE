---
title: PidLidReminderSet (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 59379b0b1345684a491f2f7f896f2b8fc8fd54c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392389"
---
# <a name="pidlidreminderset-canonical-property"></a><span data-ttu-id="d4f89-103">PidLidReminderSet (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d4f89-103">PidLidReminderSet Canonical Property</span></span>

  
  
<span data-ttu-id="d4f89-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4f89-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d4f89-105">Gibt an, ob eine Erinnerung für das Objekt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d4f89-105">Specifies whether a reminder is set on the object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d4f89-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="d4f89-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d4f89-107">dispidReminderSet</span><span class="sxs-lookup"><span data-stu-id="d4f89-107">dispidReminderSet</span></span>  <br/> |
|<span data-ttu-id="d4f89-108">-Eigenschaft festgelegt:</span><span class="sxs-lookup"><span data-stu-id="d4f89-108">Property set:</span></span>  <br/> |<span data-ttu-id="d4f89-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="d4f89-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="d4f89-110">Long-ID (Abdeckung):</span><span class="sxs-lookup"><span data-stu-id="d4f89-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="d4f89-111">0x00008503</span><span class="sxs-lookup"><span data-stu-id="d4f89-111">0x00008503</span></span>  <br/> |
|<span data-ttu-id="d4f89-112">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="d4f89-112">Data type:</span></span>  <br/> |<span data-ttu-id="d4f89-113">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="d4f89-113">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="d4f89-114">Bereich:</span><span class="sxs-lookup"><span data-stu-id="d4f89-114">Area:</span></span>  <br/> |<span data-ttu-id="d4f89-115">Erinnerung</span><span class="sxs-lookup"><span data-stu-id="d4f89-115">Reminder</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d4f89-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d4f89-116">Remarks</span></span>

<span data-ttu-id="d4f89-117">Wenn ein wiederkehrendes Calendar-Objekt dieser Eigenschaft auf TRUE festgelegt ist, kann der Client diesen Wert für Ausnahmen außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="d4f89-117">If a recurring calendar object has this property set to TRUE, the client can override this value for exceptions.</span></span>
  
<span data-ttu-id="d4f89-118">Wenn diese Eigenschaft auf false festgelegt ist auf ein wiederkehrendes Calendar-Objekt Erinnerungen für die gesamte Datenreihe, einschließlich Ausnahmen deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d4f89-118">If this property is FALSE on a recurring calendar object, reminders are disabled for the entire series, including exceptions.</span></span> <span data-ttu-id="d4f89-119">Für wiederkehrende Task-Objekten kann diese Eigenschaft von Ausnahmen überschrieben werden (Einzelheiten finden Sie unter [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) und [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="d4f89-119">For recurring task objects, this property cannot be overridden by exceptions (see [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) and [[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx) for details).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d4f89-120">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d4f89-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d4f89-121">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="d4f89-121">Protocol specifications</span></span>

<span data-ttu-id="d4f89-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4f89-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4f89-123">Enthält Eigenschaftendefinitionen und Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="d4f89-123">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d4f89-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d4f89-124">[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d4f89-125">Gibt die Eigenschaften und das Interaktionsmodell für e-Mail und anderen Objekt Erinnerungen.</span><span class="sxs-lookup"><span data-stu-id="d4f89-125">Specifies the properties and the interaction model for email and other object reminders.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d4f89-126">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="d4f89-126">Header files</span></span>

<span data-ttu-id="d4f89-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d4f89-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="d4f89-128">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="d4f89-128">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d4f89-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4f89-129">See also</span></span>



[<span data-ttu-id="d4f89-130">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4f89-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d4f89-131">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d4f89-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d4f89-132">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="d4f89-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d4f89-133">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="d4f89-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

