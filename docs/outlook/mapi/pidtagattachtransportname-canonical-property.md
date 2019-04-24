---
title: Kanonische Pidtagattachtransportname (-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361068"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="014db-103">Kanonische Pidtagattachtransportname (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="014db-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="014db-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="014db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="014db-105">Enthält den Namen einer Anlagendatei, die so geändert wurde, dass Sie TNEF-Nachrichten zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="014db-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="014db-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="014db-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="014db-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="014db-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="014db-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="014db-108">Identifier:</span></span>  <br/> |<span data-ttu-id="014db-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="014db-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="014db-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="014db-110">Data type:</span></span>  <br/> |<span data-ttu-id="014db-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="014db-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="014db-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="014db-112">Area:</span></span>  <br/> |<span data-ttu-id="014db-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="014db-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="014db-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="014db-114">Remarks</span></span>

<span data-ttu-id="014db-115">TNEF und der Transportanbieter verwenden diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="014db-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="014db-116">Sie sind in der Regel nicht für Clientanwendungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="014db-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="014db-117">Diese Eigenschaften werden in der Regel von TNEF verwendet, wenn das zugrunde liegende Messagingsystem die angegebenen Dateinamen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="014db-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="014db-118">Sie werden beispielsweise verwendet, wenn der Benutzer mehrere Dateien mit demselben Namen anfügt, beispielsweise fünf Dateien mit dem Namen CONFIG. SYS.</span><span class="sxs-lookup"><span data-stu-id="014db-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="014db-119">Der Transportanbieter muss die Namen ändern, um sicherzustellen, dass er eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="014db-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="014db-120">Jeder geänderte Name wird in den **PR_ATTACH_TRANSPORT_NAME** -und zugehörigen Eigenschaften der Anlage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="014db-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="014db-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="014db-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="014db-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="014db-122">Protocol specifications</span></span>

<span data-ttu-id="014db-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="014db-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="014db-124">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="014db-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="014db-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="014db-125">Header files</span></span>

<span data-ttu-id="014db-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="014db-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="014db-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="014db-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="014db-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="014db-128">Mapitags.h</span></span>
  
> <span data-ttu-id="014db-129">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="014db-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="014db-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="014db-130">See also</span></span>



[<span data-ttu-id="014db-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="014db-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="014db-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="014db-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="014db-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="014db-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="014db-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="014db-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

