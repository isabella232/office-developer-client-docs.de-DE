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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0863973a420920189cc32324154f1125a2b068fa
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569946"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="81582-103">PidTagUserCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="81582-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="81582-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81582-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81582-105">Enthält ein ASN. 1-Authentifizierungszertifikat für ein messaging-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="81582-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81582-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="81582-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="81582-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="81582-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="81582-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="81582-108">Identifier:</span></span>  <br/> |<span data-ttu-id="81582-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="81582-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="81582-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="81582-110">Data type:</span></span>  <br/> |<span data-ttu-id="81582-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="81582-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="81582-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="81582-112">Area:</span></span>  <br/> |<span data-ttu-id="81582-113">MAPI-e-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="81582-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="81582-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="81582-114">Remarks</span></span>

<span data-ttu-id="81582-115">Ein Authentifizierungszertifikat ist vergleichbar mit einer digitalen Signatur.</span><span class="sxs-lookup"><span data-stu-id="81582-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="81582-116">Mehrere MAPI-Eigenschaften angeben ASN. 1-Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="81582-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="81582-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="81582-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="81582-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="81582-118">Protocol specifications</span></span>

<span data-ttu-id="81582-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81582-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81582-120">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="81582-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="81582-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="81582-121">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="81582-122">Gibt die Eigenschaften und Operationen für Listen der Benutzer, Kontakte, Gruppen und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="81582-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="81582-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="81582-123">Header files</span></span>

<span data-ttu-id="81582-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="81582-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="81582-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="81582-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="81582-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="81582-126">Mapitags.h</span></span>
  
> <span data-ttu-id="81582-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="81582-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="81582-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="81582-128">See also</span></span>



[<span data-ttu-id="81582-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81582-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="81582-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="81582-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="81582-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="81582-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="81582-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="81582-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

