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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279788"
---
# <a name="objects-and-the-mapi-architecture"></a>Objekte und die MAPI-Architektur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Objekte, die MAPI definiert, fallen in eine oder mehrere Ebenen in der MAPI-Architektur. Die Ebene der Clientschnittstelle enthält alle Objekte, die von einer Clientanwendung, einem Formular Betrachter oder einem Formularserver implementiert werden können. Die Ebene der Dienstanbieter Oberfläche enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren kann. Dieser Layer umfasst Objekte, die durch Adressbücher, Nachrichtenspeicher, Transportanbieter und Formularbibliotheken implementiert werden. Die Ebene, die das MAPI-Subsystem darstellt, wird zwischen den Layern der Client-und der Dienstanbieter Oberfläche positioniert. Die MAPI-Schicht enthält alle Objekte, die MAPI für die zu verwendenden Clients oder Dienstanbieter implementiert. 
  
Die folgende Abbildung zeigt, wo jedes MAPI-Objekt in die MAPI-Architektur passt. Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt. Ein Advise-Senke-Objekt wird beispielsweise als [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle angezeigt, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) abgeleitet ist und die jedes Advise-Senke-Objekt implementiert. Die Schnittstellen, die Layer überbrücken, werden entweder von mehreren Komponenten verwendet oder implementiert. Obwohl die MAPI-Schicht angezeigt wird, um die Client-und Anbieter Ebenen zu trennen, was bedeutet, dass die gesamte Kommunikation über MAPI fließen muss, ist dies nicht der Fall. Clients können und tun direkt an Dienstanbieter Objekte kommunizieren. 
  
**Objektschichten in MAPI**
  
![Objektebenen in MAPI] (media/amapi_38.gif "Objektebenen in MAPI")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Übersicht über MAPI-Objekte und-Schnittstellen](mapi-object-and-interface-overview.md)

