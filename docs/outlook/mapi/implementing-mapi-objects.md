---
title: Implementieren von MAPI-Objekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: b1ee2533-8077-4976-846b-d42d148bf8c6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 64ea298fc078e2848093182bce2bf85f9b3bfc23
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584255"
---
# <a name="implementing-mapi-objects"></a>Implementieren von MAPI-Objekten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI-Objekte können mithilfe von C++-Klassen oder C-Datenstrukturen implementiert werden, abhängig von der Sprache und dem API-Satz, den ein Client oder Dienstanbieter verwendet. Dienstanbieter können in C oder C++ mit der MAPI-Dienstanbieterschnittstelle geschrieben werden. Clientanwendungen können auch C oder C++ verwenden. Clients und Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden, sollten nach Möglichkeit C++ verwenden. 
  
C++ ist die bevorzugte Wahl, da MAPI eine objektorientierte Technologie ist und sich C++ für die objektorientierte Entwicklung eignet. Der resultierende Code ist einfacher und einfacher, sodass er einfacher verwaltet werden kann. Die MAPI-Dokumentation ist in erster Linie für C++-Entwickler geschrieben. Alle Syntaxbeschreibungen für die MAPI-Schnittstellenmethoden in dieser Referenz befinden sich in C++.
  
Entwickler können Microsoft Visual Studio und Entwicklungstools von Drittanbietern verwenden, um Lösungen zu entwickeln, die MAPI aufrufen. Beachten Sie, dass Entwickler C oder nicht verwaltetes C++ verwenden sollten, aber nicht verwaltetes C++ zum Schreiben von MAPI-Lösungen.
  
Wenn ein MAPI-Objekt implementiert wird, erstellt ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für alle privaten Methoden, die für die Implementierung spezifisch sind, und Code zur Unterstützung privater Datenmember zum Verwalten von Statusinformationen. Der Code für die Schnittstellenmethoden muss den von mapi veröffentlichten Spezifikationen entsprechen, die das erwartete Verhalten dokumentieren. 
  
Es gibt viele Makros in der Mapidefs.h-Headerdatei und OLE-Headerdateien, die Clients und Dienstanbieter in beiden Sprachen verwenden können, um sie bei ihren Definitionen von MAPI-Objekten zu unterstützen. Beispielsweise gibt es ein Makro, um die Methoden der einzelnen MAPI-Schnittstellen zu definieren. Das Makro zum Definieren der Methoden der [IUnknown-Schnittstelle](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) wird in Mapidefs.h wie folgt angezeigt: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Siehe auch



[Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

