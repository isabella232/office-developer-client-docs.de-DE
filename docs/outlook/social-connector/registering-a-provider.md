---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden die Windows-Registrierungsspeicherorte beschrieben, die bei der Installation eines Outlook Social Connector-Anbieters (OSC) verwendet werden.
ms.openlocfilehash: a5f76850f9bebcba3c2bff31e799a3b012d6b91a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329211"
---
# <a name="registering-a-provider"></a>Registrieren eines Providers

In diesem Thema werden die Windows-Registrierungsspeicherorte beschrieben, die bei der Installation eines Outlook Social Connector-Anbieters (OSC) verwendet werden.
  
## <a name="com-registration"></a>COM-Registrierung

Sie müssen die OSC-Anbieter-DLL so konfigurieren, dass Sie die COM-Self-Registration oder regsvr32 während der Installation registriert. Die COM-Registrierung der Anbieter-DLL registriert den OSC- `HKEY_CLASSES_ROOT` Anbieter unter der Registrierungsstruktur. 
  
Ein in verwaltetem Code entwickelter OSC-Anbieter verfügt über eine COM-sichtbare Anbieter Assembly. Sie sollten eine separate Anwendungsdomäne für die Anbieterkomponente verwenden. Andernfalls verwendet der OSC-Anbieter die standardmäßige freigegebene Anwendungsdomäne, die von anderen Komponenten verwendet wird, und der Anbieter funktioniert möglicherweise nicht wie erwartet.
  
## <a name="registering-provider-progid"></a>Registrieren der Anbieter-ProgID

Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner (`ProgID`) registrieren. Das Installationsprogramm des Anbieters kann einen der folgenden Speicherorte auswählen `ProgID`:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Ihr Anbieter Installationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter nur für den derzeit angemeldeten Benutzer installiert ist.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Ihr Anbieter Installationsprogramm sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.
    
Der OSC sucht in den oben `ProgID` genannten Speicherorten nach dem Anbieter, es sei denn, der Clientcomputer hat 32-Bit Outlook auf einem 64-Bit-Windows-Betriebssystem ausgeführt. In diesem Fall sollte das Installationsprogramm des Anbieters eine der folgenden Speicherorte in der `HKEY_CURRENT_USER` oder `HKEY_LOCAL_MACHINE` -Struktur auswählen: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Bei einer Klick-und-Los-Version von Office sollte das Installationsprogramm eines der folgenden Speicherorte in der Struktur HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE wählen:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Siehe auch

- [PrüfListe für die Installation](installation-checklist.md)
- [Schnelle Schritte für die Entwicklung eines Anbieters](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

