---
title: Implementieren von IUnknown in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 08f3f3f937320d8a986b2002c761a37f0f749227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330177"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="a70b5-103">Implementieren von IUnknown in C++</span><span class="sxs-lookup"><span data-stu-id="a70b5-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="a70b5-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a70b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a70b5-105">Das Implementieren der IUnknown [:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), IUnknown:: [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)und [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methoden der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle in C++ ist relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="a70b5-105">Implementing the [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="a70b5-106">Nach einer Standard Überprüfung der Parameter, die übergeben werden, überprüft eine Implementierung von **QueryInterface** den Bezeichner der angeforderten Schnittstelle anhand der Liste der unterstützten Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="a70b5-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="a70b5-107">Wenn der angeforderte Bezeichner zu den unterstützten gehört, wird **AddRef** aufgerufen, und der **dieser** Zeiger wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a70b5-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="a70b5-108">Wenn sich der angeforderte Bezeichner nicht in der unterstützten Liste befindet, wird der Ausgabezeiger auf NULL festgelegt, und der MAPI_E_INTERFACE_NOT_SUPPORTED-Wert wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a70b5-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="a70b5-109">Das folgende Codebeispiel zeigt, wie Sie **QueryInterface** in C++ für ein Status-Objekt implementieren können, ein Objekt, das eine unterKlasse der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle darstellt.</span><span class="sxs-lookup"><span data-stu-id="a70b5-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="a70b5-110">**IMAPIStatus** erbt von **IUnknown** über [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a70b5-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="a70b5-111">Wenn ein Anrufer eine dieser Schnittstellen anfordert, kann daher **dieser** Zeiger zurückgegeben werden, da die Schnittstellen durch Vererbung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="a70b5-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
```cpp
HRESULT CMyMAPIObject::QueryInterface (REFIID   riid,
                                       LPVOID * ppvObj)
{
    // Always set out parameter to NULL, validating it first.
    if (!ppvObj)
        return E_INVALIDARG;
    *ppvObj = NULL;
    if (riid == IID_IUnknown || riid == IID_IMAPIProp ||
        riid == IID_IMAPIStatus)
    {
        // Increment the reference count and return the pointer.
        *ppvObj = (LPVOID)this;
        AddRef();
        return NOERROR;
    }
    return E_NOINTERFACE;
}

```

<span data-ttu-id="a70b5-112">Im folgenden Codebeispiel wird gezeigt, wie die Methoden **AddRef** und **Release** für das `CMyMAPIObject` Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a70b5-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="a70b5-113">Da die Implementierung von **AddRef** und **Release** einfach ist, entscheiden sich viele Dienstanbieter für eine Inline Implementierung.</span><span class="sxs-lookup"><span data-stu-id="a70b5-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="a70b5-114">Die Aufrufe der Win32-Funktionen **InterlockedIncrement** und **InterlockedDecrement** gewährleisten die Threadsicherheit.</span><span class="sxs-lookup"><span data-stu-id="a70b5-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="a70b5-115">Der Speicher für das Objekt wird vom Destruktor freigegeben, der aufgerufen wird, wenn die **Release** -Methode das Objekt löscht.</span><span class="sxs-lookup"><span data-stu-id="a70b5-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
```cpp
ULONG CMyMAPIObject::AddRef()
{
    InterlockedIncrement(m_cRef);
    return m_cRef;
}
ULONG CMyMAPIObject::Release()
{
    // Decrement the object's internal counter.
    ULONG ulRefCount = InterlockedDecrement(m_cRef);
    if (0 == m_cRef)
    {
        delete this;
    }
    return ulRefCount;
}
 
```

## <a name="see-also"></a><span data-ttu-id="a70b5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a70b5-116">See also</span></span>

- [<span data-ttu-id="a70b5-117">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="a70b5-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="a70b5-118">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a70b5-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

