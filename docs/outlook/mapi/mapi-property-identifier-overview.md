---
title: Übersicht über die MAPI-EigenschaftsKennung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 957aa00f-23d8-4f3b-bbc2-7d54f17b47b5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29626f49365a0f37f1e13d965c62bfd5ad0fb774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328186"
---
# <a name="mapi-property-identifier-overview"></a>Übersicht über die MAPI-EigenschaftsKennung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftenbezeichner ist eine Zahl, die verwendet wird, um anzugeben, wofür eine Eigenschaft verwendet wird und wer dafür zuständig ist. Eigenschaftsbezeichner werden durch MAPI in Bereiche unterteilt; wo ein Bezeichner in den Range fällt, gibt seine Verwendung und seinen Besitz an. 
  
Der Umfang der Eigenschaftsbezeichner wird von 0x0001 bis 0xFFFF ausgeführt. Eigenschaftenbezeichner 0x0000 und 0xFFFF sind in allen Fällen reserviert, was bedeutet, dass diese Bezeichner nicht verwendet werden müssen. Der Range für von MAPI definierte Eigenschaften wird von 0x0001 bis 0x3FFF ausgeführt. Diese Eigenschaften werden als MAPI-definierte Eigenschaften bezeichnet. Der 0x4000-0x7FFF gehört zu Nachrichten-und Empfänger Eigenschaften, und entweder Clients oder Dienstanbieter können Eigenschaften in diesem Range definieren. Eigenschaften im Range von 0x0001 bis 0x7FFF werden als gekennzeichnete Eigenschaften bezeichnet. Beyond 0X8000 ist der Umfang für das, was als benannte Eigenschaften bezeichnet wird, oder Eigenschaften, die einen global eindeutigen Bezeichner (GUID) mit 32 Bit und eine Unicode-Zeichenfolge oder einen numerischen Wert aufweisen. Clients können benannte Eigenschaften verwenden, um Ihren Eigenschaftensatz anzupassen.
  
Dienstanbieter können sichere Profileigenschaften im Range 0x67F0 bis 0x67FF definieren. Sichere Profileigenschaften werden für Informationen verwendet, die zusätzlichen Schutz erfordern, beispielsweise Kennwörter. Diese Eigenschaften können ausgeblendet und verschlüsselt werden. Ob sichere Eigenschaften in der Standardliste der von der [IMAPIProp::](imapiprop-getproplist.md) getproplist-Methode zurückgegebenen Eigenschaften enthalten sind, hängt von der Implementierung des Anbieters ab. In der Regel sind diese Eigenschaften nicht enthalten. Die [IProfSect: IMAPIProp](iprofsectimapiprop.md) -Schnittstelle wird für den Zugriff auf die Eigenschaften eines Profil Abschnitts, einschließlich der sicheren Eigenschaften, verwendet. 
  
Einige der Eigenschaftsbereiche sind auf transmitable-Eigenschaften oder nontransmitable-Eigenschaften beschränkt. Transmitable-Eigenschaften werden mit einer Nachricht übertragen; nicht übertragbare Eigenschaften werden nicht mit einer Nachricht übertragen. Nontransmitable-Eigenschaften enthalten in der Regel Informationen, die nur für Clients und Dienstanbieter von Nutzen sind, die mit der aktuellen Sitzung arbeiten. Diese Eigenschaften wären für ein anderes Messagingsystem und eine andere Gruppe von Dienstanbietern nicht unbedingt sinnvoll. Das Konzept der transmitable-Eigenschaften gilt in erster Linie für Transportanbieter. Um zu bestimmen, ob eine Eigenschaft transmitable ist oder nicht, übergeben Sie Ihr Property-Tag an das **FIsTransmittable** -Makro, das in der Headerdatei Mapitags. h definiert ist. 
  
Eine vollständige Beschreibung der Bezeichner Bereiche finden Sie unter [Eigenschaftenbezeichner Bereiche](property-identifier-ranges.md).
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

