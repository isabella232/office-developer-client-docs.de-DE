---
title: PidTagRecipientCertificate (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientCertificate
api_type:
- COM
ms.assetid: 7c5c749e-5463-4935-85b5-32219d06f782
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431666"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="056b1-103">PidTagRecipientCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="056b1-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="056b1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="056b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="056b1-105">Enthält das ASN.1-Zertifikat eines Nachrichtenempfängers zur Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="056b1-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="056b1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="056b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="056b1-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="056b1-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="056b1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="056b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="056b1-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="056b1-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="056b1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="056b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="056b1-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="056b1-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="056b1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="056b1-112">Area:</span></span>  <br/> |<span data-ttu-id="056b1-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="056b1-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="056b1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="056b1-114">Remarks</span></span>

<span data-ttu-id="056b1-115">Diese Eigenschaft ist eine Kopie der PR_USER_CERTIFICATE **(** [PidTagUserCertificate](pidtagusercertificate-canonical-property.md))-Eigenschaft des Empfängers zur Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="056b1-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="056b1-116">Sie kann verwendet werden, um dem Absender nachzuweisen, dass der Empfänger die Nachricht tatsächlich empfangen hat, was in einem Zustellungsbericht nicht notwendigerweise angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="056b1-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="056b1-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="056b1-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="056b1-118">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="056b1-118">Header files</span></span>

<span data-ttu-id="056b1-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="056b1-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="056b1-120">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="056b1-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="056b1-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="056b1-121">Mapitags.h</span></span>
  
> <span data-ttu-id="056b1-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="056b1-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="056b1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="056b1-123">See also</span></span>



[<span data-ttu-id="056b1-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="056b1-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="056b1-125">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="056b1-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="056b1-126">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="056b1-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="056b1-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="056b1-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

