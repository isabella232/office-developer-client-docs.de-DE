---
title: Implementierung der Status-Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392403"
---
# <a name="status-object-implementation"></a>Implementierung der Status-Objekts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle-Dienstanbieter müssen ein Statusobjekt implementieren und übermitteln Sie Eigenschaften aus der Sitzung Status-Tabelle. Sie können eine oder mehrere Zeilen in der Statustabelle, abhängig von der Anzahl der Ressourcen einschließen, die Sie steuern. Ein Transportdienstes sollte beispielsweise eine Zeile in der Statustabelle "für jeden Nachrichtenwarteschlange erstellen, die er verwaltet. Wenn Änderungen auftreten, muss die Tabellenzeile geeigneten Status aktualisiert werden. Status-Objekte werden implementiert, um Zugriff auf Informationen in der Tabelle "Status" sowie zu weiteren Informationen, die nicht in der Tabelle enthalten zu ermöglichen.
  
### <a name="to-implement-a-status-object"></a>Implementieren Sie ein Statusobjekt

1. Implementieren Sie die Methode **OpenStatusEntry** Ihrer Anmeldung-Objekts. Wenn Clients Ihr Statusobjekt öffnen möchten, rufen sie [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI erfüllt die Anforderung open durch Aufrufen des Anbieters **OpenStatusEntry** -Methode, verursacht die Anbieter für dessen Statusobjekt öffnen und einen Zeiger auf seine Implementierung **IMAPIStatus** an den Client zurückgegeben. Führen Sie in der Implementierung **OpenStatusEntry** die folgenden Schritte aus: 
    
   1. Führen Sie die folgenden Aufgaben aus, wenn Ihr Anmeldeobjekt ein Statusobjekt noch nicht erstellt wurde:
    
      1. Rufen Sie die des Unterstützungsobjekts [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) -Methode zum Ihres Anbieters Profilabschnitt zuzugreifen. 
          
      2. Erstellen eines neuen Status-Objekts.
          
      3. Speichern Sie einen Verweis auf das Profilabschnitt in Ihres Anbieters Status-Objekt, und rufen Sie Profilabschnitt [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode, um erhöht den Referenzzähler. 
          
      4. Speichern Sie einen Verweis auf das Anmeldeobjekt in Ihres Anbieters Status-Objekt, und rufen Sie das Anmeldeobjekt **IUnknown:: AddRef** -Methode, um den Referenzzähler zu erhöhen. 
          
      5. Speichern Sie einen Verweis auf die Statusobjekt im Ihres Anbieters Anmeldung-Objekt.
    
   2. Rufen Sie den Status des Objekts **IUnknown:: AddRef** -Methode, um seine Referenzzähler in das Anmeldeobjekt zu erhöhen. 
    
   3. Legen Sie den Status des Objekts **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))-Eigenschaft auf MAPI_STATUS.
    
   4. Zeigen Sie auf das Statusobjekt und Zurückgeben der _LppMAPIStatus_ Output-Parameter festgelegt. 
    
   5. Überprüfen der _UlFlags_ input-Parameter. Wenn sie auf MAPI_MODIFY festgelegt ist und vom Anbieter Lese-/Schreibzugriff auf die Statusobjekt unterstützt, zurückgeben Sie ein beschreibbaren Objekt. Wenn jedoch Ihres Anbieters Lese-/Schreibzugriff auf die Statusobjekt nicht unterstützt, führen Sie nicht fehl. Zurückgeben einer Statusobjekt, das schreibgeschützt ist. Clients, die Objekte für Lese-Schreib-Status empfangen erwarten sollten überprüfen, ob Lese-/Schreibberechtigung gewährt wurde, bevor Sie versuchen, Änderungen vorgenommen werden können. 
    
2. Legen Sie alle erforderlichen Status-Objekt und den Status Tabelleneigenschaften. Die Eigenschaften, die Sie in Ihrem Status Tabellenzeile enthalten sollte über Ihr Statusobjekt, mit Ausnahme von MAPI berechneten Eigenschaften verfügbar sein. Die erforderlichen Eigenschaften sind wie folgt:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implementieren der [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) Methoden, die für den Anbieter geeignet sind. Je nach Ihren Anbieter müssen Sie nicht alle vier Methoden in **IMAPIStatus**implementieren. Jeder Anbieter sollte eine schreibgeschützte Version der Methoden des Implementieren der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und die [IMAPIStatus::ValidateState](imapistatus-validatestate.md) -Methode. 

   Transportanbieter sollten auch [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)implementieren, und alle Anbieter sollten [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)unterstützen. Unterstützung für [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) optional ist jedoch. Diese Methode implementieren, müssen nur Dienstanbieter, die Kennwörter erfordern und Benutzern ermöglichen, diese programmgesteuert ändern möchten. Legen Sie für jede Methode, die Sie unterstützen das entsprechende Bit in der **PR_RESOURCE_METHODS** -Eigenschaft. Wenn Sie **ValidateState** und **SettingsDialog** nur unterstützt, legen Sie **PR_RESOURCE_METHODS** wie folgt fest: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Clients sollte den Wert der **PR_RESOURCE_METHODS** überprüfen, bevor Sie versuchen, das Statusobjekt aufrufen. Behandeln Sie Anrufe an Ihre nicht unterstützte Methoden, indem Sie MAPI_E_NO_SUPPORT zurückgeben. 
    
4. Rufen Sie [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) während der Anmeldung an Ihre Zeile oder Zeilen der Tabelle "Status" hinzuzufügen. Übergeben Sie eine Eigenschaft Wertearray, das die Spalteninformationen für die Zeile und 0 für den Parameter _UlFlags_ enthält. Wenn zu einem bestimmten Zeitpunkt später in der Sitzung des Anbieters ändert sich, und es ist erforderlich, um die Spalte zu aktualisieren, rufen Sie **ModifyStatusRow** mit der STATUSROW_UPDATE-Flag. 
    
Weitere Informationen zu Status-Objekten finden Sie unter [MAPI-Status-Objekten](mapi-status-objects.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieter](mapi-service-providers.md)

