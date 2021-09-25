---
title: PidTagMessageFlags (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageFlags
api_type:
- HeaderDef
ms.assetid: 7561112b-ca72-4c49-a8a0-cc1879a4e151
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d30046f7ec6b5ac3f83478769b9fd06e29f8bd7f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587475"
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
   
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft ist eine nicht übermittbare Nachrichteneigenschaft, die sowohl am sendenden als auch am empfangenden Ende einer Übertragung verfügbar gemacht wird, mit unterschiedlichen Werten, je nach beteiligter Clientanwendung oder Speicheranbieter. Diese Eigenschaft wird vom Client oder Nachrichtenspeicheranbieter initialisiert, wenn eine Nachricht zum ersten Mal erstellt und gespeichert und dann regelmäßig vom Nachrichtenspeicheranbieter, einem Transportanbieter und dem MAPI-Spooler aktualisiert wird, wenn die Nachricht verarbeitet wird und sich der Status ändert. 
  
Diese Eigenschaft ist sowohl für eine Nachricht vor als auch nach der Übermittlung und für alle Kopien der empfangenen Nachricht vorhanden. Obwohl es sich nicht um eine Empfängereigenschaft handelt, wird sie für jeden Empfänger unterschiedlich verfügbar gemacht, je nachdem, ob sie von diesem Empfänger gelesen oder geändert wurde. 
  
Mindestens eines der folgenden Flags kann für diese Eigenschaft festgelegt werden:
  
MSGFLAG_ASSOCIATED 
  
> Die Nachricht ist eine zugeordnete Nachricht eines Ordners. Der Client oder Anbieter hat schreibgeschützten Zugriff auf dieses Flag. Das flag MSGFLAG_READ wird für zugeordnete Nachrichten ignoriert, die keinen Lese-/Ungelesen-Status beibehalten. 
    
MSGFLAG_FROMME 
  
> Der Nachrichtenbenutzer, der die Nachricht empfängt, war der Nachrichtenbenutzer, der die Nachricht empfängt. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) erfolgt und danach schreibgeschützt ist. Dieses Kennzeichen sollte vom Transportanbieter festgelegt werden. 
    
MSGFLAG_HASATTACH 
  
> Die Nachricht hat mindestens eine Anlage. Dieses Flag entspricht der **eigenschaft PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md)) der Nachricht. Der Client hat schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_NRN_PENDING 
  
> Für die Nachricht muss ein nicht gelesener Bericht gesendet werden. Der Client oder Anbieter hat schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Die eingehende Nachricht wurde über das Internet empfangen. Er stammt entweder außerhalb der Organisation oder von einer Quelle, die das Gateway nicht als vertrauenswürdig betrachten kann. Der Client sollte dem Benutzer eine entsprechende Meldung anzeigen. Transportanbieter legen dieses Kennzeichen fest. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Die eingehende Nachricht wurde über einen anderen externen Link als X.400 oder das Internet empfangen. Er stammt entweder außerhalb der Organisation oder von einer Quelle, die das Gateway nicht als vertrauenswürdig betrachten kann. Der Client sollte dem Benutzer eine entsprechende Meldung anzeigen. Transportanbieter legen dieses Kennzeichen fest. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_ORIGIN_X400 
  
> Die eingehende Nachricht wurde über einen X.400-Link empfangen. Er stammt entweder außerhalb der Organisation oder von einer Quelle, die das Gateway nicht als vertrauenswürdig betrachten kann. Der Client sollte dem Benutzer eine entsprechende Meldung anzeigen. Transportanbieter legen dieses Kennzeichen fest. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_READ 
  
> Die Nachricht ist als gelesen gekennzeichnet. Dies kann als Ergebnis eines Aufrufs von [IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)auftreten. Clients können dieses Flag auch festlegen, indem sie die **IMAPIProp::SetProps-Methode** einer Nachricht aufrufen, bevor die Nachricht zum ersten Mal gespeichert wurde. Dieses Flag wird ignoriert, wenn das **MSGFLAG_ASSOCIATED-Flag** festgelegt ist. 
    
MSGFLAG_RESEND 
  
> Die Nachricht enthält eine Anforderung für einen erneuten Vorgang mit einem Nicht-Löschbericht. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) erfolgt und danach schreibgeschützt ist. 
    
MSGFLAG_RN_PENDING 
  
> Für die Nachricht muss ein Lesebericht gesendet werden. Der Client oder Anbieter hat schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_SUBMIT 
  
> Die Nachricht ist für das Senden als Ergebnis eines Aufrufs von [IMessage::SubmitMessage](imessage-submitmessage.md)markiert. Nachrichtenspeicheranbieter legen dieses Kennzeichen fest. Der Client hat schreibgeschützten Zugriff. 
    
MSGFLAG_UNMODIFIED 
  
> Die ausgehende Nachricht wurde seit dem ersten Speichern nicht mehr geändert. Die eingehende Nachricht wurde seit der Zustellung nicht geändert. 
    
MSGFLAG_UNSENT 
  
> Die Nachricht wird noch verfasst. Sie wird gespeichert, aber nicht gesendet. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag, bis der erste [IMAPIProp::SaveChanges-Aufruf](imapiprop-savechanges.md) erfolgt und danach schreibgeschützt ist. Wenn ein Client dieses Kennzeichen nicht zum Zeitpunkt des Sendens der Nachricht festlegt, legt der Nachrichtenspeicheranbieter es fest, wenn **IMessage::SubmitMessage** aufgerufen wird. In der Regel wird dieses Flag gelöscht, nachdem die Nachricht gesendet wurde. 
    
Ein Client- oder Nachrichtenspeicheranbieter kann den aktuellen Status der Nachricht jederzeit überprüfen, indem er die [IMAPIProp::GetProps-Methode aufruft,](imapiprop-getprops.md) um die Flagwerte zu lesen. Der Client oder Anbieter kann auch die [IMAPIProp::SetProps-Methode](imapiprop-setprops.md) aufrufen, um alle Flags zu ändern, die derzeit Lese-/Schreibzugriff haben. 
  
Einige der Flags sind immer schreibgeschützt. Einige sind bis zum ersten Aufruf der [IMAPIProp::SaveChanges-Methode](imapiprop-savechanges.md) lese-/schreibgeschützt, was **IMAPIProp::SetProps** betrifft. Eine dieser MSGFLAG_READ kann später über [IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)geändert werden. 
  
Die Anfänglichen Werte für diese Eigenschaft werden in der Regel MSGFLAG_UNSENT und MSGFLAG_UNMODIFIED, um eine Nachricht anzugeben, die noch nicht gesendet oder geändert wurde. Wenn eine Nachricht zum zweiten Mal gespeichert wird, löscht der Nachrichtenspeicheranbieter das MSGFLAG_UNMODIFIED Flag. Ein weiterer Wert, den ein Nachrichtenspeicheranbieter festlegen kann, wenn eine Nachricht gespeichert wird, ist das flag MSGFLAG_HASATTACH, das angibt, dass die Nachricht mindestens eine Anlage enthält. Die **PR_HASATTACH-Eigenschaft** wird anhand dieser Einstellung berechnet. 
  
Wenn ein Client die [IMessage::SubmitMessage-Methode](imessage-submitmessage.md) aufruft, um die Nachricht zu senden, erstellt der Nachrichtenspeicheranbieter eine Kopie davon für den MAPI-Spooler und aktualisiert diese Eigenschaft durch Festlegen des MSGFLAG_SUBMIT Flags. Der Nachrichtenspeicheranbieter legt auch MSGFLAG_UNSENT fest, wenn er noch nicht festgelegt ist. MSGFLAG_SUBMIT gibt an, dass **SubmitMessage** aufgerufen wurde, den Sendevorgang beginnt und die Nachricht jetzt schreibgeschützt für den Client ist. MSGFLAG_UNSENT gibt an, dass der MAPI-Spooler die Nachricht verarbeitet. Wenn der Sendevorgang abgebrochen wird, setzt der Nachrichtenspeicheranbieter dieses Flag zurück. 
  
Wenn die Nachricht an einen Transportanbieter für die Zustellung übergeben wird, legt der Transportanbieter das MSGFLAG_FROMME Flag fest, wenn der Absender dasselbe Konto auf dem Messagingserver hatte, auf dem die Nachricht empfangen wurde. Transportanbieter legen MSGFLAG_FROMME für eine eingehende Nachricht fest, die vom aktuell angemeldeten Benutzer gesendet wurde. Ein Client kann diesen Wert verwenden, um zu bestimmen, ob es besser ist, Empfängernamen im Inhaltsverzeichnis des Ordners "Gesendete Elemente" anzuzeigen als Absendernamen. Nachrichten, die während des Kompositionsprozesses gespeichert und noch nicht gesendet wurden, sollten auch mit Empfängernamen und nicht mit Absendernamen angezeigt werden. 
  
Bei einer eingehenden Nachricht löscht ein Nachrichtenspeicheranbieter das MSGFLAG_READ Flag, um den Lesestatus zurückzusetzen. Ein Client kann das MSGFLAG_READ Flag festlegen oder deaktivieren, wenn es erforderlich ist, den Lesestatus zu ändern und das Senden von Lese- und nicht gelesenen Berichten zu steuern, indem er entweder die [IMessage::SetReadFlag-Methode](imessage-setreadflag.md) der Nachricht oder die [IMAPIFolder::SetReadFlags-Methode](imapifolder-setreadflags.md) des Ordners aufruft. Der Hauptunterschied zwischen diesen Methoden, außer dem Objekt, das sie implementiert, besteht darin, dass sich die Ordnermethode auf eine, mehrere oder alle Nachrichten im Ordner auswirken kann. Die Nachrichtenmethode wirkt sich auf eine einzelne Nachricht aus. 
  
Ein Client sollte außerdem eine eingehende Nachricht für die Flags MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET und MSGFLAG_ORIGIN_MISC_EXT testen. Diese Flags werden vom Anbieter für eingehenden Transport festgelegt und geben an, dass die Nachricht von einer Quelle empfangen wurde, die das Gateway nicht als vertrauenswürdig betrachten kann. Dies bedeutet, dass die Nachricht entweder außerhalb der Organisation oder intern, aber von einer Arbeitsstation stammt, die dem Gateway nicht bekannt ist. In jedem Fall kann die Identität des Absenders nicht bestätigt werden, und es besteht das Risiko, dass ein Computerviren in die Organisation gelangt. Der Client sollte dem Benutzer eine Warnmeldung anzeigen und eine Option zum Löschen der Nachricht anbieten, ohne sie zu öffnen. 
  
Nachrichtenspeicheranbieter legen das MSGFLAG_UNMODIFIED Flag für eingehende Nachrichten fest. MSGFLAG_UNMODIFIED gibt an, dass eine Nachricht seit der Zustellung nicht geändert wurde. Ein Client kann diesen Wert nicht löschen, nachdem er von einem Nachrichtenspeicheranbieter festgelegt wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Enthält Verweise auf verwandte Exchange Server Protokollspezifikationen.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Behandelt Nachrichten- und Anlagenobjekte.
    
### <a name="header-files"></a>Headerdateien

Mapidefs.h
  
> Stellt Datentypdefinitionen bereit.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als alternative Namen aufgelistet sind.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[KANonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen kanonischer Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonischen Eigenschaftsnamen](mapping-mapi-names-to-canonical-property-names.md)

