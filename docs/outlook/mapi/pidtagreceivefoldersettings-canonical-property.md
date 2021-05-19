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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415054"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a><span data-ttu-id="8b0e0-103">PidTagReceiveFolderSettings (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="8b0e0-103">PidTagReceiveFolderSettings Canonical Property</span></span>

  
  
<span data-ttu-id="8b0e0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b0e0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b0e0-105">Enthält eine Tabelle der Empfangsordnereinstellungen eines Nachrichtenspeichers.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-105">Contains a table of a message store's receive folder settings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b0e0-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8b0e0-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b0e0-107">PR_RECEIVE_FOLDER_SETTINGS</span><span class="sxs-lookup"><span data-stu-id="8b0e0-107">PR_RECEIVE_FOLDER_SETTINGS</span></span>  <br/> |
|<span data-ttu-id="8b0e0-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8b0e0-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b0e0-109">0x3415</span><span class="sxs-lookup"><span data-stu-id="8b0e0-109">0x3415</span></span>  <br/> |
|<span data-ttu-id="8b0e0-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8b0e0-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b0e0-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="8b0e0-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="8b0e0-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8b0e0-112">Area:</span></span>  <br/> |<span data-ttu-id="8b0e0-113">MAPI-Nachrichtenspeicher</span><span class="sxs-lookup"><span data-stu-id="8b0e0-113">MAPI message store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b0e0-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8b0e0-114">Remarks</span></span>

<span data-ttu-id="8b0e0-115">Diese Eigenschaft kann in [IMAPIProp::CopyTo-Vorgängen](imapiprop-copyto.md) ausgeschlossen oder in [IMAPIProp::CopyProps-Vorgängen enthalten](imapiprop-copyprops.md) sein.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="8b0e0-116">Als Eigenschaft vom Typ PT_OBJECT kann sie nicht erfolgreich von der [IMAPIProp::GetProps-Methode abgerufen](imapiprop-getprops.md) werden. Auf deren Inhalt sollte die [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) zugreifen und die Schnittstelle mit dem Bezeichner IID_IMAPITable.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method; its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the interface with identifier IID_IMAPITable.</span></span> <span data-ttu-id="8b0e0-117">Dienstanbieter müssen sie der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) melden, wenn sie festgelegt ist, können sie jedoch optional melden oder nicht, wenn sie nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-117">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but can optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="8b0e0-118">Zum Abrufen von Tabelleninhalten sollte eine Clientanwendung die [IMsgStore::GetReceiveFolderTable-Methode](imsgstore-getreceivefoldertable.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-118">To retrieve table contents, a client application should call the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> <span data-ttu-id="8b0e0-119">Weitere Informationen finden Sie unter [Receive Folder Tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8b0e0-119">For more information, see [Receive Folder Tables](receive-folder-tables.md).</span></span>
  
<span data-ttu-id="8b0e0-120">Diese Eigenschaft enthält eine Tabelle mit Zuordnungen der Empfangsordner für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-120">This property contains a table of mappings of the receive folders for the message store.</span></span> <span data-ttu-id="8b0e0-121">Das **Aufrufen von OpenProperty** für diese Eigenschaft entspricht dem Aufrufen **von GetReceiveFolderTable** im Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-121">Calling **OpenProperty** on this property is equivalent to calling **GetReceiveFolderTable** on the message store.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b0e0-122">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b0e0-122">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="8b0e0-123">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="8b0e0-123">Header files</span></span>

<span data-ttu-id="8b0e0-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8b0e0-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b0e0-125">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b0e0-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8b0e0-126">Mapitags.h</span></span>
  
> <span data-ttu-id="8b0e0-127">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8b0e0-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b0e0-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b0e0-128">See also</span></span>



[<span data-ttu-id="8b0e0-129">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b0e0-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b0e0-130">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="8b0e0-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b0e0-131">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8b0e0-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b0e0-132">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8b0e0-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

