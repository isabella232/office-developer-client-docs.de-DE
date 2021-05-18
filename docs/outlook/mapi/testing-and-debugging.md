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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316484"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="76c41-103">Testen und Debuggen</span><span class="sxs-lookup"><span data-stu-id="76c41-103">Testing and Debugging</span></span>

  
  
<span data-ttu-id="76c41-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76c41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76c41-105">Die Teststrategien unterscheiden sich je nachdem, ob Sie einen Client oder Dienstanbieter entwickeln.</span><span class="sxs-lookup"><span data-stu-id="76c41-105">Testing strategies differ depending on whether you are developing a client or service provider.</span></span> <span data-ttu-id="76c41-106">Da für eine Clientanwendung mindestens ein Dienstanbieter ausgeführt werden muss, sollten Clients in einer Umgebung mit unterschiedlichen Sätzen von Dienstanbietern getestet werden.</span><span class="sxs-lookup"><span data-stu-id="76c41-106">Because a client application requires one or more service providers to operate, clients should be tested in an environment with different sets of service providers.</span></span>
  
<span data-ttu-id="76c41-107">Dienstanbieter sollten jedoch isoliert getestet werden, bevor sie in andere Anbieter integriert werden.</span><span class="sxs-lookup"><span data-stu-id="76c41-107">Service providers, however, should be tested in isolation before being integrated with other providers.</span></span> <span data-ttu-id="76c41-108">MAPI stellt Tools bereit, die die Features eines Dienstanbieters eines bestimmten Typs testen sollen.</span><span class="sxs-lookup"><span data-stu-id="76c41-108">MAPI provides tools that are meant to test the features of a service provider of a particular type.</span></span> <span data-ttu-id="76c41-109">Die [MFCMAPI-Beispielanwendung](https://go.microsoft.com/fwlink/?LinkId=124154) zeigt, wie Sie die Features eines Adressbuchanbieters testen und mit einem Nachrichtenspeicheranbieter zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="76c41-109">The [MFCMAPI](https://go.microsoft.com/fwlink/?LinkId=124154) sample application shows how to test the features of an address book provider and works with a message store provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="76c41-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76c41-110">See also</span></span>



[<span data-ttu-id="76c41-111">Übersicht über die MAPI-Programmierung</span><span class="sxs-lookup"><span data-stu-id="76c41-111">MAPI Programming Overview</span></span>](mapi-programming-overview.md)
  
[<span data-ttu-id="76c41-112">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="76c41-112">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

