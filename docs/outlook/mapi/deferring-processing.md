---
title: Zurückstellen der Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336932"
---
# <a name="deferring-processing"></a><span data-ttu-id="e2b22-103">Zurückstellen der Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="e2b22-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="e2b22-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2b22-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2b22-105">Führen Sie das MAPI_DEFERRED_ERRORS-Flag so weit wie möglich an Methodenaufrufe weiter.</span><span class="sxs-lookup"><span data-stu-id="e2b22-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="e2b22-106">Viele der MAPI-Methodenaufrufe wurden so optimiert, dass diese Kennzeichnung akzeptiert wird, sodass der Anbieter die angeforderte Aufgabe entweder verschiebt, bis mehrere Aufgaben gleichzeitig ausgeführt werden können, oder Sie können nicht mehr auf die Ergebnisse warten.</span><span class="sxs-lookup"><span data-stu-id="e2b22-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="e2b22-107">Wenn Sie beispielsweise MAPI_DEFERRED_ERRORS an [IMsgStore:: OpenEntry](imsgstore-openentry.md) weitergeben, um einen Ordner zu öffnen, kann das Öffnen des Ordners und ein möglicher Remoteaufruf verschoben werden, bis Sie einen weiteren Aufruf ausführen, beispielsweise einen Aufruf an \*\*\*\* die GetHierarchy-Datei des Ordners oder \*\* \*\*GetProps-Methoden.</span><span class="sxs-lookup"><span data-stu-id="e2b22-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="e2b22-108">Sowohl \*\*\*\* gethierarchyable als auch GetProps erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e2b22-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="e2b22-109">Eine andere Möglichkeit, die Verarbeitung zu verzögern, besteht darin, keinen Anruf zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="e2b22-110">Wenn Sie den Benutzer erkennen und wenn der Benutzer die Ressourcen oder die Verarbeitungszeit ausleeren kann, können Sie bestimmen, wann es sinnvoll ist, Anrufe zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="e2b22-111">Es besteht die Möglichkeit, die Leistung zu verbessern, indem Sie Anrufe entweder zu einem Zeitpunkt durchführen, zu dem der Benutzer Sie nicht bemerkt oder überhaupt nicht vornimmt.</span><span class="sxs-lookup"><span data-stu-id="e2b22-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="e2b22-112">Betrachten Sie beispielsweise die Situation, wenn Sie mehr als eine Benachrichtigung pro Sekunde aus einem Nachrichtenspeicher erhalten, der eine große Anzahl von Nachrichten verschiebt.</span><span class="sxs-lookup"><span data-stu-id="e2b22-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="e2b22-113">Eine Statusanzeige wird angezeigt, um den Prozentsatz der Fertigstellung des Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e2b22-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="e2b22-114">Dieser Vorgang wird in der Regel erst nach einigen Sekunden verlangsamt.</span><span class="sxs-lookup"><span data-stu-id="e2b22-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="e2b22-115">Wenn Sie also die Statusanzeige aktualisieren, nehmen Sie keine Änderungen vor, bevor Sie mindestens vier Sekunden nach dem Initiieren des Verschiebevorgangs beginnen.</span><span class="sxs-lookup"><span data-stu-id="e2b22-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="e2b22-116">Dies spart Zeit in den häufig verwendeten Fällen, wenn der Vorgang schnell ausgeführt wird und die Benutzerrecht zeitig informiert werden, wenn der Vorgang langsam ist.</span><span class="sxs-lookup"><span data-stu-id="e2b22-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

