---
title: Öffnen eines Nachrichtenspeichers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 43b23fd7-999a-42c0-8f4d-47f5de266bdb
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 39d6df6db329abf7509f816165341ea0eda8331b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793295"
---
# <a name="opening-a-message-store"></a>Öffnen eines Nachrichtenspeichers

**Betrifft**: Outlook 
  
Je nach dem Profil müssen ein Client einen oder mehrere Nachrichtenspeicher während einer normalen Sitzung zu öffnen. Öffnen eines Nachrichtenspeichers bedeutet den Zugriff auf einen Zeiger auf seine [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) Implementierung. Die **IMsgStore** -Schnittstelle stellt Methoden für die Benachrichtigung, Ordner Aufgaben durchführen und den Zugriff auf Ordner und Nachrichten. 
  
Öffnen Clients Nachrichtenspeicher bei der Anmeldung und ein Profil geändert wird. Wenn Ihre Client Benutzer Nachrichtenspeicher während einer aktiven Sitzung auf das Profil hinzufügen können, können Sie sofort zu öffnen oder bis zum nächsten Sitzung zu ignorieren. Durch die Registrierung für Benachrichtigungen auf die Tabelle Store, werden Sie für die Verfügbarkeit von einem neuen Nachrichtenspeicher benachrichtigt werden.
  
Um einen Nachrichtenspeicher zu öffnen, benötigen Sie die Eintrags-ID verfügbar. Die meisten Clients Zugriff auf den Eintrag-IDs für die Nachrichtenspeicher, den, die Sie durch die Nachricht Store Tabelle öffnen möchten. Eine Nachricht wird jedoch das Format der ihre Eintragsbezeichner, wodurch Clients zu umgehen die Nachricht Store Tabelle und erstellen die erforderlichen Eintrags-ID Dokument gespeichert. Sie können dieses Eintrags-ID direkt an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) übergeben und MAPI erstellt automatisch Profile-Abschnitt für den Anbieter ohne alle Messagingdiensts zuzuordnen. 
  
## <a name="retrieve-an-entry-identifier-from-the-message-store-table"></a>Abrufen eines Eintrags-ID aus der Nachricht Store-Tabelle
  
1. Rufen Sie [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) , um die Nachricht Store-Tabelle zu öffnen. 
    
2. Rufen Sie **IMAPITable::SetColumns** zum Beschränken der Tabelle einen Satz kleine Spalte, die die folgenden Spalten enthält: 
    
   - **PR_PROVIDER_DISPLAY** oder **PR_DISPLAY_NAME**
   - **PR_ENTRYID** -Eigenschaften 
   - **PR_MDB_PROVIDER**
   - **PR_RESOURCE_FLAGS**
    
3. Erstellen Sie eine Einschränkung, die Zeile herauszufiltern, die zum Öffnen des Nachrichtenspeichers darstellt. Weitere Informationen zu den standardmäßigen Nachrichtenspeicher Nachrichtensymbol finden Sie unter [Standard-Informationsspeicher zu öffnen](opening-the-default-message-store.md). Um für einen Nachrichtenspeicher nach Namen zu suchen, wenden Sie eines der folgenden Suchkriterien in Eigenschaft:
    
   - Übereinstimmung **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) mit den allgemeinen Namen für diesen Nachrichtenspeicher. Beispielsweise könnte PR_PROVIDER_DISPLAY auf "Persönliche Ordner" festgelegt werden.
    
   - Übereinstimmung **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) mit der bestimmte **MAPIUID** für diese Art von Nachrichtenspeicher. 
    
   - Übereinstimmung **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) mit dem Namen für diese bestimmten Nachrichtenspeicher. Beispielsweise kann auf "Meine Nachrichten für das Geschäftsjahr 2010" **PR_DISPLAY_NAME** festgelegt werden 
    
4. Rufen Sie [HrQueryAllRows](hrqueryallrows.md) zum Abrufen der entsprechenden Zeile aus der Nachricht Store-Tabelle. Die Eintrags-ID für die Zeile wird im Array Eigenschaft-Wert für die **aRow** Mitglied der Zeile auf das durch den Parameter _Pprows_ enthalten sein. 
    
5. Rufen Sie [FreeProws](freeprows.md) , um das Rowset fest, die auf den _Pprows_freizugeben.
    
6. Version der Nachricht Store Tabelle durch die **IUnknown** -Methode aufrufen. 
    
Wenn Sie einen benutzerdefinierten Eintrag Bezeichner für den Nachrichtenspeicher geöffnet werden erstellt haben, rufen Sie die [WrapStoreEntryID](wrapstoreentryid.md) -Funktion, um es in einer standard-Eintrags-ID zu konvertieren. 
  
Nachdem Sie einen Nachrichtenspeicher Eintrags-ID haben, rufen Sie eine der folgenden Methoden zu öffnen:
  
- [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
    
Rufen Sie **OpenMsgStore** , wenn Sie eine Vielzahl von speziellen Optionen für den Nachrichtenspeicher angeben müssen. **OpenMsgStore** können Sie zum Identifizieren des Nachrichtenspeichers als temporär oder als nonmessaging Speicher, Festlegen von Zugriffsebenen, unterdrückt die Anzeige von Dialogfeldern und Fehler zu verzögern. **OpenEntry** können Sie nur zum Festlegen von Zugriffsebenen und Fehler verzögern. 
  
Festlegen der MDB_NO_MAIL gibt an, Flag MAPI, dass der Nachrichtenspeicher nicht für das Senden oder Empfangen von Nachrichten verwendet wird. Informationen über das Vorhandensein dieses Nachrichtenspeichers informiert MAPI nicht die MAPI-Warteschlange. Das Flag MDB_TEMPORARY kennzeichnet einen Nachrichtenspeicher als temporären, sagen, dass sie zum Speichern von Daten verwendet werden kann. Temporäre Nachrichtenspeicher werden nicht in der Nachricht Store Tabelle angezeigt. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPITable::SetColumns](imapitable-setcolumns.md)

