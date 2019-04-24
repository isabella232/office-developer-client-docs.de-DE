---
title: Kanonische Pidtagrecipientcertificate (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c659b77767fddc4c783732082c2eb65c68af8dbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356714"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="59ea7-103">Kanonische Pidtagrecipientcertificate (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59ea7-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="59ea7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59ea7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59ea7-105">Enthält das ASN. 1-Zertifikat eines Nachrichtenempfängers für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="59ea7-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="59ea7-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="59ea7-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="59ea7-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="59ea7-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="59ea7-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="59ea7-108">Identifier:</span></span>  <br/> |<span data-ttu-id="59ea7-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="59ea7-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="59ea7-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="59ea7-110">Data type:</span></span>  <br/> |<span data-ttu-id="59ea7-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="59ea7-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="59ea7-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="59ea7-112">Area:</span></span>  <br/> |<span data-ttu-id="59ea7-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="59ea7-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="59ea7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59ea7-114">Remarks</span></span>

<span data-ttu-id="59ea7-115">Diese Eigenschaft ist eine Kopie der **PR_USER_CERTIFICATE** ([pidtagusercertificate (](pidtagusercertificate-canonical-property.md))-Eigenschaft des Empfängers für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="59ea7-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="59ea7-116">Es kann verwendet werden, um dem Absender zu beweisen, dass der Empfänger die Nachricht tatsächlich erhalten hat, die ein zugestellter Bericht nicht unbedingt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="59ea7-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="59ea7-117">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="59ea7-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="59ea7-118">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="59ea7-118">Header files</span></span>

<span data-ttu-id="59ea7-119">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="59ea7-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="59ea7-120">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="59ea7-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="59ea7-121">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="59ea7-121">Mapitags.h</span></span>
  
> <span data-ttu-id="59ea7-122">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="59ea7-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="59ea7-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59ea7-123">See also</span></span>



[<span data-ttu-id="59ea7-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59ea7-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="59ea7-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="59ea7-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="59ea7-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="59ea7-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="59ea7-127">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="59ea7-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

