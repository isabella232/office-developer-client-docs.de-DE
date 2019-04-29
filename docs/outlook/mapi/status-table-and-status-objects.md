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
  
MAPI stellt eine Tabelle mit Informationen zum Status des MAPI-Subsystems, des MAPI-Spoolers, des Adressbuchs oder eines bestimmten Dienstanbieters bereit. Sie können auf diese Tabelle zugreifen, indem Sie [IMAPISession::](imapisession-getstatustable.md)getstatusable aufrufen.
  
Jede Zeile in der Statustabelle stellt ein Statusobjekt dar, das von MAPI oder einem Dienstanbieter implementiert wurde. Sie können ein Status-Objekt verwenden, um das Konfigurationseigenschaften Fenster eines Anbieters anzuzeigen, ein Anbieter Kennwort zu ändern, Nachrichten hochzuladen oder herunterzuladen und mit einem bestimmten Transportanbieter zu kommunizieren. 
  
Es gibt zwei Möglichkeiten, auf ein Status-Objekt zuzugreifen:
  
- Über die Statustabelle
    
- Über die **OpenStatusEntry** -Methode eines LOGON-Objekts 
    
Da Anmeldeobjekte für Clients nicht verfügbar sind, müssen Sie die Status-Tabelle verwenden, um auf Statusobjekte zuzugreifen. Der Statustabellen Ansatz ist indirekt, erfordert ein paar Aufrufe, bevor das Status-Objekt geöffnet wird und ein Zeiger auf die **IMAPIStatus** -Implementierung zurückgegeben. 
  
 **So öffnen Sie ein Statusobjekt mithilfe der Status-Tabelle**
  
1. Rufen Sie **IMAPIStatus::** getstatusable auf, um einen [IMAPITable](imapitableiunknown.md) -Zeiger abzurufen. 
    
2. Rufen Sie die [IMAPITable::](imapitable-setcolumns.md) SetColumns-Methode der Statustabelle auf, um den Spaltensatz auf **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([pidtagresourcetype (](pidtagresourcetype-canonical-property.md)) und **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Schränkt die Tabellenansicht auf ein bestimmtes Statusobjekt ein. Bei MAPI-Implementierungen kann ein Client mithilfe von **PR_RESOURCE_TYPE**eine Eigenschaftseinschränkung definieren. Bei Implementierungen von Dienstanbietern kann ein Client die **PR_PROVIDER_DISPLAY** ([pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md)), den Namen des Anbieters oder **PR_PROVIDER_DLL_NAME** ([pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md)), den Namen der Anbieter-DLL einschränken. Datei.
    
4. Rufen Sie [IMAPITable:: Restrict](imapitable-restrict.md) auf, um die Einschränkung festzulegen. 
    
5. Rufen Sie [HrQueryAllRows](hrqueryallrows.md)auf, und übergeben Sie die [SPropertyRestriction](spropertyrestriction.md) -Struktur, um die Zeile abzurufen, die den Status des Anbieters darstellt. 
    
6. Rufen Sie [IMAPISession:: OpenEntry](imapisession-openentry.md)auf, indem Sie die Eintrags-ID aus der Zeile der Statustabelle angeben, um das Status-Objekt zu öffnen und einen **IMAPIStatus** -Zeiger abzurufen. 
    
Zum Anzeigen eines Eigenschaftenblatts rufen Sie die [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode des Status-Objekts für den Zielanbieter auf. **Settingsdialog** zeigt ein Eigenschaftenfenster zum Anzeigen und in einigen Fällen die Konfigurationseigenschaften eines Anbieters an. 
  
Wenn Sie mit einem Transportanbieter kommunizieren möchten, rufen Sie die [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode des Status-Objekts auf. **ValidateState** kann einen Transportanbieter neu konfigurieren, den Anbieter daran hindern, eine Benutzeroberfläche anzuzeigen und eine Sitzung zu steuern, die das Herunterladen von Nachrichtenkopfzeilen von einem Remoteserver abhängig von den übertragenen Kennzeichen umfasst. Wenn Sie beispielsweise das Herunterladen von Remoteheadern abbrechen möchten, müssen Sie das ABORT_XP_HEADER_OPERATION-Flag an **ValidateState**. Zum Verbinden oder Trennen vom Remoteserver führen Sie FORCE_XP_CONNECT oder FORCE_XP_DISCONNECT. Um den Anbieter neu zu konfigurieren, führen Sie CONFIG_CHANGED. 
  
Clients, die das Senden oder empfangen von Nachrichten bei Bedarf implementieren, rufen entweder die [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) -Methode eines Transportanbieters oder eines MAPI-Spoolers auf. Sie können drei Flags an die-Methode weiterleiten: FLUSH_UPLOAD, FLUSH_DOWNLOAD und FLUSH_FORCE. FLUSH_UPLOAD weist den Anbieter oder die MAPI-Warteschlange an, alle Nachrichten zu senden, die in der Ausgabewarteschlange warten, während FLUSH_DOWNLOAD den Anbieter oder den MAPI-Spooler anweist, eingehende Nachrichten zu empfangen. FLUSH_FORCE kann mit einem der anderen Flags festgelegt werden, damit das Status-Objekt den Flush unabhängig vom Timing ausführt. 
  
Erwarten Sie nicht, dass Sie **Settingsdialog** oder [CHANGEPASSWORD](imapistatus-changepassword.md) für ein MAPI-Subsystem, MAPI-Spooler oder Adressbuch Status-Objekte aufrufen können. Sowohl das Subsystem als auch das Adressbuch-Statusobjekt unterstützen nur **ValidateState**; das MAPI-Spooler Status-Objekt unterstützt **FlushQueues** zusätzlich zu **ValidateState**.
  
## <a name="see-also"></a>Siehe auch



[Status Tabellen](status-tables.md)
  
[MAPI-Status Objekte](mapi-status-objects.md)

