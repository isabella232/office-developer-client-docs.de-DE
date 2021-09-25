---
title: Implementierung von Statusobjekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e8ae261ff88d99594badc314fdac731257360d7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624139"
---
# <a name="status-object-implementation"></a>Implementierung von Statusobjekten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Dienstanbieter müssen ein Statusobjekt implementieren und eigenschaften daraus in die Sitzungsstatustabelle integrieren. Sie können eine oder mehrere Zeilen in die Statustabelle aufnehmen, abhängig von der Anzahl der ressourcen, die Sie steuern. Ein Transportanbieter sollte beispielsweise eine Zeile in der Statustabelle für jede von ihm verwalteten Nachrichtenwarteschlange erstellen. Wenn Änderungen auftreten, muss die entsprechende Statustabellenzeile aktualisiert werden. Statusobjekte werden implementiert, um sowohl auf die in der Statustabelle enthaltenen Informationen als auch auf zusätzliche Informationen zuzugreifen, die nicht in der Tabelle enthalten sind.
  
### <a name="to-implement-a-status-object"></a>So implementieren Sie ein Statusobjekt

1. Implementieren Sie die **OpenStatusEntry-Methode** des Anmeldeobjekts. Wenn Clients Ihr Statusobjekt öffnen möchten, rufen sie [IMAPISession::OpenEntry](imapisession-openentry.md)auf. MAPI erfüllt die Open-Anforderung, indem sie die **OpenStatusEntry-Methode** Ihres Anbieters aufruft, wodurch ihr Anbieter sein Statusobjekt öffnet und einen Zeiger auf die **IMAPIStatus-Implementierung** an den Client zurückgibt. Führen Sie in Der **OpenStatusEntry-Implementierung** die folgenden Schritte aus: 
    
   1. Führen Sie die folgenden Aufgaben aus, wenn ihr Anmeldeobjekt noch kein Statusobjekt erstellt hat:
    
      1. Rufen Sie die [IMAPISupport::OpenProfileSection-Methode](imapisupport-openprofilesection.md) des Supportobjekts auf, um auf den Profilabschnitt Ihres Anbieters zuzugreifen. 
          
      2. Erstellen sie ein neues Statusobjekt.
          
      3. Store einen Verweis auf den Profilabschnitt im Statusobjekt Ihres Anbieters, und rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) des Profilabschnitts auf, um die Referenzanzahl zu erhöhen. 
          
      4. Store einen Verweis auf das Anmeldeobjekt im Statusobjekt Ihres Anbieters ein, und rufen Sie die **IUnknown::AddRef-Methode** des Anmeldeobjekts auf, um die Referenzanzahl zu erhöhen. 
          
      5. Store einen Verweis auf das Statusobjekt im Anmeldeobjekt Des Anbieters.
    
   2. Rufen Sie die **IUnknown::AddRef-Methode** des Statusobjekts auf, um die Referenzanzahl im Anmeldeobjekt zu erhöhen. 
    
   3. Legen Sie die **eigenschaft PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) des Statusobjekts auf MAPI_STATUS fest.
    
   4. Legen Sie den  _lppMAPIStatus-Ausgabeparameter_ so fest, dass er auf das Statusobjekt verweist, und geben Sie es zurück. 
    
   5. Überprüfen Sie den _ulFlags-Eingabeparameter._ Wenn sie auf MAPI_MODIFY festgelegt ist und Ihr Anbieter Lese-/Schreibzugriff auf das Statusobjekt unterstützt, geben Sie ein schreibbares Objekt zurück. Wenn Ihr Anbieter jedoch keinen Lese-/Schreibzugriff auf sein Statusobjekt unterstützt, tritt kein Fehler auf. Gibt ein schreibgeschütztes Statusobjekt zurück. Clients, die Lese-/Schreibstatusobjekte erwarten, sollten überprüfen, ob Lese-/Schreibberechtigungen erteilt wurden, bevor Sie versuchen, Änderungen vorzunehmen. 
    
2. Legen Sie alle erforderlichen Statusobjekt- und Statustabelleneigenschaften fest. Die Eigenschaften, die Sie in die Statustabellenzeile einschließen, sollten über das Statusobjekt verfügbar sein, mit Ausnahme der von MAPI berechneten Eigenschaften. Die erforderlichen Eigenschaften sind wie folgt:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implementieren Sie die [IMAPIStatus : IMAPIProp-Methoden,](imapistatusimapiprop.md) die für Ihren Anbieter geeignet sind. Je nach Anbieter müssen Sie nicht alle vier Methoden in **IMAPIStatus** implementieren. Jeder Anbieter sollte eine schreibgeschützte Version der Methoden der [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) und der [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) implementieren. 

   Transportanbieter sollten auch [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)implementieren, und alle Anbieter sollten [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)unterstützen. Die Unterstützung für [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) ist jedoch optional. Nur Dienstanbieter, die Kennwörter benötigen und benutzern das programmgesteuerte Ändern gestatten möchten, müssen diese Methode implementieren. Legen Sie für jede unterstützte Methode das entsprechende Bit in der **PR_RESOURCE_METHODS-Eigenschaft** fest. Wenn Sie beispielsweise **"ValidateState"** und **"SettingsDialog"** nur unterstützen, legen **Sie PR_RESOURCE_METHODS** auf Folgendes fest: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Clients sollten den Wert von **PR_RESOURCE_METHODS** überprüfen, bevor sie versuchen, das Statusobjekt aufzurufen. Behandeln Sie Aufrufe einer der nicht unterstützten Methoden, indem Sie MAPI_E_NO_SUPPORT zurückgeben. 
    
4. Rufen Sie [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) während der Anmeldung auf, um Ihre Zeile oder Zeilen zur Statustabelle hinzuzufügen. Übergeben Sie ein Eigenschaftenwertarray, das die Spalteninformationen für die Zeile enthält, und 0 für den _ulFlags-Parameter._ Wenn sich der Status Ihres Anbieters zu einem späteren Zeitpunkt in der Sitzung ändert und es erforderlich wird, die Spalteninformationen zu aktualisieren, rufen **Sie ModifyStatusRow** erneut auf, wobei das STATUSROW_UPDATE Flag festgelegt ist. 
    
Weitere Informationen zu Statusobjekten finden Sie unter [MAPI Status Objects](mapi-status-objects.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieter](mapi-service-providers.md)

