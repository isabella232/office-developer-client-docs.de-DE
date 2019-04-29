---
title: Schreiben eines automatisierten Clients
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b8f9ac1a-b377-4f83-8fb6-ed85ab9053d0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: f9ce3452bbc2d3297cc67168835a9387235746a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439765"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="93577-103">Schreiben eines automatisierten Clients</span><span class="sxs-lookup"><span data-stu-id="93577-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="93577-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93577-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93577-105">Eine automatisierte Clientanwendung ist eine unbeaufsichtigte Anwendung, die keine Benutzeroberfläche anzeigt.</span><span class="sxs-lookup"><span data-stu-id="93577-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="93577-106">Standardmäßig zeigen viele MAPI-Schnittstellenmethoden eine Benutzeroberfläche an.</span><span class="sxs-lookup"><span data-stu-id="93577-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="93577-107">Alle diese Methoden verfügen über Flags, mit denen ein Client diese Anzeige zulassen oder unterdrücken kann.</span><span class="sxs-lookup"><span data-stu-id="93577-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="93577-108">Obwohl MAPI davon ausgeht, dass Dienstanbieter diese Flags honorieren, gibt es einige Anbieter, die diese Erwartungen nicht immer erfüllen.</span><span class="sxs-lookup"><span data-stu-id="93577-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="93577-109">Ein legitimer Grund für die Nichtanerkennung der Flags ist die Abhängigkeit des Dienstanbieters in einem anderen Dienst, der die Unterdrückung der Benutzeroberfläche nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="93577-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="93577-110">Wenn Sie einen automatisierten Client entwickeln, achten Sie sorgfältig auf die von Ihnen verwendeten Dienstanbieter und deren Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="93577-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="93577-111">Gehen Sie nicht davon aus, dass alle Aufrufe zum unterdrücken einer Benutzeroberfläche erfolgreich ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="93577-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="93577-112">Automatisierte Clients müssen über die erforderlichen Informationen für die ordnungsgemäße Konfiguration der einzelnen Nachrichtendienste im Profil verfügen.</span><span class="sxs-lookup"><span data-stu-id="93577-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="93577-113">Es gibt zwei Möglichkeiten, Konfigurationsinformationen zur Anmeldezeit bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="93577-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="93577-114">Der Dienstanbieter kann Informationen aus dem Profil abrufen.</span><span class="sxs-lookup"><span data-stu-id="93577-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="93577-115">Der Dienstanbieter kann den Benutzer auffordern, Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="93577-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="93577-116">Da die zweite Option für automatisierte Clients nicht verfügbar ist, müssen diese Clients die erste Option verwenden.</span><span class="sxs-lookup"><span data-stu-id="93577-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="93577-117">Clients müssen ihre Profile sorgfältig konfigurieren, um sicherzustellen, dass diese Option immer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="93577-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="93577-118">Automatisierte Clients legen immer das MAPI_NO_MAIL-Flag im [MAPILogonEx](mapilogonex.md) -Funktionsaufruf fest, um eine MAPI-Sitzung zu starten.</span><span class="sxs-lookup"><span data-stu-id="93577-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

