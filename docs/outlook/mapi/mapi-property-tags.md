---
title: TAGS der MAPI-Eigenschaft
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328235"
---
# <a name="mapi-property-tags"></a>TAGS der MAPI-Eigenschaft
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftstag ist eine 32-Bit-Zahl, die einen eindeutigen Eigenschaftenbezeichner in den Bits 16 bis 31 und einen Eigenschaftstyp in bits 0 bis 15 enthält, wie in der folgenden Abbildung dargestellt. 
  
**Eigenschafts-Tag-Elemente**
  
![Eigenschaftstagelemente](media/amapi_10.gif "Eigenschaftentagelemente")
  
Eigenschaftstags werden verwendet, um MAPI-Eigenschaften zu identifizieren, und jede Eigenschaft muss über eine verfügen, unabhängig davon, ob die Eigenschaft von MAPI, einem Client oder einem Dienstanbieter definiert wird. MAPI definiert eine Reihe von Eigenschaftentagkonstante für seine Eigenschaften in der Mapitags.h-Headerdatei. diese Eigenschaften werden als "MAPI-definierte Eigenschaften" bezeichnet. 
  
Die Eigenschaftentagkonstante folgen einer Benennungskonvention für Konsistenz und Benutzerfreundlichkeit. Der Name jedes Eigenschaftstags enthält zwei Teile: ein PR_-Präfix und eine oder mehrere Zeichenzeichenfolgen, die den Inhalt der Eigenschaft beschreiben. Zeichenfolgen mit mehreren Zeichen werden durch Unterstriche getrennt. Das Eigenschaftstag für den Adresstyp eines Nachrichtenempfängers ist z. B. **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) und der Eintragsbezeichner für den Ordner, der für den Empfang einer Kopie jeder ausgehenden Nachricht bestimmt **ist, lautet PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Einige Makros stehen zur Verfügung, um die Arbeit mit Eigenschaftstags zu unterstützen, darunter [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)und [PROP_TAG](prop_tag.md). **PROP \_ TYPE** extrahiert den Eigenschaftentyp aus dem Eigenschaftstag. **PROP \_ ID** extrahiert den Bezeichner. **PROP_TAG** erstellt ein Eigenschaftentag aus einem Eigenschaftentyp und einem Bezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

