---
title: Entwicklung mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie Sie mit verwaltetem Code erweitern, der in Visual Studio 2012 entwickelt wurde. Sie können Ihre Formulare dann mit Code veröffentlichen, um Bibliotheken auf SharePoint Server 2013 zu bilden.
ms.openlocfilehash: 1c67b85823fe567b494366a505be5dad51d20b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300287"
---
# <a name="develop-with-visual-studio"></a>Entwicklung mit Visual Studio

Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie Sie mit verwaltetem Code erweitern, der in Visual Studio 2012 entwickelt wurde. Sie können Ihre Formulare dann mit Code veröffentlichen, um Bibliotheken auf SharePoint Server 2013 zu bilden.
  
Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:
  
1. Installieren Sie Visual Studio 2012 mit dem Add-on [für Microsoft Visual Studio Tools for Applications 2012](https://www.microsoft.com/en-us/download/details.aspx?id=38807) . 
    
2. Legen Sie Ihre Programmiersprache fest, und schreiben und Debuggen Sie dann Code im Code-Editor von Visual Studio 2012.
    
3. Nachdem Sie das Formular entworfen und den Code entwickelt haben, kann die Formularvorlage in SharePoint Server 2013 veröffentlicht werden.
    
Im folgenden finden Sie einige Gründe für die Erstellung von Formularen, die mit SharePoint Server 2013 kompatibel sind:
  
- Formulare, die in SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, können in einem Browser ausgefüllt werden. Dadurch können Benutzer, die InfoPath nicht installiert haben, ihre Formulare öffnen und verwenden.
    
- Sie entwerfen nur eine Version des Formulars. Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch mit dem InfoPath-Filler kompatibel, aber Formulare, die nur mit dem InfoPath-Füllbereich kompatibel sind, können im Browser nicht geöffnet werden.
    
Es gibt zwei Möglichkeiten, Ihr Formular in SharePoint zu veröffentlichen: SharePoint-sandkastenlösungen und vom Administrator bereitgestellte Lösungen. Weitere Informationen zu den einzelnen Veröffentlichungsmethoden und Vorschlägen dazu, welche Methode für Ihr Szenario am besten geeignet ist, finden Sie unter [Veröffentlichen von Formularen mit Code](publishing-forms-with-code.md). Beispiele für Lösungen für sandkastenlösungen finden Sie unter [Beispiel für Sandkasten](sample-sandboxed-solutions.md)Lösungen.
  
## <a name="developing-with-visual-studio"></a>Entwickeln mit Visual Studio

Mit Visual Studio 2012 und Microsoft Visual Studio Tools for Applications 2012 Add-on installiert sind, können Sie mit der Entwicklung von InfoPath-Lösungen mit verwaltetem Code beginnen.
  
### <a name="choosing-a-programming-language"></a>Auswählen einer Programmiersprache

InfoPath bietet die Optionen zum Programmieren mit vier Versionen des InfoPath-Objektmodells in zwei Sprachen: Visual Basic und C#. Die vier Versionen des Objektmodells bieten Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>So geben Sie die Programmiersprache und das Objektmodell an

1. Wenn ein Formularvorlagenprojekt im InfoPath-Designer geöffnet ist, klicken Sie auf der Registerkarte **Entwickler** auf **Sprache** . 
    
2. Wählen Sie in der Kategorie **Programmierung** des Dialogfelds **Formularoptionen** in der Dropdownliste **Codesprache der Formularvorlage** die Sprache aus, mit der Sie arbeiten möchten. Wählen Sie dann in der Dropdownliste **Zielversion** die Version des Objektmodells aus. Die Option **Zielversion** , die nur mit InfoPath 2013 kompatibel ist, verfügt nicht über ein Versions Jahr, das dem **InfoPath** -Namen folgt. 
    
    > [!NOTE]
    > Nicht alle Formularvorlagen Typen unterstützen Code. Beispielsweise unterstützen der Typ der **SharePoint-Listen** Formularvorlagen und **Vorlagen Parts** den Formularcode nicht. Beim Entwerfen eines Formularvorlagen Typs, der keinen Code unterstützt, ist die Registerkarte **Entwicklertools** nicht verfügbar. Außerdem unterstützen nur einige Formularvorlagen Typen alle vier Versionen des Objektmodells. Der Vorlagentyp **leeres Formular (InfoPath Filler)** unterstützt beispielsweise alle vier Versionen des Objektmodells (und erstellt Formularvorlagen, die nur mit dem InfoPath-Füller in diesen Versionen kompatibel sind), aber die **leere Formular** Vorlage unterstützt nur InfoPath 2013 und InfoPath (und erstellt Formularvorlagen, die sowohl mit dem InfoPath-Füller als auch mit dem Browser kompatibel sind). 
  
    Sie können eine Standard Programmiersprache festlegen, sodass der InfoPath-Formular-Designer immer mit der Sprach-und Objektmodellversion Ihrer Wahl beginnt.
    
### <a name="to-set-the-default-programming-language"></a>So legen Sie die Standardprogrammiersprache fest

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.
    
2. Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.
    
3. Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus.  
    
### <a name="writing-code"></a>Schreiben von Code

Sie können nun mit InfoPath 2013 und Visual Studio 2012 entwickeln. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>So starten Sie den Visual Studio-Code-Editor

1. Öffnen Sie eine Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**. 
    
> [!TIP]
> Sie können den Code-Editor auch starten und automatisch Ereignishandler für Formular-und Steuerelementereignisse mithilfe von Befehlen auf der Registerkarte **Entwickler** , Kontextmenüs und andere Benutzeroberflächenmethoden hinzufügen. Weitere Informationen finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md) .
  

