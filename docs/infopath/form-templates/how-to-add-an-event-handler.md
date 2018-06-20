---
title: Hinzufügen eines Ereignishandlers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Versionupgrade-Ereignis [Infopath 2007], Behandeln von Ereignissen [InfoPath 2007], Changing-Ereignis [InfoPath 2007], InfoPath 2007, Hinzufügen von Ereignishandlern, Changed-Ereignis [InfoPath 2007], ContextChanged-Ereignis [InfoPath 2007], klicken Sie auf Ereignis [InfoPath 2007], [InfoPath-Ereignisse Laden von 2007], Hinzufügen von Ereignishandlern, Sign-Ereignis [InfoPath 2007], ViewSwitched-Ereignis [InfoPath 2007], Ereignisbehandlung [InfoPath 2007], Merge-Ereignis [InfoPath 2007], Validating-Ereignis [InfoPath 2007], Submit-Ereignis [InfoPath 2007], speichern Ereignis [InfoPath 2007] Ereignis [InfoPath 2007]
localization_priority: Normal
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern in eine Microsoft InfoPath verwaltetem Code Formularvorlage, die von Visual Studio 2012. Um eine Formularvorlage einen Ereignishandler hinzuzufügen, beginnen Sie mit der Formularvorlage im InfoPath-Designer geöffnet, und wählen Sie dann den entsprechenden Befehl Schnittstelle für das Ereignis, dass Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis in InfoPath Designer ausgewählt haben, wechselt der Fokus automatisch zum Formularcode für das Ereignis im Code-Editor von Visual Studio 2012.
ms.openlocfilehash: 5bac409fb859337b82bf6567dd4636e6d384ba59
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790771"
---
# <a name="add-an-event-handler"></a>Hinzufügen eines Ereignishandlers

In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern in eine Microsoft InfoPath verwaltetem Code Formularvorlage, die von Visual Studio 2012. Um eine Formularvorlage einen Ereignishandler hinzuzufügen, beginnen Sie mit der Formularvorlage im InfoPath-Designer geöffnet, und wählen Sie dann den entsprechenden Befehl Schnittstelle für das Ereignis, dass Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis in InfoPath Designer ausgewählt haben, wechselt der Fokus automatisch zum Formularcode für das Ereignis im Code-Editor von Visual Studio 2012.
  
> [!IMPORTANT]
> Sie sollten immer die InfoPath-Designer-Benutzeroberfläche verwenden, um einen Ereignishandler hinzuzufügen. Hinzufügen eines ereignishandlers mit der Benutzeroberfläche generiert-Bindung Ereigniscode in der **InternalStartup** -Methode der Datei "FormCode.cs" oder "FormCode.vb" in Ihrem Formularvorlagenprojekt. Sie sollten nicht die **InternalStartup** -Methode erstellen oder Hinzufügen zusätzlichen Code darin enthaltenen selbst. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Hinzufügen eines Ereignishandlers für das Click-Ereignis eines Schaltflächen-Steuerelements

1. Öffnen Sie die Formularvorlage im InfoPath-Designer, und fügen Sie dem Formular ein **Button** -Steuerelement. 
    
2. Klicken Sie auf die Schaltfläche, und klicken Sie dann auf der Registerkarte **Eigenschaften** des Menübands auf **Benutzerdefinierter Code**.
    
    Der Fokus wechselt zum Formularcode für das [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Hinzufügen eines Ereignishandlers für das Ereignis "Changing", "Validating" oder "Changed" eines Felds oder einer Gruppe

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Mit der rechten Maustaste in ein Steuerelement zur Eingabe von Daten an das Feld oder Gruppe, wie ein **Textfeld** -Steuerelement gebunden. 
    
3. Zeigen Sie auf **Programmierung**, und klicken Sie dann auf das Ereignis, dem Sie für einen Ereignishandler erstellen möchten. Der Fokus wechselt zum Formularcode für das [Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) oder [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Der Befehl erstellen Sie einen Ereignishandler für das **Changing** -Ereignis ist nicht verfügbar, wenn die Einstellung für die Formularvorlage auf **Webbrowserformular**festgelegt ist. Dies ist, da das **Changing** -Ereignis in der Geschäftslogik in Dokumentbibliotheken auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlichte Formularvorlagen nicht unterstützt wird. Um einen Ereignishandler für das **Changing** -Ereignis zu erstellen, müssen Sie die Einstellung zum **InfoPath-Editor** im InfoPath-Designer ändern. Dazu klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Formularoptionen**, klicken Sie auf **Kompatibilität**und klicken Sie dann auf **InfoPath-Editor-Formular** **Formulartyp** festgelegt. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "Loading", "ViewSwitched", "ContextChanged" und "Sign" eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Entwicklertools** des Menübands auf das Formularereignis, dem Sie für einen Ereignishandler schreiben möchten. 
    
    Der Fokus wechselt zum Formularcode für das [Laden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) , [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) , [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Die Befehle, um einen Ereignishandler für die Ereignisse [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Registrieren Sie sich](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) erstellen sind nicht verfügbar, wenn die Einstellung für die Formularvorlage auf **Webbrowserformular**festgelegt ist. Dies ist, da diese Ereignisse in der Geschäftslogik in Dokumentbibliotheken auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlichte Formularvorlagen nicht unterstützt werden. So erstellen Sie einen Ereignishandler für das Ereignis [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Registrieren Sie sich](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) , müssen Sie die kompatibilitätseinstellung in **InfoPath-Editor-Formular** im InfoPath-Designer ändern. Dazu klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Formularoptionen**, klicken Sie auf **Kompatibilität**und klicken Sie dann auf **InfoPath-Editor-Formular** **Formulartyp** festgelegt. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Submit-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , klicken **Sie** auf der Registerkarte **Info** , und klicken Sie dann auf ** Absendeoptionen **.
    
3. Klicken Sie auf **Übermitteln dieses Formulars durch Benutzer zulassen**, klicken Sie auf **benutzerdefinierte Aktion mithilfe von Code ausführen**, und klicken Sie dann auf **Code bearbeiten**.
    
    Der Fokus wechselt zum Formularcode für das [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Save-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
3. Klicken Sie auf die Kategorie **Speichern** , aktivieren Sie das Kontrollkästchen **Speichern erfolgt mittels benutzerdefinierten Code** , und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Formularcode für das [Speichern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Aktivieren Sie das Kontrollkästchen **Speichern erfolgt mittels benutzerdefinierten Code** ist nicht verfügbar, wenn die Einstellung für die Formularvorlage in **InfoPath Forms Services**festgelegt ist. Dies ist, da das Ereignis [Speichern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) in der Geschäftslogik in Dokumentbibliotheken auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlichte Formularvorlagen nicht unterstützt wird. So erstellen Sie einen Ereignishandler für das Ereignis [zu speichern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) , müssen Sie die kompatibilitätseinstellung in **InfoPath-Editor-Formular** im InfoPath-Designer ändern. Dazu klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Formularoptionen**, klicken Sie auf **Kompatibilität**und klicken Sie dann auf **InfoPath-Editor-Formular** **Formulartyp** festgelegt. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das VersionUpgrade-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
3. Klicken Sie auf die Kategorie **Versionsverwaltung** , wählen Sie im Dropdown-Liste **vorhandene Formulare aktualisieren** **benutzerdefiniertes Ereignis verwenden** aus, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Formularcode für das [Speichern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Merge-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath-Designer.
    
2. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
3. Klicken Sie auf die Kategorie **Erweitert** , klicken Sie auf das Kontrollkästchen **Zusammenführen von Formularen aktivieren** , klicken Sie auf das Kontrollkästchen **Mithilfe benutzerdefiniertem Code Zusammenführen** , und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Formularcode für das [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis im Code-Editor von Visual Studio 2012. 
    
    > [!NOTE]
    > Aktivieren Sie das Kontrollkästchen **Zusammenführen von Formularen aktivieren** ist nicht verfügbar, wenn die Einstellung für die Formularvorlage in **InfoPath Forms Services**festgelegt ist. Dies ist, da das [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis in der Geschäftslogik in Dokumentbibliotheken auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlichte Formularvorlagen nicht unterstützt wird. Um einen Ereignishandler für das [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) -Ereignis zu erstellen, müssen Sie die kompatibilitätseinstellung in **InfoPath-Editor-Formular** im InfoPath-Designer ändern. Dazu klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Formularoptionen**, klicken Sie auf **Kompatibilität**und klicken Sie dann auf **InfoPath-Editor-Formular** **Formulartyp** festgelegt. 
  
## <a name="see-also"></a>Siehe auch



[Exemplarische Vorgehensweise: Erstellen einer einfachen Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)

