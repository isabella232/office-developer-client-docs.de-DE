---
title: Entwickeln mit Visual Studio
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e39d633d-d8fb-4e2f-a396-6cb50beb8c3e
description: Sie können die Funktionalität von InfoPath-Formularen erheblich verbessern, indem Sie sie mit verwaltetem Code in Visual Studio 2012 entwickelt erweitern. Sie können von Formularen mit Code klicken Sie dann auf SharePoint Server 2013 in Formularbibliotheken veröffentlichen.
ms.openlocfilehash: d6a2cfa1847b4b59b6978b8f4a0775aedf07a72d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790756"
---
# <a name="develop-with-visual-studio"></a>Entwickeln mit Visual Studio

Sie können die Funktionalität von InfoPath-Formularen erheblich verbessern, indem Sie sie mit verwaltetem Code in Visual Studio 2012 entwickelt erweitern. Sie können von Formularen mit Code klicken Sie dann auf SharePoint Server 2013 in Formularbibliotheken veröffentlichen.
  
Wenn Sie InfoPath-Formulare mit verwaltetem Code programmieren und bereitstellen möchten, müssen Sie zunächst drei allgemeine Schritte ausführen:
  
1. Installieren Sie Visual Studio 2012, mit dem [Microsoft Visual Studio Tools for Applications 2012](http://www.microsoft.com/en-us/download/details.aspx?id=38807) Add-on. 
    
2. Die Programmiersprache festlegen und Schreiben und Debuggen von Code im Code-Editor von Visual Studio 2012.
    
3. Wenn Sie das Formular entwerfen und Entwickeln von Ihrem Code abgeschlossen haben, kann die Formularvorlage in SharePoint Server 2013 veröffentlicht werden.
    
Es folgen einige Gründe Formulare erstellen, die mit SharePoint Server 2013 kompatibel sind:
  
- Formulare, die in SharePoint Server 2013 mit InfoPath Forms Services bereitgestellt können in einem Browser ausgefüllt werden. Dies ermöglicht Benutzern, die nicht über InfoPath installiert sind, öffnen und Verwenden von Formularen verfügen.
    
- Entwerfen Sie nur eine Version des Formulars. Formulare, die mit Microsoft SharePoint Server kompatibel sind, sind auch kompatibel mit InfoPath Filler, aber die Formulare, die nur mit InfoPath Filler kompatibel sind, können nicht im Browser geöffnet werden.
    
Es gibt zwei Methoden, um das Formular in SharePoint veröffentlichen: SharePoint sandboxed Solutions und vom Administrator bereitgestellte Lösungen. Weitere Informationen zu den einzelnen Publikation-Methode und Vorschläge, welche Methode am besten für Ihr Szenario ist, finden Sie unter [Publishing Forms with Code](publishing-forms-with-code.md). Beispiel: Lösungen für sandkastenlösungen, [Beispiele für Sandkastenlösungen](sample-sandboxed-solutions.md)angezeigt.
  
## <a name="developing-with-visual-studio"></a>Bei der Entwicklung mit Visual Studio

Mit Visual Studio 2012 und Microsoft Visual Studio Tools for Applications 2012 Add-on installiert können Sie zum Entwickeln von Lösungen für InfoPath managed Code beginnen.
  
### <a name="choosing-a-programming-language"></a>Auswählen einer Programmiersprache

InfoPath finden Sie die Optionen zum Programmieren mit vier Versionen von InfoPath-Objektmodells in zwei Sprachen: Visual Basic und c#. Die vier Versionen des Objektmodells bieten die Kompatibilität mit InfoPath 2013, InfoPath, Office InfoPath 2007 und Microsoft InfoPath 2003.
  
### <a name="to-specify-the-programming-language-and-object-model"></a>So geben Sie die Programmiersprache und das Objektmodell an

1. Ein Formularvorlagenprojekt in InfoPath-Designer geöffnet klicken Sie auf der Registerkarte **Entwickler** auf **Sprache** . 
    
2. Wählen Sie in der Kategorie **Programmierung** im Dialogfeld **Formularoptionen** die Sprache, die Sie aus der Dropdownliste **Codesprache der Formularvorlage** mit arbeiten möchten. Wählen Sie dann die Version des Objektmodells aus der Dropdownliste **Zielversion** . Eine Version Jahr nach dem Namen der **InfoPath** keinen die **Zielversion** -Option, die nur mit InfoPath 2013 kompatibel ist. 
    
    > [!NOTE]
    > Nicht alle Formulartypen Vorlage unterstützen Code. Beispielsweise führen Sie die **SharePoint-Liste** Vorlage Formulartyp und **Vorlagenparts** Formularcode nicht unterstützt. Wenn Sie einen Vorlagentyp Formular entwerfen, der Code nicht unterstützt, wird die Registerkarte **Entwicklertools** nicht verfügbar. Darüber hinaus unterstützen nur einige Formulartypen Vorlage alle vier Versionen des Objektmodells. Beispielsweise der Vorlagentyp **Leeres Formular (InfoPath Filler)** unterstützt alle vier Versionen des Objektmodells (und erstellt die Formularvorlage, die nur mit InfoPath Filler in diesen Versionen kompatibel sind), aber die Vorlage **Leeres Formular** unterstützt nur InfoPath 2013 und InfoPath (und -Formularvorlagen, die mit InfoPath Filler und im Browser kompatibel sind erstellt). 
  
    Sie können festlegen, dass eine Standardprogrammiersprache, sodass immer im InfoPath-Formular-Designer mit der Sprache und Objektmodellversion Ihrer Wahl gestartet wird.
    
### <a name="to-set-the-default-programming-language"></a>So legen Sie die Standardprogrammiersprache fest

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Optionen**.
    
2. Klicken Sie im Abschnitt **Allgemein** des Dialogfelds **InfoPath-Optionen** auf **Weitere Optionen**.
    
3. Wählen Sie auf der Registerkarte **Entwurf** des Dialogfelds **Optionen** im Abschnitt **Standardeinstellungen für Programmierung** die Standardprogrammiersprache aus. 
    
### <a name="writing-code"></a>Schreiben von Code

Nun können Sie mit InfoPath 2013 und Visual Studio 2012 entwickeln. 
  
### <a name="to-start-the-visual-studio-code-editor"></a>Starten Sie im Code-Editor von Visual Studio

1. Öffnen Sie eine Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Entwicklertools** auf **Code-Editor** . 
    
> [!TIP]
> Sie können auch im Code-Editor zu starten und automatisch hinzufügen Ereignishandler für Formular- und Ereignisse, die mithilfe der Befehle auf der Registerkarte **Entwicklertools** , Kontextmenüs und andere User Interface-Methoden. Weitere Informationen finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md)
  

