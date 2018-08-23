---
title: Übersicht über die Bezeichner des MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8cf2f08a69ee87c40789b764596e514c91483c2e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563156"
---
# <a name="mapi-property-identifier-overview"></a>Übersicht über die Bezeichner des MAPI-Eigenschaft

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ein Bezeichner für eine ist eine Zahl, die verwendet wird, um anzugeben, was für eine Eigenschaft verwendet wird, und wer ist dafür verantwortlich. Eigenschaftenbezeichner sind MAPI in Bereiche unterteilt; Gibt an, bei denen ein Bezeichner des Bereichs liegt, seine Verwendung und den Besitz. 
  
Der Bereich der Eigenschaftenbezeichner verläuft vom 0 x 0001 bis 0xFFFF. Eigenschaftenbezeichner 0 x 0000 und 0xFFFF sind in allen Fällen, was bedeutet, dass dieser Bezeichner nicht verwendete bleiben müssen reserviert. Der Bereich für MAPI definierten Eigenschaften wird auf 0 x 0001 zum 0x3FFF ausgeführt. Diese Eigenschaften werden als MAPI-benutzerdefinierte Eigenschaften bezeichnet. Der Bereich 0 x 4000 auf 0x7FFF Nachrichten- und Empfängereigenschaften gehört, und Clients oder Dienstanbieter können Eigenschaften in diesem Bereich definieren. Eigenschaften im Bereich von 0 x 0001 zu 0x7FFF werden als markierte Eigenschaften bezeichnet. 0 x 8000 sprengen Bereich bekannt ist als benannten Eigenschaften oder Eigenschaften, die einen global eindeutigen Bezeichner (GUID) von 32-Bit- und eine Unicode-Zeichenfolge oder numerischen Wert enthalten. Benannte Eigenschaften können Clients ihre Eigenschaftensatz anpassen.
  
Dienstanbieter können sichere Profileigenschaften im Bereich 0x67F0 bis 0x67FF definieren. Sichern Sie die Profil, das Eigenschaften Informationen verwendet werden, die zusätzlichen Schutz, beispielsweise Kennwörter erforderlich sind. Diese Eigenschaften können ausgeblendet und verschlüsselt werden. Unabhängig davon, ob sichere Eigenschaften in der Liste der von der [IMAPIProp::GetPropList](imapiprop-getproplist.md) -Methode zurückgegebenen Eigenschaften enthalten sind, hängt von der Anbieter-Implementierung. Diese Eigenschaften sind in der Regel nicht enthalten. Die [IProfSect: IMAPIProp](iprofsectimapiprop.md) -Schnittstelle wird für den Zugriff auf die Eigenschaften eines Abschnitts Profil, einschließlich sichere Eigenschaften. 
  
Einige dieser Eigenschaft Bereiche sind auf Übertragungseinehit oder nontransmittable Eigenschaften beschränkt. Übertragungseinehit Eigenschaften werden mit einer Meldung übertragen. Nontransmittable Eigenschaften werden mit einer Nachricht nicht übertragen. Nontransmittable Eigenschaften enthalten in der Regel Informationen, die vom Wert nur für Clients und -Dienstanbieter, die mit der aktuellen Sitzung ist. Diese Eigenschaften wäre nicht sinnvoll, die einem anderen Messagingsystem und einen weiteren Satz der Dienstanbieter unbedingt. Das Konzept der Übertragungseinehit Eigenschaften wird hauptsächlich Transportanbieter betrifft. Um festzustellen, ob eine Eigenschaft Übertragungseinehit ist, übergeben Sie seine Eigenschafts-Tag an das **FIsTransmittable** -Makro, das in der Headerdatei Mapitags.h definiert. 
  
Eine vollständige Beschreibung der Bereiche Bezeichner finden Sie unter [Eigenschaft Bezeichner Bereiche](property-identifier-ranges.md).
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

