---
title: KANONISCHE EIGENSCHAFTEN VON MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540476"
---
# <a name="mapi-canonical-properties"></a>KANONISCHE EIGENSCHAFTEN VON MAPI

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine kanonische Eigenschaft ist eine virtuelle Eigenschaft, die eine MAPI-Eigenschaft darstellt, oder mehrere MAPI-Eigenschaften, die mit demselben Eigenschaftenbezeichner definiert sind. Kanonische Eigenschaften dienen nur dazu, die konsistente Identifizierung von MAPI-Eigenschaften in Diskussionen oder Dokumentationen außerhalb des Codes zu erleichtern. Im Gegensatz zu DURCH MAPI definierten Eigenschaftsnamen werden kanonische Eigenschaftsnamen in MAPI-Headerdateien nicht als globale Konstanten definiert.
  
## <a name="naming-conventions"></a>Benennungskonventionen

Kanonische Eigenschaftsnamen beginnen mit dem Präfix "Pid", das "Eigenschaftsbezeichner" darstellt. Je nachdem, ob es sich bei der Eigenschaft um eine markierte Eigenschaft, eine benannte Eigenschaft mit einem numerischen Bezeichner oder eine benannte Eigenschaft mit einem Zeichenfolgennamen handelt, wird das Präfix als "PidTag", "PidLid" bzw. "PidName" qualifiziert. Beispielsweise stellt [PidTagAccount](pidtagaccount-canonical-property.md) die markierten Eigenschaften **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) und **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)) dar, die den Kontonamen eines Empfängers angeben. [PidLidContacts](pidlidcontacts-canonical-property.md) stellt die **dispidContacts-Eigenschaft** dar, eine benannte Eigenschaft mit einer numerischen ID, die den Namen von Kontakten angibt, die einer Nachricht zugeordnet sind. und [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) stellt " ," eine benannte Eigenschaft dar, die einen Zeichenfolgennamen hat und die Zeichenfolgenmarkierungsmeldungen angibt, bei der es sich wahrscheinlich um http://schemas.microsoft.com/outlook/phishingstamp Phishing handelt. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Darstellen ähnlicher Eigenschaften mithilfe einer kanonischen Eigenschaft

### <a name="identifying-properties-in-mapi"></a>Identifizieren von Eigenschaften in MAPI

Alle Eigenschaften in MAPI werden durch einen Eigenschaftenbezeichner identifiziert, bei dem es sich um einen nicht signierten 16-Bit-Wert handelt. Der Eigenschaftenbezeichner und der Eigenschaftentyp (ein weiterer nicht signierter 16-Bit-Wert) bilden ein Eigenschaftstag für die Eigenschaft. 
  
MAPI verwendet ein Eigenschaftstag, um Eigenschaften eindeutig zu definieren. Eigenschaften mit demselben Eigenschaftentag, z. B. **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) und **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), werden in MAPI als identische Eigenschaften betrachtet. Eine Liste der Eigenschaftentags, die MAPI für eigene Eigenschaften definiert hat, finden Sie in der MAPI-Headerdatei Mapitags.h.
  
Beachten Sie, dass MAPI Eigenschaftenbezeichner in Bereiche unterteilt. Wenn ein Bezeichner in den Bereich fällt, wird dessen Verwendung und Besitz angegeben. Die Eigenschaftenbezeichner von markierten Eigenschaften liegen im Bereich von 0x0001 bis 0x7FFF. Innerhalb dieses Bereichs befinden sich die Eigenschaftenbezeichner von MAPI-definierten Eigenschaften, die in den Bereich von 0x0001 bis 0x3FFF. Die Eigenschaftenbezeichner benannter Eigenschaften liegen im Bereich von 0x8000 bis 0x8FFF. 
  
Benannte Eigenschaften werden zusätzlich durch einen Eigenschaftensatz und entweder durch eine lange ID (LID), bei der es sich um einen nicht signierten 32-Bit-Wert handelt, oder durch eine Zeichenfolge zugeordnet. Ein Eigenschaftensatz ist eine GUID, die eine Gruppe benannter Eigenschaften mit einem ähnlichen Zweck identifiziert. Der Eigenschaftensatz und DER LID- oder Zeichenfolgenname werden verwendet, um die benannte Eigenschaft zu erhalten oder zu legen.
  
### <a name="property-type"></a>Eigenschaftentyp

Neben Bezeichnern wird eine Eigenschaft durch einen Datentyp zugeordnet, der den Typ der für diese Eigenschaft zulässigen Werte angibt.
  
Bei Eigenschaften des Zeichenfolgentyps kann die Eigenschaft je nach Unterstützung von Unicode in der zugrunde liegenden Plattform vom Typ PT_STRING8 (8-Bit-Zeichenfolge null-terminated) oder PT_UNICODE (null-terminated Unicode string) sein. Eine Eigenschaft kann mit dem PT_TSTRING-Typ definiert werden, und je nach Kompilierungseinstellungen ist PT_TSTRING standardmäßig eine Unicode-Zeichenfolge für Plattformen, die Unicode unterstützen, oder eine PT_STRING8-Zeichenfolge für Plattformen, die ANSI oder DBCS unterstützen. Es ist üblich, dass eine zeichenfolgentypierte Eigenschaft durch drei ähnliche Namen identifiziert wird, z. B. **PR_ACCOUNT**, **PR_ACCOUNT_A** und **PR_ACCOUNT_W**, die den Typ PT_TSTRING, PT_STRING8 und PT_UNICODE haben.
  
Weitere Informationen zu Eigenschaftentypen und Makros im Zusammenhang mit Typen finden Sie in der MAPI-Headerdatei Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identifizieren ähnlicher Eigenschaften

In der aktuellen MAPI-Eigenschaftslandschaft ist es nicht ungewöhnlich, dass eine Eigenschaft unter verschiedenen Eigenschaftsnamen verfügbar gemacht wurde, die alle mit demselben Eigenschaftenbezeichner definiert sind. Beispielsweise werden die markierten Eigenschaften **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER** in Mapitags.h definiert, um denselben Eigenschaftenbezeichner und -typ zu haben. In engem Zusammenhang mit diesen beiden Eigenschaften stehen:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Die Eigenschaften mit dem Suffix "_A" werden als PT_STRING8 und die Eigenschaften mit dem Suffix "_W" als "PT_UNICODE" PT_UNICODE.
  
Der Zweck einer kanonischen Eigenschaft, **PidTagBusiness2TelephoneNumber** in diesem Beispiel, besteht in der Erleichterung des Verweisens auf solche eng verbundenen #A0 mithilfe eines Bezeichners und auf konsistente Weise (mit dem Präfix "Pid") für alle #A1. Informationen zu den tatsächlichen MAPI-Eigenschaften, die eine kanonische Eigenschaft darstellt, finden Sie unter [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md). Informationen zur kanonischen Eigenschaft, der eine MAPI-Eigenschaft zugeordnet ist, finden Sie unter [Mapping MAPI Names to Canonical Property Names](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>MAPI-Unterstützung für kanonische Eigenschaftsnamen

Da kanonische Eigenschaften keine echten Eigenschaften sind und nicht in #A0 definiert sind, sollten Sie im Code keine kanonischen Eigenschaftsnamen verwenden. Stattdessen sollten Sie weiterhin die genauen NAMEN der MAPI-Eigenschaft im Code verwenden. Sie können z.  B. PR_BUSINESS2_TELEPHONE_NUMBER und **PR_OFFICE2_TELEPHONE_NUMBER** außerhalb des Codes als **PidTagBusiness2TelephoneNumber** verweisen und entweder PR_BUSINESS2_TELEPHONE_NUMBER oder PR_OFFICE2_TELEPHONE_NUMBER **Code** verwenden.  
  
Wenn Sie kanonische Eigenschaftsnamen in Ihrem Code verwenden müssen, müssen Sie sie zuerst in Ihren eigenen Headerdateien definieren.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Canonical Property Names and Exchange Protocol Specifications

Auf kanonische Namen Microsoft Exchange Server Protokollspezifikationen verwiesen, die von Exchange Server für die Kommunikation mit anderen Microsoft-Produkten verwendet werden. Weitere Informationen zu Nachrichtenobjekteigenschaften, auf die Exchange verweisen, finden Sie unter [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaftstags](mapi-property-tags.md)
  
[Übersicht über die MAPI-Eigenschafts-ID](mapi-property-identifier-overview.md)
  
[Übersicht über den MAPI-Eigenschaftstyp](mapi-property-type-overview.md)

