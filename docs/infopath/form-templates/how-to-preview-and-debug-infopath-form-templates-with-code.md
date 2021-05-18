---
title: Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Vorschau von Formularvorlagen [infopath 2007],Debuggen von Formularvorlagen [InfoPath 2007],Formularvorlagen [InfoPath 2007], Vorschau,Debuggen [InfoPath 2007], Formularvorlagen mit verwalteten Code, Formularvorlagen [InfoPath 2007], Debuggen,InfoPath 2007, Debugformularvorlagen,InfoPath 2007, Vorschau von Formularvorlagen
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath mit Visual Studio 2012 ermöglicht das Debuggen, indem Formularcode im Vorschaumodus ausgeführt wird. Wenn Sie mit dem Debuggen von Formularcode beginnen, wird das Projekt kompiliert, und das Formular wird von InfoPath im InfoPath-Vorschaufenster angezeigt. Wenn eine Codezeile ermittelt wird, für die ein Haltepunkt festgelegt wurde, wird der Fokus auf den Code-Editor verschoben. Wenn Sie den Vorgang nach einem Haltepunkt fortsetzen, wird der Fokus wieder zum Vorschaufenster verschoben. Das Debuggen wird beendet, wenn Sie das Vorschaufenster schließen.
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405240"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code

Microsoft InfoPath mit Visual Studio 2012 ermöglicht das Debuggen, indem Formularcode im Vorschaumodus ausgeführt wird. Wenn Sie mit dem Debuggen von Formularcode beginnen, wird das Projekt kompiliert, und das Formular wird von InfoPath im InfoPath-Vorschaufenster angezeigt. Wenn eine Codezeile ermittelt wird, für die ein Haltepunkt festgelegt wurde, wird der Fokus auf den Code-Editor verschoben. Wenn Sie den Vorgang nach einem Haltepunkt fortsetzen, wird der Fokus wieder zum Vorschaufenster verschoben. Das Debuggen wird beendet, wenn Sie das Vorschaufenster schließen.
  
Sie können die Formularoptionen für die Formularvorlage auch so ändern, dass Vorschau und Debuggen mithilfe einer bestimmten Benutzerrolle, einer Beispieldatendatei oder durch Angeben der Domäne ausgeführt werden, in der das Formular veröffentlicht wird.  
  
> [!NOTE]
> Es ist nicht möglich, Formularvorlagen zu debuggen, nachdem sie zur Laufzeit ab Visual Studio 2012 bereitgestellt wurden. Dazu gehören Formularvorlagen, die nur mit InfoPath kompatibel sind, sowie formularkompatible Vorlagen mit InfoPath und dem Webbrowser, die InfoPath Forms Services. Sie können jedoch Werte im Code in einem Feld zur Laufzeit protokollieren, um das Debugging der Geschäftslogik einer Formularvorlage zu unterstützten. Weitere Informationen dazu finden Sie unter [Protokollieren von Werten in einem Feld zum Debuggen](how-to-log-values-to-a-field-for-debugging.md). 
  
## <a name="debugging-in-preview-mode"></a>Debuggen im Vorschaumodus

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>So debuggen Sie ein InfoPath-Projekt im Vorschaumodus

1. Erstellen oder Öffnen einer InfoPath-Formularvorlage mit verwalteten Code in Visual Studio 2012.
    
2. Legen Sie im Code-Editor im Formularcode mindestens einen Haltepunkt fest, indem Sie links neben der Codezeile, in der ein Haltepunkt eingefügt werden soll, auf die graue Leiste klicken.
    
    Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.
    
3. Klicken Sie im Menü **Debuggen** auf **Debuggen starten**, oder drücken Sie F5.
    
    Das Projekt wird kompiliert und das Formular im Vorschaufenster angezeigt.
    
4. Führen Sie eine Interaktion mit dem Formular aus, bis eine Codezeile mit einem Haltepunkt ermittelt wird.
    
    Der Fokus wechselt zurück zum Code-Editor.
    
5. Klicken Sie im Menü **Debuggen** auf **Weiter**, oder drücken Sie F5.
    
6. Wenn Sie das Debuggen abgeschlossen haben, schließen Sie das Vorschaufenster, oder klicken Sie im Menü **Debuggen** auf **Debuggen beenden**.
    
> [!NOTE]
> Zum Debuggen einer InfoPath-Formularvorlage mit verwalteten Code bei Verwendung eines Objektmodellmmitglieds, das volle Vertrauenswürdigkeit erfordert, müssen Sie die Formularvorlage konfigurieren, wie unter Vorschau und Debuggen von Formularvorlagen beschrieben, für die volle Vertrauenswürdigkeit erforderlich [ist.](how-to-preview-and-debug-form-templates-that-require-full-trust.md) 
  
## <a name="using-a-sample-data-file"></a>Verwenden einer Beispieldatendatei

Standardmäßig wird für das Debuggen und die Vorschau die Datei "template.xml" verwendet, die beim Erstellen einer Formularvorlage erstellt wird. Sie können eine eigene Datendatei erstellen und angeben, dass diese Datei zum Anzeigen der Vorschau oder zum Debuggen verwendet wird, indem Sie eine der folgenden Verfahren verwenden.  
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>So geben Sie eine Beispieldatendatei an, die beim Debuggen oder Anzeigen der Vorschau in Visual Studio Tools for Applications verwendet werden soll

1. Öffnen Sie die Formularvorlage im InfoPath-Entwurfsmodus, um die Datei "template.xml" anzuzeigen.
    
2. Klicken Sie auf die Registerkarte **Datei**, klicken Sie auf **Speichern**, dann auf **Formularvorlage speichern als** und dann auf **Quelldateien**.
    
3. Speichern Sie die Formularvorlagendateien in einem Ordner, und öffnen Sie dann die Datei template.xml in einem Text-Editor.
    
4. Erstellen Sie mit den gewünschten Beispieldaten eine Datei mit derselben Struktur wie die Datei "template.xml", und speichern Sie sie.
    
5. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
6. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Vorschau**, und geben Sie dann unter **Beispieldaten** im Feld **Pfad** die Beispieldaten an, die Sie erstellt haben. 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Angeben einer Benutzerrolle zur Verwendung während des Debuggens oder des Anzeigens der Vorschau

Wenn für das Formular, mit dem Sie arbeiten, Benutzerrollen definiert wurden, können Sie eine Benutzerrolle angeben, die während des Debuggens oder des Anzeigens der Formularvorschau verwendet werden soll. Weitere Informationen zum Definieren von Benutzerrollen finden Sie in der InfoPath-Hilfe, wenn Sie nach "Benutzerrolle" suchen.
  
> [!NOTE]
> Die Option zum Angeben einer Benutzerrolle ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformulare** festgelegt ist. Benutzerrollen werden in Formularvorlagen, die über InfoPath Forms Services im Browser geöffnet werden, nicht unterstützt. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>So geben Sie eine Rolle an, die während des Debuggens oder des Anzeigens der Vorschau verwendet werden soll

1. Wenn Sie in Visual Studio 2012 arbeiten, wechseln Sie zum InfoPath-Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Vorschau**, und geben Sie dann im Dropdownfeld **Vorschau anzeigen als** die zu verwendende Benutzerrolle an. 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>Angeben einer Domäne zur Verwendung während des Debuggens oder des Anzeigens der Vorschau

Sie können eine Vorschau eines Formulars so anzeigen, als ob das Formular in einer bestimmten Domäne veröffentlicht würde. Diese Einstellung wird nur angewendet, wenn die Sicherheitsebene der Formularvorlage explizit auf **Domäne** festgelegt wurde.
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>So geben Sie eine Domäne an, die beim Debuggen oder beim Anzeigen der Vorschau verwendet werden soll

1. Wenn Sie in Visual Studio 2012 arbeiten, wechseln Sie zum InfoPath-Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Vorschau**, und geben Sie dann im Feld **Domäne** die beim Anzeigen der Vorschau und beim Debuggen zu verwendende Domäne an. 
    
4. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung**, deaktivieren Sie das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln**, und klicken Sie dann auf **Domäne**.
    

