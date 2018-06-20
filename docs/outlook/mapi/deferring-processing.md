---
title: Verzögert die Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8f26fc6a51c3abdb4d4d009183fa8263ce97b261
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791504"
---
# <a name="deferring-processing"></a><span data-ttu-id="df778-103">Verzögert die Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="df778-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="df778-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="df778-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="df778-105">Übergeben Sie das MAPI_DEFERRED_ERRORS-Flag für die Methode anrufen so weit wie möglich.</span><span class="sxs-lookup"><span data-stu-id="df778-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="df778-106">Viele der MAPI-Methodenaufrufe wurden optimiert Annahme dieses Flag, verursacht des Anbieters, das die angeforderte Aufgabe entweder zu verschieben, bis mehrere Aufgaben gleichzeitig ausgeführt werden können oder nicht mehr für die Ergebnisse warten können.</span><span class="sxs-lookup"><span data-stu-id="df778-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="df778-107">Angenommen, wenn Sie [IMsgStore::OpenEntry](imsgstore-openentry.md) , einen Ordner öffnen MAPI_DEFERRED_ERRORS übergeben, kann das Öffnen des Ordners und einen möglichen Remoteaufruf verschoben werden, bis Sie einen weiteren Anruf wie einen Anruf an des Ordners **GetHierarchyTable** oder **vornehmen GetProps** Methoden.</span><span class="sxs-lookup"><span data-stu-id="df778-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="df778-108">**GetHierarchyTable** und **GetProps** erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="df778-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="df778-109">Eine andere Möglichkeit, Verarbeitung zurückstellen ist einfach nicht um einen Anruf zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="df778-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="df778-110">Bewusst des Benutzers und der Benutzer eine Belastung Ressourcen oder Verarbeitungszeit erkennen kann, können Sie ermitteln, wenn es sinnvoll, Anrufe tätigen.</span><span class="sxs-lookup"><span data-stu-id="df778-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="df778-111">Möglichkeit zur Verbesserung der Leistung durch Aufrufe entweder jeweils Wenn der Benutzer nicht bemerken oder durch nicht in allen besteht.</span><span class="sxs-lookup"><span data-stu-id="df778-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="df778-112">Betrachten Sie beispielsweise die Situation, wenn Sie mehr als eine Benachrichtigung pro Sekunde von einem Nachrichtenspeicher erhalten, die eine große Anzahl von Nachrichten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="df778-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="df778-113">Eine Statusanzeige wird angezeigt, um den Prozentsatz der Abschluss des Vorgangs angeben.</span><span class="sxs-lookup"><span data-stu-id="df778-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="df778-114">Benutzer werden in der Regel nicht schätzen diesen Vorgang, um langsame werden erst nach einige Sekunden vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="df778-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="df778-115">Aus diesem Grund, wenn Sie die Statusanzeige aktualisieren, führen Sie nehmen Sie keine Änderungen erst nach dem Initiieren des Verschiebevorgangs mindestens vier Sekunden.</span><span class="sxs-lookup"><span data-stu-id="df778-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="df778-116">Dadurch wird im Allgemeinen Zeit sparen, wenn der Vorgang fast ist und Benutzer in kurzer Zeit zu informieren, wenn der Vorgang langsam ist.</span><span class="sxs-lookup"><span data-stu-id="df778-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

