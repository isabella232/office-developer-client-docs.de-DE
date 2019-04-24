---
title: Kanonische MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b017089a675727703de9e2ed4d584e7f77a778a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319054"
---
# <a name="mapi-canonical-properties"></a>Kanonische MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine kanonische Eigenschaft ist eine virtuelle Eigenschaft, die eine MAPI-Eigenschaft darstellt, oder mehrere MAPI-Eigenschaften, die mit demselben Eigenschaftsbezeichner definiert sind. Kanonische Eigenschaften dienen lediglich der konsistenten Identifizierung von MAPI-Eigenschaften in Diskussionen oder Dokumentationen außerhalb von Code. Im Gegensatz zu MAPI-definierten gekennzeichneten Eigenschaftsnamen werden kanonische Eigenschaftennamen nicht als globale Konstanten in MAPI-Headerdateien definiert.
  
## <a name="naming-conventions"></a>BeNennungsKonventionen

Kanonische Eigenschaftennamen beginnen mit einem Präfix, "PID", das "Property Identifier" darstellt. Je nachdem, ob die Eigenschaft eine gekennzeichnete Eigenschaft, eine benannte Eigenschaft mit einem numerischen Bezeichner oder eine benannte Eigenschaft mit einem Zeichenfolgennamen ist, wird das Präfix weiter als "PidTag", "" PidLid "und" PidName "bezeichnet. [PidTagAccount](pidtagaccount-canonical-property.md) stellt beispielsweise die markierten Eigenschaften **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) und **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)) dar, mit denen ein Empfänger Kontoname; [Pidlidcontacts (](pidlidcontacts-canonical-property.md) stellt die **dispidContacts** -Eigenschaft dar, eine benannte Eigenschaft mit einem numerischen Bezeichner, die den Namen der Kontakte angibt, die einer Nachricht zugeordnet sind. und [pidnamephishingstamp (](pidnamephishingstamp-canonical-property.md) stellt "https://schemas.microsoft.com/outlook/phishingstamp," eine benannte Eigenschaft mit einem Zeichenfolgennamen dar und gibt die Zeichenfolge an, die Nachrichten mit hoher Wahrscheinlichkeit für Phishing angibt. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Darstellen ähnlicher Eigenschaften mit einer kanonischen Eigenschaft

### <a name="identifying-properties-in-mapi"></a>Identifizieren von Eigenschaften in MAPI

Alle Eigenschaften in MAPI werden durch einen Eigenschaftenbezeichner identifiziert, bei dem es sich um einen nicht signierten 16-Bit-Wert handelt. Der Eigenschaftenbezeichner und der Eigenschaftentyp (ein anderer nicht signierter 16-Bit-Wert) stellen ein Eigenschaftentag für die Eigenschaft dar. 
  
MAPI verwendet ein Property-Tag, um Eigenschaften eindeutig zu definieren. Eigenschaften, die dasselbe Property-Tag aufweisen, wie **PR_BUSINESS2_TELEPHONE_NUMBER** ([Pidtagbusiness2telephonenumber (](pidtagbusiness2telephonenumber-canonical-property.md)) und **PR_OFFICE2_TELEPHONE_NUMBER** ([pidtagbusiness2telephonenumber (](pidtagbusiness2telephonenumber-canonical-property.md)), werden als identisch betrachtet. Eigenschaften in MAPI. Eine Liste der Eigenschaftentags, die MAPI für eigene Eigenschaften definiert hat, finden Sie in der MAPI-Headerdatei Mapitags. h.
  
Beachten Sie, dass MAPI Eigenschaftsbezeichner in Bereiche unterteilt. Wo ein Bezeichner in den Range fällt, gibt seine Verwendung und seinen Besitz an. Die Eigenschaftenbezeichner der markierten Eigenschaften fallen im Range von 0x0001 zu 0x7FFF. Innerhalb dieses Bereiches befinden sich die Eigenschaftenbezeichner von MAPI-definierten Eigenschaften, die in den Bereich von 0x0001 zu 0x3FFF fallen. Die Eigenschaftenbezeichner von benannten Eigenschaften fallen in den Bereichen von 0X8000 zu 0x8FFF. 
  
Benannte Eigenschaften werden zusätzlich von einem Eigenschaftensatz und entweder einer Long-ID (LID), bei der es sich um einen unsignierten 32-Bit-Wert oder eine Zeichenfolge handelt, zurückgeführt. Ein Eigenschaftensatz ist eine GUID, die eine Gruppe benannter Eigenschaften mit einem ähnlichen Zweck identifiziert. Der Eigenschaftensatz und der Deckel oder der Zeichenfolgenname werden zum Abrufen oder Festlegen der benannten Eigenschaft verwendet.
  
### <a name="property-type"></a>Eigenschaftentyp

Neben Bezeichnern wird eine Eigenschaft durch einen Datentyp zurückgegeben, der den Typ der für diese Eigenschaft zulässigen Werte angibt.
  
Bei Eigenschaften, die vom Typ String sind, kann die Eigenschaft abhängig von der Unterstützung für Unicode in der zugrunde liegenden Plattform vom Typ PT_STRING8 (NULL-terminierte 8-Bit-Zeichenfolge) oder PT_UNICODE (NULL-terminierte Unicode-Zeichenfolge) sein. Eine Eigenschaft kann mit dem PT_TSTRING-Typ definiert werden, und je nach Kompilierungseinstellungen PT_TSTRING standardmäßig eine Unicode-Zeichenfolge für Plattformen, die Unicode unterstützen, oder eine PT_STRING8-Zeichenfolge für Plattformen, die ANSI oder DBCS unterstützen. Es ist üblich, dass eine Zeichenfolge typisierte Eigenschaft durch drei ähnliche Namen wie **PR_ACCOUNT**, **PR_ACCOUNT_A**und **PR_ACCOUNT_W**identifiziert wird, die vom Typ PT_TSTRING, PT_STRING8 und PT_UNICODE sind.
  
Weitere Informationen zu Eigenschaftentypen und Makros im Zusammenhang mit Typen finden Sie in der MAPI-Headerdatei Mapidefs. h.
  
### <a name="identifying-similar-properties"></a>Identifizieren ähnlicher Eigenschaften

In der aktuellen MAPI-Eigenschaften Landschaft ist es nicht unüblich, festzustellen, dass eine Eigenschaft unter verschiedenen Eigenschaftennamen verfügbar gemacht wurde, die alle mit demselben Eigenschaftsbezeichner definiert sind. Beispielsweise sind die getaggten Eigenschaften **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER**in Mapitags. h definiert, um denselben Eigenschaftenbezeichner und-Typ zu haben. Die folgenden beiden Eigenschaften sind eng miteinander verbunden:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Die Eigenschaften mit dem Suffix "_A" werden als PT_STRING8 eingegeben, und die mit dem Suffix "_W" werden als PT_UNICODE eingegeben.
  
Der Zweck einer kanonischen Eigenschaft, die in diesem Beispiel **pidtagbusiness2telephonenumber (** wird, ist die Erleichterung der Referenzierung solcher eng verbundenen MAPI-Eigenschaften mit einem Bezeichner und konsistent (mit dem Präfix "PID") für alle MAPI- Eigenschaften. Informationen zu den tatsächlichen MAPI-Eigenschaften, die eine kanonische Eigenschaft darstellt, finden Sie unter [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md). Informationen zur kanonischen Eigenschaft, mit der eine MAPI-Eigenschaft verknüpft ist, finden Sie unter [Zuordnen von MAPI-Namen zu kanonischEn Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>MAPI-Unterstützung für kanonische Eigenschaftennamen

Da kanonische Eigenschaften keine tatsächlichen Eigenschaften sind und nicht in MAPI-Headerdateien definiert sind, sollten Sie kanonische Eigenschaftennamen nicht im Code verwenden. Stattdessen sollten Sie weiterhin die genauen MAPI-Eigenschaftsnamen im Code verwenden. Sie können beispielsweise **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER** außerhalb von Code als **pidtagbusiness2telephonenumber (** verweisen und entweder **PR_BUSINESS2_TELEPHONE_NUMBER** oder **PR_OFFICE2_ TELEPHONE_NUMBER** im Code. 
  
Wenn Sie kanonische Eigenschaftennamen in Ihrem Code verwenden müssen, müssen Sie diese zuerst in ihren eigenen Headerdateien definieren.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Kanonische Eigenschaftennamen und Exchange-Protokollspezifikationen

Auf kanonische Namen wird in Microsoft Exchange Server Protocol-Spezifikationen verwiesen, die von Exchange Server für die Kommunikation mit anderen Microsoft-Produkten verwendet werden. Weitere Informationen zu Nachrichtenobjekt Eigenschaften, auf die von Exchange-Protokollspezifikationen verwiesen wird, finden Sie unter [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschafts Tags](mapi-property-tags.md)
  
[Übersicht über die MAPI-EigenschaftsKennung](mapi-property-identifier-overview.md)
  
[Übersicht über die MAPI-EigenschaftsTypen](mapi-property-type-overview.md)

