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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360515"
---
# <a name="updating-mapi-properties"></a><span data-ttu-id="25318-103">Aktualisieren von MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="25318-103">Updating MAPI properties</span></span>

<span data-ttu-id="25318-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25318-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25318-105">Clients und Dienstanbieter können einen Eigenschaftswert aktualisieren, indem Sie Folgendes aufrufen:</span><span class="sxs-lookup"><span data-stu-id="25318-105">Clients and service providers can update a property value by calling:</span></span>
  
- <span data-ttu-id="25318-106">Die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode eines Objekts zum Aktualisieren des Werts einer oder mehrerer Eigenschaften eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="25318-106">An object's [IMAPIProp::SetProps](imapiprop-setprops.md) method to update the value of one or more of an object's properties.</span></span> 
    
- <span data-ttu-id="25318-107">Die [HrSetOneProp](hrsetoneprop.md) -Funktion, um nur jeweils eine Eigenschaft zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="25318-107">The [HrSetOneProp](hrsetoneprop.md) function to update only one property at a time.</span></span> <span data-ttu-id="25318-108">Verwenden Sie **HrSetOneProp** nur, wenn das Zielobjekt lokal ist; Diese Funktion kann bei Remoteobjekten zu Leistungseinbußen führen.</span><span class="sxs-lookup"><span data-stu-id="25318-108">Use **HrSetOneProp** only if the target object is local; this function can cause performance degradation when used with remote objects.</span></span> 
    
<span data-ttu-id="25318-109">Im folgenden Verfahren wird veranschaulicht, wie \*\*\*\* Sie mithilfe von SetProps die Nachrichtenklasse oder PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))-Eigenschaft einer Nachricht aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="25318-109">The following procedure illustrates how to use **SetProps** to update the message class, or PR_MESSAGE_CLASS_A ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) property, of a message.</span></span> 
  
### <a name="to-update-the-message-class-of-a-message"></a><span data-ttu-id="25318-110">So aktualisieren Sie die Nachrichtenklasse einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="25318-110">To update the message class of a message</span></span> 
  
1. <span data-ttu-id="25318-111">Ordnen Sie eine [SPropValue](spropvalue.md) -Struktur für die Nachrichtenklasse zu, und legen Sie Ihre Member entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="25318-111">Allocate an [SPropValue](spropvalue.md) structure for the message class and set its members as appropriate.</span></span> 
    
  ```cpp
    SPropValue spvMsgClass;
    spvMsgClass.ulPropTag = PR_MESSAGE_CLASS_A;
    spvMsgClass.Value.lpszA = "IPM.NewClass";
    
  ```

2. <span data-ttu-id="25318-112">Rufen Sie die **IMAPIProp::** SetProps-Methode der Nachricht auf, um die neue Nachrichtenklasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="25318-112">Call the message's **IMAPIProp::SetProps** method to set the new message class.</span></span> 
    
  ```cpp
    hRes = lpMessage->SetProps(1, (LPSPropValue) &spvMsgClass, NULL);
  ```

## <a name="see-also"></a><span data-ttu-id="25318-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25318-113">See also</span></span>

- [<span data-ttu-id="25318-114">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="25318-114">MAPI Property Overview</span></span>](mapi-property-overview.md)

