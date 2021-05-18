---
title: PidTagMessageFlags (kanonische Eigenschaft)
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5b660b592e77279a4d60f3a036724341352c9b6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325742"
---
# <a name="pidtagmessageflags-canonical-property"></a>PidTagMessageFlags (kanonische Eigenschaft)

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält eine Bitmaske mit Flags, die den Ursprung und den aktuellen Status einer Nachricht angeben. 
  
|||
|:-----|:-----|
|Zugeordnete Eigenschaften:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Kennung:  <br/> |0x0E07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeines Messaging  <br/> |
   
## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist eine nichttransmittable Nachrichteneigenschaft, die sowohl am Sende- als auch am Empfangsende einer Übertragung mit unterschiedlichen Werten abhängig von der clientanwendung oder dem jeweiligen Speicheranbieter verfügbar gemacht wird. Diese Eigenschaft wird vom Client- oder Nachrichtenspeicheranbieter initialisiert, wenn eine Nachricht zum ersten Mal erstellt und gespeichert wird und dann regelmäßig vom Nachrichtenspeicheranbieter, einem Transportanbieter und dem MAPI-Spooler aktualisiert wird, wenn die Nachricht verarbeitet wird und sich ihr Status ändert. 
  
Diese Eigenschaft ist für eine Nachricht vor und nach der Übermittlung sowie für alle Kopien der empfangenen Nachricht vorhanden. Obwohl es sich nicht um eine Empfängereigenschaft handelt, wird sie für jeden Empfänger unterschiedlich verfügbar gemacht, je nachdem, ob sie von diesem Empfänger gelesen oder geändert wurde. 
  
Mindestens eines der folgenden Kennzeichen kann für diese Eigenschaft festgelegt werden:
  
MSGFLAG_ASSOCIATED 
  
> Die Nachricht ist eine zugeordnete Nachricht eines Ordners. Der Client oder Anbieter hat schreibgeschützten Zugriff auf dieses Flag. Das MSGFLAG_READ wird für zugeordnete Nachrichten ignoriert, die keinen Lese-/Ungelesenstatus beibehalten. 
    
MSGFLAG_FROMME 
  
> Der Messagingbenutzer, der die Nachricht sendet, war der Messagingbenutzer, der die Nachricht empfängt. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) und danach schreibgeschützt ist. Dieses Flag soll vom Transportanbieter festgelegt werden. 
    
MSGFLAG_HASATTACH 
  
> Die Nachricht verfügt über mindestens eine Anlage. Dieses Flag entspricht der eigenschaft **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)). Der Client hat schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_NRN_PENDING 
  
> Für die Nachricht muss ein nicht gelesener Bericht gesendet werden. Der Client oder Anbieter hat schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Die eingehende Nachricht wurde über das Internet empfangen. Er stammt entweder außerhalb der Organisation oder aus einer Quelle, die vom Gateway nicht als vertrauenswürdig eingestuft werden kann. Der Client sollte dem Benutzer eine entsprechende Nachricht anzeigen. Dieses Kennzeichen wird von Transportanbietern festgelegt. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Die eingehende Nachricht wurde über einen anderen externen Link als X.400 oder das Internet empfangen. Er stammt entweder außerhalb der Organisation oder aus einer Quelle, die vom Gateway nicht als vertrauenswürdig eingestuft werden kann. Der Client sollte dem Benutzer eine entsprechende Nachricht anzeigen. Dieses Kennzeichen wird von Transportanbietern festgelegt. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_ORIGIN_X400 
  
> Die eingehende Nachricht wurde über einen X.400-Link empfangen. Er stammt entweder außerhalb der Organisation oder aus einer Quelle, die vom Gateway nicht als vertrauenswürdig eingestuft werden kann. Der Client sollte dem Benutzer eine entsprechende Nachricht anzeigen. Dieses Kennzeichen wird von Transportanbietern festgelegt. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_READ 
  
> Die Nachricht ist als gelesen gekennzeichnet. Dies kann jederzeit als Ergebnis eines [Aufrufs von IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags auftreten.](imapifolder-setreadflags.md) Clients können dieses Kennzeichen auch festlegen, indem sie die **IMAPIProp::SetProps-Methode** einer Nachricht aufrufen, bevor die Nachricht zum ersten Mal gespeichert wurde. Dieses Flag wird ignoriert, wenn **MSGFLAG_ASSOCIATED** festgelegt ist. 
    
MSGFLAG_RESEND 
  
> Die Nachricht enthält eine Anforderung für einen erneuten Senden-Vorgang mit einem Nicht-Löschbericht. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) und danach schreibgeschützt ist. 
    
MSGFLAG_RN_PENDING 
  
> Für die Nachricht muss ein Lesebericht gesendet werden. Der Client oder Anbieter hat schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_SUBMIT 
  
> Die Nachricht wird als Ergebnis eines Aufrufs von [IMessage::SubmitMessage](imessage-submitmessage.md)für das Senden markiert. Nachrichtenspeicheranbieter legen dieses Flag festgelegt. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_UNMODIFIED 
  
> Die ausgehende Nachricht wurde seit dem ersten Speichern nicht geändert. Die eingehende Nachricht wurde seit der Zugestellten nicht geändert. 
    
MSGFLAG_UNSENT 
  
> Die Nachricht wird noch verfasst. Es wird gespeichert, aber nicht gesendet. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) und danach schreibgeschützt ist. Wenn ein Client dieses Flag nicht zum Zeitpunkt des Sendens der Nachricht festgelegt hat, legt der Nachrichtenspeicheranbieter es fest, wenn **IMessage::SubmitMessage** aufgerufen wird. In der Regel wird dieses Flag nach dem Senden der Nachricht geräumt. 
    
Ein Client- oder Nachrichtenspeicheranbieter kann den aktuellen Status der Nachricht jederzeit überprüfen, indem die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) zum Lesen der Kennzeichenwerte aufruft. Der Client oder Anbieter kann auch die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) aufrufen, um alle Flags zu ändern, die derzeit über Lese-/Schreibzugriff verfügen. 
  
Mehrere Kennzeichen sind immer schreibgeschützt. Einige sind lese-/schreibzugriff, bis der erste Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) durchgeführt wird und anschließend schreibgeschützt wird, was **IMAPIProp::SetProps** betrifft. Eine dieser MSGFLAG_READ kann später über [IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags geändert werden.](imapifolder-setreadflags.md) 
  
Die anfänglichen Werte für diese Eigenschaft werden MSGFLAG_UNSENT und MSGFLAG_UNMODIFIED, um eine Nachricht anzugeben, die noch nicht gesendet oder geändert wurde. Wenn eine Nachricht zum zweiten Mal gespeichert wird, wird das Flag vom Nachrichtenspeicheranbieter MSGFLAG_UNMODIFIED. Ein weiterer Wert, den ein Nachrichtenspeicheranbieter festlegen kann, wenn eine Nachricht gespeichert wird, ist das MSGFLAG_HASATTACH-Flag, das angibt, dass die Nachricht über eine oder mehrere Anlagen verfügt. Die **PR_HASATTACH-Eigenschaft** wird aus dieser Einstellung berechnet. 
  
Wenn ein Client die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufruft, um die Nachricht zu senden, macht der Nachrichtenspeicheranbieter eine Kopie davon für den MAPI-Spooler und aktualisiert diese Eigenschaft, indem er das MSGFLAG_SUBMIT legt. Der Nachrichtenspeicheranbieter legt auch MSGFLAG_UNSENT fest, wenn er noch nicht festgelegt ist. MSGFLAG_SUBMIT an, dass **SubmitMessage** aufgerufen wurde und den Sendevorgang beginnt und die Nachricht nun schreibgeschützt für den Client ist. MSGFLAG_UNSENT gibt an, dass der MAPI-Spooler die Nachricht verwendet. Wenn der Sendevorgang abgebrochen wird, setzt der Nachrichtenspeicheranbieter dieses Kennzeichen zurück. 
  
Wenn die Nachricht an einen Transportanbieter zur Zustellung gesendet wird, legt der Transportanbieter das MSGFLAG_FROMME-Flag fest, wenn der Absender das gleiche Konto auf dem Messagingserver hatte, auf dem die Nachricht empfangen wurde. Transportanbieter legen MSGFLAG_FROMME für eine eingehende Nachricht fest, die vom aktuell angemeldeten Benutzer gesendet wurde. Ein Client kann diesen Wert verwenden, um festzustellen, dass es besser ist, Empfängernamen im Inhaltsverzeichnis des Ordners "Gesendete Elemente" anzuzeigen als Absendernamen. Nachrichten, die während des Kompositionsprozesses gespeichert und noch nicht gesendet wurden, sollten auch mit Empfängernamen und nicht mit Absendernamen angezeigt werden. 
  
Bei einer eingehenden Nachricht wird von einem Nachrichtenspeicheranbieter das MSGFLAG_READ, um den Lesestatus zurückzusetzen. Ein Client kann das MSGFLAG_READ-Flag festlegen oder löschen, wenn es erforderlich ist, den Lesestatus zu ändern und das Senden von Lese- und Nichtleseberichten zu steuern, indem entweder die [IMessage::SetReadFlag-Methode](imessage-setreadflag.md) der Nachricht oder die [IMAPIFolder::SetReadFlags-Methode](imapifolder-setreadflags.md) der Nachricht aufruft. Der Hauptunterschied zwischen diesen Methoden ist, dass die Ordnermethode sich auf eine, mehrere oder alle Nachrichten im Ordner auswirken kann, mit anderen als dem Objekt, das sie implementieren. Die Message-Methode wirkt sich auf eine einzelne Nachricht aus. 
  
Ein Client sollte auch eine eingehende Nachricht für die MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET und MSGFLAG_ORIGIN_MISC_EXT testen. Diese Kennzeichen werden vom eingehenden Transportanbieter festgelegt und geben an, dass die Nachricht von einer Quelle stammt, die vom Gateway nicht als vertrauenswürdig eingestuft werden kann. Dies bedeutet, dass die Nachricht entweder außerhalb der Organisation oder intern, aber von einer Arbeitsstation stammt, die dem Gateway nicht bekannt ist. In jedem Fall wird die Identität des Absenders möglicherweise nicht bestätigt, und es besteht die Gefahr, dass ein Computervirus in die Organisation eingeführt wird. Der Client sollte dem Benutzer eine Warnmeldung anzeigen und eine Option zum Löschen der Nachricht anbieten, ohne sie zu öffnen. 
  
Nachrichtenspeicheranbieter legen das MSGFLAG_UNMODIFIED für eingehende Nachrichten festgelegt. MSGFLAG_UNMODIFIED gibt an, dass eine Nachricht seit der Zustellung nicht geändert wurde. Ein Client kann diesen Wert nicht löschen, nachdem er von einem Nachrichtenspeicheranbieter festgelegt wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Bietet Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgeführt sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANONISCHE EIGENSCHAFTEN VON MAPI](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

