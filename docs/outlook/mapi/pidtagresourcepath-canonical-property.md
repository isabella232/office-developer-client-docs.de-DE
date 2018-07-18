---
title: PidTagResourcePath (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourcePath
api_type:
- COM
ms.assetid: ac49538e-6ee8-4ab4-9d79-88a83c7d0149
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d7385ea403e7ea45c97f6fd98e422ad7eb762c4c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794981"
---
# <a name="pidtagresourcepath-canonical-property"></a><span data-ttu-id="f1852-103">PidTagResourcePath (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f1852-103">PidTagResourcePath Canonical Property</span></span>

  
  
<span data-ttu-id="f1852-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1852-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1852-105">Einen Pfad zu den Dienstanbieter Server enthält.</span><span class="sxs-lookup"><span data-stu-id="f1852-105">Contains a path to the service provider's server.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f1852-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="f1852-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f1852-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span><span class="sxs-lookup"><span data-stu-id="f1852-107">PR_RESOURCE_PATH, PR_RESOURCE_PATH_A, PR_RESOURCE_PATH_W</span></span>  <br/> |
|<span data-ttu-id="f1852-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="f1852-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f1852-109">0x3E07</span><span class="sxs-lookup"><span data-stu-id="f1852-109">0x3E07</span></span>  <br/> |
|<span data-ttu-id="f1852-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="f1852-110">Data type:</span></span>  <br/> |<span data-ttu-id="f1852-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f1852-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f1852-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="f1852-112">Area:</span></span>  <br/> |<span data-ttu-id="f1852-113">MAPI-status</span><span class="sxs-lookup"><span data-stu-id="f1852-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1852-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1852-114">Remarks</span></span>

<span data-ttu-id="f1852-115">Der Pfad in diesen Eigenschaften enthalten stellt den vorgeschlagenen Pfad, in dem der Benutzer Ressourcen suchen kann.</span><span class="sxs-lookup"><span data-stu-id="f1852-115">The path contained in these properties represents the suggested path where the user can find resources.</span></span> <span data-ttu-id="f1852-116">Die Definition dieser Eigenschaften ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="f1852-116">The definition of these properties is provider specific.</span></span> <span data-ttu-id="f1852-117">Beispielsweise verwendet eine Anwendung zur terminplanung diese Eigenschaften, um den vorgeschlagenen Speicherort für die Planung Anwendungsdateien anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f1852-117">For example, a scheduling application uses these properties to specify the suggested location for its scheduling application files.</span></span>
  
<span data-ttu-id="f1852-118">Das messaging Benutzerprofil stellt diese Eigenschaften Komfort bereit, damit eine Clientanwendung nicht den messaging-Benutzer für ein Netzwerkpfad oder Laufwerkbuchstabens auffordern.</span><span class="sxs-lookup"><span data-stu-id="f1852-118">The messaging user profile furnishes these properties as a convenience so that a client application does not have to prompt the messaging user for a network path or network drive letter.</span></span>
  
<span data-ttu-id="f1852-119">MAPI funktioniert nur mit Dateinamen in den Zeichensatz amerikanischen National Standards Institute (ANSI).</span><span class="sxs-lookup"><span data-stu-id="f1852-119">MAPI works only with filenames in the American National Standards Institute (ANSI) character set.</span></span> <span data-ttu-id="f1852-120">Anwendungen, die Dateinamen in einem Zeichensatz OEM (Original Equipment Manufacturer) verwenden, müssen diese in ANSI konvertieren, vor dem Aufruf von MAPI.</span><span class="sxs-lookup"><span data-stu-id="f1852-120">Applications that use filenames in an original equipment manufacturer (OEM) character set must convert them to ANSI before calling MAPI.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f1852-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f1852-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="f1852-122">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="f1852-122">Header files</span></span>

<span data-ttu-id="f1852-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1852-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="f1852-124">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="f1852-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="f1852-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f1852-125">Mapitags.h</span></span>
  
> <span data-ttu-id="f1852-126">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f1852-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1852-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1852-127">See also</span></span>



[<span data-ttu-id="f1852-128">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1852-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f1852-129">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f1852-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f1852-130">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="f1852-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f1852-131">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="f1852-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

