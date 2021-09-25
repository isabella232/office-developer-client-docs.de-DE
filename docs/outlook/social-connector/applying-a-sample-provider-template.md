---
title: Anwenden einer Beispielanbietervorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: da487569-f2f0-404c-b944-38ed1c1b82bb
description: 'Das Beispiel Outlook OSC-Anbietervorlagen (Social Connector) bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters. '
ms.openlocfilehash: f13c158179778404ee142ada6ef004e6719cfe1f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623593"
---
# <a name="applying-a-sample-provider-template"></a>Anwenden einer Beispielanbietervorlage

Das Beispiel Outlook OSC-Anbietervorlagen (Social Connector) bieten Ihnen ein Framework für die Implementierung eines OSC-Anbieters. Die Anbietervorlagen sind in C++, C# und Visual Basic verfügbar. Diese Vorlagen sind nur ein Ausgangspunkt für die Entwicklung Ihres Anbieters. Die Vorlagen beziehen sich nicht auf das Schreiben des Implementierungscodes für den Anbieter und das Erstellen eines Setuppakets für den Anbieter. Das folgende Verfahren zeigt, wie Sie eine OSC-Anbietervorlage anwenden, wenn Sie mit der Entwicklung eines Anbieters beginnen.
  
### <a name="to-apply-an-osc-provider-template"></a>So wenden Sie eine OSC-Anbietervorlage an

1. Klicken Sie im **Startmenü** mit der rechten Maustaste auf **Microsoft Visual Studio 2010,** und klicken Sie auf den Befehl **"Als Administrator ausführen".** Wenn Sie dazu aufgefordert werden, klicken Sie auf **"Ja",** um Visual Studio als Administrator auszuführen. 
    
2. Ändern Sie den Projektnamen und den Namespace in der Vorlage in Den Projektnamen und Namespacebezeichner.
    
3. Ändern Sie die **AssemblyInfo-Klasse,** um die entsprechenden Assemblyinformationen anzugeben. 
    
4. Implementieren Sie die als **To-Do** markierten Schnittstellenelemente, und fügen Sie nach Bedarf weitere Abhängigkeiten und Verweise hinzu. 
    
5. Erstellen Sie das Projekt.
    
6. Stellen Sie sicher, dass die Anbieterassembly ProgID als Schlüssel unter aufgeführt  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector\SocialProviders` ist.
    
7. Um das Setupprojekt zu verteilen, erstellen Sie ein Setupprojekt in Visual Studio oder ein Setuptool Ihrer Wahl.
    
8. Ihr Setupprojekt sollte die COM-Registrierung für Ihre Assembly abschließen und auch den ProgID-Schlüssel erstellen, wie in Schritt 5 aufgeführt.
    
## <a name="see-also"></a>Siehe auch

- [Herunterladen der Beispiele](downloading-the-samples.md)
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)

