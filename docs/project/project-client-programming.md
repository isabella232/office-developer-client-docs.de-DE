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
- vba, Projektobjektmodell, Project, Programmierbarkeit, Programmierbarkeit, Project VBA, Visual Basic for Applications, Project-Objektmodell, VBA, Objektmodell, VBA, Visual Basic for Applications
ms.localizationpriority: medium
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Die Project 2013-Desktopclientanwendungen – Project Standard 2013 und Project Professional 2013 – können mithilfe von VBA zum Schreiben von Makros angepasst und erweitert werden. Sie können Visual Studio 2012 verwenden, um die Benutzeroberfläche des Menübands anzupassen und komplexe Add-Ins zu erstellen. Office Add-Ins ermöglichen ein neues Erweiterbarkeitsmodell für Aufgabenbereiche in Project, die auf einer gemeinsamen Office 2013-Plattform basieren. Project Standard 2013 und Project Professional 2013 können allgemeine Office-Add-Ins ausführen und Aufgabenbereich-Add-Ins verwenden, die speziell für Project zur Integration in SharePoint, andere Websites und Webanwendungen sowie externe Daten entwickelt wurden.
ms.openlocfilehash: 952646dd27310b2fe2e999d87474055a76045c45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629018"
---
# <a name="project-client-programming"></a>Project-Clientprogrammierung

Die Project 2013-Desktopclientanwendungen – Project Standard 2013 und Project Professional 2013 – können mithilfe von VBA zum Schreiben von Makros angepasst und erweitert werden. Sie können Visual Studio 2012 verwenden, um die Benutzeroberfläche des Menübands anzupassen und komplexe Add-Ins zu erstellen. Office Add-Ins ermöglichen ein neues Erweiterbarkeitsmodell für Aufgabenbereiche in Project, die auf einer gemeinsamen Office 2013-Plattform basieren. Project Standard 2013 und Project Professional 2013 können allgemeine Office-Add-Ins ausführen und Aufgabenbereich-Add-Ins verwenden, die speziell für Project zur Integration in SharePoint, andere Websites und Webanwendungen sowie externe Daten entwickelt wurden.
  
 **Wechseln zu Visual Studio** VBA eignet sich zum Aufzeichnen von Makros und zum Entwickeln relativ einfacher Automatisierungslösungen. Um Aufgabenbereich-Add-Ins, Add-Ins und komplexere, sichere, skalierbare und leicht bereitgestellte Lösungen zu entwickeln, empfehlen wir, Visual Studio 2012 zu verwenden. Die primäre Interopassembly von Microsoft .NET Framework 4.0 und Project 2013 bietet viele Vorteile für die Entwicklung und Bereitstellung von Lösungen, die die Project 2013-Desktopclients automatisieren und integrieren. 
  
> [!NOTE]
> Sie können Visual Studio 2010 verwenden, um Project-Add-Ins zu entwickeln. Visual Studio 2012 enthält jedoch Vorlagen und Erweiterungen, die zum Erstellen Office Add-Ins-Clients entwickelt wurden. 
  
Das **MSProject-Objektmodell** für VBA in Project 2013 ist im Wesentlichen identisch mit dem **Microsoft.Office. Interop.MSProject-Objektmodell** für Lösungen mit verwaltetem Code mit Office Developer Tools für Visual Studio 2013 (auch bekannt als VSTO). Visual Studio 2012 enthält Vorlagen für die Entwicklung von Add-Ins auf Anwendungsebene für Project 2010 und für Project 2013 (entweder die Project Standard- oder Project Professional version). VSTO und Office Developer Tools für Visual Studio 2012 vereinfachen das Entwickeln, Testen und Bereitstellen erweiterter Integrationslösungen, die den Project Desktopclient und andere Office 2013-Anwendungen verwenden und in SharePoint Websites, Listen und Workflows integrieren können. 
  
Aufgabenbereich-Add-Ins und andere Add-Ins für Office und SharePoint können im Office Store verkauft werden (siehe [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/) ) zur Verwendung mit Project Online und lokalen Installationen. VBA-Makros und VSTO-Add-Ins können nicht im Office Store verteilt werden. sie sind für die lokale Verwendung mit Project Standard und Project Professional konzipiert. Sie können VBA-Makros innerhalb eines Projekts verteilen. MPP-Datei, installieren Sie sie in der Datei "Global.MPT" auf Ihrem Computer, oder verteilen Sie sie in der Enterprise-Global-Vorlage in Project Server 2013. VSTO-Add-Ins können durch [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) Bereitstellung sicherer verteilt werden, was einfache Updates ermöglicht. 
  
## <a name="reference"></a>Referenz

[Project VBA-Entwicklerreferenz](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Enthält einführungs- und VBA-Hilfeartikel. 
  
## <a name="related-sections"></a>Verwandte Abschnitte

[Project Server 2013-Architektur](project-server-2013-architecture.md) Zeigt, wie die Project-Clients mit Project Server interagieren. 
  
## <a name="see-also"></a>Siehe auch

- [Project für Entwickler](https://msdn.microsoft.com/office/aa905469)
- [Office Developer Center](https://dev.office.com)
- [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [ClickOnce Sicherheit und Bereitstellung](https://msdn.microsoft.com/library/t71a733d.aspx)
- [Referenz: Verfügbare Felder](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

