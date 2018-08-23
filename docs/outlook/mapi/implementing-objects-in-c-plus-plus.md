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
ms.openlocfilehash: 4c233f9855674080496b2e54ba9548a53738ead8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574727"
---
# <a name="implementing-objects-in-c"></a>Implementieren von Objekten in C++

**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

