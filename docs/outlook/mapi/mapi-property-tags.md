---
title: MAPI-Eigenschaftentags
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 96211d3b6e1e4dfbd4c93a98c8dd04de10eac884
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390016"
---
# <a name="mapi-property-tags"></a>MAPI-Eigenschaftentags
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftentag ist eine 32-Bit-Zahl mit dem eindeutigen Bezeichner für eine in Bits 16 bis 31 und einen Eigenschaftentyp in Bits 0 bis 15, wie in der folgenden Abbildung dargestellt. 
  
**Eigenschafts-Tag-Elemente**
  
![Eigenschaftentags] (media/amapi_10.gif "Eigenschaftentags")
  
Eigenschaftentags dienen zum Identifizieren der MAPI-Eigenschaften und hat jede Eigenschaft, unabhängig davon, ob die Eigenschaft durch MAPI, einen Client oder einem Dienstanbieter definiert ist. MAPI definiert eine Reihe von Konstanten für Tag-Eigenschaft für seine Eigenschaften in der Headerdatei Mapitags.h. Diese Eigenschaften werden als "MAPI-definierte Eigenschaften" bezeichnet. 
  
Konstanten für die Tag-Eigenschaft der Namenskonvention für Konsistenz und Bedienung. Es gibt zwei Webparts auf den Namen der einzelnen Eigenschafts-Tag: ein Präfix PR_ und eine oder mehrere Zeichenfolgen, die die Inhalte der Eigenschaft beschreiben. Mehrere Zeichenfolgen werden durch Unterstriche getrennt. Beispielsweise ist das Eigenschafts-Tag für den Adresstyp der Empfänger einer Nachricht **PR\_ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)) und die Eintrags-ID für den Ordner festgelegt, von der eine Kopie aller ausgehenden Nachrichten erhalten ist **PR_IPM_SENTMAIL_ ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Einige Makros stehen zum Eigenschaftentags zwischen diesen [PROP_TYPE](prop_type.md), [eigensch_id](prop_id.md)und [PROP_TAG](prop_tag.md)entwickelt. **Eigenschaft\_Typ** extrahiert den Eigenschaftentyp aus das Eigenschafts-Tag **Eigenschaft\_ID** extrahiert den Bezeichner. **PROP_TAG** erstellt ein Eigenschaftentag über einen Eigenschaftentyp und Bezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

