---
title: PidTagUserCertificate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagUserCertificate
api_type:
- COM
ms.assetid: 2ac14c43-36c1-4f2f-97b0-2462f2360575
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 0dd477a055562f692c8869bc436c4238c77fd02a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795284"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="81ef9-103">PidTagUserCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="81ef9-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="81ef9-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="81ef9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="81ef9-105">Enthält ein ASN. 1-Authentifizierungszertifikat für ein messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="81ef9-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81ef9-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="81ef9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81ef9-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="81ef9-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="81ef9-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="81ef9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81ef9-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="81ef9-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="81ef9-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="81ef9-110">Data type:</span></span>  <br/> |<span data-ttu-id="81ef9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="81ef9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="81ef9-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="81ef9-112">Area:</span></span>  <br/> |<span data-ttu-id="81ef9-113">MAPI-e-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="81ef9-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81ef9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="81ef9-114">Remarks</span></span>

<span data-ttu-id="81ef9-115">Ein Authentifizierungszertifikat ist vergleichbar mit einer digitalen Signatur.</span><span class="sxs-lookup"><span data-stu-id="81ef9-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="81ef9-116">Mehrere MAPI-Eigenschaften angeben ASN. 1-Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="81ef9-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81ef9-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81ef9-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81ef9-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="81ef9-118">Protocol specifications</span></span>

<span data-ttu-id="81ef9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81ef9-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81ef9-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="81ef9-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81ef9-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81ef9-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81ef9-122">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="81ef9-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81ef9-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="81ef9-123">Header files</span></span>

<span data-ttu-id="81ef9-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81ef9-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="81ef9-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="81ef9-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="81ef9-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81ef9-126">Mapitags.h</span></span>
  
> <span data-ttu-id="81ef9-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="81ef9-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81ef9-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81ef9-128">See also</span></span>



[<span data-ttu-id="81ef9-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81ef9-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81ef9-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81ef9-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81ef9-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="81ef9-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81ef9-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="81ef9-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

