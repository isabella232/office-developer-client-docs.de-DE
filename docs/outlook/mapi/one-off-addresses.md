---
title: Einmaladressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e6bda55951d8df5c5da272750c631ec105b2ccf2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409111"
---
# <a name="one-off-addresses"></a>Einmaladressen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einmaladressen werden zum Senden von Nachrichten an einmal verwendete Empfänger verwendet, empfänger, die keinen entsprechenden Eintrag in den Adressbuchcontainern der Sitzung haben. Clients können Einmaladressen erstellen, wenn sie dem Adressbuch neue Einträge oder neue Empfänger zur Empfängerliste einer ausgehenden Nachricht hinzufügen. One-off-Adressen können zu jedem Container hinzugefügt werden, der änderbar ist.
  
Zum Erstellen einer einmal verwendeten Adresse verwenden Clients eine spezielle Vorlage, die Bearbeitungssteuerelemente enthält, um alle Informationen ein eingeben zu können, aus denen eine einmal enthaltende Adresse ist. Einmaladressen wie Adressen anderer Typen verwenden ein vordefiniertes Format. Das einmal festgelegte Adressformat wird von MAPI wie folgt definiert:
  
`Display name[Address type:Email address]`
  
Dieses Format enthält sechs Komponenten und einige Regeln zum Quotieren von Zeichen. Die Komponenten werden in der folgenden Tabelle beschrieben.
  
|**Komponente**|**Verwendung**|**Beschreibung**|
|:-----|:-----|:-----|
|Anzeigename  <br/> |Optional.  <br/> |Falls nicht vorhanden, **verwendet IAddrBook::ResolveName** den sichtbaren Teil der E-Mail-Adresse als Anzeigename. Kann Leerzeichen enthalten. Weitere Informationen finden Sie unter [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Erforderlich  <br/> |Gibt den Anfang des Typs und der Adressinformationen an.  <br/> |
|]  <br/> |Erforderlich  <br/> |Delineiert das Ende der Typ- und Adressinformationen. Wenn etwas anderes als Leerzeichen diesem Zeichen folgt, wird der Eintrag nicht als benutzerdefinierter Empfänger behandelt.  <br/> |
|Adresstyp  <br/> |Erforderlich  <br/> |Adresstyp; einem bestimmten Adressformat. Weitere Informationen finden Sie unter [MAPI-Adresstypen](mapi-address-types.md).  <br/> |
|:  <br/> |Erforderlich  <br/> |Trennt den Adresstyp von der E-Mail-Adresse.  <br/> |
|E-Mail-Adresse  <br/> |Erforderlich  <br/> |Die Adresse des Empf�ngers. Kann Leerzeichen enthalten.  <br/> |
   
MAPI verwendet bestimmte Sätze von Quotierungszeichen, um Adressen Sonderzeichen wie Komma (,), linke Klammer ([) und Doppelpunkt (:) und einige nicht typierbare Zeichen, z. B. wagenrücklauf oder Zeilenvorschub oder eine andere hexadezimale Entsprechung. Das Quotierungszeichen ist der umgekehrte Schrägstrich ( \) . Wenn Clients oder Anbieter daher einen umgekehrten Schrägstrich in eine Adresse einfügen müssen, müssen sie diesen mit dem Quotierungszeichen (" \\ ") vorverlegen.
  
Clients und Dienstanbieter können dieses Zitatverfahren in einem der nicht fixierten, typierbaren Felder verwenden. Der folgende Eintrag übersetzt beispielsweise Bill Lee als Anzeigenamen, MSPEER als Adresstyp und \\ billll\in als E-Mail-Adresse:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Zum Einfügen spezieller nicht typierbarer Zeichen verwenden Clients und Dienstanbieter ein Quotierungszeichen gefolgt von einer x- und zwei hexadezimalen Ziffer, um deren hexadezimale Entsprechung zu repräsentieren. Wenn eine Adresse z. B. ein nicht typierbares Zeichen hat, das einem Wagenrücklauf entspricht, (\0d) im Hexadezimal, gibt ein Client sie wie folgt ein:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analysiert auch automatisch die meisten SMTP-Adressen und sucht nach Adressen im folgenden Format: 
  
`XXX@YYY.ZZZ`

Obwohl nicht alle möglichen RFC822-Formate behandelt werden, ist diese automatische Analyse für die meisten Benutzer geeignet. **ResolveName** umfasst diese Funktion, um Benutzern die direkte Eingabe von SMTP-Adressen in eine Nachricht zu ermöglichen und die Nachricht an den Internetbenutzer zu senden. Die XXX-, YYY- und ZZZ-Komponenten der Adresse können ein oder mehrere Zeichen sein. Das At-Zeichen (@) kann nicht in die Xxx-, YYY- oder ZZZ-Adresskomponenten einbezogen werden, und die YYY-Komponente kann auch den Zeitraum nicht enthalten. Da es sich bei den folgenden Zeichen um Sonderzeichen in SMTP-Adressen handelt, konvertiert MAPI automatisch einen Anzeigenamen, der diese Zeichen enthält, in eine Einmaladresse: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Jeder einzelnen Adresse wird ein entsprechender einmaler Eintragsbezeichner zugewiesen. Um diese Zuweisung zu erstellen, rufen Clients **IAddrBook::CreateOneOff** auf, und Transportanbieter rufen **IMAPISupport::CreateOneOff auf.** Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Bei der Verarbeitung eingehender Nachrichten erstellen Transportanbieter einmal eintragsbezeichner für Gatewayadressen und für Adressen, die nicht von den zugeordneten Adressbuchanbietern des Transports verarbeitet werden können. Transportanbieter überprüfen den Typ der einzelnen Adressen in einer Nachricht, um festzustellen, ob sie von einem Adressbuchanbieter verarbeitet werden kann, der dem Transport zugeordnet ist. Wenn dies nicht möglich ist, rufen Transportanbieter **IMAPISupport::CreateOneOff auf,** um die Adresse einem einmal verwendeten Eintragsbezeichner zuzuordnen. 
  
One-off-Eintragsbezeichner enthalten die folgenden Informationen in der folgenden Reihenfolge:
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Anzeigename
    
5. Adresstyp
    
6. E-Mail-Adresse
    
In den Aufrufen von **IAddrBook::CreateOneOff** und **IMAPISupport::CreateOneOff** können Clients und Transportanbieter ein Flag festlegen, das angibt, ob der von der einmalen Adresse dargestellte Empfänger formatierten Text oder eingebettete OLE-Objekte verarbeiten kann. Um anzugeben, dass ein Empfänger formatierten Text verarbeiten kann, legen Clients und Transportanbieter das MAPI_SEND_NO_RICH_INFO im  _ulFlags-Parameter_ fest. MAPI legt dann die #A0 **des PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) auf FALSE fest. Wenn dieses Flag nicht festgelegt ist, legt MAPI **PR_SEND_RICH_INFO** TRUE fest, es sei denn, die einmaladresse wird als SMTP-Adresse interpretiert. In diesem fall **ist PR_SEND_RICH_INFO** false. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

