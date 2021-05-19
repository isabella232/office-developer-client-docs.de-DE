---
title: Implementierung von Statusobjekten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336337"
---
# <a name="status-object-implementation"></a>Implementierung von Statusobjekten

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle Dienstanbieter müssen ein Statusobjekt implementieren und Eigenschaften davon in die Sitzungsstatustabelle einf?nnen. Sie können je nach anzahl der von Ihnen kontrollierten Ressourcen eine oder mehrere Zeilen in die Statustabelle einfügen. Ein Transportanbieter sollte beispielsweise eine Zeile in der Statustabelle für jede verwaltete Nachrichtenwarteschlange erstellen. Wenn Änderungen auftreten, muss die entsprechende Statustabelle aktualisiert werden. Status-Objekte werden implementiert, um sowohl Zugriff auf die in der Statustabelle enthaltenen Informationen als auch auf zusätzliche Informationen zu ermöglichen, die nicht in der Tabelle enthalten sind.
  
### <a name="to-implement-a-status-object"></a>So implementieren Sie ein Statusobjekt

1. Implementieren Sie **die OpenStatusEntry-Methode** des Anmeldeobjekts. Wenn Clients Ihr Statusobjekt öffnen möchten, rufen sie [IMAPISession::OpenEntry auf.](imapisession-openentry.md) MAPI erfüllt die offene Anforderung, indem sie die **OpenStatusEntry-Methode** Ihres Anbieters aufruft, wodurch Ihr Anbieter sein Statusobjekt öffnet und an den Client einen Zeiger auf die **IMAPIStatus-Implementierung** zurücksenken kann. Führen Sie **in Ihrer OpenStatusEntry-Implementierung** die folgenden Schritte aus: 
    
   1. Führen Sie die folgenden Aufgaben aus, wenn das Anmeldeobjekt noch kein Statusobjekt erstellt hat:
    
      1. Rufen Sie die [IMAPISupport::OpenProfileSection-Methode des Supportobjekts](imapisupport-openprofilesection.md) auf, um auf den Profilabschnitt Ihres Anbieters zu zugreifen. 
          
      2. Erstellen Sie ein neues Statusobjekt.
          
      3. Store einen Verweis auf den Profilabschnitt im Statusobjekt Ihres Anbieters und rufen Sie die [IUnknown::AddRef-Methode](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) des Profilabschnitts auf, um die Referenzanzahl zu erhöhen. 
          
      4. Store einen Verweis auf das Anmeldeobjekt im Statusobjekt Ihres Anbieters und rufen Sie die **IUnknown::AddRef-Methode** des Anmeldeobjekts auf, um die Referenzanzahl zu erhöhen. 
          
      5. Store einen Verweis auf das Statusobjekt im Anmeldeobjekt Ihres Anbieters.
    
   2. Rufen Sie die **IUnknown::AddRef-Methode** des Statusobjekts auf, um die Referenzanzahl im Anmeldeobjekt zu erhöhen. 
    
   3. Legen Sie die eigenschaft **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) des Statusobjekts auf MAPI_STATUS.
    
   4. Legen Sie  _den Ausgabeparameter lppMAPIStatus_ so ein, dass er auf das Statusobjekt verweisen soll, und geben Sie zurück. 
    
   5. Überprüfen Sie den _ulFlags-Eingabeparameter._ Wenn sie auf "MAPI_MODIFY" festgelegt ist und Ihr Anbieter Lese-/Schreibzugriff auf das Statusobjekt unterstützt, geben Sie ein schreibbares Objekt zurück. Wenn Ihr Anbieter jedoch keinen Lese-/Schreibzugriff auf sein Statusobjekt unterstützt, führen Sie keinen Fehler aus. Gibt ein schreibgeschütztes Statusobjekt zurück. Clients, die erwarten, dass Statusobjekte mit Lese-/Schreibzugriff empfangen werden, sollten überprüfen, ob Lese-/Schreibberechtigungen erteilt wurden, bevor sie versuchen, Änderungen vorzunehmen. 
    
2. Legen Sie alle erforderlichen Statusobjekt- und Statustabelle-Eigenschaften. Die Eigenschaften, die Sie in der Zeile statustabelle enthalten, sollten über das Statusobjekt verfügbar sein, mit Ausnahme der von MAPI berechneten Eigenschaften. Die erforderlichen Eigenschaften sind wie folgt:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implementieren Sie [die IMAPIStatus : IMAPIProp-Methoden,](imapistatusimapiprop.md) die für Ihren Anbieter geeignet sind. Je nach Anbieter müssen Sie nicht alle vier Methoden in **IMAPIStatus implementieren.** Jeder Anbieter sollte eine schreibgeschützte Version der Methoden der [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) und der [IMAPIStatus::ValidateState-Methode](imapistatus-validatestate.md) implementieren. 

   Transportanbieter sollten auch [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)implementieren, und alle Anbieter sollten [IMAPIStatus::SettingsDialog unterstützen.](imapistatus-settingsdialog.md) Die Unterstützung für [IMAPIStatus::ChangePassword](imapistatus-changepassword.md) ist jedoch optional. Diese Methode muss nur von Dienstanbietern implementiert werden, die Kennwörter benötigen und Benutzern die programmgesteuerte Änderung ermöglichen möchten. Legen Sie für jede von Ihnen unterstützten Methode das entsprechende Bit in der PR_RESOURCE_METHODS **fest.** Wenn Sie beispielsweise nur **ValidateState** und **SettingsDialog** unterstützen, legen **PR_RESOURCE_METHODS** wie folgt vor: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Clients sollten den Wert der **PR_RESOURCE_METHODS,** bevor sie versuchen, das Statusobjekt auf aufruft. Behandeln Sie Aufrufe von nicht unterstützten Methoden, indem Sie MAPI_E_NO_SUPPORT. 
    
4. Rufen [Sie IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) während der Anmeldung auf, um ihre Zeile oder Zeilen zur Statustabelle hinzuzufügen. Übergeben Sie ein Eigenschaftenwertarray, das die Spalteninformationen für die Zeile und 0 für den  _ulFlags-Parameter_ enthält. Wenn sich zu einem späteren Zeitpunkt in der Sitzung der Status Ihres Anbieters ändert und es erforderlich wird, die Spalteninformationen zu aktualisieren, rufen Sie **ModifyStatusRow** erneut mit dem STATUSROW_UPDATE auf. 
    
Weitere Informationen zu Statusobjekten finden Sie unter [MAPI Status Objects](mapi-status-objects.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieter](mapi-service-providers.md)

