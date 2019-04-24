---
title: Übersicht über das Support Objekt
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327167"
---
# <a name="support-object-overview"></a>Übersicht über das Support Objekt

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI liefert ein Support-Objekt, ein Objekt, das die [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle für alle Dienstanbieter während der Anmeldung und für alle Nachrichtendienste während der Konfiguration implementiert. 
  
Auf Support Objekte kann von Clients nicht zugegriffen werden; Sie werden von MAPI implementiert und nur von Dienstanbietern aufgerufen. Die **IMAPISupport** -Schnittstelle wird in der Headerdatei Mapispi. h angegeben. Der Bezeichner ist IID_IMAPISup, und sein Zeigertyp ist LPMAPISUP. Von Support-Objekten werden keine MAPI-Eigenschaften verfügbar gemacht. 
  
Ein Anbieter kann ein oder mehrere Support Objekte erhalten, je nachdem, wie oft MAPI den Anbieter protokolliert oder wie oft die Nachrichtendienst-Eingabefunktion des Anbieters aufgerufen wird. In der Regel wird ein Anbieter mindestens einmal pro Sitzung angemeldet. Adressbuch-und Transportanbieter werden bei jedem Start einer Sitzung mit einem Profileintrag, der Sie anfordert, bei jedem Client protokolliert. Nachrichtenspeicher Anbieter werden bei jedem Aufruf der [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) -Methode bei einem Client protokolliert. 
  
Bei mehreren Anmeldungen in einer Sitzung können Sie entweder die Option zum Aufbewahren und Verwenden der einzelnen Support Objekte separat oder zum Aufbewahren und verwenden nur des ersten, wobei jedes nachfolgende Support Objekt verworfen wird. Um ein Support Objekt beizubehalten, rufen Sie die zugehörige **IUnknown:: AddRef** -Methode auf. Das Aufrufen von **AddRef** für ein Support Objekt, das Sie während einer Sitzung aufbewahren möchten, ist äußerst wichtig; Wenn der Anruf nicht durchgeführt wird, gibt MAPI das Support Objekt frei und gibt den Arbeitsspeicher zurück. 
  
Der Zweck des Support-Objekts besteht darin, Implementierungen für eine relativ hohe Anzahl von Methoden bereitzustellen, die häufig von den Anbietern verwendet werden. Jedes Support Objekt enthält auch kontextbezogene Daten, die spezifisch für die eigene Instanz sind, beispielsweise die Sitzung, in der der Anbieter aktiv ist, den Profil Abschnitt, den der Anbieter verwendet, und Fehlerinformationen für die Sitzung. 
  
Es gibt vier verschiedene Typen von Unterstützungs Objekten: eine für jeden Haupt Anbietertyp (Adressbuch, Nachrichtenspeicher und Transport) und eine für Konfigurationsunterstützung. 
  
MAPI passt jedes Support Objekt an, indem es Implementierungen von Methoden einschließt, die für seine Verwendung relevant sind. Implementierungen einiger Methoden, wie [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md), sind in allen Support-Objekten enthalten. Implementierungen anderer Methoden wie [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md)gelten nur für bestimmte Support Objekte. Diese Methode kann nur für Nachrichtenspeicher-und Transportanbieter verwendet werden. Wenn ein Adressbuchanbieter oder ein Nachrichtendienst versucht, es aufzurufen, gibt MAPI MAPI_E_NO_SUPPORT zurück.
  
Unterstützende Objekte können zum Ausführen vieler Aufgaben verwendet werden, wie beispielsweise:
  
- Zugreifen auf einen Profil Abschnitt.
    
- Kopieren von Ordnern oder Nachrichten. Weitere Informationen finden Sie unter [Kopieren oder bewegen einer Nachricht oder eines Ordners](copying-or-moving-a-message-or-a-folder.md).
    
- Zugreifen auf Objekte, die zu anderen Anbietern gehören. Weitere Informationen finden Sie unter [unterstützen des Objektzugriffs und-Vergleichs](supporting-object-access-and-comparison.md). 
    
- Behandeln der Ereignisbenachrichtigung. Weitere Informationen finden Sie unter [UnterstützenDe Ereignisbenachrichtigung](supporting-event-notification.md).
    
- Reservieren und Freigeben von Arbeitsspeicher.
    
- Abrufen eines eindeutigen Bezeichners.
    
- Objekte werden nicht überprüft.
    
- Fehlerbehandlung.
    
- Registrieren von Nachrichten Präprozessoren. 
    
- Vorbereiten von Nachrichtenübermittlungsberichten. 
    
Während der Anmeldung ruft MAPI die Anmeldemethode des Anbieterobjekts jedes Dienstanbieters auf. Für Adressbuchanbieter ruft MAPI [IABProvider:: LOGON](iabprovider-logon.md)auf. Für Nachrichtenspeicher Anbieter ruft MAPI [IMSProvider:: LOGON](imsprovider-logon.md)auf. Für Transportanbieter ruft MAPI [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md)auf. MAPI übergibt einen Zeiger an das entsprechende Support-Objekt in einem der Parameter an diese Methode. Die Logon-Methode wiederum instanziiert ein LOGON-Objekt und übergibt dabei den Objektzeiger für den Support. Das Logon-Objekt ruft die **IUnknown:: AddRef** -Methode des Support Objekts auf, um Sie bei Bedarf beizubehalten. Weitere Informationen zum Anmeldeprozess für Dienstanbieter finden Sie unter [Starten eines Dienstanbieters](starting-a-service-provider.md).
  
Wenn ein Client sich abmeldet, ruft MAPI die Abmelde Methode des LOGON Objekts auf. Die logout-Methode ruft die **IUnknown:: Release** -Methode des Support Objekts auf, um anzugeben, dass der Anbieter keine der Supportmethoden mehr aufrufen möchte. Wie bei der Anmeldung weisen die Logoff-Methoden leicht unterschiedliche Namen auf. Die [IABLogon](iablogoniunknown.md) -und [IMSLogon](imslogoniunknown.md) -Schnittstellen weisen Abmeldemethoden auf. **** die [IXPLogon](ixplogoniunknown.md) -Schnittstelle verfügt über eine [TransportLogoff](ixplogon-transportlogoff.md) -Methode. 
  
Einstiegspunktfunktionen für den Nachrichtendienst werden aufgerufen, wenn ein Anmeldeversuch mit dem Fehler MAPI_E_UNCONFIGURED fehlschlägt oder wenn ein Client eine Konfigurationsanforderung initiiert. MAPI instanziiert ein Konfigurations Unterstützungsobjekt und ruft die Einstiegspunktfunktion des Nachrichtendiensts für den nicht konfigurierten Anbieter oder den Anbieter auf, dessen Konfiguration gerade geändert werden soll. Im Gegensatz zu anderen Support Objekten sind Konfigurations Unterstützungsobjekte nur gültig, wenn die Einstiegspunktfunktion zurückgegeben wird. Nachrichtendienste rufen die **AddRef** -Methoden dieser Objekte nicht auf, um Sie beizubehalten. 
  
In der Regel führt MAPI Aufrufe an die Funktion des Einstiegspunkts eines Anbieters für den Nachrichtendienst aus, aber manchmal wird ein Anbieter aufgefordert, den Anruf zu tätigen. Dies kann auftreten, wenn ein Client die [IMAPIStatus:: Settingsdialog](imapistatus-settingsdialog.md) -Methode eines Anbieters aufruft, um den Anbieter aufzufordern, dessen Konfigurationseigenschaften Blatt anzuzeigen. **Settingsdialog** sollte [IMAPISupport:: GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) aufrufen, um ein Konfigurations Unterstützungsobjekt abzurufen, das an die Einstiegspunktfunktion des Nachrichtendiensts weitergegeben werden kann. 
  
Die [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode ist für die Bestimmung der Adressen der Speicher Zuweisungs-und Zuordnungsfunktionen verfügbar, ohne dass eine Verknüpfung mit MAPI hergestellt werden muss. Die Verwendung von **GetMemAllocRoutines** erleichtert auch die Ablaufverfolgung von Speicherlecks, indem die Zuordnungs Funktionsaufrufe mit Debugcode umgeben werden. Wenn Sie **GetMemAllocRoutines**aufrufen, wie empfohlen, tun Sie dies, bevor Sie die [CreateIProp](createiprop.md) -Funktion aufrufen, die die Zuordnungs Funktions Adressen als Parameter erfordert. 
  
Wenn Sie ein neues Adressbuch-oder Nachrichtenspeicherobjekt erstellen müssen, erstellen Sie einen Suchschlüssel für das Objekt in seiner **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft, und legen Sie ihn fest. Rufen Sie [IMAPISupport:: NewUID](imapisupport-newuid.md) auf, um einen eindeutigen Bezeichner abzurufen, der beim Erstellen eines Suchschlüssels verwendet werden soll. Verwenden Sie nicht Ihre eigene hart codierte [MAPIUID](mapiuid.md). Die **MAPIUID** eines Anbieters sollten nur für Eintrags-IDs verwendet werden. Weitere Informationen zum Erstellen von Such Schlüsseln finden Sie unter [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
Eine Clientanwendung kann ein Objekt manchmal freigeben, ohne ein oder mehrere der zugehörigen Objekte freizugeben. In einem solchen Fall muss ein Anbieter möglicherweise ein nicht freigegebenes Objekt als unbenutzbar rendern. Hierzu gibt der Anbieter alle Ressourcen frei, die mit dem Objekt verbunden sind, und ruft dann [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) auf, um die Vtable des Objekts zu invalidisieren. **MakeInvalid** ersetzt die **IUnknown** -Methoden (**QueryInterface**, **AddRef**und **Release**) der vtable durch standardmäßige MAPI-Implementierungen und bewirkt, dass alle anderen Methoden MAPI_E_INVALID_OBJECT zurückgeben. **MakeInvalid** gibt auch den gesamten Speicher des Objekts außer der vtable frei. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

