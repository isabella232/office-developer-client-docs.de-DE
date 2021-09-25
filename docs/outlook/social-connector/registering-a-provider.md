---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden die Windows Registrierungsspeicherorte beschrieben, die bei der Installation eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) verwendet werden.
ms.openlocfilehash: 78f5b102cc5ec50e334aafa4a5fef10c37fa2953
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604055"
---
# <a name="registering-a-provider"></a>Registrieren eines Providers

In diesem Thema werden die Windows Registrierungsspeicherorte beschrieben, die bei der Installation eines OSC-Anbieters (Outlook Connector für soziale Netzwerke) verwendet werden.
  
## <a name="com-registration"></a>COM-Registrierung

Sie müssen die OSC-Anbieter-DLL so konfigurieren, dass sie während der Installation mit com-Selbstregistrierung oder regsvr32 registriert wird. Die COM-Registrierung der Anbieter-DLL registriert den OSC-Anbieter unter der `HKEY_CLASSES_ROOT` Registrierungsstruktur. 
  
Ein OSC-Anbieter, der in verwaltetem Code entwickelt wurde, verfügt über eine COM-sichtbare Anbieterassembly. Sie sollten eine separate Anwendungsdomäne für die Anbieterkomponente verwenden. Andernfalls verwendet der OSC-Anbieter die standardmäßige freigegebene Anwendungsdomäne, die von anderen Komponenten verwendet wird, und der Anbieter funktioniert möglicherweise nicht wie erwartet.
  
## <a name="registering-provider-progid"></a>Registrieren des Anbieters ProgID

Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner ( `ProgID` ) registrieren. Das Anbieter-Installationsprogramm kann einen der folgenden Speicherorte auswählen, um Folgendes hinzuzufügen oder zu `ProgID` entfernen:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;Ihr Anbieterinstallationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter nur für den aktuell angemeldeten Benutzer installiert ist.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;Ihr Anbieterinstallationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.
    
Der OSC sucht `ProgID` an den oben genannten Speicherorten nach dem Anbieter, es sei denn, der Clientcomputer verfügt über 32-Bit-Outlook, die auf einem 64-Bit-Windows Betriebssystem ausgeführt werden. In diesem Fall sollte ihr Anbieterinstallationsprogramm einen der folgenden Speicherorte in der  `HKEY_CURRENT_USER` Struktur  `HKEY_LOCAL_MACHINE` auswählen: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Für eine Klick-und-Los-Version von Office sollte ihr Anbieterinstallationsprogramm einen der folgenden Speicherorte in der Struktur HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE auswählen:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Siehe auch

- [Prüfliste für die Installation](installation-checklist.md)
- [Schnelle Schritte für Learning zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

