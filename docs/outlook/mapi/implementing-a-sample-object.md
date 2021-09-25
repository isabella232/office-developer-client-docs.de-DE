---
title: Implementieren eines Beispielsobjekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 23b6ad1a-0b50-429f-8819-ab72c56581c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8f2613dae143de41276e105a32a0d504aeb5b886
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551261"
---
# <a name="implementing-a-sample-object"></a>Implementieren eines Beispielsobjekts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Empfehlen Sie Senkenobjekte – Objekte, die die [IMAPIAdviseSink : IUnknown-Schnittstelle](imapiadvisesinkiunknown.md) unterstützen – sind MAPI-Objekte, die Clientanwendungen für die Verarbeitung von Benachrichtigungen implementieren. **IMAPIAdviseSink** erbt direkt von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) und enthält nur eine Methode, **OnNotify**. Um daher ein Empfehlungssenkenobjekt zu implementieren, erstellt ein Client Code für die drei Methoden in **IUnknown** und für [OnNotify](imapiadvisesink-onnotify.md).
  
Die Headerdatei Mapidefs.h definiert wie folgt eine **IMAPIAdviseSink-Schnittstellenimplementierungen** mithilfe **von DECLARE_MAPI_INTERFACE:**
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

Clients, die Empfehlungssenkenobjekte implementieren, können ihre Schnittstellen in ihren Objekten manuell oder mit den **Makros MAPI_IUNKNOWN_METHODS** und **MAPI_IMAPIADVISESINK_METHODS** definieren. Objektimplementierer sollten die Schnittstellenmakros nach Möglichkeit verwenden, um die Konsistenz zwischen Objekten sicherzustellen und Zeit und Mühe zu sparen. 
  
Die Implementierung der Methoden [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) und [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) ist relativ einfach, da in der Regel nur wenige Codezeilen erforderlich sind. Daher können Clients und Dienstanbieter, die Objekte implementieren, ihre **AddRef-** und **Release-Implementierungen** inline machen. Der folgende Code zeigt, wie Sie ein C++-Empfehlungssenkenobjekt mit Inlineimplementierungen von **AddRef** und **Release** definieren.
  
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

In C besteht das "advise"-Senkenobjekt aus den folgenden Elementen:
  
- Ein Zeiger auf eine vtable, die Zeiger auf Implementierungen der einzelnen Methoden in **IUnknown** und **IMAPIAdviseSink** enthält.
    
- Datenmember.
    
Das folgende Codebeispiel zeigt, wie Sie ein "advise"-Senkenobjekt in C definieren und dessen vtable erstellen. 
  
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

Nachdem Sie ein Objekt in C deklariert haben, müssen Sie es initialisieren, indem Sie den vtable-Zeiger auf die Adresse der konstruierten vtable festlegen, wie im folgenden Code gezeigt:
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)
- [Implementieren von MAPI-Objekten](implementing-mapi-objects.md)

