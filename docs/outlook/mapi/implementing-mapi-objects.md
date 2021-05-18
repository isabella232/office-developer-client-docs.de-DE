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
# <a name="implementing-mapi-objects"></a>Implementieren von MAPI-Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
#A0 können mithilfe von C++-Klassen oder C-Datenstrukturen implementiert werden, abhängig von der Sprache und dem API-Satz, den ein Client oder Dienstanbieter verwendet. Dienstanbieter können in C oder C++ mit der #A0 geschrieben werden. Clientanwendungen können auch C oder C++ verwenden. Wenn möglich, sollten Clients und Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden, C++ verwenden. 
  
C++ ist die bevorzugte Wahl, da MAPI eine objektorientierte Technologie ist und C++ sich leichter für objektorientierte Entwicklung eignet. Der resultierende Code ist einfacher und einfacher, was die Wartung vereinfacht. Die #A0 ist in erster Linie für C++-Entwickler geschrieben. Alle Syntaxbeschreibungen für die #A0 in dieser Referenz befinden sich in C++.
  
Entwickler können Microsoft Visual Studio Und Drittanbieter-Entwicklungstools verwenden, um Lösungen zu entwickeln, die MAPI aufrufen. Beachten Sie, dass Entwickler C oder nicht verwaltetes C++ verwenden sollten, aber nicht verwaltetes C++ zum Schreiben von #A0 verwenden sollten.
  
Wenn ein MAPI-Objekt implementiert wird, erstellt ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für alle privaten Methoden, die für die Implementierung spezifisch sind, und Code zur Unterstützung privater Datenm member für die Verwaltung von Statusinformationen. Der Code für die Schnittstellenmethoden muss den von MAPI veröffentlichten Spezifikationen entsprechen, die das erwartete Verhalten dokumentieren. 
  
Die Headerdatei Mapidefs.h und die OLE-Headerdateien enthalten viele Makros, die Clients und Dienstanbieter in beiden Sprachen verwenden können, um sie bei ihren Definitionen von MAPI-Objekten zu unterstützen. Beispielsweise gibt es ein Makro, um die Methoden der einzelnen MAPI-Schnittstellen zu definieren. Das Makro zum Definieren der Methoden der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) wird in Mapidefs.h wie folgt angezeigt: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Siehe auch



[Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

