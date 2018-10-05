---
title: Objekte und die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391040"
---
# <a name="objects-and-the-mapi-architecture"></a>Objekte und die MAPI-Architektur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Objekte, die MAPI definiert fallen in eine oder mehrere Ebenen in der MAPI-Architektur. Die Ebene der Client-Schnittstelle enthält alle Objekte, die eine Clientanwendung, Formular Viewer oder Formular Server implementieren können. Die Service Provider-Schnittstellenebene enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren können. Diese Schicht umfasst Objekte, die von Adressbüchern, Nachrichtenspeicher, Transportanbieter und Formularbibliotheken implementiert. Die Ebene, die das MAPI-Subsystem steht, wird zwischen dem Client und Dienst Anbieter Benutzeroberflächenebenen positioniert. Die MAPI-Ebene enthält alle Objekte, die MAPI-Clients oder-Dienstanbieter verwenden implementiert wird. 
  
Die folgende Abbildung zeigt, in dem einzelnen MAPI-Objekte in der MAPI-Architektur passt. Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt. Beispielsweise ein Empfängerobjekt Advise wird angezeigt als [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) abgeleitet wird und an, die jedes Empfängerobjekt Advise implementiert wird. Die Schnittstellen, die Ebenen Brücke sind entweder verwendet oder von mehreren Komponenten implementiert. Obwohl die MAPI-Ebene angezeigt wird, trennen die Client- und Anbieter Ebenen, sagen, dass die gesamte Kommunikation über MAPI, flow muss ist dies nicht der Fall. Clients können, und führen Sie kommunizieren direkt an dienstanbieterobjekten. 
  
**Objektschichten in MAPI**
  
![Objektebenen in MAPI] (media/amapi_38.gif "Objektebenen in MAPI")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

