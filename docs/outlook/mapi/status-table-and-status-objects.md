---
title: Statustabelle und Statusobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425176"
---
# <a name="status-table-and-status-objects"></a>Statustabelle und Statusobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI enthält eine Tabelle mit Informationen zum Status des MAPI-Subsystems, des MAPI-Spoolers, des Adressbuchs oder eines bestimmten Dienstanbieters. Sie können auf diese Tabelle zugreifen, indem Sie [IMAPISession::GetStatusTable aufrufen.](imapisession-getstatustable.md)
  
Jede Zeile in der Statustabelle stellt ein status-Objekt dar, das von MAPI oder einem Dienstanbieter implementiert wurde. Mit einem Statusobjekt können Sie das Konfigurationseigenschaftsblatt eines Anbieters anzeigen, ein Anbieterkennwort ändern, Nachrichten hochladen oder herunterladen und mit einem bestimmten Transportanbieter kommunizieren. 
  
Es gibt zwei Möglichkeiten für den Zugriff auf ein Statusobjekt:
  
- Durch die Statustabelle
    
- Über die **OpenStatusEntry-Methode eines Anmeldeobjekts** 
    
Da Anmeldeobjekte für Clients nicht verfügbar sind, müssen Sie die Statustabelle verwenden, um auf Statusobjekte zu zugreifen. Der Ansatz der Statustabelle ist indirekt und erfordert einige Aufrufe, bevor das status-Objekt geöffnet wird, und ein Zeiger auf seine **IMAPIStatus-Implementierung** wird zurückgegeben. 
  
 **So öffnen Sie ein Statusobjekt mithilfe der Statustabelle**
  
1. Rufen **Sie IMAPIStatus::GetStatusTable auf,** um einen [IMAPITable-Zeiger abzurufen.](imapitableiunknown.md) 
    
2. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zu beschränken.
    
3. Beschränken Sie die Tabellenansicht auf ein bestimmtes Statusobjekt. Für MAPI-Implementierungen kann ein Client eine Eigenschaftseinschränkung mithilfe von **PR_RESOURCE_TYPE.** Bei Dienstanbieterimplementierung kann ein Client **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), den Namen des Anbieters oder **auf PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) den Namen der Anbieter-DLL-Datei einschränken.
    
4. Rufen [Sie IMAPITable::Restrict auf, um](imapitable-restrict.md) die Einschränkung zu setzen. 
    
5. Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md)und übergeben Sie die [SPropertyRestriction-Struktur,](spropertyrestriction.md) um die Zeile abzurufen, die den Status des Anbieters darstellt. 
    
6. Rufen [Sie IMAPISession::OpenEntry](imapisession-openentry.md)auf, und geben Sie den Eintragsbezeichner aus der Zeile der Statustabelle an, um das Statusobjekt zu öffnen und einen **IMAPIStatus-Zeiger abzurufen.** 
    
Rufen Sie zum Anzeigen eines Eigenschaftenblatts die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) des Statusobjekts für den Zielanbieter auf. **SettingsDialog zeigt** ein Eigenschaftenblatt zum Anzeigen und in einigen Fällen zum Ändern der Konfigurationseigenschaften eines Anbieters an. 
  
Um mit einem Transportanbieter zu kommunizieren, rufen Sie die [IMAPIStatus::ValidateState-Methode des Statusobjekts](imapistatus-validatestate.md) auf. **ValidateState** kann einen Transportanbieter neu konfigurieren, verhindern, dass der Anbieter eine Benutzeroberfläche anzeigen kann, und eine Sitzung steuern, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver erfordert, abhängig von den von Ihnen übergebenen Flags. Wenn Sie beispielsweise das Herunterladen von Remoteheadern abbrechen möchten, übergeben Sie das ABORT_XP_HEADER_OPERATION **an ValidateState**. Um eine Verbindung mit dem Remoteserver herzustellen oder die Verbindung zu trennen, übergeben FORCE_XP_CONNECT oder FORCE_XP_DISCONNECT. Um den Anbieter neu zu konfigurieren, übergeben Sie CONFIG_CHANGED. 
  
Clients, die das Senden oder Empfangen von Nachrichten bei Bedarf implementieren, rufen entweder die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) eines Transportanbieters oder des MAPI-Spoolers auf. Sie können drei Flags an die Methode übergeben: FLUSH_UPLOAD, FLUSH_DOWNLOAD und FLUSH_FORCE. FLUSH_UPLOAD an den Anbieter oder den MAPI-Spooler, alle nachrichten zu senden, die in der Ausgabewarteschlange warten, während FLUSH_DOWNLOAD den Anbieter oder den MAPI-Spooler anweisen, eingehende Nachrichten zu empfangen. FLUSH_FORCE kann mit einem der anderen Flags festgelegt werden, damit das status-Objekt die Leerung unabhängig vom Zeitpunkt ausführen kann. 
  
Erwarten Sie nicht, dass **SettingsDialog** oder [ChangePassword](imapistatus-changepassword.md) für eines der MAPI-Subsysteme, MAPI-Spooler- oder Adressbuchstatusobjekte aufrufen können. Sowohl die Subsystem- als auch die Adressbuchstatusobjekte unterstützen **nur ValidateState**; Das MAPI-Spoolerstatusobjekt unterstützt **FlushQueues** zusätzlich zu **ValidateState**.
  
## <a name="see-also"></a>Siehe auch



[Statustabellen](status-tables.md)
  
[MAPI-Statusobjekte](mapi-status-objects.md)

