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
  
Alle objekte, die MAPI definiert, fallen in eine oder mehrere Ebenen der MAPI-Architektur. Die Clientschnittstellenebene enthält alle Objekte, die eine Clientanwendung, eine Formularanzeige oder ein Formularserver implementieren kann. Die Schnittstellesebene des Dienstanbieters enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren kann. Diese Ebene umfasst Objekte, die von Adressbüchern, Nachrichtenspeichern, Transportanbietern und Formularbibliotheken implementiert werden. Die Ebene, die das MAPI-Subsystem darstellt, wird zwischen den Client- und Dienstanbieterschnittstellenebenen positioniert. Die MAPI-Ebene enthält alle Objekte, die MAPI für Clients oder Dienstanbieter implementiert. 
  
Die folgende Abbildung zeigt, wo die einzelnen MAPI-Objekte in die MAPI-Architektur passen. Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt. Beispielsweise wird ein Advise Sink -Objekt als [IMAPIAdviseSink angezeigt: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) ab leitet und die jedes advise sink -Objekt implementiert. Die Schnittstellen, die Layer überbrücken, werden von mehreren Komponenten verwendet oder implementiert. Obwohl die MAPI-Ebene die Client- und Anbieterebenen zu trennen scheint, bedeutet dies, dass die kommunikation über MAPI fließen muss, dies ist jedoch nicht der Fall. Clients können und können direkt mit Dienstanbieterobjekten kommunizieren. 
  
**Objektschichten in MAPI**
  
![Objektebenen in MAPI-Objektebenen](media/amapi_38.gif "in MAPI")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

