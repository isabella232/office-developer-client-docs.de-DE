---
title: PidTagReceiveFolderSettings (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e93325873f1d9e89bb591d136df04aa27403375f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794901"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="ed53c-103">PidTagReceiveFolderSettings (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ed53c-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="ed53c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed53c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed53c-105">Enthält eine Tabelle mit einer Nachricht des Speichers erhalten Ordner Settings.</span><span class="sxs-lookup"><span data-stu-id="ed53c-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed53c-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="ed53c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ed53c-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="ed53c-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="ed53c-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="ed53c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ed53c-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="ed53c-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="ed53c-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="ed53c-110">Data type:</span></span>  <br/> |<span data-ttu-id="ed53c-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="ed53c-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="ed53c-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="ed53c-112">Area:</span></span>  <br/> |<span data-ttu-id="ed53c-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="ed53c-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed53c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed53c-114">Remarks</span></span>

<span data-ttu-id="ed53c-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo](imapiprop-copyto.md) Vorgänge aus- oder in [IMAPIProp::CopyProps](imapiprop-copyprops.md) Vorgänge eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="ed53c-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="ed53c-116">Als Eigenschaft vom Typ PT_OBJECT kann nicht es erfolgreich von der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode abgerufen werden. von der [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode die Schnittstelle mit der ID IID_IMAPITable anfordern sollte seinen Inhalt zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="ed53c-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="ed53c-117">Dienstanbieter müssen es an die [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode melden, wenn er festgelegt ist, jedoch kann positives oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ed53c-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="ed53c-118">Zum Abrufen von Inhaltsverzeichnisses sollte eine Clientanwendung die [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ed53c-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="ed53c-119">Weitere Informationen finden Sie unter [Ordner Tabellen erhalten](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="ed53c-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="ed53c-120">Diese Eigenschaft enthält eine Tabelle von Zuordnungen der Ordner für den Nachrichtenspeicher empfangen.</span><span class="sxs-lookup"><span data-stu-id="ed53c-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="ed53c-121">Aufrufen von **OpenProperty** für diese Eigenschaft entspricht dem Aufrufen von **GetReceiveFolderTable** für den Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ed53c-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="ed53c-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ed53c-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="ed53c-123">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="ed53c-123">Header files</span></span>

<span data-ttu-id="ed53c-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ed53c-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="ed53c-125">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="ed53c-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="ed53c-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ed53c-126">Mapitags.h</span></span>
  
> <span data-ttu-id="ed53c-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ed53c-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ed53c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed53c-128">See also</span></span>



[<span data-ttu-id="ed53c-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed53c-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ed53c-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ed53c-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ed53c-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="ed53c-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ed53c-132">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="ed53c-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

