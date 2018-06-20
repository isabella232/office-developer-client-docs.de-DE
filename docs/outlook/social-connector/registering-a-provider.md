---
title: Registrieren eines Providers
manager: soliver
ms.date: 03/05/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b60b3634-4c8b-4273-97a0-0a8a5a8a5342
description: In diesem Thema werden die Speicherorte der Windows-Registrierung, die verwendet werden, wenn Sie einen Anbieter für Outlook Social Connector (OSC) installieren.
ms.openlocfilehash: 3ec594ec94b045d2ceb583144781a5746b945b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796075"
---
# <a name="registering-a-provider"></a>Registrieren eines Providers

In diesem Thema werden die Speicherorte der Windows-Registrierung, die verwendet werden, wenn Sie einen Anbieter für Outlook Social Connector (OSC) installieren.
  
## <a name="com-registration"></a>COM-Registrierung

Sie müssen den OSC-Anbieter-DLL zum Registrieren von COM-Self-Registrierung oder regsvr32 während der Installation konfigurieren. COM-Registrierung der Provider-DLL registriert den OSC-Anbieter unter der `HKEY_CLASSES_ROOT` Registrierungsstruktur. 
  
Ein OSC-Anbieter in verwaltetem Code entwickelt hat eine COM-sichtbare Anbieterassembly. Sie sollten eine separate Anwendungsdomäne für die Providerkomponente verwenden. Sie andernfalls der OSC-Anbieter verwendet die Standarddomäne für den freigegebenen Anwendung, die von anderen Komponenten verwendet wird, und der Anbieter funktionieren möglicherweise nicht wie erwartet.
  
## <a name="registering-provider-progid"></a>Provider-ProgID registrieren

Jeder OSC-Anbieter muss einen programmgesteuerten Bezeichner registrieren (`ProgID`). Das Installationsprogramm Anbieter kann wählen Sie eine der folgenden Speicherorte zum Hinzufügen oder Entfernen der `ProgID`:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Das Installationsprogramm der Anbieter sollte diesen Speicherort verwenden, wenn der Anbieter nur für den aktuell angemeldeten Benutzer installiert ist.
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`&ndash; Das Installationsprogramm der Anbieter sollte diesen Speicherort verwenden, wenn der Anbieter für alle Benutzer auf dem Computer installiert ist.
    
Die OSC sucht für den Anbieter `ProgID` an die oben genannten Speicherorten, wenn es sich bei dem Clientcomputer 32-Bit-Outlook auf einem 64-Bit-Windows-Betriebssystem ausgeführt wird. In diesem Fall sollte das Installationsprogramm der Anbieter auswählen eine der folgenden Speicherorten in der `HKEY_CURRENT_USER` oder `HKEY_LOCAL_MACHINE` Struktur: 
  
- `HKEY_CURRENT_USER\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
Eine Klick-und-Los-Version von Office sollte das Installationsprogramm der Anbieter eine der folgenden Speicherorte in der Struktur HKEY_CURRENT_USER oder HKEY_LOCAL_MACHINE auswählen:
  
- `HKEY_CURRENT_USER\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`
    
- `HKEY_LOCAL_MACHINE\Software\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Outlook\SocialConnector\SocialProviders`
    
## <a name="see-also"></a>Siehe auch

- [Checkliste für Installation](installation-checklist.md)
- [QuickSteps für Informationen zum Entwickeln eines Providers](quick-steps-for-learning-to-develop-a-provider.md)
- [Bereitstellen eines Providers](deploying-a-provider.md)

