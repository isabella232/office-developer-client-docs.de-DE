---
title: Einmaladressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1fccf0f3e72cb2619566e074cde3dbb52c539ef2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583981"
---
# <a name="one-off-addresses"></a>Einmaladressen

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Einmalige Adressen werden verwendet, um Nachrichten an einmalige Empfänger zu senden, Empfänger, die keinen entsprechenden Eintrag in den Adressbuchcontainern der Sitzung haben. Clients können einmalige Adressen erstellen, wenn sie neue Einträge zum Adressbuch oder neue Empfänger zur Empfängerliste einer ausgehenden Nachricht hinzufügen. Einmalige Adressen können jedem Container hinzugefügt werden, der modifizierbar ist.
  
Zum Erstellen einer einmaligen Adresse verwenden Clients eine spezielle Vorlage mit Bearbeitungssteuerelementen zum Eingeben aller Informationen, die eine einmalige Adresse bilden. Einmalige Adressen verwenden wie Adressen anderer Typen ein vordefiniertes Format. Das einmalige Adressformat wird von MAPI wie folgt definiert:
  
`Display name[Address type:Email address]`
  
Es gibt sechs Komponenten für dieses Format und einige Regeln zum Angeben von Zeichen. Die Komponenten werden in der folgenden Tabelle beschrieben.
  
|**Komponente**|**Verwendung**|**Beschreibung**|
|:-----|:-----|:-----|
|Anzeigename  <br/> |Optional  <br/> |Wenn nicht vorhanden, verwendet **IAddrBook::ResolveName** den sichtbaren Teil der E-Mail-Adresse als Anzeigenamen. Kann Leerstellen enthalten. Weitere Informationen finden Sie unter [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Erforderlich  <br/> |Gibt den Anfang der Typ- und Adressinformationen an.  <br/> |
|]  <br/> |Erforderlich  <br/> |Gibt das Ende der Typ- und Adressinformationen an. Wenn etwas anderes als Leerzeichen auf dieses Zeichen folgt, wird der Eintrag nicht als benutzerdefinierter Empfänger behandelt.  <br/> |
|Adresstyp  <br/> |Erforderlich  <br/> |Adresstyp; ist einem bestimmten Adressformat zugeordnet. Weitere Informationen finden Sie unter [MAPI-Adresstypen.](mapi-address-types.md)  <br/> |
|:  <br/> |Erforderlich  <br/> |Trennt den Adresstyp von der E-Mail-Adresse.  <br/> |
|E-Mail-Adresse  <br/> |Erforderlich  <br/> |Die Adresse des Empf�ngers. Kann Leerstellen enthalten.  <br/> |
   
MAPI verwendet bestimmte Sätze von Zitatzeichen, damit Adressen Sonderzeichen wie Komma (,), linke Klammer ([) und Doppelpunkt (:) und einige nicht typisierbare Zeichen, z. B. wagenrücklauf, Zeilenvorschub oder andere hexadezimale Entsprechungen. Das Zitatzeichen ist der umgekehrte Schrägstrich ( \) . Wenn Clients oder Anbieter daher einen umgekehrten Schrägstrich in eine Adresse einfügen müssen, müssen sie ihr das zitatende Zeichen (" ") vorangestellt haben. \\
  
Clients und Dienstanbieter können dieses Zitatverfahren in jedem der nicht fixierten, typisierten Felder verwenden. Beispielsweise wird der folgende Eintrag in Bill Lee als Anzeigenamen, MSPEER als Adresstyp und \\ billll\in als E-Mail-Adresse übersetzt:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Um sonderbare, nicht typierbare Zeichen einzufügen, verwenden Clients und Dienstanbieter ein Zitat gefolgt von einer x- und zwei Hexadezimalziffern, um deren hexadezimale Entsprechung darzustellen. Wenn eine Adresse beispielsweise ein nicht typierbares Zeichen aufweist, das einem Wagenrücklauf (\0d) im Hexadezimalwert entspricht, würde ein Client sie wie folgt eingeben:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analysiert auch automatisch die meisten SMTP-Adressen und sucht nach Adressen im folgenden Format: 
  
`XXX@YYY.ZZZ`

Obwohl nicht alle möglichen RFC822-Formate verarbeitet werden, ist diese automatische Analyse für die meisten Benutzer ausreichend. **ResolveName** enthält diese Funktion, damit Benutzer SMTP-Adressen direkt in eine Nachricht eingeben und diese Nachricht an den Internetbenutzer senden können. Die XXX-, YYY- und ZZZ-Komponenten der Adresse können ein oder mehrere Zeichen sein. Das At-Zeichen (@) kann nicht in den XXX-, YYY- oder ZZZ-Adresskomponenten enthalten sein, und die YYY-Komponente kann auch den Punkt nicht enthalten. Da die folgenden Zeichen Sonderzeichen in SMTP-Adressen sind, konvertiert MAPI automatisch einen Anzeigenamen, der diese Zeichen enthält, in eine einmalige Adresse: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Jeder einmaligen Adresse wird ein entsprechender einmaliger Eintragsbezeichner zugewiesen. Um diese Zuweisung vorzunehmen, rufen Clients **IAddrBook::CreateOneOff auf,** und Transportanbieter rufen **IMAPISupport::CreateOneOff** auf. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Bei der Verarbeitung eingehender Nachrichten erstellen Transportanbieter einmalige Eintragsbezeichner für Gatewayadressen und für Adressen, die nicht von den zugeordneten Adressbuchanbietern des Transports verarbeitet werden können. Transportanbieter überprüfen den Typ jeder Adresse in einer Nachricht, um festzustellen, ob sie von einem Adressbuchanbieter verarbeitet werden kann, der dem Transport zugeordnet ist. Ist dies nicht der Fall, rufen Transportanbieter **IMAPISupport::CreateOneOff** auf, um die Adresse einem einmaligen Eintragsbezeichner zuzuordnen. 
  
One-off entry identifiers include the following information in the following order:
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Anzeigename
    
5. Adresstyp
    
6. E-Mail-Adresse
    
In den Aufrufen von **IAddrBook::CreateOneOff** und **IMAPISupport::CreateOneOff** können Clients und Transportanbieter ein Flag festlegen, das angibt, ob der durch die einmalige Adresse dargestellte Empfänger formatierten Text oder eingebettete OLE-Objekte verarbeiten kann. Um anzugeben, dass ein Empfänger formatierten Text und OLE-Objekte verarbeiten kann, legen Clients und Transportanbieter das flag MAPI_SEND_NO_RICH_INFO im  _ulFlags-Parameter_ fest. MAPI legt dann die **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) -Eigenschaft des einmaligen Empfängers auf FALSE fest. Wenn dieses Kennzeichen nicht festgelegt ist, legt MAPI **PR_SEND_RICH_INFO** auf TRUE fest, es sei denn, die einmalige Adresse wird als SMTP-Adresse interpretiert. In diesem einen Fall wird **PR_SEND_RICH_INFO** standardmäßig auf FALSE festgelegt. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

