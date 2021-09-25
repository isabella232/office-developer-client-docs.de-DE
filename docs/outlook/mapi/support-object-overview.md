---
title: Supportobjektübersicht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b22632aecc048089f49aa92681bf6af1b43b7947
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566367"
---
# <a name="support-object-overview"></a>Supportobjektübersicht

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI stellt ein Unterstützungsobjekt bereit, ein Objekt, das die [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) implementiert, für alle Dienstanbieter während der Anmeldung und für alle Nachrichtendienste während der Konfiguration. 
  
Auf Supportobjekte kann von Clients nicht zugegriffen werden. sie werden von der MAPI implementiert und nur von Dienstanbietern aufgerufen. Die **IMAPISupport-Schnittstelle** wird in der Headerdatei Mapispi.h angegeben. Der Bezeichner ist IID_IMAPISup, und der Zeigertyp lautet LPMAPISUP. Supportobjekte machen keine MAPI-Eigenschaften verfügbar. 
  
Ein Anbieter kann ein oder mehrere Unterstützungsobjekte erhalten, je nachdem, wie oft mapi den Anbieter protokolliert oder wie oft die Nachrichtendienst-Eintragsfunktion des Anbieters aufgerufen wird. In der Regel wird ein Anbieter mindestens einmal pro Sitzung angemeldet. Adressbuch- und Transportanbieter werden jedes Mal angemeldet, wenn ein Client eine Sitzung mit einem Profileintrag startet, der sie anfordert. Nachrichtenspeicheranbieter werden jedes Mal angemeldet, wenn ein Client die [IMAPISession::OpenMsgStore-Methode aufruft.](imapisession-openmsgstore.md) 
  
Bei mehreren Anmeldungen in einer Sitzung können Sie entweder jedes Supportobjekt separat aufbewahren und verwenden oder nur das erste beibehalten und verwenden, und jedes nachfolgende Supportobjekt verwerfen. Rufen Sie die **IUnknown::AddRef-Methode** auf, um ein Supportobjekt beizubehalten. Das Aufrufen von **AddRef** für ein Supportobjekt, das Sie während einer Sitzung beibehalten möchten, ist äußerst wichtig. Wenn der Aufruf nicht erfolgt, gibt MAPI das Supportobjekt frei und gibt seinen Speicher frei. 
  
Der Zweck des Supportobjekts besteht darin, Implementierungen für eine relativ große Anzahl von Methoden bereitzustellen, die häufig von den Anbietern verwendet werden. Jedes Supportobjekt enthält auch Kontextdaten, die für seine eigene Instanz spezifisch sind, z. B. die Sitzung, in der der Anbieter ausgeführt wird, den Profilabschnitt, den der Anbieter verwendet, und Fehlerinformationen für die Sitzung. 
  
Es gibt vier verschiedene Arten von Unterstützungsobjekten: einen für jeden Hauptanbietertyp (Adressbuch, Nachrichtenspeicher und Transport) und einen für die Konfigurationsunterstützung. 
  
MAPI passt jedes Unterstützungsobjekt an, indem Implementierungen von Methoden eingeschlossen werden, die für seine Verwendung relevant sind. Implementierungen einiger Methoden, z. B. [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md)sind in allen Unterstützungsobjekten enthalten. Implementierungen anderer Methoden, z. B. [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md)gelten nur für bestimmte Unterstützungsobjekte. Nur Nachrichtenspeicher- und Transportanbieter können diese Methode verwenden. Wenn ein Adressbuchanbieter oder ein Nachrichtendienst versucht, ihn aufzurufen, gibt MAPI MAPI_E_NO_SUPPORT zurück.
  
Unterstützungsobjekte können verwendet werden, um viele Aufgaben auszuführen, z. B. die folgenden:
  
- Zugreifen auf einen Profilabschnitt.
    
- Kopieren von Ordnern oder Nachrichten. Weitere Informationen finden Sie unter [Kopieren oder Verschieben einer Nachricht oder eines Ordners.](copying-or-moving-a-message-or-a-folder.md)
    
- Zugreifen auf Objekte, die zu anderen Anbietern gehören. Weitere Informationen finden Sie unter [Unterstützen des Objektzugriffs und -vergleichs.](supporting-object-access-and-comparison.md) 
    
- Behandeln von Ereignisbenachrichtigungen. Weitere Informationen finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md)
    
- Zuordnen und Freigeben von Arbeitsspeicher.
    
- Abrufen eines eindeutigen Bezeichners.
    
- Ungültige Objekte.
    
- Behandeln von Fehlern.
    
- Registrieren von Nachrichtenpräprozessoren. 
    
- Vorbereiten von Nachrichtenübermittlungsberichten. 
    
Zur Anmeldezeit ruft MAPI die Anmeldemethode des Anbieterobjekts jedes Dienstanbieters auf. Für Adressbuchanbieter ruft MAPI [IABProvider::Logon auf.](iabprovider-logon.md) Für Nachrichtenspeicheranbieter ruft MAPI [IMSProvider::Logon auf.](imsprovider-logon.md) Für Transportanbieter ruft MAPI [IXPProvider::TransportLogon auf.](ixpprovider-transportlogon.md) MAPI übergibt einen Zeiger an das entsprechende Unterstützungsobjekt in einem der Parameter an diese Methode. Die Anmeldemethode instanziiert wiederum ein Anmeldeobjekt und übergibt es an den Supportobjektzeiger. Das Anmeldeobjekt ruft die **IUnknown::AddRef-Methode** des Supportobjekts auf, um es bei Bedarf beizubehalten. Weitere Informationen zum Anmeldevorgang für Dienstanbieter finden Sie unter ["Starten eines Dienstanbieters".](starting-a-service-provider.md)
  
Wenn sich ein Client abmeldet, ruft MAPI die Abmeldemethode des Anmeldeobjekts auf. Die Abmeldemethode ruft die **IUnknown::Release-Methode** des Supportobjekts auf, um anzugeben, dass der Anbieter nicht mehr beabsichtigt, eine der Supportmethoden aufzurufen. Wie bei der Anmeldung weisen die Abmeldemethoden leicht unterschiedliche Namen auf. Die [IABLogon-](iablogoniunknown.md) und [IMSLogon-Schnittstellen](imslogoniunknown.md) verfügen über **Abmeldemethoden.** Die [IXPLogon-Schnittstelle](ixplogoniunknown.md) verfügt über eine [TransportLogoff-Methode.](ixplogon-transportlogoff.md) 
  
Nachrichtendienst-Einstiegspunktfunktionen werden aufgerufen, wenn ein Anmeldeversuch mit dem Fehler MAPI_E_UNCONFIGURED fehlschlägt oder wenn ein Client eine Konfigurationsanforderung initiiert. Die MAPI instanziiert ein Konfigurationsunterstützungsobjekt und ruft die Nachrichtendienst-Einstiegspunktfunktion für den nicht konfigurierten Anbieter oder den Anbieter auf, dessen Konfiguration sich ändern wird. Im Gegensatz zu den anderen Unterstützungsobjekten sind Konfigurationsunterstützungsobjekte nur gültig, bis die Einstiegspunktfunktion zurückgegeben wird. Nachrichtendienste rufen die **AddRef-Methoden** dieser Objekte nicht auf, um sie beizubehalten. 
  
In der Regel führt die MAPI Aufrufe an die Nachrichtendienst-Einstiegspunktfunktion eines Anbieters durch, manchmal wird jedoch ein Anbieter aufgefordert, den Aufruf auszuführen. Dies kann vorkommen, wenn ein Client die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) eines Anbieters aufruft, um den Anbieter aufzufordern, sein Konfigurationseigenschaftenblatt anzuzeigen. **SettingsDialog** sollte [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) aufrufen, um ein Konfigurationsunterstützungsobjekt abzurufen, das an die Nachrichtendienst-Einstiegspunktfunktion übergeben werden kann. 
  
Die [IMAPISupport::GetMemAllocRoutines-Methode](imapisupport-getmemallocroutines.md) ist verfügbar, um die Adressen der Speicherzuweisungs- und Zuordnungsfunktionen zu ermitteln, ohne eine Verknüpfung mit mapi herstellen zu müssen. Die Verwendung von **GetMemAllocRoutines** erleichtert auch das Nachverfolgen von Speicherverlusten, indem die Zuordnungsfunktionsaufrufe mit Debugcode umgeben werden. Wenn Sie **GetMemAllocRoutines** wie empfohlen aufrufen, tun Sie dies, bevor Sie die [CreateIProp-Funktion](createiprop.md) aufrufen, die die Zuordnungsfunktionsadressen als Parameter erfordert. 
  
Wenn Sie ein neues Adressbuch- oder Nachrichtenspeicherobjekt erstellen müssen, erstellen und legen Sie einen Suchschlüssel für das Objekt in der **eigenschaft PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) fest. Rufen Sie [IMAPISupport::NewUID](imapisupport-newuid.md) auf, um einen eindeutigen Bezeichner abzurufen, der beim Erstellen eines Suchschlüssels verwendet werden soll. Verwenden Sie keine eigenen hartcodierten [MAPIUID](mapiuid.md). Die **MAPIUID** eines Anbieters sollte nur für Eintragsbezeichner verwendet werden. Weitere Informationen zum Erstellen von Suchschlüsseln finden Sie unter [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
Eine Clientanwendung kann manchmal ein Objekt freigeben, ohne eines oder mehrere der zugehörigen Objekte freizugeben. In einem solchen Fall muss ein Anbieter möglicherweise ein nicht freigegebenes Objekt unbrauchbar rendern. Zu diesem Zweck gibt der Anbieter alle mit dem Objekt verbundenen Ressourcen frei und ruft dann [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) auf, um die vtable des Objekts ungültig zu machen. **MakeInvalid** ersetzt die **IUnknown-Methoden** der vtable (**QueryInterface**, **AddRef** und **Release**) durch standardmäßige MAPI-Implementierungen und bewirkt, dass alle anderen Methoden MAPI_E_INVALID_OBJECT zurückgeben. **MakeInvalid** gibt auch den gesamten Arbeitsspeicher des Objekts frei, außer der vtable. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

