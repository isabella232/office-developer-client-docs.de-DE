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
ms.openlocfilehash: 5cff3a6cbf4bfca7b414f9663e71834da71926d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795785"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="1029a-103">Aktualisieren von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1029a-103">Updating MAPI properties</span></span>

<span data-ttu-id="1029a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1029a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1029a-105">Clients und Dienstanbieter können durch Aufrufen ein Eigenschaftswerts aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="1029a-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="1029a-106">Ein Objekt [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode zum Aktualisieren des Werts, der eine oder mehrere der Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="1029a-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="1029a-107">Die [HrSetOneProp](hrsetoneprop.md) -Funktion, die nur eine Eigenschaft gleichzeitig zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1029a-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="1029a-108">Verwenden Sie **HrSetOneProp** , nur, wenn das Zielobjekt lokalen ist. Diese Funktion kann zu Leistungseinbußen bei der remote-Objekte mit führen.</span><span class="sxs-lookup"><span data-stu-id="1029a-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="1029a-109">Das folgende Verfahren veranschaulicht, wie **SetProps** verwenden, um die Nachrichtenklasse, oder die Eigenschaft PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) einer Nachricht zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1029a-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="1029a-110">So aktualisieren Sie die Nachrichtenklasse einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="1029a-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="1029a-111">Reservieren Sie eine [SPropValue](spropvalue.md) -Struktur für die Nachrichtenklasse und festlegen Sie seine Member entsprechend.</span><span class="sxs-lookup"><span data-stu-id="1029a-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="1029a-112">Rufen Sie die Nachricht **IMAPIProp::SetProps** -Methode, um die neue Nachrichtenklasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1029a-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="1029a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1029a-113">See also</span></span>

- [<span data-ttu-id="1029a-114">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1029a-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

