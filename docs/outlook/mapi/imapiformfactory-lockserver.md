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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c33fea8a2aba875fcdc06dea3343add4b7ac5dde
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792145"
---
# <a name="imapiformfactorylockserver"></a><span data-ttu-id="65813-103">IMAPIFormFactory::LockServer</span><span class="sxs-lookup"><span data-stu-id="65813-103">IMAPIFormFactory::LockServer</span></span>

  
  
<span data-ttu-id="65813-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="65813-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="65813-105">Wird einen geöffnete Formular Server im Arbeitsspeicher gespeichert.</span><span class="sxs-lookup"><span data-stu-id="65813-105">Keeps an open form server in memory.</span></span>
  
```cpp
HRESULT LockServer(
  ULONG ulFlags,
  ULONG fLockServer
);
```

## <a name="parameters"></a><span data-ttu-id="65813-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="65813-106">Parameters</span></span>

 <span data-ttu-id="65813-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="65813-107">_ulFlags_</span></span>
  
> <span data-ttu-id="65813-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="65813-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="65813-109">_fLockServer_</span><span class="sxs-lookup"><span data-stu-id="65813-109">_fLockServer_</span></span>
  
> <span data-ttu-id="65813-110">[in] **true,** um die Anzahl der Sperren zu erhöhen. anderenfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="65813-110">[in] **true** to increment the lock count; otherwise, **false**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="65813-111">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="65813-111">Return value</span></span>

<span data-ttu-id="65813-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="65813-112">S_OK</span></span> 
  
> <span data-ttu-id="65813-113">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="65813-113">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="65813-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="65813-114">Remarks</span></span>

<span data-ttu-id="65813-115">Formular Viewer rufen Sie die **IMAPIFormFactory::LockServer** -Methode, um eine geöffnete Formular-Server-Anwendung im Arbeitsspeicher zu halten.</span><span class="sxs-lookup"><span data-stu-id="65813-115">Form viewers call the **IMAPIFormFactory::LockServer** method to keep an open form server application in memory.</span></span> <span data-ttu-id="65813-116">Aufrechterhaltung des Formulars im Arbeitsspeicher verbessert die Leistung, wenn Formulare häufig erstellt und veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="65813-116">Keeping the form server in memory improves its performance when forms are frequently created and released.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="65813-117">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="65813-117">Notes to implementers</span></span>

<span data-ttu-id="65813-118">Die **IMAPIFormFactory::LockServer** -Methode ähnelt der [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="65813-118">The **IMAPIFormFactory::LockServer** method is very similar to the [IClassFactory::LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="65813-119">Im Wesentlichen verwaltet die **IMAPIFormFactory::LockServer** -Methode an, dass die Anzahl, wie oft aufgerufen wurde. als diese Anzahl größer als 0 ist, verhindert, dass die-Methode den Formular-Server, die aus dem Speicher entladen wird.</span><span class="sxs-lookup"><span data-stu-id="65813-119">Essentially, the **IMAPIFormFactory::LockServer** method maintains a count of how many times it has been called; as long as that count is greater than 0, the method prevents the form server from being unloaded from memory.</span></span> <span data-ttu-id="65813-120">Die [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) -Funktion können Sie um dies zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="65813-120">You can use the [CoLockObjectExternal](http://msdn.microsoft.com/en-us/library/ms680592%28VS.85%29.aspx) function to implement this.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="65813-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65813-121">See also</span></span>



[<span data-ttu-id="65813-122">IMAPIFormFactory : IUnknown</span><span class="sxs-lookup"><span data-stu-id="65813-122">IMAPIFormFactory : IUnknown</span></span>](imapiformfactoryiunknown.md)

