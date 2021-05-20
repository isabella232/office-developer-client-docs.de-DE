---
title: IAddrBookUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.Unadvise
api_type:
- COM
ms.assetid: e0db9e86-9528-43de-b8ba-a5af8b7bda4b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2988f1fc149bbfc2d724b62b12bd12ae4f4664a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436153"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="06491-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="06491-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="06491-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06491-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06491-105">Bricht eine Benachrichtigungsregistrierung ab, die zuvor für einen Adressbucheintrag eingerichtet wurde.</span><span class="sxs-lookup"><span data-stu-id="06491-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="06491-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06491-106">Parameters</span></span>

 <span data-ttu-id="06491-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="06491-107">_ulConnection_</span></span>
  
> <span data-ttu-id="06491-108">[in] Eine Verbindungsnummer, die die zu kündigende Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="06491-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="06491-109">Der  _ulConnection-Parameter_ sollte einen Wert enthalten, der durch einen vorherigen Aufruf der [IAddrBook::Advise-Methode zurückgegeben](iaddrbook-advise.md) wurde.</span><span class="sxs-lookup"><span data-stu-id="06491-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="06491-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06491-110">Return value</span></span>

<span data-ttu-id="06491-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="06491-111">S_OK</span></span> 
  
> <span data-ttu-id="06491-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="06491-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="06491-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="06491-113">Remarks</span></span>

<span data-ttu-id="06491-114">Clients rufen die **Unadvise-Methode** auf, um den Empfang von Benachrichtigungen über Änderungen an einem bestimmten Adressbucheintrag zu beenden.</span><span class="sxs-lookup"><span data-stu-id="06491-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="06491-115">Wenn eine Benachrichtigungsregistrierung abgebrochen wird, gibt der Adressbuchanbieter seinen Zeiger auf die Ratgebersenke des Anrufers frei.</span><span class="sxs-lookup"><span data-stu-id="06491-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="06491-116">Die Veröffentlichung kann jedoch während des **Unadvise-Aufrufs** oder zu einem späteren Zeitpunkt auftreten, wenn ein anderer Thread die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="06491-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="06491-117">Wenn eine Benachrichtigung ausgeführt wird, wird die Veröffentlichung verzögert, bis die **OnNotify-Methode zurückgegeben** wird.</span><span class="sxs-lookup"><span data-stu-id="06491-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06491-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06491-118">See also</span></span>



[<span data-ttu-id="06491-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="06491-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="06491-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="06491-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="06491-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="06491-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

