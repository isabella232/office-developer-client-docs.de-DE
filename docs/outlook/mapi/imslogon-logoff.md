---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d9a57cee371675493ba71b2df52b83941d34fc2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792685"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="3544a-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="3544a-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="3544a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3544a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3544a-105">Eine Nachricht Abmeldung Speicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="3544a-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3544a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3544a-106">Parameters</span></span>

 <span data-ttu-id="3544a-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="3544a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="3544a-108">[in] Reserviert. Ein Zeiger auf 0 (null) muss sein.</span><span class="sxs-lookup"><span data-stu-id="3544a-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3544a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3544a-109">Return value</span></span>

<span data-ttu-id="3544a-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3544a-110">S_OK</span></span> 
  
> <span data-ttu-id="3544a-111">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="3544a-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3544a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3544a-112">Remarks</span></span>

<span data-ttu-id="3544a-113">Nachricht Anbieter implementieren Sie die **IMSLogon::Logoff** -Methode eine Nachricht Speicheranbieter zwangsweise Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="3544a-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="3544a-114">**IMSLogon::Logoff** wird in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="3544a-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="3544a-115">Während MAPI deaktiviert Clientidentität nach einem Aufruf der Methode [IMAPISession::Logoff](imapisession-logoff.md) protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="3544a-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="3544a-116">Während MAPI aus einer Nachricht Speicheranbieter protokolliert wird.</span><span class="sxs-lookup"><span data-stu-id="3544a-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="3544a-117">In diesem Fall **IMSLogon::Logoff** im Rahmen der Verarbeitung der [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methode des Support-Objekts, mit dem Anbieter der Nachricht erstellt, während ein [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) oder **IUnknown verarbeitet wird MAPI aufgerufen wird: Version** Methodenaufruf für eine Nachricht Store-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3544a-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3544a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3544a-118">See also</span></span>



[<span data-ttu-id="3544a-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="3544a-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="3544a-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3544a-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="3544a-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="3544a-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="3544a-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="3544a-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="3544a-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3544a-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3544a-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3544a-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

