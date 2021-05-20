---
title: Übertragen und Kopieren benannter Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 37075cfc-461d-4983-9045-d9f1da6739be
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6534e7344a62717e406c112249d26407b0852d93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437777"
---
# <a name="transmitting-and-copying-named-properties"></a><span data-ttu-id="92e20-103">Übertragen und Kopieren benannter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="92e20-103">Transmitting and Copying Named Properties</span></span>

  
  
<span data-ttu-id="92e20-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92e20-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92e20-105">Wenn eine benannte Eigenschaft gesendet, verschoben oder kopiert wird, bleibt der Name konstant, aber der Bezeichner muss geändert werden, um der Zuordnung des Zielobjekts zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="92e20-105">Whenever a named property is sent, moved, or copied, the name remains constant but the identifier must change to adhere to the mapping of the destination object.</span></span> <span data-ttu-id="92e20-106">Die einzige Ausnahme von dieser Regel ist, wenn Die Quelle und das Ziel dieselbe Zuordnungssignatur haben, wodurch die Neuzuordnung nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="92e20-106">The only exception to this rule is when the source and destination have the same mapping signature, making remapping unnecessary.</span></span>
  
<span data-ttu-id="92e20-107">Es liegt in der Verantwortung des Transportanbieters, die Namen der übertragenen benannten Eigenschaften den entsprechenden Bezeichnern neu zu karten, die am Ziel funktionieren.</span><span class="sxs-lookup"><span data-stu-id="92e20-107">It is the responsibility of the transport provider to remap the names of transmitted named properties to appropriate identifiers that work at the destination.</span></span> <span data-ttu-id="92e20-108">Der sendende Transportanbieter kann nicht wissen, was die richtige Zuordnung am Ziel ist. Sie muss die Namen übertragen und sich auf den empfangenden Transportanbieter verlassen, um sie den bezeichnern zu zuordnungen, die funktionieren.</span><span class="sxs-lookup"><span data-stu-id="92e20-108">The sending transport provider cannot know what the correct mapping is at the destination; it must transmit the names and rely on the receiving transport provider to map them to identifiers that work.</span></span> <span data-ttu-id="92e20-109">Die MAPI-Implementierung von TNEF behandelt die Neuzuordnung benannter Eigenschaften für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="92e20-109">The MAPI implementation of TNEF handles the remapping of named properties for transport providers.</span></span> <span data-ttu-id="92e20-110">Transportanbieter können die Neuanweisung entweder manuell verarbeiten oder die TNEF-Implementierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="92e20-110">Transport providers can either handle the remapping manually or use the TNEF implementation.</span></span> 
  
<span data-ttu-id="92e20-111">Eine ähnliche Neuappierung benannter Eigenschaften muss auftreten, wenn diese Eigenschaften zwischen Nachrichtenspeichern kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="92e20-111">A similar remapping of named properties must occur when these properties are copied between message stores.</span></span> <span data-ttu-id="92e20-112">Da Nachrichtenspeicheranbieter jedoch die Zuordnung des Namens zum Bezeichner des Ziels abrufen können, können sie die Eigenschaften sofort neu zuordnen und müssen sich nicht auf den Zielnachrichtenspeicher verlassen.</span><span class="sxs-lookup"><span data-stu-id="92e20-112">However, because message store providers can retrieve the name to identifier mapping of the destination, they can remap the properties right away and not have to rely on the destination message store.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92e20-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92e20-113">See also</span></span>



[<span data-ttu-id="92e20-114">Benannte Eigenschaften MAPI</span><span class="sxs-lookup"><span data-stu-id="92e20-114">MAPI Named Properties</span></span>](mapi-named-properties.md)

