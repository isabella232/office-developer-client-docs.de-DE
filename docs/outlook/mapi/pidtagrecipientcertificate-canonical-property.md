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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bb51e9a602bd5c2e59bb56fdbf44fddc39651de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794909"
---
# <a name="pidtagrecipientcertificate-canonical-property"></a><span data-ttu-id="496c5-103">PidTagRecipientCertificate (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="496c5-103">PidTagRecipientCertificate Canonical Property</span></span>

  
  
<span data-ttu-id="496c5-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="496c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="496c5-105">Enthält einen Nachrichtenempfänger ASN. 1-Zertifikat für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="496c5-105">Contains a message recipient's ASN.1 certificate for use in a report.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="496c5-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="496c5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="496c5-107">PR_RECIPIENT_CERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="496c5-107">PR_RECIPIENT_CERTIFICATE</span></span>  <br/> |
|<span data-ttu-id="496c5-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="496c5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="496c5-109">0x0C13</span><span class="sxs-lookup"><span data-stu-id="496c5-109">0x0C13</span></span>  <br/> |
|<span data-ttu-id="496c5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="496c5-110">Data type:</span></span>  <br/> |<span data-ttu-id="496c5-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="496c5-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="496c5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="496c5-112">Area:</span></span>  <br/> |<span data-ttu-id="496c5-113">MAPI-Empfänger</span><span class="sxs-lookup"><span data-stu-id="496c5-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="496c5-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="496c5-114">Remarks</span></span>

<span data-ttu-id="496c5-115">Diese Eigenschaft ist eine Kopie des Empfängers **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md))-Eigenschaft für die Verwendung in einem Bericht.</span><span class="sxs-lookup"><span data-stu-id="496c5-115">This property is a copy of the recipient's **PR_USER_CERTIFICATE** ([PidTagUserCertificate](pidtagusercertificate-canonical-property.md)) property for use in a report.</span></span> <span data-ttu-id="496c5-116">Hiermit können Sie an den Ersteller nachweisen, dass der Empfänger tatsächlich die Nachricht empfangen hat, die die ein Unzustellbarkeitsberichts nicht notwendigerweise aufweisen.</span><span class="sxs-lookup"><span data-stu-id="496c5-116">It can be used to prove to the originator that the recipient actually received the message, which a delivery report does not necessarily indicate.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="496c5-117">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="496c5-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="496c5-118">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="496c5-118">Header files</span></span>

<span data-ttu-id="496c5-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="496c5-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="496c5-120">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="496c5-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="496c5-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="496c5-121">Mapitags.h</span></span>
  
> <span data-ttu-id="496c5-122">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="496c5-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="496c5-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="496c5-123">See also</span></span>



[<span data-ttu-id="496c5-124">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="496c5-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="496c5-125">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="496c5-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="496c5-126">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="496c5-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="496c5-127">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="496c5-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

