---
title: MAPI-Transport-Anbieter-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d7311857ff54ef253fd00634671f4a510443f19
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793099"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="59419-103">MAPI-Transport-Anbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="59419-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="59419-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="59419-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="59419-105">Zusätzlich zu den standardmäßigen Provider und Logon-Objekten, die von allen Dienstanbietern implementiert werden Transportanbieter erforderlich, um einem Statusobjekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="59419-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="59419-106">Implementieren ein Statusobjekt ist für die anderen Anbieter Diensttypen optional.</span><span class="sxs-lookup"><span data-stu-id="59419-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="59419-107">Muss allerdings MAPI für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="59419-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="59419-108">Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="59419-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="59419-109">Die folgende Abbildung zeigt alle Objekte, die Transportanbieter mit ihren entsprechenden Schnittstellen implementieren können.</span><span class="sxs-lookup"><span data-stu-id="59419-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="59419-110">Die Abbildung wird angegeben, ob MAPI oder ein Client das Objekt-Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="59419-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="59419-111">![Objekte, mit denen Transportanbieter implementiert] (media/amapi_66.gif "Objekte, mit denen Transportanbieter implementiert")</span><span class="sxs-lookup"><span data-stu-id="59419-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="59419-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59419-112">See also</span></span>

- [<span data-ttu-id="59419-113">MAPI-Dienstanbieterobjekten</span><span class="sxs-lookup"><span data-stu-id="59419-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

