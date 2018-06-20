---
title: Implementieren ein Beispielobjekt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 85de8dd7211fa19b7cdbda9f5ced1f00a736ca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792536"
---
# <a name="implementing-a-sample-object"></a>Implementieren ein Beispielobjekt

**Betrifft**: Outlook 
  
Beraten der Empfängerobjekten – Objekte, die das unterstützen die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle – MAPI-Objekten, die Clientanwendungen für die Verarbeitung von Benachrichtigungen implementiert werden. **IMAPIAdviseSink** erbt direkt von [IUnknown](http://msdn.microsoft.com/en-us/library/ms680509%28v=VS.85%29.aspx) und enthält nur eine Methode, **OnNotify**. Aus diesem Grund wird ein Client zum Implementieren einer Advise-Empfängerobjekt Code für die drei Methoden in **IUnknown** und [OnNotify](imapiadvisesink-onnotify.md)erstellt.
  
Die Headerdatei Mapidefs.h definiert eine **IMAPIAdviseSink** Implementierung mit **DECLARE_MAPI_INTERFACE**, wie folgt:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Clients, die implementiert werden ausschließlich Empfängerobjekten ihre Schnittstellen in ihre Objekte manuell oder mit den Makros **MAPI_IUNKNOWN_METHODS** und **MAPI_IMAPIADVISESINK_METHODS** definieren können. Objekt Implementierer sollten die Schnittstelle Makros immer möglich, Objekte Konsistenz sicherzustellen und die Zeit und Mühe sparen verwenden. 
  
Die [IUnknown:: AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) und [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) -Methoden implementieren ist relativ einfach, da nur ein paar Codezeilen in der Regel benötigt werden. Aus diesem Grund können Clients und Dienstanbieter, die Objekte implementieren ihrer **AddRef** und **Release** Implementierungen Inline tätigen. Der folgende Code zeigt, wie Sie eine C++ definieren advise-Empfängerobjekt mit Inline Implementierungen von **AddRef** und **Release**.
  
```cpp
class  CMAPIAdviseSink : public IMAPIAdviseSink
{
public:
    STDMETHODIMP QueryInterface
                    (REFIID                     riid,
                     LPVOID *                   ppvObj);
    inline STDMETHODIMP_(ULONG) AddRef
                    () { InterlockedIncrement(m_cRef);
                         ++m_cRef;
                         InterlockedDecrement(m_cRef);
                         return m_cRef; };
    inline STDMETHODIMP_(ULONG) Release
                    () { InterlockedIncrement(m_cRef);
                         ULONG ulCount = --m_cRef;
                         InterlockedDecrement(m_cRef);
                         if (!ulCount)  delete this;
                         return ulCount;};
    MAPI_IMAPIADVISESINK_METHODS(IMPL);
    BOOL WINAPI AddConnection (LPMDB pMDBObj, ULONG ulConnection);
    void WINAPI RemoveAllLinks (LPMDB pMDBObj);
// Constructors and destructors.
public :
    inline CMAPIAdviseSink  (CStoreClient * pStore)
                            { m_cRef = 1;
                              m_ulConnection = 0;
                              m_pStore = pStore;
                              AddRef;};
    ~CMAPIAdviseSink () {Release};
private :
    ULONG               m_cRef;
    CStoreClient *      m_pStore;
    ULONG               m_ulConnection;
};
 
```

In C besteht das Advise-Empfängerobjekt die folgenden Elemente:
  
- Ein Zeiger auf eine virtuelle Tabelle, die Zeiger auf die Implementierung von Methoden in **IUnknown** und **IMAPIAdviseSink**enthält.
    
- Datenelemente.
    
Im folgenden Codebeispiel wird veranschaulicht, wie ein Advise-Empfängerobjekt in C# definieren und erstellen die vtable des Objekts. 
  
```cpp
// Object definition.
typedef struct _ADVISESINK
{
    const ADVISE_Vtbl FAR *    lpVtbl;
    ULONG             cRef;
    STORECLIENT      *pStore;
    ULONG             ulConnection;
} ADVISESINK, *LPADVISESINK;
// vtable definition.
static const ADVISE_Vtbl vtblADVISE =
{
    ADVISE_QueryInterface,
    ADVISE_AddRef,
    ADVISE_Release,
    ADVISE_OnNotify
};
 
```

Nachdem Sie ein Objekt im C deklarieren, müssen Sie es initialisieren durch Festlegen des Vtable-Zeigers auf die Adresse des organisierten Vtable wie im folgenden Code dargestellt:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Siehe auch

- [�bersicht �ber die MAPI-Eigenschaft](mapi-property-overview.md)
- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

