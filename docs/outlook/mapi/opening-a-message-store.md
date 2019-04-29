---
title: Öffnen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 665c14b285db166e4f2a421d46e57f23e2f7ad52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432373"
---
# <a name="opening-a-message-store"></a>Öffnen eines Nachrichtenspeichers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Je nach Profil muss ein Client einen oder mehrere Nachrichtenspeicher während einer typischen Sitzung öffnen. Das Öffnen eines Nachrichtenspeichers ermöglicht den Zugriff auf einen Zeiger auf seine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) -Implementierung. Die **IMsgStore** -Schnittstelle stellt Methoden für Benachrichtigungen, Ordner Zuweisungen und den Zugriff auf Ordner und Nachrichten bereit. 
  
Clients öffnen Nachrichtenspeicher bei der Anmeldung und bei der Änderung eines Profils. Wenn Ihr Client Benutzern das Hinzufügen von Nachrichtenspeicher zu dem Profil während einer aktiven Sitzung ermöglicht, können Sie Sie entweder sofort öffnen oder bis zur nächsten Sitzung ignorieren. Wenn Sie sich für Benachrichtigungen in der Nachrichtenspeichertabelle registrieren, werden Sie über die Verfügbarkeit eines neuen Nachrichtenspeichers benachrichtigt.
  
Zum Öffnen eines Nachrichtenspeichers muss die Eintrags-ID verfügbar sein. Die meisten Clients greifen auf die Eintrags-IDs für die Nachrichtenspeicher zu, die Sie über die Nachrichtenspeichertabelle öffnen möchten. Einige Nachrichtenspeicher dokumentieren jedoch das Format Ihrer Eintrags-IDs und ermöglichen Clients somit, die Nachrichtenspeichertabelle zu umgehen und die erforderliche Eintrags-ID zu erstellen. Sie können diese Eintrags-ID direkt an [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) und MAPI wird automatisch einen Profil Abschnitt für den Anbieter ohne Zuordnung zu einem Nachrichtendienst. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Abrufen einer Eintrags-ID aus der Nachrichtenspeichertabelle
  
1. Rufen Sie [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) auf, um die Nachrichtenspeichertabelle zu öffnen. 
    
2. Rufen Sie **IMAPITable::** SetColumns auf, um die Tabelle auf einen kleinen Spaltensatz einzuschränken, der die folgenden Spalten enthält: 
    
   - **PR_PROVIDER_DISPLAY** oder **PR_DISPLAY_NAME**
   - **PR_ENTRYID** -Eigenschaften 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Erstellen Sie eine Einschränkung zum Filtern der Zeile, die den zu öffnenden Nachrichtenspeicher darstellt. Weitere Informationen zum Suchen nach dem Standardnachrichtenspeicher finden Sie unter [Öffnen des Standardnachrichten Speichers](opening-the-default-message-store.md). Wenn Sie nach einem Nachrichtenspeicher anhand des Namens suchen möchten, wenden Sie die folgenden Eigenschaftseinschränkungen an:
    
   - Vergleichen Sie **PR_PROVIDER_DISPLAY** ([pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md)) mit dem allgemeinen Namen für diesen Nachrichten Speichertyp. PR_PROVIDER_DISPLAY kann beispielsweise auf "Persönliche Ordner" festgelegt werden.
    
   - Vergleichen Sie **PR_MDB_PROVIDER** ([pidtagstoreprovider (](pidtagstoreprovider-canonical-property.md)) mit dem spezifischen **MAPIUID** für diesen Nachrichten Speichertyp. 
    
   - Vergleichen Sie **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen für diesen bestimmten Nachrichtenspeicher. **PR_DISPLAY_NAME** kann beispielsweise auf "meine Nachrichten für das geschäftsjahr 2010" festgelegt werden. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um die entsprechende Zeile aus der Nachrichtenspeichertabelle abzurufen. Der Eintragsbezeichner für die Zeile wird in das Eigenschafts Wertarray für das **aRow** -Element des Zeilen Satzes eingeschlossen, auf den durch den _pprows_ -Parameter verwiesen wird. 
    
5. Rufen Sie [FreeProws](freeprows.md) auf, um den Zeilensatz freizugeben, auf den von _pprows_verwiesen wird.
    
6. Geben Sie die Nachrichtenspeichertabelle durch Aufrufen der **IUnknown:: Release** -Methode frei. 
    
Wenn Sie einen benutzerdefinierten Eintragsbezeichner für den zu öffnenden Nachrichtenspeicher erstellt haben, rufen Sie die [WrapStoreEntryID](wrapstoreentryid.md) -Funktion auf, um Sie in eine Standardeintrags-ID zu konvertieren. 
  
Nachdem Sie die Eintrags-ID eines Nachrichtenspeichers angegeben haben, rufen Sie eine der folgenden Methoden auf, um Sie zu öffnen:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Rufen Sie **OpenMsgStore** auf, wenn Sie eine Vielzahl spezieller Optionen für den Nachrichtenspeicher angeben müssen. **OpenMsgStore** ermöglicht es Ihnen, die Anzeige von Dialogfeldern zu unterdrücken, den Nachrichtenspeicher als vorübergehend oder als nonmessaging-Speicher zu identifizieren, Zugriffsebenen festzulegen und Fehler zu verzögern. **** Mit OpenEntry können Sie nur Zugriffsebenen festlegen und Fehler zurückstellen. 
  
Das Festlegen des MDB_NO_MAIL-Flags gibt MAPI an, dass der Nachrichtenspeicher nicht zum Senden oder empfangen von Nachrichten verwendet wird. MAPI informiert den MAPI-Spooler nicht über das vorhanden sein dieses Nachrichtenspeichers. Das MDB_TEMPORARY-Flag kennzeichnet einen Nachrichtenspeicher als vorübergehend, was impliziert, dass er nicht zum Speichern von dauerhaften Informationen verwendet werden kann. Temporäre Nachrichtenspeicher werden nicht in der Nachrichtenspeichertabelle angezeigt. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

