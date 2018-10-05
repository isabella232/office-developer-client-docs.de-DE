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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397100"
---
# <a name="implementing-mapi-objects"></a>Implementieren von MAPI-Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Objekten mithilfe von C++-Klassen oder C-Datenstrukturen, abhängig von der Sprache implementiert werden können und die API Einrichten eines Clients oder -Dienstanbieter verwendet. Dienstanbieter können mit der MAPI-Dienst in C oder C++ geschrieben werden. Clientanwendungen können auch C oder C++ verwenden. Wenn möglich, sollten Clients und -Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden C++ verwenden. 
  
C++ ist die erste Wahl, da MAPI eine objektorientierte Technologie ist und C++ sich besser für objektorientierte Entwicklung eignet. Der resultierende Code ist einfacher und einfacher, Wartung zu erleichtern. Die MAPI-Dokumentation ist in erster Linie für C++-Entwickler geschrieben. Alle Syntax für die MAPI-Schnittstellenmethoden in dieser Referenz werden in C++.
  
Entwickler können Microsoft Visual Studio und Drittanbieter-Entwicklungstools zum Entwickeln von Lösungen, die MAPI-Aufruf. Beachten Sie, dass Entwickler sollten C oder nicht verwaltetem C++ verwenden, aber nicht C++ verwaltet um MAPI-Lösungen zu schreiben.
  
Wenn ein MAPI-Objekt implementiert wird, wird ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für privaten Methoden, die speziell für die Implementierung und Code zur Unterstützung von private Datenmember zur Aufrechterhaltung von Statusinformationen erstellt. Der Code für die Schnittstellenmethoden muss die Spezifikationen von MAPI befolgen, die Erwartetes Verhalten zu dokumentieren. 
  
Es gibt viele Makros in die Headerdatei Mapidefs.h und OLE-Headerdateien, mit denen Clients und -Dienstanbieter in beiden Sprachen können sie deren Definitionen von MAPI-Objekten zu unterstützen. Beispielsweise ist ein Makro so definieren Sie die Methoden des jeweils die MAPI-Schnittstellen. Das Makro so definieren Sie die Methoden für die [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle in Mapidefs.h wird wie folgt angezeigt: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Siehe auch



[MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

