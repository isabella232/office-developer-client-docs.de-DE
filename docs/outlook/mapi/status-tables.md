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
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422362"
---
# <a name="status-tables"></a>Statustabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Statustabelle enthält Informationen zum Status der aktuellen Sitzung. Es gibt eine Statustabelle für jede MAPI-Sitzung, die Informationen enthält, die von MAPI und von Dienstanbietern bereitgestellt werden. MAPI bietet Daten für drei Zeilen: eine Zeile für das MAPI-Subsystem, eine Zeile für den MAPI-Spooler und eine Zeile für das integrierte Adressbuch. Da Transportanbieter statusinformationen für die Statustabelle liefern müssen, gibt es für jeden aktiven Transportanbieter eine Zeile. Adressbuch- und Nachrichtenspeicheranbieter können auswählen, ob die Statustabelle unterstützt werden soll. 
  
Da jede Zeile von einer anderen Ressource bereitgestellt wird, kann der Satz von Spalten von Zeile zu Zeile variieren. Es gibt eine Reihe von Spalten, die für jedes Statusobjekt erforderlich sind, und eine Reihe von Spalten, die MAPI liefert. Ein Dienstanbieter kann diese Sätze hinzufügen, um anbieterspezifische Eigenschaften verfügbar zu machen. Nachrichtenspeicheranbieter können z. B. PR_STORE_RECORD_KEY **(** [PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) hinzufügen, um Clients den Bezeichner ihres Nachrichtenspeichers zur Verfügung zu stellen. Clients müssen vorab über das Vorhandensein dieser zusätzlichen Informationen informiert sein, um sie verwenden zu können. 
  
In der folgenden Tabelle sind die Eigenschaften aufgeführt, die in jeder Statustabelle enthalten sein müssen. Der Implementier des status-Objekts stellt einige der Eigenschaften zur. andere werden von MAPI berechnet.
  
|**Vom Statusobjekt bereitgestellte Eigenschaften**|**Von MAPI bereitgestellte Eigenschaften**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Wenn das status-Objekt eine Identität enthält, sollte es **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) und **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) festlegen und diese Eigenschaften in die Tabelle enthalten. 
  
Vier Eigenschaften werden von MAPI für jede Statustabelle berechnet:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI weist der Statuszeile einen Eintragsbezeichner zu, damit Clients das entsprechende Statusobjekt öffnen können. Ein Zeilenbezeichner wird auch zugewiesen, um die Zeile in der Tabelle zu identifizieren, da es sich um einen Instanzschlüssel zum Identifizieren der Daten im Statusobjekt handelt. Die **PR_OBJECT_TYPE-Eigenschaft** ist auf MAPI_STATUS. 
  
Um auf die Statustabelle zu zugreifen, rufen Clients die [IMAPISession::GetStatusTable-Methode](imapisession-getstatustable.md) auf. Dieser Aufruf sollte nicht sofort nach dem Start erfolgt sein. Dies liegt **daran, dass GetStatusTable** warten muss, bis der MAPI-Spooler die Transportanbieter initialisiert, ein Vorgang, der bis nach abschluss der Clientanmeldung verschoben wird. **GetStatusTable** ist ein relativ schneller Aufruf, nachdem der MAPI-Spooler die Startverarbeitung abgeschlossen hat. 
  
Statustabelleinformationen können auf unterschiedliche Weise verwendet werden, z. B. um auf ein Statusobjekt zu zugreifen, um zu bestimmen, ob ein Client in einem verbundenen oder offline-Modus ausgeführt wird, und um den Status eines Anbieters zu überwachen. Clients können beispielsweise das Statusobjekt eines bestimmten Dienstanbieters öffnen, indem der Wert der **PR_ENTRYID-Eigenschaft** an die [IMAPISession::OpenEntry-Methode übergeben](imapisession-openentry.md) wird. Das Status-Objekt unterstützt die **IMAPIStatus-Schnittstelle,** eine Schnittstelle, die Methoden zum Ändern eines Dienstanbieterkennworts, Leeren der Nachrichtenwarteschlange, Anzeigen eines Konfigurationseigenschaftsblatts oder Zum Bestätigen des Status bei einem Anbieter direkt enthält. Statustabelle-Informationen können auch zum Erstellen eines Dialogfelds verwendet werden, um Clients während eines langwierigen Vorgangs über den Fortschritt zu informieren. 
  
Dienstanbieter, die die Statustabelle unterstützen, verwenden die [IMAPISupport::ModifyStatusRow-Methode,](imapisupport-modifystatusrow.md) um ihre Zeile zu erstellen und zu aktualisieren. Wenn eine Änderung an ihrer Zeile auftritt, müssen alle beratenden Sinkobjekte benachrichtigt werden, die für den Empfang von Statustabelle-Benachrichtigungen registriert sind. Dienstanbieter können die [IMAPISupport::Notify-Methode](imapisupport-notify.md) aufrufen, wenn sie das MAPI-Benachrichtigungs-Hilfsprogramm verwenden, oder die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) jeder Ratgebersenke direkt aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

