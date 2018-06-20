---
title: MAPI-Eigenschaften
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3cf118866bbc305678201a42a9a91998334f5cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793090"
---
# <a name="mapi-string-properties"></a>MAPI-Eigenschaften

  
  
**Betrifft**: Outlook 
  
MAPI bietet drei verschiedene Eigenschaftstypen um Zeichenfolgeneigenschaften beschrieben:
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
Zeichenfolgeneigenschaften werden am häufigsten als PT_TSTRING definiert. Der Eigenschaftentyp PT_TSTRING kompiliert bedingt auf eine der anderen Zeichenfolge Eigenschaftentypen, je nachdem, je nachdem, ob das Unicode-Makro definiert wurde. PT_STRING8 beschreibt 8-Bit-Null endende Zeichenfolgen in ANSI-Format. PT_UNICODE beschreibt Doppelbyte-Null endende Zeichenfolgen. 
  
Zur Unterstützung von Unicode-Zeichenfolgen können entweder ein Client oder einem-Dienstanbieter oder sowohl Client und Anbieter auswählen. Es ist nicht erforderlich. Ein Client, der nur für Zeichenfolgen PT_STRING8 unterstützt, kann mit einem Anbieter ausgeführt werden, der Unicode und umgekehrt unterstützt. Um diese Interoperabilität zu aktivieren, übergeben Sie Clients und Dienstanbieter ein Kennzeichen, die Option MAPI_UNICODE, um anzugeben, dass Unicode in Methoden unterstützt wird, die den Austausch von Zeichenfolgen betreffen. 
  
Nehmen wir beispielsweise bei einem Client unterstützt Unicode und den Anzeigenamen eines Ordners abrufen muss. Alle Eigenschaften für den Client PT_TSTRING werden zur Eingabe von PT_UNICODE kompiliert. Wenn der Client den Ordner [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen von dessen **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft aufruft, übergibt sie die Option MAPI_UNICODE um anzufordern, dass die Zeichenfolge des Anzeigenamens in das Unicode-Format zurückgegeben werden soll . 
  
Clients und -Dienstanbieter müssen berücksichtigen, die Angabe eines Zeichensatzes in einem Methodenaufruf wird nur eine Anforderung. Unterstützung einer oder beide Zeichensätze ist die Implementierung des Objekts. Dienstanbieter werden jedoch empfohlen, beide Zeichensätze, da es ermöglicht es ihnen, mehr Verbreitung als Anbieter zu erzielen, die nur einen Satz zu unterstützen. 
  
Zeichenfolgeneigenschaften anwachsen können sehr groß sein, da binäre Eigenschaften können – Geben Sie PT_BINARY Eigenschaften, die die-Eigenschaft verwenden. Zum Vereinfachen der Arbeit mit großen Eigenschaften kann MAPI-Dienstanbieter Festlegen dieser Eigenschaften zum Erzwingen von größenbeschränkungen für Nachrichten. Diese Grenzwerte können variieren je nach:
  
- Gibt an, ob die Eigenschaften werden gelesenen oder geschriebenen.
    
- Wie der Dienstanbieter die **IMAPIProp** Methoden implementiert. 
    
- Common Language Runtime Aspekte wie Speicherkapazität.
    
- Zeichensatz Übersetzungsfehler. 
    
Größenbeschränkungen für Nachrichten auch auf Zeichenfolge platziert werden können und binäre Eigenschaften, wenn sie in der Spalte verwendet werden Festlegen einer Tabelle, da es in einigen Fällen nicht möglich, alle große den Wert einer Eigenschaft sichtbar zu machen ist. Viele Dienstanbieter Abschneiden großen Zeichenfolge oder binäre Eigenschaften, die in den Tabellen auf 255 Byte verwendet werden. 
  
Wenn ein Client ein Objekt **GetProps** oder **SetProps** -Methode zum Arbeiten mit einer großen Zeichenfolge oder eine binäre Eigenschaft ruft und der Aufruf, aufgrund der Eigenschaftsgröße fehlschlägt, gibt die Methode den Fehlerwert MAPI_E_NOT_ENOUGH_MEMORY zurück. Wenn es **GetProps** , die für eine bestimmte Eigenschaft ein Fehler aufgetreten ist ist, kann der Client wiederhergestellt werden durch Aufrufen von [IMAPIProp::OpenProperty](imapiprop-openproperty.md) und **IStream** für den Zugriff durch Angeben von IID_IStream als Schnittstellenbezeichner anfordern. **OpenProperty**verwenden, kann der Client abrufen eine große Eigenschaft über die eine Schnittstelle wie **IStream** , der besser für das Arbeiten mit großen Eigenschaften geeignet ist. 
  
## <a name="see-also"></a>Siehe auch



[�bersicht �ber die MAPI-Eigenschaft](mapi-property-overview.md)

