---
title: Implementierung des Nachrichtendiensts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434032"
---
# <a name="message-service-implementation"></a><span data-ttu-id="86685-103">Implementierung des Nachrichtendiensts</span><span class="sxs-lookup"><span data-stu-id="86685-103">Message Service Implementation</span></span>

  
  
<span data-ttu-id="86685-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86685-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86685-105">Bei einem Nachrichtendienst handelt es sich um einen oder mehrere verwandte Dienstanbieter, die zum Zweck der Vereinfachung der Installation und Konfiguration zusammen gruppieren.</span><span class="sxs-lookup"><span data-stu-id="86685-105">A message service is one or more related service providers grouped together for the purpose of simplifying installation and configuration.</span></span> <span data-ttu-id="86685-106">Alle Dienstanbieter sollten in einen Nachrichtendienst einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="86685-106">All service providers should be included in a message service.</span></span>
  
<span data-ttu-id="86685-107">Verwenden Sie das folgende Verfahren, um einen Nachrichtendienst mit einem oder mehreren Anbietern zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="86685-107">To implement a message service with one or more providers, use the following procedure:</span></span>
  
1. <span data-ttu-id="86685-108">Entwerfen Sie den Nachrichtendienst, und bestimmen Sie die Anzahl und den Typ der Dienstanbieter, die einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="86685-108">Design the message service, determining the number and type of service providers to be included.</span></span> <span data-ttu-id="86685-109">Weitere Informationen zum Entwerfen eines Nachrichtendiensts finden Sie unter [Designing a Message Service](designing-a-message-service.md).</span><span class="sxs-lookup"><span data-stu-id="86685-109">For more information about how to design a message service, see [Designing a Message Service](designing-a-message-service.md).</span></span>
    
2. <span data-ttu-id="86685-110">Erstellen Sie ein Setupprogramm, um die Dienstanbieter im Nachrichtendienst zu installieren.</span><span class="sxs-lookup"><span data-stu-id="86685-110">Create a setup program to install the service providers in the message service.</span></span> <span data-ttu-id="86685-111">Weitere Informationen zum Schreiben eines Nachrichtendienst-Setupprogramms finden Sie unter [Supporting Message Service Installation](supporting-message-service-installation.md).</span><span class="sxs-lookup"><span data-stu-id="86685-111">For more information about writing a message service setup program, see [Supporting Message Service Installation](supporting-message-service-installation.md).</span></span> 
    
3. <span data-ttu-id="86685-112">Erstellen Sie eine Einstiegspunktfunktion zum Ausführen der Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="86685-112">Create an entry point function to perform configuration.</span></span> <span data-ttu-id="86685-113">Weitere Informationen zum Schreiben einer Nachrichtendienst-Einstiegspunktfunktion finden Sie unter [Supporting Message Service Configuration](supporting-message-service-configuration.md) und [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="86685-113">For more information about writing a message service entry point function, see [Supporting Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY](msgserviceentry.md).</span></span> 
    
4. <span data-ttu-id="86685-114">Erstellen Sie eine öffentliche Headerdatei, die die Eigenschaftstags und Beschreibungen gültiger Werte für alle benutzerdefinierten Eigenschaften enthält, die vom Nachrichtendienst unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="86685-114">Create a public header file that contains the property tags and descriptions of valid values for any custom properties that the message service supports.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="86685-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86685-115">See also</span></span>



[<span data-ttu-id="86685-116">MAPI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="86685-116">MAPI Service Providers</span></span>](mapi-service-providers.md)

