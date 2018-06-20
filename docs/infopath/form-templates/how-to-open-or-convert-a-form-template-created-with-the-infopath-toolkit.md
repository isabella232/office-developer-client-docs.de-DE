---
title: Öffnen oder Konvertieren einer mit dem InfoPath Toolkit erstellten Formularvorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Konvertieren von Formularvorlagen [Infopath 2007] InfoPath Toolkit, Öffnen von Formularvorlagen von Formularvorlagen [InfoPath 2007], öffnen, InfoPath 2007, Konvertieren von Formularvorlagen für InfoPath Toolkit, Öffnen von Formularvorlagen [InfoPath 2007], [InfoPath-Formularvorlagen 2007], verwalteten konvertieren in Konvertieren von Skript [InfoPath 2007], code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Wenn Sie eine InfoPath 2003 verwaltetem Code Formularvorlage, die mit einem der InfoPath 2003 Toolkits für Visual Studio erstellt und Kompatibilität mit InfoPath 2003 beibehalten möchten, können Sie weiterhin arbeiten und weiterzuentwickeln Ihrer Formularvorlagenprojekt durch Öffnen des Formulars in Microsoft InfoPath und Visual Studio 2012.
ms.openlocfilehash: 7ca6a676c9db740b6b176783273a523715032387
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790754"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Öffnen oder Konvertieren einer mit dem InfoPath Toolkit erstellten Formularvorlage

Wenn Sie eine InfoPath 2003 verwaltetem Code Formularvorlage, die mit einem der InfoPath 2003 Toolkits für Visual Studio erstellt und Kompatibilität mit InfoPath 2003 beibehalten möchten, können Sie weiterhin arbeiten und weiterzuentwickeln Ihrer Formularvorlagenprojekt durch Öffnen des Formulars in Microsoft InfoPath und Visual Studio 2012.
  
Alternativ können Sie migrieren und aktualisieren den Code in Ihrem InfoPath 2003-Projekt mit dem neuen Objektmodell für .NET vom [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt. Dabei müssen alle des Codes neu geschrieben werden, der Member des **Microsoft.Office.InfoPath** -Namespaces verwenden, jedoch ist der gesamte Code aus dem vorherigen Projekt beibehalten und umgeben von **#if InfoPathManagedObjectModel** und **#endif **(C#) oder **#If InfoPathManagedObject Modell** und **#End If** (Visual Basic)-Anweisungen für den Verweis. 
  
Die folgenden Verfahren wird beschrieben, wie mithilfe des InfoPath Toolkit erstellte Formularvorlage verwaltetem Code öffnen und Beibehaltung der Kompatibilität mit InfoPath 2003 oder migrieren und aktualisieren Sie auf das neue InfoPath-Objektmodell. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code unter Beibehaltung der Kompatibilität mit InfoPath 2003 mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf der Registerkarte **Datei** auf **Öffnen** . 
    
2. Navigieren Sie zum Projektordner, in dem das Formularvorlagenprojekt InfoPath Toolkit gespeichert ist, klicken Sie im Dialogfeld **im Entwurfsmodus öffnen** . 
    
    Standardmäßig werden in einem Ordner `C:\Users\` *Username* `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   Oder Sie können den Ordner verschieben, zu dem Speicherort, in dem InfoPath Projekte mit Visual Studio 2012, speichert, standardmäßig ist `C:\Users\` *Benutzername*  `\Documents\InfoPath Projects`
    
3. Klicken Sie auf die Datei mit dem Namen manifest.xsf, und klicken Sie dann auf **Öffnen**.
    
4. Klicken Sie auf der Registerkarte **Entwicklertools** auf **Code-Editor**.
    
5. Die Meldung "Diese Formularvorlage gespeichert werden muss, bevor Sie Visual Basic oder C#-Code hinzufügen können" angezeigt wird. Klicken Sie auf **OK** , um den Vorgang fortzusetzen. 
    
6. Navigieren Sie zu dem Speicherort, in dem Sie speichern Sie die Datei, nennen Sie die Datei, und klicken Sie dann auf **Speichern**möchten.
    
7. Die Meldung "dieses Codes mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio. erstellt wurde InfoPath muss das Toolkitprojekt in ein neues Format migrieren"wird angezeigt. Klicken Sie auf **OK** , um den Vorgang fortzusetzen. 
    
8. Wählen Sie die Datei Visual Studio-Lösungsdatei (.sln) für das Projekt, und klicken Sie dann auf **Öffnen**.
    
9. Die Meldung "Ihr Projekt migriert wurde" wird angezeigt, wenn der Migrationsprozess abgeschlossen ist. Klicken Sie auf **OK** , um den Vorgang fortzusetzen. 
    
10. Wird die Meldung "der Code in diesem Formular das InfoPath 2003-Objektmodell verwendet" mit der Aufforderung angezeigt "möchten Sie den Code, um das Microsoft Office InfoPath-Objektmodell verwenden aktualisieren?" Klicken Sie auf **Nein** , die Kompatibilität mit InfoPath 2003 beibehalten werden und mit der [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellte Objektmodell arbeiten. 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwaltetem Code, die mit InfoPath 2003 kompatibel sind, finden Sie unter [Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code und Aktualisieren dieser Formularvorlage für die Verwendung des neuen InfoPath-Objektmodells mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf der Registerkarte **Datei** auf **Öffnen** . 
    
2. Klicken Sie unter **Öffnen einer Formularvorlage**klicken Sie auf **Auf meinem Computer**.
    
3. Navigieren Sie zum Projektordner, in dem das Formularvorlagenprojekt InfoPath Toolkit gespeichert ist, klicken Sie im Dialogfeld **im Entwurfsmodus öffnen** . 
    
    Standardmäßig werden in einem Ordner `C:\Users\` *Username* `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   Oder Sie können den Ordner verschieben, zu dem Speicherort, in dem InfoPath Projekte mit Visual Studio 2012, speichert, standardmäßig ist `C:\Users\` *Benutzername*  `\Documents\InfoPath Projects`
    
4. Klicken Sie auf die Datei mit dem Namen manifest.xsf, und klicken Sie dann auf **Öffnen**.
    
5. Klicken Sie auf der Registerkarte **Entwicklertools** auf **Code-Editor**.
    
6. Die Meldung "Diese Formularvorlage gespeichert werden muss, bevor Sie Visual Basic oder C#-Code hinzufügen können" angezeigt wird. Klicken Sie auf **OK** , um den Vorgang fortzusetzen. 
    
7. Navigieren Sie zu dem Speicherort, in dem Sie speichern Sie die Datei, nennen Sie die Datei, und klicken Sie dann auf **Speichern**möchten.
    
8. Die Meldung "dieses Codes mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio. erstellt wurde InfoPath muss das Toolkitprojekt in ein neues Format migrieren"wird angezeigt. Klicken Sie auf **OK** , um den Vorgang fortzusetzen. 
    
9. Wählen Sie die Datei Visual Studio-Lösungsdatei (.sln) für das Projekt, und klicken Sie dann auf **Öffnen**.
    
10. Die Meldung "Ihr Projekt migriert wurde" wird angezeigt, wenn der Migrationsprozess abgeschlossen ist. Klicken Sie auf **OK** , um den Vorgang fortzusetzen. 
    
11. Wird die Meldung "der Code in diesem Formular das InfoPath 2003-Objektmodell verwendet" mit der Aufforderung angezeigt "möchten Sie den Code, um das Microsoft Office InfoPath-Objektmodell verwenden aktualisieren?" Klicken Sie auf **Ja** , um das neue Objektmodell für verwalteten Code des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace verwenden, um die Formularvorlage aktualisieren. 
    
    Formularcode ist in Visual Studio 2012 Code-Editor mit den gesamten Code aus dem vorherigen Projekt umgeben von **#if** **InfoPathManagedObjectModel** und **#endif** (c#) oder **#If InfoPathManagedObjectModel** und **#End If geöffnet. **(Visual Basic)-Anweisungen für den Verweis. Alle dieses Codes müssen neu geschrieben werden, dass Mitglieder des Objektmodells vom **Microsoft.Office.InfoPath** -Namespace bereitgestellt. 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwaltetem Code, die das neue Objektmodell für InfoPath verwalteten Code verwenden, finden Sie unter [Entwickeln von InfoPath-Formularvorlagen mit Code](developing-infopath-form-templates-with-code.md).
    

