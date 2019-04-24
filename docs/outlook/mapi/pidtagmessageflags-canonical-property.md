---
title: Kanonische PidTagMessageFlags-Eigenschaft
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325742"
---
# <a name="pidtagmessageflags-canonical-property"></a>Kanonische PidTagMessageFlags-Eigenschaft

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske von Flags, die den Ursprung und den aktuellen Status einer Nachricht angeben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Kennung:  <br/> |0x0E07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine Nachrichtenübermittlung  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine nontransmitable-Nachrichteneigenschaft, die sowohl an den sendenden als auch an den Empfänger Enden einer Übertragung mit unterschiedlichen Werten abhängig von der jeweiligen Clientanwendung oder dem betreffenden Speicheranbieter verfügbar gemacht wird. Diese Eigenschaft wird vom Client-oder Nachrichtenspeicher Anbieter initialisiert, wenn eine Nachricht erstellt und zum ersten Mal gespeichert und dann regelmäßig vom Nachrichtenspeicher Anbieter, einem Transportanbieter und dem MAPI-Spooler aktualisiert wird, während die Nachricht verarbeitet wird, und ihren Status Änderungen. 
  
Diese Eigenschaft ist für eine Nachricht sowohl vor als auch nach der Übermittlung und für alle Kopien der empfangenen Nachricht vorhanden. Obwohl es sich nicht um eine Empfänger Eigenschaft handelt, wird es für jeden Empfänger unterschiedlich angezeigt, je nachdem, ob es von diesem Empfänger gelesen oder geändert wurde. 
  
Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden:
  
MSGFLAG_ASSOCIATED 
  
> Die Nachricht ist eine zugeordnete Nachricht eines Ordners. Der Client oder Anbieter verfügt über Lesezugriff auf dieses Flag. Das MSGFLAG_READ-flag wird für zugeordnete Nachrichten ignoriert, die den Status "lesen/ungelesen" nicht erhalten. 
    
MSGFLAG_FROMME 
  
> Der Messagingbenutzer, der die Nachricht gesendet hat, war der Messagingbenutzer. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Aufruf und danach schreibgeschützt ist. Dieses Flag soll vom Transportanbieter festgelegt werden. 
    
MSGFLAG_HASATTACH 
  
> Die Nachricht verfügt über mindestens eine Anlage. Dieses Flag entspricht der **PR_HASATTACH** ([pidtaghasattachments (](pidtaghasattachments-canonical-property.md))-Eigenschaft der Nachricht. Der Client verfügt über Lesezugriff auf dieses Flag. 
    
MSGFLAG_NRN_PENDING 
  
> Ein ungelesener Bericht muss für die Nachricht gesendet werden. Der Client oder Anbieter verfügt über Lesezugriff auf dieses Flag. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Die eingehende Nachricht kam über das Internet. Sie stammt entweder außerhalb der Organisation oder aus einer Quelle, die das Gateway als vertrauenswürdig einstuft. Der Client sollte dem Benutzer eine entsprechende Meldung anzeigen. Transport Anbieter legen dieses Flag fest; der Client verfügt über schreibgeschützten Zugriff. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Die eingehende Nachricht kam über einen externen Link außer X. 400 oder das Internet. Sie stammt entweder außerhalb der Organisation oder aus einer Quelle, die das Gateway als vertrauenswürdig einstuft. Der Client sollte dem Benutzer eine entsprechende Meldung anzeigen. Transport Anbieter legen dieses Flag fest; der Client verfügt über schreibgeschützten Zugriff. 
    
MSGFLAG_ORIGIN_X400 
  
> Die eingehende Nachricht kam über einen X. 400-Link. Sie stammt entweder außerhalb der Organisation oder aus einer Quelle, die das Gateway als vertrauenswürdig einstuft. Der Client sollte dem Benutzer eine entsprechende Meldung anzeigen. Transport Anbieter legen dieses Flag fest; der Client verfügt über schreibgeschützten Zugriff. 
    
MSGFLAG_READ 
  
> Die Nachricht wird als gelesen markiert. Dies kann als Ergebnis eines Anrufs jederzeit für [IMessage:: SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md)auftreten. Clients können dieses Flag auch festlegen, indem Sie die **IMAPIProp::** SetProps-Methode einer Nachricht aufrufen, bevor die Nachricht zum ersten Mal gespeichert wird. Dieses Flag wird ignoriert, wenn das **MSGFLAG_ASSOCIATED** -Flag festgelegt ist. 
    
MSGFLAG_RESEND 
  
> Die Nachricht enthält eine Anforderung für einen erneuten Sendevorgang mit einem Unzustellbarkeitsbericht. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Aufruf und danach schreibgeschützt ist. 
    
MSGFLAG_RN_PENDING 
  
> Ein Lesebericht muss für die Nachricht gesendet werden. Der Client oder Anbieter verfügt über Lesezugriff auf dieses Flag. 
    
MSGFLAG_SUBMIT 
  
> Die Nachricht wird als Ergebnis eines Aufrufs von [IMessage:: SubmitMessage](imessage-submitmessage.md)als senden markiert. Nachrichtenspeicher Anbieter legen dieses Flag fest; der Client verfügt über schreibgeschützten Zugriff. 
    
MSGFLAG_UNMODIFIED 
  
> Die ausgehende Nachricht wurde nicht geändert, seit Sie zum ersten Mal gespeichert wurde. die eingehende Nachricht wurde seit der Zustellung nicht geändert. 
    
MSGFLAG_UNSENT 
  
> Die Nachricht wird noch zusammengestellt. Es wird gespeichert, aber nicht gesendet. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Aufruf und danach schreibgeschützt ist. Wenn ein Client dieses Flag nicht zu dem Zeitpunkt festlegt, zu dem die Nachricht gesendet wird, wird er vom Nachrichtenspeicher Anbieter festgelegt, wenn **IMessage:: SubmitMessage** aufgerufen wird. In der Regel wird dieses Flag gelöscht, nachdem die Nachricht gesendet wurde. 
    
Ein Client-oder Nachrichtenspeicher Anbieter kann den aktuellen Status der Nachricht jederzeit überprüfen, indem die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode zum Lesen der Flagwerte aufgerufen wird. Der Client oder Anbieter kann auch die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode aufrufen, um alle Flags zu ändern, die derzeit Lese-/Schreibzugriff besitzen. 
  
Mehrere der Flags sind immer schreibgeschützt. Einige sind bis zum ersten Aufruf der [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode Lese-/Schreibzugriff und werden dann schreibgeschützt, soweit **IMAPIProp::** SetProps betroffen sind. Eine dieser MSGFLAG_READ kann später über [IMessage:: SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md)geändert werden. 
  
Die anfänglichen Werte für diese Eigenschaft sind in der Regel MSGFLAG_UNSENT und MSGFLAG_UNMODIFIED, um eine Nachricht anzugeben, die noch nicht gesendet oder geändert wurde. Wenn eine Nachricht zum zweiten Mal gespeichert wird, löscht der Nachrichtenspeicher Anbieter das MSGFLAG_UNMODIFIED-Flag. Ein weiterer Wert, den ein Nachrichtenspeicher Anbieter beim Speichern einer Nachricht festlegen kann, ist das MSGFLAG_HASATTACH-Flag, das angibt, dass die Nachricht eine oder mehrere Anlagen enthält. Die **PR_HASATTACH** -Eigenschaft wird aus dieser Einstellung berechnet. 
  
Wenn ein Client die [IMessage:: SubmitMessage](imessage-submitmessage.md) -Methode zum Senden der Nachricht aufruft, erstellt der Nachrichtenspeicher Anbieter eine Kopie für den MAPI-Spooler und aktualisiert diese Eigenschaft, indem das MSGFLAG_SUBMIT-Flag festgelegt wird. Der Nachrichtenspeicher Anbieter legt auch MSGFLAG_UNSENT fest, wenn er noch nicht festgelegt ist. MSGFLAG_SUBMIT gibt an, dass **SubmitMessage** aufgerufen wurde, den Sendeprozess begonnen hat und dass die Nachricht jetzt für den Client schreibgeschützt ist. MSGFLAG_UNSENT gibt an, dass die MAPI-Warteschlange die Nachricht verarbeitet. Wenn der Sendevorgang abgebrochen wird, setzt der Nachrichtenspeicher Anbieter dieses Flag zurück. 
  
Wenn die Nachricht an einen Transportanbieter für die Übermittlung übermittelt wird, legt der Transportanbieter das MSGFLAG_FROMME-Flag fest, wenn der Absender das gleiche Konto auf dem Messaging Server hatte, in dem die Nachricht empfangen wurde. Transport Anbieter legen MSGFLAG_FROMME für eine eingehende Nachricht fest, die vom derzeit angemeldeten Benutzer gesendet wurde. Ein Client kann diesen Wert verwenden, um zu ermitteln, ob die Empfängernamen in der Tabelle Inhalt des Ordners gesendete Elemente als Absendernamen angezeigt werden sollen. Nachrichten, die während des Kompositions Vorgangs gespeichert und noch nicht gesendet wurden, sollten auch mit Empfängernamen anstelle von Absendernamen angezeigt werden. 
  
Für eine eingehende Nachricht löscht ein Nachrichtenspeicher Anbieter das MSGFLAG_READ-flag, um den Lesestatus zurückzusetzen. Ein Client kann das MSGFLAG_READ-Flag festlegen oder löschen, wenn es erforderlich ist, den Lesestatus zu ändern und das Senden von Lese-und nonread-Berichten zu steuern, indem entweder die [IMessage:: SetReadFlag](imessage-setreadflag.md) -Methode oder der Ordner [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) -Methode. Der Hauptunterschied zwischen diesen Methoden, außer dem Objekt, das Sie implementiert, besteht darin, dass die Folder-Methode sich auf eine, mehrere oder alle Nachrichten im Ordner auswirken kann. Die Message-Methode wirkt sich auf eine einzelne Nachricht aus. 
  
Ein Client sollte auch eine eingehende Nachricht für die Flags MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET und MSGFLAG_ORIGIN_MISC_EXT testen. Diese Flags werden vom eingehenden Transportanbieter festgelegt und geben an, dass die Nachricht von einer Quelle eingetroffen ist, die das Gateway als vertrauenswürdig einstuft. Dies hat zur Folge, dass die Nachricht entweder außerhalb der Organisation oder intern, aber von einer Arbeitsstation stammt, die dem Gateway nicht bekannt ist. In jedem Fall wird die Identität des Absenders möglicherweise nicht bestätigt, und es besteht das Risiko der Einführung eines Computervirus in der Organisation. Der Client sollte dem Benutzer eine Warnmeldung anzeigen und eine Option zum Löschen der Nachricht bieten, ohne Sie zu öffnen. 
  
Nachrichtenspeicher Anbieter legen das MSGFLAG_UNMODIFIED-Flag für eingehende Nachrichten fest. MSGFLAG_UNMODIFIED gibt an, dass eine Nachricht seit der Übermittlung nicht geändert wurde. Ein Client kann diesen Wert nicht löschen, nachdem er von einem Nachrichtenspeicher Anbieter festgelegt wurde. 
  
## <a name="related-resources"></a>Zugehörige Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf zugehörige Exchange Server-Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Verarbeitet Nachrichten-und Anlagenobjekte.
    
### <a name="header-files"></a>Header Dateien

Mapidefs. h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags. h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

