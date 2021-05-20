---
title: Öffnen oder Konvertieren einer Formularvorlage, die mit dem InfoPath Toolkit erstellt wurde
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Konvertieren von Formularvorlagen [infopath 2007],InfoPath Toolkit, Öffnen von Formularvorlagen aus,Formularvorlagen [InfoPath 2007], opening,InfoPath 2007, Konvertieren von InfoPath Toolkit-Formularvorlagen,Öffnen von Formularvorlagen [InfoPath 2007],Formularvorlagen [InfoPath 2007], Konvertieren,Skript [InfoPath 2007], Konvertieren in verwalteten Code
localization_priority: Normal
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Wenn Sie eine Formularvorlage für verwalteten Code in InfoPath 2003 mithilfe eines der InfoPath 2003 Toolkits für Visual Studio erstellt haben und die Kompatibilität mit InfoPath 2003 beibehalten möchten, können Sie ihr Formularvorlagenprojekt weiter bearbeiten und weiterentwickeln, indem Sie es in Microsoft InfoPath und Visual Studio 2012 öffnen.
ms.openlocfilehash: 0acbfab4a83a71d94a1c70a667a963056f5b9a38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428585"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Öffnen oder Konvertieren einer Formularvorlage, die mit dem InfoPath Toolkit erstellt wurde

Wenn Sie eine Formularvorlage für verwalteten Code in InfoPath 2003 mithilfe eines der InfoPath 2003 Toolkits für Visual Studio erstellt haben und die Kompatibilität mit InfoPath 2003 beibehalten möchten, können Sie ihr Formularvorlagenprojekt weiter bearbeiten und weiterentwickeln, indem Sie es in Microsoft InfoPath und Visual Studio 2012 öffnen.
  
Alternativ können Sie den Code in Ihrem InfoPath 2003-Projekt migrieren und aktualisieren, um das neue .NET-Objektmodell zu verwenden, das von [Microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Dabei muss der ganze Code neu geschrieben werden, um Mitglieder der **Microsoft.Office. InfoPath-Namespace,** aber der ganze Code aus Dem vorherigen Projekt wird beibehalten und von **#if InfoPathManagedObjectModel** und **#endif** (C#) oder **#If InfoPathManagedObject Model** und #End **If** (Visual Basic)-Anweisungen für Ihren Verweis umgeben. 
  
In den folgenden Verfahren wird beschrieben, wie Sie eine formularvorlage für verwalteten Code öffnen, die mithilfe des InfoPath Toolkits erstellt wurde, und die Kompatibilität mit InfoPath 2003 bzw. das Migrieren und Upgrade auf das neue InfoPath-Objektmodell beibehalten. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code unter Beibehaltung der Kompatibilität mit InfoPath 2003 mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath Designer, und klicken Sie **dann** auf der Registerkarte **Datei** auf Öffnen. 
    
2. Navigieren Sie im Dialogfeld **Im Entwurfsmodus** öffnen zu dem Projektordner, in dem das Formularvorlagenprojekt des InfoPath Toolkits gespeichert wird. 
    
    Standardmäßig ist dies ein Ordner mit Benutzername `C:\Users\`  `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   Sie können den Ordner auch an den Speicherort verschieben, an dem InfoPath Visual Studio 2012-Projekte speichert, der standardmäßig Benutzername `C:\Users\` *ist.*  `\Documents\InfoPath Projects`
    
3. Klicken Sie auf die Datei mit dem Namen manifest.xsf, und klicken Sie dann auf **Öffnen**.
    
4. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.
    
5. Die Meldung "Diese Formularvorlage muss gespeichert werden, bevor Sie Visual Basic- oder C#-Code hinzufügen können." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
6. Navigieren Sie zu dem gewünschten Speicherort für die Datei, benennen Sie die Datei, und klicken Sie dann auf **Speichern**.
    
7. Die Meldung "Dieser Code wurde mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio erstellt. InfoPath muss das Toolkitprojekt in ein neues Format migrieren." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
8. Wählen Sie Visual Studio Projektmappendatei (SLN) für das Projekt aus, und klicken Sie dann auf **Öffnen**.
    
9. Die Meldung "Das Projekt wurde migriert." wird angezeigt, wenn der Migrationsvorgang abgeschlossen ist. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
10. Die Meldung "Im Code dieses Formulars wird das Objektmodell von InfoPath 2003 verwendet." wird mit der Frage "Möchten Sie den Code aktualisieren, damit das Microsoft Office InfoPath-Objektmodell verwendet wird?" angezeigt. Klicken **Sie auf Nein,** um die Kompatibilität mit InfoPath 2003 zu erhalten und die Arbeit mit dem objektmodell fortzufahren, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt wird. 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwalteten Code, die mit InfoPath 2003 kompatibel sind, finden Sie unter [Developing Form Templates Using the InfoPath 2003 Object Model](developing-form-templates-using-the-infopath-2003-object-model.md).
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code und Aktualisieren dieser Formularvorlage für die Verwendung des neuen InfoPath-Objektmodells mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath Designer, und klicken Sie **dann** auf der Registerkarte **Datei** auf Öffnen. 
    
2. Klicken Sie unter **Formularvorlage öffnen** auf **Auf meinem Computer**.
    
3. Navigieren Sie im Dialogfeld **Im Entwurfsmodus** öffnen zu dem Projektordner, in dem das Formularvorlagenprojekt des InfoPath Toolkits gespeichert wird. 
    
    Standardmäßig ist dies ein Ordner mit Benutzername `C:\Users\`  `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   Sie können den Ordner auch an den Speicherort verschieben, an dem InfoPath Visual Studio 2012-Projekte speichert, der standardmäßig Benutzername `C:\Users\` *ist.*  `\Documents\InfoPath Projects`
    
4. Klicken Sie auf die Datei mit dem Namen manifest.xsf, und klicken Sie dann auf **Öffnen**.
    
5. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.
    
6. Die Meldung "Diese Formularvorlage muss gespeichert werden, bevor Sie Visual Basic- oder C#-Code hinzufügen können." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
7. Navigieren Sie zu dem gewünschten Speicherort für die Datei, benennen Sie die Datei, und klicken Sie dann auf **Speichern**.
    
8. Die Meldung "Dieser Code wurde mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio erstellt. InfoPath muss das Toolkitprojekt in ein neues Format migrieren." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
9. Wählen Sie Visual Studio Projektmappendatei (SLN) für das Projekt aus, und klicken Sie dann auf **Öffnen**.
    
10. Die Meldung "Das Projekt wurde migriert." wird angezeigt, wenn der Migrationsvorgang abgeschlossen ist. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
11. Die Meldung "Im Code dieses Formulars wird das Objektmodell von InfoPath 2003 verwendet." wird mit der Frage "Möchten Sie den Code aktualisieren, damit das Microsoft Office InfoPath-Objektmodell verwendet wird?" angezeigt. Klicken **Sie auf Ja,** um die Formularvorlage so zu aktualisieren, dass das neue objektmodell für verwalteten Code verwendet wird, das von [Microsoft.Office. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
    
    Der Formularcode wird im Visual Studio 2012-Code-Editor geöffnet, und der code aus Dem vorherigen Projekt wird von **den Anweisungen #if** **InfoPathManagedObjectModel** und **#endif** (C#) oder **#If InfoPathManagedObjectModel** und **#End If** (Visual Basic) für Ihren Verweis umgeben. Dieser Code muss neu geschrieben werden, um Elemente des objektmodells zu verwenden, das von **Microsoft.Office. InfoPath-Namespace.** 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwalteten Code, die das neue Objektmodell für verwalteten Code von InfoPath verwenden, finden Sie unter [Developing InfoPath Form Templates with Code](developing-infopath-form-templates-with-code.md).
    

