---
title: Hinzufügen eines Ereignishandlers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], Hinzufügen von Ereignishandlern,Sign-Ereignis [InfoPath 2007],ViewSwitched-Ereignis [InfoPath 2007],Ereignisbehandlung [InfoPath 2007],Merge-Ereignis [InfoPath 2007],Validating event [InfoPath 2007],Submit event [InfoPath 2007],Save event [InfoPath 2007] ,Loading-Ereignis [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern zu einer Formularvorlage für verwalteten Microsoft InfoPath mithilfe von Visual Studio 2012 beschrieben. Wenn Sie einer Formularvorlage einen Ereignishandler hinzufügen möchten, beginnen Sie mit dem Öffnen der Formularvorlage im InfoPath-Designer, und wählen Sie dann den entsprechenden Benutzeroberflächenbefehl für das Ereignis aus, für das Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis im InfoPath Designer ausgewählt haben, wechselt der Fokus automatisch zum Skeletonereignishandler für dieses Ereignis im Visual Studio 2012-Code-Editor.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427185"
---
# <a name="add-an-event-handler"></a>Hinzufügen eines Ereignishandlers

In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern zu einer Formularvorlage für verwalteten Microsoft InfoPath mithilfe von Visual Studio 2012 beschrieben. Wenn Sie einer Formularvorlage einen Ereignishandler hinzufügen möchten, beginnen Sie mit dem Öffnen der Formularvorlage im InfoPath-Designer, und wählen Sie dann den entsprechenden Benutzeroberflächenbefehl für das Ereignis aus, für das Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis im InfoPath Designer ausgewählt haben, wechselt der Fokus automatisch zum Skeletonereignishandler für dieses Ereignis im Visual Studio 2012-Code-Editor.
  
> [!IMPORTANT]
> Sie sollten immer die Benutzeroberfläche von InfoPath Designer verwenden, um einen Ereignishandler hinzuzufügen. Durch hinzufügen eines Ereignishandlers mit der Benutzeroberfläche wird Ereignisbindungscode in der **InternalStartup-Methode** der Datei FormCode.cs oder FormCode.vb in Ihrem Formularvorlagenprojekt generiert. Sie sollten die **InternalStartup-Methode nicht** erstellen oder selbst keinen zusätzlichen Code hinzufügen. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Hinzufügen eines Ereignishandlers für das Click-Ereignis eines Schaltflächen-Steuerelements

1. Öffnen Sie die Formularvorlage im InfoPath Designer, und fügen Sie dem Formular ein **Button-Steuerelement** hinzu. 
    
2. Klicken Sie auf die Schaltfläche, und klicken Sie dann auf der Registerkarte **Eigenschaften** des Menübands auf **Benutzerdefinierter Code**.
    
    Der Fokus wechselt zum Skeletonereignishandler für das [Clicked-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) im Visual Studio 2012-Code-Editor. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Hinzufügen eines Ereignishandlers für das Ereignis "Changing", "Validating" oder "Changed" eines Felds oder einer Gruppe

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie mit der rechten Maustaste auf ein an das Feld oder die Gruppe gebundenes Dateneingabe-Steuerelement, wie z. B. ein Steuerelement vom Typ **Textfeld**. 
    
3. Zeigen Sie **auf Programmierung,** und klicken Sie dann auf das Ereignis, für das Sie einen Ereignishandler erstellen möchten. Der Fokus wechselt zum Skeletonereignishandler für das [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) -, [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) - oder [Changed-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) im Visual Studio 2012-Code-Editor. 
    
    > [!NOTE]
    > Der Befehl zum Erstellen eines Ereignishandlers für das **Changing-Ereignis** ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformular festgelegt ist.** Dies liegt daran, dass das **Changing-Ereignis** nicht in der Geschäftslogik von Formularvorlagen unterstützt wird, die in Dokumentbibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services. Zum Erstellen eines Ereignishandlers für das **Changing-Ereignis** müssen Sie die Kompatibilitätseinstellung in **InfoPath-Editor** im InfoPath-Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei,** klicken Sie auf **Formularoptionen,** klicken Sie auf **Kompatibilität,** und legen Sie dann **den** Formulartyp auf **InfoPath-Editorformular fest.** 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "Loading", "ViewSwitched", "ContextChanged" und "Sign" eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf der Registerkarte **Entwickler** des Menübands auf das Formularereignis, für das Sie einen Ereignishandler schreiben möchten. 
    
    Der Fokus wechselt zum Skeletonereignishandler für das [Loading-,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) [ViewSwitched-,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) [ContextChanged-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) im Visual Studio 2012-Code-Editor. 
    
    > [!NOTE]
    > Die Befehle zum Erstellen eines Ereignishandlers für die [ContextChanged-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign-Ereignisse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) sind nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformular festgelegt ist.** Dies liegt daran, dass diese Ereignisse nicht in der Geschäftslogik von Formularvorlagen unterstützt werden, die in Dokumentbibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services. Zum Erstellen eines Ereignishandlers für das [ContextChanged-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) müssen Sie die Kompatibilitätseinstellung in **InfoPath Editor Form** im InfoPath Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei,** klicken Sie auf **Formularoptionen,** klicken Sie auf **Kompatibilität,** und legen Sie dann **den** Formulartyp auf **InfoPath-Editorformular fest.** 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Submit-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie **auf die** Registerkarte Datei, **klicken** Sie auf der Registerkarte **Informationen** auf Absenden an, und klicken Sie dann auf ** Absenden von Optionen **.
    
3. Klicken Sie auf **Übermitteln dieses Formulars durch Benutzer zulassen**, klicken Sie auf **Benutzerdefinierte Aktion mithilfe von Code ausführen**, und klicken Sie dann auf **Code bearbeiten**.
    
    Der Fokus wechselt zum Skeletonereignishandler für das [Submit-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) im Visual Studio 2012-Code-Editor. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Save-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Speichern**, aktivieren Sie das Kontrollkästchen **Speichern erfolgt mittels benutzerdefiniertem Code**, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeletonereignishandler für das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) im Visual Studio 2012-Code-Editor. 
    
    > [!NOTE]
    > Das **Kontrollkästchen Speichern mit benutzerdefiniertem** Code ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **InfoPath Forms Services.** Dies liegt daran, dass das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) nicht in der Geschäftslogik von Formularvorlagen unterstützt wird, die in Dokumentbibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services. Zum Erstellen eines Ereignishandlers für das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) müssen Sie die Kompatibilitätseinstellung in **InfoPath-Editorformular** im InfoPath-Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei,** klicken Sie auf **Formularoptionen,** klicken Sie auf **Kompatibilität,** und legen Sie dann **den** Formulartyp auf **InfoPath-Editorformular fest.** 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das VersionUpgrade-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Versionsverwaltung**, wählen Sie im Dropdownfeld **Vorhandene Formulare aktualisieren** die Option **Benutzerdefiniertes Ereignis verwenden** aus, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeletonereignishandler für das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) im Visual Studio 2012-Code-Editor. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Merge-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Erweitert**, aktivieren Sie die Kontrollkästchen **Zusammenführen von Formularen aktivieren** und **Mithilfe benutzerdefiniertem Code zusammenführen**, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeletonereignishandler für das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) im Visual Studio 2012-Code-Editor. 
    
    > [!NOTE]
    > Das **Kontrollkästchen Formular zusammenführen** aktivieren ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **InfoPath Forms Services.** Der Grund dafür ist, dass das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) nicht in der Geschäftslogik von Formularvorlagen unterstützt wird, die in Dokumentbibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services. Zum Erstellen eines Ereignishandlers für das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) müssen Sie die Kompatibilitätseinstellung in **InfoPath Editor Form** im InfoPath Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei,** klicken Sie auf **Formularoptionen,** klicken Sie auf **Kompatibilität,** und legen Sie dann **den** Formulartyp auf **InfoPath-Editorformular fest.** 
  
## <a name="see-also"></a>Siehe auch



[Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)

