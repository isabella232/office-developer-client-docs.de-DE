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
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348874"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="8e64f-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="8e64f-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="8e64f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8e64f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8e64f-105">Protokolliert einen Nachrichtenspeicheranbieter.</span><span class="sxs-lookup"><span data-stu-id="8e64f-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="8e64f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e64f-106">Parameters</span></span>

 <span data-ttu-id="8e64f-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="8e64f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="8e64f-108">[in] Reserviert; muss ein Zeiger auf Null sein.</span><span class="sxs-lookup"><span data-stu-id="8e64f-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8e64f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8e64f-109">Return value</span></span>

<span data-ttu-id="8e64f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="8e64f-110">S_OK</span></span> 
  
> <span data-ttu-id="8e64f-111">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="8e64f-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8e64f-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8e64f-112">Remarks</span></span>

<span data-ttu-id="8e64f-113">Nachrichtenspeicheranbieter implementieren die **IMSLogon::Logoff-Methode** zum gewaltsamen Herunterfahren eines Nachrichtenspeicheranbieters.</span><span class="sxs-lookup"><span data-stu-id="8e64f-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="8e64f-114">**IMSLogon::Logoff** wird in den folgenden Situationen aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="8e64f-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="8e64f-115">Während MAPI einen Client nach einem Aufruf der [IMAPISession::Logoff-Methode](imapisession-logoff.md) abmeldet.</span><span class="sxs-lookup"><span data-stu-id="8e64f-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="8e64f-116">Während MAPI einen Nachrichtenspeicheranbieter abmeldet.</span><span class="sxs-lookup"><span data-stu-id="8e64f-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="8e64f-117">In diesem Fall wird **IMSLogon::Logoff** als Teil der MAPI-Verarbeitung der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) des Supportobjekts aufgerufen, das der Nachrichtenspeicheranbieter erstellt, während er einen [IMsgStore::StoreLogoff-](imsgstore-storelogoff.md) oder **IUnknown::Release-Methodenaufruf** für ein Nachrichtenspeicherobjekt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8e64f-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="8e64f-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e64f-118">See also</span></span>



[<span data-ttu-id="8e64f-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="8e64f-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="8e64f-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e64f-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="8e64f-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="8e64f-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="8e64f-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="8e64f-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="8e64f-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8e64f-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8e64f-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8e64f-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

