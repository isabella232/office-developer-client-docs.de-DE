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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404295"
---
# <a name="designing-a-message-service"></a><span data-ttu-id="39efe-103">Entwerfen eines Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="39efe-103">Designing a message service</span></span>

<span data-ttu-id="39efe-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39efe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39efe-105">Bevor Sie mit dem Schreiben von Code zur Unterstützung Ihres Nachrichtendiensts beginnen, ist es wichtig, einen Entwurf zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="39efe-105">Before you begin to write code to support your message service, it is important to create a design.</span></span> <span data-ttu-id="39efe-106">Beheben Sie die folgenden Probleme in Ihrem Entwurfsprozess:</span><span class="sxs-lookup"><span data-stu-id="39efe-106">Resolve the following issues in your design process:</span></span>
  
1. <span data-ttu-id="39efe-107">Bestimmen Sie, wie viele Dienstanbieter in den Nachrichtendienst einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="39efe-107">Determine how many service providers should be included in the message service.</span></span> <span data-ttu-id="39efe-108">Schließen Sie nur verwandte Dienstanbieter (d. h. Anbieter, die mit demselben Messagingsystem arbeiten) in Ihren Dienst ein.</span><span class="sxs-lookup"><span data-stu-id="39efe-108">Include only related service providers (that is, providers that work with the same messaging system) in your service.</span></span> <span data-ttu-id="39efe-109">Nicht verwandte Dienstanbieter gehören nicht zum gleichen Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="39efe-109">Unrelated service providers do not belong in the same message service.</span></span> <span data-ttu-id="39efe-110">Verwenden Sie das Profil zum Integrieren nicht verwandter Dienstanbieter und Nachrichtendienste.</span><span class="sxs-lookup"><span data-stu-id="39efe-110">Use the profile for integrating unrelated service providers and message services.</span></span>
    
2. <span data-ttu-id="39efe-111">Bestimmen Sie, welcher Typ von Dienstanbietern in den Nachrichtendienst einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="39efe-111">Determine what type of service providers should be included in the message service.</span></span> <span data-ttu-id="39efe-112">Die meisten Messgedienste enthalten einen Anbieter für jeden der gängigen Typen.</span><span class="sxs-lookup"><span data-stu-id="39efe-112">Most messge services include one provider of each of the common types.</span></span> <span data-ttu-id="39efe-113">Das heißt, der typische Nachrichtendienst verfügt über einen Adressbuchanbieter, einen Nachrichtenspeicheranbieter und einen Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="39efe-113">That is, the typical message service has one address book provider, one message store provider, and one transport provider.</span></span>
    
3. <span data-ttu-id="39efe-114">Bestimmen Sie, wie viele DLLs den Nachrichtendienst enthalten sollen.</span><span class="sxs-lookup"><span data-stu-id="39efe-114">Determine how many DLLs should contain the message service.</span></span> <span data-ttu-id="39efe-115">Die Anzahl der dlLs, die ein Nachrichtendienst verwendet, hängt von folgenden Kriterien ab:</span><span class="sxs-lookup"><span data-stu-id="39efe-115">The number of DLLs that a message service uses depends on the following:</span></span>
    
   - <span data-ttu-id="39efe-116">Der Komplexitätsgrad, den Sie als Verfasser des Nachrichtendiensts verarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="39efe-116">The degree of complexity that you as the writer of the message service are willing to handle.</span></span>
    
   - <span data-ttu-id="39efe-117">Der Typ der Dienstanbieter im Nachrichtendienst.</span><span class="sxs-lookup"><span data-stu-id="39efe-117">The type of service providers in the message service.</span></span>
    
   - <span data-ttu-id="39efe-118">Die Beziehung, die der Nachrichtendienst möglicherweise mit einem anderen Nachrichtendienst hat.</span><span class="sxs-lookup"><span data-stu-id="39efe-118">The relationship that the message service might have with another message service.</span></span>
    
   <span data-ttu-id="39efe-119">Da MAPI nur einen Einstiegspunkt für jeden Anbietertyp speichert, schließen Sie nicht mehrere Anbieter desselben Typs in eine einzelne DLL ein.</span><span class="sxs-lookup"><span data-stu-id="39efe-119">Because MAPI stores only one entry point for each provider type, do not include multiple providers of the same type in a single DLL.</span></span> <span data-ttu-id="39efe-120">Wenn es sinnvoll ist, mehrere Anbieter eines Typs zu verwenden, implementieren Sie sie entweder in separaten DLLs, oder lassen Sie sie eine Einstiegspunktfunktion gemeinsam nutzen.</span><span class="sxs-lookup"><span data-stu-id="39efe-120">If it makes sense to include multiple providers of one type, either implement them in separate DLLs or have them share an entry point function.</span></span> <span data-ttu-id="39efe-121">Eine weitere Option besteht in der Implementierung verwandter Nachrichtendienste oder Nachrichtendienste, die denselben Installations- und Konfigurationscode und dieselbe DLL-Einstiegspunktfunktion in einer DLL verwenden können.</span><span class="sxs-lookup"><span data-stu-id="39efe-121">Another option is to implement related message services, or message services that are able to use the same installation and configuration code and the same DLL entry point function, in one DLL.</span></span>
    
   <span data-ttu-id="39efe-122">Halten Sie es möglichst einfach, und verwenden Sie eine DLL, die die Implementierung aller Dienstanbieter im Nachrichtendienst und den ganzen Code zum Installieren und Konfigurieren des Nachrichtendiensts enthält.</span><span class="sxs-lookup"><span data-stu-id="39efe-122">If possible, keep it simple and use one DLL that contains the implementation of all the service providers in the message service and all the code to install and configure the message service.</span></span> <span data-ttu-id="39efe-123">Wenn dies nicht möglich ist, können Sie eine DLL für den Installations- und Konfigurationscode und entweder eine einzelne DLL für alle Dienstanbieter oder eine DLL für jeden Anbieter implementieren.</span><span class="sxs-lookup"><span data-stu-id="39efe-123">If this is not possible, you can implement one DLL for the installation and configuration code and either a single DLL for all of the service providers or one DLL for each provider.</span></span>
    
4. <span data-ttu-id="39efe-124">Bestimmen Sie einen Namen für die Nachrichtendienst-DLL oder DLLs.</span><span class="sxs-lookup"><span data-stu-id="39efe-124">Determine a name for the message service DLL or DLLs.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="39efe-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39efe-125">See also</span></span>

- [<span data-ttu-id="39efe-126">Implementierung des Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="39efe-126">Message Service Implementation</span></span>](message-service-implementation.md)

