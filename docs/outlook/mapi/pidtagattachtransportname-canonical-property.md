---
title: Kanonische PidTagAttachTransportName-Eigenschaft
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
ms.openlocfilehash: 6828a6436946de27020fa1177223955e07a08faf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794130"
---
# <a name="pidtagattachtransportname-canonical-property"></a><span data-ttu-id="28040-103">Kanonische PidTagAttachTransportName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="28040-103">PidTagAttachTransportName Canonical Property</span></span>

  
  
<span data-ttu-id="28040-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="28040-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="28040-105">Enthält den Namen einer Anlage-Datei geändert, sodass es TNEF-Nachrichten zugeordnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="28040-105">Contains the name of an attachment file modified so that it can be associated with TNEF messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28040-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="28040-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="28040-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span><span class="sxs-lookup"><span data-stu-id="28040-107">PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W</span></span>  <br/> |
|<span data-ttu-id="28040-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="28040-108">Identifier:</span></span>  <br/> |<span data-ttu-id="28040-109">0x370C</span><span class="sxs-lookup"><span data-stu-id="28040-109">0x370C</span></span>  <br/> |
|<span data-ttu-id="28040-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="28040-110">Data type:</span></span>  <br/> |<span data-ttu-id="28040-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="28040-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="28040-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="28040-112">Area:</span></span>  <br/> |<span data-ttu-id="28040-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="28040-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28040-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28040-114">Remarks</span></span>

<span data-ttu-id="28040-115">TNEF und der Adressbuchhierarchie verwenden diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="28040-115">TNEF and the transport provider use these properties.</span></span> <span data-ttu-id="28040-116">Sie sind in der Regel nicht Clientanwendungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="28040-116">They are usually not available to client applications.</span></span> 
  
<span data-ttu-id="28040-117">Diese Eigenschaften werden häufig von TNEF verwendet, wenn das zugrunde liegende messaging-System die angegebenen Dateinamen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="28040-117">These properties are commonly used by TNEF when the underlying messaging system does not support the supplied filenames.</span></span> <span data-ttu-id="28040-118">Beispielsweise werden sie verwendet, wenn der Benutzer mehrere Dateien mit dem gleichen Namen, beispielsweise fünf Dateien mit dem Namen CONFIG angehängt wird. SYS.</span><span class="sxs-lookup"><span data-stu-id="28040-118">For example, they are used when the user attaches multiple files with the same name, such as five files named CONFIG.SYS.</span></span> <span data-ttu-id="28040-119">Der Transportdienst müssen Sie sicherstellen, dass sie eindeutig sind die Namen ändern.</span><span class="sxs-lookup"><span data-stu-id="28040-119">The transport provider must modify the names to make sure they are unique.</span></span> <span data-ttu-id="28040-120">Jede geänderte Name wird in der Anlage **PR_ATTACH_TRANSPORT_NAME** und zugeordneten Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="28040-120">Each modified name appears in its attachment's **PR_ATTACH_TRANSPORT_NAME** and associated properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="28040-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28040-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="28040-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="28040-122">Protocol specifications</span></span>

<span data-ttu-id="28040-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="28040-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="28040-124">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="28040-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="28040-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="28040-125">Header files</span></span>

<span data-ttu-id="28040-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="28040-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="28040-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="28040-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="28040-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="28040-128">Mapitags.h</span></span>
  
> <span data-ttu-id="28040-129">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="28040-129">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="28040-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28040-130">See also</span></span>



[<span data-ttu-id="28040-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28040-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="28040-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28040-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="28040-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="28040-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="28040-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="28040-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

