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
ms.openlocfilehash: e5357c1e822dda35d3f38e00f91b58adbaf0ff9d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795848"
---
# <a name="writing-an-automated-client"></a><span data-ttu-id="a0b21-103">Schreiben eines automatisierten Clients</span><span class="sxs-lookup"><span data-stu-id="a0b21-103">Writing an Automated Client</span></span>

  
  
<span data-ttu-id="a0b21-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0b21-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0b21-105">Eine automatisierte Client-Anwendung ist eine Anwendung, die unbeaufsichtigte, ohne Benutzeroberfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0b21-105">An automated client application is an application that runs unattended, displaying no user interface.</span></span>
  
 <span data-ttu-id="a0b21-106">Standardmäßig an vielen MAPI-Schnittstellenmethoden eine Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="a0b21-106">By default, many MAPI interface methods show a user interface.</span></span> <span data-ttu-id="a0b21-107">Alle diese Methoden haben Flags, die einen Client zulassen oder unterdrückt diese Anzeige zulassen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-107">All of these methods have flags that allow a client to either allow or suppress this display.</span></span> <span data-ttu-id="a0b21-108">Obwohl MAPI-Dienstanbieter diese Flags berücksichtigt erwartet, sind einige Anbieter, die diese Erwartungen nicht immer entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-108">Although MAPI expects service providers to honor these flags, there are some providers that do not always meet these expectations.</span></span> <span data-ttu-id="a0b21-109">Ein legitimer Grund nicht berücksichtigt die Kennzeichen ist die Abhängigkeit des Dienstanbieters einer anderen Dienst, der keine Benutzer Schnittstelle Unterdrückung zulässt.</span><span class="sxs-lookup"><span data-stu-id="a0b21-109">A legitimate reason for not honoring the flags is the reliance of the service provider on another service that does not allow user interface suppression.</span></span> <span data-ttu-id="a0b21-110">Wenn Sie einen automatisierten Client entwickeln, achten Sie darauf achten auf der Dienstanbieter, die Sie verwenden und wie diese konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="a0b21-110">If you are developing an automated client, pay careful attention to the service providers you are using and how they are configured.</span></span> <span data-ttu-id="a0b21-111">Gehen Sie nicht, dass alle Ihre Anrufe an eine Benutzeroberfläche unterdrücken hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="a0b21-111">Do not assume that all of your calls to suppress a user interface will be successful.</span></span> 
  
<span data-ttu-id="a0b21-112">Automatisierte Clients benötigen in das Profil die erforderliche Informationen für die ordnungsgemäße Konfiguration der einzelnen Message-Dienste zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a0b21-112">Automated clients must have the necessary information available for proper configuration of each of the message services in the profile.</span></span> <span data-ttu-id="a0b21-113">Es gibt zwei Methoden, um Konfigurationsinformationen bei der Anmeldung angeben:</span><span class="sxs-lookup"><span data-stu-id="a0b21-113">There are two ways to supply configuration information at logon time:</span></span>
  
- <span data-ttu-id="a0b21-114">Der Dienstanbieter kann Informationen aus dem Profil abrufen.</span><span class="sxs-lookup"><span data-stu-id="a0b21-114">The service provider can retrieve information from the profile.</span></span>
    
- <span data-ttu-id="a0b21-115">Der Dienstanbieter kann der Benutzer Informationen aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="a0b21-115">The service provider can prompt the user for information.</span></span> 
    
<span data-ttu-id="a0b21-116">Da die zweite Option für automatisierte Clients als nicht verfügbar ist, müssen diese Clients die erste Option verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0b21-116">Since the second option is unavailable to automated clients, these clients must use the first option.</span></span> <span data-ttu-id="a0b21-117">Clients müssen ihre Profile sorgfältig durch, um sicherzustellen, dass diese Option immer konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a0b21-117">Clients must configure their profiles carefully to ensure that this option always works.</span></span>
  
<span data-ttu-id="a0b21-118">Automatisierte Clients legen Sie das MAPI_NO_MAIL-Flag immer im Funktionsaufruf [MAPILogonEx](mapilogonex.md) um einen MAPI-Sitzung zu starten.</span><span class="sxs-lookup"><span data-stu-id="a0b21-118">Automated clients always set the MAPI_NO_MAIL flag in the [MAPILogonEx](mapilogonex.md) function call to begin a MAPI session.</span></span> 
  

