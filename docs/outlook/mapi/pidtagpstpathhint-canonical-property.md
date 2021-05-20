---
title: PidTagPstPathHint (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 9cb4af50-3735-4029-a608-a6e7927019dd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6415ddcec2823192967b8869b46b22b58b08ba5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437308"
---
# <a name="pidtagpstpathhint-canonical-property"></a><span data-ttu-id="b4954-103">PidTagPstPathHint (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b4954-103">PidTagPstPathHint Canonical Property</span></span>

  
  
<span data-ttu-id="b4954-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4954-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4954-105">Stellt den Namen der persönlichen Speichertabelle (PST-Datei) für das Konfigurationsdialogfeld zur Verfügung, den der Benutzer bearbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="b4954-105">Provides the personal storage table (.pst file) name, which the user can edit, for the configuration dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4954-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="b4954-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b4954-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span><span class="sxs-lookup"><span data-stu-id="b4954-107">PR_PST_PATH_HINT, PR_PST_PATH_HINT_A, PR_PST_PATH_HINT_W</span></span>  <br/> |
|<span data-ttu-id="b4954-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="b4954-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b4954-109">0x6771</span><span class="sxs-lookup"><span data-stu-id="b4954-109">0x6771</span></span>  <br/> |
|<span data-ttu-id="b4954-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="b4954-110">Data type:</span></span>  <br/> |<span data-ttu-id="b4954-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b4954-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b4954-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="b4954-112">Area:</span></span>  <br/> |<span data-ttu-id="b4954-113">Interne Persönliche Speichertabelle (PST)</span><span class="sxs-lookup"><span data-stu-id="b4954-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4954-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4954-114">Remarks</span></span>

<span data-ttu-id="b4954-115">Wenn stattdessen die **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) -Eigenschaft verwendet wird, wird das Konfigurationsdialogfeld geöffnet, aber der Benutzer kann den Pfad und viele andere Eigenschaften nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="b4954-115">If the **PR_PST_PATH** ([PidTagPstPath](pidtagpstpath-canonical-property.md)) property is used instead, the configuration dialog box will open, but the user will not be allowed to edit the path and many other properties.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b4954-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b4954-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b4954-117">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="b4954-117">Protocol specifications</span></span>

<span data-ttu-id="b4954-118">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="b4954-118">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="b4954-119">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="b4954-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b4954-120">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="b4954-120">Header files</span></span>

<span data-ttu-id="b4954-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4954-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="b4954-122">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="b4954-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="b4954-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b4954-123">Mapitags.h</span></span>
  
> <span data-ttu-id="b4954-124">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b4954-124">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b4954-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4954-125">See also</span></span>



[<span data-ttu-id="b4954-126">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b4954-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b4954-127">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="b4954-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b4954-128">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="b4954-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b4954-129">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="b4954-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

