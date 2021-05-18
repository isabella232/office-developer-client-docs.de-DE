---
title: Aktualisieren von MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: faafde3d-3989-4182-91f1-a0cf0f1b5388
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6c2c733b87b85971fad8060040e713b41b0f5616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407522"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="53931-103">Aktualisieren von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="53931-103">Updating MAPI properties</span></span>

<span data-ttu-id="53931-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53931-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53931-105">Clients und Dienstanbieter können einen Eigenschaftswert aktualisieren, indem sie:</span><span class="sxs-lookup"><span data-stu-id="53931-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="53931-106">Die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) eines Objekts, um den Wert einer oder mehreren Eigenschaften eines Objekts zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="53931-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="53931-107">Die [HrSetOneProp-Funktion,](hrsetoneprop.md) um immer nur eine Eigenschaft zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="53931-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="53931-108">Verwenden **Sie HrSetOneProp nur,** wenn das Zielobjekt lokal ist. Diese Funktion kann bei Verwendung mit Remoteobjekten zu Leistungsbeeinträchtigungen führen.</span><span class="sxs-lookup"><span data-stu-id="53931-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="53931-109">Das folgende Verfahren veranschaulicht, wie **Sie SetProps** verwenden, um die Nachrichtenklasse oder PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) -Eigenschaft einer Nachricht zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="53931-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="53931-110">So aktualisieren Sie die Nachrichtenklasse einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="53931-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="53931-111">Ordnen Sie [eine SPropValue-Struktur](spropvalue.md) für die Nachrichtenklasse zu, und legen Sie ihre Member entsprechend.</span><span class="sxs-lookup"><span data-stu-id="53931-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="53931-112">Rufen Sie die **IMAPIProp::SetProps-Methode** der Nachricht auf, um die neue Nachrichtenklasse zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="53931-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="53931-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53931-113">See also</span></span>

- [<span data-ttu-id="53931-114">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="53931-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

