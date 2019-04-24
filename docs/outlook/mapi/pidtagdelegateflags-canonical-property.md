---
title: Kanonische Pidtagdelegateflags (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 20ffc6f7f4d21f980e5f0f387464430ba187192a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359899"
---
# <a name="pidtagdelegateflags-canonical-property"></a><span data-ttu-id="729b4-103">Kanonische Pidtagdelegateflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="729b4-103">PidTagDelegateFlags Canonical Property</span></span>

  
  
<span data-ttu-id="729b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="729b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="729b4-105">Gibt an, ob ein Delegat die privaten Nachrichtenobjekte des delegators anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="729b4-105">Specifies whether a delegate can view the delegator's private message objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="729b4-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="729b4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="729b4-107">PR_DELEGATE_FLAGS</span><span class="sxs-lookup"><span data-stu-id="729b4-107">PR_DELEGATE_FLAGS</span></span>  <br/> |
|<span data-ttu-id="729b4-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="729b4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="729b4-109">0x686B</span><span class="sxs-lookup"><span data-stu-id="729b4-109">0x686B</span></span>  <br/> |
|<span data-ttu-id="729b4-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="729b4-110">Data type:</span></span>  <br/> |<span data-ttu-id="729b4-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="729b4-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="729b4-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="729b4-112">Area:</span></span>  <br/> |<span data-ttu-id="729b4-113">Nachrichtenklassen definierte transmitable</span><span class="sxs-lookup"><span data-stu-id="729b4-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="729b4-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="729b4-114">Remarks</span></span>

<span data-ttu-id="729b4-115">Jeder Eintrag dieser Eigenschaft muss auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="729b4-115">Each entry of this property must be set to one of the following values.</span></span>
  
|<span data-ttu-id="729b4-116">**Wert**</span><span class="sxs-lookup"><span data-stu-id="729b4-116">**Flag**</span></span>|<span data-ttu-id="729b4-117">**Wert**</span><span class="sxs-lookup"><span data-stu-id="729b4-117">**Value**</span></span>|<span data-ttu-id="729b4-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="729b4-118">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="729b4-119">HidePrivate</span><span class="sxs-lookup"><span data-stu-id="729b4-119">HidePrivate</span></span>  <br/> |<span data-ttu-id="729b4-120">0</span><span class="sxs-lookup"><span data-stu-id="729b4-120">0</span></span>  <br/> |<span data-ttu-id="729b4-121">Der Delegat sollte keine privaten Nachrichtenobjekte anzeigen dürfen.</span><span class="sxs-lookup"><span data-stu-id="729b4-121">The delegate should not be allowed to view private message objects.</span></span>  <br/> |
|<span data-ttu-id="729b4-122">ShowPrivate</span><span class="sxs-lookup"><span data-stu-id="729b4-122">ShowPrivate</span></span>  <br/> |<span data-ttu-id="729b4-123">1</span><span class="sxs-lookup"><span data-stu-id="729b4-123">1</span></span>  <br/> |<span data-ttu-id="729b4-124">Der Stellvertreter sollte private Nachrichtenobjekte anzeigen dürfen.</span><span class="sxs-lookup"><span data-stu-id="729b4-124">The delegate should be allowed to view private message objects.</span></span>  <br/> |
   
<span data-ttu-id="729b4-125">Diese Eigenschaft muss im Delegate Information-Objekt festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="729b4-125">This property must be set in the delegate information object.</span></span> <span data-ttu-id="729b4-126">Der Wert "ShowPrivate" gibt an, dass der delegator private Nachrichtenobjekte sichtbar machen möchte.</span><span class="sxs-lookup"><span data-stu-id="729b4-126">The value of "ShowPrivate" indicates that the delegator wants to make private message objects visible.</span></span> <span data-ttu-id="729b4-127">Diese Einstellung gilt für alle Ordner, für die der Stellvertreter eine Rolle als Prüfer, Autor oder Editor aufweist.</span><span class="sxs-lookup"><span data-stu-id="729b4-127">This preference is applicable to all folders for which the delegate has a role of reviewer, author, or editor.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="729b4-128">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="729b4-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="729b4-129">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="729b4-129">Protocol specifications</span></span>

<span data-ttu-id="729b4-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="729b4-130">[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="729b4-131">Gibt Methoden zum Herstellen einer Verbindung mit und Konfigurieren von Postfächern als Stellvertreter sowie Interaktionen mit Nachrichten-und Kalenderobjekten an, wenn Sie im Auftrag eines anderen Benutzers agieren.</span><span class="sxs-lookup"><span data-stu-id="729b4-131">Specifies methods for connecting to and configuring mailboxes as delegates, and interactions with message and calendar objects when they act on behalf of another user.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="729b4-132">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="729b4-132">Header files</span></span>

<span data-ttu-id="729b4-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="729b4-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="729b4-134">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="729b4-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="729b4-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="729b4-135">Mapitags.h</span></span>
  
> <span data-ttu-id="729b4-136">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="729b4-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="729b4-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="729b4-137">See also</span></span>



[<span data-ttu-id="729b4-138">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="729b4-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="729b4-139">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="729b4-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="729b4-140">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="729b4-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="729b4-141">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="729b4-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

