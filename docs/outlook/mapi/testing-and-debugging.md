---
title: Testen und Debuggen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0afceb1f-9086-4cc9-8ce4-fb9256a81a9c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96bc2e58482ba259b14e820f3380978f80c542c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795713"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="d12be-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="d12be-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="d12be-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d12be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d12be-105">Teststrategien unterscheiden sich je nachdem, ob Sie einen Client oder Dienstanbieter entwickeln.</span><span class="sxs-lookup"><span data-stu-id="d12be-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="d12be-106">Da eine Clientanwendung eine oder mehrere Dienstanbieter Betrieb erforderlich sind, sollten Clients in einer Umgebung mit unterschiedlichen Dienstanbieter getestet werden.</span><span class="sxs-lookup"><span data-stu-id="d12be-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="d12be-107">Dienstanbieter, sollten jedoch vor der Integration mit anderen Anbietern isoliert getestet werden.</span><span class="sxs-lookup"><span data-stu-id="d12be-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="d12be-108">MAPI bietet Tools, die zum Testen der Features von einem Dienstanbieter eines bestimmten Typs vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="d12be-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="d12be-109">Die beispielanwendung [MFCMAPI (engl.)](http://go.microsoft.com/fwlink/?LinkId=124154) zeigt, wie die Features des Adressbuch-Dienstanbieter testen und Speicheranbieter Works mit einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d12be-109">The [MFCMAPI](http://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d12be-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d12be-110">See also</span></span>



[<span data-ttu-id="d12be-111">�bersicht �ber die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="d12be-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="d12be-112">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d12be-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

