---
title: PidTagAttachNumber (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327251"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="cefe8-103">PidTagAttachNumber (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="cefe8-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="cefe8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cefe8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cefe8-105">Enthält eine Zahl, die die Anlage innerhalb der übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cefe8-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cefe8-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="cefe8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cefe8-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="cefe8-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="cefe8-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="cefe8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cefe8-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="cefe8-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="cefe8-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="cefe8-110">Data type:</span></span>  <br/> |<span data-ttu-id="cefe8-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="cefe8-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="cefe8-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="cefe8-112">Area:</span></span>  <br/> |<span data-ttu-id="cefe8-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="cefe8-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cefe8-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cefe8-114">Remarks</span></span>

<span data-ttu-id="cefe8-115">Nachrichtenspeicher generieren und verwalten diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cefe8-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="cefe8-116">Die Anlagennummer ist der sekundäre Sortierschlüssel nach der Renderingposition in der Anlagentabelle.</span><span class="sxs-lookup"><span data-stu-id="cefe8-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="cefe8-117">**PR_ATTACH_NUM** wird verwendet, um die Anlage mit der [IMessage::OpenAttach-Methode zu](imessage-openattach.md) öffnen.</span><span class="sxs-lookup"><span data-stu-id="cefe8-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="cefe8-118">Innerhalb der Sitzung einer Clientanwendung bleibt **die PR_ATTACH_NUM** einer Nachrichtenanlage konstant, solange die Anlagentabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="cefe8-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="cefe8-119">Der Nachrichtenspeicher gibt Änderungen an der Tabelle mithilfe der **Methoden IMessage::CreateAttach** und **IMessage::D eleteAttach** weiter.</span><span class="sxs-lookup"><span data-stu-id="cefe8-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="cefe8-120">Bei dieser Option kann der Nachrichtenspeicher Tabellenbenachrichtigungen in geöffneten Anlagentabellen generieren, sodass Clients diese Änderungen erneut synchronisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="cefe8-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="cefe8-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cefe8-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cefe8-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="cefe8-122">Protocol specifications</span></span>

<span data-ttu-id="cefe8-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cefe8-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cefe8-124">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="cefe8-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cefe8-125">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="cefe8-125">Header files</span></span>

<span data-ttu-id="cefe8-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cefe8-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="cefe8-127">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="cefe8-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="cefe8-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="cefe8-128">Mapitags.h</span></span>
  
> <span data-ttu-id="cefe8-129">Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="cefe8-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cefe8-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cefe8-130">See also</span></span>



[<span data-ttu-id="cefe8-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cefe8-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cefe8-132">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="cefe8-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cefe8-133">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="cefe8-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cefe8-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="cefe8-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

