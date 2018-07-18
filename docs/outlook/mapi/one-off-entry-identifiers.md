---
title: Einmaligen-Eintragsbezeichner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 1335de3c1decf6c594f0148fbbf055061d7ce7e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793293"
---
# <a name="one-off-entry-identifiers"></a>Einmaligen-Eintragsbezeichner
  
**Betrifft**: Outlook 
  
Einmaligen-Eintragsbezeichner werden erstellt, indem MAPI in der **IAddrBook::CreateOneOff** -Methode und Komponenten, die keinen Zugriff auf die MAPI-Subsystems, wie beispielsweise Gateway-Komponenten. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). Die folgende Abbildung zeigt das Format einer einmaligen Eintrags-ID an.
  
**Format von Eintragsbezeichner mit einmaliger Eingabe**
  
![Format von Eintragsbezeichner mit Einmaliger Eingabe] (media/amapi_69.gif "Format von Eintragsbezeichner mit Einmaliger Eingabe")
  
Das erste Feld ist eine spezielle [MAPIUID](mapiuid.md) -Struktur, die Eintrags-ID als einen benutzerdefinierten Empfänger Darstellung angibt. Diese Struktur **MAPIUID** muss auf die Konstante MAPI_ONE_OFF_UID festgelegt werden. MAPI_ONE_OFF_UID ist in der Headerdatei MAPIDEFS definiert. H. 
  
Die Version und die Kennzeichen Felder sind Wörter 16-Bit-Intel-Byte-Reihenfolge. Das Versionsfeld muss auf 0 (null) festgelegt werden. Das Flags-Feld kann auf die folgenden Werte festgelegt werden:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
Das Flag MAPI_ONE_OFF_NO_RICH_INFO wird festgelegt, wenn ein Empfänger nicht Nachrichteninhalt in Transport Neutral Encapsulation Format (TNEF) empfangen sollen. Dieses Kennzeichen werden festgelegt, wenn MAPI_SEND_NO_RICH_INFO [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) -Methode übergeben wird. 
  
Das Flag MAPI_ONE_OFF_UNICODE wird festgelegt, wenn der Anzeigename und e-Mail-Adresse Unicode-Zeichenfolgen werden. Dieses Kennzeichen werden festgelegt, wenn der Parameter MAPI_UNICODE an **IAddrBook::CreateOneOff**übergeben wird. Wenn die Option MAPI_UNICODE nicht an **CreateOneOff**übergeben wird, wird MAPI davon ausgegangen, dass die Zeichenfolgen Display Name und e-Mail-Adresse der Arbeitsstation aktuellen ANSI-Zeichensatz sind. ANSI-Zeichenfolgen in der Regel funktionieren nicht, auch in Nachrichten, die zwischen Plattformen unterschiedliche Zeichensätze verwenden, da die Codepage nicht in die Eintrags-ID codiert wird gesendet werden. Zum Schutz gegen diese potenziellen Inkompatibilität sind viele-Adresstypen auf nur die Zeichen, die für mehrere Zeichensätze sind beschränkt. Um Character Set und Plattform-Kompatibilität zu gewährleisten, sollten Clients jedoch Unicode für die Zeichenfolgen in ihren Nachrichten verwenden.
  
Der Anzeigename ist eine Null endende Zeichenfolge, die die Eigenschaft des Empfängers **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und an den _Wert_ -Parameter übergeben **IAddrBook::CreateOneOff**entspricht. Der Zeichensatz ist Unicode, wenn das Flag MAPI_ONE_OFF_UNICODE-Satz und ANSI ist, wenn es deaktiviert ist. 
  
Der Adresstyp ist eine Null endende Zeichenfolge, die die Eigenschaft des Empfängers **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) und an den _LpszAdrType_ -Parameter übergeben **IAddrBook::CreateOneOff**entspricht. 
  
Die e-Mail-Adresse ist eine Null endende Zeichenfolge, die die Eigenschaft des Empfängers **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) und an den _LpszAddress_ -Parameter übergeben **IAddrBook::CreateOneOff**entspricht. 
  
> [!NOTE]
> Es ist keine Textabstand in Eingangs Bezeichner Strukturen. die Bytes genau wie oben angegebenen verpackt wurden und die Eintrags-ID Länge sollte keine Bytes hinter dem Abbruch Null-Zeichen, der die e-Mail-Adresse enthalten. 
  
Clients und adressbuchanbietern implementierte, die manuell einmaligen-Eintragsbezeichner konstruieren müssen möglicherweise auch zum Generieren von Werten für die **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaften. Der Datensatzschlüssel ist identisch mit der Eintrags-ID. Die suchen-Taste sollte durch Verketten die folgenden Felder in der folgenden Reihenfolge gebildet werden:
  
1. Der Adresstyp in Großbuchstaben konvertiert.
    
2. Ein Doppelpunkt (:)).
    
3. Die e-Mail-Adresse in Großbuchstaben umgewandelt wurde.
    
4. Ein Abbruch Null-Zeichen.
    
Keine Character Set Konvertierung muss beim Generieren des Schlüssels Suche ausgeführt wird.
  

