---
title: Testen der Bereitstellung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: In diesem Thema werden einige Szenarien beschrieben, auf die Sie im Hinblick auf die Installation und Deinstallation eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) testen sollten.
ms.openlocfilehash: 3860deb1157477f156b0fae1506c5c6b08699786
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590352"
---
# <a name="testing-deployment"></a>Testen der Bereitstellung

In diesem Thema werden einige Szenarien beschrieben, auf die Sie im Hinblick auf die Installation und Deinstallation eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) testen sollten.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Vorhandensein von Outlook und osc auf dem Clientcomputer

Zu den Faktoren, die sich auf die Installation eines OSC-Anbieters auswirken, gehören die Bitanzahl des Betriebssystems, das Vorhandensein und die Bitanzahl von Outlook und das in Outlook aktivierte OSC.
  
Ein OSC-Anbieter kann für eine 32-Bit- oder 64-Bit-Version des OSC geschrieben werden. Outlook 2010 und Outlook 2013 sind sowohl in 32-Bit- als auch in 64-Bit-Versionen verfügbar, und Office Outlook 2003 und Office Outlook 2007 sind nur in 32-Bit-Versionen verfügbar. Auf einem 64-Bit-Windows Betriebssystem können Sie entweder 32-Bit- oder 64-Bit-Outlook installieren. Unter einem 32-Bit-Betriebssystem können Sie nur 32-Bit-, aber nicht 64-Bit-Outlook installieren. Abhängig von der Bitanzahl der installierten Version von Outlook und dem OSC-Anbieter selbst sollte der Benutzer das entsprechende Installationsprogramm verwenden, um einen OSC-Anbieter mit der entsprechenden Bitanzahl zu installieren. Wenn beispielsweise 64-Bit-Outlook installiert ist und der OSC-Anbieter eine systemeigene COM-Komponente ist, funktioniert kein 32-Bit-OSC-Anbieter, und der Benutzer muss das entsprechende Installationsprogramm verwenden, um einen 64-Bit-OSC-Anbieter zu installieren.
  
Der Bereitstellungscode Ihres OSC-Anbieters kann davon ausgehen, dass der Benutzer über eine unterstützte Version von Outlook auf dem Computer verfügt. Wenn sich die aktuelle Version von OSC jedoch nicht auf dem Clientcomputer befindet, kann Ihr Bereitstellungscode eine entsprechende Version des OSC herunterladen und installieren, indem speziell erstellte G-Link-URLs auf verwendet https://g.live.com werden. Diese g-Links hängen von der Version und Bitanzahl von Outlook und dem Gebietsschema des Clientcomputers ab. Weitere Informationen zur Verwendung von g-Links zum Installieren oder Aktualisieren des OSC finden Sie unter [Installationscheckliste.](installation-checklist.md)
  
Vor der Installation eines OSC-Anbieters sollte der Outlook Benutzer sicherstellen, dass das OSC-Add-In in Outlook aktiviert ist.
  
Die empfohlene Methode zum Bereitstellen eines OSC-Anbieters ist die Verwendung eines Windows Installer-Pakets (.msi). Testen Sie jedes der folgenden Szenarien, um zu überprüfen, ob die Bereitstellung für den Anbieter ordnungsgemäß funktioniert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Outlook ist nicht vorhanden – Outlook 2003 oder Outlook 2007 ist nicht installiert, und Outlook 2010 oder Microsoft Outlook 2013 wird weder installiert noch per Klick-und-Los bereitgestellt.  <br/> |Die Bereitstellung schlägt fehl.  <br/> |
|Outlook 2003 oder Outlook 2007 ist nicht installiert, aber Outlook 2010 oder Microsoft Outlook 2013 wurde per Klick-und-Los bereitgestellt.  <br/> |Der 32-Bit-Anbieter wird bereitgestellt.  <br/> |
|Outlook 2003 oder Outlook 2007 ist installiert, der OSC ist jedoch nicht installiert.  <br/> |Das Installationsprogramm installiert osc und alle Patches. Nachdem das OSC erfolgreich installiert wurde, stellt das Installationsprogramm den Anbieter bereit.  <br/> |
|Outlook 2003 oder Outlook 2007 installiert ist und eine frühere Version des OSC installiert ist.  <br/> |Das Installationsprogramm aktualisiert den OSC über einen g-Link zu Patches und stellt dann den Anbieter bereit.  <br/> |
|Outlook 2003 oder 2007 installiert ist und der OSC auf dem neuesten Stand ist.  <br/> |Das Installationsprogramm stellt den 32-Bit-Anbieter bereit.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert ist, der OSC ist jedoch nicht installiert.  <br/> |Das Installationsprogramm schlägt mit einer entsprechenden Fehlermeldung fehl.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert ist und eine ältere Version des OSC installiert ist.  <br/> |Das Installationsprogramm, das für die Bitanzahl der installierten Outlook 2010 oder Microsoft Outlook 2013 geeignet ist, aktualisiert osc über den g-Link auf Patches und stellt dann den entsprechenden Anbieter bereit.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert ist und der OSC auf dem neuesten Stand ist.  <br/> |Das Installationsprogramm, das der Bitanzahl des installierten Outlook 2010 oder Microsoft Outlook 2013 (32-Bit oder 64-Bit) entspricht, stellt den entsprechenden Anbieter bereit.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Installierter Speicherort und Registrierungsschlüssel

Überprüfen Sie den Dateispeicherort, an dem Ihr OSC-Anbieter bereitgestellt wurde, und die Speicherorte in der Windows Registrierung, in der Registrierungsschlüssel für Ihren Anbieter erstellt werden.
  
### <a name="file-location-for-osc-provider-dlls"></a>Dateispeicherort für OSC-Anbieter-DLLs

Testen Sie die Szenarien, wie in der folgenden Tabelle aufgeführt. Beachten Sie, dass in der Tabelle die Standardinstallationspfade für OSC-Anbieter-DLLs aufgeführt sind. Benutzer können anpassen, wo sie diese DLLs installieren.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Microsoft Outlook 2013 auf dem Clientcomputer installiert ist.  <br/> |Anbieter-DLLs werden im Office15-Ordner bereitgestellt. Wenn das Betriebssystem 64-Bit und Microsoft Outlook 2013 32-Bit ist, werden die 32-Bit-DLLs unter "C:\Program Files (x86)\Microsoft Office\Office15" bereitgestellt. Wenn das Betriebssystem 64-Bit und Microsoft Outlook 2013 64-Bit ist, werden die 64-Bit-DLLs unter "C:\Programme\Microsoft Office\Office15" bereitgestellt. Wenn das Betriebssystem 32-Bit ist, werden DLLs unter "C:\Programme\Microsoft Office\Office15" bereitgestellt.  <br/> |
|Outlook 2010 wird auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden im Office14-Ordner bereitgestellt. Wenn das Betriebssystem 64-Bit und Outlook 2010 32-Bit ist, werden die 32-Bit-DLLs unter "C:\Programme (x86)\Microsoft Office\Office14" bereitgestellt. Wenn das Betriebssystem 64-Bit und Outlook 2010 64-Bit ist, werden die 64-Bit-DLLs unter "C:\Programme\Microsoft Office\Office14" bereitgestellt. Wenn das Betriebssystem 32-Bit ist, werden DLLs unter "C:\Programme\Microsoft Office\Office14" bereitgestellt.  <br/> |
|Outlook 2007 wird auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden unter "C:\Programme\Microsoft Office\Office14" bereitgestellt. Beim Installieren des OSC wird der Office14-Ordner erstellt, und der OSC sollte vor allen Anbieter-DLLs installiert werden. Siehe den vorherigen Abschnitt [Anwesenheit von Outlook und osc auf Clientcomputer](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 wird auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden unter "C:\Programme\Microsoft Office\Office14" bereitgestellt. Beim Installieren des OSC wird der Office14-Ordner erstellt, und der OSC sollte vor allen Anbieter-DLLs installiert werden. Siehe den vorherigen Abschnitt [Anwesenheit von Outlook und osc auf Clientcomputer](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 wird nicht installiert, aber per Klick-und-Los auf dem Clientcomputer bereitgestellt.  <br/> |Anbieter-DLLs werden im Office15-Ordner bereitgestellt. Wenn das Betriebssystem 64-Bit ist, werden 32-Bit-DLLs unter "C:\Program Files (x86)\Microsoft Office\Office15 or C:\Program Files\Microsoft Office\Office15" bereitgestellt. Wenn das Betriebssystem 32-Bit ist, werden DLLs unter "C:\Programme\Microsoft Office\Office15" bereitgestellt. Wenn der Office15-Ordner nicht vorhanden ist, erstellt die Installation den Ordner.  <br/> |
|Outlook 2010 wird nicht installiert, sondern per Klick-und-Los auf dem Clientcomputer bereitgestellt.  <br/> |Anbieter-DLLs werden im Office14-Ordner bereitgestellt. Wenn das Betriebssystem 64-Bit ist, werden 32-Bit-DLLs unter "C:\Program Files (x86)\Microsoft Office\Office14 or C:\Program Files\Microsoft Office\Office14" bereitgestellt. Wenn das Betriebssystem 32-Bit ist, werden DLLs unter "C:\Programme\Microsoft Office\Office14" bereitgestellt. Wenn der Office14-Ordner nicht vorhanden ist, erstellt die Installation den Ordner.  <br/> |
   
### <a name="windows-registry-locations"></a>Windows Registrierungsspeicherorte

Überprüfen Sie Folgendes:
  
- Das OSC-Anbieterinstallationsprogramm erstellt einen ProgID-Wert für den OSC-Anbieter in der Windows-Registrierung, entweder `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` oder `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` . 
    
- Die Ausnahme ist, wenn der Clientcomputer 32-Bit-Outlook auf einem 64-Bit-Windows Betriebssystem ausgeführt wird. In diesem Fall wird die ProgID entweder  `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` oder  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` erstellt.
    
- Die Registrierungsschlüssel sollten identisch und am selben Speicherort sein, wenn die DLLs stattdessen von regsvr32.exe registriert werden.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Entfernen der Installation

Es folgen einige Tests, um sicherzustellen, dass der Deinstallationsprozess für Ihren OSC-Anbieter ordnungsgemäß funktioniert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Der Benutzer entscheidet sich für die Deinstallation des Anbieters.  <br/> |Der Anbieter deinstalliert die DLLs und löscht die Registrierung.  <br/> |
|Der Benutzer entscheidet sich, den Deinstallationsprozess des Anbieters abzubrechen.  <br/> |Der Anbieter bricht den Deinstallationsprozess ab und versetzt den Benutzer wieder in den Zustand, bevor der Deinstallationsprozess gestartet wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Anbieters](registering-a-provider.md)  
- [Prüfliste für die Installation](installation-checklist.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

