---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden Windows Registrierungsstandorte beschrieben, die bei der Installation eines Outlook Social Connector (OSC) verwendet werden.
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421760"
---
# <a name="registering-a-provider"></a>Registrieren eines Providers

In diesem Thema werden Windows Registrierungsstandorte beschrieben, die bei der Installation eines Outlook Social Connector (OSC) verwendet werden.
  
## <a name="com-registration"></a>COM-Registrierung

Sie müssen die OSC-Anbieter-DLL so konfigurieren, dass sie sich während der Installation mithilfe der COM-Selbstregistrierung oder regsvr32 registriert. Die COM-Registrierung der Anbieter-DLL registriert den OSC-Anbieter unter der `HKEY_CLASSES_ROOT` Registrierungsstruktur. 
  
Ein in verwalteter Code entwickelter OSC-Anbieter verfügt über eine COM-sichtbare Anbieter-Assembly. Sie sollten eine separate Anwendungsdomäne für die Anbieterkomponente verwenden. Andernfalls verwendet der OSC-Anbieter die standardmäßige freigegebene Anwendungsdomäne, die von anderen Komponenten verwendet wird, und der Anbieter funktioniert möglicherweise nicht wie erwartet.
  
## <a name="registering-provider-progid"></a>Registrieren des Anbieters ProgID

Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner ( `ProgID` ) registrieren. Das Installationsprogramm des Anbieters kann einen der folgenden Speicherorte auswählen, um folgendes hinzuzufügen oder zu `ProgID` entfernen:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Ihr Anbieterinstallationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter nur für den aktuell &ndash; angemeldeten Benutzer installiert ist.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash;Ihr Anbieterinstallationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.
    
Das Betriebssystem sucht an den oben genannten Speicherorten nach dem Anbieter, es sei denn, der Clientcomputer verfügt über `ProgID` 32-Bit-Outlook auf einem 64-Bit-Betriebssystem Windows betriebssystem. In einem solchen Fall sollte Ihr Anbieterinstallationsprogramm einen der folgenden Speicherorte im oder im  `HKEY_CURRENT_USER`  `HKEY_LOCAL_MACHINE` Hive auswählen: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Für eine Klick-und-Aus-Version von Office sollte Ihr Anbieterinstaller einen der folgenden Speicherorte im HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE auswählen:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Siehe auch

- [Prüfliste für die Installation](installation-checklist.md)
- [Schnelle Schritte zum Entwickeln eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

