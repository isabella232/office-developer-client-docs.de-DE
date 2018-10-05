---
title: Testen und Debuggen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8e1f15ae354894aede4e8418e6428d0524ccb70d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383660"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="eedeb-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="eedeb-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="eedeb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eedeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eedeb-105">Teststrategien unterscheiden sich je nachdem, ob Sie einen Client oder Dienstanbieter entwickeln.</span><span class="sxs-lookup"><span data-stu-id="eedeb-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="eedeb-106">Da eine Clientanwendung eine oder mehrere Dienstanbieter Betrieb erforderlich sind, sollten Clients in einer Umgebung mit unterschiedlichen Dienstanbieter getestet werden.</span><span class="sxs-lookup"><span data-stu-id="eedeb-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="eedeb-107">Dienstanbieter, sollten jedoch vor der Integration mit anderen Anbietern isoliert getestet werden.</span><span class="sxs-lookup"><span data-stu-id="eedeb-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="eedeb-108">MAPI bietet Tools, die zum Testen der Features von einem Dienstanbieter eines bestimmten Typs vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="eedeb-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="eedeb-109">Die beispielanwendung [MFCMAPI (engl.)](https://go.microsoft.com/fwlink/?LinkId=124154) zeigt, wie die Features des Adressbuch-Dienstanbieter testen und Speicheranbieter Works mit einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="eedeb-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eedeb-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eedeb-110">See also</span></span>



[<span data-ttu-id="eedeb-111">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="eedeb-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="eedeb-112">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="eedeb-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

