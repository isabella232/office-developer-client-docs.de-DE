---
title: Stornieren einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409762"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="95349-103">Stornieren einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="95349-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="95349-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95349-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95349-105">Um eine Benachrichtigung abzubrechen, rufen die Clients eine **Unadvise** -Methode der Advise-Quelle auf.</span><span class="sxs-lookup"><span data-stu-id="95349-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="95349-106">Das \*\*\*\* Aufrufen von Unadvise ist wichtig, da der Dienstanbieter den Verweis auf Ihre Advise-Senke freigibt.</span><span class="sxs-lookup"><span data-stu-id="95349-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="95349-107">Solange ein Dienstanbieter einen Verweis auf eine Advise-Senke beibehält, kann die Advise-Senke weiterhin [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Anrufe empfangen.</span><span class="sxs-lookup"><span data-stu-id="95349-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="95349-108">Aufgrund der asynchronen Art der Ereignisbenachrichtigung können Clients sogar nach einem erfolgreichen Unadvise-Aufruf benachrichtigt werden \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="95349-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="95349-109">Clients müssen den Empfang von Benachrichtigungen jederzeit verarbeiten können.</span><span class="sxs-lookup"><span data-stu-id="95349-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="95349-110">Da sich die Implementierung von Dienstanbietern unterscheidet, \*\*\*\* können Clients, die nicht Unadvise aufrufen, eine Benachrichtigung abzubrechen, nicht davon ausgehen, wann ein Anbieter ihren Verweis auf die Advise-Senke freigibt.</span><span class="sxs-lookup"><span data-stu-id="95349-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="95349-111">Einige Dienstanbieter veröffentlichen ihre Verweise auf Advise-Senken, wenn Sie Ihre Advise-Quellen freigeben.</span><span class="sxs-lookup"><span data-stu-id="95349-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="95349-112">Einige Dienstanbieter nicht.</span><span class="sxs-lookup"><span data-stu-id="95349-112">Some service providers do not.</span></span> <span data-ttu-id="95349-113">Solange ein Dienstanbieter einen Verweis auf eine Advise-Senke beibehält, kann diese Advise-Senke weiterhin Benachrichtigungen erhalten.</span><span class="sxs-lookup"><span data-stu-id="95349-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

