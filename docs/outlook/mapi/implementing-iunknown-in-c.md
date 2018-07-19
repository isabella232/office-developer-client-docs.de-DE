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
ms.openlocfilehash: d12201d8476d15021e896a44797ae5fc21178802
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792569"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="3c443-103">Implementieren von IUnknown in C</span><span class="sxs-lookup"><span data-stu-id="3c443-103">Implementing IUnknown in C</span></span>

<span data-ttu-id="3c443-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3c443-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3c443-105">Implementierungen von [QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) -Methode in C# sind C++ Implementierungen sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="3c443-105">Implementations of the [IUnknown::QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx) method in C are very similar to C++ implementations.</span></span> <span data-ttu-id="3c443-106">Es gibt zwei grundlegende Schritte an der Implementierung:</span><span class="sxs-lookup"><span data-stu-id="3c443-106">There are two basic steps to the implementation:</span></span> 
  
1. <span data-ttu-id="3c443-107">Überprüfen die Parameter.</span><span class="sxs-lookup"><span data-stu-id="3c443-107">Validating parameters.</span></span>
    
2. <span data-ttu-id="3c443-108">Überprüfen den Bezeichner des mit der Liste der Schnittstellen, die durch das Objekt unterstützt die angeforderte Schnittstelle und Zurückgeben der E_NO_INTERFACE-Wert oder einen Zeiger gültige Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3c443-108">Checking the identifier of the requested interface against the list of interfaces supported by the object and returning either the E_NO_INTERFACE value or a valid interface pointer.</span></span> <span data-ttu-id="3c443-109">Wenn ein Schnittstellenzeiger zurückgegeben wird, sollte die Implementierung die [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) -Methode, um den Referenzzähler erhöhen auch aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3c443-109">If an interface pointer is returned, the implementation should also call the [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) method to increment the reference count.</span></span> 
    
<span data-ttu-id="3c443-110">Der Hauptunterschied zwischen einer Implementierung von **QueryInterface** in C# und C++ ist der erste zusätzliche Parameter in der C-Version.</span><span class="sxs-lookup"><span data-stu-id="3c443-110">The main difference between an implementation of **QueryInterface** in C and C++ is the additional first parameter in the C version.</span></span> <span data-ttu-id="3c443-111">Da der Parameterliste der Objektzeiger hinzugefügt wird, benötigen eine C#-Implementierung von **QueryInterface** Weitere Parameter Überprüfung als eine C++-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="3c443-111">Because the object pointer is added to the parameter list, a C implementation of **QueryInterface** must have more parameter validation than a C++ implementation.</span></span> <span data-ttu-id="3c443-112">Die Logik für die Überprüfung der Identifier, erhöht den Referenzzähler und Zurückgeben eines Objektzeigers muss in beiden Sprachen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="3c443-112">The logic for checking the interface identifier, incrementing the reference count, and returning an object pointer should be identical in both languages.</span></span> 
  
<span data-ttu-id="3c443-113">Im folgenden Codebeispiel wird veranschaulicht, wie **QueryInterface** in C für ein Statusobjekt implementieren.</span><span class="sxs-lookup"><span data-stu-id="3c443-113">The following code example shows how to implement **QueryInterface** in C for a status object.</span></span> 
  
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

<span data-ttu-id="3c443-114">Während die Implementierung der **AddRef** -Methode in C# eine C++-Implementierung ähnlich ist, kann eine C#-Implementierung der [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methode aufwendigeres als eine C++-Version abrufen.</span><span class="sxs-lookup"><span data-stu-id="3c443-114">Whereas the implementation of the **AddRef** method in C is similar to a C++ implementation, a C implementation of the [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) method can get more elaborate than a C++ version.</span></span> <span data-ttu-id="3c443-115">Dies ist, da der Großteil der Funktionalität Zusammenhang mit der Freigabe eines Objekts in C++ Konstruktor und Destruktor integriert werden kann und C hat kein entsprechender Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="3c443-115">This is because much of the functionality involved with freeing an object can be incorporated into the C++ constructor and destructor, and C has no such mechanism.</span></span> <span data-ttu-id="3c443-116">Alle diese Funktionalität muss in der **Version** -Methode enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="3c443-116">All of this functionality must be included in the **Release** method.</span></span> <span data-ttu-id="3c443-117">Darüber hinaus ist aufgrund der zusätzliche Parameter und dessen explizite Vtable, weitere Validierung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3c443-117">Also, because of the additional parameter and its explicit vtable, more validation is required.</span></span> 
  
<span data-ttu-id="3c443-118">Der folgende Aufruf von **AddRef** -Methode veranschaulicht eine typische C-Implementierung für ein Statusobjekt.</span><span class="sxs-lookup"><span data-stu-id="3c443-118">The following **AddRef** method call illustrates a typical C implementation for a status object.</span></span> 
  
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

<span data-ttu-id="3c443-119">Das folgende Codebeispiel zeigt für ein Objekt der C-Status eine normale Implementierung der **Version** .</span><span class="sxs-lookup"><span data-stu-id="3c443-119">The following code example shows a typical implementation of **Release** for a C status object.</span></span> <span data-ttu-id="3c443-120">Wenn Sie der Referenzzähler 0 ist, nachdem er verringert wird, sollte eine C Status objektimplementierung die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="3c443-120">If the reference count is 0 after it is decremented, a C status object implementation should perform the following tasks:</span></span> 
  
- <span data-ttu-id="3c443-121">Lassen Sie alle angehaltenen Zeiger auf Objekte.</span><span class="sxs-lookup"><span data-stu-id="3c443-121">Release any held pointers to objects.</span></span> 
    
- <span data-ttu-id="3c443-122">Die Vtable auf NULL festgelegt wurde, im Fall, in dem ein Objekt Benutzer mit dem Namen **Version** noch fortgesetzt versuchen, verwenden Sie das Objekt, Debuggen erleichtern.</span><span class="sxs-lookup"><span data-stu-id="3c443-122">Set the vtable to NULL, facilitating debugging in the case where an object's user called **Release** yet continued to try to use the object.</span></span> 
    
- <span data-ttu-id="3c443-123">Rufen Sie **MAPIFreeBuffer** , um das Objekt frei.</span><span class="sxs-lookup"><span data-stu-id="3c443-123">Call **MAPIFreeBuffer** to free the object.</span></span> 
    
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

## <a name="see-also"></a><span data-ttu-id="3c443-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c443-124">See also</span></span>

- [<span data-ttu-id="3c443-125">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="3c443-125">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="3c443-126">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3c443-126">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

