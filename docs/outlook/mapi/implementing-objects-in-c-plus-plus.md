---
title: Implementieren von Objekten in C++
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d1a050ff-3cf9-4bf7-812d-b7c1b31056e7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea9f37183f33459b09f2730b3efbb7afed3d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792560"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C++

**Betrifft**: Outlook 
  
C++-Clients und -Dienstanbieter definieren MAPI-Objekten durch Erstellen von Klassen, die von den Schnittstellen erben, die sie implementiert werden. Jede-Schnittstellenmethoden ist öffentlich, wie der Konstruktor und der Destruktor für die Klasse sind. Wenn die Klasse zusätzliche Methoden verfügt, können sie öffentliche oder private, je nach der Implementierung werden. Alle Datenmember sind privat. 
  
Das folgende Codebeispiel veranschaulicht, wie ein C++ Status-Objekt definieren. Die `CMyMAPIObject` Klasse erbt von der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Schnittstelle. Viele der in diesem Beispiel verwendete Makros werden in der OLE-Headerdatei Compobj.h definiert. Der erste Member der Klasse sind die Methoden für die Basis-Schnittstelle, gefolgt von den Methoden der geerbten Schnittstellen in der Reihenfolge der Vererbung. Befolgen die Schnittstellendefinitionen sind zusätzlichen Methoden, den Konstruktor und Destruktor und die Datenelemente. 
  
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

Verwenden Sie eine Instanz der `CMyMAPIObject` -Klasse, C++-Clients oder Dienstanbieter rufen Sie eine seiner Methoden wie folgt: 
  
```cpp
lpMyObj->ValidateState(ulUIParam, ulFlags);

```

## <a name="see-also"></a>Siehe auch

- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

