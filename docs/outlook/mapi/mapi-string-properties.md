---
title: MAPI-Zeichenfolgeneigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309520"
---
# <a name="mapi-string-properties"></a>MAPI-Zeichenfolgeneigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet drei verschiedene Eigenschaftstypen zur Beschreibung von Zeichenfolgeneigenschaften:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Zeichenfolgeneigenschaften werden am häufigsten als PT_TSTRING definiert. Der PT_TSTRING-Eigenschafts wird abhängig davon, ob das Unicode-Makro definiert wurde, auf einen der anderen Eigenschaftentypen der Zeichenfolge festgelegt. PT_STRING8 beschreibt 8-Bit-NULL-terminierte Zeichenfolgen im ANSI-Format; PT_UNICODE beschreibt Double-Byte-Zeichenfolgen mit nullabschluss. 
  
Entweder ein Client oder ein Dienstanbieter oder sowohl Client als auch Anbieter können Unicode-Zeichenfolgen unterstützen. Er ist nicht erforderlich. Ein Client, der nur PT_STRING8-Zeichenfolgen unterstützt, kann mit einem Anbieter betrieben werden, der Unicode unterstützt und umgekehrt. Um diese Interoperabilität zu aktivieren, geben Clients und Dienstanbieter ein Flag, das MAPI_UNICODE-Flag, an, um anzugeben, dass Unicode in Methoden unterstützt wird, die den Austausch von Zeichen Zeichenfolgen beinhalten. 
  
Angenommen, ein Client unterstützt Unicode und muss den Anzeigenamen eines Ordners abrufen. Alle PT_TSTRING-Eigenschaften des Clients werden in den Typ PT_UNICODE kompiliert. Wenn der Client die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Ordners zum Abrufen seiner **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft AUFruft, übergibt er das MAPI_UNICODE-Flag, um anzufordern, dass die Zeichenfolge für den Anzeigenamen im Unicode-Format zurückgegeben wird. . 
  
Clients und Dienstanbieter müssen sich darüber im klaren sein, dass das Angeben eines Zeichensatzes in einem Methodenaufruf nur eine Anforderung ist. Für die Unterstützung eines oder beider Zeichensätze gilt die Implementierung des Objekts. Dienstanbieter werden jedoch ermutigt, beide Zeichensätze zu unterstützen, da Sie eine breitere Verteilung erzielen können als Anbieter, die nur einen Satz unterstützen. 
  
Zeichenfolgeneigenschaften können relativ groß werden, da Sie binäre Eigenschaften aufweisen können – Eigenschaften, die den Eigenschaftentyp PT_BINARY verwenden. Um das Arbeiten mit großen Eigenschaften zu erleichtern, ermöglicht MAPI Dienstanbietern das Festlegen dieser Eigenschaften, um Größenbeschränkungen zu erzwingen. Diese Grenzwerte können je nach:
  
- Gibt an, ob die Eigenschaften gelesen oder geschrieben werden.
    
- Wie der Dienstanbieter die **IMAPIProp** -Methoden implementiert. 
    
- Überlegungen zur Laufzeit, wie etwa Arbeitsspeichereinschränkungen.
    
- Übersetzungsprobleme in Zeichensätzen. 
    
Größenbeschränkungen können auch für String-und Binary-Eigenschaften festgelegt werden, wenn Sie im Spaltensatz einer Tabelle verwendet werden, da es manchmal unmöglich ist, den Wert einer großen Eigenschaft sichtbar zu machen. Viele Dienstanbieter kürzen große Zeichenfolgen-oder binäre Eigenschaften, die in Tabellen verwendet werden, auf 255 Byte. 
  
Wenn ein Client die getProps **** -oder SetProps-Methode eines Objekts aufruft, um mit einer großen Zeichenfolge oder binären Eigenschaft zu arbeiten, und der Aufruf aufgrund der Eigenschaftsgröße fehlschlägt, gibt die Methode den Fehlerwert MAPI_E_NOT_ENOUGH_MEMORY zurück. **** Wenn es sich **** um GetProps handelt, das für eine bestimmte Eigenschaft fehlschlägt, kann der Client die Wiederherstellung durch Aufrufen von [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) und das Anfordern von **IStream** für den Zugriff durch Angeben von IID_IStream als Schnittstellenbezeichner. Mit **OpenProperty**kann der Client eine umfangreiche Eigenschaft mithilfe einer Schnittstelle wie **IStream** abrufen, die für das Arbeiten mit umfangreichen Eigenschaften besser geeignet ist. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

