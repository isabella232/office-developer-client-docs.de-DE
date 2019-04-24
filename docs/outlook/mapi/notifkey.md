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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280047"
---
# <a name="notifkey"></a><span data-ttu-id="7c037-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="7c037-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="7c037-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c037-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c037-105">Identifiziert eindeutig eine Verbindung zwischen einer Advise-Senke, einer Advise-Quelle und MAPI.</span><span class="sxs-lookup"><span data-stu-id="7c037-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7c037-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7c037-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c037-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="7c037-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="7c037-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="7c037-108">Members</span></span>

 <span data-ttu-id="7c037-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="7c037-109">**cb**</span></span>
  
> <span data-ttu-id="7c037-110">Die Anzahl der Bytes im **ab** -Element.</span><span class="sxs-lookup"><span data-stu-id="7c037-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="7c037-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="7c037-111">**ab**</span></span>
  
> <span data-ttu-id="7c037-112">Bytearray, das den Benachrichtigungs Schlüssel beschreibt.</span><span class="sxs-lookup"><span data-stu-id="7c037-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c037-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c037-113">Remarks</span></span>

<span data-ttu-id="7c037-114">Die [subscribe](imapisupport-subscribe.md) -und [Notify](imapisupport-notify.md) -Methoden von [IMAPISupport](imapisupportiunknown.md) verwenden die **NOTIFKEY** -Struktur, um Benachrichtigungen für die entsprechende Advise-Quelle zu generieren.</span><span class="sxs-lookup"><span data-stu-id="7c037-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="7c037-115">Dienstanbieter generieren Benachrichtigungs Schlüssel, wenn Ihre **Advise** -Methode aufgerufen wird, und Sie möchten **abonnieren** aufrufen, um die Benachrichtigungs Registrierung und das anschließende Senden von Benachrichtigungen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="7c037-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="7c037-116">Ein Benachrichtigungs Schlüssel kann die Eintrags-ID der Advise-Quelle oder ein beliebiges anderes identifizierendes Element wie eine Konstante sein.</span><span class="sxs-lookup"><span data-stu-id="7c037-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="7c037-117">Beispielsweise kann ein Nachrichtenspeicher Anbieter den Pfad eines Ordners als Benachrichtigungs Schlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="7c037-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="7c037-118">Der Benachrichtigungs Schlüssel sollte über mehrere Prozesse hinweg funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7c037-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="7c037-119">Die Bereichsanforderungen für einen Benachrichtigungs Schlüssel ähneln denen für eine langfristige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="7c037-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="7c037-120">Anders als bei einer Eintrags-ID muss ein Benachrichtigungs Schlüssel jedoch Binär-vergleichbar sein.</span><span class="sxs-lookup"><span data-stu-id="7c037-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="7c037-121">In der Regel enthält ein Benachrichtigungs Schlüssel einen vom Dienstanbieter definierten **GUID** -Wert, gefolgt von anderen anbieterspezifischen Informationen, die für das Objekt eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="7c037-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="7c037-122">Eine Erläuterung der Verwendung der **NOTIFKEY** -Struktur zum Verwalten der Verbindungen zwischen den Advise-Senken und den Objekten, die die Benachrichtigungen generieren, finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="7c037-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c037-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c037-123">See also</span></span>



[<span data-ttu-id="7c037-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="7c037-124">MAPI Structures</span></span>](mapi-structures.md)

