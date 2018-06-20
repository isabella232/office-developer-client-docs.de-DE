---
title: Kanonische PidTagPstConfigurationFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b5a3978741f7ecb871e3c3de28e52dffdcf3a74f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794844"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="1a06b-103">Kanonische PidTagPstConfigurationFlags-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1a06b-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="1a06b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1a06b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1a06b-105">Gibt Konfiguration Flags für eine Tabelle persönlicher Speicher (PST-Datei).</span><span class="sxs-lookup"><span data-stu-id="1a06b-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1a06b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1a06b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1a06b-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="1a06b-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="1a06b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="1a06b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1a06b-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="1a06b-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="1a06b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1a06b-110">Data type:</span></span>  <br/> |<span data-ttu-id="1a06b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1a06b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1a06b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1a06b-112">Area:</span></span>  <br/> |<span data-ttu-id="1a06b-113">Persönlicher Speicher-Tabelle (. pst) interne</span><span class="sxs-lookup"><span data-stu-id="1a06b-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a06b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a06b-114">Remarks</span></span>

<span data-ttu-id="1a06b-115">Folgende sind gültige Werte für diese Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="1a06b-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="1a06b-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1a06b-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="1a06b-117">Gibt eine Unicode-PST-Datei an.</span><span class="sxs-lookup"><span data-stu-id="1a06b-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="1a06b-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="1a06b-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="1a06b-119">Wenn Satz aus der Client Kennzeichen an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode, wie Gespräch [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) **ConfigureMsgService** behandelt und überspringt die "dieser Informationsdienst wurde nicht konfiguriert" Warnung.</span><span class="sxs-lookup"><span data-stu-id="1a06b-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="1a06b-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="1a06b-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="1a06b-121">Teilt **ConfigureMsgService** nicht den Wert der Eigenschaft **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ändern, obwohl es bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a06b-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="1a06b-122">Es wurde in diesem Fall nur für neue PST-Dateien angegeben.</span><span class="sxs-lookup"><span data-stu-id="1a06b-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="1a06b-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="1a06b-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="1a06b-124">Erfahren Sie mehr Konfigurationscode für das erste anzuzeigende ein Dialogfeld zu bestätigen, dass eine Datei Offlineordnerdatei (OST) wurde gefunden und, je nach Antwort des Benutzers, verwenden Sie entweder den gefundenen Ordner Offline oder aktivieren den Benutzer Offline einen anderen Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1a06b-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="1a06b-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="1a06b-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="1a06b-126">Kopiert die OST-Datei mit einem neuen eindeutigen Namen und den aktuellen Namen verwirft.</span><span class="sxs-lookup"><span data-stu-id="1a06b-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="1a06b-127">Die vorhandenen OST-Datei auf dem Computer bleibt jedoch nicht mehr in diesem Profil verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a06b-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="1a06b-128">Dies tritt normalerweise auf, wenn Microsoft Outlook, eine bestimmte OST-Datei nicht länger ermöglicht und Registrierungsrichtlinien den Benutzer, benennen Sie die Datei nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="1a06b-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="1a06b-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1a06b-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1a06b-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1a06b-130">Protocol specifications</span></span>

<span data-ttu-id="1a06b-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="1a06b-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="1a06b-132">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="1a06b-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1a06b-133">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1a06b-133">Header files</span></span>

<span data-ttu-id="1a06b-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1a06b-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="1a06b-135">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1a06b-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="1a06b-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1a06b-136">Mapitags.h</span></span>
  
> <span data-ttu-id="1a06b-137">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1a06b-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1a06b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a06b-138">See also</span></span>



[<span data-ttu-id="1a06b-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a06b-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1a06b-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1a06b-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1a06b-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1a06b-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1a06b-142">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1a06b-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

