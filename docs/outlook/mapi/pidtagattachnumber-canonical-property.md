---
title: Kanonische PidTagAttachNumber-Eigenschaft
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
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794111"
---
# <a name="pidtagattachnumber-canonical-property"></a><span data-ttu-id="2fb3b-103">Kanonische PidTagAttachNumber-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2fb3b-103">PidTagAttachNumber Canonical Property</span></span>

  
  
<span data-ttu-id="2fb3b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2fb3b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2fb3b-105">Enthält eine Zahl, die die Anlage innerhalb der übergeordneten Nachricht eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-105">Contains a number that uniquely identifies the attachment within its parent message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2fb3b-106">Zugeordneten Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="2fb3b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="2fb3b-107">PR_ATTACH_NUM</span><span class="sxs-lookup"><span data-stu-id="2fb3b-107">PR_ATTACH_NUM</span></span>  <br/> |
|<span data-ttu-id="2fb3b-108">Bezeichner:</span><span class="sxs-lookup"><span data-stu-id="2fb3b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="2fb3b-109">0x0E21</span><span class="sxs-lookup"><span data-stu-id="2fb3b-109">0x0E21</span></span>  <br/> |
|<span data-ttu-id="2fb3b-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="2fb3b-110">Data type:</span></span>  <br/> |<span data-ttu-id="2fb3b-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="2fb3b-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="2fb3b-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="2fb3b-112">Area:</span></span>  <br/> |<span data-ttu-id="2fb3b-113">E-Mail-Anlage</span><span class="sxs-lookup"><span data-stu-id="2fb3b-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fb3b-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2fb3b-114">Remarks</span></span>

<span data-ttu-id="2fb3b-115">Nachrichtenspeicher generieren und verwalten diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-115">Message stores generate and maintain this property.</span></span> <span data-ttu-id="2fb3b-116">Die Anzahl der Anlage ist die sekundäre Sortierschlüssel, nach dem Renderingposition in der Anlagentabelle.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-116">The attachment number is the secondary sort key, after the rendering position, in the attachment table.</span></span> 
  
 <span data-ttu-id="2fb3b-117">**PR_ATTACH_NUM** wird zum Öffnen der Anlage mit der [IMessage::OpenAttach](imessage-openattach.md) -Methode verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-117">**PR_ATTACH_NUM** is used to open the attachment with the [IMessage::OpenAttach](imessage-openattach.md) method.</span></span> <span data-ttu-id="2fb3b-118">Innerhalb einer Clientanwendung-Sitzung bleibt die **PR_ATTACH_NUM** -Eigenschaft des e-Mail-Anlagen konstant, wie die Anlagentabelle geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-118">Within a client application's session, the **PR_ATTACH_NUM** property of a message attachment remains constant as long as the attachment table is open.</span></span> 
  
<span data-ttu-id="2fb3b-119">Der Nachrichtenspeicher verteilt die Änderungen auf die Tabelle mit den Methoden **IMessage::CreateAttach** und **IMessage::DeleteAttach** .</span><span class="sxs-lookup"><span data-stu-id="2fb3b-119">The message store propagates changes to the table using the **IMessage::CreateAttach** and **IMessage::DeleteAttach** methods.</span></span> <span data-ttu-id="2fb3b-120">Ermessen kann der Nachrichtenspeicher Tabelle Benachrichtigungen auf Anlage öffnen Tabellen generieren, damit Clients auf diese Änderungen synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-120">At its option the message store can generate table notifications on open attachment tables so that clients can resynchronize to those changes.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="2fb3b-121">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2fb3b-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="2fb3b-122">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="2fb3b-122">Protocol specifications</span></span>

<span data-ttu-id="2fb3b-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="2fb3b-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="2fb3b-124">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="2fb3b-125">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="2fb3b-125">Header files</span></span>

<span data-ttu-id="2fb3b-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2fb3b-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="2fb3b-127">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="2fb3b-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="2fb3b-128">Mapitags.h</span></span>
  
> <span data-ttu-id="2fb3b-129">Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2fb3b-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2fb3b-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2fb3b-130">See also</span></span>



[<span data-ttu-id="2fb3b-131">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fb3b-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="2fb3b-132">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="2fb3b-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="2fb3b-133">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="2fb3b-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="2fb3b-134">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="2fb3b-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

