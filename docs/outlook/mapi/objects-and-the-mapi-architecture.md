---
title: Objekte und die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9f37b5bd452f35e54edee6f98387c6f39d284106
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561180"
---
# <a name="objects-and-the-mapi-architecture"></a>Objekte und die MAPI-Architektur

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle von der MAPI definierten Objekte fallen in eine oder mehrere Ebenen in der MAPI-Architektur. Die Clientschnittstellenebene enthält alle Objekte, die eine Clientanwendung, eine Formularanzeige oder ein Formularserver implementieren kann. Die Dienstanbieter-Schnittstellenebene enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren kann. Diese Ebene umfasst Objekte, die von Adressbüchern, Nachrichtenspeichern, Transportanbietern und Formularbibliotheken implementiert werden. Die Ebene, die das MAPI-Subsystem darstellt, wird zwischen client- und dienstanbieterschnittstellenebenen positioniert. Die MAPI-Ebene enthält alle Objekte, die MAPI für Clients oder Dienstanbieter implementiert. 
  
Die folgende Abbildung zeigt, wo jedes der MAPI-Objekte in die MAPI-Architektur passt. Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt. Beispielsweise wird ein Empfehlungssenkenobjekt als [IMAPIAdviseSink angezeigt: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) abgeleitet wird und die jedes Empfehlungssenkenobjekt implementiert. Die Schnittstellen, die Layer überbrücken, werden entweder von mehreren Komponenten verwendet oder implementiert. Obwohl die MAPI-Ebene die Client- und Anbieterebene zu trennen scheint, was bedeutet, dass die gesamte Kommunikation über die MAPI fließen muss, ist dies nicht der Fall. Clients können und können direkt mit Dienstanbieterobjekten kommunizieren. 
  
**Objektschichten in MAPI**
  
![Objektschichten in MAPI](media/amapi_38.gif "Objektschichten in MAPI")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)
- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

