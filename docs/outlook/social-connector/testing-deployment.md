---
title: Testen der Bereitstellung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: In diesem Thema werden einige Szenarien beschrieben, die Sie testen sollten, um einen Anbieter Outlook Social Connector (OSC) zu installieren und zu deinstallieren.
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329162"
---
# <a name="testing-deployment"></a>Testen der Bereitstellung

In diesem Thema werden einige Szenarien beschrieben, die Sie testen sollten, um einen Anbieter Outlook Social Connector (OSC) zu installieren und zu deinstallieren.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Vorhandensein von Outlook und der OSC auf dem Clientcomputer

Faktoren, die sich auf die Installation eines OsC-Anbieters auswirken, umfassen die Bitität des Betriebssystems, das Vorhandensein und die Bitität von Outlook und die osC, die in der Outlook.
  
Ein OSC-Anbieter kann für eine 32-Bit- oder 64-Bit-Version des Betriebssystems geschrieben werden. Outlook 2010 und Outlook 2013 sind sowohl in 32-Bit- als auch in 64-Bit-Versionen verfügbar, und Office Outlook 2003 und Office Outlook 2007 sind nur in 32-Bit-Versionen verfügbar. Unter einem 64-Bit-Windows können Sie entweder 32-Bit- oder 64-Bit-Outlook. Unter einem 32-Bit-Betriebssystem können Sie nur 32-Bit-, aber keine 64-Bit-Outlook. Abhängig von der Bitität der installierten Version von Outlook und des OSC-Anbieters selbst sollte der Benutzer das entsprechende Installationsprogramm verwenden, um einen OSC-Anbieter mit der entsprechenden Bitität zu installieren. Wenn beispielsweise 64-Bit-Outlook installiert ist und der OSC-Anbieter eine systemeigene COM-Komponente ist, funktioniert ein 32-Bit-OSC-Anbieter nicht, und der Benutzer muss das entsprechende Installationsprogramm verwenden, um einen 64-Bit-OSC-Anbieter zu installieren.
  
Der Bereitstellungscode Ihres OSC-Anbieters kann davon ausgehen, dass der Benutzer über eine unterstützte Outlook auf dem Computer verfügt. Wenn sich die aktuelle Version von OSC jedoch nicht auf dem Clientcomputer befindet, kann Ihr Bereitstellungscode eine entsprechende Version des BETRIEBSSYSTEMS herunterladen und installieren, indem sie speziell konstruierte g-link-URLs auf https://g.live.com verwendet. Diese g-Links hängen von der Version und Bitität der Outlook und dem Locale des Clientcomputers ab. Weitere Informationen zum Verwenden von g-Links zum Installieren oder Aktualisieren des Betriebssystems finden Sie unter [Installationscheckliste](installation-checklist.md).
  
Vor der Installation eines OSC-Anbieters sollte Outlook Benutzer sicherstellen, dass das OSC-Add-In in der Outlook.
  
Die empfohlene Methode für die Bereitstellung eines OSC-Anbieters ist die Verwendung eines Windows Installer (.msi). Testen Sie jedes der folgenden Szenarien, um zu überprüfen, ob die Bereitstellung für den Anbieter geeignet ist.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Outlook ist nicht vorhanden – Outlook 2003 oder Outlook 2007 ist nicht installiert, und Outlook 2010 oder Microsoft Outlook 2013 ist nicht installiert oder wurde von Click-to-Run zugestellt.  <br/> |Die Bereitstellung schlägt fehl.  <br/> |
|Outlook 2003 oder Outlook 2007 ist nicht installiert, aber Outlook 2010 oder Microsoft Outlook 2013 wurde von Click-to-Run zugestellt.  <br/> |Der 32-Bit-Anbieter wird bereitgestellt.  <br/> |
|Outlook 2003 oder Outlook 2007 ist installiert, das Betriebssystem ist jedoch nicht installiert.  <br/> |Das Installationsprogramm installiert das OSC und alle Patches. Nachdem das Betriebssystem erfolgreich installiert wurde, stellt das Installationsprogramm den Anbieter zur Bereitstellung.  <br/> |
|Outlook 2003 oder Outlook 2007 installiert, und eine frühere Version des Betriebssystems ist installiert.  <br/> |Das Installationsprogramm aktualisiert das BETRIEBSSYSTEM über einen g-Link zu Patches und stellt dann den Anbieter zur Verfügung.  <br/> |
|Outlook 2003 oder 2007 ist installiert, und das Betriebssystem ist auf dem neuesten Stand.  <br/> |Das Installationsprogramm stellt den 32-Bit-Anbieter zur Bereitstellung.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert, aber das Betriebssystem ist nicht installiert.  <br/> |Das Installationsprogramm schlägt mit einer entsprechenden Fehlermeldung fehl.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert und eine ältere Version des Betriebssystems installiert.  <br/> |Das Installationsprogramm, das für die Bitkraft des installierten Outlook 2010 oder Microsoft Outlook 2013 geeignet ist, aktualisiert das Betriebssystem über den g-Link auf Patches und stellt dann den entsprechenden Anbieter zur Verfügung.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert, und das Betriebssystem ist auf dem neuesten Stand.  <br/> |Das Installationsprogramm, das für die Bitität des installierten Outlook 2010 oder Microsoft Outlook 2013 (32-Bit oder 64-Bit) geeignet ist, stellt den entsprechenden Anbieter zur Bereitstellung.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Installierter Speicherort und Registrierungsschlüssel

Überprüfen Sie den Dateispeicherort, an dem Ihr OsC-Anbieter bereitgestellt wurde, und die Speicherorte in der Windows, an denen Registrierungsschlüssel für Ihren Anbieter erstellt werden.
  
### <a name="file-location-for-osc-provider-dlls"></a>Dateispeicherort für OSC-Anbieter-DLLs

Testen Sie die Szenarien, wie in der folgenden Tabelle aufgeführt. Beachten Sie, dass in der Tabelle die Standardinstallationspfade für OSC-Anbieter-DLLs aufgeführt sind. Benutzer können anpassen, wo sie diese DLLs installieren.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Microsoft Outlook 2013 auf dem Clientcomputer installiert ist.  <br/> |Anbieter-DLLs werden im Ordner Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit und Microsoft Outlook 2013 32-Bit hat, werden die 32-Bit-DLLs unter C:\Program Files (x86)\Microsoft Office\Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit und Microsoft Outlook 2013 64-Bit hat, werden die 64-Bit-DLLs unter C:\Programme\Microsoft Office\Office15 bereitgestellt. Wenn das Betriebssystem 32-Bit hat, werden DLLs unter C:\Program Files\Microsoft Office\Office15 bereitgestellt.  <br/> |
|Outlook 2010 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden im Ordner Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit hat und Outlook 2010 32-Bit hat, werden die 32-Bit-DLLs unter C:\Program Files (x86)\Microsoft Office\Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit hat und Outlook 2010 64-Bit hat, werden die 64-Bit-DLLs unter C:\Programme\Microsoft Office\Office14 bereitgestellt. Wenn das Betriebssystem 32-Bit hat, werden DLLs unter C:\Program Files\Microsoft Office\Office14 bereitgestellt.  <br/> |
|Outlook 2007 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden unter C:\Programme\Microsoft Office\Office14 bereitgestellt. Beim Installieren des OSC wird der Ordner Office14 erstellt, und das OSC sollte vor beliebigen Anbieter-DLLs installiert werden. Siehe den vorherigen Abschnitt [Anwesenheit von Outlook und osC auf Clientcomputer](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden unter C:\Programme\Microsoft Office\Office14 bereitgestellt. Beim Installieren des OSC wird der Ordner Office14 erstellt, und das OSC sollte vor beliebigen Anbieter-DLLs installiert werden. Siehe den vorherigen Abschnitt [Anwesenheit von Outlook und osC auf Clientcomputer](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 wird nicht installiert, aber von Klick-und-Ausführen auf dem Clientcomputer zugestellt.  <br/> |Anbieter-DLLs werden im Ordner Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit hat, werden 32-Bit-DLLs unter C:\Program Files (x86)\Microsoft Office\Office15 oder C:\Program Files\Microsoft Office\Office15 bereitgestellt. Wenn das Betriebssystem 32-Bit hat, werden DLLs unter C:\Program Files\Microsoft Office\Office15 bereitgestellt. Wenn der Ordner Office15 nicht vorhanden ist, erstellt die Installation den Ordner.  <br/> |
|Outlook 2010 wird nicht installiert, aber von Klick-und-Ausführen auf dem Clientcomputer zugestellt.  <br/> |Anbieter-DLLs werden im Ordner Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit hat, werden 32-Bit-DLLs unter C:\Program Files (x86)\Microsoft Office\Office14 oder C:\Program Files\Microsoft Office\Office14 bereitgestellt. Wenn das Betriebssystem 32-Bit hat, werden DLLs unter C:\Program Files\Microsoft Office\Office14 bereitgestellt. Wenn der Ordner Office14 nicht vorhanden ist, erstellt die Installation den Ordner.  <br/> |
   
### <a name="windows-registry-locations"></a>Windows Registrierungsstandorte

Überprüfen Sie Folgendes:
  
- Das Installationsprogramm des OSC-Anbieters erstellt einen ProgID-Wert für den OSC-Anbieter in der Windows in oder `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` . 
    
- Die Ausnahme ist, wenn auf dem Clientcomputer 32-Bit-Outlook unter einem 64-Bit-Windows ausgeführt wird. In diesem Fall wird die ProgID entweder oder  `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` erstellt.
    
- Die Registrierungsschlüssel sollten identisch und am gleichen Speicherort sein, wenn stattdessen die DLLs von der regsvr32.exe.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Entfernen der Installation

Im Folgenden finden Sie einige Tests, um zu überprüfen, ob der Deinstallationsvorgang für Ihren OSC-Anbieter ordnungsgemäß funktioniert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Der Benutzer wählt, den Anbieter zu deinstallieren.  <br/> |Der Anbieter deinstalliert die DLLs und deaktiviert die Registrierung.  <br/> |
|Der Benutzer bricht den Deinstallationsprozess des Anbieters ab.  <br/> |Der Anbieter bricht den Deinstallationsvorgang ab und führt den Benutzer zurück in den Status, bevor der Deinstallationsvorgang gestartet wurde.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Anbieters](registering-a-provider.md)  
- [Prüfliste für die Installation](installation-checklist.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

