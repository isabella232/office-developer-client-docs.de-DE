---
title: Hinzufügen eines Ereignishandlers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- VersionUpgrade-Ereignis [InfoPath 2007], behandeln von Ereignissen [InfoPath 2007], Ändern des Ereignisses [InfoPath 2007], InfoPath 2007, Hinzufügen von Ereignishandlern, Changed-Ereignis [InfoPath 2007], Context-Ereignis [InfoPath 2007], Click-Ereignis [InfoPath 2007], Ereignisse [InfoPath 2007], Hinzufügen von Ereignishandlern, Signieren eines Ereignisses [InfoPath 2007], ViewSwitched-Ereignis [InfoPath 2007], Ereignisbehandlung [InfoPath 2007], zusammenFührungs Ereignis [InfoPath 2007], Validating-Ereignis [InfoPath 2007], Ereignis senden [InfoPath 2007], Ereignis speichern [InfoPath 2007], laden Ereignis [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern zu einer Microsoft InfoPath-Formularvorlage mit verwaltetem Code mithilfe von Visual Studio 2012 beschrieben. Wenn Sie einer Formularvorlage einen Ereignishandler hinzufügen möchten, beginnen Sie mit der im InfoPath-Designer geöffneten Formularvorlage, und wählen Sie dann den entsprechenden Benutzeroberflächenbefehl für das Ereignis aus, für das Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis im InfoPath-Designer ausgewählt haben, wechselt der Fokus automatisch zum Skelett-Ereignishandler für dieses Ereignis im Code-Editor von Visual Studio 2012.
ms.openlocfilehash: c6406ec1604355c59f4ee4818fdaea5d70f696bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427185"
---
# <a name="add-an-event-handler"></a>Hinzufügen eines Ereignishandlers

In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern zu einer Microsoft InfoPath-Formularvorlage mit verwaltetem Code mithilfe von Visual Studio 2012 beschrieben. Wenn Sie einer Formularvorlage einen Ereignishandler hinzufügen möchten, beginnen Sie mit der im InfoPath-Designer geöffneten Formularvorlage, und wählen Sie dann den entsprechenden Benutzeroberflächenbefehl für das Ereignis aus, für das Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis im InfoPath-Designer ausgewählt haben, wechselt der Fokus automatisch zum Skelett-Ereignishandler für dieses Ereignis im Code-Editor von Visual Studio 2012.
  
> [!IMPORTANT]
> Sie sollten immer die InfoPath-Designer-Benutzeroberfläche verwenden, um einen Ereignishandler hinzuzufügen. Durch Hinzufügen eines Ereignishandlers zur Benutzeroberfläche wird der Ereignisbindungscode in der **InternalStartup** -methode der FormCode.cs-oder FormCode. vb-Datei im Formularvorlagenprojekt generiert. Sie sollten die **InternalStartup** -Methode nicht erstellen oder selbst zusätzlichen Code hinzufügen. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Hinzufügen eines Ereignishandlers für das Click-Ereignis eines Schaltflächen-Steuerelements

1. Öffnen Sie die Formularvorlage im InfoPath-Designer, und fügen Sie dem Formular ein **Schaltflächen** Steuerelement hinzu. 
    
2. Klicken Sie auf die Schaltfläche, und klicken Sie dann auf der Registerkarte **Eigenschaften** des Menübands auf **Benutzerdefinierter Code**.
    
    Der Fokus wechselt zum Skelett-Ereignishandler für das [clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Hinzufügen eines Ereignishandlers für das Ereignis "Changing", "Validating" oder "Changed" eines Felds oder einer Gruppe

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie mit der rechten Maustaste auf ein an das Feld oder die Gruppe gebundenes Dateneingabe-Steuerelement, wie z. B. ein Steuerelement vom Typ **Textfeld**. 
    
3. Zeigen Sie auf **Programmierung**, und klicken Sie dann auf das Ereignis, für das Sie einen Ereignishandler erstellen möchten. Der Fokus wechselt zum Skelett-Ereignishandler für das [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) -, [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) -oder [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) -Ereignis im code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Der Befehl zum Erstellen eines Ereignishandlers für das **Changing** -Ereignis ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformular**festgelegt ist. Der Grund ist, dass das **Changing** -Ereignis in der Geschäftslogik von Formularvorlagen, die in dokumentBibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt wird. Zum Erstellen eines Ereignishandlers für das **Changing** -Ereignis müssen Sie die Kompatibilitätseinstellung in **InfoPath Editor** im InfoPath-Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei** , dann auf **Formularoptionen**, auf **Kompatibilität**und dann auf **** **InfoPath-Editor-Formular**Formulartyp festlegen. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "Loading", "ViewSwitched", "ContextChanged" und "Sign" eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Entwickler** des Menübands auf das Formularereignis, für das Sie einen Ereignishandler schreiben möchten. 
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) -, [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) -, [context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) -oder [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Die Befehle zum Erstellen eines Ereignishandlers für die [context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) -oder [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignisse sind nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformular**festgelegt ist. Der Grund ist, dass diese Ereignisse in der Geschäftslogik von Formularvorlagen, die in Dokumentbibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt werden. Zum Erstellen eines Ereignishandlers für das [context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) -oder [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis müssen Sie die Kompatibilitätseinstellung in **InfoPath-Editor-Formular** im InfoPath-Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei** , dann auf **Formularoptionen**, auf **Kompatibilität**und dann auf **** **InfoPath-Editor-Formular**Formulartyp festlegen. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Submit-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf die Registerkarte **Datei** , klicken Sie auf der Registerkarte **Info** auf **Senden an** , und klicken Sie dann auf * * Submit Options * *.
    
3. Klicken Sie auf **Übermitteln dieses Formulars durch Benutzer zulassen**, klicken Sie auf **Benutzerdefinierte Aktion mithilfe von Code ausführen**, und klicken Sie dann auf **Code bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Save-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Speichern**, aktivieren Sie das Kontrollkästchen **Speichern erfolgt mittels benutzerdefiniertem Code**, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Das Kontrollkästchen **mit benutzerdefiniertem Code speichern** ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **InfoPath Forms Services**festgelegt ist. Der Grund dafür ist, dass das [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) -Ereignis in der Geschäftslogik von Formularvorlagen, die in dokumentBibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt wird. Zum Erstellen eines Ereignishandlers für das [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) -Ereignis müssen Sie die Kompatibilitätseinstellung in **InfoPath-Editor-Formular** im InfoPath-Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei** , dann auf **Formularoptionen**, auf **Kompatibilität**und dann auf **** **InfoPath-Editor-Formular**Formulartyp festlegen. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das VersionUpgrade-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Versionsverwaltung**, wählen Sie im Dropdownfeld **Vorhandene Formulare aktualisieren** die Option **Benutzerdefiniertes Ereignis verwenden** aus, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Merge-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Erweitert**, aktivieren Sie die Kontrollkästchen **Zusammenführen von Formularen aktivieren** und **Mithilfe benutzerdefiniertem Code zusammenführen**, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Das Kontrollkästchen **Formularzusammenführung aktivieren** ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **InfoPath Forms Services**festgelegt ist. Der Grund ist, [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) dass das Zusammenführungs Ereignis in der Geschäftslogik von Formularvorlagen, die in Dokumentbibliotheken in Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt wird. Zum Erstellen eines Ereignishandlers für [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) das Zusammenführungs Ereignis müssen Sie die Kompatibilitätseinstellung in **InfoPath-Editor-Formular** im InfoPath-Designer ändern. Klicken Sie dazu auf die Registerkarte **Datei** , dann auf **Formularoptionen**, auf **Kompatibilität**und dann auf **** **InfoPath-Editor-Formular**Formulartyp festlegen. 
  
## <a name="see-also"></a>Siehe auch



[Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)

