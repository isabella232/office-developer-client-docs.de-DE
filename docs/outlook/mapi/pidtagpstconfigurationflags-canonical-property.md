---
title: PidTagPstConfigurationFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408943"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="c32e3-103">PidTagPstConfigurationFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c32e3-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="c32e3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c32e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c32e3-105">Gibt Konfigurationskennzeichen für eine persönliche Speichertabelle (PST-Datei) an.</span><span class="sxs-lookup"><span data-stu-id="c32e3-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c32e3-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="c32e3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c32e3-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="c32e3-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="c32e3-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="c32e3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c32e3-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="c32e3-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="c32e3-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="c32e3-110">Data type:</span></span>  <br/> |<span data-ttu-id="c32e3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c32e3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c32e3-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="c32e3-112">Area:</span></span>  <br/> |<span data-ttu-id="c32e3-113">Interne Persönliche Speichertabelle (PST)</span><span class="sxs-lookup"><span data-stu-id="c32e3-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c32e3-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c32e3-114">Remarks</span></span>

<span data-ttu-id="c32e3-115">Es folgen gültige Werte für diese Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="c32e3-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="c32e3-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c32e3-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="c32e3-117">Gibt eine Unicode-PST-Datei an.</span><span class="sxs-lookup"><span data-stu-id="c32e3-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="c32e3-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="c32e3-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="c32e3-119">Wenn sie von den Clientflags auf die [IMsgServiceAdmin::ConfigureMsgService-Methode](imsgserviceadmin-configuremsgservice.md) festgelegt ist, behandelt **ConfigureMsgService** wie ein [IMsgServiceAdmin::CreateMsgService-Aufruf](imsgserviceadmin-createmsgservice.md) und überspringt die Warnung "Dieser Informationsdienst wurde nicht konfiguriert".</span><span class="sxs-lookup"><span data-stu-id="c32e3-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="c32e3-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="c32e3-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="c32e3-121">Weist **ConfigureMsgService** an, den Wert der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft nicht zu ändern, obwohl sie bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c32e3-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="c32e3-122">In diesem Fall wurde sie nur für neue PST-Dateien bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c32e3-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="c32e3-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="c32e3-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="c32e3-124">Weist den Konfigurationscode an, zunächst ein Dialogfeld anzuzeigen, um zu bestätigen, ob eine Offlineordnerdatei (OST) gefunden wurde, und je nach Antwort des Benutzers entweder den gefundenen Offlineordner verwenden oder dem Benutzer das Durchsuchen eines anderen Offlineordners ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c32e3-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="c32e3-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="c32e3-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="c32e3-126">Kopiert die OST-Datei mit einem neuen eindeutigen Namen und verwirft den aktuellen Namen.</span><span class="sxs-lookup"><span data-stu-id="c32e3-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="c32e3-127">Die vorhandene OST-Datei verbleibt auf dem Computer, wird jedoch in diesem Profil nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="c32e3-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="c32e3-128">Dies tritt in der Regel auf, wenn Microsoft Outlook eine bestimmte OST-Datei nicht mehr zulässt und registrierungsrichtlinien es dem Benutzer nicht erlauben, die Datei umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="c32e3-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="c32e3-129">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c32e3-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c32e3-130">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="c32e3-130">Protocol specifications</span></span>

<span data-ttu-id="c32e3-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="c32e3-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="c32e3-132">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="c32e3-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c32e3-133">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="c32e3-133">Header files</span></span>

<span data-ttu-id="c32e3-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c32e3-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="c32e3-135">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="c32e3-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="c32e3-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c32e3-136">Mapitags.h</span></span>
  
> <span data-ttu-id="c32e3-137">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c32e3-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c32e3-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c32e3-138">See also</span></span>



[<span data-ttu-id="c32e3-139">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c32e3-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c32e3-140">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="c32e3-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c32e3-141">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="c32e3-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c32e3-142">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="c32e3-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

