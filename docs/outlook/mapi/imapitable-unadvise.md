---
title: IMAPITableUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Unadvise
api_type:
- COM
ms.assetid: 19f0dad9-9704-4bbe-a689-9531e7198351
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da11f15dfe9d269b79f465f01f713de401584962
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328805"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="fd452-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="fd452-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="fd452-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd452-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd452-105">Bricht das Senden von Benachrichtigungen ab, die zuvor mit einem Aufruf der [IMAPITable:: Advise](imapitable-advise.md) -Methode eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="fd452-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="fd452-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fd452-106">Parameters</span></span>

 <span data-ttu-id="fd452-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="fd452-107">_ulConnection_</span></span>
  
> <span data-ttu-id="fd452-108">in Die Nummer der Registrierungs Verbindung, die von einem Aufruf von [IMAPITable:: Advise](imapitable-advise.md)zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fd452-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd452-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fd452-109">Return value</span></span>

<span data-ttu-id="fd452-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd452-110">S_OK</span></span> 
  
> <span data-ttu-id="fd452-111">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fd452-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd452-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd452-112">Remarks</span></span>

<span data-ttu-id="fd452-113">Verwenden Sie die **IMAPITable:: Unadvise** -Methode, um den Zeiger auf das Advise-Senke-Objekt, das im _lpAdviseSink_ -Parameter im vorherigen Aufruf von **IMAPITable:: Advise**übergeben wird, aufzuheben, wodurch eine Benachrichtigungs Registrierung abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="fd452-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="fd452-114">Als Teil des Verwerfens des Zeigers auf das Advise-Senke-Objekt wird die **IUnknown:: Release** -Methode des Objekts aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fd452-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="fd452-115">Im Allgemeinen wird **Release** während des Unadvise-Aufrufs aufgerufen, aber wenn ein anderer Thread gerade \*\*\*\* die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Senke aufruft, wird der **Freigabe** Aufruf verzögert, bis die OnNotify \*\*\*\* Methode gibt zurück.</span><span class="sxs-lookup"><span data-stu-id="fd452-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="fd452-116">Weitere Informationen zum Benachrichtigungsprozess finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="fd452-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="fd452-117">Spezifische Informationen zur Tabellenbenachrichtigung finden Sie unter [Informationen zu Tabellen Benachrichtigungen](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="fd452-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="fd452-118">Informationen zur Verwendung der **IMAPISupport** -Methoden zur Unterstützung von Benachrichtigungen finden Sie unter [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="fd452-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fd452-119">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="fd452-119">MFCMAPI reference</span></span>

<span data-ttu-id="fd452-120">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="fd452-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fd452-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="fd452-121">**File**</span></span>|<span data-ttu-id="fd452-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="fd452-122">**Function**</span></span>|<span data-ttu-id="fd452-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="fd452-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd452-124">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="fd452-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="fd452-125">CContentsTableListCtrl:: NotificationOff</span><span class="sxs-lookup"><span data-stu-id="fd452-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="fd452-126">MFCMAPI verwendet die **IMAPITable:: Unadvise** -Methode, um Benachrichtigungen für die Tabelle abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="fd452-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd452-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd452-127">See also</span></span>



[<span data-ttu-id="fd452-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="fd452-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="fd452-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="fd452-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="fd452-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd452-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="fd452-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="fd452-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

