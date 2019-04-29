---
title: Anwenden einer Beispielanbieter Vorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Die Beispielvorlagen für Outlook Social Connector (OSC) bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters. '
ms.openlocfilehash: 10fb21ab640e298bc655b8cad554fae789e2ad47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425911"
---
# <a name="applying-a-sample-provider-template"></a>Anwenden einer Beispielanbieter Vorlage

Die Beispielvorlagen für Outlook Social Connector (OSC) bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters. Die Anbietervorlagen sind in C++, C# und Visual Basic verfügbar. Diese Vorlagen sind nur ein Ausgangspunkt für die Entwicklung Ihres Anbieters. die Vorlagen richten sich nicht auf das Schreiben des Implementierungscodes für den Anbieter und das Erstellen eines Setuppakets für den Anbieter. Im folgenden Verfahren wird gezeigt, wie Sie eine OSC-Anbietervorlage anwenden, wenn Sie mit der Entwicklung eines Anbieters beginnen.
  
### <a name="to-apply-an-osc-provider-template"></a>So wenden Sie eine OSC-Anbietervorlage an

1. Klicken Sie im **Startmenü** mit der rechten Maustaste auf **Microsoft Visual Studio 2010** , und klicken Sie auf den Befehl **als Administrator ausführen** . Wenn Sie dazu aufgefordert werden, klicken Sie auf **Ja** , um Visual Studio als Administrator auszuführen. 
    
2. Ändern Sie den Projektnamen und den Namespace in der Vorlage in den Projektnamen und die Namespace-IDs.
    
3. Ändern Sie die **AssemblyInfo** -Klasse, um die entsprechenden Assemblyinformationen anzugeben. 
    
4. Implementieren Sie die Schnittstellenmember, die als **Aufgabe** markiert sind, und fügen Sie je nach Bedarf weitere Abhängigkeiten und Verweise hinzu. 
    
5. Erstellen Sie das Projekt.
    
6. Stellen Sie sicher, dass die ProgID der Anbieter-Assembly als `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders`Schlüssel unter aufgeführt wird.
    
7. Um das Setup-Projekt zu verteilen, erstellen Sie ein Setup-Projekt in Visual Studio oder ein Setup-Tool Ihrer Wahl.
    
8. Das Setupprojekt sollte die COM-Registrierung für Ihre Assembly abschließen und auch den ProgID-Schlüssel erstellen, wie in Schritt 5 aufgeführt.
    
## <a name="see-also"></a>Siehe auch

- [Herunterladen der Beispiele](downloading-the-samples.md)
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)

