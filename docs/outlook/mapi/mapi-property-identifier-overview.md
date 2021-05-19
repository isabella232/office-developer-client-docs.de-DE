---
title: Übersicht über die MAPI-Eigenschafts-ID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29626f49365a0f37f1e13d965c62bfd5ad0fb774
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414697"
---
# <a name="mapi-property-identifier-overview"></a>Übersicht über die MAPI-Eigenschafts-ID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine Eigenschafts-ID ist eine Zahl, die verwendet wird, um anzugeben, wofür eine Eigenschaft verwendet wird und wer dafür verantwortlich ist. Eigenschaftsbezeichner werden durch MAPI in Bereiche unterteilt. wobei ein Bezeichner in den Bereich fällt, der seine Verwendung und den Besitz angibt. 
  
Der Bereich der Eigenschaftenbezeichner wird von 0x0001 bis 0xFFFF. Eigenschaftsbezeichner 0x0000 und 0xFFFF sind in allen Fällen reserviert, d. h., diese Bezeichner müssen nicht verwendet werden. Der Von MAPI definierte Bereich für Eigenschaften wird von 0x0001 bis 0x3FFF. Diese Eigenschaften werden als MAPI-definierte Eigenschaften bezeichnet. Der Bereich 0x4000 0x7FFF nachrichten- und empfängereigenschaften gehört, und Clients oder Dienstanbieter können Eigenschaften in diesem Bereich definieren. Eigenschaften im Bereich von 0x0001 bis 0x7FFF werden als markierte Eigenschaften bezeichnet. Darüber 0x8000 der Bereich für so genannte benannte Eigenschaften oder Eigenschaften, die eine 32-Bit-GUID (Globally Unique Identifier) und eine Unicode-Zeichenzeichenfolge oder einen numerischen Wert enthalten. Clients können benannte Eigenschaften verwenden, um ihren Eigenschaftensatz anzupassen.
  
Dienstanbieter können sichere Profileigenschaften im Bereich von 0x67F0 über 0x67FF. Sichere Profileigenschaften werden für Informationen verwendet, die zusätzlichen Schutz erfordern, z. B. Kennwörter. Diese Eigenschaften können ausgeblendet und verschlüsselt werden. Ob sichere Eigenschaften in der Standardliste der von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegebenen Eigenschaften enthalten sind, hängt von der Implementierung des Anbieters ab. In der Regel sind diese Eigenschaften nicht enthalten. Die [IProfSect : IMAPIProp-Schnittstelle](iprofsectimapiprop.md) wird für den Zugriff auf die Eigenschaften eines Profilabschnitts verwendet, einschließlich sicherer Eigenschaften. 
  
Einige Eigenschaftsbereiche sind auf übertragungsfähige Eigenschaften oder nicht durchsetzbare Eigenschaften beschränkt. Übertragene Eigenschaften werden mit einer Nachricht übertragen. Nichttransmittable Eigenschaften werden nicht mit einer Nachricht übertragen. Nichttransmittable Eigenschaften enthalten in der Regel Informationen, die nur für Clients und Dienstanbieter von Wert sind, die mit der aktuellen Sitzung arbeiten. Diese Eigenschaften wären nicht unbedingt für ein anderes Messagingsystem und einen anderen Satz von Dienstanbietern hilfreich. Das Konzept der übertragungsbaren Eigenschaften gilt in erster Linie für Transportanbieter. Um zu bestimmen, ob eine Eigenschaft übertragen werden kann oder nicht, übergeben Sie ihr Eigenschaftstag an das **FIsTransmittable-Makro,** das in der Mapitags.h-Headerdatei definiert ist. 
  
Eine vollständige Beschreibung der Bezeichnerbereiche finden Sie unter [Property Identifier Ranges](property-identifier-ranges.md).
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

