---
title: MAPI-Zeichenfolgeneigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c6a8594e0849a500146842254feb95ee6ffc2c27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600799"
---
# <a name="mapi-string-properties"></a>MAPI-Zeichenfolgeneigenschaften

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI bietet drei verschiedene Eigenschaftstypen, um Zeichenfolgeneigenschaften zu beschreiben:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Zeichenfolgeneigenschaften werden am häufigsten als PT_TSTRING definiert. Der PT_TSTRING Eigenschaftstyp wird bedingt zu einem der anderen Zeichenfolgeneigenschaftentypen kompiliert, je nachdem, ob das UNICODE-Makro definiert wurde. PT_STRING8 beschreibt zeichenfolgen mit 8-Bit-Null-Terminen im ANSI-Format; PT_UNICODE beschreibt Zeichenfolgen mit Doppeltbyte-Null-Endung. 
  
Entweder ein Client oder ein Dienstanbieter oder client- und anbieterseitig können Unicode-Zeichenzeichenfolgen unterstützen. Dies ist nicht erforderlich. Ein Client, der nur PT_STRING8 Zeichenfolgen unterstützt, kann mit einem Anbieter arbeiten, der Unicode unterstützt und umgekehrt. Um diese Interoperabilität zu aktivieren, übergeben Clients und Dienstanbieter ein Flag, das MAPI_UNICODE Flag, um anzugeben, dass Unicode in Methoden unterstützt wird, die den Austausch von Zeichenzeichenfolgen umfassen. 
  
Angenommen, ein Client unterstützt Unicode und muss den Anzeigenamen eines Ordners abrufen. Alle PT_TSTRING Eigenschaften des Clients werden kompiliert, um PT_UNICODE einzugeben. Wenn der Client die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Ordners aufruft, um seine **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft abzurufen, übergibt er das flag MAPI_UNICODE, um anzufordern, dass die Anzeigenamenzeichenfolge im Unicode-Format zurückgegeben wird. 
  
Clients und Dienstanbieter müssen beachten, dass das Angeben eines Zeichensatzes in einem Methodenaufruf nur eine Anforderung ist. Die Unterstützung eines oder beider Zeichensätze obliegt dem Implementierer des Objekts. Dienstanbieter werden jedoch aufgefordert, beide Zeichensätze zu unterstützen, da sie eine größere Verteilung erzielen können als Anbieter, die nur einen Satz unterstützen. 
  
Zeichenfolgeneigenschaften können sehr groß werden, ebenso wie binäre Eigenschaften – Eigenschaften, die den Eigenschaftstyp PT_BINARY verwenden. Um die Arbeit mit großen Eigenschaften zu vereinfachen, ermöglicht MAPI Dienstanbietern das Festlegen dieser Eigenschaften, um Größenbeschränkungen zu erzwingen. Diese Grenzwerte können je nach:
  
- Gibt an, ob die Eigenschaften gelesen oder geschrieben werden.
    
- Implementierung der **IMAPIProp-Methoden** durch den Dienstanbieter. 
    
- Überlegungen zur Laufzeit, z. B. Speichereinschränkungen.
    
- Probleme bei der Übersetzung von Zeichensatz. 
    
Größenbeschränkungen können auch auf Zeichenfolgen- und binäre Eigenschaften angewendet werden, wenn sie in der Spaltengruppe einer Tabelle verwendet werden, da es manchmal unmöglich ist, den gesamten Wert einer großen Eigenschaft sichtbar zu machen. Viele Dienstanbieter kürzen große Zeichenfolgen- oder binäre Eigenschaften, die in Tabellen verwendet werden, auf 255 Bytes. 
  
Wenn ein Client die **GetProps- oder SetProps-Methode** eines Objekts **aufruft,** um mit einer großen Zeichenfolge oder binären Eigenschaft zu arbeiten, und der Aufruf aufgrund der Eigenschaftsgröße fehlschlägt, gibt die Methode den Fehlerwert MAPI_E_NOT_ENOUGH_MEMORY zurück. Wenn **getProps** für eine bestimmte Eigenschaft fehlschlägt, kann der Client dies wiederherstellen, indem [er IMAPIProp::OpenProperty](imapiprop-openproperty.md) aufruft und den **IStream** für den Zugriff anfordert, indem IID_IStream als Schnittstellenbezeichner angegeben wird. Mit **OpenProperty** kann der Client eine große Eigenschaft mithilfe einer Schnittstelle wie **IStream** abrufen, die besser für die Arbeit mit großen Eigenschaften geeignet ist. 
  
## <a name="see-also"></a>Siehe auch



[Übersicht über die MAPI-Eigenschaft](mapi-property-overview.md)

