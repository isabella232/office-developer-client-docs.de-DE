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
# <a name="implementing-iunknown-in-c"></a>Implementieren von IUnknown in C++

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Implementierung der [IUnknown::QueryInterface-,](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) [IUnknown::AddRef-](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)und [IUnknown::Release-Methoden](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) in C++ ist recht einfach. Nach einigen Standardüberprüfungen der übergebenen Parameter überprüft eine Implementierung von **QueryInterface** den Bezeichner der angeforderten Schnittstelle mit der Liste der unterstützten Schnittstellen. Wenn der angeforderte Bezeichner zu den unterstützten gehört, wird **AddRef** aufgerufen, **und** der Zeiger wird zurückgegeben. Wenn sich der angeforderte Bezeichner nicht in der unterstützten Liste befindet, wird der Ausgabezeiger auf NULL festgelegt, MAPI_E_INTERFACE_NOT_SUPPORTED zurückgegeben wird. 
  
Das folgende Codebeispiel zeigt, wie **Sie QueryInterface** in C++ für ein Statusobjekt implementieren können, ein Objekt, das eine Unterklasse der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) ist. **IMAPIStatus** erbt von **IUnknown** über [IMAPIProp : IUnknown](imapipropiunknown.md). Daher kann der Zeiger zurückgegeben werden, wenn  ein Aufrufer nach einer dieser Schnittstellen fragt, da die Schnittstellen durch Vererbung miteinander verbunden sind. 
  
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

Das folgende Codebeispiel zeigt, wie die **AddRef-** und **Release-Methoden** für das Objekt implementiert  `CMyMAPIObject` werden. Da die **Implementierung von AddRef** **und Release** unkompliziert ist, entscheiden sich viele Dienstanbieter dafür, sie inline zu implementieren. Die Aufrufe der Win32-Funktionen **InterlockedIncrement** und **InterlockedDecrement** sorgen für Threadsicherheit. Der Arbeitsspeicher für das Objekt wird vom Destruktor freigegeben, der aufgerufen wird, wenn die **Release-Methode** das Objekt löscht. 
  
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

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)
- [Implementieren der IUnknown-Schnittstelle](implementing-the-iunknown-interface.md)

