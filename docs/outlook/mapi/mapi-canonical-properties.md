---
title: KANonische MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb0d0efe3eb0b6b9ec81fd0bff9a0893c3b950c7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595896"
---
# <a name="mapi-canonical-properties"></a>KANonische MAPI-Eigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine kanonische Eigenschaft ist eine virtuelle Eigenschaft, die eine MAPI-Eigenschaft oder mehrere MAPI-Eigenschaften darstellt, die mit demselben Eigenschaftenbezeichner definiert sind. Kanonische Eigenschaften sollen nur die konsistente Identifizierung von MAPI-Eigenschaften in Diskussionen oder Dokumentationen außerhalb des Codes ermöglichen. Im Gegensatz zu mapidefinierten Eigenschaftsnamen werden kanonische Eigenschaftennamen in MAPI-Headerdateien nicht als globale Konstanten definiert.
  
## <a name="naming-conventions"></a>Namenskonventionen

Kanonische Eigenschaftennamen beginnen mit dem Präfix "Pid", das "Eigenschaftsbezeichner" darstellt. Je nachdem, ob es sich bei der Eigenschaft um eine markierte Eigenschaft, eine benannte Eigenschaft mit einem numerischen Bezeichner oder eine benannte Eigenschaft mit einem Zeichenfolgennamen handelt, wird das Präfix weiter als "PidTag", "PidLid" und "PidName" qualifiziert. [PidTagAccount](pidtagaccount-canonical-property.md) stellt beispielsweise die markierten Eigenschaften **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) und **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)) dar, die den Kontonamen eines Empfängers angeben. [PidLidContacts](pidlidcontacts-canonical-property.md) stellt die **dispidContacts-Eigenschaft** dar, eine benannte Eigenschaft mit einem numerischen Bezeichner, die den Namen der einer Nachricht zugeordneten Kontakte angibt. und [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) stellt http://schemas.microsoft.com/outlook/phishingstamp "," eine benannte Eigenschaft mit einem Zeichenfolgennamen dar, die die Zeichenfolge zum Markieren von Nachrichten angibt, die wahrscheinlich Phishing sind. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Darstellen ähnlicher Eigenschaften mithilfe einer kanonischen Eigenschaft

### <a name="identifying-properties-in-mapi"></a>Identifizieren von Eigenschaften in MAPI

Alle Eigenschaften in der MAPI werden durch einen Eigenschaftsbezeichner identifiziert, bei dem es sich um einen nicht signierten 16-Bit-Wert handelt. Der Eigenschaftsbezeichner und der Eigenschaftentyp (ein weiterer nicht signierter 16-Bit-Wert) bilden ein Eigenschaftstag für die Eigenschaft. 
  
MAPI verwendet ein Eigenschaftstag, um Eigenschaften eindeutig zu definieren. Eigenschaften mit demselben Eigenschaftentag, z. **B. PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) und **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), werden als identische Eigenschaften in MAPI betrachtet. Eine Liste der Eigenschaftentags, die MAPI für ihre eigenen Eigenschaften definiert hat, finden Sie in der MAPI-Headerdatei Mapitags.h.
  
Beachten Sie, dass die MAPI Eigenschaftsbezeichner in Bereiche unterteilt. Wenn ein Bezeichner in den Bereich fällt, gibt dies die Verwendung und den Besitz an. Die Eigenschaftsbezeichner von markierten Eigenschaften liegen im Bereich der 0x0001 bis 0x7FFF. Innerhalb dieses Bereichs befinden sich die Eigenschaftsbezeichner von MAPI-definierten Eigenschaften, die in den Bereich der 0x0001 0x3FFF fallen. Die Eigenschaftsbezeichner benannter Eigenschaften liegen im Bereich von 0x8000 bis 0x8FFF. 
  
Benannte Eigenschaften werden zusätzlich von einem Eigenschaftensatz und entweder einer langen ID (LID) zugeordnet, bei der es sich um einen nicht signierten 32-Bit-Wert handelt, oder einer Zeichenfolge. Ein Eigenschaftensatz ist eine GUID, die eine Gruppe benannter Eigenschaften mit einem ähnlichen Zweck identifiziert. Der Eigenschaftensatz und der LID- oder Zeichenfolgenname werden verwendet, um die benannte Eigenschaft abzurufen oder festzulegen.
  
### <a name="property-type"></a>Eigenschaftentyp

Abgesehen von Bezeichnern wird eine Eigenschaft durch einen Datentyp attributiert, der den Typ der für diese Eigenschaft zulässigen Werte angibt.
  
Bei Eigenschaften vom Zeichenfolgentyp kann die Eigenschaft abhängig von der Unterstützung für Unicode in der zugrunde liegenden Plattform vom Typ PT_STRING8 (mit Null beendete 8-Bit-Zeichenzeichenfolge) oder PT_UNICODE (Unicode-Zeichenfolge mit NULL-Terminierung) sein. Eine Eigenschaft kann mit dem PT_TSTRING Typ definiert werden, und je nach Kompilierungseinstellungen ist PT_TSTRING standardmäßig eine Unicode-Zeichenfolge für Plattformen, die Unicode unterstützen, oder eine PT_STRING8 Zeichenfolge für Plattformen, die ANSI oder DBCS unterstützen. Es ist üblich, dass eine Eigenschaft mit Zeichenfolgentyp durch drei ähnliche Namen identifiziert wird, z. **B. PR_ACCOUNT,** **PR_ACCOUNT_A** und **PR_ACCOUNT_W,** die vom Typ PT_TSTRING, PT_STRING8 und PT_UNICODE sind.
  
Weitere Informationen zu Eigenschaftstypen und Makros im Zusammenhang mit Typen finden Sie in der MAPI-Headerdatei Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identifizieren ähnlicher Eigenschaften

In der aktuellen MAPI-Eigenschaftenlandschaft ist es nicht ungewöhnlich, dass eine Eigenschaft unter verschiedenen Eigenschaftennamen verfügbar gemacht wurde, die alle mit demselben Eigenschaftsbezeichner definiert sind. Beispielsweise werden die markierten Eigenschaften **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER** in Mapitags.h so definiert, dass sie denselben Eigenschaftsbezeichner und -typ aufweisen. Eng mit diesen beiden Eigenschaften verbunden sind:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Die Eigenschaften mit dem Suffix "_A" werden als PT_STRING8 eingegeben, und die Eigenschaften mit dem Suffix "_W" werden als PT_UNICODE eingegeben.
  
Der Zweck einer kanonischen Eigenschaft, **PidTagBusiness2TelephoneNumber** in diesem Beispiel, besteht darin, das Verweisen auf so eng verbundene MAPI-Eigenschaften mit einem Bezeichner und auf konsistente Weise (unter Verwendung des Präfixes "Pid") über alle MAPI-Eigenschaften hinweg zu vereinfachen. Informationen dazu, welche echten MAPI-Eigenschaften eine kanonische Eigenschaft darstellt, finden Sie unter [Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen.](mapping-canonical-property-names-to-mapi-names.md) Informationen zur Suche nach der kanonischen Eigenschaft, der eine MAPI-Eigenschaft zugeordnet ist, finden Sie unter [Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen.](mapping-mapi-names-to-canonical-property-names.md)
  
## <a name="mapi-support-of-canonical-property-names"></a>MAPI-Unterstützung kanonischer Eigenschaftennamen

Da kanonische Eigenschaften keine realen Eigenschaften sind und nicht in MAPI-Headerdateien definiert sind, sollten Sie im Code keine kanonischen Eigenschaftennamen verwenden. Stattdessen sollten Sie weiterhin die genauen MAPI-Eigenschaftsnamen im Code verwenden. Sie können beispielsweise **PR_BUSINESS2_TELEPHONE_NUMBER** und **PR_OFFICE2_TELEPHONE_NUMBER** außerhalb des Codes als **PidTagBusiness2TelephoneNumber** bezeichnen und im Code **entweder PR_BUSINESS2_TELEPHONE_NUMBER** oder **PR_OFFICE2_TELEPHONE_NUMBER** verwenden. 
  
Wenn Sie kanonische Eigenschaftennamen in Ihrem Code verwenden müssen, müssen Sie sie zuerst in Ihren eigenen Headerdateien definieren.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Kanonische Eigenschaftennamen und Exchange-Protokollspezifikationen

Auf kanonische Namen wird in Microsoft Exchange Server Protokollspezifikationen verwiesen, die von Exchange Server für die Kommunikation mit anderen Microsoft-Produkten verwendet werden. Weitere Informationen zu Nachrichtenobjekteigenschaften, auf die von Exchange Protokollspezifikationen verwiesen wird, finden Sie unter [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch



[MAPI-Eigenschaftstags](mapi-property-tags.md)
  
[Übersicht über mapi-Eigenschaftsbezeichner](mapi-property-identifier-overview.md)
  
[Übersicht über mapi-Eigenschaftstypen](mapi-property-type-overview.md)

