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
# <a name="implementing-a-sample-object"></a><span data-ttu-id="a0bbd-103">Implementieren ein Beispielobjekt</span><span class="sxs-lookup"><span data-stu-id="a0bbd-103">Implementing a sample object</span></span>

<span data-ttu-id="a0bbd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0bbd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0bbd-105">Beraten der Empfängerobjekten – Objekte, die das unterstützen die [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md) Schnittstelle – MAPI-Objekten, die Clientanwendungen für die Verarbeitung von Benachrichtigungen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-105">Advise sink objects — objects that support the [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md) interface — are MAPI objects that client applications implement for processing notifications.</span></span> <span data-ttu-id="a0bbd-106">**IMAPIAdviseSink** erbt direkt von [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) und enthält nur eine Methode, **OnNotify**.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-106">**IMAPIAdviseSink** inherits directly from [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) and contains only one method, **OnNotify**.</span></span> <span data-ttu-id="a0bbd-107">Aus diesem Grund wird ein Client zum Implementieren einer Advise-Empfängerobjekt Code für die drei Methoden in **IUnknown** und [OnNotify](imapiadvisesink-onnotify.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-107">Therefore, to implement an advise sink object, a client creates code for the three methods in **IUnknown** and for [OnNotify](imapiadvisesink-onnotify.md).</span></span>
  
<span data-ttu-id="a0bbd-108">Die Headerdatei Mapidefs.h definiert eine **IMAPIAdviseSink** Implementierung mit **DECLARE_MAPI_INTERFACE**, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a0bbd-108">The Mapidefs.h header file defines an **IMAPIAdviseSink** interface implementation by using **DECLARE_MAPI_INTERFACE**, as follows:</span></span>
  
```cpp
#define      INTERFACE  IMAPIAdviseSink
DECLARE_MAPI_INTERFACE_(IMAPIAdviseSink, IUnknown)
{
    BEGIN_INTERFACE
    MAPI_IUNKNOWN_METHODS(PURE)
    MAPI_IMAPIADVISESINK_METHODS(PURE)
};
 
```

<span data-ttu-id="a0bbd-109">Clients, die implementiert werden ausschließlich Empfängerobjekten ihre Schnittstellen in ihre Objekte manuell oder mit den Makros **MAPI_IUNKNOWN_METHODS** und **MAPI_IMAPIADVISESINK_METHODS** definieren können.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-109">Clients that implement advise sink objects can define their interfaces in their objects manually or with the **MAPI_IUNKNOWN_METHODS** and **MAPI_IMAPIADVISESINK_METHODS** macros.</span></span> <span data-ttu-id="a0bbd-110">Objekt Implementierer sollten die Schnittstelle Makros immer möglich, Objekte Konsistenz sicherzustellen und die Zeit und Mühe sparen verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-110">Object implementers should use the interface macros whenever possible to ensure consistency across objects and to save time and effort.</span></span> 
  
<span data-ttu-id="a0bbd-111">Die [IUnknown:: AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) und [IUnknown](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) -Methoden implementieren ist relativ einfach, da nur ein paar Codezeilen in der Regel benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-111">Implementing the [IUnknown::AddRef](http://msdn.microsoft.com/de-de/library/ms691379%28v=VS.85%29.aspx) and [IUnknown::Release](http://msdn.microsoft.com/de-de/library/ms682317%28v=VS.85%29.aspx) methods is relatively simple because typically only a few lines of code are needed.</span></span> <span data-ttu-id="a0bbd-112">Aus diesem Grund können Clients und Dienstanbieter, die Objekte implementieren ihrer **AddRef** und **Release** Implementierungen Inline tätigen.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-112">Therefore, clients and service providers that implement objects can make their **AddRef** and **Release** implementations inline.</span></span> <span data-ttu-id="a0bbd-113">Der folgende Code zeigt, wie Sie eine C++ definieren advise-Empfängerobjekt mit Inline Implementierungen von **AddRef** und **Release**.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-113">The following code shows how to define a C++ advise sink object with inline implementations of **AddRef** and **Release**.</span></span>
  
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

<span data-ttu-id="a0bbd-114">In C besteht das Advise-Empfängerobjekt die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="a0bbd-114">In C, the advise sink object is composed of the following elements:</span></span>
  
- <span data-ttu-id="a0bbd-115">Ein Zeiger auf eine virtuelle Tabelle, die Zeiger auf die Implementierung von Methoden in **IUnknown** und **IMAPIAdviseSink**enthält.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-115">A pointer to a vtable that contains pointers to implementations of each of the methods in **IUnknown** and **IMAPIAdviseSink**.</span></span>
    
- <span data-ttu-id="a0bbd-116">Datenelemente.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-116">Data members.</span></span>
    
<span data-ttu-id="a0bbd-117">Im folgenden Codebeispiel wird veranschaulicht, wie ein Advise-Empfängerobjekt in C# definieren und erstellen die vtable des Objekts.</span><span class="sxs-lookup"><span data-stu-id="a0bbd-117">The following code example shows how to define an advise sink object in C and construct its vtable.</span></span> 
  
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

<span data-ttu-id="a0bbd-118">Nachdem Sie ein Objekt im C deklarieren, müssen Sie es initialisieren durch Festlegen des Vtable-Zeigers auf die Adresse des organisierten Vtable wie im folgenden Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="a0bbd-118">After you declare an object in C, you must initialize it by setting the vtable pointer to the address of the constructed vtable, as shown in the following code:</span></span>
  
```cpp
LPADVISESINK lpMyObj = NULL;
HRESULT hr = (*lpAllocateBuffer) (sizeof(ADVISESINK),
                 (LPVOID *)&lpMyObj);
lpMyObj->lpVtbl = &vtblADVISE;
 
```

## <a name="see-also"></a><span data-ttu-id="a0bbd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0bbd-119">See also</span></span>

- [<span data-ttu-id="a0bbd-120">�bersicht �ber die MAPI-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a0bbd-120">MAPI Property Overview</span></span>](mapi-property-overview.md)
- [<span data-ttu-id="a0bbd-121">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="a0bbd-121">Implementing MAPI Objects</span></span>](implementing-mapi-objects.md)

