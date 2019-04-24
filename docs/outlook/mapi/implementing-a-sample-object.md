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
# <a name="implementing-a-sample-object"></a><span data-ttu-id="21a75-103">Implementieren eines Beispielsobjekts</span><span class="sxs-lookup"><span data-stu-id="21a75-103">Implementing a sample object</span></span>

<span data-ttu-id="21a75-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21a75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21a75-105">Advise-Empfängerobjekte – Objekte, die die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) -Schnittstelle unterstützen, sind MAPI-Objekte, die von Clientanwendungen für Verarbeitungs Benachrichtigungen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="21a75-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="21a75-106">**IMAPIAdviseSink** erbt direkt von [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) und enthält nur eine Methode, OnNotify. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="21a75-106">**IMAPIAdviseSink** inherits directly from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="21a75-107">Daher erstellt ein Client für die Implementierung eines Advise-Senke-Objekts Code für die drei Methoden in **IUnknown** und für OnNotify. [](imapiadvisesink-onnotify.md)</span><span class="sxs-lookup"><span data-stu-id="21a75-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="21a75-108">Die Headerdatei Mapidefs. h definiert eine **IMAPIAdviseSink** -Schnittstellenimplementierung mithilfe von **DECLARE_MAPI_INTERFACE**wie folgt:</span><span class="sxs-lookup"><span data-stu-id="21a75-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="21a75-109">Clients, die Advise-Senke-Objekte implementieren, können Ihre Schnittstellen in ihren Objekten manuell oder mit den **MAPI_IUNKNOWN_METHODS** -und **MAPI_IMAPIADVISESINK_METHODS** -Makros definieren.</span><span class="sxs-lookup"><span data-stu-id="21a75-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="21a75-110">Objekt Implementierer sollten die Schnittstellen Makros immer dann verwenden, um die Konsistenz zwischen Objekten sicherzustellen und Zeit und Aufwand zu sparen.</span><span class="sxs-lookup"><span data-stu-id="21a75-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="21a75-111">Das Implementieren der [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) -und [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) -Methoden ist relativ einfach, da in der Regel nur wenige Codezeilen benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="21a75-111">Implementing the [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="21a75-112">Daher können Clients und Dienstanbieter, die Objekte implementieren, Ihre **AddRef** -und **Release** -Implementierungen Inline machen.</span><span class="sxs-lookup"><span data-stu-id="21a75-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="21a75-113">Mit dem folgenden Code wird gezeigt, wie ein C++ Advise-Senke-Objekt mit Inline Implementierungen von **AddRef** und **Release**definiert wird.</span><span class="sxs-lookup"><span data-stu-id="21a75-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="21a75-114">In C besteht das Advise-Senke-Objekt aus den folgenden Elementen:</span><span class="sxs-lookup"><span data-stu-id="21a75-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="21a75-115">Ein Zeiger auf eine Vtable, die Zeiger auf Implementierungen der einzelnen Methoden in **IUnknown** und **IMAPIAdviseSink**enthält.</span><span class="sxs-lookup"><span data-stu-id="21a75-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="21a75-116">Datenmember.</span><span class="sxs-lookup"><span data-stu-id="21a75-116">Data members.</span></span>
    
<span data-ttu-id="21a75-117">Im folgenden Codebeispiel wird gezeigt, wie Sie ein Advise-Senke-Objekt in C definieren und dessen Vtable erstellen.</span><span class="sxs-lookup"><span data-stu-id="21a75-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="21a75-118">Nachdem Sie ein Objekt in C deklariert haben, müssen Sie es initialisieren, indem Sie den vtable-Zeiger auf die Adresse der erstellten Vtable festlegen, wie im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="21a75-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="21a75-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21a75-119">See also</span></span>

- [<span data-ttu-id="21a75-120">Übersicht über die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="21a75-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="21a75-121">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="21a75-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

