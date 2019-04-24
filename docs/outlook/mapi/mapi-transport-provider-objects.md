---
title: MAPI-Transportanbieter Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3f05e5b4b45e18d580737d37250e183c4cead881
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357376"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="4e5ef-103">MAPI-Transportanbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="4e5ef-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="4e5ef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e5ef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e5ef-105">Zusätzlich zu den Standardanbieter-und anmeldeobjekten, die von allen Dienstanbietern implementiert werden, müssen Transportanbieter ein Status-Objekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="4e5ef-106">Für die anderen Dienstanbieter Typen ist die Implementierung eines Status-Objekts optional.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="4e5ef-107">MAPI ist jedoch für Transportanbieter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="4e5ef-108">Transport Anbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="4e5ef-109">In der folgenden Abbildung sind alle Objekte dargestellt, die Transportanbieter mit den entsprechenden Schnittstellen implementieren können.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="4e5ef-110">Die Abbildung gibt auch an, ob MAPI oder ein Client der Benutzer des Objekts ist.</span><span class="sxs-lookup"><span data-stu-id="4e5ef-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="4e5ef-111">Von ![Transportanbietern implementierte Objekte] Von (media/amapi_66.gif "Transportanbietern implementierte Objekte")</span><span class="sxs-lookup"><span data-stu-id="4e5ef-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4e5ef-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e5ef-112">See also</span></span>

- [<span data-ttu-id="4e5ef-113">MAPI-Dienstanbieter Objekte</span><span class="sxs-lookup"><span data-stu-id="4e5ef-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

