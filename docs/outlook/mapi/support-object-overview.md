---
title: Übersicht über Unterstützungsobjekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f43a50d08daedc623fa1e4570eafa5d58be71f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577436"
---
# <a name="support-object-overview"></a>Übersicht über Unterstützungsobjekte

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI stellt ein Support-Objekt, ein Objekt, das implementiert bereit die [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle, die für alle Dienstanbieter bei der Anmeldung und für alle Nachrichtendienste während der Konfiguration. 
  
Unterstützungsobjekte sind nicht Clients zugreifen können. Sie sind von MAPI implementierte und nur vom Dienstanbieter aufgerufen. Die **IMAPISupport** -Schnittstelle wird in der Headerdatei Mapispi.h angegeben. Des Bezeichners IID_IMAPISup und dieses Zeigertyps LPMAPISUP. Keine MAPI-Eigenschaften werden von Unterstützungsobjekte verfügbar gemacht. 
  
Ein Anbieter kann zugewiesen werden, eine oder mehrere Unterstützungsobjekte, je nachdem, wie oft sollen MAPI den Anbieter oder die Anzahl der Häufigkeit, mit die der Anbieter Nachricht Service Eintrag-Funktion aufgerufen wird. In der Regel wird ein Anbieter mindestens einmal pro Sitzung angemeldet sein. Address Book und Transport-Provider sind angemeldet, jedes Mal, wenn ein Client eine Sitzung mit einem Profileintrag gestartet, der sie anfordert. Jedes Mal, wenn ein Client die [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) -Methode aufruft, sind Nachricht Anbieter angemeldet. 
  
Im Fall von mehreren Anmeldungen in einer Sitzung können Sie entweder zu behalten und jedes Objekt Unterstützung separat verwenden oder beibehalten werden, und verwenden Sie nur die ersten jedes nachfolgende Support-Objekt verworfen. Um ein Objekt Support beizubehalten, rufen Sie seine **IUnknown:: AddRef** -Methode. Aufruf von **AddRef** für ein Support-Objekt, das Sie während einer Sitzung beibehalten möchten ist äußerst wichtig. Wenn der Anruf nicht erfolgt, MAPI-Freigaben für den Support-Objekt und gibt den Speicherplatz frei. 
  
Der Zweck des Support-Objekts ist bei Implementierungen für eine relativ große Anzahl von Methoden, die der Anbieter verwendet werden. Jedes Support-Objekt enthält auch Kontextdaten speziell für ihre eigene Instanz, wie der Sitzungen, in denen der Anbieter im Profilabschnitt, den der Anbieter verwendet ausgeführt wird, und die Fehlerinformationen für die Sitzung. 
  
Es gibt vier verschiedene Typen von Unterstützungsobjekte: einen für jeden Haupt-Anbietertyp (Adressbuch, Nachrichtenspeicher und Transport) und einen für die Konfiguration. 
  
MAPI passt jedes Objekt Unterstützung durch das Einbeziehen von Implementierungen der Methoden, die für die Verwendung von Bedeutung sind. Implementierungen von einige Methoden wie [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), sind alle Support-Objekte enthalten. Die Implementierung von anderen Methoden wie [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md), gelten nur für bestimmte Unterstützungsobjekte. Nur Nachrichtenspeicher und Transportanbieter können diese Methode verwenden. Wenn Adressbuch-Dienstanbieter oder eine Message Service versuchen es aufrufen, gibt MAPI MAPI_E_NO_SUPPORT zurück.
  
Unterstützungsobjekte können viele, wie die folgenden Aufgaben verwendet werden:
  
- Zugreifen auf einen Profilabschnitt.
    
- Kopieren von Ordnern oder Nachrichten. Weitere Informationen finden Sie unter [Kopieren oder Verschieben einer Nachricht oder eines Ordners](copying-or-moving-a-message-or-a-folder.md).
    
- Zugreifen auf Objekte, die andere Anbieter angehören. Weitere Informationen finden Sie unter [Vergleich und unterstützende Object Access](supporting-object-access-and-comparison.md). 
    
- Behandeln von ereignisbenachrichtigung. Weitere Informationen finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md).
    
- Reservieren und Freigeben von Arbeitsspeicher.
    
- Abrufen eines eindeutigen Bezeichners.
    
- Objekte für ungültig erklärt.
    
- Behandeln von Fehlern.
    
- Nachricht Präprozessoren registrieren. 
    
- Vorbereiten der Nachricht Übermittlungsberichte. 
    
Bei der Anmeldung ruft MAPI die Logon-Methode des jeder Dienstanbieter Anbieter-Objekts. Für adressbuchanbietern implementierte ruft MAPI [IABProvider::Logon](iabprovider-logon.md). Für Nachricht-Anbieter ruft MAPI [IMSProvider::Logon](imsprovider-logon.md). Für Transportanbieter für ruft MAPI [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). MAPI übergibt einen Zeiger auf das entsprechende Unterstützung-Objekt in einer der Parameter an diese Methode. Die Logon-Methode instanziiert wiederum eine Anmeldung-Objekt, übergeben sie den Zeiger Support-Objekt. Das Anmeldeobjekt Ruft die des Unterstützungsobjekts **IUnknown:: AddRef** -Methode zum beibehalten, bei Bedarf. Weitere Informationen zu den Anmeldevorgang für Dienstanbieter finden Sie unter [einem Dienstanbieter zu starten](starting-a-service-provider.md).
  
Wenn ein Client abmeldet, ruft MAPI das Anmeldeobjekt logoff (Methode). Logoff (Methode) Ruft das Support-Objekt **IUnknown** -Methode, um darauf hinzuweisen, dass der Anbieter nicht mehr die Support-Methoden aufrufen will. Wie bei der Anmeldung haben die Methoden Abmeldung etwas andere Namen. Die [IABLogon](iablogoniunknown.md) und [IMSLogon](imslogoniunknown.md) Schnittstellen haben **Abmeldung** Methoden. die Schnittstelle [IXPLogon](ixplogoniunknown.md) verfügt über eine [TransportLogoff](ixplogon-transportlogoff.md) -Methode. 
  
Nachricht Webdienstfunktionen Entry Point werden aufgerufen, wenn ein Anmeldeversuch fehlschlägt, mit dem Fehler MAPI_E_UNCONFIGURED oder wenn ein Client eine Anforderung Konfiguration initiiert. MAPI instanziiert ein Support-Konfigurationsobjekt und ruft die Meldung Service Entry Point-Funktion für den Anbieter nicht konfiguriert oder der Anbieter, deren Konfiguration geändert wird. Im Gegensatz zu anderen Unterstützungsobjekte gelten Unterstützungsobjekte Konfiguration nur, bis der Einstiegspunkt-Funktion gibt zurück; Diese Objekte **AddRef** -Methoden, um zu verhindern, sie rufen Sie Message-Dienste. 
  
In der Regel MAPI des Anbieters Nachricht Service Entry Point-Funktion aufruft, aber in einigen Fällen ist ein Anbieter aufgefordert werden, den Anruf zu tätigen. Dies kann vorkommen, wenn ein Client [einen Anbieter SettingsDialog des Dienstanbieters für das Eigenschaftenblatt Konfiguration anzuzeigen aufgefordert](imapistatus-settingsdialog.md) aufruft. **SettingsDialog** sollte Aufrufen [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) um ein Konfigurationsobjekt Support zu erhalten, die an die Nachricht Service Entry Point-Funktion übergeben werden kann. 
  
Die [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode ist für die Bestimmung der Adressen der Arbeitsspeicher Reservierung und Freigabe Funktionen ohne Verknüpfung mit MAPI verfügbar. Verwenden von **GetMemAllocRoutines** vereinfacht auch So verfolgen Sie Speicherverluste umgebenden die Zuweisung Funktionsaufrufe mit Debuggen von Code. Wenn Sie **GetMemAllocRoutines**, rufen Sie wie empfohlen wird, führen Sie vor dem Aufrufen der [CreateIProp](createiprop.md) -Funktion, die die Zuordnung Funktion Adressen als Parameter erforderlich sind. 
  
Wenn Sie erstellen müssen ein neues Adressbuch oder einer Nachricht Objekt speichern, erstellen und einen Search-Schlüssel für das Objekt in der **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))-Eigenschaft festlegen. Rufen Sie [IMAPISupport::NewUID](imapisupport-newuid.md) , um eine eindeutige ID verwenden Sie beim Erstellen eines Schlüssels für die Suche zu erhalten. Verwenden Sie eine eigene hartcodierte [MAPIUID](mapiuid.md)nicht. Ein Anbieter **MAPIUID** sollte nur für Eintragsbezeichner verwendet werden. Weitere Informationen zum Erstellen von Search-Schlüssel finden Sie unter [MAPI-Datensatz und Suche Schlüssel](mapi-record-and-search-keys.md).
  
Eine Clientanwendung kann ein Objekt ohne einen oder mehrere verbundenen Objekte freigibt manchmal freigeben. In diesem Fall müssen ein Anbieter für ein nicht freigegebene Objekt nicht mehr wiedergegeben. Zu diesem Zweck der Anbieter gibt alle Ressourcen verbunden mit dem Objekt frei und ruft dann [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) , um das Objekt Vtable ungültig. **MakeInvalid** ersetzt die Vtable **IUnknown** -Methoden (**QueryInterface**, **AddRef**und **Release**) mit standard MAPI Implementierungen und bewirkt, dass alle anderen Methoden zur MAPI_E_INVALID_OBJECT zurückzugeben. **MakeInvalid** gibt auch alle der Speicher des Objekts als Vtable frei. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

