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
ms.openlocfilehash: c899eb0afd123b26e12081f5157be3bae7917813
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792567"
---
# <a name="implementing-iunknown-in-c"></a><span data-ttu-id="fa2e6-103">Implementieren von IUnknown in C++</span><span class="sxs-lookup"><span data-stu-id="fa2e6-103">Implementing IUnknown in C++</span></span>

<span data-ttu-id="fa2e6-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa2e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa2e6-105">Implementieren die [QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx), [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx)und [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methoden des die [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle in C++ ist relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-105">Implementing the [IUnknown::QueryInterface](http://msdn.microsoft.com/de-de/library/ms682521%28v=VS.85%29.aspx), [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx), and [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) methods of the [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) interface in C++ is fairly simple.</span></span> <span data-ttu-id="fa2e6-106">Nach einigen standard Überprüfung der Parameter, die übergeben werden, wird eine Implementierung von **QueryInterface** den Bezeichner der angeforderten Schnittstelle anhand der Liste der unterstützten Schnittstellen überprüft.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-106">After some standard validation of the parameters that are passed in, an implementation of **QueryInterface** checks the identifier of the requested interface against the list of supported interfaces.</span></span> <span data-ttu-id="fa2e6-107">Ist der Bezeichner der angeforderte unterstützt, **AddRef** aufgerufen wird, und der **diesem** Zeiger wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-107">If the requested identifier is among those supported, **AddRef** is called and the **this** pointer is returned.</span></span> <span data-ttu-id="fa2e6-108">Ist der Bezeichner der angeforderte nicht auf die Liste der unterstützten, der Ausgabezeiger auf NULL festgelegt ist, und der Wert des MAPI_E_INTERFACE_NOT_SUPPORTED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-108">If the requested identifier is not on the supported list, the output pointer is set to NULL and the MAPI_E_INTERFACE_NOT_SUPPORTED value is returned.</span></span> 
  
<span data-ttu-id="fa2e6-109">Im folgenden Codebeispiel wird veranschaulicht, wie **QueryInterface** in C++ für ein Objekt ein Statusobjekt implementiert werden kann, die eine Unterklasse der ist die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-109">The following code example shows how you can implement **QueryInterface** in C++ for a status object, an object that is a subclass of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="fa2e6-110">**IMAPIStatus** erbt von **IUnknown** über [IMAPIProp: IUnknown](imapipropiunknown.md).</span><span class="sxs-lookup"><span data-stu-id="fa2e6-110">**IMAPIStatus** inherits from **IUnknown** through [IMAPIProp : IUnknown](imapipropiunknown.md).</span></span> <span data-ttu-id="fa2e6-111">Aus diesem Grund, wenn ein Anrufer für alle diese Schnittstellen gefragt werden, kann **diese** der Zeiger zurückgegeben werden, da die Schnittstellen über Vererbung verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-111">Therefore, if a caller asks for any of these interfaces, the **this** pointer can be returned because the interfaces are related through inheritance.</span></span> 
  
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

<span data-ttu-id="fa2e6-112">Im folgenden Codebeispiel wird veranschaulicht, wie Sie die **AddRef** und **Release** Methoden zum Implementieren der `CMyMAPIObject` Objekt.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-112">The following code example shows how to implement the **AddRef** and **Release** methods for the  `CMyMAPIObject` object.</span></span> <span data-ttu-id="fa2e6-113">Da implementieren, **AddRef** und **Release** recht einfach ist, wählen viele Dienstanbieter sie Inline implementieren.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-113">Because implementing **AddRef** and **Release** is straightforward, many service providers choose to implement them inline.</span></span> <span data-ttu-id="fa2e6-114">Die Anrufe an die Win32-Funktionen **InterlockedIncrement** und **InterlockedDecrement** sicherstellen Threadsicherheit.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-114">The calls to the Win32 functions **InterlockedIncrement** and **InterlockedDecrement** ensure thread safety.</span></span> <span data-ttu-id="fa2e6-115">Der Speicher für das Objekt wird durch den Destruktor freigegeben, die aufgerufen wird, wenn die **Release** -Methode das Objekt löscht.</span><span class="sxs-lookup"><span data-stu-id="fa2e6-115">The memory for the object is freed by the destructor, which is called when the **Release** method deletes the object.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="fa2e6-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa2e6-116">See also</span></span>

- [<span data-ttu-id="fa2e6-117">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="fa2e6-117">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)
- [<span data-ttu-id="fa2e6-118">Implementieren der IUnknown-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fa2e6-118">Implementing the IUnknown Interface</span></span>](implementing-the-iunknown-interface.md)

