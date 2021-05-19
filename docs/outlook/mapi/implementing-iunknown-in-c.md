---
title: Implementieren von IUnknown in C
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 807b6dc4-cdb7-40a4-87d7-ebc1ad5fab76
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3c634defcad76755fc6604a23d2091bb21e15111
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346774"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="bc42d-103">Implementieren von IUnknown in C</span><span class="sxs-lookup"><span data-stu-id="bc42d-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="bc42d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bc42d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bc42d-105">Implementierungen der [IUnknown::QueryInterface-Methode](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) in C ähneln C++-Implementierungen sehr.</span><span class="sxs-lookup"><span data-stu-id="bc42d-105">Implementations of the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="bc42d-106">Es gibt zwei grundlegende Schritte für die Implementierung:</span><span class="sxs-lookup"><span data-stu-id="bc42d-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="bc42d-107">Überprüfen von Parametern.</span><span class="sxs-lookup"><span data-stu-id="bc42d-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="bc42d-108">Überprüfen des Bezeichners der angeforderten Schnittstelle mit der Liste der vom Objekt unterstützten Schnittstellen und Zurückgeben des werts E_NO_INTERFACE oder eines gültigen Schnittstellenzeigers.</span><span class="sxs-lookup"><span data-stu-id="bc42d-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="bc42d-109">Wenn ein Schnittstellenzeiger zurückgegeben wird, sollte die Implementierung auch die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) aufrufen, um die Referenzanzahl zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bc42d-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="bc42d-110">Der Hauptunterschied zwischen einer Implementierung von **QueryInterface** in C und C++ ist der zusätzliche erste Parameter in der C-Version.</span><span class="sxs-lookup"><span data-stu-id="bc42d-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="bc42d-111">Da der Objektzeiger der Parameterliste hinzugefügt wird, muss eine C-Implementierung von **QueryInterface** mehr Parameterüberprüfung als eine C++-Implementierung haben.</span><span class="sxs-lookup"><span data-stu-id="bc42d-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="bc42d-112">Die Logik zum Überprüfen der Schnittstellen-ID, zum Erhöhen der Referenzanzahl und zum Zurückgeben eines Objektzeigers sollte in beiden Sprachen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="bc42d-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="bc42d-113">Das folgende Codebeispiel zeigt, wie **Sie QueryInterface** in C für ein Statusobjekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="bc42d-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
```cpp
STDMETHODIMP STATUS_QueryInterface(LPMYSTATUSOBJ lpMyObj, REFIID riid,
                                   LPVOID FAR * lppvObj)
{
    HRESULT hr = hrSuccess;
    // Validate the object pointer.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS )
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Validate other parameters.
    if (!lppvObj)
    {
        hr = ResultFromScode(E_INVALIDARG);
        return hr;
    }
    // Set the output pointer to NULL.
    *lppvObj = NULL;
    // Check the interface identifier.
    if (memcmp(riid, &IID_IUnknown, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIProp, sizeof(IID)) &&
        memcmp(riid, &IID_IMAPIStatus, sizeof(IID)))
    {
        hr = ResultFromScode(E_NOINTERFACE);
        return hr;
    }
    // The interface is supported. Increment the reference count and return.
    lpMyObj->lpVtbl->AddRef(lpMyObj);
    *lppvObj = lpMyObj;
    return hr;
}

```

<span data-ttu-id="bc42d-114">Während die Implementierung der **AddRef-Methode** in C einer C++-Implementierung ähnelt, kann eine C-Implementierung der [IUnknown::Release-Methode](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) aufwändiger sein als eine C++-Version.</span><span class="sxs-lookup"><span data-stu-id="bc42d-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="bc42d-115">Dies liegt daran, dass ein Teil der Funktionalität, die mit der Freimachen eines Objekts in den C++-Konstruktor und -Destruktor integriert werden kann, und C über keinen solchen Mechanismus verfügt.</span><span class="sxs-lookup"><span data-stu-id="bc42d-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="bc42d-116">Alle diese Funktionen müssen in der **Release-Methode enthalten** sein.</span><span class="sxs-lookup"><span data-stu-id="bc42d-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="bc42d-117">Außerdem ist aufgrund des zusätzlichen Parameters und der expliziten vtable eine weitere Überprüfung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc42d-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="bc42d-118">Der folgende **AddRef-Methodenaufruf** veranschaulicht eine typische C-Implementierung für ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="bc42d-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
```cpp
STDMETHODIMP_(ULONG) STATUS_AddRef(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check to see whether it has a lpVtbl object member.
    if (!lpMyObj || lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    // Check the method.
    if (STATUS_AddRef != lpMyObj->lpVtbl->AddRef)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = ++lpMyObj->cRef;
    InterlockedDecrement (lpMyObj->cRef);
    return cRef;
}

```

<span data-ttu-id="bc42d-119">Das folgende Codebeispiel zeigt eine typische Implementierung von **Release** für ein C-Status-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc42d-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="bc42d-120">Wenn die Referenzanzahl nach der Dekrementierung 0 ist, sollte eine C-Statusobjektimplementierung die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="bc42d-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="bc42d-121">Lassen Sie alle gehaltenen Zeiger auf Objekte los.</span><span class="sxs-lookup"><span data-stu-id="bc42d-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="bc42d-122">Legen Sie die vtable auf NULL fest, was das Debuggen in dem Fall erleichtert, in dem der Benutzer eines Objekts mit dem Namen **"Release"** das Objekt weiterhin zu verwenden versucht.</span><span class="sxs-lookup"><span data-stu-id="bc42d-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="bc42d-123">Rufen **Sie MAPIFreeBuffer auf,** um das Objekt frei zu machen.</span><span class="sxs-lookup"><span data-stu-id="bc42d-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
```cpp
STDMETHODIMP_(ULONG) STATUS_Release(LPMYSTATUSOBJ lpMyObj)
{
    LONG cRef;
    // Check the size of the vtable.
    if (!lpMyObj)
    {
        return 1;
    }
    // Check whether the vtable is correct.
    if (lpMyObj->lpVtbl != &vtblSTATUS)
    {
        return 1;
    }
    InterlockedIncrement(lpMyObj->cRef);
    cRef = --lpMyObj->cRef;
    InterlockedIncrement (lpMyObj->cRef);
    if (cRef == 0)
    {
        lpMyObj->lpVtbl->Release(lpMyObj);
        DeleteCriticalSection(&lpMyObj->cs);
        // Release the IMAPIProp pointer.
        lpMyObj->lpProp->Release(lpMyObj->lpProp);
        lpMyObj->lpVtbl = NULL;
        lpMyObj->lpFreeBuff(lpMyObj);
        return 0;
    }
    return cRef;
}

```

## <a name="see-also"></a><span data-ttu-id="bc42d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc42d-124">See also</span></span>

- [<span data-ttu-id="bc42d-125">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="bc42d-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="bc42d-126">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bc42d-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

