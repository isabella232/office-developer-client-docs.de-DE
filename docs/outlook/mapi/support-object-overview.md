---
title: Übersicht über das Supportobjekt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433612"
---
# <a name="support-object-overview"></a>Übersicht über das Supportobjekt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI stellt ein Supportobjekt bereit, ein Objekt, das die [IMAPISupport : IUnknown-Schnittstelle](imapisupportiunknown.md) implementiert, für alle Dienstanbieter während der Anmeldung und für alle Nachrichtendienste während der Konfiguration. 
  
Auf Supportobjekte kann von Clients nicht zugegriffen werden. sie werden von MAPI implementiert und nur von Dienstanbietern aufgerufen. Die **IMAPISupport-Schnittstelle** wird in der Mapispi.h-Headerdatei angegeben. Der Bezeichner ist IID_IMAPISup, und der Zeigertyp ist LPMAPISUP. Keine MAPI-Eigenschaften werden von Supportobjekten verfügbar gemacht. 
  
Ein Anbieter kann ein oder mehrere Supportobjekte erhalten, je nachdem, wie oft MAPI den Anbieter protokolliert oder wie oft die Nachrichtendiensteintragsfunktion des Anbieters aufgerufen wird. In der Regel wird ein Anbieter mindestens einmal pro Sitzung angemeldet. Adressbuch- und Transportanbieter werden jedes Mal angemeldet, wenn ein Client eine Sitzung mit einem Profileintrag startet, der sie anfordert. Nachrichtenspeicheranbieter werden jedes Mal angemeldet, wenn ein Client die [IMAPISession::OpenMsgStore-Methode](imapisession-openmsgstore.md) aufruft. 
  
Bei mehreren Anmeldungen in einer Sitzung können Sie entweder jedes Supportobjekt separat beibehalten und verwenden oder nur das erste beibehalten und verwenden und jedes nachfolgende Supportobjekt verwerfen. Rufen Sie die **IUnknown::AddRef-Methode** auf, um ein Supportobjekt zu erhalten. Das **Aufrufen von AddRef** für ein Supportobjekt, das Sie während einer Sitzung beibehalten möchten, ist äußerst wichtig. Wenn der Aufruf nicht erfolgt, gibt MAPI das Supportobjekt frei und gibt den Arbeitsspeicher frei. 
  
Der Zweck des Supportobjekts besteht in der Bereitstellung von Implementierungen für eine relativ große Anzahl von Methoden, die häufig von den Anbietern verwendet werden. Jedes Supportobjekt enthält auch Kontextdaten, die für die eigene Instanz spezifisch sind, z. B. die Sitzung, in der der Anbieter ausgeführt wird, den Profilabschnitt, den der Anbieter verwendet, und Fehlerinformationen für die Sitzung. 
  
Es gibt vier verschiedene Arten von Supportobjekten: eines für jeden hauptanbietertyp (Adressbuch, Nachrichtenspeicher und Transport) und eines für die Konfigurationsunterstützung. 
  
MAPI passt jedes Supportobjekt an, indem Implementierungen von Methoden hinzugefügt werden, die für die Verwendung relevant sind. Implementierungen einiger Methoden, z. B. [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md)sind in allen Supportobjekten enthalten. Implementierungen anderer Methoden, z. B. [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md), gelten nur für bestimmte Supportobjekte. Diese Methode kann nur von Nachrichtenspeicher- und Transportanbietern verwendet werden. Wenn ein Adressbuchanbieter oder ein Nachrichtendienst versucht, ihn auf den Anruf zu rufen, gibt MAPI MAPI_E_NO_SUPPORT.
  
Unterstützungsobjekte können verwendet werden, um viele Aufgaben auszuführen, z. B.:
  
- Zugreifen auf einen Profilabschnitt.
    
- Kopieren von Ordnern oder Nachrichten. Weitere Informationen finden Sie unter [Kopieren oder Verschieben einer Nachricht oder eines Ordners.](copying-or-moving-a-message-or-a-folder.md)
    
- Zugreifen auf Objekte, die zu anderen Anbietern gehören. Weitere Informationen finden Sie unter [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md). 
    
- Behandeln der Ereignisbenachrichtigung. Weitere Informationen finden Sie unter [Supporting Event Notification](supporting-event-notification.md).
    
- Zuordnen und Freispeichern.
    
- Abrufen eines eindeutigen Bezeichners.
    
- Ungültige Objekte.
    
- Behandeln von Fehlern.
    
- Registrieren von Nachrichtenvorprozessoren. 
    
- Vorbereiten von Nachrichtenzustellungsberichten. 
    
Zum Zeitpunkt der Anmeldung ruft MAPI die Anmeldemethode des Anbieterobjekts jedes Dienstanbieters auf. Für Adressbuchanbieter ruft MAPI [IABProvider::Logon auf.](iabprovider-logon.md) Für Nachrichtenspeicheranbieter ruft MAPI [IMSProvider::Logon auf.](imsprovider-logon.md) Für Transportanbieter ruft MAPI [IXPProvider::TransportLogon auf.](ixpprovider-transportlogon.md) MAPI übergibt einen Zeiger auf das entsprechende Supportobjekt in einem der Parameter an diese Methode. Die Anmeldemethode instanziiert wiederum ein Anmeldeobjekt, und übergeben es an den Unterstützungsobjektzeiger. Das Anmeldeobjekt ruft die **IUnknown::AddRef-Methode** des Supportobjekts auf, um es bei Bedarf zu behalten. Weitere Informationen zum Anmeldeprozess für Dienstanbieter finden Sie unter [Starting a Service Provider](starting-a-service-provider.md).
  
Wenn sich ein Client abmeldet, ruft MAPI die Abmeldemethode des Anmeldeobjekts auf. Die Abmeldemethode ruft die **IUnknown::Release-Methode** des Supportobjekts auf, um anzugeben, dass der Anbieter keine der Supportmethoden mehr aufrufen möchte. Wie bei der Anmeldung haben die Abmeldemethoden geringfügig andere Namen. Die [Schnittstellen IABLogon](iablogoniunknown.md) und [IMSLogon](imslogoniunknown.md) verfügen **über Logoff-Methoden.** Die [IXPLogon-Schnittstelle](ixplogoniunknown.md) verfügt über eine [TransportLogoff-Methode.](ixplogon-transportlogoff.md) 
  
Nachrichtendienst-Einstiegspunktfunktionen werden aufgerufen, wenn ein Anmeldeversuch mit dem Fehler MAPI_E_UNCONFIGURED oder wenn ein Client eine Konfigurationsanforderung initiiert. MAPI instanziiert ein Konfigurationsunterstützungsobjekt und ruft die Einstiegspunktfunktion des Nachrichtendiensts entweder für den nicht konfigurierten Anbieter oder den Anbieter auf, dessen Konfiguration sich ändern wird. Im Gegensatz zu den anderen Supportobjekten sind Konfigurationsunterstützungsobjekte nur gültig, bis die Einstiegspunktfunktion zurückgegeben wird. Nachrichtendienste rufen die **AddRef-Methoden** dieser Objekte nicht auf, um sie zu behalten. 
  
In der Regel ruft MAPI die Einstiegspunktfunktion des Nachrichtendiensts eines Anbieters auf, manchmal wird jedoch ein Anbieter aufgefordert, den Anruf zu machen. Dies kann auftreten, wenn ein Client die [IMAPIStatus::SettingsDialog-Methode](imapistatus-settingsdialog.md) eines Anbieters aufruft, um den Anbieter zur Anzeige seines Konfigurationseigenschaftsblatts aufforderen. **SettingsDialog** sollte [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) aufrufen, um ein Konfigurationsunterstützungsobjekt zu erhalten, das an die Einstiegspunktfunktion des Nachrichtendiensts übergeben werden kann. 
  
Die [IMAPISupport::GetMemAllocRoutines-Methode](imapisupport-getmemallocroutines.md) steht zum Bestimmen der Adressen der Speicherzuweisungs- und Deallocationfunktionen zur Verfügung, ohne eine Verknüpfung mit MAPI erstellen zu müssen. Die **Verwendung von GetMemAllocRoutines** vereinfacht außerdem die Nachverfolgung von Speicherverlusten, indem die Zuweisungsfunktionsaufrufe mit Debugcode umgeben werden. Wenn Sie **GetMemAllocRoutines** aufrufen, wie empfohlen, tun Sie dies, bevor Sie die [CreateIProp-Funktion](createiprop.md) aufrufen, die die Zuordnungsfunktionsadressen als Parameter erfordert. 
  
Wenn Sie ein neues Adressbuch- oder Nachrichtenspeicherobjekt erstellen müssen, erstellen und legen Sie einen Suchschlüssel für das Objekt in seiner **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft. Rufen [Sie IMAPISupport::NewUID auf,](imapisupport-newuid.md) um einen eindeutigen Bezeichner zu erhalten, der beim Erstellen eines Suchschlüssels verwendet werden soll. Verwenden Sie keine eigene hart codierte [MAPIUID](mapiuid.md). Die **MAPIUID** eines Anbieters sollte nur für Eintragsbezeichner verwendet werden. Weitere Informationen zum Erstellen von Suchschlüsseln finden Sie unter [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
Eine Clientanwendung kann manchmal ein Objekt freigeben, ohne eines oder mehrere der verbundenen Objekte frei zu geben. In diesem Fall muss ein Anbieter möglicherweise ein unveröffentlichtes Objekt unbrauchbar machen. Dazu gibt der Anbieter alle ressourcen frei, die mit dem Objekt verbunden sind, und ruft [dann IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) auf, um die vtable des Objekts ungültig zu machen. **MakeInvalid** ersetzt die **IUnknown-Methoden** der vtable (**QueryInterface,** **AddRef** und **Release**) durch standardmäßige MAPI-Implementierungen und bewirkt, dass alle anderen Methoden MAPI_E_INVALID_OBJECT. **MakeInvalid** gibt auch den speicher des Objekts frei, der nicht die vtable ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

