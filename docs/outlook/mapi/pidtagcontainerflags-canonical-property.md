---
title: PidTagContainerFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357547"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="cdea5-103">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cdea5-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="cdea5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdea5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdea5-105">Enthält eine Bitmaske mit Flags, die funktionen eines Adressbuchcontainers beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cdea5-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cdea5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cdea5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cdea5-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="cdea5-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="cdea5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cdea5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cdea5-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="cdea5-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="cdea5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cdea5-110">Data type:</span></span>  <br/> |<span data-ttu-id="cdea5-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cdea5-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cdea5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cdea5-112">Area:</span></span>  <br/> |<span data-ttu-id="cdea5-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="cdea5-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cdea5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cdea5-114">Remarks</span></span>

<span data-ttu-id="cdea5-115">Mindestens eines der folgenden Flags kann für die Bitmaske festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="cdea5-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="cdea5-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="cdea5-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="cdea5-117">Zeigt ein Dialogfeld an, um eine Einschränkung an fordern, bevor Inhalte des Containers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cdea5-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="cdea5-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="cdea5-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="cdea5-119">Einträge können dem Container hinzugefügt und aus dem Container entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cdea5-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="cdea5-120">Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cdea5-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="cdea5-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="cdea5-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="cdea5-122">Der Container kann Empfänger enthalten.</span><span class="sxs-lookup"><span data-stu-id="cdea5-122">The container can hold recipients.</span></span> <span data-ttu-id="cdea5-123">Dieses Flag gibt nicht an, ob empfänger tatsächlich im Container vorhanden sind oder ob sie hinzugefügt oder entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="cdea5-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="cdea5-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="cdea5-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="cdea5-125">Der Container kann untergeordnete Container enthalten.</span><span class="sxs-lookup"><span data-stu-id="cdea5-125">The container can hold child containers.</span></span> <span data-ttu-id="cdea5-126">Dieses Flag gibt nicht an, ob subcontainer tatsächlich im Container vorhanden sind oder ob sie hinzugefügt oder entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="cdea5-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="cdea5-127">AB_SUBCONTAINERS muss festgelegt werden, damit der Container [IMAPIContainer::GetHierarchyTable unterstützt.](imapicontainer-gethierarchytable.md)</span><span class="sxs-lookup"><span data-stu-id="cdea5-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="cdea5-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="cdea5-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="cdea5-129">Einträge können nicht dem Container hinzugefügt oder aus dem Container entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="cdea5-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="cdea5-130">Dieses Flag gibt nicht an, ob Einträge im Container geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="cdea5-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="cdea5-131">Das AB_FIND_ON_OPEN wird dringend für Container empfohlen, die mit Onlinediensten oder mit langsamen Verbindungen zu Servern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdea5-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="cdea5-132">Wenn ein Container geöffnet wird, AB_FIND_ON_OPEN festgelegt  ist, wird dem Benutzer ein Dialogfeld Suchen angezeigt, um die angezeigten Messagingbenutzer einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="cdea5-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="cdea5-133">Selbst eine Teilspezifikation, die die Messagingbenutzer einschränkt, kann die Anzeige der Inhalte erheblich beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="cdea5-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="cdea5-134">Entweder das AB_MODIFIABLE oder AB_UNMODIFIABLE muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cdea5-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="cdea5-135">Beide Flags können so festgelegt werden, dass der Container nicht weiß, ob er geändert werden kann oder nicht, z. B. ob die Änderung von den Zugriffsrechten des Benutzers abhängt.</span><span class="sxs-lookup"><span data-stu-id="cdea5-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="cdea5-136">In diesem Fall muss eine Clientanwendung einen Aufruf versuchen und den Rückgabecode untersuchen, um die Funktionen des Containers zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cdea5-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="cdea5-137">Ein Client beginnt normalerweise mit der AB_MODIFIABLE.</span><span class="sxs-lookup"><span data-stu-id="cdea5-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="cdea5-138">Wenn sie festgelegt ist, wird vom Client ein Aufruf ausgeführt, der versucht, den Container zu ändern und den Rückgabewert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="cdea5-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="cdea5-139">Das AB_MODIFIABLE gibt nicht an, welche Arten von Einträgen dem Container hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="cdea5-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="cdea5-140">Um dies zu ermitteln, sollte der Client die entsprechende [OpenProperty-Methode](imapiprop-openproperty.md) verwenden, um die **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) -Eigenschaft des Containers zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cdea5-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="cdea5-141">Durch **PR_CREATE_TEMPLATES** wird die einmal erstellte Tabelle des Containers zurückgegeben, in der die Arten von Einträgen aufgeführt werden, die im Container erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="cdea5-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cdea5-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cdea5-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cdea5-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cdea5-143">Protocol specifications</span></span>

<span data-ttu-id="cdea5-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdea5-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdea5-145">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="cdea5-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cdea5-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdea5-146">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdea5-147">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="cdea5-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="cdea5-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cdea5-148">[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cdea5-149">Verarbeitet die Kommunikation eines Clients mit einem NSPI-Server (Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="cdea5-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cdea5-150">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="cdea5-150">Header files</span></span>

<span data-ttu-id="cdea5-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cdea5-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="cdea5-152">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cdea5-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="cdea5-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cdea5-153">Mapitags.h</span></span>
  
> <span data-ttu-id="cdea5-154">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cdea5-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cdea5-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdea5-155">See also</span></span>



[<span data-ttu-id="cdea5-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cdea5-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cdea5-157">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="cdea5-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cdea5-158">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cdea5-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cdea5-159">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cdea5-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

