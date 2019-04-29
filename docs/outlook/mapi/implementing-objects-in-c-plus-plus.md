---
title: Implementieren von Objekten in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 89247ca1b263d6f06af73f1ffa14709a2aff23de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432954"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C++

**Gilt für**: Outlook 2013 | Outlook 2016 
  
C++-Clients und-Dienstanbieter definieren MAPI-Objekte, indem Sie Klassen erstellen, die von den von Ihnen implementierten Schnittstellen erben. Jede der Interface-Methoden ist öffentlich, ebenso wie der Konstruktor und der Destruktor für die Klasse. Wenn die Klasse über zusätzliche Methoden verfügt, können Sie je nach Implementierung öffentlich oder privat sein. Alle Datenmember sind privat. 
  
Der folgende Beispielcode zeigt, wie Sie ein C++-Statusobjekt definieren. Die `CMyMAPIObject` Klasse erbt von der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Schnittstelle. Viele der in diesem Beispiel verwendeten Makros sind in der OLE-Headerdatei COMPOBJ. h definiert. Die ersten Member der Klasse sind die Methoden der Basisschnittstelle, gefolgt von den Methoden der geerbten Schnittstellen in der Reihenfolge der Vererbung. Nach den Schnittstellendefinitionen werden zusätzliche Methoden, der Konstruktor und der Destruktor sowie die Datenmember angezeigt. 
  
```cpp
class  CMyMAPIObject : public IMAPIStatus
{
public:
// Methods of IUnknown.
    STDMETHODIMP QueryInterface (REFIID riid, LPVOID * ppvObj);
    STDMETHODIMP_(ULONG) AddRef ();
    STDMETHODIMP_(ULONG) Release ();
    MAPI_IMAPIPROP_METHODS(IMPL);
    MAPI_IMAPISTATUS_METHODS(IMPL);
// Other methods specific to CMyMAPIObject.
    BOOL WINAPI Method1 ();
    void WINAPI Method2 ();
// Constructors and destructors.
public :
    CMyMAPIObject () {};
    ~CMyMAPIObject () {};
// Data members specific to CMyMAPIObject.
private :
    ULONG               m_cRef;
    CAnotherObj *       m_pObj;
};
 
```

Um eine Instanz der `CMyMAPIObject` Klasse zu verwenden, führen C++-Clients oder-Dienstanbieter einen Aufruf einer der folgenden Methoden aus: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

