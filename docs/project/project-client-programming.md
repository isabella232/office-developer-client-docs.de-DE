---
title: Project-Clientprogrammierung
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- vba, project object model,Project, programmability,Programmability, Project VBA,Visual Basic for Applications, Project object model,VBA, object model,VBA,Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Die Project 2013-Desktopclientanwendungen – Project Standard 2013 und Project Professional 2013 – können angepasst und mithilfe von VBA zum Schreiben von Makros erweitert werden. Sie können die Visual Studio 2012 verwenden, um die Menübandoberfläche anzupassen und komplexe Add-Ins zu erstellen. Office-Add-Ins ermöglichen ein neues Erweiterbarkeitsmodell für Aufgabenbereiche in Project, die auf einer gemeinsamen Office 2013-Plattform aufgebaut sind. Project Standard 2013 und Project Professional 2013 können allgemeine Office-Add-Ins ausführen und Aufgabenbereich-Add-Ins verwenden, die speziell für Project entwickelt wurden, um sharePoint, andere Websites und Webanwendungen sowie externe Daten zu integrieren.
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301512"
---
# <a name="project-client-programming"></a>Project-Clientprogrammierung

Die Project 2013-Desktopclientanwendungen – Project Standard 2013 und Project Professional 2013 – können angepasst und mithilfe von VBA zum Schreiben von Makros erweitert werden. Sie können die Visual Studio 2012 verwenden, um die Menübandoberfläche anzupassen und komplexe Add-Ins zu erstellen. Office-Add-Ins ermöglichen ein neues Erweiterbarkeitsmodell für Aufgabenbereiche in Project, die auf einer gemeinsamen Office 2013-Plattform aufgebaut sind. Project Standard 2013 und Project Professional 2013 können allgemeine Office-Add-Ins ausführen und Aufgabenbereich-Add-Ins verwenden, die speziell für Project entwickelt wurden, um sharePoint, andere Websites und Webanwendungen sowie externe Daten zu integrieren.
  
 **Verschieben zu Visual Studio** VBA ist nützlich für die Aufzeichnung von Makros und die Entwicklung relativ einfacher Automatisierungslösungen. Um Aufgabenbereich-Add-Ins, Add-Ins und komplexere, sichere, skalierbare und einfach bereitgestellte Lösungen zu entwickeln, empfehlen wir die Verwendung von Visual Studio 2012. Die primäre Interop-Assembly von Microsoft .NET Framework 4.0 und project 2013 bieten viele Vorteile für die Entwicklung und Bereitstellung von Lösungen, die die Project 2013-Desktopclients automatisieren und integrieren. 
  
> [!NOTE]
> Sie können die Visual Studio 2010 zum Entwickeln von Project-Add-Ins verwenden. Allerdings enthält Visual Studio 2012 Vorlagen und Erweiterungen, die zum Erstellen von Office-Add-Ins-Clients entwickelt wurden. 
  
Das **MSProject-Objektmodell** für VBA in Project 2013 ist im Wesentlichen identisch mit dem **Microsoft.Office.Interop.MSProject-Objektmodell** für Lösungen mit verwalteten Code mit Office Developer Tools für Visual Studio 2013 (auch VSTO bezeichnet). Visual Studio 2012 enthält Vorlagen zum Entwickeln von Add-Ins auf Anwendungsebene für Project 2010 und Project 2013 (entweder die Versionen Project Standard oder Project Professional). VSTO und Office Developer Tools für Visual Studio 2012 vereinfachen das Entwickeln, Testen und Bereitstellen erweiterter Integrationslösungen, die den Project-Desktopclient und andere Office 2013-Anwendungen verwenden und in SharePoint-Websites, Listen und Workflows integrieren können. 
  
Aufgabenbereich-Add-Ins und andere Add-Ins für Office und SharePoint können im Office Store (siehe ) zur Verwendung mit Project Online und lokalen [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) Installationen verkauft werden. #A0 und VSTO-Add-Ins können nicht im Office Store verteilt werden. sie sind für die lokale Verwendung mit Project Standard und Project Professional konzipiert. Sie können VBA-Makros innerhalb eines Projekts verteilen. MPP-Datei, installieren Sie sie in der Datei Global.MPT auf Ihrem Computer, oder verteilen Sie sie in der Enterprise-Global-Vorlage in Project Server 2013. VSTO-Add-Ins können sicherer über [](https://msdn.microsoft.com/library/t71a733d.aspx) eine ClickOnce verteilt werden, was einfache Updates ermöglicht. 
  
## <a name="reference"></a>Referenz

[Project VBA-Entwicklerreferenz](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Enthält Einführungs- und VBA-Hilfeartikel. 
  
## <a name="related-sections"></a>Verwandte Abschnitte

[Project Server 2013-Architektur](project-server-2013-architecture.md) Zeigt, wie die Project-Clients mit Project Server interagieren. 
  
## <a name="see-also"></a>Siehe auch

- [Project für Entwickler](https://msdn.microsoft.com/office/aa905469)
- [Office Developer Center](https://dev.office.com)
- [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce Sicherheit und Bereitstellung](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referenz: Verfügbare Felder](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

