---
title: Kanonische Pidtagattachextension (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319761"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="5932d-103">Kanonische Pidtagattachextension (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5932d-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="5932d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5932d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5932d-105">Enthält eine Dateinamenerweiterung, die den Dokumenttyp einer Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="5932d-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5932d-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="5932d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5932d-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="5932d-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="5932d-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="5932d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5932d-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="5932d-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="5932d-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="5932d-110">Data type:</span></span>  <br/> |<span data-ttu-id="5932d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5932d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="5932d-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="5932d-112">Area:</span></span>  <br/> |<span data-ttu-id="5932d-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="5932d-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5932d-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5932d-114">Remarks</span></span>

<span data-ttu-id="5932d-115">Diese Eigenschaften werden von der Clientanwendung zum Zeitpunkt der Übermittlung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5932d-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="5932d-116">Das Messagingsystem verwendet **PR_ATTACH_EXTENSION** beim Konvertieren von Nachrichtenanlagen (in-Route-Konvertierung) oder beim Starten von Anwendungen basierend auf Anlagen in empfangenen Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="5932d-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="5932d-117">Wenn der sendende Client keinen Wert für diese Eigenschaften bereitstellt, ist der Nachrichtenspeicher, der die Anlage verarbeitet, nicht dazu verpflichtet, Sie zu generieren.</span><span class="sxs-lookup"><span data-stu-id="5932d-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="5932d-118">Der empfangende Client sollte zunächst nach **PR_ATTACH_EXTENSION**suchen, und falls nicht angegeben, sollte die Dateinamenerweiterung aus der **PR_ATTACH_FILENAME** ([pidtagattachfilename (](pidtagattachfilename-canonical-property.md)) oder PR_ATTACH_LONG_FILENAME der Anlage analysiert werden. \*\* \*\*([Pidtagattachlongfilename (](pidtagattachlongfilename-canonical-property.md))-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5932d-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5932d-119">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5932d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5932d-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="5932d-120">Protocol specifications</span></span>

<span data-ttu-id="5932d-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5932d-121">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5932d-122">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="5932d-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5932d-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="5932d-123">Header files</span></span>

<span data-ttu-id="5932d-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5932d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="5932d-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5932d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="5932d-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5932d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="5932d-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="5932d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5932d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5932d-128">See also</span></span>



[<span data-ttu-id="5932d-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5932d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5932d-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="5932d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5932d-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="5932d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5932d-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="5932d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

