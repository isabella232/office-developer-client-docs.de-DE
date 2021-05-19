---
title: Bezeichner für Einmal-Einträge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: abe52cb45e13e6713d28fffe379e245e2483bffa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411043"
---
# <a name="one-off-entry-identifiers"></a>Bezeichner für Einmal-Einträge
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
One-off-Eintragsbezeichner werden von MAPI in der **IAddrBook::CreateOneOff-Methode** und von Komponenten erstellt, die keinen Zugriff auf das MAPI-Subsystem haben, z. B. Gatewaykomponenten. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). Die folgende Abbildung zeigt das Format einer einmal verwendeten Eintrags-ID.
  
**Format von Eintragsbezeichner mit einmaliger Eingabe**
  
![One-off Entry Identifier Format](media/amapi_69.gif "One-off Entry Identifier Format")
  
Das erste Feld ist eine spezielle [MAPIUID-Struktur,](mapiuid.md) die den Eintragsbezeichner als darstellung eines benutzerdefinierten Empfängers identifiziert. Diese **MAPIUID-Struktur** muss auf die Konstante festgelegt MAPI_ONE_OFF_UID. MAPI_ONE_OFF_UID wird in der Headerdatei MAPIDEFS.H definiert. 
  
Die Versions- und Kennzeichenfelder sind 16-Bit-Wörter in Intel-Bytereihenfolge. Das Versionsfeld muss auf Null festgelegt sein. Das Flags-Feld kann auf die folgenden Werte festgelegt werden:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
Das MAPI_ONE_OFF_NO_RICH_INFO wird festgelegt, wenn ein Empfänger keine Nachrichteninhalte im Transport Neutral Encapsulation Format (TNEF) empfangen soll. Dieses Flag wird festgelegt, wenn MAPI_SEND_NO_RICH_INFO an [die IAddrBook::CreateOneOff-Methode übergeben](iaddrbook-createoneoff.md) wird. 
  
Das MAPI_ONE_OFF_UNICODE wird festgelegt, wenn der Anzeigename und die E-Mail-Adresse Unicode-Zeichenfolgen sind. Dieses Flag wird festgelegt, wenn MAPI_UNICODE an **IAddrBook::CreateOneOff übergeben wird.** Wenn das MAPI_UNICODE nicht an **CreateOneOff** übergeben wird, geht MAPI davon aus, dass sich der Anzeigename und die E-Mail-Adresszeichenfolgen im aktuellen ANSI-Zeichensatz der Arbeitsstation befinden. ANSI-Zeichenfolgen funktionieren in der Regel nicht gut in Nachrichten, die zwischen Plattformen mit unterschiedlichen Zeichensätzen gesendet werden, da die Codeseite nicht in der Eintrags-ID codiert ist. Um diese potenzielle Inkompatibilität zu schützen, sind viele Adresstypen auf die Zeichen beschränkt, die für mehrere Zeichensätze gemeinsam sind. Um jedoch die Zeichensatz- und Plattformkompatibilität sicherzustellen, sollten Clients Unicode für die Zeichenzeichenfolgen in ihren Nachrichten verwenden.
  
Der Anzeigename ist eine Zeichenfolge mit Nullen, die der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Empfängers und dem  _lpszName-Parameter_ entspricht, der an **IAddrBook::CreateOneOff** übergeben wird. Der Zeichensatz ist Unicode, wenn das MAPI_ONE_OFF_UNICODE festgelegt ist, und ANSI, wenn es klar ist. 
  
Bei dem Adresstyp handelt es sich um eine Zeichenfolge **mit Nullen,** die der PR_ADDRTYPE ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft des Empfängers und dem  _lpszAdrType-Parameter_ entspricht, der an **IAddrBook::CreateOneOff** übergeben wird. 
  
Die E-Mail-Adresse ist eine Zeichenfolge mit Nullen, die der **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))-Eigenschaft des Empfängers und dem  _lpszAddress-Parameter_ entspricht, der an **IAddrBook::CreateOneOff** übergeben wird. 
  
> [!NOTE]
> Es gibt keinen Abstand in einer einmal verwendeten Eintragsbezeichnerstruktur. Die Bytes werden genau wie oben angegeben verpackt, und die Länge der Eintrags-ID sollte keine Bytes enthalten, die über das endende Nullzeichen der E-Mail-Adresse hinausgehen. 
  
Clients und Adressbuchanbieter, die eindeutige Eintragsbezeichner manuell erstellen, müssen möglicherweise auch Werte für die **Eigenschaften PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) generieren. Der Datensatzschlüssel ist identisch mit dem Eintragsbezeichner. Der Suchschlüssel sollte durch Verkettung der folgenden Felder in der folgenden Reihenfolge gebildet werden:
  
1. Der Adresstyp, der in Großbuchstaben konvertiert wird.
    
2. Ein Doppelpunkt (:).
    
3. Die in Großbuchstaben konvertierte E-Mail-Adresse.
    
4. Ein endendes Nullzeichen.
    
Beim Generieren des Suchschlüssels muss keine Zeichensatzkonvertierung durchgeführt werden.
  

