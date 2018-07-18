---
title: Kanonische MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2a080b9e6a824e50648a6df0757826f45b5da1f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792959"
---
# <a name="mapi-canonical-properties"></a>Kanonische MAPI-Eigenschaften

  
  
**Betrifft**: Outlook 
  
Eine kanonische-Eigenschaft ist eine virtuelle Eigenschaft, die ein MAPI-Eigenschaft oder mehrere MAPI-Eigenschaften definiert, mit der gleichen Eigenschaftenbezeichner darstellt. Kanonische Eigenschaften sind nur zur Erleichterung der konsistente Identifizierung der MAPI-Eigenschaften in Diskussionen oder Dokumentation außerhalb Code vorgesehen. Im Gegensatz zu MAPI-defined markierte Eigenschaftennamen sind kanonische Eigenschaftennamen als globale Konstanten in MAPI-Headerdateien nicht definiert.
  
## <a name="naming-conventions"></a>Benennungskonventionen

Kanonische Eigenschaftennamen beginnen mit dem Präfix, "Pid", womit "Eigenschaftenbezeichner." Je nachdem, ob die Eigenschaft eine bereichsspezifische-Eigenschaft, eine benannte Eigenschaft durch eine numerische Kennung oder eine benannte Eigenschaft mit einem Zeichenfolgennamen ist, wird das Präfix weiter als "PidTag," qualifiziert "PidLid" und "PidName" fest. Beispielsweise stellt [PidTagAccount](pidtagaccount-canonical-property.md) die markierten Eigenschaften, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) und **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), die eines Empfängers angeben Kontoname. Die **DispidContacts** -Eigenschaft, eine benannte Eigenschaft an, die einen numerischen Bezeichner hat und den Namen der Kontakte im Zusammenhang mit einer Meldung festlegt, stellt [PidLidContacts](pidlidcontacts-canonical-property.md) dar. und [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) stellt "http://schemas.microsoft.com/outlook/phishingstamp," eine benannte Eigenschaft an, die ein Name vom Typ String hat und die Zeichenfolge Markieren von Nachrichten, die wahrscheinlich Phishing sind angibt. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Ähnliche Eigenschaften, die mithilfe einer Kanonischer-Eigenschaft darstellt

### <a name="identifying-properties-in-mapi"></a>Identifizieren von Eigenschaften in MAPI

Alle Eigenschaften in MAPI werden durch einen Eigenschaftenbezeichner identifiziert, die einen 16-Bit-Wert ohne Vorzeichen ist. Der Bezeichner für die und den Eigenschaftentyp (eine andere nicht signierte 16-Bit-Wert) bilden eine Eigenschaftentag für die Eigenschaft. 
  
MAPI verwendet ein Eigenschaftentag Eigenschaften eindeutig definiert. Eigenschaften, die das gleiche Eigenschafts-Tag, wie **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) und **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) gelten identische Eigenschaften in MAPI. Eine Liste der Eigenschaftentags, die MAPI für ihre eigenen Eigenschaften definiert wurde, finden Sie unter der MAPI-Headerdatei Mapitags.h.
  
Beachten Sie, dass MAPI-IDs in Bereiche unterteilt. Gibt an, bei denen ein Bezeichner des Bereichs liegt, seine Verwendung und den Besitz. Die Eigenschaftenbezeichner der markierten Eigenschaften liegen im Bereich von 0 x 0001 zu 0x7FFF. Innerhalb dieses Bereichs liegen die Eigenschaftenbezeichner der MAPI-benutzerdefinierte Eigenschaften, die im Bereich von 0 x 0001 bis 0x3FFF fallen. Die Eigenschaftenbezeichner eines benannten Eigenschaften rückfalls im Bereich von 0 x 8000 zu 0x8FFF. 
  
Benannte Eigenschaften werden außerdem durch einen Eigenschaftensatz und entweder ein long-ID (Abdeckung), der eine nicht signierte 32-Bit-Wert ist, oder eine Zeichenfolge zugeordnet. Ein Eigenschaftensatz ist eine GUID, die eine Gruppe von benannten Eigenschaften mit einem ähnlichen Zweck identifiziert werden kann. Die Eigenschaftensatz und Abdeckung oder Zeichenfolge Namen dienen zum Abrufen oder Festlegen der benannten Eigenschaft.
  
### <a name="property-type"></a>Eigenschaftentyp

Neben dem Bezeichner ist eine Eigenschaft durch einen Datentyp Ergebnisarray als Attribut zugewiesen, die den Typ der zulässigen Werte für diese Eigenschaft angibt.
  
Für Eigenschaften, die vom Typ String, abhängig von der Unterstützung von Unicode in der zugrunde liegenden Plattform, sind die-Eigenschaft vom Typ PT_STRING8 werden kann (8-Bit-Zeichen Null endende Zeichenfolge) oder PT_UNICODE (Null terminierte Unicode-Zeichenfolge). Eine Eigenschaft mit dem Typ PT_TSTRING definiert werden kann, und von den Einstellungen für Kompilierung, PT_TSTRING wird standardmäßig auf eine Unicode-Zeichenfolge für Plattformen, die Unterstützung für Unicode oder in einen String PT_STRING8 für Plattformen, die ANSI oder DBCS unterstützen. Eine Zeichenfolge typisierten-Eigenschaft ist der Regel wird identifiziert durch drei ähnliche Namen wie **PR_ACCOUNT**, **PR_ACCOUNT_A**und **PR_ACCOUNT_W**, sind vom Typ PT_TSTRING, PT_STRING8 und PT_UNICODE fest.
  
Weitere Informationen zu Eigenschaftstypen und Makros im Zusammenhang mit Typen finden Sie unter der MAPI-Headerdatei Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identifizieren von ähnlichen Eigenschaften

In der aktuellen MAPI-Eigenschaft im Querformat ist es nicht ungewöhnlich, feststellen, dass eine Eigenschaft unter verschiedenen Eigenschaftennamen, ausgesetzt ist die mit der gleichen Eigenschaftenbezeichner definiert sind. Beispielsweise werden die markierten Eigenschaften, **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER**, in Mapitags.h haben den gleichen Eigenschaftenbezeichner und den Typ definiert. Eng mit diesen beiden Eigenschaften sind:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Die Eigenschaften mit dem Suffix "_A" werden als PT_STRING8 eingegeben, und die mit dem Suffix "_W" werden als PT_UNICODE eingegeben.
  
Dient der kanonische **PidTagBusiness2TelephoneNumber** in diesem Beispiel-Eigenschaft zum Verweisen auf eine solche eng verbundenen MAPI-Eigenschaften, die mit einem Bezeichner zu vereinfachen und einheitlich (mit dem Präfix "Pid") über alle MAPI Eigenschaften. Welche realen MAPI-Eigenschaften eine kanonische Eigenschaft darstellt, finden Sie unter [Zuordnen kanonische Eigenschaftennamen MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md). Die kanonische-Eigenschaft, der eine MAPI-Eigenschaft verknüpft ist, finden Sie unter [Zuordnen von MAPI-Objektnamen kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>MAPI-Unterstützung von kanonische Eigenschaftennamen

Da kanonische Eigenschaften keine Real Eigenschaften sind und nicht in MAPI-Headerdateien definiert sind, sollten Sie nicht kanonische Eigenschaftennamen im Code verwenden. Sie sollten fahren Sie stattdessen die genauen Namen der MAPI-Eigenschaft im Code verwenden. Angenommen, können Sie finden Sie unter **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER** außerhalb von Code als **PidTagBusiness2TelephoneNumber**und **PR_BUSINESS2_TELEPHONE_NUMBER** oder **PR_OFFICE2_ verwenden TELEPHONE_NUMBER** im Code. 
  
Wenn Sie kanonische Eigenschaftennamen in Ihrem Code verwenden müssen, müssen Sie zuerst in Ihren eigenen Headerdateien definieren.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Kanonische Eigenschaftsnamen und Exchange-Spezifikationen

Kanonische Namen werden in Microsoft Exchange Server-Spezifikationen verwiesen, die vom Exchange-Server für die Kommunikation mit anderen Microsoft-Produkten verwendet werden. Weitere Informationen zu Nachrichteneigenschaften-Objekt auf die Exchange-Spezifikationen verweist finden Sie unter [[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaftentags](mapi-property-tags.md)
  
[Übersicht über die Bezeichner des MAPI-Eigenschaft](mapi-property-identifier-overview.md)
  
[Übersicht über Typ von MAPI-Eigenschaft](mapi-property-type-overview.md)

