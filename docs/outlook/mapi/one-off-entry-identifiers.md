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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279692"
---
# <a name="one-off-entry-identifiers"></a>Bezeichner für Einmal-Einträge
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einmalige Eintrags-IDs werden von MAPI in der **IAddrBook:: CreateOneOff** -Methode und von Komponenten erstellt, die keinen Zugriff auf das MAPI-Subsystem haben, wie beispielsweise Gateway-Komponenten. For more information, see [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md). Die folgende Abbildung zeigt das Format einer einmaligen Eintrags-ID.
  
**Format von Eintragsbezeichner mit einmaliger Eingabe**
  
![Einmaliges Eintrags-ID-Format] (media/amapi_69.gif "Einmaliges Eintrags-ID-Format")
  
Das erste Feld ist eine spezielle [MAPIUID](mapiuid.md) -Struktur, die die Eintrags-ID als Darstellung eines benutzerdefinierten Empfängers identifiziert. Diese **MAPIUID** -Struktur muss auf die Konstante MAPI_ONE_OFF_UID festgelegt werden. MAPI_ONE_OFF_UID ist in der Headerdatei MAPIDEFS definiert. H. 
  
Die Felder Version und Flags sind 16-Bit-Wörter in der Intel-Bytereihenfolge. Das Feld Version muss auf NULL festgelegt sein. Das Flags-Feld kann auf die folgenden Werte festgelegt werden:
  
MAPI_ONE_OFF_NO_RICH_INFO
  
MAPI_ONE_OFF_UNICODE
  
Das MAPI_ONE_OFF_NO_RICH_INFO-Flag wird festgelegt, wenn ein Empfänger keinen Nachrichteninhalt im Transport Neutral Encapsulation Format (TNEF) empfangen soll. Dieses Flag wird festgelegt, wenn MAPI_SEND_NO_RICH_INFO an [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) -Methode übergeben wird. 
  
Das MAPI_ONE_OFF_UNICODE-Flag wird festgelegt, wenn der Anzeigename und die e-Mail-Adresse Unicode-Zeichenfolgen sind. Dieses Flag wird festgelegt, wenn die MAPI_UNICODE an **IAddrBook:: CreateOneOff**übergeben wird. Wenn das MAPI_UNICODE-Flag nicht an **CreateOneOff**übergeben wird, wird davon ausgegangen, dass die Zeichenfolgen für den Anzeigenamen und die e-Mail-Adresse im aktuellen ANSI-Zeichensatz der Arbeitsstation liegen. ANSI-Zeichenfolgen funktionieren im Allgemeinen nicht gut in Nachrichten, die zwischen Plattformen mit unterschiedlichen Zeichensätzen gesendet werden, da die Codepage nicht in der Eintrags-ID codiert ist. Um diese potenzielle Inkompatibilität zu vermeiden, sind viele Adresstypen auf die Zeichen beschränkt, die für mehrere Zeichensätze häufig gelten. Zur Sicherstellung der Zeichensatz-und Plattformkompatibilität sollten Clients Unicode für die Zeichenfolgen in ihren Nachrichten verwenden.
  
Der Anzeigename ist eine mit NULL endende Zeichenfolge, die der **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft des Empfängers und dem _lpszName_ -Parameter entspricht, der an **IAddrBook:: CreateOneOff**übergeben wird. Der Zeichensatz ist Unicode, wenn das MAPI_ONE_OFF_UNICODE-Flag festgelegt ist, und ANSI, wenn es klar ist. 
  
Der Adresstyp ist eine mit NULL endende Zeichenfolge, die der **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft des Empfängers und dem _lpszAdrType_ -Parameter entspricht, der an **IAddrBook:: CreateOneOff**übergeben wird. 
  
Die e-Mail-Adresse ist eine NULL-terminierte Zeichenfolge, die der **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))-Eigenschaft des Empfängers und dem _lpszAddress_ -Parameter entspricht, der an **IAddrBook:: CreateOneOff**übergeben wird. 
  
> [!NOTE]
> Es gibt keinen Abstand in einmaligen Eintrags-ID-Strukturen; die Bytes werden genau wie oben angegeben verpackt, und die Länge des Eintrags-Bezeichners sollte keine Bytes über das abschließende Null-Zeichen der e-Mail-Adresse hinaus umfassen. 
  
Clients und Adressbuchanbieter, die einmalige Eintrags-IDs manuell erstellen, müssen möglicherweise auch Werte für die Eigenschaften **PR_RECORD_KEY** ([Pidtagrecordkey (](pidtagrecordkey-canonical-property.md)) und **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md)) generieren. Der Record-Schlüssel ist identisch mit der Eintrags-ID. Der Suchschlüssel sollte durch Verketten der folgenden Felder in der folgenden Reihenfolge gebildet werden:
  
1. Der Adresstyp, konvertiert in Großbuchstaben.
    
2. Ein Doppelpunkt (:).
    
3. Die e-Mail-Adresse, konvertiert in Großbuchstaben.
    
4. Ein abschließendes NULL-Zeichen.
    
Beim Generieren des Suchschlüssels muss keine Zeichensatzkonvertierung ausgeführt werden.
  

