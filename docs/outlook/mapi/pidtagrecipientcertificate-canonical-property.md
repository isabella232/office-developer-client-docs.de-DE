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
ms.openlocfilehash: 464db3d360f6e872ac28f8d7cbec842d8b521f7e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585115"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="1dfbf-103">PidTagRecipientCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1dfbf-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="1dfbf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1dfbf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1dfbf-105">Enthält einen Nachrichtenempfänger ASN. 1-Zertifikat für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="1dfbf-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1dfbf-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1dfbf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1dfbf-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="1dfbf-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="1dfbf-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1dfbf-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1dfbf-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="1dfbf-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="1dfbf-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1dfbf-110">Data type:</span></span>  <br/> |<span data-ttu-id="1dfbf-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1dfbf-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1dfbf-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1dfbf-112">Area:</span></span>  <br/> |<span data-ttu-id="1dfbf-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="1dfbf-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1dfbf-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dfbf-114">Remarks</span></span>

<span data-ttu-id="1dfbf-115">Diese Eigenschaft ist eine Kopie des Empfängers **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md))-Eigenschaft für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="1dfbf-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="1dfbf-116">Hiermit können Sie an den Ersteller nachweisen, dass der Empfänger tatsächlich die Nachricht empfangen hat, die die ein Unzustellbarkeitsberichts nicht notwendigerweise aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1dfbf-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1dfbf-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1dfbf-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1dfbf-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="1dfbf-118">Header files</span></span>

<span data-ttu-id="1dfbf-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1dfbf-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1dfbf-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1dfbf-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1dfbf-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1dfbf-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1dfbf-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1dfbf-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1dfbf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dfbf-123">See also</span></span>



[<span data-ttu-id="1dfbf-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dfbf-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1dfbf-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1dfbf-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1dfbf-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1dfbf-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1dfbf-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1dfbf-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

