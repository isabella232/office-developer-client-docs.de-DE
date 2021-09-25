---
title: Implementieren von IUnknown in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c64f29c91341209988f7980957468cd96ff70779
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630551"
---
# <a name="implementing-iunknown-in-c"></a>Implementieren von IUnknown in C++

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Das Implementieren der [IUnknown::QueryInterface-,](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) [IUnknown::AddRef-](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx)und [IUnknown::Release-Methoden](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) in C++ ist ziemlich einfach. Nach einer Standardüberprüfung der übergebenen Parameter überprüft eine Implementierung von **QueryInterface** den Bezeichner der angeforderten Schnittstelle anhand der Liste der unterstützten Schnittstellen. Wenn der angeforderte Bezeichner zu den unterstützten gehört, wird **AddRef** aufgerufen, und **dieser** Zeiger wird zurückgegeben. Wenn der angeforderte Bezeichner nicht in der unterstützten Liste enthalten ist, wird der Ausgabezeiger auf NULL festgelegt, und der MAPI_E_INTERFACE_NOT_SUPPORTED Wert wird zurückgegeben. 
  
Das folgende Codebeispiel zeigt, wie Sie **QueryInterface** in C++ für ein Statusobjekt implementieren können, ein Objekt, das eine Unterklasse der [IMAPIStatus : IMAPIProp-Schnittstelle](imapistatusimapiprop.md) ist. **IMAPIStatus** erbt von **IUnknown** über [IMAPIProp: IUnknown](imapipropiunknown.md). Wenn ein Aufrufer eine dieser Schnittstellen anfragt, kann **dieser** Zeiger daher zurückgegeben werden, da die Schnittstellen durch Vererbung verknüpft sind. 
  
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

Das folgende Codebeispiel zeigt, wie die **AddRef-** und **Release-Methoden** für das Objekt implementiert  `CMyMAPIObject` werden. Da die Implementierung von **AddRef** und **Release** einfach ist, entscheiden sich viele Dienstanbieter dafür, sie inline zu implementieren. Die Aufrufe der Win32-Funktionen **"InterlockedIncrement"** und **"InterlockedDecrement"** stellen Threadsicherheit sicher. Der Speicher für das Objekt wird vom Destruktor freigegeben, der aufgerufen wird, wenn die **Release-Methode** das Objekt löscht. 
  
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

