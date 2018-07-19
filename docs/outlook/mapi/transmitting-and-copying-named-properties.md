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
ms.openlocfilehash: a5d2244270463fcc2fe0a9786112590e741a8a66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795748"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="55aca-103">Übertragen und Kopieren von benannten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="55aca-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="55aca-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="55aca-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="55aca-105">Wenn eine benannte Eigenschaft gesendet wird, verschoben oder kopiert haben, der Namen bleibt konstant, aber der Bezeichner muss ändern, um die Zuordnung der Zielobjekt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="55aca-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="55aca-106">Die einzige Ausnahme zu dieser Regel ist, wenn die Quell- und die gleiche Zuordnung Signatur haben Neuzuordnen unnötige vornehmen.</span><span class="sxs-lookup"><span data-stu-id="55aca-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="55aca-107">Es ist der Verantwortung der Adressbuchhierarchie, die Namen der übertragenen benannten Eigenschaften auf die entsprechende Bezeichner neu zuzuordnen, die an das Ziel arbeiten.</span><span class="sxs-lookup"><span data-stu-id="55aca-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="55aca-108">Der sendenden Adressbuchhierarchie kann nicht wissen, was die korrekte Zuordnung am Ziel ist; Es muss die Namen übermitteln und hängen von der empfangenden Adressbuchhierarchie zu Bezeichner zuordnen, die funktionieren.</span><span class="sxs-lookup"><span data-stu-id="55aca-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="55aca-109">Die MAPI-Implementierung von TNEF verarbeitet Neuzuordnen des benannten Eigenschaften für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="55aca-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="55aca-110">Transportanbieter können entweder behandeln Neuzuordnen manuell oder verwenden Sie die TNEF-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="55aca-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="55aca-111">Eine ähnliche Neuzuordnen des benannten Eigenschaften muss auftreten, wenn diese Eigenschaften zwischen Nachrichtenspeicher kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="55aca-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="55aca-112">Da Nachricht-Anbieter den Namen Bezeichner-Zuordnung, der das Ziel abrufen können, können sie jedoch dann sofort neu zuordnen die Eigenschaften und nicht auf dem Ziel-Nachrichtenspeicher verlassen haben.</span><span class="sxs-lookup"><span data-stu-id="55aca-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55aca-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55aca-113">See also</span></span>



[<span data-ttu-id="55aca-114">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="55aca-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

