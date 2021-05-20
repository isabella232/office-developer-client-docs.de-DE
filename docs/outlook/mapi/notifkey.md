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
ms.openlocfilehash: ab1586696a4b72aa9e88545c2069c3f8b5d22d72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429628"
---
# <a name="notifkey"></a><span data-ttu-id="eba44-103">NOTIFKEY</span><span class="sxs-lookup"><span data-stu-id="eba44-103">NOTIFKEY</span></span>

  
  
<span data-ttu-id="eba44-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eba44-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eba44-105">Identifiziert eindeutig eine Verbindung zwischen einer Ratensenke, einer Ratenquelle und MAPI.</span><span class="sxs-lookup"><span data-stu-id="eba44-105">Uniquely identifies a connection between an advise sink, an advise source, and MAPI.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="eba44-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="eba44-106">Header file:</span></span>  <br/> |<span data-ttu-id="eba44-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="eba44-107">Mapispi.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE ab[MAPI_DIM];
} NOTIFKEY, FAR *LPNOTIFKEY;

```

## <a name="members"></a><span data-ttu-id="eba44-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="eba44-108">Members</span></span>

 <span data-ttu-id="eba44-109">**cb**</span><span class="sxs-lookup"><span data-stu-id="eba44-109">**cb**</span></span>
  
> <span data-ttu-id="eba44-110">Anzahl der Bytes im **ab-Element.**</span><span class="sxs-lookup"><span data-stu-id="eba44-110">Count of bytes in the **ab** member.</span></span> 
    
 <span data-ttu-id="eba44-111">**ab**</span><span class="sxs-lookup"><span data-stu-id="eba44-111">**ab**</span></span>
  
> <span data-ttu-id="eba44-112">Array von Bytes, die den Benachrichtigungsschlüssel beschreiben.</span><span class="sxs-lookup"><span data-stu-id="eba44-112">Array of bytes describing the notification key.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eba44-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="eba44-113">Remarks</span></span>

<span data-ttu-id="eba44-114">Die [Subscribe-](imapisupport-subscribe.md) und [Notify-Methoden](imapisupport-notify.md) von [IMAPISupport](imapisupportiunknown.md) verwenden die **NOTIFKEY-Struktur,** um Benachrichtigungen an die entsprechende Ratensenke über die entsprechende Informationsquelle zu generieren.</span><span class="sxs-lookup"><span data-stu-id="eba44-114">The [Subscribe](imapisupport-subscribe.md) and [Notify](imapisupport-notify.md) methods of [IMAPISupport](imapisupportiunknown.md) use the **NOTIFKEY** structure to generate notifications to the appropriate advise sink about the appropriate advise source.</span></span> 
  
<span data-ttu-id="eba44-115">Dienstanbieter generieren Benachrichtigungsschlüssel, wenn ihre **Advise-Methode** aufgerufen wird, und sie möchten **Subscribe** aufrufen, um die Benachrichtigungsregistrierung und das nachfolgende Senden von Benachrichtigungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="eba44-115">Service providers generate notification keys when their **Advise** method is called and they want to call **Subscribe** to handle the notification registration and the subsequent sending of notifications.</span></span> <span data-ttu-id="eba44-116">Ein Benachrichtigungsschlüssel kann der Eintragsbezeichner der Beratenden Quelle oder ein anderes identifizierendes Element wie eine Konstante sein.</span><span class="sxs-lookup"><span data-stu-id="eba44-116">A notification key can be the entry identifier of the advise source or it can be any other identifying item such as a constant.</span></span> <span data-ttu-id="eba44-117">Beispielsweise kann ein Nachrichtenspeicheranbieter den Pfad eines Ordners als Benachrichtigungsschlüssel verwenden.</span><span class="sxs-lookup"><span data-stu-id="eba44-117">For example, a message store provider might use the path of a folder as its notification key.</span></span> 
  
<span data-ttu-id="eba44-118">Der Benachrichtigungsschlüssel sollte über mehrere Prozesse hinweg funktionieren.</span><span class="sxs-lookup"><span data-stu-id="eba44-118">The notification key should work across multiple processes.</span></span> 
  
<span data-ttu-id="eba44-119">Die Bereichsanforderungen für einen Benachrichtigungsschlüssel ähneln denen für eine langfristige Eintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="eba44-119">The scope requirements for a notification key resemble those for a long-term entry identifier.</span></span> <span data-ttu-id="eba44-120">Im Gegensatz zu einem Eintragsbezeichner muss ein Benachrichtigungsschlüssel jedoch binär vergleichbar sein.</span><span class="sxs-lookup"><span data-stu-id="eba44-120">However, unlike an entry identifier, a notification key must be binary-comparable.</span></span> <span data-ttu-id="eba44-121">In der Regel enthält ein Benachrichtigungsschlüssel einen vom Dienstanbieter definierten **GUID-Wert,** gefolgt von anderen anbieterspezifischen Informationen, die für das Objekt eindeutig sind.</span><span class="sxs-lookup"><span data-stu-id="eba44-121">Typically, a notification key includes a **GUID** value defined by the service provider followed by other provider-specific information unique to the object.</span></span> 
  
<span data-ttu-id="eba44-122">Eine Diskussion über die Verwendung der **NOTIFKEY-Struktur** zum Verwalten der Verbindungen zwischen den Ratensenken und den Objekten, die die Benachrichtigungen generieren, finden Sie unter [Supporting Event Notification](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="eba44-122">For a discussion of the use of the **NOTIFKEY** structure to manage the connections between the advise sinks and the objects that generate the notifications, see [Supporting Event Notification](supporting-event-notification.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eba44-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eba44-123">See also</span></span>



[<span data-ttu-id="eba44-124">MAPI-Strukturen</span><span class="sxs-lookup"><span data-stu-id="eba44-124">MAPI Structures</span></span>](mapi-structures.md)

