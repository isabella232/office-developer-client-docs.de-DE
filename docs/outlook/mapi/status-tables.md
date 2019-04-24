---
title: Status Tabellen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336463"
---
# <a name="status-tables"></a>Status Tabellen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Die Status-Tabelle enthält Informationen zum Status der aktuellen Sitzung. Es gibt eine Statustabelle für jede MAPI-Sitzung mit Informationen, die von MAPI und von Dienstanbietern bereitgestellt werden. MAPI stellt Daten für drei Zeilen bereit: eine Zeile für das MAPI-Subsystem, eine Zeile für den MAPI-Spooler und eine Zeile für das integrierte Adressbuch. Da Transportanbieter zur Bereitstellung von Statusinformationen für die Statustabelle erforderlich sind, gibt es eine Zeile für jeden aktiven Transportanbieter. Adressbuch-und Nachrichtenspeicher Anbieter können auswählen, ob die Statustabelle unterstützt werden soll. 
  
Da jede Zeile von einer anderen Ressource bereitgestellt wird, kann die Gruppe von Spalten von Zeile zu Zeile variieren. Es gibt eine Reihe von Spalten, die jedes Statusobjekt benötigt, und eine Reihe von Spalten, die von MAPI bereitgestellt werden. Ein Dienstanbieter kann diesen Gruppen hinzufügen, um anbieterspezifische Eigenschaften verfügbar zu machen. Beispielsweise können Nachrichtenspeicher Anbieter **PR_STORE_RECORD_KEY** ([pidtagstorerecordkey (](pidtagstorerecordkey-canonical-property.md)) hinzufügen, um Clients den Bezeichner des Nachrichtenspeichers zur Verfügung zu stellen. Clients müssen vorab über das vorhanden sein dieser zusätzlichen Informationen informiert sein, damit Sie diese verwenden können. 
  
In der folgenden Tabelle sind die Eigenschaften aufgeführt, die in jeder Statustabellen Zeile angegeben werden müssen. Die Implementierung des Status-Objekts stellt einige der Eigenschaften bereit; andere werden von MAPI berechnet.
  
|**Vom Status-Objekt bereitgestellte Eigenschaften**|**Von MAPI bereitgestellte Eigenschaften**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([Pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([Pidtagstatuscode (](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([Pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))  <br/> |
   
Wenn das Status-Objekt eine Identität bereitstellt, sollte es **PR_IDENTITY_DISPLAY** ([Pidtagidentitydisplay (](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([pidtagidentityentryid (](pidtagidentityentryid-canonical-property.md)) und **PR_IDENTITY_SEARCH_KEY** ([ Pidtagidentitysearchkey (](pidtagidentitysearchkey-canonical-property.md)), und fügen Sie diese Eigenschaften in die Tabelle ein. 
  
Vier Eigenschaften werden von MAPI für jede Statustabellen Zeile berechnet:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([Pidtaginstancekey (](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([Pidtagobjecttype (](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([Pidtagrowid (](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI weist der Statuszeile eine Eintrags-ID zu, damit Clients das entsprechende Statusobjekt öffnen können. Außerdem wird ein Zeilenbezeichner zugewiesen, um die Zeile in der Tabelle zu identifizieren, ebenso wie ein Instanzschlüssel, um die Daten im Status-Objekt zu identifizieren. Die **PR_OBJECT_TYPE** -Eigenschaft ist auf MAPI_STATUS festgelegt. 
  
Um auf die Statustabelle zuzugreifen, rufen die Clients die [IMAPISession::](imapisession-getstatustable.md) getstatusable-Methode auf. Dieser Aufruf sollte nicht sofort nach dem Start vorgenommen werden. Der Grund dafür **** ist, dass getstatusable auf den MAPI-Spooler warten muss, um die Transportanbieter zu initialisieren, eine Operation, die verschoben wird, bis der Client die Anmeldung beendet hat. **** Getstatusable ist ein relativ schneller Aufruf, nachdem der MAPI-Spooler seine Start Verarbeitung abgeschlossen hat. 
  
Statustabellen Informationen können auf unterschiedliche Weise verwendet werden, beispielsweise für den Zugriff auf ein Statusobjekt, um zu bestimmen, ob ein Client in einem verbundenen oder Offlinemodus ausgeführt wird, und um den Status eines Anbieters zu überwachen. Clients können beispielsweise das Status-Objekt eines bestimmten Dienstanbieters öffnen, indem Sie den Wert der **PR_ENTRYID** -Eigenschaft an die [IMAPISession:: OpenEntry](imapisession-openentry.md) -Methode übergeben. Das Status-Objekt unterstützt die **IMAPIStatus** -Schnittstelle, eine Schnittstelle mit Methoden zum Ändern eines Dienstanbieter Kennworts, zum leeren der Nachrichtenwarteschlange, zum Anzeigen eines Konfigurationseigenschaften Blatts oder zum Bestätigen des Status bei einem Anbieter direkt. Status Tabelleninformationen können auch zum Erstellen eines Dialogfelds verwendet werden, um Clients über den Fortschritt während eines längeren Vorgangs zu informieren. 
  
Dienstanbieter, die die Statustabelle unterstützen, verwenden die [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode, um Ihre Zeile zu erstellen und zu aktualisieren. Bei jeder Änderung einer Zeile müssen alle Advise-Empfängerobjekte benachrichtigt werden, die für Empfangsstatus-Tabellen Benachrichtigungen registriert sind. Dienstanbieter können die [IMAPISupport:: notify](imapisupport-notify.md) -Methode aufrufen, wenn Sie das MAPI-Benachrichtigungs Dienstprogramm verwenden oder die [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) -Methode der einzelnen Advise-Senke direkt aufrufen. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Tabellen](mapi-tables.md)

