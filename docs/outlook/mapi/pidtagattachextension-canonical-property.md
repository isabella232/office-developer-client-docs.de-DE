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
ms.openlocfilehash: 71ad53880c400d924d73c903bd77f7b447a69d8b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577723"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="ecd27-103">PidTagAttachExtension (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ecd27-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="ecd27-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecd27-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecd27-105">Enthält eine Erweiterung, die den Dokumenttyp einer Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="ecd27-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecd27-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ecd27-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecd27-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="ecd27-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="ecd27-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="ecd27-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecd27-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="ecd27-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="ecd27-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ecd27-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecd27-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ecd27-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ecd27-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ecd27-112">Area:</span></span>  <br/> |<span data-ttu-id="ecd27-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="ecd27-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecd27-114">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="ecd27-114">Remarks</span></span>

<span data-ttu-id="ecd27-115">Diese Eigenschaften werden von der Clientanwendung Zeitpunkt der Übermittlung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ecd27-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="ecd27-116">Der messaging-System verwendeten **PR_ATTACH_EXTENSION** beim Konvertieren von Nachrichtenanlagen (Konvertierung in Route) oder Starten von Anwendungen basierend auf Anlagen in empfangene Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ecd27-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="ecd27-117">Wenn der sendende Client keinen Wert für diese Eigenschaften bereitstellen, ist der Nachrichtenspeicher behandeln die Anlage nicht verpflichtet zum erzeugen.</span><span class="sxs-lookup"><span data-stu-id="ecd27-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="ecd27-118">Der empfangende Client sollte zunächst für **PR_ATTACH_EXTENSION**überprüfen, und wenn es nicht angegeben wird, sollte die Dateinamenerweiterung aus der Anlage **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) oder **PR_ATTACH_LONG_FILENAME analysieren **-Eigenschaft ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ecd27-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ecd27-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ecd27-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecd27-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="ecd27-120">Protocol specifications</span></span>

<span data-ttu-id="ecd27-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecd27-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecd27-122">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="ecd27-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecd27-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ecd27-123">Header files</span></span>

<span data-ttu-id="ecd27-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecd27-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecd27-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ecd27-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecd27-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecd27-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ecd27-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ecd27-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecd27-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecd27-128">See also</span></span>



[<span data-ttu-id="ecd27-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecd27-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecd27-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ecd27-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecd27-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ecd27-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecd27-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ecd27-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

