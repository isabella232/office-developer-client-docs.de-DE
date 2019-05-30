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
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540476"
---
# <a name="mapi-canonical-properties"></a>Kanonische MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine kanonische Eigenschaft ist eine virtuelle Eigenschaft, die eine MAPI-Eigenschaft darstellt, oder mehrere MAPI-Eigenschaften, die mit demselben Eigenschaftenbezeichner definiert sind. Kanonische Eigenschaften dienen nur zur Vereinfachung der konsistenten Identifizierung von MAPI-Eigenschaften in Diskussionen oder Dokumentationen außerhalb des Codes. Im Gegensatz zu MAPI-definierten Tagged-Eigenschaftennamen werden kanonische Eigenschaftennamen nicht als globale Konstanten in MAPI-Headerdateien definiert.
  
## <a name="naming-conventions"></a>Benennungskonventionen

Kanonische Eigenschaftennamen beginnen mit dem Präfix "PID", das "Eigenschaftenbezeichner" darstellt. Je nachdem, ob es sich bei der Eigenschaft um eine Tagged-Eigenschaft, eine benannte Eigenschaft mit einem numerischen Bezeichner oder eine benannte Eigenschaft mit einem Zeichenfolgennamen handelt, wird das Präfix weiter als "PidTag", "" PidLid "und" PidName "qualifiziert. [PidTagAccount](pidtagaccount-canonical-property.md) stellt beispielsweise die markierten Eigenschaften, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) und **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)) dar, die den Empfänger angeben. Konto Name; [Pidlidcontacts (](pidlidcontacts-canonical-property.md) stellt die **dispidContacts** -Eigenschaft dar, eine benannte Eigenschaft mit numerischem Bezeichner, die den Namen der Kontakte angibt, die einer Nachricht zugeordnet sind. und [pidnamephishingstamp (](pidnamephishingstamp-canonical-property.md) stellt "http://schemas.microsoft.com/outlook/phishingstamp," eine benannte Eigenschaft mit einem Zeichenfolgennamen dar und gibt die Zeichenfolge an, die Nachrichten markiert, die wahrscheinlich als Phishing eingestuft werden. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Darstellen ähnlicher Eigenschaften mit einer kanonischen Eigenschaft

### <a name="identifying-properties-in-mapi"></a>Identifizieren von Eigenschaften in MAPI

Alle Eigenschaften in MAPI werden durch einen Eigenschaftenbezeichner identifiziert, bei dem es sich um einen unsignierten 16-Bit-Wert handelt. Der Eigenschaftenbezeichner und der Eigenschaftentyp (ein weiterer 16-Bit-Wert ohne Vorzeichen) bilden ein Eigenschaftentag für die Eigenschaft. 
  
MAPI verwendet ein Property-Tag, um Eigenschaften eindeutig zu definieren. Eigenschaften, die dasselbe Eigenschaftentag aufweisen, wie **PR_BUSINESS2_TELEPHONE_NUMBER** ([pidtagbusiness2telephonenumber (](pidtagbusiness2telephonenumber-canonical-property.md)) und **PR_OFFICE2_TELEPHONE_NUMBER** ([pidtagbusiness2telephonenumber (](pidtagbusiness2telephonenumber-canonical-property.md)), gelten als identisch. Eigenschaften in MAPI. Eine Liste der Eigenschaftentags, die von MAPI für eigene Eigenschaften definiert wurden, finden Sie in der MAPI-Headerdatei Mapitags. h.
  
Beachten Sie, dass die Eigenschaftenbezeichner von MAPI in Bereiche unterteilt werden. Wenn ein Bezeichner in den Bereich fällt, wird dessen Verwendung und Besitz angegeben. Die Eigenschaftenbezeichner von getaggten Eigenschaften fallen im Bereich von 0x0001 auf 0x7FFF. Innerhalb dieses Bereichs befinden sich die Eigenschaftenbezeichner von MAPI-definierten Eigenschaften, die im Bereich von 0x0001 zu 0x3FFF liegen. Die Eigenschaftenbezeichner benannter Eigenschaften liegen im Bereich von 0X8000 bis 0x8FFF. 
  
Benannte Eigenschaften werden zusätzlich durch einen Eigenschaftensatz und entweder eine lange ID (LID), bei der es sich um einen unsignierten 32-Bit-Wert handelt, oder eine Zeichenfolge zurückgegeben. Ein Eigenschaftenset ist eine GUID, die eine Gruppe benannter Eigenschaften mit einem ähnlichen Zweck identifiziert. Die Eigenschaftengruppe und der Deckel oder der Zeichenfolgenname werden verwendet, um die benannte Eigenschaft abzurufen oder festzulegen.
  
### <a name="property-type"></a>Eigenschaftentyp

Abgesehen von Bezeichnern wird eine Eigenschaft von einem Datentyp attributiert, der den Typ der für diese Eigenschaft zulässigen Werte angibt.
  
Bei Eigenschaften des Typs String kann die Eigenschaft in Abhängigkeit von der Unterstützung für Unicode in der zugrunde liegenden Plattform vom Typ PT_String8 (NULL-terminierte 8-Bit-Zeichenfolge) oder PT_UNICODE (NULL-terminierte Unicode-Zeichenfolge) sein. Eine Eigenschaft kann mit dem PT_TSTRING-Typ definiert werden, und in Abhängigkeit von den Kompilierungseinstellungen wird für PT_TSTRING standardmäßig eine Unicode-Zeichenfolge für Plattformen verwendet, die Unicode unterstützen, oder eine PT_String8-Zeichenfolge für Plattformen, die ANSI oder DBCS unterstützen. Es ist üblich, dass eine Zeichenfolge typisierte Eigenschaft durch drei ähnliche Namen wie **PR_ACCOUNT**, **PR_ACCOUNT_A**und **PR_ACCOUNT_W**identifiziert wird, die vom Typ PT_TSTRING, PT_STRING8 und PT_UNICODE jeweils sind.
  
Weitere Informationen zu Eigenschaftentypen und Makros im Zusammenhang mit Typen finden Sie in der MAPI-Headerdatei Mapidefs. h.
  
### <a name="identifying-similar-properties"></a>Identifizieren ähnlicher Eigenschaften

In der aktuellen MAPI-Eigenschafts Landschaft ist es nicht ungewöhnlich festzustellen, dass eine Eigenschaft unter anderen Eigenschaftennamen verfügbar gemacht wurde, die alle mit demselben Eigenschaftenbezeichner definiert sind. Beispielsweise sind die getaggten Eigenschaften **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER**in Mapitags. h so definiert, dass Sie denselben Eigenschaftenbezeichner und Typ aufweisen. Eng mit diesen beiden Eigenschaften verbunden sind:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Die Eigenschaften mit dem Suffix "_A" werden als PT_String8 typisiert, und diejenigen mit dem Suffix "_W" werden als PT_UNICODE eingegeben.
  
Der Zweck einer kanonischen Eigenschaft, **pidtagbusiness2telephonenumber (** in diesem Beispiel, besteht darin, die Referenzierung solcher eng angegliederter MAPI-Eigenschaften mithilfe eines Bezeichners und in einer konsistenten Weise (unter Verwendung des Präfix "PID") für alle MAPI-Zwecke zu vereinfachen. Eigenschaften. Informationen zu den tatsächlichen MAPI-Eigenschaften, die eine kanonische Eigenschaft darstellt, finden Sie unter [Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md). Informationen zur kanonischen Eigenschaft, der eine MAPI-Eigenschaft zugeordnet ist, finden Sie unter [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>MAPI-Unterstützung von kanonischen Eigenschaftennamen

Da kanonische Eigenschaften keine echten Eigenschaften sind und nicht in MAPI-Headerdateien definiert sind, sollten Sie keine kanonischen Eigenschaftennamen in Code verwenden. Stattdessen sollten Sie weiterhin die genauen MAPI-Eigenschaftennamen im Code verwenden. Sie können beispielsweise **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER** außerhalb von Code als **pidtagbusiness2telephonenumber (** referieren und entweder **PR_BUSINESS2_TELEPHONE_NUMBER** oder PR_OFFICE2_ verwenden. ** TELEPHONE_NUMBER** im Code. 
  
Wenn Sie kanonische Eigenschaftennamen in Ihrem Code verwenden müssen, müssen Sie diese zunächst in ihren eigenen Headerdateien definieren.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Kanonische Eigenschaftennamen und Exchange-Protokollspezifikationen

In Exchange Server Protokollspezifikationen wird auf kanonische Namen verwiesen, die von Exchange Server für die Kommunikation mit anderen Microsoft-Produkten verwendet werden. Weitere Informationen zu Nachrichtenobjekt Eigenschaften, auf die durch die Exchange-Protokollspezifikationen verwiesen wird, finden Sie unter [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschafts Tags](mapi-property-tags.md)
  
[MAPI-Eigenschaftenbezeichner (Übersicht)](mapi-property-identifier-overview.md)
  
[Übersicht über MAPI-Eigenschaftentypen](mapi-property-type-overview.md)

