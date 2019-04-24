---
title: Implementieren von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0d67d10d54591de926724cbf594a44f17e9ea14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310171"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="627aa-103">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="627aa-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="627aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="627aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="627aa-105">MAPI-Objekte können mithilfe von C++-Klassen oder C-Datenstrukturen implementiert werden, je nach Sprache und API-Satz, den ein Client oder Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="627aa-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="627aa-106">Dienstanbieter können in C oder C++ mit der MAPI-Dienstanbieter-Schnittstelle geschrieben werden. Clientanwendungen können auch C oder C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="627aa-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="627aa-107">Wenn möglich, sollten Clients und Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden, C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="627aa-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="627aa-108">C++ ist die bevorzugte Wahl, da MAPI eine objektorientierte Technologie ist und sich C++ leichter zur objektorientierten Entwicklung eignet.</span><span class="sxs-lookup"><span data-stu-id="627aa-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="627aa-109">Der resultierende Code ist einfacher und einfacher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="627aa-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="627aa-110">Die MAPI-Dokumentation wurde in erster Linie für C++-Entwickler geschrieben; Alle Syntaxbeschreibungen für die MAPI-Schnittstellenmethoden in diesem Verweis befinden sich in C++.</span><span class="sxs-lookup"><span data-stu-id="627aa-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="627aa-111">Entwickler können Microsoft Visual Studio und Drittanbieter-Entwicklungstools verwenden, um Lösungen zu entwickeln, die MAPI aufrufen.</span><span class="sxs-lookup"><span data-stu-id="627aa-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="627aa-112">Beachten Sie, dass Entwickler C oder nicht verwaltete C++, aber nicht verwalteten C++ verwenden sollten, um MAPI-Lösungen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="627aa-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="627aa-113">Wenn ein MAPI-Objekt implementiert wird, erstellt ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für alle privaten Methoden, die für die Implementierung spezifisch sind, und Code zur Unterstützung privater Datenmember für die Verwaltung von Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="627aa-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="627aa-114">Der Code für die Schnittstellenmethoden muss den von MAPI veröffentlichten Spezifikationen entsprechen, die das erwartete Verhalten dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="627aa-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="627aa-115">Es gibt viele Makros in der Headerdatei Mapidefs. h und OLE-Headerdateien, die von Clients und Dienstanbietern in beiden Sprachen verwendet werden können, um Sie bei der Definition von MAPI-Objekten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="627aa-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="627aa-116">Beispielsweise gibt es ein Makro, um die Methoden der einzelnen MAPI-Schnittstellen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="627aa-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="627aa-117">Das Makro zum Definieren der Methoden der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle wird in Mapidefs. h wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="627aa-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="627aa-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="627aa-118">See also</span></span>



[<span data-ttu-id="627aa-119">Übersicht über MAPI-Objekte und-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="627aa-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

