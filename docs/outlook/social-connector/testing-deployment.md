---
title: Testen der Bereitstellung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: In diesem Thema werden einige Szenarien beschrieben, die Sie hinsichtlich der Installation und Deinstallation eines OSC-Anbieters (Outlook Social Connector) testen sollten.
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329162"
---
# <a name="testing-deployment"></a>Testen der Bereitstellung

In diesem Thema werden einige Szenarien beschrieben, die Sie hinsichtlich der Installation und Deinstallation eines OSC-Anbieters (Outlook Social Connector) testen sollten.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Anwesenheit von Outlook und des OSC auf dem Clientcomputer

Zu den Faktoren, die sich auf die Installation eines OSC-Anbieters auswirken, gehören die Bitanzahl des Betriebssystems, der Anwesenheits-und Bitanzahl von Outlook und der OSC, der in Outlook aktiviert wird.
  
Ein OSC-Anbieter kann für eine 32-Bit-oder 64-Bit-Version des OSC geschrieben werden. Outlook 2010 und Outlook 2013 sind sowohl in 32-Bit-als auch in 64-Bit-Versionen verfügbar, und Office Outlook 2003 und Office Outlook 2007 sind nur in 32-Bit-Versionen verfügbar. Bei einem 64-Bit-Windows-Betriebssystem können Sie entweder 32-Bit oder 64-Bit Outlook installieren. Bei einem 32-Bit-Betriebssystem können Sie nur 32-Bit, aber nicht 64-Bit, Outlook installieren. Je nach Bitanzahl der installierten Version von Outlook und des OSC-Anbieters selbst sollte der Benutzer das entsprechende Installationsprogramm verwenden, um einen OSC-Anbieter der entsprechenden Bitanzahl zu installieren. Wenn beispielsweise 64-Bit Outlook installiert ist und der OSC-Anbieter eine systemeigene COM-Komponente ist, kann ein 32-Bit-OSC-Anbieter nicht funktionieren, und der Benutzer muss das entsprechende Installationsprogramm verwenden, um einen 64-Bit OSC-Anbieter zu installieren.
  
Der Bereitstellungscode des OSC-Anbieters kann davon ausgehen, dass der Benutzer eine unterstützte Version von Outlook auf dem Computer hat. Wenn sich die aktuelle Version von OSC jedoch nicht auf dem Clientcomputer befindet, kann Ihr Bereitstellungscode eine entsprechende Version des OSC herunterladen und installieren, indem Sie speziell erstellte g-Link https://g.live.com-URLs verwenden. Diese g-Links hängen von der Version und Bitanzahl von Outlook und dem Gebietsschema des Clientcomputers ab. Weitere Informationen zur Verwendung von g-Links zum Installieren oder Aktualisieren des OSC finden Sie unter [Installationscheckliste](installation-checklist.md).
  
Vor der Installation eines OSC-Anbieters sollte der Outlook-Benutzer sicherstellen, dass das OSC-Add-in in Outlook aktiviert ist.
  
Die empfohlene Methode zur Bereitstellungeines OSC-Anbieters ist die Verwendung eines Windows Installer-Pakets (. msi). Testen Sie jedes der folgenden Szenarien, um zu überprüfen, ob die Bereitstellung für den Anbieter geeignet ist.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Outlook ist nicht vorhanden – Outlook 2003 oder Outlook 2007 ist nicht installiert, und Outlook 2010 oder Microsoft Outlook 2013 ist nicht installiert und wurde nicht per Klick-und-Los geliefert.  <br/> |Die Bereitstellung schlägt fehl.  <br/> |
|Outlook 2003 oder Outlook 2007 ist nicht installiert, aber Outlook 2010 oder Microsoft Outlook 2013 wurde von Klick-und-Los bereitgestellt.  <br/> |Der 32-Bit-Anbieter wird bereitgestellt.  <br/> |
|Outlook 2003 oder Outlook 2007 ist installiert, aber OSC ist nicht installiert.  <br/> |Das Installationsprogramm installiert OSC und alle Patches. Nachdem der OSC erfolgreich installiert wurde, stellt das Installationsprogramm den Anbieter bereit.  <br/> |
|Outlook 2003 oder Outlook 2007 ist installiert, und eine frühere Version des OSC ist installiert.  <br/> |Das Installationsprogramm aktualisiert den OSC über einen g-Link zu Patches und stellt dann den Anbieter bereit.  <br/> |
|Outlook 2003 oder 2007 ist installiert, und der OSC ist auf dem neuesten Stand.  <br/> |Das Installationsprogramm stellt den 32-Bit-Anbieter bereit.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 ist installiert, aber der OSC ist nicht installiert.  <br/> |Das Installationsprogramm schlägt mit einer entsprechenden Fehlermeldung fehl.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 wird installiert, und es wird eine ältere Version des OSC installiert.  <br/> |Das Installationsprogramm, das für die Bitanzahl der installierten Outlook 2010 oder Microsoft Outlook 2013 geeignet ist, aktualisiert den OSC über den g-Link zu Patches und stellt dann den entsprechenden Anbieter bereit.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 ist installiert, und der OSC ist auf dem neuesten Stand.  <br/> |Das Installationsprogramm, das für die Bitanzahl der installierten Outlook 2010-oder Microsoft Outlook 2013 (32-Bit oder 64-Bit) geeignet ist, stellt den entsprechenden Anbieter bereit.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Installierter Speicherort und Registrierungsschlüssel

Überprüfen Sie den Dateispeicherort des OSC-Anbieters und die Speicherorte in der Windows-Registrierung, in denen Registrierungsschlüssel für Ihren Anbieter erstellt werden.
  
### <a name="file-location-for-osc-provider-dlls"></a>Dateispeicherort für OSC-Anbieter-DLLs

Testen Sie die in der folgenden Tabelle aufgeführten Szenarien. Beachten Sie, dass in der Tabelle die Standardinstallationspfade für OSC-Anbieter-DLLs aufgeführt sind. Benutzer können anpassen, wo Sie diese DLLs installieren.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Microsoft Outlook 2013 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden im Ordner Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit ist und Microsoft Outlook 2013 32-Bit ist, werden die 32-Bit-DLLs unter C:\Program Files (x86) \Microsoft Office\Office15. bereitgestellt. Wenn das Betriebssystem 64-Bit ist und Microsoft Outlook 2013 64-Bit ist, werden die 64-Bit-DLLs unter C:\Programme\Microsoft Office\Office15. Wenn das Betriebssystem 32-Bit lautet, werden DLLs unter C:\Programme\Microsoft Office\Office15.  <br/> |
|Outlook 2010 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden im Ordner Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit ist und Outlook 2010 32-Bit ist, werden die 32-Bit-DLLs unter C:\Program Files (x86) \Microsoft Office\Office14. bereitgestellt. Wenn das Betriebssystem 64-Bit ist und Outlook 2010 64-Bit ist, werden die 64-Bit-DLLs unter C:\Programme\Microsoft Office\Office14. Wenn das Betriebssystem 32-Bit lautet, werden DLLs unter C:\Programme\Microsoft Office\Office14.  <br/> |
|Outlook 2007 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden unter C:\Programme\Microsoft Office\Office14. Bei der Installation von OSC wird der Office14-Ordner erstellt, und der OSC sollte vor allen Anbieter-DLLs installiert werden. Weitere Informationen finden Sie im vorherigen Abschnitt [Anwesenheit von Outlook und des osc auf dem Client Computer](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 ist auf dem Clientcomputer installiert.  <br/> |Anbieter-DLLs werden unter C:\Programme\Microsoft Office\Office14. Bei der Installation von OSC wird der Office14-Ordner erstellt, und der OSC sollte vor allen Anbieter-DLLs installiert werden. Weitere Informationen finden Sie im vorherigen Abschnitt [Anwesenheit von Outlook und des osc auf dem Client Computer](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 wird nicht installiert, sondern per Klick-und-Los auf dem Clientcomputer bereitgestellt.  <br/> |Anbieter-DLLs werden im Ordner Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit lautet, werden 32-Bit-DLLs unter C:\Program Files (x86) \Microsoft Office\Office15 oder C:\Programme\Microsoft Office\Office15. bereitgestellt. Wenn das Betriebssystem 32-Bit lautet, werden DLLs unter C:\Programme\Microsoft Office\Office15. Wenn der Office15-Ordner nicht vorhanden ist, wird der Ordner von der Installation erstellt.  <br/> |
|Outlook 2010 wird nicht installiert, sondern per Klick-und-Los auf dem Clientcomputer bereitgestellt.  <br/> |Anbieter-DLLs werden im Ordner Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit lautet, werden 32-Bit-DLLs unter C:\Program Files (x86) \Microsoft Office\Office14 oder C:\Programme\Microsoft Office\Office14. bereitgestellt. Wenn das Betriebssystem 32-Bit lautet, werden DLLs unter C:\Programme\Microsoft Office\Office14. Wenn der Office14-Ordner nicht vorhanden ist, wird der Ordner von der Installation erstellt.  <br/> |
   
### <a name="windows-registry-locations"></a>Windows-Registrierungsspeicherorte

Überprüfen Sie Folgendes:
  
- Das OSC-Anbieter-Installationsprogramm erstellt einen ProgID-Wert für den OSC-Anbieter in der `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` Windows `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`-Registrierung in oder. 
    
- Die Ausnahme ist, wenn auf dem Clientcomputer 32-Bit-Outlook unter einem 64-Bit-Windows-Betriebssystem ausgeführt wird. In diesem Fall wird die ProgID in `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` oder `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`erstellt.
    
- Die Registrierungsschlüssel sollten identisch und am selben Speicherort sein, wenn stattdessen die DLLs von regsvr32. exe registriert werden.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Entfernen der Installation

Im folgenden finden Sie einige Tests, um zu überprüfen, ob der Deinstallationsprozess für Ihren OSC-Anbieter ordnungsgemäß funktioniert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Der Benutzer wählt die Deinstallation des Anbieters aus.  <br/> |Der Anbieter deinstalliert die DLLs und löscht die Registrierung.  <br/> |
|Der Benutzer wählt den Deinstallationsvorgang des Anbieters aus.  <br/> |Der Anbieter bricht den Deinstallationsvorgang ab und bringt den Benutzer vor dem Start des Deinstallationsvorgangs in den Zustand zurück.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Anbieters](registering-a-provider.md)  
- [PrüfListe für die Installation](installation-checklist.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

