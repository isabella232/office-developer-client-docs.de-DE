---
title: Öffnen oder Konvertieren einer mit dem InfoPath-Toolkit erstellten Formularvorlage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- converting form templates [infopath 2007],InfoPath Toolkit, opening form templates from,form templates [InfoPath 2007], opening,InfoPath 2007, converting InfoPath Toolkit form templates,opening form templates [InfoPath 2007],form templates [InfoPath 2007], converting,script [InfoPath 2007], converting to managed code
ms.localizationpriority: medium
ms.assetid: af8eca2e-ba9a-4c37-94af-662815fff518
description: Wenn Sie eine InfoPath 2003-Formularvorlage mit verwaltetem Code mit einem der InfoPath 2003-Toolkits für Visual Studio erstellt haben und die Kompatibilität mit InfoPath 2003 aufrechterhalten möchten, können Sie ihr Formularvorlagenprojekt weiter entwickeln, indem Sie es in Microsoft InfoPath und Visual Studio 2012 öffnen.
ms.openlocfilehash: 8a8b4f35857d2ae55c60429c00803eadfdada091
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625847"
---
# <a name="open-or-convert-a-form-template-created-with-the-infopath-toolkit"></a>Öffnen oder Konvertieren einer mit dem InfoPath-Toolkit erstellten Formularvorlage

Wenn Sie eine InfoPath 2003-Formularvorlage mit verwaltetem Code mit einem der InfoPath 2003-Toolkits für Visual Studio erstellt haben und die Kompatibilität mit InfoPath 2003 aufrechterhalten möchten, können Sie ihr Formularvorlagenprojekt weiter entwickeln, indem Sie es in Microsoft InfoPath und Visual Studio 2012 öffnen.
  
Alternativ können Sie den Code in Ihrem InfoPath 2003-Projekt migrieren und aktualisieren, um das neue .NET-Objektmodell zu verwenden, das von [Microsoft.Office bereitgestellt wird. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) Dabei muss der gesamte Code neu geschrieben werden, um Mitglieder der **Microsoft.Office zu verwenden. InfoPath-Namespace,** aber der gesamte Code aus Dem vorherigen Projekt wird beibehalten und von **#if InfoPathManagedObjectModel-** und **#endif** -Anweisungen (C#) oder **#If InfoPathManagedObject Model** und #End **If-Anweisungen** (Visual Basic) für Den Verweis umgeben. 
  
In den folgenden Verfahren wird beschrieben, wie Sie eine Mithilfe des InfoPath-Toolkits erstellte Formularvorlage mit verwaltetem Code öffnen und die Kompatibilität mit InfoPath 2003 aufrechterhalten oder zum neuen InfoPath-Objektmodell migrieren und auf dieses aktualisieren. 
  
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-maintain-compatibility-with-infopath-2003-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code unter Beibehaltung der Kompatibilität mit InfoPath 2003 mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf der Registerkarte **"Datei"** auf **"Öffnen".** 
    
2. Navigieren Sie im Dialogfeld **"Im Entwurfsmodus öffnen"** zum Projektordner, in dem das InfoPath Toolkit-Formularvorlagenprojekt gespeichert ist. 
    
    Standardmäßig ist dies ein Ordner mit `C:\Users\` *Benutzername* `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   Sie können den Ordner auch an den Speicherort verschieben, an dem InfoPath Visual Studio 2012-Projekte speichert, was standardmäßig benutzername ist. `C:\Users\`   `\Documents\InfoPath Projects`
    
3. Klicken Sie auf die Datei mit dem Namen "manifest.xsf", und klicken Sie dann auf **"Öffnen".**
    
4. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.
    
5. Die Meldung "Diese Formularvorlage muss gespeichert werden, bevor Sie Visual Basic- oder C#-Code hinzufügen können." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
6. Navigieren Sie zu dem gewünschten Speicherort für die Datei, benennen Sie die Datei, und klicken Sie dann auf **Speichern**.
    
7. Die Meldung "Dieser Code wurde mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio erstellt. InfoPath muss das Toolkitprojekt in ein neues Format migrieren." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
8. Wählen Sie die Visual Studio Projektmappendatei (SLN) für das Projekt aus, und klicken Sie dann auf **"Öffnen".**
    
9. Die Meldung "Das Projekt wurde migriert." wird angezeigt, wenn der Migrationsvorgang abgeschlossen ist. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
10. Die Meldung "Im Code dieses Formulars wird das Objektmodell von InfoPath 2003 verwendet." wird mit der Frage "Möchten Sie den Code aktualisieren, damit das Microsoft Office InfoPath-Objektmodell verwendet wird?" angezeigt. Klicken Sie auf **"Nein",** um die Kompatibilität mit InfoPath 2003 beizubehalten und die Arbeit mit dem vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace bereitgestellten](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) Objektmodell fortzusetzen. 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwaltetem Code, die mit InfoPath 2003 kompatibel sind, finden Sie unter [Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells.](developing-form-templates-using-the-infopath-2003-object-model.md)
    
### <a name="open-a-managed-code-form-template-created-with-the-infopath-toolkit-and-upgrade-it-to-use-the-new-infopath-object-model-using-visual-studio-tools-for-applications"></a>Öffnen einer mit dem InfoPath Toolkit erstellten Formularvorlage mit verwaltetem Code und Aktualisieren dieser Formularvorlage für die Verwendung des neuen InfoPath-Objektmodells mithilfe von Visual Studio Tools for Applications

1. Öffnen Sie den InfoPath-Designer, und klicken Sie dann auf der Registerkarte **"Datei"** auf **"Öffnen".** 
    
2. Klicken Sie unter **Formularvorlage öffnen** auf **Auf meinem Computer**.
    
3. Navigieren Sie im Dialogfeld **"Im Entwurfsmodus öffnen"** zum Projektordner, in dem das InfoPath Toolkit-Formularvorlagenprojekt gespeichert ist. 
    
    Standardmäßig ist dies ein Ordner mit `C:\Users\` *Benutzername* `\Documents\Visual Studio Projects` auf dem Computer, auf dem das Projekt erstellt wurde.   Sie können den Ordner auch an den Speicherort verschieben, an dem InfoPath Visual Studio 2012-Projekte speichert, was standardmäßig benutzername ist. `C:\Users\`   `\Documents\InfoPath Projects`
    
4. Klicken Sie auf die Datei mit dem Namen "manifest.xsf", und klicken Sie dann auf **"Öffnen".**
    
5. Klicken Sie auf der Registerkarte **Entwickler** auf **Code-Editor**.
    
6. Die Meldung "Diese Formularvorlage muss gespeichert werden, bevor Sie Visual Basic- oder C#-Code hinzufügen können." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
7. Navigieren Sie zu dem gewünschten Speicherort für die Datei, benennen Sie die Datei, und klicken Sie dann auf **Speichern**.
    
8. Die Meldung "Dieser Code wurde mit einem der InfoPath 2003 Toolkits für Microsoft Visual Studio erstellt. InfoPath muss das Toolkitprojekt in ein neues Format migrieren." wird angezeigt. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
9. Wählen Sie die Visual Studio Projektmappendatei (SLN) für das Projekt aus, und klicken Sie dann auf **"Öffnen".**
    
10. Die Meldung "Das Projekt wurde migriert." wird angezeigt, wenn der Migrationsvorgang abgeschlossen ist. Klicken Sie auf **OK**, um den Vorgang fortzusetzen. 
    
11. Die Meldung "Im Code dieses Formulars wird das Objektmodell von InfoPath 2003 verwendet." wird mit der Frage "Möchten Sie den Code aktualisieren, damit das Microsoft Office InfoPath-Objektmodell verwendet wird?" angezeigt. Klicken Sie auf **"Ja",** um die Formularvorlage so zu aktualisieren, dass das neue objektmodell mit verwaltetem Code verwendet wird, das von [Microsoft.Office bereitgestellt wird. InfoPath-Namespace.](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 
    
    Der Formularcode wird im Visual Studio 2012-Code-Editor mit dem gesamten Code aus dem vorherigen Projekt geöffnet, der von **#if** **InfoPathManagedObjectModel-** und **#endif** -Anweisungen (C#) oder **#If InfoPathManagedObjectModel-** und **#End If-Anweisungen** (Visual Basic) umgeben ist. Dieser gesamte Code muss neu geschrieben werden, um Elemente des vom Microsoft.Office bereitgestellten Objektmodells zu **verwenden. InfoPath-Namespace.** 
    
    Informationen zum Arbeiten mit Formularvorlagen mit verwaltetem Code, die das neue InfoPath-Objektmodell mit verwaltetem Code verwenden, finden Sie unter [Entwickeln von InfoPath-Formularvorlagen mit Code.](developing-infopath-form-templates-with-code.md)
    

