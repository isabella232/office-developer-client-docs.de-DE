---
title: Statustabelle und Statusobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 774aaea0365066981b9d6426a2579160f6578844
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795631"
---
# <a name="status-table-and-status-objects"></a>Statustabelle und Statusobjekte

  
  
**Betrifft**: Outlook 
  
MAPI enthält eine Tabelle mit Informationen über den Status des MAPI-Subsystems, MAPI-Warteschlange, Adressbuch oder einem bestimmten Dienstanbieter. Sie können in dieser Tabelle durch Aufrufen von [IMAPISession::GetStatusTable](imapisession-getstatustable.md)zugreifen.
  
Jede Zeile in der Tabelle "Status" stellt ein Statusobjekt von MAPI oder einem Dienstanbieter implementiert. Ein Statusobjekt können Sie einen Anbieter Konfiguration Eigenschaftenfenster zum Ändern eines Kennworts Anbieter, den upload oder download von Nachrichten und zur Kommunikation mit einem bestimmten Adressbuchhierarchie anzuzeigen. 
  
Es gibt zwei Methoden, um ein Statusobjekt zuzugreifen:
  
- Durch die Statustabelle
    
- Über einem Anmeldeobjekt **OpenStatusEntry** -Methode 
    
Da Logon-Objekten für Clients als nicht verfügbar sind, müssen Sie die Statustabelle verwenden, Zugriff auf Objekte Status. Der Status Tabelle Ansatz ist indirekte, einige Anrufe erfordern, bevor das Statusobjekt geöffnet wird und ein Zeiger auf seine Implementierung **IMAPIStatus** zurückgegeben. 
  
 **Um die Statustabelle verwenden, öffnen Sie ein Statusobjekt**
  
1. Rufen Sie **IMAPIStatus::GetStatusTable** , um einen Zeiger [IMAPITable](imapitableiunknown.md) abzurufen. 
    
2. Rufen Sie die Statustabelle [IMAPITable::SetColumns](imapitable-setcolumns.md) -Methode zum Beschränken der Spalte **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) und **PR_DISPLAY_NAME** ([ festlegen PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Beschränken Sie die Tabellenansicht auf einen bestimmten Status-Objekt. Für Implementierungen MAPI kann ein Client eine eigenschaftseinschränkung mit **PR_RESOURCE_TYPE**definieren. Ein Client für Service Provider Implementierungen kann auf **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) den Namen des Anbieters, oder auf **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) den Namen des Anbieters DLL einschränken Datei.
    
4. Rufen Sie die [Methode IMAPITable:: Restrict](imapitable-restrict.md) , um die Einschränkung festzulegen. 
    
5. Rufen Sie [HrQueryAllRows](hrqueryallrows.md), indem Sie in der Struktur [SPropertyRestriction](spropertyrestriction.md) übergeben, um die Zeile abzurufen, die den Status des Anbieters darstellt. 
    
6. Rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md), angeben die Eintrags-ID aus der Tabellenzeile Status zum Öffnen Sie das Statusobjekt und Abrufen eines **IMAPIStatus** Zeigers. 
    
Rufen Sie [SettingsDialog den Status des Objekts](imapistatus-settingsdialog.md) für den Ziel-Anbieter, um einem Eigenschaftenfenster anzuzeigen. **SettingsDialog** zeigt ein Eigenschaftenblatt für die Anzeige und in einigen Fällen die Konfigurationseigenschaften eines Anbieters zu ändern. 
  
Rufen Sie die Kommunikation mit einem Adressbuchhierarchie des Status Objekts [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode. **ValidateState** können Neukonfigurieren ein Transportdienstes, verhindern, dass den Anbieter eine Benutzeroberfläche und steuern eine Sitzung, die von einem Remoteserver, je nach den Flags, denen Sie übergeben Nachrichtenkopfzeilen downloaden beinhaltet. Übergeben Sie um abzubrechen, das Herunterladen von remote-Header, beispielsweise das Flag ABORT_XP_HEADER_OPERATION an **ValidateState**. Um eine Verbindung herstellen oder vom Remoteserver zu trennen, übergeben Sie FORCE_XP_CONNECT oder FORCE_XP_DISCONNECT. Um den Anbieter neu konfigurieren möchten, übergeben Sie CONFIG_CHANGED. 
  
Clients, die implementiert werden senden oder Empfangen von Nachrichten bei Bedarf Aufrufen eines Transportdienstes oder der MAPI-Warteschlange [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) -Methode. Sie können drei Kennzeichen in die-Methode übergeben: FLUSH_UPLOAD, FLUSH_DOWNLOAD und FLUSH_FORCE. FLUSH_UPLOAD weist den Anbieter oder die MAPI-Warteschlange zum Senden von Nachrichten in der Ausgabewarteschlange wartet, während FLUSH_DOWNLOAD des Anbieters weist oder die MAPI-Warteschlange empfangen alle eingehenden Nachrichten. FLUSH_FORCE können dazu führen, dass das Statusobjekt zum Ausführen der Flush unabhängig von den Zeitpunkt mit einem anderen Flags festgelegt werden. 
  
Davon ausgehen, dass **SettingsDialog** oder [ChangePassword](imapistatus-changepassword.md) auf eines der MAPI-Subsystems, MAPI-Warteschlange oder Adresse Adressbuch Status Objekte aufrufen können. Die Subsystem und die Adresse Status Book-Objekten unterstützen nur **ValidateState**; das MAPI-Warteschlange Status-Objekt unterstützt **FlushQueues** zusätzlich zu **ValidateState**.
  
## <a name="see-also"></a>Siehe auch



[Statustabellen](status-tables.md)
  
[MAPI-Status-Objekte](mapi-status-objects.md)

