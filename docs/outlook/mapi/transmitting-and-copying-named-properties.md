---
title: Übertragen und Kopieren von benannten Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1c225712e354d72b79313ee4c3f36da55f11b0a3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587516"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="3b19a-103">Übertragen und Kopieren von benannten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b19a-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="3b19a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3b19a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3b19a-105">Wenn eine benannte Eigenschaft gesendet wird, verschoben oder kopiert haben, der Namen bleibt konstant, aber der Bezeichner muss ändern, um die Zuordnung der Zielobjekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3b19a-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="3b19a-106">Die einzige Ausnahme zu dieser Regel ist, wenn die Quell- und die gleiche Zuordnung Signatur haben Neuzuordnen unnötige vornehmen.</span><span class="sxs-lookup"><span data-stu-id="3b19a-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="3b19a-107">Es ist der Verantwortung der Adressbuchhierarchie, die Namen der übertragenen benannten Eigenschaften auf die entsprechende Bezeichner neu zuzuordnen, die an das Ziel arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3b19a-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="3b19a-108">Der sendenden Adressbuchhierarchie kann nicht wissen, was die korrekte Zuordnung am Ziel ist; Es muss die Namen übermitteln und hängen von der empfangenden Adressbuchhierarchie zu Bezeichner zuordnen, die funktionieren.</span><span class="sxs-lookup"><span data-stu-id="3b19a-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="3b19a-109">Die MAPI-Implementierung von TNEF verarbeitet Neuzuordnen des benannten Eigenschaften für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="3b19a-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="3b19a-110">Transportanbieter können entweder behandeln Neuzuordnen manuell oder verwenden Sie die TNEF-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="3b19a-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="3b19a-111">Eine ähnliche Neuzuordnen des benannten Eigenschaften muss auftreten, wenn diese Eigenschaften zwischen Nachrichtenspeicher kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b19a-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="3b19a-112">Da Nachricht-Anbieter den Namen Bezeichner-Zuordnung, der das Ziel abrufen können, können sie jedoch dann sofort neu zuordnen die Eigenschaften und nicht auf dem Ziel-Nachrichtenspeicher verlassen haben.</span><span class="sxs-lookup"><span data-stu-id="3b19a-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3b19a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b19a-113">See also</span></span>



[<span data-ttu-id="3b19a-114">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="3b19a-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

