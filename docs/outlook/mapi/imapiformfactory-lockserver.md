---
title: IMAPIFormFactoryLockServer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory.LockServer
api_type:
- COM
ms.assetid: b9bd389a-6975-41a2-a2f4-e501312e434b
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ab51b939651bc3c121f357545969d26832a19d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342140"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="7fdf6-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="7fdf6-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="7fdf6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fdf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fdf6-105">Behält einen geöffneten Formularserver im Arbeitsspeicher bei.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="7fdf6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fdf6-106">Parameters</span></span>

 <span data-ttu-id="7fdf6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7fdf6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7fdf6-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7fdf6-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="7fdf6-109">_fLockServer_</span></span>
  
> <span data-ttu-id="7fdf6-110">[in] **true,** um die Sperranzahl zu erhöhen. Andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7fdf6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fdf6-111">Return value</span></span>

<span data-ttu-id="7fdf6-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="7fdf6-112">S_OK</span></span> 
  
> <span data-ttu-id="7fdf6-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7fdf6-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7fdf6-114">Remarks</span></span>

<span data-ttu-id="7fdf6-115">Formularbetrachter rufen die **IMAPIFormFactory::LockServer-Methode auf,** um eine geöffnete Formularserveranwendung im Arbeitsspeicher zu behalten.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="7fdf6-116">Das Halten des Formularservers im Arbeitsspeicher verbessert die Leistung, wenn Formulare häufig erstellt und freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7fdf6-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7fdf6-117">Notes to implementers</span></span>

<span data-ttu-id="7fdf6-118">Die **IMAPIFormFactory::LockServer-Methode** ist der [IClassFactory::LockServer-Methode sehr](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) ähnlich.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="7fdf6-119">Im Wesentlichen behält die **IMAPIFormFactory::LockServer-Methode** die Anzahl der Aufrufe bei. Solange diese Anzahl größer als 0 ist, verhindert die Methode, dass der Formularserver aus dem Arbeitsspeicher entladen wird.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="7fdf6-120">Sie können [dies mithilfe der CoLockObjectExternal-Funktion](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) implementieren.</span><span class="sxs-lookup"><span data-stu-id="7fdf6-120">You can use the [CoLockObjectExternal](https://msdn.microsoft.com/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7fdf6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fdf6-121">See also</span></span>



[<span data-ttu-id="7fdf6-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7fdf6-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

