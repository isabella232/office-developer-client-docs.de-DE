---
title: MAPI-Eigenschaftstags
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 380dad4c-7fbf-4c49-b67c-ab612c923499
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c0fb964b74539ea05cb638add5d3c964a992c3d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567137"
---
# <a name="mapi-property-tags"></a>MAPI-Eigenschaftstags
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ein Eigenschaftstag ist eine 32-Bit-Nummer, die einen eindeutigen Eigenschaftenbezeichner in den Bits 16 bis 31 und einen Eigenschaftstyp in den Bits 0 bis 15 enthält, wie in der folgenden Abbildung dargestellt. 
  
**Eigenschafts-Tag-Elemente**
  
![Eigenschafts-Tag-Elemente](media/amapi_10.gif "Eigenschafts-Tag-Elemente")
  
Eigenschaftentags werden verwendet, um MAPI-Eigenschaften zu identifizieren, und jede Eigenschaft muss über eine eigenschaft verfügen, unabhängig davon, ob die Eigenschaft von der MAPI, einem Client oder einem Dienstanbieter definiert wird. MAPI definiert einen Satz von Eigenschaftstagkonstanten für seine Eigenschaften in der Headerdatei Mapitags.h; diese Eigenschaften werden als "MAPI-definierte Eigenschaften" bezeichnet. 
  
Die Eigenschaftentagkonstanten folgen einer Benennungskonvention, um Konsistenz und Benutzerfreundlichkeit zu gewährleisten. Der Name der einzelnen Eigenschaftstags besteht aus zwei Teilen: einem PR_ Präfix und einer oder mehreren Zeichenfolgen, die den Inhalt der Eigenschaft beschreiben. Mehrere Zeichenfolgen werden durch Unterstriche getrennt. Das Eigenschaftstag für den Adresstyp eines Nachrichtenempfängers lautet z. B. **PR \_ ADDRTYPE** ([PidTagOrgAddrtype](https://msdn.microsoft.com/library/d40b5707-e4d5-4746-88d4-8616a3789789%28Office.15%29.aspx)), und der Eintragsbezeichner für den Ordner, der eine Kopie jeder ausgehenden Nachricht empfangen **soll,** ist PR_IPM_SENTMAIL_ENTRYID ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)).
  
Einige Makros sind verfügbar, um die Arbeit mit Eigenschaftentags zu erleichtern, darunter [PROP_TYPE,](prop_type.md) [PROP_ID](prop_id.md)und [PROP_TAG.](prop_tag.md) **PROP \_ TYPE** extrahiert den Eigenschaftstyp aus dem Eigenschaftentag. **PROP \_ ID** extrahiert den Bezeichner. **PROP_TAG** erstellt ein Eigenschaftstag aus einem Eigenschaftstyp und einem Bezeichner. 
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

