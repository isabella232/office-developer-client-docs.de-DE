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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bf72e6f182f67861f909e21f0ec1871d76617974
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792022"
---
# <a name="iaddrbookunadvise"></a><span data-ttu-id="5849d-103">IAddrBook::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5849d-103">IAddrBook::Unadvise</span></span>

  
  
<span data-ttu-id="5849d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5849d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5849d-105">Benachrichtigungsregistrierung eines für einen Adresseintrag Adressbuch zuvor eingerichtet werden abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5849d-105">Cancels a notification registration previously established for an address book entry.</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG_PTR ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5849d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5849d-106">Parameters</span></span>

 <span data-ttu-id="5849d-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="5849d-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5849d-108">[in] Eine Verbindung Zahl, die die Registrierung abgebrochen werden darstellt.</span><span class="sxs-lookup"><span data-stu-id="5849d-108">[in] A connection number that represents the registration to be canceled.</span></span> <span data-ttu-id="5849d-109">Der Parameter _UlConnection_ sollte einen von einem vorherigen Aufruf der [IAddrBook::Advise](iaddrbook-advise.md) -Methode zurückgegebenen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="5849d-109">The  _ulConnection_ parameter should contain a value returned by a prior call to the [IAddrBook::Advise](iaddrbook-advise.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="5849d-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="5849d-110">Return value</span></span>

<span data-ttu-id="5849d-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5849d-111">S_OK</span></span> 
  
> <span data-ttu-id="5849d-112">Die Registrierung wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="5849d-112">The registration was successfully canceled.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5849d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5849d-113">Remarks</span></span>

<span data-ttu-id="5849d-114">Clients aufrufen die **Unadvise** -Methode zum Empfangen von Benachrichtigungen zu Änderungen an einer bestimmten Adressbuch Adresseintrag beenden.</span><span class="sxs-lookup"><span data-stu-id="5849d-114">Clients call the **Unadvise** method to stop receiving notifications about changes to a particular address book entry.</span></span> <span data-ttu-id="5849d-115">Wenn ein benachrichtigungsregistrierung abgebrochen wird, der Adressbuchdateien Anbieter Versionen der Zeiger auf den Anrufer der advise-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="5849d-115">When a notification registration is canceled, the address book provider releases its pointer to the caller's advise sink.</span></span> <span data-ttu-id="5849d-116">Die Version kann jedoch während des Anrufs **Unadvise** oder zu einem späteren Zeitpunkt, auftreten, wenn ein anderer Thread ist die [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="5849d-116">However, the release can occur during the **Unadvise** call or at some later point, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method.</span></span> <span data-ttu-id="5849d-117">Wenn eine Benachrichtigung ausgeführt wird, wird die Version verzögert, bis die **OnNotify** -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5849d-117">When a notification is in progress, the release is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5849d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5849d-118">See also</span></span>



[<span data-ttu-id="5849d-119">IAddrBook::Advise</span><span class="sxs-lookup"><span data-stu-id="5849d-119">IAddrBook::Advise</span></span>](iaddrbook-advise.md)
  
[<span data-ttu-id="5849d-120">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="5849d-120">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="5849d-121">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5849d-121">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)

