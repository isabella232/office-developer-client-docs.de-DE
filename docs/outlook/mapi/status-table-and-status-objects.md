---
title: StatusTabellen- und Statusobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b982b6ba528091e574e927edc8ab5cc9f8233e6d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566374"
---
# <a name="status-table-and-status-objects"></a>StatusTabellen- und Statusobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die MAPI stellt eine Tabelle mit Informationen zum Status des MAPI-Subsystems, des MAPI-Spoolers, des Adressbuchs oder eines bestimmten Dienstanbieters bereit. Sie können auf diese Tabelle zugreifen, indem Sie [IMAPISession::GetStatusTable](imapisession-getstatustable.md)aufrufen.
  
Jede Zeile in der Statustabelle stellt ein Statusobjekt dar, das von MAPI oder einem Dienstanbieter implementiert wird. Mit einem Statusobjekt können Sie das Konfigurationseigenschaftenblatt eines Anbieters anzeigen, ein Anbieterkennwort ändern, Nachrichten hochladen oder herunterladen und mit einem bestimmten Transportanbieter kommunizieren. 
  
Es gibt zwei Möglichkeiten, auf ein Statusobjekt zuzugreifen:
  
- Durch die Statustabelle
    
- Über die **OpenStatusEntry-Methode** eines Anmeldeobjekts 
    
Da Anmeldeobjekte für Clients nicht verfügbar sind, müssen Sie die Statustabelle verwenden, um auf Statusobjekte zuzugreifen. Der Statustabellenansatz ist indirekt, sodass einige Aufrufe erforderlich sind, bevor das Statusobjekt geöffnet und ein Zeiger auf die **IMAPIStatus-Implementierung** zurückgegeben wird. 
  
 **So öffnen Sie ein Statusobjekt mithilfe der Statustabelle**
  
1. Rufen Sie **IMAPIStatus::GetStatusTable** auf, um einen [IMAPITable-Zeiger](imapitableiunknown.md) abzurufen. 
    
2. Rufen Sie die [IMAPITable::SetColumns-Methode](imapitable-setcolumns.md) der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) und **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) zu beschränken.
    
3. Beschränken Sie die Tabellenansicht auf ein bestimmtes Statusobjekt. Bei MAPI-Implementierungen kann ein Client eine Eigenschaftseinschränkung mit **PR_RESOURCE_TYPE** definieren. Bei Dienstanbieterimplementierungen kann ein Client den Namen **der** Anbieter-DLL-Datei auf PR_PROVIDER_DISPLAY ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), den Namen des Anbieters oder auf **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) beschränken.
    
4. Rufen Sie [IMAPITable::Restrict](imapitable-restrict.md) auf, um die Einschränkung festzulegen. 
    
5. Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie die [SPropertyRestriction-Struktur,](spropertyrestriction.md) um die Zeile abzurufen, die den Status des Anbieters darstellt. 
    
6. Rufen Sie [IMAPISession::OpenEntry](imapisession-openentry.md)auf, und geben Sie den Eintragsbezeichner aus der Statustabellenzeile an, um das Statusobjekt zu öffnen und einen **IMAPIStatus-Zeiger** abzurufen. 
    
Rufen Sie zum Anzeigen eines Eigenschaftenblatts die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) des Statusobjekts für den Zielanbieter auf. **SettingsDialog** zeigt ein Eigenschaftenfenster zum Anzeigen und in einigen Fällen zum Ändern der Konfigurationseigenschaften eines Anbieters an. 
  
Um mit einem Transportanbieter zu kommunizieren, rufen Sie die [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) des Statusobjekts auf. **ValidateState** kann einen Transportanbieter neu konfigurieren, verhindern, dass der Anbieter eine Benutzeroberfläche anzeigt, und eine Sitzung steuern, bei der Nachrichtenheader von einem Remoteserver heruntergeladen werden, je nach den von Ihnen übergebenen Flags. Um beispielsweise das Herunterladen von Remoteheadern abzubrechen, übergeben Sie das flag ABORT_XP_HEADER_OPERATION an **ValidateState**. Übergeben Sie FORCE_XP_CONNECT oder FORCE_XP_DISCONNECT, um eine Verbindung mit dem Remoteserver herzustellen oder die Verbindung mit dem Remoteserver zu trennen. Übergeben Sie CONFIG_CHANGED, um den Anbieter neu zu konfigurieren. 
  
Clients, die das Senden oder Empfangen von Nachrichten bei Bedarf implementieren, rufen die [IMAPIStatus::FlushQueues-Methode](imapistatus-flushqueues.md) eines Transportanbieters oder des MAPI-Spoolers auf. Sie können drei Flags an die Methode übergeben: FLUSH_UPLOAD, FLUSH_DOWNLOAD und FLUSH_FORCE. FLUSH_UPLOAD weist den Anbieter oder den MAPI-Spooler an, alle Nachrichten zu senden, die in der Ausgabewarteschlange warten, während FLUSH_DOWNLOAD den Anbieter oder den MAPI-Spooler anweist, eingehende Nachrichten zu empfangen. FLUSH_FORCE können mit einem der anderen Flags festgelegt werden, damit das Statusobjekt die Leerung unabhängig vom Zeitpunkt durchführt. 
  
Erwarten Sie nicht, dass **Sie SettingsDialog** oder [ChangePassword](imapistatus-changepassword.md) für eines der MAPI-Subsysteme, MAPI-Spooler oder Adressbuchstatusobjekte aufrufen können. Sowohl die Subsystem- als auch die Adressbuchstatusobjekte unterstützen nur **ValidateState;** Das MAPI-Spoolerstatusobjekt unterstützt **flushQueues** zusätzlich zu **ValidateState**.
  
## <a name="see-also"></a>Siehe auch



[Statustabellen](status-tables.md)
  
[MAPI-Statusobjekte](mapi-status-objects.md)

