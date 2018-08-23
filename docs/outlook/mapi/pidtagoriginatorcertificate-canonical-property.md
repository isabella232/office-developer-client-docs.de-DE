---
title: PidTagOriginatorCertificate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorCertificate
api_type:
- COM
ms.assetid: 65f890d8-9d25-408e-ab29-89991278b92d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 966af9b3b3cbe52031402450be324ab6821d53ac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586578"
---
# <a name="pidtagoriginatorcertificate-canonical-property"></a><span data-ttu-id="6bc45-103">PidTagOriginatorCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6bc45-103">PidTagOriginatorCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="6bc45-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bc45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bc45-105">Ein ASN. 1-Zertifikat für den Absender der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="6bc45-105">Contains an ASN.1 certificate for the message originator.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6bc45-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6bc45-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6bc45-107">PR_ORIGINATOR_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="6bc45-107">PR_ORIGINATOR_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="6bc45-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6bc45-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6bc45-109">0 x 0022</span><span class="sxs-lookup"><span data-stu-id="6bc45-109">0x0022</span></span>  <br/> |
|<span data-ttu-id="6bc45-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6bc45-110">Data type:</span></span>  <br/> |<span data-ttu-id="6bc45-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="6bc45-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="6bc45-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6bc45-112">Area:</span></span>  <br/> |<span data-ttu-id="6bc45-113">MIME</span><span class="sxs-lookup"><span data-stu-id="6bc45-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bc45-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="6bc45-114">Remarks</span></span>

<span data-ttu-id="6bc45-115">Diese Eigenschaft ist eine Kopie der Absender **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6bc45-115">This property is a copy of the originator's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6bc45-116">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6bc45-116">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6bc45-117">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="6bc45-117">Header files</span></span>

<span data-ttu-id="6bc45-118">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6bc45-118">Mapidefs.h</span></span>
  
> <span data-ttu-id="6bc45-119">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="6bc45-119">Provides data type definitions.</span></span>
    
<span data-ttu-id="6bc45-120">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6bc45-120">Mapitags.h</span></span>
  
> <span data-ttu-id="6bc45-121">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="6bc45-121">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6bc45-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6bc45-122">See also</span></span>



[<span data-ttu-id="6bc45-123">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bc45-123">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6bc45-124">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6bc45-124">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6bc45-125">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6bc45-125">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6bc45-126">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6bc45-126">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

