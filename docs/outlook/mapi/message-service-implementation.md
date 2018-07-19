---
title: Nachrichtendienstimplementierung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ba2f9542fd021c544d73d8208ed356a7bf95309
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793258"
---
# <a name="message-service-implementation"></a><span data-ttu-id="1295e-103">Nachrichtendienstimplementierung</span><span class="sxs-lookup"><span data-stu-id="1295e-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="1295e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1295e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1295e-105">Ein Nachrichtendienst ist eine oder mehrere verwandte Dienstanbieter zur Vereinfachung der Installation und Konfiguration von gruppiert.</span><span class="sxs-lookup"><span data-stu-id="1295e-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="1295e-106">Alle-Dienstanbieter sollten in einem Nachrichtendienst enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="1295e-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="1295e-107">Um einen Nachrichtendienst mit einem oder mehreren Dienstanbietern implementieren möchten, verwenden Sie die folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1295e-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="1295e-108">Entwerfen Sie den Dienst, Bestimmen der Anzahl und Typ der Dienstanbieter eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="1295e-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="1295e-109">Weitere Informationen zum Entwerfen einer Messagingdiensts finden Sie unter [Entwerfen einer Messagingdiensts](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="1295e-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="1295e-110">Erstellen Sie ein Setup-Programm, die-Dienstanbieter in den Dienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="1295e-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="1295e-111">Weitere Informationen zum Schreiben einer Nachricht Service Setup-Programm finden Sie unter [Message Service-Installation unterstützt](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="1295e-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="1295e-112">Erstellen Sie eine Eintrag Point-Funktion zum Konfigurationsschritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="1295e-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="1295e-113">Weitere Informationen zum Schreiben eines Nachricht Diensteintrag Funktion finden Sie [Unterstützung Nachricht Dienstkonfiguration](supporting-message-service-configuration.md) und [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="1295e-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="1295e-114">Erstellen Sie eine öffentliche Headerdatei die Eigenschaftentags und enthält eine Beschreibung der gültigen Werte für alle benutzerdefinierten Eigenschaften, die der Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1295e-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="1295e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1295e-115">See also</span></span>



[<span data-ttu-id="1295e-116">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1295e-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

