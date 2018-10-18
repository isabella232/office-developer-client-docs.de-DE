---
title: Bestimmen, ob Outlook eine Klick-und-Los-Anwendung auf einem Computer ist
TOCTitle: Determine whether Outlook is a Click-to-Run application on a computer
ms:assetid: 1b8573be-8ea8-4973-869d-87fda57ce525
ms:mtpsurl: https://msdn.microsoft.com/library/Ff522355(v=office.15)
ms:contentKeyID: 55119804
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: c155fed72a314c5c260ed2fe574474afd45c44c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406652"
---
# <a name="determine-whether-outlook-is-a-click-to-run-application-on-a-computer"></a>Bestimmen, ob Outlook eine Klick-und-Los-Anwendung auf einem Computer ist

Klick-und-Los ist in Office 2010 und höheres Versionen eine Möglichkeit zur Bereitstellung und Aktualisierung von Software. Produkte, die über Klick-und-Los bereitgestellt werden, werden in einer virtuellen Umgebung auf dem lokalen Betriebssystem ausgeführt. Dies bedeutet, dass diese Produkte über private Kopien ihrer Dateien und Einstellungen verfügen und sämtliche erfolgten Änderungen in der virtuellen Umgebung erfasst werden.

Klick-und-Los ist schnell – Benutzer können innerhalb kürzester Zeit mit dem Ausführen einer Anwendung beginnen, ohne warten zu müssen, bis das ganze Produkt installiert wurde. Updates werden automatisch im Hintergrund ausgeführt, ohne dass ein Benutzerzuerst eine Installation entfernen oder Updates manuell installieren muss. Klick-und-Los-Produkte sind virtualisiert und stehen nicht im Konflikt mit anderer installierter Software. Da ein Produkt, das über Klick-und-Los bereitgestellt wurde, aber über private Kopien aller Dateien und der Registrierung verfügt, kann der Add-In-Entwickler nicht in gleicher Weise über das Vorhandensein des Produkts bestimmen, wie dies bei einem Produkt der Fall ist, das auf der Festplatte des Clientcomputers installiert wurde. Ab Outlook 2010 sollten Add-In-Entwickler überprüfen, ob Outlook installiert wurde und ob Outlook als Klick-und-Los-Produkt bereitgestellt wurde.


> [!NOTE]
> In der virtuellen Klick-und-Los-Anwendungsumgebung wird nur 32-Bit-Office 2013 unterstützt, auch wenn der Clientcomputer über ein 64-Bit-Betriebssystem verfügt.



### <a name="to-check-whether-outlook-2013-was-delivered-by-click-to-run-on-a-client-computer"></a>So prüfen Sie, ob Outlook 2013 per Klick-und-Los auf dem Clientcomputer bereitgestellt wurde

- Überprüfen Sie, ob der VirtualOutlook-Schlüssel am folgenden Speicherort in der Windows-Registrierung vorhanden ist:
    
  `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432Node\Microsoft\Office\15.0\Common\InstallRoot\Virtual\VirtualOutlook`
    
  Der Schlüssel VirtualOutlook ist ein REG\_SZ-Wert mit dem Gebietsschemakennzeichen des installierten Produkts, z. B. "en-us".

## <a name="see-also"></a>Siehe auch

- [Add-In-Verwaltung](add-in-administration.md)

