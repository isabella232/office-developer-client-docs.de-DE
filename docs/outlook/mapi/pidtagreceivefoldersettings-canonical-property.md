---
title: Kanonische Pidtagreceivefoldersettings (-Eigenschaft
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415054"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="6ea99-103">Kanonische Pidtagreceivefoldersettings (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6ea99-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="6ea99-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ea99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ea99-105">Enthält eine Tabelle der Einstellungen für den Empfangsordner eines Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="6ea99-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6ea99-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="6ea99-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6ea99-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="6ea99-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="6ea99-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="6ea99-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6ea99-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="6ea99-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="6ea99-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="6ea99-110">Data type:</span></span>  <br/> |<span data-ttu-id="6ea99-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="6ea99-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="6ea99-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="6ea99-112">Area:</span></span>  <br/> |<span data-ttu-id="6ea99-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="6ea99-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ea99-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ea99-114">Remarks</span></span>

<span data-ttu-id="6ea99-115">Diese Eigenschaft kann in [IMAPIProp:: CopyTo](imapiprop-copyto.md) -Vorgängen oder in [IMAPIProp:: CopyProps](imapiprop-copyprops.md) -Vorgängen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="6ea99-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="6ea99-116">Als Eigenschaft vom Typ PT_OBJECT kann Sie nicht erfolgreich von der [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode abgerufen werden; auf den Inhalt sollte von der [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode zugegriffen werden, um die Schnittstelle mit dem Bezeichner IID_IMAPITable anzufordern.</span><span class="sxs-lookup"><span data-stu-id="6ea99-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="6ea99-117">Dienstanbieter müssen Sie an die [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode melden, wenn Sie festgelegt ist, aber optional melden können, wenn Sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6ea99-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="6ea99-118">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6ea99-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="6ea99-119">Weitere Informationen finden Sie unter [Receive Folder Tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6ea99-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="6ea99-120">Diese Eigenschaft enthält eine Tabelle mit Zuordnungen der Empfangsordner für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="6ea99-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="6ea99-121">Das \*\*\*\* Aufrufen von OpenProperty für diese Eigenschaft entspricht dem Aufrufen von **GetReceiveFolderTable** im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="6ea99-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6ea99-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6ea99-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6ea99-123">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="6ea99-123">Header files</span></span>

<span data-ttu-id="6ea99-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="6ea99-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="6ea99-125">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="6ea99-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="6ea99-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="6ea99-126">Mapitags.h</span></span>
  
> <span data-ttu-id="6ea99-127">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="6ea99-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ea99-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ea99-128">See also</span></span>



[<span data-ttu-id="6ea99-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ea99-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6ea99-130">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6ea99-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6ea99-131">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="6ea99-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6ea99-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="6ea99-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

