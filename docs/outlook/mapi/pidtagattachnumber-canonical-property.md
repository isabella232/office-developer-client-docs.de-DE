---
title: Kanonische Pidtagattachnumber (-Eigenschaft
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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327251"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="8b206-103">Kanonische Pidtagattachnumber (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8b206-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="8b206-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b206-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b206-105">Enthält eine Zahl, die die Anlage in der übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8b206-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b206-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="8b206-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8b206-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="8b206-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="8b206-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="8b206-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8b206-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="8b206-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="8b206-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="8b206-110">Data type:</span></span>  <br/> |<span data-ttu-id="8b206-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="8b206-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="8b206-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="8b206-112">Area:</span></span>  <br/> |<span data-ttu-id="8b206-113">Nachrichtenanlage</span><span class="sxs-lookup"><span data-stu-id="8b206-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b206-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b206-114">Remarks</span></span>

<span data-ttu-id="8b206-115">Nachrichtenspeicher generieren und verwalten diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="8b206-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="8b206-116">Die Anlagennummer ist der sekundäre Sortierschlüssel nach der Wiedergabeposition in der Anlage Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8b206-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="8b206-117">**PR_ATTACH_NUM** wird zum Öffnen der Anlage mit der [IMessage:: openattach](imessage-openattach.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b206-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="8b206-118">Innerhalb einer Client Anwendungssitzung bleibt die **PR_ATTACH_NUM** -Eigenschaft einer Nachrichtenanlage konstant, solange die Anlage Tabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="8b206-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="8b206-119">Der Nachrichtenspeicher propagiert Änderungen an der Tabelle mithilfe der Methoden **IMessage:: createattach** und **IMessage::D eleteattach** .</span><span class="sxs-lookup"><span data-stu-id="8b206-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="8b206-120">Nach seiner Option kann der nachrichtenspeichertabellen Benachrichtigungen für offene Anlagen Tabellen generieren, sodass Clients erneut eine Synchronisierung mit diesen Änderungen ausführen können.</span><span class="sxs-lookup"><span data-stu-id="8b206-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8b206-121">Zugehörige Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8b206-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8b206-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="8b206-122">Protocol specifications</span></span>

<span data-ttu-id="8b206-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8b206-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8b206-124">Verarbeitet Nachrichten-und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="8b206-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8b206-125">Header Dateien</span><span class="sxs-lookup"><span data-stu-id="8b206-125">Header files</span></span>

<span data-ttu-id="8b206-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="8b206-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="8b206-127">Stellt Datentypdefinitionen bereit.</span><span class="sxs-lookup"><span data-stu-id="8b206-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="8b206-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="8b206-128">Mapitags.h</span></span>
  
> <span data-ttu-id="8b206-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="8b206-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8b206-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b206-130">See also</span></span>



[<span data-ttu-id="8b206-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b206-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8b206-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8b206-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8b206-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="8b206-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8b206-134">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="8b206-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

