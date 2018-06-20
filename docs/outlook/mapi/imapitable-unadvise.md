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
ms.openlocfilehash: e9d8565cfaa17764e92bddafb29e744d23872515
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792491"
---
# <a name="imapitableunadvise"></a><span data-ttu-id="ba6e0-103">IMAPITable::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ba6e0-103">IMAPITable::Unadvise</span></span>

  
  
<span data-ttu-id="ba6e0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ba6e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ba6e0-105">Bricht ab, das Senden von Benachrichtigungen, die zuvor mit einem Aufruf der Methode [IMAPITable::Advise](imapitable-advise.md) eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-105">Cancels the sending of notifications previously set up with a call to the [IMAPITable::Advise](imapitable-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="ba6e0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba6e0-106">Parameters</span></span>

 <span data-ttu-id="ba6e0-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="ba6e0-107">_ulConnection_</span></span>
  
> <span data-ttu-id="ba6e0-108">[in] Die Anzahl der Registrierung Verbindung durch einen Aufruf von [IMAPITable::Advise](imapitable-advise.md)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-108">[in] The number of the registration connection returned by a call to [IMAPITable::Advise](imapitable-advise.md).</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ba6e0-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ba6e0-109">Return value</span></span>

<span data-ttu-id="ba6e0-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ba6e0-110">S_OK</span></span> 
  
> <span data-ttu-id="ba6e0-111">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-111">The call succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ba6e0-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ba6e0-112">Remarks</span></span>

<span data-ttu-id="ba6e0-113">Verwenden Sie die **IMAPITable::Unadvise** -Methode, um den Zeiger auf den im Parameter _LpAdviseSink_ im vorherigen Aufruf **IMAPITable::Advise**, wodurch Stornieren einer benachrichtigungsregistrierung übergeben Advise-Empfängerobjekt freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-113">Use the **IMAPITable::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMAPITable::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="ba6e0-114">Im Rahmen des Zeigers auf das Empfängerobjekt Advise verwerfen wird das Objekt **IUnknown** -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-114">As part of discarding the pointer to the advise sink object, the object's **IUnknown::Release** method is called.</span></span> <span data-ttu-id="ba6e0-115">Im allgemeinen **Release** aufgerufen wird während des Anrufs **Unadvise** , jedoch ist, wenn ein anderer Thread aufruft, die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode für die Advise-Empfänger der Anruf **Version** verzögert, bis die **OnNotify** -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-115">Generally, **Release** is called during the **Unadvise** call, but if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
<span data-ttu-id="ba6e0-116">Weitere Informationen zu den Benachrichtigungsprozess finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e0-116">For more information on the notification process, see [Event Notification in MAPI](event-notification-in-mapi.md).</span></span> <span data-ttu-id="ba6e0-117">Spezifische Informationen zur Tabelle Benachrichtigung finden Sie unter [Zur Tabelle Benachrichtigungen](about-table-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e0-117">For specific information about table notification, see [About Table Notifications](about-table-notifications.md).</span></span> <span data-ttu-id="ba6e0-118">Informationen zur Verwendung der Methods **IMAPISupport** zum Benachrichtigung zu unterstützen finden Sie unter [Event Notification unterstützen](supporting-event-notification.md).</span><span class="sxs-lookup"><span data-stu-id="ba6e0-118">For information about using the **IMAPISupport** methods to support notification, see [Supporting Event Notification](supporting-event-notification.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba6e0-119">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="ba6e0-119">MFCMAPI reference</span></span>

<span data-ttu-id="ba6e0-120">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-120">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba6e0-121">**Datei**</span><span class="sxs-lookup"><span data-stu-id="ba6e0-121">**File**</span></span>|<span data-ttu-id="ba6e0-122">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="ba6e0-122">**Function**</span></span>|<span data-ttu-id="ba6e0-123">**Comment**</span><span class="sxs-lookup"><span data-stu-id="ba6e0-123">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba6e0-124">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ba6e0-124">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ba6e0-125">CContentsTableListCtrl::NotificationOff</span><span class="sxs-lookup"><span data-stu-id="ba6e0-125">CContentsTableListCtrl::NotificationOff</span></span>  <br/> |<span data-ttu-id="ba6e0-126">MFCMAPI (engl.) verwendet die **IMAPITable::Unadvise** -Methode, um Benachrichtigungen für die Tabelle abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="ba6e0-126">MFCMAPI uses the **IMAPITable::Unadvise** method to cancel notifications for the table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba6e0-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba6e0-127">See also</span></span>



[<span data-ttu-id="ba6e0-128">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="ba6e0-128">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="ba6e0-129">IMAPITable::Advise</span><span class="sxs-lookup"><span data-stu-id="ba6e0-129">IMAPITable::Advise</span></span>](imapitable-advise.md)
  
[<span data-ttu-id="ba6e0-130">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ba6e0-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="ba6e0-131">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="ba6e0-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

