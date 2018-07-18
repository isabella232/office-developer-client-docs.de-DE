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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c13acd1c3b759602a5fbe07c21ca8b784e0fe4d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794215"
---
# <a name="pidtagcontainerflags-canonical-property"></a><span data-ttu-id="1e335-103">PidTagContainerFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1e335-103">PidTagContainerFlags Canonical Property</span></span>

  
  
<span data-ttu-id="1e335-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1e335-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1e335-105">Enthält eine Bitmaske der Flags, die ein Adressbuchcontainer Funktionen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1e335-105">Contains a bitmask of flags describing capabilities of an address book container.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e335-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1e335-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e335-107">PR_CONTAINER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1e335-107">PR_CONTAINER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1e335-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1e335-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e335-109">0x3600</span><span class="sxs-lookup"><span data-stu-id="1e335-109">0x3600</span></span>  <br/> |
|<span data-ttu-id="1e335-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1e335-110">Data type:</span></span>  <br/> |<span data-ttu-id="1e335-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e335-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e335-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1e335-112">Area:</span></span>  <br/> |<span data-ttu-id="1e335-113">Adressbuch</span><span class="sxs-lookup"><span data-stu-id="1e335-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e335-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1e335-114">Remarks</span></span>

<span data-ttu-id="1e335-115">Für die Bitmaske kann eine oder mehrere der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1e335-115">One or more of the following flags can be set for the bitmask:</span></span>
  
<span data-ttu-id="1e335-116">AB_FIND_ON_OPEN</span><span class="sxs-lookup"><span data-stu-id="1e335-116">AB_FIND_ON_OPEN</span></span> 
  
> <span data-ttu-id="1e335-117">Zeigt ein Dialogfeld zum Anfordern einer Einschränkung vor dem Anzeigen der Inhalt des Containers an.</span><span class="sxs-lookup"><span data-stu-id="1e335-117">Displays a dialog box to request a restriction before displaying any contents of the container.</span></span> 
    
<span data-ttu-id="1e335-118">AB_MODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="1e335-118">AB_MODIFIABLE</span></span> 
  
> <span data-ttu-id="1e335-119">Einträge können hinzugefügt und aus dem Container entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1e335-119">Entries can be added to and removed from the container.</span></span> <span data-ttu-id="1e335-120">Dieses Kennzeichen gibt nicht an, ob alle Einträge im Container geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1e335-120">This flag does not indicate whether any entries in the container can be modified.</span></span>
    
<span data-ttu-id="1e335-121">AB_RECIPIENTS</span><span class="sxs-lookup"><span data-stu-id="1e335-121">AB_RECIPIENTS</span></span> 
  
> <span data-ttu-id="1e335-122">Der Container kann Empfänger enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e335-122">The container can hold recipients.</span></span> <span data-ttu-id="1e335-123">Dieses Kennzeichen werden nicht angegeben, gibt an, ob alle Empfänger tatsächlich in den Container vorhanden sind, oder gibt an, ob sie hinzugefügt oder entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="1e335-123">This flag does not indicate whether any recipients are actually present in the container, or whether they can be added or removed.</span></span> 
    
<span data-ttu-id="1e335-124">AB_SUBCONTAINERS</span><span class="sxs-lookup"><span data-stu-id="1e335-124">AB_SUBCONTAINERS</span></span> 
  
> <span data-ttu-id="1e335-125">Der Container kann untergeordnete Container enthalten.</span><span class="sxs-lookup"><span data-stu-id="1e335-125">The container can hold child containers.</span></span> <span data-ttu-id="1e335-126">Dieses Kennzeichen nicht an, ob alle Untercontainer tatsächlich in den Container vorhanden sind, noch, ob sie hinzugefügt oder entfernt werden können.</span><span class="sxs-lookup"><span data-stu-id="1e335-126">This flag does not indicate whether any subcontainers are actually present in the container, nor whether they can be added or removed.</span></span> <span data-ttu-id="1e335-127">AB_SUBCONTAINERS muss für den Container zur Unterstützung von [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1e335-127">AB_SUBCONTAINERS must be set for the container to support [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md).</span></span> 
    
<span data-ttu-id="1e335-128">AB_UNMODIFIABLE</span><span class="sxs-lookup"><span data-stu-id="1e335-128">AB_UNMODIFIABLE</span></span> 
  
> <span data-ttu-id="1e335-129">Einträge können nicht hinzugefügt oder aus dem Container entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="1e335-129">Entries cannot be added to or removed from the container.</span></span> <span data-ttu-id="1e335-130">Dieses Kennzeichen gibt nicht an, ob alle Einträge im Container geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="1e335-130">This flag does not indicate whether any entries in the container can be modified.</span></span> 
    
<span data-ttu-id="1e335-131">Das Flag AB_FIND_ON_OPEN empfiehlt sich insbesondere für Container mit online-Dienste oder langsame Verbindung zum Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="1e335-131">The AB_FIND_ON_OPEN flag is highly recommended for containers used with online services or with slow connections to servers.</span></span> <span data-ttu-id="1e335-132">Wenn ein Container, die AB_FIND_ON_OPEN festgelegt wurde geöffnet wird, wird ein Dialogfeld **Suchen** für den Benutzer zum Einschränken der angezeigten messaging Benutzer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e335-132">When a container is opened that has AB_FIND_ON_OPEN set, a **Find** dialog box is presented to the user to restrict the displayed messaging users.</span></span> <span data-ttu-id="1e335-133">Sogar eine teilweise Spezifikation Einschränken der messaging-Benutzer kann eine Darstellung des Inhalts erheblich beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="1e335-133">Even a partial specification limiting the messaging users can dramatically speed up a display of the contents.</span></span> 
  
<span data-ttu-id="1e335-134">Die AB_MODIFIABLE oder AB_UNMODIFIABLE-Flag muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1e335-134">Either the AB_MODIFIABLE or AB_UNMODIFIABLE flag must be set.</span></span> <span data-ttu-id="1e335-135">Beide Flags können festgelegt werden, um anzugeben, dass es sich bei der Container nicht bekannt ist, ob sie oder nicht kann beispielsweise geändert werden, wenn der Benutzer Zugriffsrechte Änderung abhängt.</span><span class="sxs-lookup"><span data-stu-id="1e335-135">Both flags can be set to indicate that the container does not know whether it can be modified or not, for example if modification depends on the user's access rights.</span></span> <span data-ttu-id="1e335-136">In diesem Fall muss eine Clientanwendung versuchen, einen Anruf und untersuchen den Rückgabecode um das Container-Funktionen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="1e335-136">In this case, a client application must attempt a call and examine the return code to determine the container's capabilities.</span></span> <span data-ttu-id="1e335-137">Ein Client gestartet wird normalerweise durch AB_MODIFIABLE untersuchen.</span><span class="sxs-lookup"><span data-stu-id="1e335-137">A client typically starts by examining AB_MODIFIABLE.</span></span> <span data-ttu-id="1e335-138">Wenn sie festgelegt ist, wird der Client, die versucht, den Container geändert und überprüft den Rückgabewert aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e335-138">If it is set, the client makes a call that attempts to modify the container and checks the return value.</span></span> 
  
<span data-ttu-id="1e335-139">Die Kennzeichen AB_MODIFIABLE gibt die Einträge werden kann nicht zum Container hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="1e335-139">The AB_MODIFIABLE flag does not indicate what types of entries can be added to the container.</span></span> <span data-ttu-id="1e335-140">Um dies zu bestimmen, sollte der Client die entsprechende [OpenProperty](imapiprop-openproperty.md) -Methode zum Öffnen des Containers **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md))-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="1e335-140">To determine this, the client should use the appropriate [OpenProperty](imapiprop-openproperty.md) method to open the container's **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) property.</span></span> <span data-ttu-id="1e335-141">Öffnende **PR_CREATE_TEMPLATES** Ursachen des Containers einmaligen Tabelle zurückgegeben werden soll, Auflisten der Arten von Einträgen, die im Container erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="1e335-141">Opening **PR_CREATE_TEMPLATES** causes the container's one-off table to be returned, listing the kinds of entries that can be created in the container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e335-142">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1e335-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e335-143">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1e335-143">Protocol specifications</span></span>

<span data-ttu-id="1e335-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e335-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e335-145">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1e335-145">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1e335-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e335-146">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e335-147">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1e335-147">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
<span data-ttu-id="1e335-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e335-148">[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e335-149">Verarbeitet ein Client-Kommunikation mit einem Server (NSPI = Name Service Provider Interface).</span><span class="sxs-lookup"><span data-stu-id="1e335-149">Handles a client's communications with a Name Service Provider Interface (NSPI) server.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e335-150">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1e335-150">Header files</span></span>

<span data-ttu-id="1e335-151">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e335-151">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e335-152">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1e335-152">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e335-153">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e335-153">Mapitags.h</span></span>
  
> <span data-ttu-id="1e335-154">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1e335-154">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e335-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e335-155">See also</span></span>



[<span data-ttu-id="1e335-156">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e335-156">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e335-157">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e335-157">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e335-158">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1e335-158">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e335-159">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1e335-159">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

