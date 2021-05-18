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
# <a name="implementing-mapi-objects"></a><span data-ttu-id="15441-103">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="15441-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="15441-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15441-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15441-105">#A0 können mithilfe von C++-Klassen oder C-Datenstrukturen implementiert werden, abhängig von der Sprache und dem API-Satz, den ein Client oder Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="15441-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="15441-106">Dienstanbieter können in C oder C++ mit der #A0 geschrieben werden. Clientanwendungen können auch C oder C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="15441-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="15441-107">Wenn möglich, sollten Clients und Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden, C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="15441-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="15441-108">C++ ist die bevorzugte Wahl, da MAPI eine objektorientierte Technologie ist und C++ sich leichter für objektorientierte Entwicklung eignet.</span><span class="sxs-lookup"><span data-stu-id="15441-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="15441-109">Der resultierende Code ist einfacher und einfacher, was die Wartung vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="15441-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="15441-110">Die #A0 ist in erster Linie für C++-Entwickler geschrieben. Alle Syntaxbeschreibungen für die #A0 in dieser Referenz befinden sich in C++.</span><span class="sxs-lookup"><span data-stu-id="15441-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="15441-111">Entwickler können Microsoft Visual Studio Und Drittanbieter-Entwicklungstools verwenden, um Lösungen zu entwickeln, die MAPI aufrufen.</span><span class="sxs-lookup"><span data-stu-id="15441-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="15441-112">Beachten Sie, dass Entwickler C oder nicht verwaltetes C++ verwenden sollten, aber nicht verwaltetes C++ zum Schreiben von #A0 verwenden sollten.</span><span class="sxs-lookup"><span data-stu-id="15441-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="15441-113">Wenn ein MAPI-Objekt implementiert wird, erstellt ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für alle privaten Methoden, die für die Implementierung spezifisch sind, und Code zur Unterstützung privater Datenm member für die Verwaltung von Statusinformationen.</span><span class="sxs-lookup"><span data-stu-id="15441-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="15441-114">Der Code für die Schnittstellenmethoden muss den von MAPI veröffentlichten Spezifikationen entsprechen, die das erwartete Verhalten dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="15441-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="15441-115">Die Headerdatei Mapidefs.h und die OLE-Headerdateien enthalten viele Makros, die Clients und Dienstanbieter in beiden Sprachen verwenden können, um sie bei ihren Definitionen von MAPI-Objekten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="15441-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="15441-116">Beispielsweise gibt es ein Makro, um die Methoden der einzelnen MAPI-Schnittstellen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="15441-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="15441-117">Das Makro zum Definieren der Methoden der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) wird in Mapidefs.h wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="15441-117">The macro to define the methods of the [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="15441-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15441-118">See also</span></span>



[<span data-ttu-id="15441-119">Übersicht über das MAPI-Objekt und die Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="15441-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

