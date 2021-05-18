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
ms.openlocfilehash: 53ee4019752cf717840199d4a51cbc90133b8636
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320391"
---
# <a name="pidtagusercertificate-canonical-property"></a><span data-ttu-id="84af7-103">PidTagUserCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="84af7-103">PidTagUserCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="84af7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84af7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84af7-105">Enthält ein ASN.1-Authentifizierungszertifikat für einen Messagingbenutzer.</span><span class="sxs-lookup"><span data-stu-id="84af7-105">Contains an ASN.1 authentication certificate for a messaging user.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84af7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="84af7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="84af7-107">PR_USER_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="84af7-107">PR_USER_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="84af7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="84af7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="84af7-109">0x3A22</span><span class="sxs-lookup"><span data-stu-id="84af7-109">0x3A22</span></span>  <br/> |
|<span data-ttu-id="84af7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="84af7-110">Data type:</span></span>  <br/> |<span data-ttu-id="84af7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="84af7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="84af7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="84af7-112">Area:</span></span>  <br/> |<span data-ttu-id="84af7-113">MAPI-E-Mail-Benutzer</span><span class="sxs-lookup"><span data-stu-id="84af7-113">MAPI mail user</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84af7-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84af7-114">Remarks</span></span>

<span data-ttu-id="84af7-115">Ein Authentifizierungszertifikat ähnelt einer digitalen Signatur.</span><span class="sxs-lookup"><span data-stu-id="84af7-115">An authentication certificate is similar to a digital signature.</span></span> <span data-ttu-id="84af7-116">Mehrere MAPI-Eigenschaften liefern ASN.1-Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="84af7-116">Several MAPI properties supply ASN.1 certificates.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="84af7-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="84af7-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="84af7-118">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="84af7-118">Protocol specifications</span></span>

<span data-ttu-id="84af7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84af7-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84af7-120">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="84af7-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="84af7-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="84af7-121">[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="84af7-122">Gibt die Eigenschaften und Vorgänge für Listen von Benutzern, Kontakten, Gruppen und Ressourcen an.</span><span class="sxs-lookup"><span data-stu-id="84af7-122">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="84af7-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="84af7-123">Header files</span></span>

<span data-ttu-id="84af7-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="84af7-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="84af7-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="84af7-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="84af7-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="84af7-126">Mapitags.h</span></span>
  
> <span data-ttu-id="84af7-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="84af7-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84af7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84af7-128">See also</span></span>



[<span data-ttu-id="84af7-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="84af7-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="84af7-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="84af7-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="84af7-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="84af7-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="84af7-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="84af7-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

