---
title: Öffnen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 428b5b59a5f1a73ae440e4406a5a2971fed26b39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610097"
---
# <a name="opening-a-message-store"></a>Öffnen eines Nachrichtenspeichers

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Je nach Profil muss ein Client während einer typischen Sitzung einen oder mehrere Nachrichtenspeicher öffnen. Das Öffnen eines Nachrichtenspeichers bedeutet, zugriff auf einen Zeiger auf dessen [IMsgStore: IMAPIProp-Implementierung](imsgstoreimapiprop.md) zu erhalten. Die **IMsgStore-Schnittstelle** bietet Methoden zum Benachrichtigen, Erstellen von Ordnerzuweisungen und Zugreifen auf Ordner und Nachrichten. 
  
Clients öffnen Nachrichtenspeicher bei der Anmeldung und beim Ändern eines Profils. Wenn Ihr Client Benutzern ermöglicht, dem Profil während einer aktiven Sitzung Nachrichtenspeicher hinzuzufügen, können Sie sie entweder sofort öffnen oder bis zur nächsten Sitzung ignorieren. Durch die Registrierung für Benachrichtigungen in der Nachrichtenspeichertabelle werden Sie über die Verfügbarkeit eines neuen Nachrichtenspeichers informiert.
  
Um einen Nachrichtenspeicher zu öffnen, muss der Eintragsbezeichner verfügbar sein. Die meisten Clients greifen auf die Eintrags-IDs für die Nachrichtenspeicher zu, die sie über die Nachrichtenspeichertabelle öffnen möchten. Einige Nachrichtenspeicher dokumentieren jedoch das Format ihrer Eintragsbezeichner, wodurch Clients die Tabelle des Nachrichtenspeichers umgehen und den erforderlichen Eintragsbezeichner erstellen können. Sie können diesen Eintragsbezeichner direkt an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) übergeben, und MAPI erstellt automatisch einen Profilabschnitt für den Anbieter, ohne ihn einem Nachrichtendienst zuzuordnen. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Abrufen eines Eintragsbezeichners aus der Nachrichtenspeichertabelle
  
1. Rufen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) auf, um die Nachrichtenspeichertabelle zu öffnen. 
    
2. Rufen Sie **IMAPITable::SetColumns** auf, um die Tabelle auf einen kleinen Spaltensatz zu beschränken, der die folgenden Spalten enthält: 
    
   - **PR_PROVIDER_DISPLAY** oder **PR_DISPLAY_NAME**
   - **PR_ENTRYID** Eigenschaften 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Erstellen Sie eine Einschränkung, um die Zeile herauszufiltern, die den zu öffnenden Nachrichtenspeicher darstellt. Weitere Informationen zum Suchen nach dem Standardnachrichtenspeicher finden Sie unter [Öffnen der Standardnachricht Store](opening-the-default-message-store.md). Um nach einem Nachrichtenspeicher anhand des Namens zu suchen, wenden Sie eine der folgenden Eigenschaftseinschränkungen an:
    
   - Match **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) with the general name for this type of message store. Beispielsweise kann PR_PROVIDER_DISPLAY auf "Persönliche Ordner" festgelegt werden.
    
   - Match **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) with the specific **MAPIUID** for this type of message store. 
    
   - Match **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name for this particular message store. Beispielsweise kann **PR_DISPLAY_NAME** auf "My Messages for Fiscal Year 2010" festgelegt sein. 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um die entsprechende Zeile aus der Nachrichtenspeichertabelle abzurufen. Der Eintragsbezeichner für die Zeile wird in das Eigenschaftswertarray für das **aRow-Element** der Zeilengruppe eingeschlossen, auf die durch den  _Pprows-Parameter_ verwiesen wird. 
    
5. Rufen Sie [FreeProws](freeprows.md) auf, um die Zeile freizugeben, auf die durch  _Pprows_ verwiesen wird.
    
6. Geben Sie die Nachrichtenspeichertabelle frei, indem Sie die **IUnknown::Release-Methode** aufrufen. 
    
Wenn Sie einen benutzerdefinierten Eintragsbezeichner für den zu öffnenden Nachrichtenspeicher erstellt haben, rufen Sie die [WrapStoreEntryID-Funktion](wrapstoreentryid.md) auf, um sie in einen Standardeintragsbezeichner zu konvertieren. 
  
Nachdem Sie über die Eintrags-ID eines Nachrichtenspeichers verfügen, rufen Sie eine der folgenden Methoden auf, um sie zu öffnen:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Rufen Sie **OpenMsgStore** auf, wenn Sie eine Vielzahl spezieller Optionen für den Nachrichtenspeicher angeben müssen. **OpenMsgStore** ermöglicht es Ihnen, die Anzeige von Dialogfeldern zu unterdrücken, den Nachrichtenspeicher als temporären speicher oder als nicht zusammenhängenden Speicher zu identifizieren, Zugriffsebenen festzulegen und Fehler zu verzögern. **Mit OpenEntry** können Sie nur Zugriffsebenen festlegen und Fehler zurückstellen. 
  
Das Festlegen des MDB_NO_MAIL Flags gibt der MAPI an, dass der Nachrichtenspeicher nicht zum Senden oder Empfangen von Nachrichten verwendet wird. Die MAPI informiert den MAPI-Spooler nicht über das Vorhandensein dieses Nachrichtenspeichers. Das flag MDB_TEMPORARY legt einen Nachrichtenspeicher als temporär fest, was bedeutet, dass er nicht zum Speichern dauerhafter Informationen verwendet werden kann. Temporäre Nachrichtenspeicher werden nicht in der Nachrichtenspeichertabelle angezeigt. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

