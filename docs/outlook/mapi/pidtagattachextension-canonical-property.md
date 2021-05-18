---
title: PidTagAttachExtension (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319761"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="1d4c1-103">PidTagAttachExtension (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="1d4c1-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="1d4c1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d4c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d4c1-105">Enthält eine Dateinamenerweiterung, die den Dokumenttyp einer Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1d4c1-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="1d4c1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1d4c1-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="1d4c1-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="1d4c1-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="1d4c1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1d4c1-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="1d4c1-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="1d4c1-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="1d4c1-110">Data type:</span></span>  <br/> |<span data-ttu-id="1d4c1-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1d4c1-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1d4c1-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="1d4c1-112">Area:</span></span>  <br/> |<span data-ttu-id="1d4c1-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="1d4c1-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d4c1-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d4c1-114">Remarks</span></span>

<span data-ttu-id="1d4c1-115">Diese Eigenschaften werden von der Clientanwendung zur Übermittlungszeit festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="1d4c1-116">Das Messagingsystem **verwendet** PR_ATTACH_EXTENSION beim Konvertieren von Nachrichtenanlagen (In-Route-Konvertierung) oder beim Starten von Anwendungen basierend auf Anlagen in empfangenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="1d4c1-117">Wenn der sendende Client keinen Wert für diese Eigenschaften zur Verfügung stellt, ist der Nachrichtenspeicher, der die Anlage verwendet, nicht verpflichtet, ihn zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="1d4c1-118">Der empfangende Client sollte zuerst nach **PR_ATTACH_EXTENSION** suchen, und wenn er nicht bereitgestellt wird, sollte die Dateinamenerweiterung aus der **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) oder **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md))-Eigenschaft der Anlage analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1d4c1-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1d4c1-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1d4c1-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="1d4c1-120">Protocol specifications</span></span>

<span data-ttu-id="1d4c1-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1d4c1-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1d4c1-122">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1d4c1-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="1d4c1-123">Header files</span></span>

<span data-ttu-id="1d4c1-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1d4c1-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="1d4c1-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="1d4c1-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1d4c1-126">Mapitags.h</span></span>
  
> <span data-ttu-id="1d4c1-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="1d4c1-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1d4c1-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d4c1-128">See also</span></span>



[<span data-ttu-id="1d4c1-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1d4c1-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1d4c1-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="1d4c1-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1d4c1-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="1d4c1-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1d4c1-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="1d4c1-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

