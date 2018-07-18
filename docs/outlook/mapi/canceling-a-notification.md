---
title: Stornieren einer Benachrichtigung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791379"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="2e7e1-103">Stornieren einer Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2e7e1-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="2e7e1-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e7e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e7e1-105">Um eine Benachrichtigung zu löschen, rufen Clients einer Advise-Datenquelle **Unadvise** -Methode.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="2e7e1-106">Aufrufen von **Unadvise** ist wichtig, da dadurch den Dienstanbieter den Verweis auf die Advise-Empfänger freigeben.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="2e7e1-107">Als ein Dienstanbieter einen Verweis auf ein Advise-Empfänger verwaltet werden, kann der Advise-Empfänger weiterhin [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) Anrufe entgegennehmen.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="2e7e1-108">Aufgrund der asynchronen Art der Benachrichtigung, können sogar Clients benachrichtigt werden, auch nach einer erfolgreichen **Unadvise** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="2e7e1-109">Clients müssen, können Sie jederzeit den Empfang von Benachrichtigungen behandeln können.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="2e7e1-110">Da Service Provider Implementierungen unterscheiden, können nicht Clients, die nicht aufrufen **Unadvise** um eine Benachrichtigung abzubrechen nichts zu davon ausgehen bei der Freigabe eines Anbieters seinen Verweis auf ihre Advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="2e7e1-111">Einige Dienstanbieter freigeben ihre Verweise ausschließlich senken, wenn sie ihren Advise-Quellen freigeben zum.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="2e7e1-112">Einige Dienstanbieter nicht.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-112">Some service providers do not.</span></span> <span data-ttu-id="2e7e1-113">Als ein Dienstanbieter einen Verweis auf ein Advise-Empfänger verwaltet werden, kann diese Advise-Empfänger auch weiterhin zum Empfangen von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="2e7e1-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

