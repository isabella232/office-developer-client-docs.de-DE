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
  
Alle Dienstanbieter müssen ein Status-Objekt implementieren und dessen Eigenschaften in die Tabelle Sitzungsstatus einteilen. Sie können je nach Anzahl der Ressourcen, die Sie steuern, eine oder mehrere Zeilen in die Statustabelle aufnehmen. Ein Transportanbieter sollte beispielsweise für jede von ihm verwaltete Nachrichtenwarteschlange eine Zeile in der Statustabelle erstellen. Wenn Änderungen auftreten, muss die entsprechende Statustabellen Zeile aktualisiert werden. Statusobjekte werden implementiert, um sowohl auf die in der Statustabelle enthaltenen Informationen als auch auf zusätzliche Informationen, die nicht in der Tabelle enthalten sind, zuzugreifen.
  
### <a name="to-implement-a-status-object"></a>So implementieren Sie ein Statusobjekt

1. Implementieren Sie die **OpenStatusEntry** -Methode des LOGON-Objekts. Wenn Clients Ihr Status-Objekt öffnen möchten, rufen Sie [IMAPISession:: OpenEntry](imapisession-openentry.md)auf. MAPI erfüllt die offene Anforderung durch Aufrufen der **OpenStatusEntry** -Methode Ihres Anbieters, sodass der Anbieter sein Status-Objekt öffnen und zum Client einen Zeiger auf seine **IMAPIStatus** -Implementierung zurückgeben kann. Führen Sie in der **OpenStatusEntry** -Implementierung die folgenden Schritte aus: 
    
   1. Führen Sie die folgenden Aufgaben aus, wenn Ihr Logon-Objekt noch kein Status-Objekt erstellt hat:
    
      1. Rufen Sie die [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) -Methode des Support Objekts auf, um auf den Profilbereich Ihres Anbieters zuzugreifen. 
          
      2. Erstellen Sie ein neues Status-Objekt.
          
      3. Speichern Sie einen Verweis auf den profile-Abschnitt im Status-Objekt Ihres Anbieters, und rufen Sie die [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) -Methode des profile-Abschnitts auf, um den Verweiszähler zu erhöhen. 
          
      4. Speichern Sie einen Verweis auf das Logon-Objekt im Status-Objekt Ihres Anbieters, und rufen Sie die **IUnknown:: AddRef** -Methode des LOGON-Objekts auf, um den Verweiszähler zu erhöhen. 
          
      5. Speichern Sie einen Verweis auf das Status-Objekt im Logon-Objekt Ihres Anbieters.
    
   2. Rufen Sie die **IUnknown:: AddRef** -Methode des Status-Objekts auf, um den Verweiszähler im Logon-Objekt zu erhöhen. 
    
   3. Legen Sie die **PR_OBJECT_TYPE** ([pidtagobjecttype (](pidtagobjecttype-canonical-property.md))-Eigenschaft des Status-Objekts auf MAPI_STATUS.
    
   4. Legen Sie den _lppMAPIStatus_ -Ausgabeparameter so fest, dass er auf das Status-Objekt zeigt, und geben Sie zurück. 
    
   5. Überprüfen Sie den _ulFlags_ -Eingabeparameter. Wenn es auf MAPI_MODIFY festgelegt ist und Ihr Anbieter Lese-/Schreibzugriff auf sein Status-Objekt unterstützt, geben Sie ein beschreibbares Objekt zurück. Wenn Ihr Anbieter jedoch keinen Lese-/Schreibzugriff auf sein Status-Objekt unterstützt, schlagen Sie nicht fehl. Gibt ein schreibgeschütztes Statusobjekt zurück. Clients, die erwarten, dass Sie Lese-/Schreibzugriff auf Statusobjekte erhalten, sollten überprüfen, ob Lese-/Schreibzugriff erteilt wurde, bevor Sie Änderungen vornehmen. 
    
2. Legen Sie alle erforderlichen Status-und Statustabellen Eigenschaften fest. Die Eigenschaften, die Sie in Ihre Statustabellen Zeile aufnehmen, sollten über Ihr Status-Objekt verfügbar sein, mit Ausnahme der von MAPI berechneten Eigenschaften. Folgende Eigenschaften sind erforderlich:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([Pidtagproviderdllname (](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([Pidtagproviderdisplay (](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([Pidtagresourcetype (](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([Pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([Pidtagresourceflags (](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([Pidtagstatuscode (](pidtagstatuscode-canonical-property.md))
    
3. Implementieren Sie die [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) -Methoden, die für Ihren Anbieter geeignet sind. Je nach Anbieter müssen Sie nicht alle vier Methoden in **IMAPIStatus**implementieren. Jeder Anbieter sollte eine schreibgeschützte Version der Methoden der [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle und der [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) -Methode implementieren. 

   Transport Anbieter sollten auch [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md)implementieren, und alle Anbieter sollten [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md)unterstützen. Die Unterstützung für [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) ist jedoch optional. Nur Dienstanbieter, die Kennwörter erfordern und es Benutzern ermöglichen möchten, Sie programmgesteuert zu ändern, müssen diese Methode implementieren. Legen Sie für jede unterstützte Methode das entsprechende Bit in der **PR_RESOURCE_METHODS** -Eigenschaft fest. Wenn Sie beispielsweise **ValidateState** und **Settingsdialog** unterstützen, legen Sie **PR_RESOURCE_METHODS** auf Folgendes fest: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Clients sollten den Wert von **PR_RESOURCE_METHODS** überprüfen, bevor Sie versuchen, Ihr Status-Objekt aufzurufen. Behandeln Sie Aufrufe einer der nicht unterstützten Methoden, indem Sie MAPI_E_NO_SUPPORT zurückgeben. 
    
4. Rufen Sie [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) während der Anmeldung auf, um die Zeile oder Zeilen zur Statustabelle hinzuzufügen. Übergeben Sie ein Eigenschafts Wertarray, das die Spalteninformationen für die Zeile und 0 für den _ulFlags_ -Parameter enthält. Wenn sich der Status Ihres Anbieters zu einem späteren Zeitpunkt in der Sitzung ändert und es erforderlich ist, die Spalteninformationen zu aktualisieren, rufen Sie **ModifyStatusRow** erneut mit dem STATUSROW_UPDATE-Flagsatz auf. 
    
Weitere Informationen zu Statusobjekten finden Sie unter [MAPI-Statusobjekte](mapi-status-objects.md).
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Dienstanbieter](mapi-service-providers.md)

