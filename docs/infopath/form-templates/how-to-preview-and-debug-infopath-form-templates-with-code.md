---
title: Anzeigen der Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Debuggen von Formularvorlagen [InfoPath 2007], Formularvorlagen [InfoPath 2007], Vorschau, Debuggen [InfoPath 2007], Formularvorlagen für verwalteten Code, Formularvorlagen [InfoPath 2007], InfoPath 2007-Debuggen, Debuggen Vorschau von Formularvorlagen [Infopath 2007] Formularvorlagen, InfoPath 2007, Vorschau von Formularvorlagen
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath mit Visual Studio 2012 ermöglicht das Debuggen von Formularcode im Vorschaumodus ausgeführt. Wenn Sie das Debuggen von Formularcode starten, das Projekt wird kompiliert und InfoPath zeigt das Formular im InfoPath-Vorschaufenster. Wenn eine Codezeile, die einen Haltepunkt festgelegt hat wird es erreicht und der Fokus wechselt zum Code-Editor. Wenn Sie über einen Haltepunkt fortfahren, verschiebt den Fokus wieder auf das Vorschaufenster. Debuggen wird beendet, wenn Sie das Vorschaufenster schließen.
ms.openlocfilehash: c33a7740d5f5dba1f8443f020007a2942bc0fc3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790740"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a>Anzeigen der Vorschau und Debuggen von InfoPath-Formularvorlagen mit Code

Microsoft InfoPath mit Visual Studio 2012 ermöglicht das Debuggen von Formularcode im Vorschaumodus ausgeführt. Wenn Sie das Debuggen von Formularcode starten, das Projekt wird kompiliert und InfoPath zeigt das Formular im InfoPath-Vorschaufenster. Wenn eine Codezeile, die einen Haltepunkt festgelegt hat wird es erreicht und der Fokus wechselt zum Code-Editor. Wenn Sie über einen Haltepunkt fortfahren, verschiebt den Fokus wieder auf das Vorschaufenster. Debuggen wird beendet, wenn Sie das Vorschaufenster schließen.
  
Sie können die Formularoptionen für die Formularvorlage auch so ändern, dass Vorschau und Debuggen mithilfe einer bestimmten Benutzerrolle, einer Beispieldatendatei oder durch Angeben der Domäne ausgeführt werden, in der das Formular veröffentlicht wird.  
  
> [!NOTE]
> Es ist nicht möglich, Formularvorlagen Debuggen, nachdem sie während der Laufzeit von Visual Studio 2012 bereitgestellt werden. Dazu gehören Formularvorlagen, die nur mit InfoPath als auch diejenigen, die mithilfe von InfoPath und Webbrowser mithilfe des InfoPath Forms Services kompatibel sind kompatibel sind. Es ist jedoch möglich, die Werte eines Felds aus Code zur Laufzeit, das Ihnen bei der Geschäftslogik einer Formularvorlage Debuggen Anmeldung bei. Informationen dazu, wie folgt vor finden Sie unter [Log Werte an ein Feld für das Debugging](how-to-log-values-to-a-field-for-debugging.md). 
  
## <a name="debugging-in-preview-mode"></a>Debuggen im Vorschaumodus

### <a name="to-debug-an-infopath-project-in-preview-mode"></a>So debuggen Sie ein InfoPath-Projekt im Vorschaumodus

1. Erstellen Sie oder öffnen Sie eine InfoPath-Formularvorlage für verwalteten Code in Visual Studio 2012.
    
2. Legen Sie im Code-Editor im Formularcode mindestens einen Haltepunkt fest, indem Sie links neben der Codezeile, in der ein Haltepunkt eingefügt werden soll, auf die graue Leiste klicken.
    
    Ein roter Kreis wird angezeigt, und die Codezeile wird hervorgehoben, um darauf hinzuweisen, dass die Laufzeit an diesem Haltepunkt im Formularcode angehalten wird.
    
3. Klicken Sie im Menü **Debuggen** auf **Debuggen starten**. oder drücken Sie F5.
    
    Das Projekt wird kompiliert und das Formular im Vorschaufenster angezeigt.
    
4. Führen Sie eine Interaktion mit dem Formular aus, bis eine Codezeile mit einem Haltepunkt ermittelt wird.
    
    Der Fokus wechselt zurück zum Code-Editor.
    
5. Klicken Sie im Menü **Debuggen** auf **Weiter**. oder drücken Sie F5.
    
6. Wenn Sie nach Abschluss des Vorgangs sind Debuggen, schließen Sie das Vorschaufenster, oder klicken Sie im Menü **Debuggen** auf **Debuggen beenden**.
    
> [!NOTE]
> Um einer InfoPath-Formularvorlage für verwalteten Code Debuggen, wenn Sie ein Objektmodellmember verwenden, die volle Vertrauenswürdigkeit erfordert, müssen Sie die Formularvorlage konfigurieren, wie beschrieben in der [Vorschau und Debuggen von Formularvorlagen, die volle Vertrauenswürdigkeit erfordern](how-to-preview-and-debug-form-templates-that-require-full-trust.md). 
  
## <a name="using-a-sample-data-file"></a>Verwenden einer Beispieldatendatei

Standardmäßig wird für das Debuggen und die Vorschau die Datei "template.xml" verwendet, die beim Erstellen einer Formularvorlage erstellt wird. Sie können eine eigene Datendatei erstellen und angeben, dass diese Datei zum Anzeigen der Vorschau oder zum Debuggen verwendet wird, indem Sie eine der folgenden Verfahren verwenden.  
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a>So geben Sie eine Beispieldatendatei an, die beim Debuggen oder Anzeigen der Vorschau in Visual Studio Tools for Applications verwendet werden soll

1. Öffnen Sie die Formularvorlage im InfoPath-Entwurfsmodus, um die Datei "template.xml" anzuzeigen.
    
2. Klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Speichern**, klicken Sie auf **Vorlage speichern unter**, und klicken Sie dann auf **Quelldateien**.
    
3. Speichern Sie die Formularvorlagendateien in einem Ordner, und öffnen Sie dann die Datei template.xml in einem Text-Editor.
    
4. Erstellen Sie mit den gewünschten Beispieldaten eine Datei mit derselben Struktur wie die Datei "template.xml", und speichern Sie sie.
    
5. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
6. Klicken Sie auf die Kategorie **Vorschau** im Dialogfeld **Formularoptionen** , und geben Sie dann unter **Beispieldaten** Beispieldatendatei an, den Sie im Feld **Speicherort** erstellt haben. 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a>Angeben einer Benutzerrolle zur Verwendung während des Debuggens oder des Anzeigens der Vorschau

Wenn für das Formular, mit dem Sie arbeiten, Benutzerrollen definiert wurden, können Sie eine Benutzerrolle angeben, die während des Debuggens oder des Anzeigens der Formularvorschau verwendet werden soll. Weitere Informationen zum Definieren von Benutzerrollen finden Sie in der InfoPath-Hilfe, wenn Sie nach "Benutzerrolle" suchen.
  
> [!NOTE]
> Die Option zum Angeben einer Benutzerrolle ist nicht verfügbar, wenn die Einstellung für die Formularvorlage auf **Webbrowserformular**festgelegt ist. Benutzerrollen werden in Formularvorlagen geöffnet im Browser von InfoPath Forms Services nicht unterstützt. 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a>So geben Sie eine Rolle an, die während des Debuggens oder des Anzeigens der Vorschau verwendet werden soll

1. Wenn Sie in Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
3. Klicken Sie auf die Kategorie **Vorschau** im Dialogfeld **Formularoptionen** , und geben Sie die Rolle des Benutzers in der **Vorschau anzeigen als** Dropdown-Feld. 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a>Angeben einer Domäne zur Verwendung während des Debuggens oder des Anzeigens der Vorschau

Sie können ein Formular anzeigen, als ob es eine bestimmte Domäne veröffentlicht wurde. Diese Einstellung gilt nur, wenn die Sicherheitsstufe der Formularvorlage explizit auf die **Domäne**festgelegt ist.
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a>So geben Sie eine Domäne an, die beim Debuggen oder beim Anzeigen der Vorschau verwendet werden soll

1. Wenn Sie in Visual Studio 2012 arbeiten, wechseln Sie zu InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
3. Klicken Sie auf die Kategorie **Vorschau** im Dialogfeld **Formularoptionen** , und geben Sie die Domäne, beim Anzeigen einer Vorschau und Debuggen in das Feld **Domäne** verwendet. 
    
4. Klicken Sie auf die Kategorie **Sicherheit und Vertrauensstellung** im Dialogfeld **Formularoptionen** , deaktivieren Sie das Kontrollkästchen **Sicherheitsstufe automatisch ermitteln** , und klicken Sie dann auf **Domäne**.
    

