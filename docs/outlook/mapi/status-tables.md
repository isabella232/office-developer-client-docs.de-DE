---
title: Statustabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a3bb89cb54dafe6c3f82f4633c15ed4e67751448
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591066"
---
# <a name="status-tables"></a>Statustabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Statustabelle enthält Informationen zum Status der aktuellen Sitzung. Es gibt eine Statustabelle für jede MAPI-Sitzung, die Informationen enthält, die von der MAPI und von Dienstanbietern bereitgestellt werden. MAPI stellt Daten für drei Zeilen bereit: eine Zeile für das MAPI-Subsystem, eine Zeile für den MAPI-Spooler und eine Zeile für das integrierte Adressbuch. Da Transportanbieter statusinformationen für die Statustabelle angeben müssen, gibt es für jeden aktiven Transportanbieter eine Zeile. Adressbuch- und Nachrichtenspeicheranbieter können auswählen, ob die Statustabelle unterstützt werden soll. 
  
Da jede Zeile von einer anderen Ressource bereitgestellt wird, kann der Satz von Spalten von Zeile zu Zeile variieren. Es gibt eine Reihe von Spalten, die von jedem Statusobjekt bereitgestellt werden müssen, und eine Reihe von Spalten, die mapi bereitstellt. Ein Dienstanbieter kann diesen Gruppen hinzufügen, um anbieterspezifische Eigenschaften verfügbar zu machen. Beispielsweise können Nachrichtenspeicheranbieter **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) hinzufügen, um Clients den Bezeichner ihres Nachrichtenspeichers zu liefern. Clients müssen im Voraus wissen, dass diese zusätzlichen Informationen vorhanden sind, um sie verwenden zu können. 
  
In der folgenden Tabelle sind die Eigenschaften aufgeführt, die sich in jeder Statustabellenzeile befinden müssen. Der Implementierer des Statusobjekts stellt einige der Eigenschaften bereit. andere werden von mapi berechnet.
  
|**Vom Statusobjekt bereitgestellte Eigenschaften**|**Von MAPI bereitgestellte Eigenschaften**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Wenn das Statusobjekt eine Identität bereitstellt, sollte es **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) und **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) festlegen und diese Eigenschaften in die Tabelle einschließen. 
  
Vier Eigenschaften werden von der MAPI für jede Statustabellenzeile berechnet:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI weist der Statuszeile einen Eintragsbezeichner zu, damit Clients das entsprechende Statusobjekt öffnen können. Ein Zeilenbezeichner wird auch zugewiesen, um die Zeile in der Tabelle zu identifizieren, ebenso wie ein Instanzschlüssel, um die Daten im Statusobjekt zu identifizieren. Die **PR_OBJECT_TYPE-Eigenschaft** ist auf MAPI_STATUS festgelegt. 
  
Um auf die Statustabelle zuzugreifen, rufen Clients die [IMAPISession::GetStatusTable-Methode](imapisession-getstatustable.md) auf. Dieser Aufruf sollte nicht sofort beim Start erfolgen. Dies liegt daran, dass **GetStatusTable** warten muss, bis der MAPI-Spooler die Transportanbieter initialisiert. Dies ist ein Vorgang, der verschoben wird, bis der Client seine Anmeldung abgeschlossen hat. **GetStatusTable** ist ein relativ schneller Aufruf, nachdem der MAPI-Spooler die Startverarbeitung abgeschlossen hat. 
  
Statustabelleninformationen können auf verschiedene Arten verwendet werden, z. B. um auf ein Statusobjekt zuzugreifen, um zu bestimmen, ob ein Client im verbundenen oder Offlinemodus ausgeführt wird, und um den Status eines Anbieters zu überwachen. Clients können z. B. das Statusobjekt eines bestimmten Dienstanbieters öffnen, indem sie den Wert der **PR_ENTRYID-Eigenschaft** an die [IMAPISession::OpenEntry-Methode](imapisession-openentry.md) übergeben. Das Statusobjekt unterstützt die **IMAPIStatus-Schnittstelle,** eine Schnittstelle, die Methoden zum Ändern eines Dienstanbieterkennworts, zum Leeren der Nachrichtenwarteschlange, zum Anzeigen eines Konfigurationseigenschaftenblatts oder zum direkten Bestätigen des Status bei einem Anbieter enthält. Statustabelleninformationen können auch zum Erstellen eines Dialogfelds verwendet werden, um Clients während eines längeren Vorgangs über den Fortschritt zu informieren. 
  
Dienstanbieter, die die Statustabelle unterstützen, verwenden die [IMAPISupport::ModifyStatusRow-Methode,](imapisupport-modifystatusrow.md) um ihre Zeile zu erstellen und zu aktualisieren. Wenn eine Änderung an der Zeile vorgenommen wird, müssen alle zum Empfangen von Statustabellenbenachrichtigungen registrierten Senkenobjekte benachrichtigt werden. Dienstanbieter können die [IMAPISupport::Notify-Methode](imapisupport-notify.md) aufrufen, wenn sie das MAPI-Benachrichtigungsprogramm verwenden oder die [IMAPIAdviseSink::OnNotify-Methode](imapiadvisesink-onnotify.md) jeder Empfehlungssenke direkt aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

