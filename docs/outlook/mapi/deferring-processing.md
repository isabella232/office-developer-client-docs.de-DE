---
title: Zurückdringen der Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a791b95f-56ad-493a-9ba5-fb4c7dd80e89
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2d3fbf8f7a725f121579066001715fb0bc6beba0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430931"
---
# <a name="deferring-processing"></a><span data-ttu-id="ad56e-103">Zurückdringen der Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="ad56e-103">Deferring Processing</span></span>

  
  
<span data-ttu-id="ad56e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad56e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad56e-105">Übergeben Sie MAPI_DEFERRED_ERRORS-Flag an Methodenaufrufe so weit wie möglich.</span><span class="sxs-lookup"><span data-stu-id="ad56e-105">Pass the MAPI_DEFERRED_ERRORS flag to method calls as much as possible.</span></span> <span data-ttu-id="ad56e-106">Viele aufrufe der MAPI-Methode wurden für die Annahme dieses Kennzeichens optimiert, sodass der Anbieter die angeforderte Aufgabe entweder verschieben kann, bis mehrere Aufgaben gleichzeitig ausgeführt werden können, oder Sie können nicht mehr auf die Ergebnisse warten.</span><span class="sxs-lookup"><span data-stu-id="ad56e-106">Many of the MAPI method calls have been optimized to accept this flag, causing the provider to either postpone the requested task until multiple tasks can be performed at once or you can wait no longer for the results.</span></span>
  
<span data-ttu-id="ad56e-107">Wenn Sie z. B. MAPI_DEFERRED_ERRORS an [IMsgStore::OpenEntry](imsgstore-openentry.md) übergeben, um einen Ordner zu öffnen, können das Öffnen des Ordners und ein möglicher Remoteaufruf verschoben werden, bis Sie einen weiteren Aufruf wie z. B. einen Aufruf der **GetHierarchyTable-** oder **GetProps-Methoden** des Ordners machen.</span><span class="sxs-lookup"><span data-stu-id="ad56e-107">For example, if you pass MAPI_DEFERRED_ERRORS to [IMsgStore::OpenEntry](imsgstore-openentry.md) to open a folder, the opening of the folder and a possible remote call can be postponed until you make another call such as a call to the folder's **GetHierarchyTable** or **GetProps** methods.</span></span> <span data-ttu-id="ad56e-108">Sowohl **GetHierarchyTable** als auch **GetProps** erfordern die Rückgabe von Daten vom Dienstanbieter, eine Aufgabe, die sofort ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ad56e-108">Both **GetHierarchyTable** and **GetProps** require the return of data from the service provider, a task that must be performed immediately.</span></span> 
  
<span data-ttu-id="ad56e-109">Eine weitere Möglichkeit zum Aufschub der Verarbeitung ist einfach, keinen Anruf zu machen.</span><span class="sxs-lookup"><span data-stu-id="ad56e-109">Another way to defer processing is simply not to make a call.</span></span> <span data-ttu-id="ad56e-110">Wenn Sie sich des Benutzers bewusst sind und wann der Benutzer ressourcen- oder verarbeitungszeitablaufend wahrgenommen werden kann, können Sie bestimmen, wann es sinnvoll ist, Anrufe zu machen.</span><span class="sxs-lookup"><span data-stu-id="ad56e-110">By being aware of the user and when the user can perceive a drain on resources or processing time, you can determine when it makes sense to make calls.</span></span> <span data-ttu-id="ad56e-111">Es besteht die Möglichkeit, die Leistung zu verbessern, indem Sie anrufe entweder zu einem Zeitpunkt, zu dem der Benutzer sie nicht bemerkt oder gar nicht macht.</span><span class="sxs-lookup"><span data-stu-id="ad56e-111">There is an opportunity to improve performance by making calls either at a time when the user will not notice or by not making them at all.</span></span>
  
<span data-ttu-id="ad56e-112">Berücksichtigen Sie beispielsweise die Situation, dass Sie mehr als eine Benachrichtigung pro Sekunde von einem Nachrichtenspeicher erhalten, der eine große Anzahl von Nachrichten bewegt.</span><span class="sxs-lookup"><span data-stu-id="ad56e-112">For example, consider the situation when you are receiving more than one notification per second from a message store that is moving a great number of messages.</span></span> <span data-ttu-id="ad56e-113">Es wird ein Fortschrittsindikator angezeigt, der den Prozentsatz des Abschlusses des Vorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="ad56e-113">A progress indicator is displayed to indicate the percentage of the operation's completion.</span></span> <span data-ttu-id="ad56e-114">Benutzer sehen diesen Vorgang in der Regel erst langsam, wenn einige Sekunden vergangen sind.</span><span class="sxs-lookup"><span data-stu-id="ad56e-114">Users typically will not perceive this operation to be slow until a few seconds have passed.</span></span> <span data-ttu-id="ad56e-115">Wenn Sie die Statusanzeige aktualisieren, nehmen Sie daher erst mindestens vier Sekunden nach Beginn des Verschiebens Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="ad56e-115">Therefore, if you are updating the progress indicator, do not make any changes until at least four seconds after the initiation of the move operation.</span></span> <span data-ttu-id="ad56e-116">Dies spart zeit in den häufigen Fällen, in denen der Vorgang schnell ist, und informiert benutzer zeitnah, wenn der Vorgang langsam ist.</span><span class="sxs-lookup"><span data-stu-id="ad56e-116">This will save time in the common cases when the operation is fast and inform users in a timely manner when the operation is slow.</span></span>
  

