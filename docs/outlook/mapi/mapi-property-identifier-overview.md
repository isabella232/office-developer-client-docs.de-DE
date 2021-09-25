---
title: Übersicht über mapi-Eigenschaftsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 83712c9a432c31e0a02d7eca39397a1bef92271d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600813"
---
# <a name="mapi-property-identifier-overview"></a>Übersicht über mapi-Eigenschaftsbezeichner

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftsbezeichner ist eine Zahl, die verwendet wird, um anzugeben, wofür eine Eigenschaft verwendet wird und wer dafür verantwortlich ist. Eigenschaftsbezeichner werden durch MAPI in Bereiche unterteilt. wenn ein Bezeichner in den Bereich fällt, gibt die Verwendung und den Besitz an. 
  
Der Bereich der Eigenschaftsbezeichner wird von 0x0001 bis 0xFFFF ausgeführt. Eigenschaftsbezeichner 0x0000 und 0xFFFF sind in allen Fällen reserviert, was bedeutet, dass diese Bezeichner nicht verwendet werden müssen. Der Bereich für von MAPI definierte Eigenschaften wird von 0x0001 bis 0x3FFF ausgeführt. Diese Eigenschaften werden als MAPI-definierte Eigenschaften bezeichnet. Der Bereich 0x4000 0x7FFF gehört zu nachrichten- und empfängereigenschaften, und entweder Clients oder Dienstanbieter können Eigenschaften in diesem Bereich definieren. Eigenschaften im Bereich von 0x0001 zu 0x7FFF werden als markierte Eigenschaften bezeichnet. Über 0x8000 hinaus ist der Bereich für so genannte Eigenschaften oder Eigenschaften, die einen 32-Bit-GUID (Globally Unique Identifier) und eine Unicode-Zeichenzeichenfolge oder einen numerischen Wert enthalten. Clients können benannte Eigenschaften verwenden, um ihren Eigenschaftensatz anzupassen.
  
Dienstanbieter können sichere Profileigenschaften im Bereich 0x67F0 über 0x67FF definieren. Sichere Profileigenschaften werden für Informationen verwendet, die zusätzlichen Schutz erfordern, z. B. Kennwörter. Diese Eigenschaften können ausgeblendet und verschlüsselt werden. Ob sichere Eigenschaften in der Standardliste der eigenschaften enthalten sind, die von der [IMAPIProp::GetPropList-Methode](imapiprop-getproplist.md) zurückgegeben werden, hängt von der Implementierung des Anbieters ab. In der Regel sind diese Eigenschaften nicht enthalten. Die [IProfSect : IMAPIProp-Schnittstelle](iprofsectimapiprop.md) wird für den Zugriff auf die Eigenschaften eines Profilabschnitts verwendet, einschließlich sicherer Eigenschaften. 
  
Einige Der Eigenschaftenbereiche sind auf übertragbare oder nicht verarbeitbare Eigenschaften beschränkt. Übertragbare Eigenschaften werden mit einer Nachricht übertragen. Nichtübertragbare Eigenschaften werden nicht mit einer Nachricht übertragen. Nicht transparente Eigenschaften enthalten in der Regel Informationen, die nur für Clients und Dienstanbieter von Wert sind, die mit der aktuellen Sitzung arbeiten. Diese Eigenschaften sind nicht notwendigerweise für ein anderes Messagingsystem und eine andere Gruppe von Dienstanbietern nützlich. Das Konzept der übertragbaren Eigenschaften gilt in erster Linie für Transportanbieter. Um zu bestimmen, ob eine Eigenschaft übertragen werden kann oder nicht, übergeben Sie ihr Eigenschaftstag an das **FIsTransmittable-Makro,** das in der Headerdatei Mapitags.h definiert ist. 
  
Eine vollständige Beschreibung der Bezeichnerbereiche finden Sie unter [Eigenschaftenbezeichnerbereiche.](property-identifier-ranges.md)
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

