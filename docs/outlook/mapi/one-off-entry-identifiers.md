---
title: Bezeichner für Einmal-Einträge
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 741d21ae-f14a-4b7f-80aa-91d0f0ff3f34
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: befb72506ee8b31628b10567996a92db6de3f89b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584003"
---
# <a name="one-off-entry-identifiers"></a>Bezeichner für Einmal-Einträge
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
One-off entry identifiers are created by MAPI in the **IAddrBook::CreateOneOff** method and by components that do not have access to the MAPI subsystem, such as gateway components. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). Die folgende Abbildung zeigt das Format eines einmaligen Eintragsbezeichners.
  
**Format von Eintragsbezeichner mit einmaliger Eingabe**
  
![Format von Eintragsbezeichner mit einmaliger Eingabe](media/amapi_69.gif "Format von Eintragsbezeichner mit einmaliger Eingabe")
  
Das erste Feld ist eine spezielle [MAPIUID-Struktur,](mapiuid.md) die den Eintragsbezeichner so identifiziert, dass er einen benutzerdefinierten Empfänger darstellt. Diese **MAPIUID-Struktur** muss auf die Konstante MAPI_ONE_OFF_UID festgelegt werden. MAPI_ONE_OFF_UID ist in der Headerdatei MAPIDEFS.H definiert. 
  
Die Felder "Version" und "Flags" sind 16-Bit-Wörter in Intel-Bytereihenfolge. Das Versionsfeld muss auf Null festgelegt sein. Das Flags-Feld kann auf die folgenden Werte festgelegt werden:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
Die MAPI_ONE_OFF_NO_RICH_INFO-Kennzeichnung wird festgelegt, wenn ein Empfänger keine Nachrichteninhalte im transportneutralen Kapselungsformat (Transport Neutral Encapsulation Format, TNEF) empfangen soll. Dieses Flag wird festgelegt, wenn MAPI_SEND_NO_RICH_INFO an die [IAddrBook::CreateOneOff-Methode](iaddrbook-createoneoff.md) übergeben wird. 
  
Das flag MAPI_ONE_OFF_UNICODE wird festgelegt, wenn der Anzeigename und die E-Mail-Adresse Unicode-Zeichenfolgen sind. Dieses Flag wird festgelegt, wenn die MAPI_UNICODE an **IAddrBook::CreateOneOff** übergeben wird. Wenn das MAPI_UNICODE-Flag nicht an **CreateOneOff** übergeben wird, geht MAPI davon aus, dass sich der Anzeigename und die E-Mail-Adresszeichenfolgen im aktuellen ANSI-Zeichensatz der Arbeitsstation befinden. ANSI-Zeichenfolgen funktionieren in Nachrichten, die zwischen Plattformen mit unterschiedlichen Zeichensätzen gesendet werden, in der Regel nicht gut, da die Codeseite nicht im Eintragsbezeichner codiert ist. Zum Schutz vor dieser potenziellen Inkompatibilität sind viele Adresstypen auf die Zeichen beschränkt, die in mehreren Zeichensätzen verwendet werden. Um jedoch die Zeichensatz- und Plattformkompatibilität sicherzustellen, sollten Clients Unicode für die Zeichenzeichenfolgen in ihren Nachrichten verwenden.
  
Der Anzeigename ist eine Zeichenfolge, die mit NULL beendet wird und der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) -Eigenschaft des Empfängers und dem  _lpszName_ -Parameter entspricht, der an **IAddrBook::CreateOneOff** übergeben wird. Der Zeichensatz ist Unicode, wenn das MAPI_ONE_OFF_UNICODE-Kennzeichen festgelegt ist, und ANSI, wenn es eindeutig ist. 
  
Der Adresstyp ist eine Zeichenfolge, die mit Null beendet wird und der **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) -Eigenschaft des Empfängers und dem  _lpszAdrType_ -Parameter entspricht, der an **IAddrBook::CreateOneOff** übergeben wird. 
  
Die E-Mail-Adresse ist eine Zeichenfolge, die mit Null beendet wird und der **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) -Eigenschaft des Empfängers und dem  _lpszAddress_ -Parameter entspricht, der an **IAddrBook::CreateOneOff** übergeben wird. 
  
> [!NOTE]
> Es gibt keinen Abstand in einmaligen Eintragsbezeichnerstrukturen; Die Bytes werden genau wie oben angegeben verpackt, und die Länge des Eintragsbezeichners sollte keine Bytes enthalten, die über das endende NULL-Zeichen der E-Mail-Adresse hinausgehen. 
  
Clients und Adressbuchanbieter, die manuell einmalige Eintragsbezeichner erstellen, müssen möglicherweise auch Werte für die Eigenschaften **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) generieren. Der Datensatzschlüssel ist identisch mit dem Eintragsbezeichner. Der Suchschlüssel sollte durch Verketten der folgenden Felder in der folgenden Reihenfolge gebildet werden:
  
1. Der Adresstyp, der in Großbuchstaben konvertiert wird.
    
2. Doppelpunkt (:).
    
3. Die in Großbuchstaben konvertierte E-Mail-Adresse.
    
4. Ein endendes NULL-Zeichen.
    
Beim Generieren des Suchschlüssels muss keine Konvertierung des Zeichensatzes erfolgen.
  

