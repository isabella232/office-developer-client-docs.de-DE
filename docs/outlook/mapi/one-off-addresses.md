---
title: Einmal-Adressen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9224c694-b26f-42c7-9404-ee2dd832cfbb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 598ced18d659fcbe52ded07cc3bb80dc396eddbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793314"
---
# <a name="one-off-addresses"></a>Einmal-Adressen

**Betrifft**: Outlook 
  
Einmalige-Adressen dienen zum Senden von Nachrichten an Empfänger einmaligen Empfänger, die nicht über einen entsprechenden Eintrag in einer der der Sitzung Address Book Container verfügen. Clients können einmalige-Adressen erstellen, wenn sie neue Einträge Adressbuch oder neue Empfänger an die Empfängerliste von ausgehenden Nachrichten hinzufügen. Einmalige-Adressen können Container hinzugefügt werden, die geändert werden kann.
  
Zum Erstellen einer einmaligen Adresse verwenden Clients eine spezielle Vorlage mit Bearbeitungssteuerelementen für die Eingabe alle Informationen, die eine einmal Adresse darstellt. Einmalige-Adressen, wie Adressen anderer Typen verwenden ein vordefiniertes Formats ein. Das einmaligen Adressformat wird durch MAPI wie folgt definiert:
  
`Display name[Address type:Email address]`
  
Es gibt sechs Komponenten in diesem Format und einige Regeln darüber, wie Sie Zeichen. In der folgenden Tabelle werden die Komponenten beschrieben.
  
|**Komponente**|**Verwendung**|**Beschreibung**|
|:-----|:-----|:-----|
|Anzeigename  <br/> |Optional  <br/> |Wenn nicht vorhanden ist, wird **IAddrBook::ResolveName** sichtbaren Teil der e-Mail-Adresse als Anzeigename verwendet. Kann Leerzeichen enthalten. Weitere Informationen finden Sie unter [IAddrBook::ResolveName](iaddrbook-resolvename.md).  <br/> |
|[  <br/> |Erforderlich  <br/> |Starten des Typ und die Adresse bezeichnet.  <br/> |
|]  <br/> |Erforderlich  <br/> |Bezeichnet das Ende des Typ und die Adresse an. Wenn keine Leerzeichen dieses Zeichen folgt, wird der Eintrag nicht als ein benutzerdefinierter Empfänger behandelt.  <br/> |
|Adresstyp  <br/> |Erforderlich  <br/> |Art der Adresse. wird ein bestimmtes Adressformat. Weitere Informationen finden Sie unter [MAPI-Adresstypen](mapi-address-types.md).  <br/> |
|:  <br/> |Erforderlich  <br/> |Trennt den Adresstyp aus der e-Mail-Adresse.  <br/> |
|E-Mail-Adresse  <br/> |Erforderlich  <br/> |Die Adresse des Empf�ngers. Kann Leerzeichen enthalten.  <br/> |
   
MAPI-Adressen an, wie Komma (,), Klammern ([]), von links Sonderzeichen kann verwendet werden bestimmte Gruppen von Anführungszeichen Zeichen und Doppelpunkt (:)) und einige untypeable Zeichen wie etwa die Wagenrücklauf zurück oder line Feed oder eine andere hexadezimale entsprechende. Das Angabe Zeichen ist die umgekehrten Schrägstrich (\). Aus diesem Grund, wenn Clients oder Anbieter einen umgekehrten Schrägstrich in einer Adresse einfügen müssen, müssen sie Länderkürzel es mit der Angabe Zeichen ("\\").
  
Clients und Dienstanbieter können diese Angabe Technik in die Felder nonfixed, darstellbares verwenden. Beispielsweise wird der folgende Eintrag in Bill Lee als Anzeigename, MSPEER als Adresstyp, übersetzt und \\Billll\in als die e-Mail-Adresse:
  
`Bill Lee[MSPEER:\\\\billl\in]`

Clients und -Dienstanbieter verwenden eine Angabe Zeichen, gefolgt von einem x und zwei hexadezimale Stellen, um spezielle Nontypeable Zeichen einzufügen, um die entsprechenden hexadezimalen darzustellen. Beispielsweise, wenn eine Adresse ein Nontypeable Zeichen enthält, der ein Wagenrücklauf entspricht zurückgegeben, (\0d) Hexadezimal, ein Client Geben sie als:
  
`Fax Recipient[fax:recipient\x0dbuilding\x0doffice\x0d555-1212\x0d]`

**IAddrBook::ResolveName** analysiert auch automatisch die meisten SMTP-Adressen, die Adressen mit dem folgenden Format gesucht: 
  
`XXX@YYY.ZZZ`

Zwar nicht alle möglichen RFC822-Formate behandelt werden, ist die automatische Analyse für die meisten Benutzer ausreichend. **ResolveName** enthält diese Funktionalität, damit Benutzer SMTP-Adressen direkt in eine Nachricht eingeben und die Nachricht an das Internet-Benutzer umgeleitet wird. Die XXX YYY und ZZZ Komponenten der Adresse können eine oder mehrere Zeichen lang sein. Das @-Zeichen (@) kann nicht eingeschlossen werden in XXX, YYY oder ZZZ Adresse Komponenten und die Komponente YYY auch können nicht enthalten, den Zeitraum an. Da die folgenden Zeichen Sonderzeichen im SMTP-Adressen sind, konvertiert MAPI automatisch einen Anzeigenamen ein, die diese Zeichen in einer einmaligen Adresse enthält: 
  
- \>\>
    
- @
    
- \<\>
    
- .
    
Jede einmaligen Adresse wird eine entsprechende einmaligen Eintrags-ID zugewiesen. Um diese Zuordnung zu machen, Clients **IAddrBook::CreateOneOff** aufrufen und Transportanbieter Aufrufen **IMAPISupport::CreateOneOff**. Weitere Informationen finden Sie unter [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) und [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md). Bei der Verarbeitung eingehender Nachrichten erstellen Transportanbieter einmaligen-Eintragsbezeichner für Gateway-Adressen und Adressen, die von der Transport zugeordneten adressbuchanbietern implementierte bearbeitet werden können. Transportanbieter überprüfen Sie den Typ jeder Adresse in einer Nachricht zu ermitteln, ob es von der Transport zugeordnete Adressbuch-Dienstanbieter behandelt werden kann. Ist es nicht möglich, rufen Sie Transportanbieter **IMAPISupport::CreateOneOff** , um die Adresse einer einmaligen Eintrags-ID zuzuordnen. 
  
Einmaligen-Eintragsbezeichner enthalten die folgenden Informationen in der folgenden Reihenfolge:
  
1. **MAPIUID**
    
2. Version
    
3. Flags
    
4. Anzeigename
    
5. Adresstyp
    
6. E-Mail-Adresse
    
In der Anrufe für **IAddrBook::CreateOneOff** und **IMAPISupport::CreateOneOff**können Clients und Transportanbieter ein Flag festlegen, der angibt, ob der Empfänger, dargestellt durch die einmaligen Adresse formatierten Text verarbeitet werden kann oder nicht oder eingebettete OLE Objekte. Um anzugeben, dass ein Empfänger formatierter Text und OLE-Objekte, Clients und Transport Anbieter Set das Flag MAPI_SEND_NO_RICH_INFO im Parameter _UlFlags_ verarbeitet werden kann. MAPI wird dann der einmaligen Empfänger **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))-Eigenschaft auf false festgelegt. Wenn dieses Flag nicht festgelegt ist, wird MAPI **PR_SEND_RICH_INFO** auf TRUE festgelegt, es sei denn, die als eine SMTP-Adresse die Adresse der einmalige interpretiert wird. In diesem Fall eine wird standardmäßig auf "false" **PR_SEND_RICH_INFO** . 
  
## <a name="see-also"></a>Siehe auch

- [IAddrBook::ResolveName](iaddrbook-resolvename.md)

