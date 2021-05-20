---
title: OBJEKTE des MAPI-Transportanbieters
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430357"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="860bf-103">OBJEKTE des MAPI-Transportanbieters</span><span class="sxs-lookup"><span data-stu-id="860bf-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="860bf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="860bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="860bf-105">Zusätzlich zu den von allen Dienstanbietern implementierten Standardanbieter- und Anmeldeobjekten müssen Transportanbieter ein Statusobjekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="860bf-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="860bf-106">Für die anderen Dienstanbietertypen ist die Implementierung eines Statusobjekts optional.</span><span class="sxs-lookup"><span data-stu-id="860bf-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="860bf-107">MapI erfordert dies jedoch für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="860bf-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="860bf-108">Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="860bf-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="860bf-109">Die folgende Abbildung zeigt jedes der Objekte, die Transportanbieter mit ihren entsprechenden Schnittstellen implementieren können.</span><span class="sxs-lookup"><span data-stu-id="860bf-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="860bf-110">Die Abbildung gibt außerdem an, ob MAPI oder ein Client der Benutzer des Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="860bf-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="860bf-111">![Objekte, die Transportanbieter implementieren Objekte,](media/amapi_66.gif "die von Transportanbietern implementiert werden")</span><span class="sxs-lookup"><span data-stu-id="860bf-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="860bf-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="860bf-112">See also</span></span>

- [<span data-ttu-id="860bf-113">OBJEKTE des MAPI-Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="860bf-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

