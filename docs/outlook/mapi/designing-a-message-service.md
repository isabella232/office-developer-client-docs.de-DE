---
title: Entwerfen einer Messagingdiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 04aa4348560396c8237811252fd96a2b461cd791
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791522"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="8258e-103">Entwerfen einer Messagingdiensts</span><span class="sxs-lookup"><span data-stu-id="8258e-103">Designing a message service</span></span>

<span data-ttu-id="8258e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8258e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8258e-105">Bevor Sie beginnen, dem Schreiben von Code, um Ihre Nachrichtendienst zu unterstützen, ist es wichtig, einen Entwurf erstellen.</span><span class="sxs-lookup"><span data-stu-id="8258e-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="8258e-106">Beheben Sie die folgenden Probleme in Ihrer Entwurfsprozess:</span><span class="sxs-lookup"><span data-stu-id="8258e-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="8258e-107">Bestimmen Sie, wie viele Dienstanbieter in der Nachrichtendienst enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8258e-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="8258e-108">Enthalten Sie nur verwandte-Dienstanbieter (d. h., Providers, mit denen die selben Nachrichtensystem zusammenarbeiten) in Ihrem Dienst.</span><span class="sxs-lookup"><span data-stu-id="8258e-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="8258e-109">Damit nicht zusammenhängenden-Dienstanbietern gehören nicht in der gleichen Message-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8258e-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="8258e-110">Verwenden Sie das Profil für die Integration von unabhängigen Dienstanbietern und Message-Dienste.</span><span class="sxs-lookup"><span data-stu-id="8258e-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="8258e-111">Bestimmen Sie, welche Art von Dienstanbietern in den Dienst enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="8258e-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="8258e-112">Die meisten Messge Dienste enthalten einen Anbieter der einzelnen die Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="8258e-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="8258e-113">D. h., hat der normalen Messagingdiensts eine Adressbuchanbieter, eine Nachricht Speicheranbieter und eine Adressbuchhierarchie.</span><span class="sxs-lookup"><span data-stu-id="8258e-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="8258e-114">Bestimmen, wie viele DLLs sollte die Messagingdiensts enthalten.</span><span class="sxs-lookup"><span data-stu-id="8258e-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="8258e-115">Die Anzahl von DLLs, die ein Nachrichtendienst verwendet hängt von folgendem ab:</span><span class="sxs-lookup"><span data-stu-id="8258e-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="8258e-116">Der Grad der Komplexität, die Sie als Writer des Diensts Nachricht bereit sind, zu behandeln sind.</span><span class="sxs-lookup"><span data-stu-id="8258e-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="8258e-117">Der Typ der Dienstanbieter in der Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="8258e-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="8258e-118">Die Beziehung, die der Dienst möglicherweise mit einem anderen Messagingdiensts muss.</span><span class="sxs-lookup"><span data-stu-id="8258e-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="8258e-119">Da MAPI nur über einen Einstiegspunkt für jeden Anbietertyp speichert, nehmen Sie mehrere Anbieter des gleichen Typs nicht in einer einzigen DLL.</span><span class="sxs-lookup"><span data-stu-id="8258e-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="8258e-120">Wenn es sinnvoll, mehrere Anbieter eines Typs enthalten ist, in separaten DLLs zu implementieren, oder haben sie eine Eintrag Funktion freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8258e-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="8258e-121">Eine andere Option besteht darin, implementieren Sie verwandte Message Dienste oder Message-Dienste, die die gleiche Installation verwenden können, und Konfigurationscode und Seitenverweisen auf dieselbe DLL zeigen-Funktion in einer DLL.</span><span class="sxs-lookup"><span data-stu-id="8258e-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="8258e-122">Wenn möglich, ganz einfach, und verwenden Sie eine DLL, die die Implementierung der der Dienstanbieter in der Nachrichtendienst und der gesamte Code zum Installieren und Konfigurieren des Diensts Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="8258e-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="8258e-123">Wenn dies nicht möglich ist, können Sie eine DLL für die Installation und Konfiguration von Code und entweder eine einzelne DLL für alle-Dienstanbieter oder eine DLL für jeden Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8258e-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="8258e-124">Bestimmen Sie einen Namen für den Dienst DLL oder DLLs.</span><span class="sxs-lookup"><span data-stu-id="8258e-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8258e-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8258e-125">See also</span></span>

- [<span data-ttu-id="8258e-126">Nachrichtendienstimplementierung</span><span class="sxs-lookup"><span data-stu-id="8258e-126">Message Service Implementation</span></span>](message-service-implementation.md)

