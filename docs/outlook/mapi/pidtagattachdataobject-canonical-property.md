---
title: PidTagAttachDataObject (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataObject
api_type:
- HeaderDef
ms.assetid: b76312c6-7682-4ded-be25-55e21b0b091b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3961330476cad8947f94152e49c90adb1e8f8b21
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398073"
---
# <a name="pidtagattachdataobject-canonical-property"></a><span data-ttu-id="bdda5-103">PidTagAttachDataObject (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="bdda5-103">PidTagAttachDataObject Canonical Property</span></span>

  
  
<span data-ttu-id="bdda5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bdda5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bdda5-105">Enthält ein Attachment-Objekt in der Regel über die Schnittstelle Object Linking and Embedding (OLE) **IStorage** zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="bdda5-105">Contains an attachment object typically accessed through the Object Linking and Embedding (OLE) **IStorage** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bdda5-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="bdda5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bdda5-107">PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="bdda5-107">PR_ATTACH_DATA_OBJ</span></span>  <br/> |
|<span data-ttu-id="bdda5-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="bdda5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bdda5-109">0x3701</span><span class="sxs-lookup"><span data-stu-id="bdda5-109">0x3701</span></span>  <br/> |
|<span data-ttu-id="bdda5-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="bdda5-110">Data type:</span></span>  <br/> |<span data-ttu-id="bdda5-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="bdda5-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="bdda5-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="bdda5-112">Area:</span></span>  <br/> |<span data-ttu-id="bdda5-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="bdda5-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bdda5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bdda5-114">Remarks</span></span>

<span data-ttu-id="bdda5-115">Diese Eigenschaft enthält das Attachment-Objekt, wenn der Wert der Eigenschaft **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) **ATTACH_EMBEDDED_MSG** oder **ATTACH_OLE**ist.</span><span class="sxs-lookup"><span data-stu-id="bdda5-115">This property holds the attachment when the value of the **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) property is **ATTACH_EMBEDDED_MSG** or **ATTACH_OLE**.</span></span> <span data-ttu-id="bdda5-116">Das Codierungstyp OLE kann aus **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="bdda5-116">The OLE encoding type can be determined from **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)).</span></span> 
  
<span data-ttu-id="bdda5-117">Für eine Anlage **ATTACH_EMBEDDED_MSG** Wert zugeordnet ist kann die [IMessage:IMAPIProp](imessageimapiprop.md) -Schnittstelle für einen schnelleren Zugriff verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdda5-117">For an attachment associated with the **ATTACH_EMBEDDED_MSG** value, the [IMessage:IMAPIProp](imessageimapiprop.md) interface can be used for faster access.</span></span> 
  
<span data-ttu-id="bdda5-118">Bei einem eingebetteten dynamische OLE-Objekt die **PR_ATTACH_DATA_OBJ** -Eigenschaft enthält eine eigenen Renderinginformationen und die **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md))-Eigenschaft sollte entweder nicht vorhanden oder leer sein.</span><span class="sxs-lookup"><span data-stu-id="bdda5-118">For an embedded dynamic OLE object, the **PR_ATTACH_DATA_OBJ** property contains its own rendering information, and the **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) property should be either nonexistent or empty.</span></span> 
  
<span data-ttu-id="bdda5-119">Für ein OLE-Dokument-Dateianlage Anbieter die Nachricht muss auf einen Aufruf [IMAPIProp::OpenProperty](imapiprop-openproperty.md) **PR_ATTACH_DATA_OBJ** reagieren und reagiert optional zu einem Anruf auf **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="bdda5-119">For an OLE document file attachment, the message store provider must respond to an [IMAPIProp::OpenProperty](imapiprop-openproperty.md) call on **PR_ATTACH_DATA_OBJ** and may optionally respond to a call on **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)).</span></span> <span data-ttu-id="bdda5-120">Die Eigenschaften **PR_ATTACH_DATA_BIN** und **PR_ATTACH_DATA_OBJ** Freigeben der Bezeichner für die gleichen und daher sind zwei Darstellungen der gleichen-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bdda5-120">The **PR_ATTACH_DATA_BIN** and **PR_ATTACH_DATA_OBJ** properties share the same property identifier and thus are two renditions of the same property.</span></span> 
  
<span data-ttu-id="bdda5-121">Für ein Speicherobjekt können beispielsweise eine Verbunddatei in OLE 2.0-Dokumentdatei-Format, einige Dienstanbieter geöffnet werden, mit der MAPI- **IStreamDocfile** -Schnittstelle eine Unterklasse der **IStream** ohne zusätzliche Mitglieder, entwickelt, um die Leistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="bdda5-121">For a storage object, such as a compound file in OLE 2.0 docfile format, some service providers allow it to be opened with the MAPI **IStreamDocfile** interface, a subclass of **IStream** with no additional members, designed to optimize performance.</span></span> <span data-ttu-id="bdda5-122">Das potenzielle speichern reicht zu rechtfertigen Versuch **PR_ATTACH_DATA_OBJ** über **IStreamDocfile**zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bdda5-122">The potential saving is enough to justify attempting to open **PR_ATTACH_DATA_OBJ** through **IStreamDocfile**.</span></span> <span data-ttu-id="bdda5-123">Wenn **MAPI_E_INTERFACE_NOT_SUPPORTED** zurückgegeben wurde, kann der Client **PR_ATTACH_DATA_BIN** mit **IStream**öffnen.</span><span class="sxs-lookup"><span data-stu-id="bdda5-123">If **MAPI_E_INTERFACE_NOT_SUPPORTED** is returned, the client can then open **PR_ATTACH_DATA_BIN** with **IStream**.</span></span> 
  
<span data-ttu-id="bdda5-124">Wenn der Clientanwendung oder Dienstanbieter ein Unterobjekt Anlage nicht öffnen kann mithilfe von **PR_ATTACH_DATA_OBJ** mit Hilfe von **PR_ATTACH_METHOD**, sollte **PR_ATTACH_DATA_BIN**verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bdda5-124">If the client application or service provider cannot open an attachment subobject by using **PR_ATTACH_DATA_OBJ** with the help of **PR_ATTACH_METHOD**, it should use **PR_ATTACH_DATA_BIN**.</span></span> 
  
<span data-ttu-id="bdda5-125">Weitere Informationen zu OLE-Schnittstellen und Formate finden Sie unter [OLE und Daten übertragen](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span><span class="sxs-lookup"><span data-stu-id="bdda5-125">For more information on OLE interfaces and formats, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="bdda5-126">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bdda5-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bdda5-127">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="bdda5-127">Protocol specifications</span></span>

<span data-ttu-id="bdda5-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bdda5-128">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bdda5-129">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="bdda5-129">Handles message and attachment objects.</span></span>
    
## <a name="header-files"></a><span data-ttu-id="bdda5-130">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="bdda5-130">Header Files</span></span>

<span data-ttu-id="bdda5-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bdda5-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="bdda5-132">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="bdda5-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="bdda5-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="bdda5-133">Mapitags.h</span></span>
  
> <span data-ttu-id="bdda5-134">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="bdda5-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bdda5-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdda5-135">See also</span></span>



[<span data-ttu-id="bdda5-136">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bdda5-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bdda5-137">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bdda5-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bdda5-138">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="bdda5-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bdda5-139">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="bdda5-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

