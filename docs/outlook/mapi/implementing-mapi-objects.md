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
  
MAPI-Objekte können mithilfe von C++-Klassen oder C-Datenstrukturen implementiert werden, je nach Sprache und API-Satz, den ein Client oder Dienstanbieter verwendet. Dienstanbieter können in C oder C++ mit der MAPI-Dienstanbieter-Schnittstelle geschrieben werden. Clientanwendungen können auch C oder C++ verwenden. Wenn möglich, sollten Clients und Dienstanbieter, die die objektorientierte Programmierschnittstelle verwenden, C++ verwenden. 
  
C++ ist die bevorzugte Wahl, da MAPI eine objektorientierte Technologie ist und sich C++ leichter zur objektorientierten Entwicklung eignet. Der resultierende Code ist einfacher und einfacher zu verwalten. Die MAPI-Dokumentation wurde in erster Linie für C++-Entwickler geschrieben; Alle Syntaxbeschreibungen für die MAPI-Schnittstellenmethoden in diesem Verweis befinden sich in C++.
  
Entwickler können Microsoft Visual Studio und Drittanbieter-Entwicklungstools verwenden, um Lösungen zu entwickeln, die MAPI aufrufen. Beachten Sie, dass Entwickler C oder nicht verwaltete C++, aber nicht verwalteten C++ verwenden sollten, um MAPI-Lösungen zu schreiben.
  
Wenn ein MAPI-Objekt implementiert wird, erstellt ein Client oder Dienstanbieter Code für alle Schnittstellenmethoden, Code für alle privaten Methoden, die für die Implementierung spezifisch sind, und Code zur Unterstützung privater Datenmember für die Verwaltung von Statusinformationen. Der Code für die Schnittstellenmethoden muss den von MAPI veröffentlichten Spezifikationen entsprechen, die das erwartete Verhalten dokumentieren. 
  
Es gibt viele Makros in der Headerdatei Mapidefs. h und OLE-Headerdateien, die von Clients und Dienstanbietern in beiden Sprachen verwendet werden können, um Sie bei der Definition von MAPI-Objekten zu unterstützen. Beispielsweise gibt es ein Makro, um die Methoden der einzelnen MAPI-Schnittstellen zu definieren. Das Makro zum Definieren der Methoden der [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) -Schnittstelle wird in Mapidefs. h wie folgt angezeigt: 
  
```cpp
#define MAPI_IUNKNOWN_METHODS(IPURE)          \
    MAPIMETHOD(QueryInterface)                \
        (THIS_ REFIID riid, LPVOID FAR * ppvObj) IPURE;    \
    MAPIMETHOD_(ULONG,AddRef)  (THIS) IPURE;               \
    MAPIMETHOD_(ULONG,Release) (THIS) IPURE;   \
 
```

## <a name="see-also"></a>Siehe auch



[Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

