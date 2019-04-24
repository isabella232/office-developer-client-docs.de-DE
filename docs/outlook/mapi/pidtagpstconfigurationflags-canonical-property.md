---
title: Kanonische Pidtagpstconfigurationflags (-Eigenschaft
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
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286408"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="87028-103">Kanonische Pidtagpstconfigurationflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="87028-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="87028-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87028-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87028-105">Gibt an-Konfigurations Kennzeichen für eine persönliche Speichertabelle (PST-Datei).</span><span class="sxs-lookup"><span data-stu-id="87028-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="87028-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="87028-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="87028-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="87028-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="87028-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="87028-108">Identifier:</span></span>  <br/> |<span data-ttu-id="87028-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="87028-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="87028-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="87028-110">Data type:</span></span>  <br/> |<span data-ttu-id="87028-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="87028-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="87028-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="87028-112">Area:</span></span>  <br/> |<span data-ttu-id="87028-113">Persönliche Speichertabelle (PST) intern</span><span class="sxs-lookup"><span data-stu-id="87028-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87028-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87028-114">Remarks</span></span>

<span data-ttu-id="87028-115">Für diese Eigenschaft gelten die folgenden gültigen Werte:</span><span class="sxs-lookup"><span data-stu-id="87028-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="87028-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="87028-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="87028-117">Gibt eine Unicode-PST-Datei an.</span><span class="sxs-lookup"><span data-stu-id="87028-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="87028-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="87028-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="87028-119">Wenn Sie von den Client-Flags auf die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode festgelegt wird, behandelt **ConfigureMsgService** wie ein [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) -Aufruf und überspringt den "Dieser Informationsdienst wurde nicht konfiguriert" Warnung.</span><span class="sxs-lookup"><span data-stu-id="87028-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="87028-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="87028-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="87028-121">Weist **ConfigureMsgService** an, den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft nicht zu ändern, obwohl Sie bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="87028-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="87028-122">In diesem Fall wurde es nur für neue PST-Dateien bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="87028-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="87028-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="87028-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="87028-124">Weist den Konfigurationscode an, zunächst ein Dialogfeld anzuzeigen, um zu bestätigen, ob eine Offlineordnerdatei (Ost) gefunden wurde, und je nach Antwort des Benutzers entweder den gefundenen Offlineordner verwenden oder dem Benutzer ermöglichen, nach einem anderen Offlineordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="87028-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="87028-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="87028-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="87028-126">Kopiert die OST-Datei mit einem neuen eindeutigen Namen und verwirft den aktuellen Namen.</span><span class="sxs-lookup"><span data-stu-id="87028-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="87028-127">Die vorhandene OST-Datei verbleibt auf dem Computer, wird aber in diesem Profil nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="87028-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="87028-128">Dies ist in der Regel der Fall, wenn Microsoft Outlook eine bestimmte OST-Datei nicht mehr zulässt und Registrierungsrichtlinien dem Benutzer die Umbenennung der Datei nicht gestatten.</span><span class="sxs-lookup"><span data-stu-id="87028-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="87028-129">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="87028-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="87028-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="87028-130">Protocol specifications</span></span>

<span data-ttu-id="87028-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="87028-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="87028-132">Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="87028-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="87028-133">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="87028-133">Header files</span></span>

<span data-ttu-id="87028-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="87028-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="87028-135">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="87028-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="87028-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="87028-136">Mapitags.h</span></span>
  
> <span data-ttu-id="87028-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="87028-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="87028-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87028-138">See also</span></span>



[<span data-ttu-id="87028-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87028-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="87028-140">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="87028-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="87028-141">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="87028-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="87028-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="87028-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

