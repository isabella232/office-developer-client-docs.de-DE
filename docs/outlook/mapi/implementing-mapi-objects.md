---
title: Implementieren von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d53304dd74a0e54974d479c66637079cd48b2fc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792554"
---
# <a name="implementing-mapi-objects"></a><span data-ttu-id="be223-103">Implementieren von MAPI-Objekten</span><span class="sxs-lookup"><span data-stu-id="be223-103">Implementing MAPI Objects</span></span>

  
  
<span data-ttu-id="be223-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be223-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be223-105">MAPI-Objekten mithilfe von C++-Klassen oder C-Datenstrukturen, abhängig von der Sprache implementiert werden können und die API Einrichten eines Clients oder -Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="be223-105">MAPI objects can be implemented by using C++ classes or C data structures, depending on the language and the API set a client or service provider is using.</span></span> <span data-ttu-id="be223-106">Dienstanbieter können mit der MAPI-Dienst in C oder C++ geschrieben werden. Clientanwendungen können auch C oder C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="be223-106">Service providers can be written in C or C++ with the MAPI service provider interface; client applications can also use C or C++.</span></span> <span data-ttu-id="be223-107">Wenn möglich, sollten Clients und -Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden C++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="be223-107">If possible, clients and service providers that use the object-oriented programming interface should use C++.</span></span> 
  
<span data-ttu-id="be223-108">C++ ist die erste Wahl, da MAPI eine objektorientierte Technologie ist und C++ sich besser für objektorientierte Entwicklung eignet.</span><span class="sxs-lookup"><span data-stu-id="be223-108">C++ is the preferred choice because MAPI is an object-oriented technology, and C++ lends itself more readily to object-oriented development.</span></span> <span data-ttu-id="be223-109">Der resultierende Code ist einfacher und einfacher, Wartung zu erleichtern.</span><span class="sxs-lookup"><span data-stu-id="be223-109">The resulting code is simpler and more straightforward, making it easier to maintain.</span></span> <span data-ttu-id="be223-110">Die MAPI-Dokumentation ist in erster Linie für C++-Entwickler geschrieben. Alle Syntax für die MAPI-Schnittstellenmethoden in dieser Referenz werden in C++.</span><span class="sxs-lookup"><span data-stu-id="be223-110">The MAPI documentation is written primarily for C++ developers; all of the syntax descriptions for the MAPI interface methods in this Reference are in C++.</span></span>
  
<span data-ttu-id="be223-111">Entwickler können Microsoft Visual Studio und Drittanbieter-Entwicklungstools zum Entwickeln von Lösungen, die MAPI-Aufruf.</span><span class="sxs-lookup"><span data-stu-id="be223-111">Developers can use Microsoft Visual Studio and third-party development tools to develop solutions that call MAPI.</span></span> <span data-ttu-id="be223-112">Beachten Sie, dass Entwickler sollten C oder nicht verwaltetem C++ verwenden, aber nicht C++ verwaltet um MAPI-Lösungen zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="be223-112">Note that developers should use C or unmanaged C++, but not managed C++ to write MAPI solutions.</span></span>
  
<span data-ttu-id="be223-113">Wenn ein MAPI-Objekt implementiert wird, wird ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für privaten Methoden, die speziell für die Implementierung und Code zur Unterstützung von private Datenmember zur Aufrechterhaltung von Statusinformationen erstellt.</span><span class="sxs-lookup"><span data-stu-id="be223-113">When a MAPI object is implemented, a client or service provider creates code for all of the interface methods, code for any private methods that are specific to the implementation, and code to support private data members for maintaining state information.</span></span> <span data-ttu-id="be223-114">Der Code für die Schnittstellenmethoden muss die Spezifikationen von MAPI befolgen, die Erwartetes Verhalten zu dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="be223-114">The code for the interface methods must follow the specifications published by MAPI that document expected behavior.</span></span> 
  
<span data-ttu-id="be223-115">Es gibt viele Makros in die Headerdatei Mapidefs.h und OLE-Headerdateien, mit denen Clients und -Dienstanbieter in beiden Sprachen können sie deren Definitionen von MAPI-Objekten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="be223-115">There are many macros in the Mapidefs.h header file and OLE header files that clients and service providers in either language can use to help them with their definitions of MAPI objects.</span></span> <span data-ttu-id="be223-116">Beispielsweise ist ein Makro so definieren Sie die Methoden des jeweils die MAPI-Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="be223-116">For example, there is a macro to define the methods of each of the MAPI interfaces.</span></span> <span data-ttu-id="be223-117">Das Makro so definieren Sie die Methoden für die [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle in Mapidefs.h wird wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="be223-117">The macro to define the methods of the [IUnknown](http://msdn.microsoft.com/de-de/library/ms680509%28v=VS.85%29.aspx) interface appears in Mapidefs.h as follows:</span></span> 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a><span data-ttu-id="be223-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be223-118">See also</span></span>



[<span data-ttu-id="be223-119">MAPI-Objekt und Übersicht über die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="be223-119">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

