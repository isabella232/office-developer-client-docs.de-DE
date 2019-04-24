---
title: MAPI-Eigenschaftstags
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
# <a name="mapi-property-tags"></a>MAPI-Eigenschaftstags
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Property-Tag ist eine 32-Bit-Zahl, die einen eindeutigen Eigenschaftenbezeichner in Bits 16 bis 31 und einen Eigenschaftentyp in Bits 0 bis 15 enthält, wie in der folgenden Abbildung dargestellt. 
  
**Eigenschafts-Tag-Elemente**
  
![Eigenschaftentag Elemente] (media/amapi_10.gif "Eigenschaftentag Elemente")
  
Eigenschaftstags werden verwendet, um MAPI-Eigenschaften zu identifizieren, und jede Eigenschaft muss einen haben, unabhängig davon, ob die Eigenschaft von MAPI, einem Client oder einem Dienstanbieter definiert wird. MAPI definiert eine Reihe von Eigenschaftentag Konstanten für die Eigenschaften in der Headerdatei Mapitags. h; Diese Eigenschaften werden als "MAPI-definierte Eigenschaften" bezeichnet. 
  
Die Eigenschaftentag Konstanten Folgen einer Benennungskonvention für Konsistenz und Benutzerfreundlichkeit. Es gibt zwei Teile des Namens jedes Property-Tags: ein PR_-Präfix und eine oder mehrere Zeichenfolgen, die den Inhalt der Eigenschaft beschreiben. Mehrere Zeichenfolgen werden durch Unterstriche getrennt. Beispielsweise ist das Property-Tag für den Adresstyp eines Nachrichtenempfängers **PR\_addrType** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)), und die Eintrags-ID für den Ordner, der für das Empfangen einer Kopie jeder ausgehenden Nachricht bestimmt ist **PR_IPM_SENTMAIL_ EINTRAGs** -Nr. ([pidtagipmsentmailentryid (](pidtagipmsentmailentryid-canonical-property.md)).
  
Es stehen einige Makros zur Verfügung, um mit Eigenschaftstags zu arbeiten, darunter [PROP_TYPE](prop_type.md), [PROP_ID](prop_id.md)und [PROP_TAG](prop_tag.md). **PROP\_-Typ** extrahiert den Eigenschaftentyp aus dem Property-Tag; **Prop\_ID** extrahiert den Bezeichner. **PROP_TAG** erstellt ein Property-Tag aus einem Eigenschaftentyp und einem Bezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

