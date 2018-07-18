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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f2e565dc8137edee441643a5d02a154f78737099
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19794613"
---
# <a name="pidtagmessageflags-canonical-property"></a>PidTagMessageFlags (kanonische Eigenschaft)

  
  
**Betrifft**: Outlook 
  
Enthält eine Bitmaske aus Flags, die angeben, den Ursprung und den aktuellen Status einer Nachricht. 
  
|||
|:-----|:-----|
|Zugeordneten Eigenschaften:  <br/> |PR_MESSAGE_FLAGS  <br/> |
|Bezeichner:  <br/> |0x0E07  <br/> |
|Datentyp:  <br/> |PT_LONG  <br/> |
|Bereich:  <br/> |Allgemeine messaging  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist eine Eigenschaft eines Nontransmittable zur das Senden und Empfangen von Enden einer Übertragung mit unterschiedlichen Werten abhängig von der Client-Anwendung oder Store Anbieter beteiligten verfügbar gemacht werden. Diese Eigenschaft wird durch den Speicheranbieter Client oder einer Nachricht, wenn eine Nachricht erstellt und zum ersten Mal gespeichert und dann aktualisiert in regelmäßigen Abständen durch den Anbieter für die Nachricht anmelden, eines Transportdienstes und die MAPI-Warteschlange wie die Nachricht verarbeitet wird und den Zustand initialisiert ändert. 
  
Diese Eigenschaft ist auf eine Nachricht vor und nach der Übermittlung, und klicken Sie auf alle Kopien der empfangenen Nachricht vorhanden. Auch wenn es sich nicht um ein Empfänger-Eigenschaft ist, wird es anders verfügbar gemacht, die auf jeden Empfänger entsprechend gibt an, ob sie lesen oder durch diesen Empfänger geändert wurde. 
  
Für diese Eigenschaft kann eine oder mehrere der folgenden Werte festgelegt werden:
  
MSGFLAG_ASSOCIATED 
  
> Die Nachricht ist eine zugehörige Nachricht eines Ordners. Der Client oder Anbieter verfügt über schreibgeschützten Zugriff auf dieses Flag. Das Flag MSGFLAG_READ ignoriert für zugeordnete Nachrichten, die einen gelesen/ungelesen Zustand nicht beibehalten. 
    
MSGFLAG_FROMME 
  
> Das messaging Benutzer senden, wurde die messaging-Benutzer empfangen der Nachricht. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag erst nach dem ersten Aufruf [IMAPIProp::SaveChanges](imapiprop-savechanges.md) und Read-only danach. Dieses Kennzeichen vom der Adressbuchhierarchie festgelegt werden soll. 
    
MSGFLAG_HASATTACH 
  
> Die Nachricht enthält mindestens eine Anlage. Dieses Kennzeichen entspricht der Nachricht **PR_HASATTACH** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))-Eigenschaft. Der Client hat schreibgeschützte Zugriff auf dieses Flag. 
    
MSGFLAG_NRN_PENDING 
  
> Ein Bericht nonread muss für die Nachricht gesendet werden. Der Client oder Anbieter verfügt über schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_ORIGIN_INTERNET 
  
> Die eingehende Nachricht angezeigt, über das Internet. Außerhalb der Organisation oder aus einer Datenquelle, die das Gateway berücksichtigen kann nicht vertrauenswürdige zurückgeht. Der Client sollte eine entsprechende Meldung für den Benutzer angezeigt werden. Transportanbieter legen Sie dieses Flag; der Client hat schreibgeschützte Zugriff. 
    
MSGFLAG_ORIGIN_MISC_EXT 
  
> Die eingehende Nachricht über eine externe Verknüpfung als x. 400- oder im Internet gelangen. Außerhalb der Organisation oder aus einer Datenquelle, die das Gateway berücksichtigen kann nicht vertrauenswürdige zurückgeht. Der Client sollte eine entsprechende Meldung für den Benutzer angezeigt werden. Transportanbieter legen Sie dieses Flag; der Client hat schreibgeschützte Zugriff. 
    
MSGFLAG_ORIGIN_X400 
  
> Die eingehende Nachricht angekommen über ein x. 400-Verbindung. Außerhalb der Organisation oder aus einer Datenquelle, die das Gateway berücksichtigen kann nicht vertrauenswürdige zurückgeht. Der Client sollte eine entsprechende Meldung für den Benutzer angezeigt werden. Transportanbieter legen Sie dieses Flag; der Client hat schreibgeschützte Zugriff. 
    
MSGFLAG_READ 
  
> Die Nachricht wird als gelesen markiert. Dies kann als Ergebnis eines Anrufs können Sie jederzeit auf [IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)auftreten. Clients können auch dieses Flag festlegen, indem Sie eine Nachricht **IMAPIProp::SetProps** -Methode aufrufen, bevor die Nachricht zum ersten Mal gespeichert wurde. Dieses Kennzeichen werden ignoriert, wenn das Flag **MSGFLAG_ASSOCIATED** festgelegt ist. 
    
MSGFLAG_RESEND 
  
> Die Nachricht enthält eine Anforderung für einen Vorgang erneut mit einem Unzustellbarkeitsbericht an. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag erst nach dem ersten Aufruf [IMAPIProp::SaveChanges](imapiprop-savechanges.md) und Read-only danach. 
    
MSGFLAG_RN_PENDING 
  
> Ein Bericht lesen muss für die Nachricht gesendet werden. Der Client oder Anbieter verfügt über schreibgeschützten Zugriff auf dieses Flag. 
    
MSGFLAG_SUBMIT 
  
> Die Nachricht wird für das Senden von nach einem Aufruf von [IMessage::SubmitMessage](imessage-submitmessage.md)markiert. Nachricht Anbieter legen Sie dieses Flag; der Client hat schreibgeschützte Zugriff. 
    
MSGFLAG_UNMODIFIED 
  
> Die ausgehende Nachricht wurde nicht seit der ersten geändert, das es gespeichert wurde; die eingehende Nachricht wurde nicht geändert, da er übermittelt wurde. 
    
MSGFLAG_UNSENT 
  
> Die Nachricht ist noch verfasst wird. Es wird gespeichert, aber nicht gesendet wurde. Der Client oder Anbieter hat Lese-/Schreibzugriff auf dieses Flag erst nach dem ersten Aufruf [IMAPIProp::SaveChanges](imapiprop-savechanges.md) und Read-only danach. Wenn ein Client dieses Flag jeweils festlegt, die die Nachricht gesendet wird, wird der Nachricht Speicheranbieter **IMessage::SubmitMessage** aufgerufen wird. In der Regel werden dieses Kennzeichen gelöscht, nachdem die Nachricht gesendet wird. 
    
Ein Client oder einer Nachricht Informationsdienst kann den aktuellen Status der Nachricht durch Aufrufen der [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode, um Werte für die Kennzeichen lesen können Sie jederzeit überprüfen. Der Client oder Anbieter können Sie auch die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode, um alle Flags ändern, die Lese-/Schreibzugriff besitzen aufrufen. 
  
Einige der Flags sind immer schreibgeschützt. Einige sind Lese-/Schreibzugriff, bis der erste Aufruf der [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode und danach sind schreibgeschützt, soweit **IMAPIProp::SetProps** ist. Eine der folgenden MSGFLAG_READ, kann über [IMessage::SetReadFlag](imessage-setreadflag.md) oder [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md)später geändert werden. 
  
Die Ausgangswerte für diese Eigenschaft sind in der Regel MSGFLAG_UNSENT und MSGFLAG_UNMODIFIED eine Meldung an, die noch nicht gesendet oder geändert wurde. Wenn eine Nachricht zum zweiten Mal gespeichert wird, löscht der Nachricht Speicheranbieter MSGFLAG_UNMODIFIED-Flag. Ein anderer Wert, den eine Nachricht Speicheranbieter festlegen kann, wenn eine Nachricht gespeichert ist ist das MSGFLAG_HASATTACH-Flag, was bedeutet, dass die Nachricht eine oder mehrere Anlagen enthält. Die **PR_HASATTACH** -Eigenschaft wird diese Einstellung berechnet. 
  
Wenn ein Client die [IMessage::SubmitMessage](imessage-submitmessage.md) -Methode zum Senden der Nachricht aufruft, wird die Nachrichtenanbieter erstellt eine Kopie für die MAPI-Warteschlange und aktualisiert diese Eigenschaft durch das MSGFLAG_SUBMIT-Flag festlegen. Der Nachricht Speicheranbieter festgelegt auch MSGFLAG_UNSENT, wenn sie noch nicht festgelegt ist. MSGFLAG_SUBMIT gibt an, dass **SubmitMessage** aufgerufen wurde, beginnen mit dem senden, und die Meldung lautet nun an den Client schreibgeschützt. MSGFLAG_UNSENT gibt an, dass die MAPI-Warteschlange die Nachricht behandelt wird. Wenn der Send-Prozess abgebrochen wird, setzt der Nachricht Informationsdienst dieses Flag zurück. 
  
Wenn die Meldung zur eines Transportdienstes für die Übermittlung angegeben wird, festgelegt der Adressbuchhierarchie das Flag MSGFLAG_FROMME, wenn der Absender dasselbe Konto auf dem Messagingserver hatte, wie auf die Nachricht empfangen wurde. Transportanbieter für festlegen MSGFLAG_FROMME für eine eingehende Nachricht, die von den derzeit angemeldeten Benutzer gesendet wurde. Ein Client kann diesen Wert verwenden, um zu bestimmen, dass es zum Anzeigen der Names der Empfänger in der Inhaltstabelle des Ordners gesendete Elemente als Absendernamen besser geeignet ist. Nachrichten, die während des Aktivierungsvorgangs Zusammensetzung gespeichert und noch nicht gesendet wurden, sollten auch mit Empfängernamen statt Absendernamen angezeigt werden. 
  
Für eine eingehende Nachricht löscht eine Nachricht Speicheranbieter die Kennzeichen MSGFLAG_READ gelesen-Status zurücksetzen. Ein Client festzulegen oder die MSGFLAG_READ Kennzeichnung löschen, wenn es erforderlich ist, ändern Sie den lesen-Status und das Senden von Lese- und nonread Berichte durch Aufrufen der Nachricht [IMessage::SetReadFlag](imessage-setreadflag.md) -Methode oder der Ordner [IMAPIFolder steuern kann:: SetReadFlags](imapifolder-setreadflags.md) Methode. Der Hauptunterschied zwischen diesen Methoden, als das Objekt implementieren, ist, dass die Folder-Methode eine, mehrere oder alle Nachrichten in den Ordner auswirken kann. Die Nachricht-Methode wirkt sich auf eine Nachricht. 
  
Außerdem sollten Sie ein Client eine eingehende Nachricht für die Flags MSGFLAG_ORIGIN_X400, MSGFLAG_ORIGIN_INTERNET und MSGFLAG_ORIGIN_MISC_EXT testen. Diese Flags werden von der eingehenden Adressbuchhierarchie festgelegt und darauf hinzuweisen, dass die Nachricht von einer Quelle gelangen, die das Gateway berücksichtigen kann nicht vertrauenswürdige. Dies bedeutet, dass die Nachricht stammt entweder außerhalb der Organisation oder intern jedoch von einer Arbeitsstation an das Gateway nicht bekannt. In jedem Fall die Identität des Absenders kann nicht bestätigt werden, und es wird ein Risiko dar, der einen Virus in der Organisation einführen. Der Client sollte dem Benutzer eine Warnmeldung angezeigt und bieten eine Möglichkeit, Löschen der Nachricht, ohne Sie zu öffnen. 
  
Nachricht Anbieter festlegen MSGFLAG_UNMODIFIED Flag für eingehende Nachrichten. MSGFLAG_UNMODIFIED gibt an, dass eine Nachricht nicht seit Übermittlung geändert wurde. Ein Client kann nicht dieser Wert zu löschen, nachdem er vom Anbieter eine Nachricht festgelegt wurde. 
  
## <a name="related-resources"></a>Verwandte Ressourcen

### <a name="protocol-specifications"></a>Protokollspezifikationen

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Nachrichten und Anlagen Objekte behandelt.
    
### <a name="header-files"></a>Header-Dateien

Mapidefs.h
  
> Enthält die Datentypdefinitionen.
    
Mapitags.h
  
> Enthält Definitionen von Eigenschaften, die als Alternative Namen aufgelistet.
    
## <a name="see-also"></a>Siehe auch



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)


[MAPI-Eigenschaften](mapi-properties.md)
  
[Kanonische MAPI-Eigenschaften](mapi-canonical-properties.md)
  
[Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen](mapping-canonical-property-names-to-mapi-names.md)
  
[Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen](mapping-mapi-names-to-canonical-property-names.md)

