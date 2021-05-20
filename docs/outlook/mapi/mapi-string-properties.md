---
title: EIGENSCHAFTEN DER MAPI-Zeichenfolge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431393"
---
# <a name="mapi-string-properties"></a>EIGENSCHAFTEN DER MAPI-Zeichenfolge

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet drei verschiedene Eigenschaftstypen zum Beschreiben von Zeichenfolgeneigenschaften:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Zeichenfolgeneigenschaften werden am häufigsten als PT_TSTRING. Der PT_TSTRING-Eigenschaftstyp wird abhängig davon, ob das UNICODE-Makro definiert wurde, bedingt in einen der anderen Zeichenfolgeneigenschaftstypen kompiliert. PT_STRING8 beschreibt 8-Bit-Zeichenzeichenfolgen mit Null-Termin im ANSI-Format. PT_UNICODE beschreibt Zeichenfolgen mit Nullenendzeichen mit Doppel-Byte. 
  
Entweder ein Client oder ein Dienstanbieter, oder Client und Anbieter können Unicode-Zeichenzeichenfolgen unterstützen. Sie ist nicht erforderlich. Ein Client, der nur PT_STRING8 Zeichenfolgen unterstützt, kann mit einem Anbieter arbeiten, der Unicode unterstützt und umgekehrt. Um diese Interoperabilität zu aktivieren, übergeben Clients und Dienstanbieter ein Flag, das MAPI_UNICODE-Flag, um anzugeben, dass Unicode in Methoden unterstützt wird, die den Austausch von Zeichenzeichenfolgen beinhalten. 
  
Angenommen, ein Client unterstützt Unicode und muss den Anzeigenamen eines Ordners abrufen. Alle Eigenschaften des Clients PT_TSTRING zum Eingeben von PT_UNICODE. Wenn der Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Ordners aufruft, um seine **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft abzurufen, übergibt er das MAPI_UNICODE-Flag, um an die Anforderung zu senden, dass die Anzeigenamenzeichenfolge im Unicode-Format zurückgegeben wird. 
  
Clients und Dienstanbieter müssen beachten, dass das Angeben eines Zeichensatzs in einem Methodenaufruf nur eine Anforderung ist. Die Unterstützung eines oder beider Zeichensätze liegt beim Implementier des Objekts. Dienstanbieter werden jedoch ermutigt, beide Zeichensätze zu unterstützen, da sie dadurch eine breitere Verteilung erzielen können als Anbieter, die nur einen Satz unterstützen. 
  
Zeichenfolgeneigenschaften können relativ groß werden, ebenso wie binäre Eigenschaften – Eigenschaften, die den Eigenschaftentyp PT_BINARY. Um das Arbeiten mit großen Eigenschaften zu erleichtern, ermöglicht MAPI Dienstanbietern das Festlegen dieser Eigenschaften, um Größenbeschränkungen zu erzwingen. Diese Grenzwerte können je nach Folgenden variieren:
  
- Gibt an, ob die Eigenschaften gelesen oder geschrieben werden.
    
- Implementierung der **IMAPIProp-Methoden** durch den Dienstanbieter. 
    
- Überlegungen zur Laufzeit, z. B. Speichereinschränkungen.
    
- Übersetzungsprobleme mit Zeichensatz. 
    
Größenbeschränkungen können auch für Zeichenfolgen- und Binäreigenschaften festgelegt werden, wenn sie im Spaltensatz einer Tabelle verwendet werden, da es manchmal unmöglich ist, den Wert einer großen Eigenschaft sichtbar zu machen. Viele Dienstanbieter kürzen große Zeichenfolgen- oder Binäreigenschaften, die in Tabellen verwendet werden, auf 255 Byte. 
  
Wenn ein Client die **GetProps-** oder **SetProps-Methode** eines Objekts aufruft, um mit einer großen Zeichenfolge oder binären Eigenschaft zu arbeiten, und der Aufruf aufgrund der Eigenschaftsgröße fehlschlägt, gibt die Methode den Fehlerwert MAPI_E_NOT_ENOUGH_MEMORY. Wenn **getProps** für eine bestimmte Eigenschaft einen Fehler hat, kann der Client wiederhergestellt werden, indem [er IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufruft und den **IStream** für den Zugriff anfordert, indem IID_IStream als Schnittstellenbezeichner angegeben wird. Mithilfe **von OpenProperty** kann der Client eine große Eigenschaft über eine Schnittstelle wie **IStream** abrufen, die besser für das Arbeiten mit großen Eigenschaften geeignet ist. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

