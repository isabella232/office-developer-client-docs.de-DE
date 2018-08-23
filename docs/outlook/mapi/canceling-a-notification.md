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
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564773"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="0e509-103">Stornieren einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="0e509-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="0e509-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0e509-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0e509-105">Um eine Benachrichtigung zu löschen, rufen Clients einer Advise-Datenquelle **Unadvise** -Methode.</span><span class="sxs-lookup"><span data-stu-id="0e509-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="0e509-106">Aufrufen von **Unadvise** ist wichtig, da dadurch den Dienstanbieter den Verweis auf die Advise-Empfänger freigeben.</span><span class="sxs-lookup"><span data-stu-id="0e509-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="0e509-107">Als ein Dienstanbieter einen Verweis auf ein Advise-Empfänger verwaltet werden, kann der Advise-Empfänger weiterhin [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Anrufe entgegennehmen.</span><span class="sxs-lookup"><span data-stu-id="0e509-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="0e509-108">Aufgrund der asynchronen Art der Benachrichtigung, können sogar Clients benachrichtigt werden, auch nach einer erfolgreichen **Unadvise** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0e509-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="0e509-109">Clients müssen, können Sie jederzeit den Empfang von Benachrichtigungen behandeln können.</span><span class="sxs-lookup"><span data-stu-id="0e509-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="0e509-110">Da Service Provider Implementierungen unterscheiden, können nicht Clients, die nicht aufrufen **Unadvise** um eine Benachrichtigung abzubrechen nichts zu davon ausgehen bei der Freigabe eines Anbieters seinen Verweis auf ihre Advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="0e509-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="0e509-111">Einige Dienstanbieter freigeben ihre Verweise ausschließlich senken, wenn sie ihren Advise-Quellen freigeben zum.</span><span class="sxs-lookup"><span data-stu-id="0e509-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="0e509-112">Einige Dienstanbieter nicht.</span><span class="sxs-lookup"><span data-stu-id="0e509-112">Some service providers do not.</span></span> <span data-ttu-id="0e509-113">Als ein Dienstanbieter einen Verweis auf ein Advise-Empfänger verwaltet werden, kann diese Advise-Empfänger auch weiterhin zum Empfangen von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="0e509-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

