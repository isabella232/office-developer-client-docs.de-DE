---
title: Implementieren von Objekten in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b471dc260731aedc3b97a134a0facee1ef7471e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579884"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C++

**Gilt für**: Outlook 2013 | Outlook 2016 
  
C++-Clients und Dienstanbieter definieren MAPI-Objekte, indem Klassen erstellt werden, die von den von ihnen implementierten Schnittstellen erben. Jede der Schnittstellenmethoden ist öffentlich, ebenso wie der Konstruktor und destruktor für die Klasse. Wenn die Klasse über zusätzliche Methoden verfügt, können sie je nach Implementierung öffentlich oder privat sein. Alle Datenmember sind privat. 
  
Der folgende Beispielcode zeigt, wie Sie ein C++-Statusobjekt definieren. Die `CMyMAPIObject` Klasse erbt von der [IMAPIStatus : IMAPIProp-Schnittstelle.](imapistatusimapiprop.md) Viele der in diesem Beispiel verwendeten Makros sind in der OLE-Headerdatei Compobj.h definiert. Die ersten Member der Klasse sind die Methoden der Basisschnittstelle, gefolgt von den Methoden der geerbten Schnittstellen in der Reihenfolge der Vererbung. Im Anschluss an die Schnittstellendefinitionen sind alle zusätzlichen Methoden, der Konstruktor und destruktor sowie die Datenmember aufgeführt. 
  
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

Um eine Instanz der  `CMyMAPIObject` Klasse zu verwenden, rufen C++-Clients oder Dienstanbieter eine der folgenden Methoden auf: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

