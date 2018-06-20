---
title: Kanonische PidTagAttachExtension-Eigenschaft
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
ms.openlocfilehash: 4d71a0e26e2043bbaf961ae5096afc5789be36be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794097"
---
# <a name="pidtagattachextension-canonical-property"></a><span data-ttu-id="29b57-103">Kanonische PidTagAttachExtension-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="29b57-103">PidTagAttachExtension Canonical Property</span></span>

  
  
<span data-ttu-id="29b57-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="29b57-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="29b57-105">Enthält eine Erweiterung, die den Dokumenttyp einer Anlage angibt.</span><span class="sxs-lookup"><span data-stu-id="29b57-105">Contains a file name extension that indicates the document type of an attachment.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29b57-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="29b57-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="29b57-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span><span class="sxs-lookup"><span data-stu-id="29b57-107">PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W</span></span>  <br/> |
|<span data-ttu-id="29b57-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="29b57-108">Identifier:</span></span>  <br/> |<span data-ttu-id="29b57-109">0x3703</span><span class="sxs-lookup"><span data-stu-id="29b57-109">0x3703</span></span>  <br/> |
|<span data-ttu-id="29b57-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="29b57-110">Data type:</span></span>  <br/> |<span data-ttu-id="29b57-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="29b57-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="29b57-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="29b57-112">Area:</span></span>  <br/> |<span data-ttu-id="29b57-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="29b57-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29b57-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="29b57-114">Remarks</span></span>

<span data-ttu-id="29b57-115">Diese Eigenschaften werden von der Clientanwendung Zeitpunkt der Übermittlung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29b57-115">These properties are set by the client application at submission time.</span></span> 
  
<span data-ttu-id="29b57-116">Der messaging-System verwendeten **PR_ATTACH_EXTENSION** beim Konvertieren von Nachrichtenanlagen (Konvertierung in Route) oder Starten von Anwendungen basierend auf Anlagen in empfangene Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="29b57-116">The messaging system uses **PR_ATTACH_EXTENSION** when converting message attachments (in-route conversion) or launching applications based on attachments in received messages.</span></span> <span data-ttu-id="29b57-117">Wenn der sendende Client keinen Wert für diese Eigenschaften bereitstellen, ist der Nachrichtenspeicher behandeln die Anlage nicht verpflichtet zum erzeugen.</span><span class="sxs-lookup"><span data-stu-id="29b57-117">If the sending client does not provide a value for these properties, the message store handling the attachment is not obligated to generate it.</span></span> <span data-ttu-id="29b57-118">Der empfangende Client sollte zunächst für **PR_ATTACH_EXTENSION**überprüfen, und wenn es nicht angegeben wird, sollte die Dateinamenerweiterung aus der Anlage **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) oder **PR_ATTACH_LONG_FILENAME analysieren **-Eigenschaft ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="29b57-118">The receiving client should first check for **PR_ATTACH_EXTENSION**, and if it is not provided, should parse the file name extension from the attachment's **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) or **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="29b57-119">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="29b57-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="29b57-120">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="29b57-120">Protocol specifications</span></span>

<span data-ttu-id="29b57-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="29b57-121">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="29b57-122">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="29b57-122">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="29b57-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="29b57-123">Header files</span></span>

<span data-ttu-id="29b57-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="29b57-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="29b57-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="29b57-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="29b57-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="29b57-126">Mapitags.h</span></span>
  
> <span data-ttu-id="29b57-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="29b57-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29b57-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29b57-128">See also</span></span>



[<span data-ttu-id="29b57-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29b57-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="29b57-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="29b57-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="29b57-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="29b57-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="29b57-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="29b57-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

