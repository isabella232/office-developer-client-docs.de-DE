---
title: NOTIFKEY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFKEY
api_type:
- COM
ms.assetid: 031b7e18-59b2-445c-a747-348fda92f458
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 36b8381e2bf98f5ddcb88a54b56f2b5c91b3b668
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572599"
---
# <a name="notifkey"></a><span data-ttu-id="36742-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="36742-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="36742-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36742-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36742-105">Identifiziert eindeutig eine Verbindung zwischen einer Advise-Empfänger, eine Advise-Quelle und MAPI.</span><span class="sxs-lookup"><span data-stu-id="36742-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36742-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="36742-106">Header file:</span></span>  <br/> |<span data-ttu-id="36742-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="36742-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="36742-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="36742-108">Members</span></span>

 <span data-ttu-id="36742-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="36742-109">**cb**</span></span>
  
> <span data-ttu-id="36742-110">Die Anzahl von Bytes in das Element **Ab** .</span><span class="sxs-lookup"><span data-stu-id="36742-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="36742-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="36742-111">**ab**</span></span>
  
> <span data-ttu-id="36742-112">Array von Bytes, beschreibt die Benachrichtigung-Taste.</span><span class="sxs-lookup"><span data-stu-id="36742-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36742-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="36742-113">Remarks</span></span>

<span data-ttu-id="36742-114">Die Methoden [Abonnieren](imapisupport-subscribe.md) und [Benachrichtigen](imapisupport-notify.md) der [IMAPISupport](imapisupportiunknown.md) verwenden Sie die Struktur **NOTIFKEY** zum Generieren von Benachrichtigungen an den entsprechenden Advise-Empfänger über die entsprechenden Advise-Quelle.</span><span class="sxs-lookup"><span data-stu-id="36742-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="36742-115">Dienstanbieter generieren Benachrichtigung Schlüssel, wenn ihre **Advise** -Methode aufgerufen wird und sie **Abonnieren** , um die benachrichtigungsregistrierung und das nachfolgende Senden von Benachrichtigungen zu behandeln anrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="36742-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="36742-116">Eine Taste Benachrichtigung kann die Eintrags-ID der Advise-Quelle oder andere identifizierende Elemente wie etwa eine Konstante sein.</span><span class="sxs-lookup"><span data-stu-id="36742-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="36742-117">Beispielsweise kann Anbieter eine Nachricht den Pfad eines Ordners als dessen Benachrichtigung Schlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="36742-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="36742-118">Der Schlüssel Benachrichtigung sollte für mehrere Prozesse funktionieren.</span><span class="sxs-lookup"><span data-stu-id="36742-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="36742-119">Die bereichsanforderungen für eine Benachrichtigung Schlüssel ähneln jenen für langfristige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="36742-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="36742-120">Im Gegensatz zu einer Eintrags-ID, muss eine Benachrichtigung Taste jedoch binär-vergleichbar sein.</span><span class="sxs-lookup"><span data-stu-id="36742-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="36742-121">In der Regel enthält ein Benachrichtigung Schlüssel einen **GUID** -Wert, der vom Dienstanbieter gefolgt von anderen eindeutigen anbieterspezifische Informationen auf das Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="36742-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="36742-122">Eine Erläuterung der Verwendung der Struktur **NOTIFKEY** zum Verwalten von Verbindungen zwischen der Advise-senken und die Objekte, die die Benachrichtigungen generieren finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="36742-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36742-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36742-123">See also</span></span>



[<span data-ttu-id="36742-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="36742-124">MAPI Structures</span></span>](mapi-structures.md)

