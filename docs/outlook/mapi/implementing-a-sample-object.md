---
title: Implementieren eines Beispielsobjekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a681e68c0718e49da331946d75ecb7b4fab7afe2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332830"
---
# <a name="implementing-a-sample-object"></a>Implementieren eines Beispielsobjekts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Advise-Empfängerobjekte – Objekte, die die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle unterstützen, sind MAPI-Objekte, die von Clientanwendungen für Verarbeitungs Benachrichtigungen implementiert werden. **IMAPIAdviseSink** erbt direkt von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) und enthält nur eine Methode, OnNotify. **** Daher erstellt ein Client für die Implementierung eines Advise-Senke-Objekts Code für die drei Methoden in **IUnknown** und für OnNotify. [](imapiadvisesink-onnotify.md)
  
Die Headerdatei Mapidefs. h definiert eine **IMAPIAdviseSink** -Schnittstellenimplementierung mithilfe von **DECLARE_MAPI_INTERFACE**wie folgt:
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Clients, die Advise-Senke-Objekte implementieren, können Ihre Schnittstellen in ihren Objekten manuell oder mit den **MAPI_IUNKNOWN_METHODS** -und **MAPI_IMAPIADVISESINK_METHODS** -Makros definieren. Objekt Implementierer sollten die Schnittstellen Makros immer dann verwenden, um die Konsistenz zwischen Objekten sicherzustellen und Zeit und Aufwand zu sparen. 
  
Das Implementieren der [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -und [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methoden ist relativ einfach, da in der Regel nur wenige Codezeilen benötigt werden. Daher können Clients und Dienstanbieter, die Objekte implementieren, Ihre **AddRef** -und **Release** -Implementierungen Inline machen. Mit dem folgenden Code wird gezeigt, wie ein C++ Advise-Senke-Objekt mit Inline Implementierungen von **AddRef** und **Release**definiert wird.
  
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

In C besteht das Advise-Senke-Objekt aus den folgenden Elementen:
  
- Ein Zeiger auf eine Vtable, die Zeiger auf Implementierungen der einzelnen Methoden in **IUnknown** und **IMAPIAdviseSink**enthält.
    
- Datenmember.
    
Im folgenden Codebeispiel wird gezeigt, wie Sie ein Advise-Senke-Objekt in C definieren und dessen Vtable erstellen. 
  
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

Nachdem Sie ein Objekt in C deklariert haben, müssen Sie es initialisieren, indem Sie den vtable-Zeiger auf die Adresse der erstellten Vtable festlegen, wie im folgenden Code dargestellt:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)
- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

