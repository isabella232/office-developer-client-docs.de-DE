---
title: Öffnen oder Konvertieren einer mit dem InfoPath-Toolkit erstellten Formularvorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Konvertieren von Formularvorlagen [InfoPath 2007], InfoPath Toolkit, Öffnen von Formularvorlagen aus, Formularvorlagen [InfoPath 2007], öffnen, InfoPath 2007, Konvertieren von InfoPath Toolkit-Formularvorlagen, Öffnen von Formularvorlagen [InfoPath 2007], Formularvorlagen [InfoPath 2007], konvertieren, Skript [InfoPath 2007], konvertieren in verwalteten Code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Wenn Sie eine InfoPath 2003-Formularvorlage mit verwaltetem Code mit einem der InfoPath 2003-Toolkits für Visual Studio erstellt haben und die Kompatibilität mit InfoPath 2003 beibehalten möchten, können Sie das Formularvorlagenprojekt weiterhin bearbeiten und weiterentwickeln, indem Sie es in Microsoft InfoPath und Visual Studio 2012.
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300112"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Öffnen oder Konvertieren einer mit dem InfoPath-Toolkit erstellten Formularvorlage

Wenn Sie eine InfoPath 2003-Formularvorlage mit verwaltetem Code mit einem der InfoPath 2003-Toolkits für Visual Studio erstellt haben und die Kompatibilität mit InfoPath 2003 beibehalten möchten, können Sie das Formularvorlagenprojekt weiterhin bearbeiten und weiterentwickeln, indem Sie es in Microsoft InfoPath und Visual Studio 2012.
  
Alternativ können Sie den Code im InfoPath 2003-Projekt migrieren und aktualisieren, um das neue .NET-Objektmodell zu verwenden, das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellt wird. Auf diese Weise muss der gesamte Code erneut geschrieben werden, um Mitglieder des **Microsoft. Office. InfoPath** -Namespaces zu verwenden, aber der gesamte Code aus dem vorherigen Projekt wird beibehalten und von **#if InfoPathManagedObjectModel** und **#endif **(C#) oder **#If InfoPathManagedObject-modell** und **#End If** (Visual Basic)-Anweisungen für Ihren Verweis. 
  
In den folgenden Verfahren wird beschrieben, wie Sie eine mit dem InfoPath-Toolkit erstellte Formularvorlage mit verwaltetem Code öffnen und die Kompatibilität mit InfoPath 2003 verwalten oder migrieren und auf das neue InfoPath-Objektmodell aktualisieren. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code unter Beibehaltung der Kompatibilität mit InfoPath 2003 mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf der Registerkarte **Datei** auf **Öffnen** . 
    
2. Navigieren Sie im Dialogfeld **im Entwurfsmodus öffnen** zu dem Projektordner, in dem das InfoPath Toolkit-Formularvorlagenprojekt gespeichert wird. 
    
    Standardmäßig handelt es sich um einen Ordner in `C:\Users\` *username* `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   sie können den ordner auch an den speicherort verschieben, an dem InfoPath Visual Studio 2012-projekte speichert, die standard `C:\Users\` mäßig *username*  `\Documents\InfoPath Projects`
    
3. Klicken Sie auf die Datei mit dem Namen Manifest. xsf, und klicken Sie dann auf **Öffnen**.
    
4. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.
    
5. Die Meldung "Diese Formularvorlage muss gespeichert werden, bevor Sie Visual Basic- oder C#-Code hinzufügen können." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
6. Navigieren Sie zu dem gewünschten Speicherort für die Datei, benennen Sie die Datei, und klicken Sie dann auf **Speichern**.
    
7. Die Meldung "Dieser Code wurde mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio erstellt. InfoPath muss das Toolkitprojekt in ein neues Format migrieren." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
8. Wählen Sie die Visual Studio-Projektmappendatei (. sln) für das Projekt aus, und klicken Sie dann auf **Öffnen**.
    
9. Die Meldung "Das Projekt wurde migriert." wird angezeigt, wenn der Migrationsvorgang abgeschlossen ist. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
10. Die Meldung "Im Code dieses Formulars wird das Objektmodell von InfoPath 2003 verwendet." wird mit der Frage "Möchten Sie den Code aktualisieren, damit das Microsoft Office InfoPath-Objektmodell verwendet wird?" angezeigt. Klicken Sie auf **Nein** , um die Kompatibilität mit InfoPath 2003 beizubehalten und weiterhin mit dem vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellten Objektmodell zu arbeiten. 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwaltetem Code, die mit InfoPath 2003 kompatibel sind, finden Sie unter [entwickeln von Formularvorlagen mithilfe des infopath 2003-Objektmodells](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code und Aktualisieren dieser Formularvorlage für die Verwendung des neuen InfoPath-Objektmodells mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf der Registerkarte **Datei** auf **Öffnen** . 
    
2. Klicken Sie unter **Formularvorlage öffnen** auf **Auf meinem Computer**.
    
3. Navigieren Sie im Dialogfeld **im Entwurfsmodus öffnen** zu dem Projektordner, in dem das InfoPath Toolkit-Formularvorlagenprojekt gespeichert wird. 
    
    Standardmäßig handelt es sich um einen Ordner `C:\Users\` in *username* `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   sie können den ordner auch an den speicherort verschieben, an dem InfoPath Visual Studio 2012-projekte speichert, die standard `C:\Users\` mäßig *username*  `\Documents\InfoPath Projects`
    
4. Klicken Sie auf die Datei mit dem Namen Manifest. xsf, und klicken Sie dann auf **Öffnen**.
    
5. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.
    
6. Die Meldung "Diese Formularvorlage muss gespeichert werden, bevor Sie Visual Basic- oder C#-Code hinzufügen können." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
7. Navigieren Sie zu dem gewünschten Speicherort für die Datei, benennen Sie die Datei, und klicken Sie dann auf **Speichern**.
    
8. Die Meldung "Dieser Code wurde mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio erstellt. InfoPath muss das Toolkitprojekt in ein neues Format migrieren." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
9. Wählen Sie die Visual Studio-Projektmappendatei (. sln) für das Projekt aus, und klicken Sie dann auf **Öffnen**.
    
10. Die Meldung "Das Projekt wurde migriert." wird angezeigt, wenn der Migrationsvorgang abgeschlossen ist. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
11. Die Meldung "Im Code dieses Formulars wird das Objektmodell von InfoPath 2003 verwendet." wird mit der Frage "Möchten Sie den Code aktualisieren, damit das Microsoft Office InfoPath-Objektmodell verwendet wird?" angezeigt. Klicken Sie auf **Ja** , um die Formularvorlage so zu aktualisieren, dass das vom [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace bereitgestellte neue verwaltete Codeobjektmodell verwendet wird. 
    
    Der Formularcode wird im Code-Editor von Visual Studio 2012 mit vollständigem Code aus dem vorherigen Projekt geöffnet, umgeben von **#if** **InfoPathManagedObjectModel** und **#endif** (C#) oder **#If InfoPathManagedObjectModel** und **#End, wenn **(Visual Basic)-Anweisungen für Ihren Verweis. Der gesamte Code muss erneut geschrieben werden, um Member des Objektmodells zu verwenden, das vom **Microsoft. Office. InfoPath** -Namespace bereitgestellt wird. 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwaltetem Code, die das neue InfoPath-Objektmodell mit verwaltetem Code verwenden, finden Sie unter [entwickeln von InfoPath-Formularvorlagen mit Code](developing-infopath-form-templates-with-code.md).
    

