---
title: Anwenden einer Beispielvorlage Anbieter
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Die Outlook Social Connector (OSC)-Anbieter Beispielvorlagen können Sie einen Rahmen für die Implementierung eines OSC-Anbieters. '
ms.openlocfilehash: 2388da58690e1870434c576bfa68649937156c54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795946"
---
# <a name="applying-a-sample-provider-template"></a>Anwenden einer Beispielvorlage Anbieter

Die Outlook Social Connector (OSC)-Anbieter Beispielvorlagen können Sie einen Rahmen für die Implementierung eines OSC-Anbieters. Die Anbietervorlagen vom sind in C++, c# und Visual Basic verfügbar. Diese Vorlagen sind nur als Ausgangspunkt für die Entwicklung Anbieter. die Vorlagen berücksichtigen nicht schreiben den Code zur Implementierung für den Anbieter und erstellen ein Setup-Paket für den Anbieter. Das folgende Verfahren zeigt, wie eine OSC-Anbietervorlage anwenden, wenn Sie beginnen, um einen Anbieter zu entwickeln.
  
### <a name="to-apply-an-osc-provider-template"></a>Anwenden eine OSC-Anbieter-Vorlage

1. Klicken Sie im **Startmenü** mit der rechten Maustaste in **Microsoft Visual Studio 2010** , und klicken Sie auf den Befehl **als Administrator ausführen** . Wenn Sie aufgefordert werden, klicken Sie auf **Ja** , um Visual Studio als Administrator ausführen. 
    
2. Ändern Sie den Namen des Projekts und den Namespace in der Vorlage in Ihrem Projekt Name und Namespacebezeichnern.
    
3. Ändern Sie die **AssemblyInfo** -Klasse, um die entsprechenden Assemblyinformationen anzugeben. 
    
4. Implementieren Sie die Schnittstellenmember als **Aufgabe** gekennzeichnet, und fügen Sie weitere Abhängigkeiten und Referenzen, nach Bedarf. 
    
5. Erstellen Sie das Projekt.
    
6. Stellen Sie sicher, dass die Anbieterassembly ProgID, als Schlüssel unter aufgeführt ist `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`.
    
7. Erstellen Sie ein Setup-Projekt in Visual Studio oder ein Setup-Tool Ihrer Wahl, um das Setup-Projekt zu verteilen.
    
8. Das Setup-Projekt auszufüllen COM-Registrierung für die Assembly und auch den Schlüssel ProgID erstellen, wie in Schritt 5 aufgeführt.
    
## <a name="see-also"></a>Siehe auch

- [Herunterladen der Beispiele](downloading-the-samples.md)
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)

