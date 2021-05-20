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
  
Je nach Profil muss ein Client während einer typischen Sitzung mindestens einen Nachrichtenspeicher öffnen. Wenn Sie einen Nachrichtenspeicher öffnen, erhalten Sie Zugriff auf einen Zeiger auf die [IMsgStore : IMAPIProp-Implementierung.](imsgstoreimapiprop.md) Die **IMsgStore-Schnittstelle** bietet Methoden für die Benachrichtigung, das Erstellen von Ordnerzuweisungen und den Zugriff auf Ordner und Nachrichten. 
  
Clients öffnen Nachrichtenspeicher bei der Anmeldung und bei der Änderung eines Profils. Wenn Ihr Client Benutzern das Hinzufügen von Nachrichtenspeichern zum Profil während einer aktiven Sitzung ermöglicht, können Sie sie entweder sofort öffnen oder bis zur nächsten Sitzung ignorieren. Durch die Registrierung für Benachrichtigungen in der Nachrichtenspeichertabelle werden Sie auf die Verfügbarkeit eines neuen Nachrichtenspeichers aufmerksam.
  
Zum Öffnen eines Nachrichtenspeichers muss der Eintragsbezeichner verfügbar sein. Die meisten Clients greifen auf die Eintragsbezeichner für die Nachrichtenspeicher zu, die sie über die Nachrichtenspeichertabelle öffnen möchten. Einige Nachrichtenspeicher dokumentieren jedoch das Format ihrer Eintragsbezeichner, wodurch Clients die Tabelle des Nachrichtenspeichers umgehen und die erforderliche Eintrags-ID erstellen können. Sie können diese Eintrags-ID direkt an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) übergeben, und MAPI erstellt automatisch einen Profilabschnitt für den Anbieter, ohne ihn einem Nachrichtendienst zuzuordnen. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Abrufen einer Eintrags-ID aus der Nachrichtenspeichertabelle
  
1. Rufen [Sie IMAPISession::GetMsgStoresTable auf,](imapisession-getmsgstorestable.md) um die Nachrichtenspeichertabelle zu öffnen. 
    
2. Rufen **Sie IMAPITable::SetColumns auf,** um die Tabelle auf einen kleinen Spaltensatz zu beschränken, der die folgenden Spalten enthält: 
    
   - **PR_PROVIDER_DISPLAY** oder **PR_DISPLAY_NAME**
   - **PR_ENTRYID** Eigenschaften 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Erstellen Sie eine Einschränkung, um die Zeile herausfiltern, die den zu öffnende Nachrichtenspeicher darstellt. Weitere Informationen zum Suchen nach dem Standardnachrichtenspeicher finden Sie unter [Öffnen des Standardnachrichtenspeichers Store](opening-the-default-message-store.md). Wenden Sie eine der folgenden Eigenschaftseinschränkungen an, um nach einem Nachrichtenspeicher nach Namen zu suchen:
    
   - Match **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) mit dem allgemeinen Namen für diesen Typ von Nachrichtenspeicher. Beispielsweise kann PR_PROVIDER_DISPLAY "Persönliche Ordner" festgelegt werden.
    
   - Match **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) mit der spezifischen **MAPIUID** für diesen Typ von Nachrichtenspeicher. 
    
   - Match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen für diesen bestimmten Nachrichtenspeicher. Beispielsweise kann **PR_DISPLAY_NAME** auf "Meine Nachrichten für das Geschäftsjahr 2010" festgelegt werden. 
    
4. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md) um die entsprechende Zeile aus der Nachrichtenspeichertabelle abzurufen. Der Eintragsbezeichner für die Zeile wird im Eigenschaftenwertarray für das **aRow-Element** der Zeilensatz enthalten, auf die der  _pprows-Parameter_ verweist. 
    
5. Rufen [Sie FreeProws auf,](freeprows.md) um den Zeilensatz frei zu machen, auf den _pprows verweist._
    
6. Geben Sie die Tabelle für den Nachrichtenspeicher frei, indem Sie die **IUnknown::Release-Methode** aufrufen. 
    
Wenn Sie einen benutzerdefinierten Eintragsbezeichner für den zu öffnenden Nachrichtenspeicher erstellt haben, rufen Sie die [WrapStoreEntryID-Funktion](wrapstoreentryid.md) auf, um sie in einen Standardeintragsbezeichner zu konvertieren. 
  
Nachdem Sie den Eintragsbezeichner eines Nachrichtenspeichers verwendet haben, rufen Sie eine der folgenden Methoden auf, um ihn zu öffnen:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Rufen **Sie OpenMsgStore** auf, wenn Sie eine Vielzahl spezieller Optionen für den Nachrichtenspeicher angeben müssen. **Mit OpenMsgStore** können Sie die Anzeige von Dialogfeldern unterdrücken, den Nachrichtenspeicher als temporär oder als Nichtmessagingspeicher identifizieren, Zugriffsebenen festlegen und Fehler zurückspeichern. **Mit OpenEntry** können Sie nur Zugriffsebenen festlegen und Fehler aufschubsen. 
  
Das Festlegen MDB_NO_MAIL zeigt MAPI an, dass der Nachrichtenspeicher nicht zum Senden oder Empfangen von Nachrichten verwendet wird. MAPI informiert den MAPI-Spooler nicht über das Vorhandensein dieses Nachrichtenspeichers. Das MDB_TEMPORARY kennzeichnet einen Nachrichtenspeicher als temporär, was bedeutet, dass er nicht zum Speichern dauerhafter Informationen verwendet werden kann. Temporäre Nachrichtenspeicher werden nicht in der Nachrichtenspeichertabelle angezeigt. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

