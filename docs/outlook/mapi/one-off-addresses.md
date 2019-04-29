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
  
Einmalige Adressen werden verwendet, um Nachrichten an einmalige Empfänger zu senden, Empfänger, die keinen entsprechenden Eintrag in einem der Adressbuchcontainer der Sitzung haben. Clients können einmalige Adressen erstellen, wenn Sie dem Adressbuch oder neuen Empfängern neue Einträge zur Empfängerliste einer ausgehenden Nachricht hinzufügen. Einmaladressen können jedem Container hinzugefügt werden, der änderbar ist.
  
Um eine einmalige Adresse zu erstellen, verwenden Clients eine spezielle Vorlage mit Bearbeitungssteuerelementen zum Eingeben aller Informationen, aus denen eine einmalige Adresse besteht. Einmalige Adressen, wie Adressen anderer Typen, verwenden ein vordefiniertes Format. Das einmalige Adressformat wird von MAPI wie folgt definiert:
  
`Display name[Address type:Email address]`
  
Es gibt sechs Komponenten in diesem Format und einige Regeln zum Zitieren von Zeichen. Die Komponenten werden in der folgenden Tabelle beschrieben.
  
|**Komponente**|**Verwendung**|**Beschreibung**|
|:-----|:-----|:-----|
|Distinguished Name (DN)  <br/> |Optional  <br/> |Wenn nicht vorhanden, verwendet **IAddrBook::** ResolveName den sichtbaren Teil der e-Mail-Adresse als Anzeigenamen. Kann Leerzeichen aufweisen. Weitere Informationen finden Sie unter [IAddrBook::](iaddrbook-resolvename.md)ResolveName.  <br/> |
|[  <br/> |Erforderlich  <br/> |Gibt den Anfang der Typen-und Adressinformationen an.  <br/> |
|]  <br/> |Erforderlich  <br/> |Gibt das Ende der Typen-und Adressinformationen an. Wenn ein anderer als Leerraum diesem Zeichen folgt, wird der Eintrag nicht als benutzerdefinierter Empfänger behandelt.  <br/> |
|Adresstyp  <br/> |Erforderlich  <br/> |Adresstyp; ordnet einem bestimmten Adressformat zu. Weitere Informationen finden Sie unter [MAPI-Adresstypen](mapi-address-types.md).  <br/> |
|:  <br/> |Erforderlich  <br/> |Trennt den Adresstyp von der e-Mail-Adresse.  <br/> |
|E-Mail-Adresse  <br/> |Erforderlich  <br/> |Die Adresse des Empf�ngers. Kann Leerzeichen aufweisen.  <br/> |
   
MAPI verwendet bestimmte Sätze von Anführungszeichen, damit Adressen Sonderzeichen wie Komma (,), linke eckige Klammer ([) und Doppelpunkt (:) und einige nicht typisierte Zeichen wie die Wagenrücklauf-oder Zeilenvorschub oder eine andere hexadezimale Entsprechung. Das Anführungszeichen ist der\)umgekehrte Schrägstrich (. Wenn also Clients oder Anbieter einen umgekehrten Schrägstrich in eine Adresse einfügen müssen, müssen Sie ihn mit dem Anführungs\\Zeichen ("") bevorstehen.
  
Clients und Dienstanbieter können diese Angebots Methode in einem der nicht fixierten Felder verwenden. Der folgende Eintrag wird beispielsweise in Bill Lee als Anzeigename, MSPEER als Adresstyp und \\billll\in als e-Mail-Adresse übersetzt:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Zum Einfügen spezieller nicht typisierter Zeichen verwenden Clients und Dienstanbieter ein Anführungszeichen, gefolgt von einem x-und zwei Hexadezimalziffern, um Ihre Hexadezimalentsprechung darzustellen. Wenn eine Adresse beispielsweise ein nicht typfähiges Zeichen hat, das einem Wagenrücklauf (\0d) in hexadezimaler Form entspricht, würde ein Client Sie wie folgt eingeben:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::** ResolveName analysiert auch automatisch die meisten SMTP-Adressen und sucht nach Adressen mit dem folgenden Format: 
  
`XXX@YYY.ZZZ`

Obwohl nicht alle möglichen RFC822-Formate behandelt werden, ist diese automatische Analyse für die meisten Benutzer ausreichend. **** ResolveName enthält diese Funktionalität, mit der Benutzer SMTP-Adressen direkt in eine Nachricht eingeben können, und die Nachricht wird an den Internet Benutzer gesendet. Die XXX-, YYY-und ZZZ-Komponenten der Adresse können ein oder mehrere Zeichen sein. Das at-Zeichen (@) kann nicht in die Adresskomponenten XXX, YYY oder ZZZ eingeschlossen werden, und die YYY-Komponente kann auch den Zeitraum nicht enthalten. Da die folgenden Zeichen Sonderzeichen in SMTP-Adressen sind, konvertiert MAPI automatisch einen Anzeigenamen, der diese Zeichen enthält, in eine einmalige Adresse: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Jeder einmaligen Adresse wird eine entsprechende einmalige Eintrags-ID zugewiesen. Um diese Zuweisung vorzunehmen, rufen die Clients **IAddrBook:: CreateOneOff** und Transportanbieter rufen **IMAPISupport:: CreateOneOff**auf. Weitere Informationen finden Sie unter [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md). Bei der Verarbeitung eingehender Nachrichten erstellen Transportanbieter einmalige Eintrags-IDs für Gateway-Adressen und für Adressen, die von den zugeordneten Adressbuch Anbietern des Transports nicht bearbeitet werden können. Transport Anbieter überprüfen den Typ jeder Adresse in einer Nachricht, um zu bestimmen, ob Sie von einem Adressbuchanbieter verarbeitet werden kann, der dem Transport zugeordnet ist. Wenn dies nicht möglich ist, rufen Transportanbieter **IMAPISupport:: CreateOneOff** auf, um die Adresse mit einem einmaligen Eintragsbezeichner zu verknüpfen. 
  
Einmalige Eintrags-IDs bieten die folgenden Informationen in der folgenden Reihenfolge:
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Distinguished Name (DN)
    
5. Adresstyp
    
6. E-Mail-Adresse
    
In den Aufrufen von **IAddrBook:: CreateOneOff** und **IMAPISupport:: CreateOneOff**können Clients und Transportanbieter ein Flag festlegen, das angibt, ob der durch die einmalige Adresse dargestellte Empfänger formatierten Text oder eingebettete OLE verarbeiten kann. Objekte. Um anzugeben, dass ein Empfänger formatierten Text und OLE-Objekte verarbeiten kann, legen Clients und Transportanbieter das MAPI_SEND_NO_RICH_INFO-Flag im _ulFlags_ -Parameter fest. Anschließend wird die **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft des einmaligen Empfängers auf false festgelegt. Wenn dieses Flag nicht festgelegt ist, legt MAPI **PR_SEND_RICH_INFO** auf true fest, es sei denn, die einmalige Adresse wird als SMTP-Adresse interpretiert. In diesem Fall ist **PR_SEND_RICH_INFO** standardmäßig auf FALSE festgelegt. 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

