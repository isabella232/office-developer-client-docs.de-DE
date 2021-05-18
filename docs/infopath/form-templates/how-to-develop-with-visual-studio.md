---
title: Entwicklung mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie sie mit verwalteten Code erweitern, der in Visual Studio 2012 entwickelt wurde. Anschließend können Sie Ihre Formulare mit Code in Formularbibliotheken auf SharePoint Server 2013 veröffentlichen.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300287"
---
# <a name="develop-with-visual-studio"></a>Entwicklung mit Visual Studio

Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie sie mit verwalteten Code erweitern, der in Visual Studio 2012 entwickelt wurde. Anschließend können Sie Ihre Formulare mit Code in Formularbibliotheken auf SharePoint Server 2013 veröffentlichen.
  
Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:
  
1. Installieren Visual Studio 2012 mit [dem Microsoft Visual Studio-Tools für Anwendungen 2012-Add-On.](https://www.microsoft.com/en-us/download/details.aspx?id=38807) 
    
2. Legen Sie Ihre Programmiersprache, und schreiben und debuggen Sie code dann im Visual Studio 2012-Code-Editor.
    
3. Wenn Sie mit dem Entwerfen des Formulars und der Entwicklung des Codes fertig sind, kann die Formularvorlage auf server 2013 SharePoint veröffentlicht werden.
    
Hier finden Sie einige Gründe, warum Sie das Erstellen von Formularen in Betracht ziehen sollten, die mit SharePoint Server 2013 kompatibel sind:
  
- Formulare, die auf SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, können in einem Browser ausgefüllt werden. Auf diese Weise können Benutzer, für die InfoPath nicht installiert ist, Ihre Formulare öffnen und verwenden.
    
- Sie entwerfen nur eine Version des Formulars. Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch mit dem InfoPath Filler kompatibel, aber Formulare, die nur mit dem InfoPath Filler kompatibel sind, können nicht im Browser geöffnet werden.
    
Es gibt zwei Möglichkeiten zum Veröffentlichen des Formulars SharePoint: SharePoint Sandkastenlösungen und vom Administrator bereitgestellte Lösungen. Weitere Informationen zu jeder Publikationsmethode und Vorschläge dazu, welche Methode für Ihr Szenario am besten ist, finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md). Beispiellösungen für Sandkastenlösungen finden Sie unter [Beispiel sandkastenlösungen](sample-sandboxed-solutions.md).
  
## <a name="developing-with-visual-studio"></a>Entwickeln mit Visual Studio

Mit Visual Studio 2012 und dem Microsoft Visual Studio-Tools für Anwendungen 2012-Add-On können Sie mit der Entwicklung von Lösungen für verwalteten Code von InfoPath beginnen.
  
### <a name="choosing-a-programming-language"></a>Auswählen einer Programmiersprache

InfoPath bietet die Optionen zum Programmieren mithilfe von vier Versionen des InfoPath-Objektmodells in zwei Sprachen: Visual Basic und C#. Die vier Versionen des Objektmodells bieten Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>So geben Sie die Programmiersprache und das Objektmodell an

1. Wenn ein Formularvorlagenprojekt im InfoPath-Designer geöffnet ist, klicken Sie auf **der** Registerkarte Entwickler auf **Sprache.** 
    
2. Wählen Sie in der Kategorie **Programmierung** des Dialogfelds **Formularoptionen** in der Dropdownliste **Codesprache der Formularvorlage** die Sprache aus, mit der Sie arbeiten möchten. Wählen Sie dann in der Dropdownliste  Zielversion die Version des Objektmodells aus. Die **Option Zielversion,** die nur mit InfoPath 2013 kompatibel ist, verfügt nicht über ein Versionsjahr nach dem **Namen InfoPath.** 
    
    > [!NOTE]
    > Nicht alle Formularvorlagentypen unterstützen Code. Der Formularvorlagentyp SharePoint **und** Vorlagenteile  unterstützen z. B. keinen Formularcode. Beim Entwerfen eines Formularvorlagentyps, der keinen Code unterstützt, ist **die** Registerkarte Entwickler nicht verfügbar. Außerdem unterstützen nur einige Formularvorlagentypen alle vier Versionen des Objektmodells. Beispielsweise unterstützt der Vorlagentyp Leeres **Formular (InfoPath Filler)** alle vier Versionen des Objektmodells (und erstellt Formularvorlagen,  die nur mit dem InfoPath Filler in diesen Versionen kompatibel sind), aber die Vorlage Leeres Formular unterstützt nur InfoPath 2013 und InfoPath (und erstellt Formularvorlagen, die sowohl mit dem InfoPath Filler als auch mit dem Browser kompatibel sind). 
  
    Sie können eine Standardprogrammiersprache festlegen, damit der InfoPath-Formulardesigner immer mit der Sprach- und Objektmodellversion Ihrer Wahl beginnt.
    
### <a name="to-set-the-default-programming-language"></a>So legen Sie die Standardprogrammiersprache fest

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.
    
2. Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.
    
3. Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus.  
    
### <a name="writing-code"></a>Schreiben von Code

Sie können nun mit der Entwicklung mit InfoPath 2013 und Visual Studio 2012 beginnen. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>So starten Sie den Visual Studio Code Editor

1. Öffnen Sie eine Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**. 
    
> [!TIP]
> Sie können auch den Code-Editor starten und mithilfe von Befehlen  auf der Registerkarte Entwickler, Kontextmenüs und anderen Benutzeroberflächenmethoden automatisch Ereignishandler für Formular- und Steuerelementereignisse hinzufügen. Weitere Informationen finden Sie unter [Add an Event Handler](how-to-add-an-event-handler.md)
  

