---
title: Entwicklung mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie sie mit verwaltetem Code erweitern, der in Visual Studio 2012 entwickelt wurde. Anschließend können Sie Ihre Formulare mit Code in Formularbibliotheken auf SharePoint Server 2013 veröffentlichen.
ms.openlocfilehash: b7d2437e671a13ceafc6c11a6dd83d39f8ffa76b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625903"
---
# <a name="develop-with-visual-studio"></a>Entwicklung mit Visual Studio

Sie können die Funktionalität Ihrer InfoPath-Formulare erheblich verbessern, indem Sie sie mit verwaltetem Code erweitern, der in Visual Studio 2012 entwickelt wurde. Anschließend können Sie Ihre Formulare mit Code in Formularbibliotheken auf SharePoint Server 2013 veröffentlichen.
  
Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:
  
1. Installieren Sie Visual Studio 2012 mit dem [Microsoft Visual Studio-Tools für Anwendungen 2012-Add-On.](https://www.microsoft.com/en-us/download/details.aspx?id=38807) 
    
2. Legen Sie Ihre Programmiersprache fest, und schreiben und debuggen Sie dann Code im Code-Editor Visual Studio 2012.
    
3. Wenn Sie das Entwerfen des Formulars und das Entwickeln des Codes abgeschlossen haben, kann die Formularvorlage auf SharePoint Server 2013 veröffentlicht werden.
    
Hier sind einige Gründe für die Erstellung von Formularen, die mit SharePoint Server 2013 kompatibel sind:
  
- Formulare, die auf SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt werden, können in einem Browser ausgefüllt werden. Dadurch können Benutzer, die InfoPath nicht installiert haben, Formulare öffnen und verwenden.
    
- Sie entwerfen nur eine Version des Formulars. Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch mit infoPath Filler kompatibel, Formulare, die nur mit infoPath Filler kompatibel sind, können jedoch nicht im Browser geöffnet werden.
    
Es gibt zwei Möglichkeiten, Ihr Formular in SharePoint zu veröffentlichen: SharePoint Sandkastenlösungen und vom Administrator bereitgestellte Lösungen. Weitere Informationen zu den einzelnen Publikationsmethoden und Vorschläge dazu, welche Methode für Ihr Szenario am besten geeignet ist, finden Sie unter [Veröffentlichen von Formularen mit Code.](publishing-forms-with-code.md) Beispiellösungen für Sandkastenlösungen finden Sie unter ["Beispiel für Sandkastenlösungen".](sample-sandboxed-solutions.md)
  
## <a name="developing-with-visual-studio"></a>Entwickeln mit Visual Studio

Nachdem Visual Studio 2012 und das Add-On Microsoft Visual Studio-Tools für Anwendungen 2012 installiert sind, können Sie mit der Entwicklung von InfoPath-Lösungen mit verwaltetem Code beginnen.
  
### <a name="choosing-a-programming-language"></a>Auswählen einer Programmiersprache

InfoPath bietet die Programmieroptionen mithilfe von vier Versionen des InfoPath-Objektmodells in zwei Sprachen: Visual Basic und C#. Die vier Versionen des Objektmodells bieten Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>So geben Sie die Programmiersprache und das Objektmodell an

1. Wenn ein Formularvorlagenprojekt im InfoPath-Designer geöffnet ist, klicken Sie auf der Registerkarte **"Entwicklertools"** auf **"Sprache".** 
    
2. Wählen Sie in der Kategorie **Programmierung** des Dialogfelds **Formularoptionen** in der Dropdownliste **Codesprache der Formularvorlage** die Sprache aus, mit der Sie arbeiten möchten. Wählen Sie dann die Version des Objektmodells aus der Dropdownliste für die **Zielversion** aus. Die **Zielversionsoption,** die nur mit InfoPath 2013 kompatibel ist, hat kein Versionsjahr nach dem **InfoPath-Namen.** 
    
    > [!NOTE]
    > Nicht alle Formularvorlagentypen unterstützen Code. Beispielsweise unterstützen der **SharePoint Formularvorlagentyp "List"** und **die Vorlagenteile** keinen Formularcode. Beim Entwerfen eines Formularvorlagentyps, der keinen Code unterstützt, ist die Registerkarte **"Entwickler"** nicht verfügbar. Außerdem unterstützen nur einige Formularvorlagentypen alle vier Versionen des Objektmodells. Beispielsweise unterstützt der Vorlagentyp **"Leeres Formular" (InfoPath Filler)** alle vier Versionen des Objektmodells (und erstellt Formularvorlagen, die in diesen Versionen nur mit InfoPath Filler kompatibel sind), die Vorlage **"Leeres Formular"** unterstützt jedoch nur InfoPath 2013 und InfoPath (und erstellt Formularvorlagen, die sowohl mit InfoPath Filler als auch mit dem Browser kompatibel sind). 
  
    Sie können eine Standardprogrammiersprache festlegen, damit der InfoPath-Formular-Designer immer mit der Gewünschten Sprach- und Objektmodellversion beginnt.
    
### <a name="to-set-the-default-programming-language"></a>So legen Sie die Standardprogrammiersprache fest

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.
    
2. Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.
    
3. Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus.  
    
### <a name="writing-code"></a>Schreiben von Code

Sie können jetzt mit der Entwicklung mit InfoPath 2013 und Visual Studio 2012 beginnen. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>So starten Sie den Visual Studio Code-Editor

1. Öffnen Sie eine Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**. 
    
> [!TIP]
> Sie können auch den Code-Editor starten und automatisch Ereignishandler für Formular- und Steuerelementereignisse hinzufügen, indem Sie Befehle auf der Registerkarte **"Entwickler",** Kontextmenüs und andere Benutzeroberflächenmethoden verwenden. Weitere Informationen finden Sie unter ["Hinzufügen eines Ereignishandlers"](how-to-add-an-event-handler.md)
  

