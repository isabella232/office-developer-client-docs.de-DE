---
title: PidTagDelegateFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392277"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="a7fa7-103">PidTagDelegateFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="a7fa7-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="a7fa7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7fa7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7fa7-105">Gibt an, ob eine Stellvertretung den Delegator privaten Message Objekte anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7fa7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="a7fa7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7fa7-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a7fa7-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="a7fa7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="a7fa7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7fa7-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="a7fa7-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="a7fa7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="a7fa7-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7fa7-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="a7fa7-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="a7fa7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="a7fa7-112">Area:</span></span>  <br/> |<span data-ttu-id="a7fa7-113">Nachricht-Klasse definiert Übertragungseinehit</span><span class="sxs-lookup"><span data-stu-id="a7fa7-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7fa7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a7fa7-114">Remarks</span></span>

<span data-ttu-id="a7fa7-115">Jeder Eintrag in dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="a7fa7-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a7fa7-116">**Flag**</span></span>|<span data-ttu-id="a7fa7-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a7fa7-117">**Value**</span></span>|<span data-ttu-id="a7fa7-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7fa7-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a7fa7-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="a7fa7-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="a7fa7-120">0</span><span class="sxs-lookup"><span data-stu-id="a7fa7-120">0</span></span>  <br/> |<span data-ttu-id="a7fa7-121">Die Stellvertretung sollte nicht möglich, zum Anzeigen von privaten Message-Objekten.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="a7fa7-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="a7fa7-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="a7fa7-123">1</span><span class="sxs-lookup"><span data-stu-id="a7fa7-123">1</span></span>  <br/> |<span data-ttu-id="a7fa7-124">Die Stellvertretung sollte zum Anzeigen von Objekten private Nachricht zugelassen werden.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="a7fa7-125">Diese Eigenschaft muss im Delegaten Informationen-Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="a7fa7-126">Der Wert der "ShowPrivate" gibt an, dass Stellvertreters private Nachrichtenobjekte sichtbar machen möchte.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="a7fa7-127">Diese Einstellung gilt für alle Ordner, für die die Stellvertretung die Rolle des Reviewer, Autor oder Editor verfügt.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7fa7-128">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a7fa7-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7fa7-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="a7fa7-129">Protocol specifications</span></span>

<span data-ttu-id="a7fa7-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7fa7-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7fa7-131">Gibt die Methoden zum Herstellen einer Verbindung mit und Konfiguration von Postfächer als Stellvertretungen und Interaktionen mit Nachricht und Kalender-Objekte, wenn sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7fa7-132">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="a7fa7-132">Header files</span></span>

<span data-ttu-id="a7fa7-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7fa7-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7fa7-134">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7fa7-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7fa7-135">Mapitags.h</span></span>
  
> <span data-ttu-id="a7fa7-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="a7fa7-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7fa7-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7fa7-137">See also</span></span>



[<span data-ttu-id="a7fa7-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7fa7-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7fa7-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a7fa7-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7fa7-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="a7fa7-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7fa7-141">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="a7fa7-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

