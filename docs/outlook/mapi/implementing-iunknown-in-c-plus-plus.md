---
title: Implementieren von IUnknown in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 68519f6c-fba8-47f5-9401-316e276f770e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c899eb0afd123b26e12081f5157be3bae7917813
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792567"
---
# <a name="implementing-iunknown-in-c"></a>Implementieren von IUnknown in C++

**Betrifft**: Outlook 
  
Implementieren die [QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx), [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx)und [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methoden des die [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle in C++ ist relativ einfach. Nach einigen standard Überprüfung der Parameter, die übergeben werden, wird eine Implementierung von **QueryInterface** den Bezeichner der angeforderten Schnittstelle anhand der Liste der unterstützten Schnittstellen überprüft. Ist der Bezeichner der angeforderte unterstützt, **AddRef** aufgerufen wird, und der **diesem** Zeiger wird zurückgegeben. Ist der Bezeichner der angeforderte nicht auf die Liste der unterstützten, der Ausgabezeiger auf NULL festgelegt ist, und der Wert des MAPI_E_INTERFACE_NOT_SUPPORTED zurückgegeben. 
  
Im folgenden Codebeispiel wird veranschaulicht, wie **QueryInterface** in C++ für ein Objekt ein Statusobjekt implementiert werden kann, die eine Unterklasse der ist die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle. **IMAPIStatus** erbt von **IUnknown** über [IMAPIProp: IUnknown](imapipropiunknown.md). Aus diesem Grund, wenn ein Anrufer für alle diese Schnittstellen gefragt werden, kann **diese** der Zeiger zurückgegeben werden, da die Schnittstellen über Vererbung verknüpft sind. 
  
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

Im folgenden Codebeispiel wird veranschaulicht, wie Sie die **AddRef** und **Release** Methoden zum Implementieren der `CMyMAPIObject` Objekt. Da implementieren, **AddRef** und **Release** recht einfach ist, wählen viele Dienstanbieter sie Inline implementieren. Die Anrufe an die Win32-Funktionen **InterlockedIncrement** und **InterlockedDecrement** sicherstellen Threadsicherheit. Der Speicher für das Objekt wird durch den Destruktor freigegeben, die aufgerufen wird, wenn die **Release** -Methode das Objekt löscht. 
  
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

