---
title: MAPI-Transport-Anbieter-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4f28fab8-2ce1-4398-a941-6d718c9bbd6a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: de0334ee9a90da38e472571314136195c84a7866
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592703"
---
# <a name="mapi-transport-provider-objects"></a><span data-ttu-id="ff6a3-103">MAPI-Transport-Anbieter-Objekte</span><span class="sxs-lookup"><span data-stu-id="ff6a3-103">MAPI transport provider objects</span></span>
  
<span data-ttu-id="ff6a3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff6a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff6a3-105">Zusätzlich zu den standardmäßigen Provider und Logon-Objekten, die von allen Dienstanbietern implementiert werden Transportanbieter erforderlich, um einem Statusobjekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ff6a3-105">In addition to the standard provider and logon objects implemented by all service providers, transport providers are required to implement a status object.</span></span> <span data-ttu-id="ff6a3-106">Implementieren ein Statusobjekt ist für die anderen Anbieter Diensttypen optional.</span><span class="sxs-lookup"><span data-stu-id="ff6a3-106">For the other service provider types, implementing a status object is optional.</span></span> <span data-ttu-id="ff6a3-107">Muss allerdings MAPI für Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="ff6a3-107">However, MAPI requires it for transport providers.</span></span> <span data-ttu-id="ff6a3-108">Transportanbieter, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver unterstützen, implementieren auch einen Ordner und eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ff6a3-108">Transport providers that support the downloading of message headers from a remote server also implement a folder and a table.</span></span> 
  
<span data-ttu-id="ff6a3-109">Die folgende Abbildung zeigt alle Objekte, die Transportanbieter mit ihren entsprechenden Schnittstellen implementieren können.</span><span class="sxs-lookup"><span data-stu-id="ff6a3-109">The following illustration shows each of the objects that transport providers can implement with their corresponding interfaces.</span></span> <span data-ttu-id="ff6a3-110">Die Abbildung wird angegeben, ob MAPI oder ein Client das Objekt-Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="ff6a3-110">The illustration also indicates whether MAPI or a client is the object's user.</span></span>
  
<span data-ttu-id="ff6a3-111">![Objekte, mit denen Transportanbieter implementiert] (media/amapi_66.gif "Objekte, mit denen Transportanbieter implementiert")</span><span class="sxs-lookup"><span data-stu-id="ff6a3-111">![Objects that transport providers implement](media/amapi_66.gif "Objects that transport providers implement")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ff6a3-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff6a3-112">See also</span></span>

- [<span data-ttu-id="ff6a3-113">MAPI-Dienstanbieterobjekten</span><span class="sxs-lookup"><span data-stu-id="ff6a3-113">MAPI Service Provider Objects</span></span>](mapi-service-provider-objects.md)

