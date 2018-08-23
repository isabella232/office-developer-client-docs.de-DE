---
title: Statustabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ee7d729000fbda895918458993437fd4fe72e370
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591611"
---
# <a name="status-tables"></a>Statustabellen

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Statustabelle enthält Informationen, die sich auf den Status der aktuellen Sitzung beziehen. Es wird eine Statustabelle für jede MAPI-Sitzung, die durch MAPI und Dienstanbieter bereitgestellten Informationen enthält. MAPI stellt Daten für drei Zeilen: eine Zeile für das MAPI-Subsystem, eine Zeile für die MAPI-Warteschlange und eine Zeile für die integrierte Adressbuch. Da Transportanbieter Statusinformationen an die Statustabelle bereitstellen erforderlich sind, ist eine Zeile für jedes Adressbuchhierarchie aktiv. Address Book und Message-Anbieter können auswählen, ob die Statustabelle zu unterstützen. 
  
Da jede Zeile durch eine andere Ressource bereitgestellt wird, kann die Gruppe von Spalten von Zeile zu Zeile variieren. Es gibt eine Reihe von Spalten an, denen jedes Statusobjekt bereitstellen erforderlich ist und eine Reihe von Spalten, die MAPI bereitstellt. Diese Sätze anbieterspezifische Eigenschaften verfügbar machen kann ein Dienstanbieter hinzufügen. Beispielsweise könnte Nachricht Anbieter **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) Clients mit der ID des ihren Nachrichtenspeicher angeben hinzufügen. Clients benötigen Advance Kenntnisse über das Vorhandensein diese zusätzlichen Informationen, um es verwenden zu können. 
  
Die folgende Tabelle enthält die Eigenschaften, die in jeder Tabellenzeile Status sein müssen. Die Implementierung des Status-Objekts enthält einige der Eigenschaften; andere Benutzer werden MAPI berechnet.
  
|**Statusobjekt bereitgestellten Eigenschaften**|**MAPI-Eigenschaften**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Wenn das Statusobjekt eine Identität bereitstellt, sollten sie **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) und **PR_IDENTITY_SEARCH_KEY** ([ festgelegt. PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)), und diese Eigenschaften in der Tabelle enthalten. 
  
Vier Eigenschaften werden für jede Tabellenzeile Status MAPI berechnet:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI weist eine Eintrags-ID der Statuszeile damit Clients den entsprechenden Status-Objekts öffnen können. Zeilen-ID wird auch zugewiesen, um die Zeile in der Tabelle zu identifizieren, ist eine Instanz-Taste, um die Daten im Statusobjekt zu identifizieren. Die **PR_OBJECT_TYPE** -Eigenschaft wird auf MAPI_STATUS festgelegt. 
  
Wenn die Statustabelle zugreifen zu können, rufen Clients die [IMAPISession::GetStatusTable](imapisession-getstatustable.md) -Methode. Dieses Anrufs soll nicht unmittelbar nach dem Start erfolgen. Dies ist, da **GetStatusTable** wurde auf die MAPI-Warteschlange zum Initialisieren der Transportanbieter eines Vorgangs gewartet werden soll, die bis verschoben wird, wenn der Client die Anmeldung abgeschlossen hat. **GetStatusTable** ist ein relativ schnelle Aufruf, nachdem die MAPI-Warteschlange die Verarbeitung Start abgeschlossen wurde. 
  
Tabelle Statusinformationen kann in verschiedene Arten, wie ein Statusobjekt, um festzustellen, ob ein Client in einem verbundenen oder offline-Modus ausgeführt wird, und klicken Sie zum Überwachen des Status eines Anbieters Zugriff auf verwendet werden. Beispielsweise können Clients des Dienstanbieters für einen bestimmten Statusobjekt zu öffnen, indem Sie den Wert der Eigenschaft **PR_ENTRYID** an die [IMAPISession::OpenEntry](imapisession-openentry.md) -Methode übergeben. Das Statusobjekt unterstützt die **IMAPIStatus** -Schnittstelle, eine Schnittstelle, die enthält Methoden, um ein Kennwort für das Anbieter zu ändern, die Nachrichtenwarteschlange geleert, Anzeigen eines Eigenschaftenblatts Konfiguration oder Status direkt mit einem Anbieter zu bestätigen. Statusinformationen für die Tabelle kann auch verwendet werden, erstellen Sie ein Dialogfeld, um Clients des Fortschritts während einer langen Operation zu informieren. 
  
Dienstanbieter, die Unterstützung für die Statustabelle verwenden Sie die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode zum Erstellen und aktualisieren Sie ihre Zeile. Bei eine Änderung auf die Zeile, beraten alle Empfängerobjekten Erhalt von Benachrichtigungen der Status-Tabelle registriert benachrichtigt werden müssen. Dienstanbieter können die [IMAPISupport::Notify](imapisupport-notify.md) -Methode aufrufen, wenn sie das MAPI-Notification-Dienstprogramm oder rufen direkt auf jeden Advise-Empfänger [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) -Methode. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

