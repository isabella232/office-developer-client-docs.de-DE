---
title: Entwerfen eines Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 32627ebb-547f-4fac-a406-e7243ec5521b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 19a8a939685c440901f3f57d72baf673a579e590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316723"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="8002b-103">Entwerfen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="8002b-103">Designing a message service</span></span>

<span data-ttu-id="8002b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8002b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8002b-105">Bevor Sie mit dem Schreiben von Code beginnen, um den Nachrichtendienst zu unterstützen, ist es wichtig, einen Entwurf zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8002b-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="8002b-106">Beheben Sie die folgenden Probleme in Ihrem Entwurfsprozess:</span><span class="sxs-lookup"><span data-stu-id="8002b-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="8002b-107">Legen Sie fest, wie viele Dienstanbieter in den Nachrichtendienst aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8002b-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="8002b-108">Schließen Sie nur Verwandte Dienstanbieter (also Anbieter, die mit demselben Messagingsystem arbeiten) in ihren Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="8002b-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="8002b-109">Nicht verwandte Dienstanbieter gehören nicht in den gleichen Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="8002b-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="8002b-110">Verwenden Sie das Profil für die Integration nicht zusammenhängender Dienstanbieter und Nachrichtendienste.</span><span class="sxs-lookup"><span data-stu-id="8002b-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="8002b-111">Legen Sie fest, welche Art von Dienstanbietern in den Nachrichtendienst aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8002b-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="8002b-112">Die meisten Messge-Dienste verfügen über einen Anbieter der einzelnen allgemeinen Typen.</span><span class="sxs-lookup"><span data-stu-id="8002b-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="8002b-113">Das heißt, der typische Nachrichtendienst verfügt über einen Adressbuchanbieter, einen Nachrichtenspeicher Anbieter und einen Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="8002b-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="8002b-114">Bestimmen Sie, wie viele DLLs den Nachrichtendienst enthalten sollen.</span><span class="sxs-lookup"><span data-stu-id="8002b-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="8002b-115">Die Anzahl der DLLs, die ein Nachrichtendienst verwendet, hängt von den folgenden:</span><span class="sxs-lookup"><span data-stu-id="8002b-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="8002b-116">Der Grad an Komplexität, den Sie als Verfasser des Nachrichtendiensts bereit sind.</span><span class="sxs-lookup"><span data-stu-id="8002b-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="8002b-117">Der Typ der Dienstanbieter im Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="8002b-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="8002b-118">Die Beziehung, die der Nachrichtendienst möglicherweise mit einem anderen Nachrichtendienst hat.</span><span class="sxs-lookup"><span data-stu-id="8002b-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="8002b-119">Da MAPI nur einen Einstiegspunkt für jeden Anbietertyp speichert, dürfen Sie nicht mehrere Anbieter desselben Typs in eine einzelne DLL einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="8002b-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="8002b-120">Wenn es sinnvoll ist, mehrere Anbieter eines Typs einzuschließen, implementieren Sie Sie entweder in separaten DLLs, oder lassen Sie Sie eine Einstiegspunktfunktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="8002b-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="8002b-121">Eine weitere Option ist die Implementierung zugehöriger Nachrichtendienste oder Nachrichtendienste, die in der Lage sind, denselben Installations-und Konfigurationscode und dieselbe DLL-Einstiegspunktfunktion in einer DLL zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8002b-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="8002b-122">Wenn möglich, halten Sie es einfach, und verwenden Sie eine DLL, die die Implementierung aller Dienstanbieter im Nachrichtendienst und den gesamten Code zum Installieren und Konfigurieren des Nachrichtendiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="8002b-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="8002b-123">Wenn dies nicht möglich ist, können Sie eine DLL für den Installations-und Konfigurationscode und entweder eine einzelne DLL für alle Dienstanbieter oder eine DLL für jeden Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="8002b-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="8002b-124">Bestimmen Sie einen Namen für die Nachrichtendienst-DLL oder DLLs.</span><span class="sxs-lookup"><span data-stu-id="8002b-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8002b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8002b-125">See also</span></span>

- [<span data-ttu-id="8002b-126">Nachrichtendienst Implementierung</span><span class="sxs-lookup"><span data-stu-id="8002b-126">Message Service Implementation</span></span>](message-service-implementation.md)

