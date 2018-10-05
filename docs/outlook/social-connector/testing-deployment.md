---
title: Testen der Bereitstellung
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b585200-33e7-4607-a603-0c7e52a6b09d
description: In diesem Thema werden einige Szenarien, die zur Installation und Deinstallation von einem Anbieter Outlook Social Connector (OSC) für getestet werden soll.
ms.openlocfilehash: 9c811683097a08b9f6e575d4ea2fee29cdd545d6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383934"
---
# <a name="testing-deployment"></a>Testen der Bereitstellung

In diesem Thema werden einige Szenarien, die zur Installation und Deinstallation von einem Anbieter Outlook Social Connector (OSC) für getestet werden soll.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="presence-of-outlook-and-the-osc-on-client-computer"></a>Vorhandensein von Outlook und der OSC auf Clientcomputer

Faktoren beeinflussen Installieren eines OSC-Anbieters enthält die Bitness der das Betriebssystem, das Vorhandensein und Bitness von Outlook und der OSC an, die in Outlook aktiviert.
  
Ein OSC-Anbieter kann für eine 32-Bit oder 64-Bit-Version von der OSC geschrieben werden. Outlook 2010 und Outlook 2013 32-Bit- und 64-Bit-Versionen verfügbar sind, und Office Outlook 2003 und Office Outlook 2007 sind nur 32-Bit-Versionen verfügbar. Auf einem 64-Bit-Windows-Betriebssystem können Sie die 32-Bit oder 64-Bit-Outlook installieren. Auf einem 32-Bit-Betriebssystem, können Sie aber nicht nur 32-Bit, installieren 64-Bit, Outlook. Je nach der Bitness der installierten Version von Outlook und die OSC-Anbieter selbst sollte der Benutzer das entsprechende Installationsprogramm verwenden, um ein OSC-Anbieter von der entsprechenden Bitness zu installieren. Beispielsweise wenn 64-Bit-Outlook installiert ist, und der OSC-Anbieter eine systemeigene COM-Komponente ist, ein 32-Bit-OSC-Anbieter funktionieren nicht, und der Benutzer muss das entsprechende Installationsprogramm verwenden, um einen 64-Bit-OSC-Anbieter zu installieren.
  
Der Bereitstellungscode Ihres OSC-Anbieters kann davon ausgehen, dass der Benutzer eine unterstützte Version von Outlook auf dem Computer verfügt. Jedoch ist die aktuelle Version von OSC nicht auf dem Clientcomputer, Ihre Bereitstellungscode herunterladen und installieren kann eine geeignete Version von der OSC mithilfe von speziell gestalteten g-Link URLs auf https://g.live.com. Diese g-Links hängen von der Version und Bitness von Outlook und das Gebietsschema des Clientcomputers ab. Weitere Informationen zur Verwendung von g Links zum Installieren oder aktualisieren das osc bilden finden Sie unter [Installationsprüfliste](installation-checklist.md).
  
Vor der Installation von einem OSC-Anbieter, sollten der Outlook-Benutzer des OSC-add-Ins in Outlook aktiviert ist.
  
Die empfohlene Methode für das Bereitstellen einer OSC-Providers ist die Verwendung von Windows Installer (MSI)-Paket. Testen Sie alle der folgenden Szenarien Ablauf der inhaltsbereitstellung entsprechend für den Anbieter überprüfen.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Outlook ist nicht vorhanden – Outlook 2003 oder Outlook 2007 nicht installiert ist, und Outlook 2010 oder Microsoft Outlook 2013 ist nicht installiert, noch er übermittelt wurde per Klick-und-los.  <br/> |Die Bereitstellung schlägt fehl.  <br/> |
|Outlook 2003 oder Outlook 2007 nicht installiert ist, aber Outlook 2010 oder Microsoft Outlook 2013 per Klick-und-Los übermittelt wurde.  <br/> |Der 32-Bit-Anbieter bereitgestellt wird.  <br/> |
|Outlook 2003 oder Outlook 2007 installiert ist, aber die OSC ist nicht installiert.  <br/> |Das Installationsprogramm installiert die OSC und alle Patches. Nachdem die OSC erfolgreich installiert wurde, wird das Installationsprogramm den Anbieter bereitgestellt.  <br/> |
|Outlook 2003 oder Outlook 2007 installiert ist, und eine frühere Version von der OSC installiert ist.  <br/> |Das Installationsprogramm der OSC über einen g-Link auf Patches, aktualisiert und anschließend den Anbieter.  <br/> |
|Outlook 2003 oder 2007 installiert ist und die OSC ist auf dem neuesten Stand.  <br/> |Das Installationsprogramm wird den 32-Bit-Anbieter bereitgestellt.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 ist installiert, aber die OSC ist nicht installiert.  <br/> |Das Installationsprogramm schlägt fehl und eine entsprechende Fehlermeldung angezeigt.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert ist und das osc bilden eine ältere Version installiert ist.  <br/> |Das Installationsprogramm für die Bitness der installierten Outlook 2010 oder Microsoft Outlook 2013 geeignet ist die OSC über den g-Link wird aktualisiert und Patches und anschließend den entsprechenden Anbieter.  <br/> |
|Outlook 2010 oder Microsoft Outlook 2013 installiert ist und die OSC ist auf dem neuesten Stand.  <br/> |Das Installationsprogramm, das für die Bitness der installierten Outlook 2010 oder Microsoft Outlook 2013 (32-Bit oder 64-Bit) geeignet ist, wird den entsprechenden Anbieter bereitgestellt.  <br/> |

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="installed-location-and-registry-keys"></a>Installierte Speicherort und Registrierung Schlüssel

Überprüfen Sie den Speicherort der Datei, in dem der OSC-Anbieter bereitgestellt wurde, und die Speicherorte in der Windows-Registrierung in dem Registrierungsschlüssel für den Anbieter erstellt werden.
  
### <a name="file-location-for-osc-provider-dlls"></a>Speicherort für OSC-Provider-DLLs

Testen Sie für die Szenarien, wie in der folgenden Tabelle aufgeführt. Beachten Sie, dass die Tabelle die standardmäßigen Installationspfade für OSC-Anbieter-DLLs enthält. Benutzer können anpassen, von denen diese DLLs installiert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Microsoft Outlook 2013 ist auf dem Clientcomputer installiert.  <br/> |Provider-DLLs werden in den Ordner Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit ist- und Microsoft Outlook 2013 32-Bit ist, werden die 32-Bit-DLLs unter c:\Programme\Gemeinsame Dateien (x86) \Microsoft Office\Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit ist- und Microsoft Outlook 2013 64-Bit ist, werden die 64-Bit-DLLs unter C:\Program Files\Microsoft Office\Office15 bereitgestellt. Wenn das Betriebssystem 32-Bit-Version ist, werden unter C:\Program Files\Microsoft Office\Office15 DLLs bereitgestellt.  <br/> |
|Outlook 2010 wird auf dem Clientcomputer installiert.  <br/> |Provider-DLLs werden in den Ordner Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit ist- und Outlook 2010 32-Bit-Version ist, werden die 32-Bit-DLLs unter c:\Programme\Gemeinsame Dateien (x86) \Microsoft Office\Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit ist- und Outlook 2010 64-Bit-Version ist, werden die 64-Bit-DLLs unter c:\Programme\Microsoft Office\Office14 bereitgestellt. Wenn das Betriebssystem 32-Bit-Version ist, werden unter c:\Programme\Microsoft Office\Office14 DLLs bereitgestellt.  <br/> |
|Outlook 2007 ist auf dem Clientcomputer installiert.  <br/> |Provider-DLLs werden unter c:\Programme\Microsoft Office\Office14 bereitgestellt. Installieren der OSC der Office14 Ordner erstellt, und der OSC vor jedem Provider DLLs installiert werden soll. Finden Sie im vorherigen Abschnitt [Anwesenheit von Outlook und der OSC auf dem Clientcomputer vorhanden](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Outlook 2003 wird auf dem Clientcomputer installiert.  <br/> |Provider-DLLs werden unter c:\Programme\Microsoft Office\Office14 bereitgestellt. Installieren der OSC der Office14 Ordner erstellt, und der OSC vor jedem Provider DLLs installiert werden soll. Finden Sie im vorherigen Abschnitt [Anwesenheit von Outlook und der OSC auf dem Clientcomputer vorhanden](#olosc_TestingDeployment_PresenceOfOutlook).  <br/> |
|Microsoft Outlook 2013 ist nicht installiert, aber von Klick-und-Los auf dem Clientcomputer bereitgestellt.  <br/> |Provider-DLLs werden in den Ordner Office15 bereitgestellt. Wenn das Betriebssystem 64-Bit-, 32-Bit ist sind DLLs unter c:\Programme\Gemeinsame Dateien (x86) \Microsoft Office\Office15 oder C:\Program Files\Microsoft Office\Office15 bereitgestellt. Wenn das Betriebssystem 32-Bit-Version ist, werden unter C:\Program Files\Microsoft Office\Office15 DLLs bereitgestellt. Wenn der Office15 Ordner nicht vorhanden ist, wird die Installation der Ordner erstellt.  <br/> |
|Outlook 2010 ist nicht installiert, aber von Klick-und-Los auf dem Clientcomputer bereitgestellt.  <br/> |Provider-DLLs werden in den Ordner Office14 bereitgestellt. Wenn das Betriebssystem 64-Bit-, 32-Bit ist sind DLLs unter c:\Programme\Gemeinsame Dateien (x86) \Microsoft Office\Office14 oder c:\Programme\Microsoft Office\Office14 bereitgestellt. Wenn das Betriebssystem 32-Bit-Version ist, werden unter c:\Programme\Microsoft Office\Office14 DLLs bereitgestellt. Wenn der Office14 Ordner nicht vorhanden ist, wird die Installation der Ordner erstellt.  <br/> |
   
### <a name="windows-registry-locations"></a>Speicherorte der Windows-Registrierung

Überprüfen Sie Folgendes:
  
- Das OSC-Anbieter-Installationsprogramm erstellt einen Programm-ID-Wert für den OSC-Anbieter in der Windows-Registrierung in einem `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` oder `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`. 
    
- Die Ausnahme ist, wenn es sich bei dem Clientcomputer 32-Bit-Outlook auf einem 64-Bit-Windows-Betriebssystem ausgeführt wird. In diesem Fall wird die ProgID erstellt, in einem `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders` oder `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
- Der Registrierungsschlüssel sollten identisch sein und am selben Speicherort, wenn Sie stattdessen die DLLs von regsvr32.exe registriert sind.

<a name="olosc_TestingDeployment_PresenceOfOutlook"> </a>

## <a name="removing-the-installation"></a>Entfernen der installation

Es folgen einige Tests, um sicherzustellen, dass während des Deinstallationsvorgangs für Ihr OSC-Anbieter ordnungsgemäß funktioniert.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Der Benutzer entscheidet, deinstallieren Sie den Anbieter.  <br/> |Der Anbieter die DLLs deinstalliert und die Registrierung gelöscht.  <br/> |
|Der Benutzer entscheidet, die Deinstallation des Anbieters abzubrechen.  <br/> |Der Anbieter wird während des Deinstallationsvorgangs aufgehoben und den Benutzer auf den Zustand vor der Deinstallation gestartet wird.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Registrieren eines Providers](registering-a-provider.md)  
- [Checkliste für Installation](installation-checklist.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

