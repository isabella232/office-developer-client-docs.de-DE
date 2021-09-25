---
title: Hinzufügen eines Ereignishandlers
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- versionupgrade event [infopath 2007],handling events [InfoPath 2007],Changing event [InfoPath 2007],InfoPath 2007, adding event handlers,Changed event [InfoPath 2007],ContextChanged event [InfoPath 2007],Click event [InfoPath 2007],events [InfoPath 2007], adding event handlers,Sign event [InfoPath 2007],ViewSwitched-Ereignis [InfoPath 2007],Ereignisbehandlung [InfoPath 2007],Merge-Ereignis [InfoPath 2007],Validating-Ereignis [InfoPath 2007],Submit-Ereignis [InfoPath 2007], Save-Ereignis [InfoPath 2007],Loading-Ereignis [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: d69393fb-fb5a-4edb-abc0-38f5d7e80bcc
description: In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern zu einer Microsoft InfoPath-Formularvorlage mit verwaltetem Code mit Visual Studio 2012 beschrieben. Um einer Formularvorlage einen Ereignishandler hinzuzufügen, beginnen Sie mit der geöffneten Formularvorlage im InfoPath Designer, und wählen Sie dann den entsprechenden Benutzeroberflächenbefehl für das Ereignis aus, für das Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis im InfoPath Designer ausgewählt haben, wechselt der Fokus automatisch zum Skeleton-Ereignishandler für dieses Ereignis im Code-Editor Visual Studio 2012.
ms.openlocfilehash: bb94bc074c601dc215a72b7873992cb1891931d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592879"
---
# <a name="add-an-event-handler"></a>Hinzufügen eines Ereignishandlers

In diesem Thema werden die Verfahren zum Hinzufügen von Ereignishandlern zu einer Microsoft InfoPath-Formularvorlage mit verwaltetem Code mit Visual Studio 2012 beschrieben. Um einer Formularvorlage einen Ereignishandler hinzuzufügen, beginnen Sie mit der geöffneten Formularvorlage im InfoPath Designer, und wählen Sie dann den entsprechenden Benutzeroberflächenbefehl für das Ereignis aus, für das Sie Code schreiben möchten. Nachdem Sie den Befehl für ein Ereignis im InfoPath Designer ausgewählt haben, wechselt der Fokus automatisch zum Skeleton-Ereignishandler für dieses Ereignis im Code-Editor Visual Studio 2012.
  
> [!IMPORTANT]
> Sie sollten immer die InfoPath Designer-Benutzeroberfläche verwenden, um einen Ereignishandler hinzuzufügen. Das Hinzufügen eines Ereignishandlers zur Benutzeroberfläche generiert Ereignisbindungscode in der **InternalStartup-Methode** der Datei "FormCode.cs" oder "FormCode.vb" in Ihrem Formularvorlagenprojekt. Sie sollten die **InternalStartup-Methode** nicht selbst erstellen oder zusätzlichen Code hinzufügen. 
  
### <a name="add-an-event-handler-for-the-click-event-of-a-button-control"></a>Hinzufügen eines Ereignishandlers für das Click-Ereignis eines Schaltflächen-Steuerelements

1. Öffnen Sie die Formularvorlage im InfoPath Designer, und fügen Sie dem Formular dann ein **Schaltflächensteuerelement** hinzu. 
    
2. Klicken Sie auf die Schaltfläche, und klicken Sie dann auf der Registerkarte **Eigenschaften** des Menübands auf **Benutzerdefinierter Code**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Clicked-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) im Code-Editor Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-changing-validating-or-changed-event-of-a-field-or-group"></a>Hinzufügen eines Ereignishandlers für das Ereignis "Changing", "Validating" oder "Changed" eines Felds oder einer Gruppe

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie mit der rechten Maustaste auf ein an das Feld oder die Gruppe gebundenes Dateneingabe-Steuerelement, wie z. B. ein Steuerelement vom Typ **Textfeld**. 
    
3. Zeigen Sie auf **die Programmierung,** und klicken Sie dann auf das Ereignis, für das Sie einen Ereignishandler erstellen möchten. Der Fokus wechselt zum Skeleton-Ereignishandler für das [Ereignis Changing](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) , [Validating](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) oder [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) im Code-Editor Visual Studio 2012. 
    
    > [!NOTE]
    > Der Befehl zum Erstellen eines Ereignishandlers für das **Changing -Ereignis** ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformular** festgelegt ist. Dies liegt daran, dass das **Changing-Ereignis** in der Geschäftslogik von Formularvorlagen, die in Dokumentbibliotheken am Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt wird. Um einen Ereignishandler für das **Changing-Ereignis** zu erstellen, müssen Sie die Kompatibilitätseinstellung im InfoPath-Designer in **InfoPath-Editor** ändern. Klicken Sie dazu auf die Registerkarte **"Datei",** auf **"Formularoptionen",** auf **"Kompatibilität",** und legen Sie dann den **Formulartyp** auf das **InfoPath-Editor-Formular** fest. 
  
### <a name="add-an-event-handler-for-the-loading-viewswitched-contextchanged-and-sign-events-of-a-form"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "Loading", "ViewSwitched", "ContextChanged" und "Sign" eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf der Registerkarte **Entwickler** des Menübands auf das Formularereignis, für das Sie einen Ereignishandler schreiben möchten. 
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Ereignis Loading,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) [ViewSwitched,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) [ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) im Code-Editor Visual Studio 2012. 
    
    > [!NOTE]
    > Die Befehle zum Erstellen eines Ereignishandlers für die [ContextChanged-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign-Ereignisse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) sind nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **Webbrowserformular** festgelegt ist. Dies liegt daran, dass diese Ereignisse in der Geschäftslogik von Formularvorlagen, die am Microsoft SharePoint Server 2010 mit InfoPath Forms Services in Dokumentbibliotheken veröffentlicht wurden, nicht unterstützt werden. Um einen Ereignishandler für das [ContextChanged-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) oder [Sign-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) zu erstellen, müssen Sie die Kompatibilitätseinstellung im InfoPath-Designer in das **InfoPath-Editor-Formular** ändern. Klicken Sie dazu auf die Registerkarte **"Datei",** auf **"Formularoptionen",** auf **"Kompatibilität",** und legen Sie dann den **Formulartyp** auf das **InfoPath-Editor-Formular** fest. 
  
### <a name="add-an-event-handler-for-the-submit-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Submit-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **"Datei",** klicken Sie auf der Registerkarte **"Info"** auf **"An übermitteln",** und klicken Sie dann auf ** Absenden-Optionen **.
    
3. Klicken Sie auf **Übermitteln dieses Formulars durch Benutzer zulassen**, klicken Sie auf **Benutzerdefinierte Aktion mithilfe von Code ausführen**, und klicken Sie dann auf **Code bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Submit-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) im Code-Editor Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-save-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Save-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Speichern**, aktivieren Sie das Kontrollkästchen **Speichern erfolgt mittels benutzerdefiniertem Code**, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) im Code-Editor Visual Studio 2012. 
    
    > [!NOTE]
    > Das Kontrollkästchen **"Mit benutzerdefiniertem Code speichern"** ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **InfoPath Forms Services** festgelegt ist. Dies liegt daran, dass das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) in der Geschäftslogik von Formularvorlagen, die in Dokumentbibliotheken am Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt wird. Um einen Ereignishandler für das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) zu erstellen, müssen Sie die Kompatibilitätseinstellung im InfoPath-Designer in das **InfoPath-Editor-Formular** ändern. Klicken Sie dazu auf die Registerkarte **"Datei",** auf **"Formularoptionen",** auf **"Kompatibilität",** und legen Sie dann den **Formulartyp** auf das **InfoPath-Editor-Formular** fest. 
  
### <a name="add-an-event-handler-for-the-versionupgrade-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das VersionUpgrade-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Versionsverwaltung**, wählen Sie im Dropdownfeld **Vorhandene Formulare aktualisieren** die Option **Benutzerdefiniertes Ereignis verwenden** aus, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Save-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) im Code-Editor Visual Studio 2012. 
    
### <a name="add-an-event-handler-for-the-merge-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das Merge-Ereignis eines Formulars

1. Öffnen Sie die Formularvorlage im InfoPath Designer.
    
2. Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen**. 
    
3. Klicken Sie auf die Kategorie **Erweitert**, aktivieren Sie die Kontrollkästchen **Zusammenführen von Formularen aktivieren** und **Mithilfe benutzerdefiniertem Code zusammenführen**, und klicken Sie dann auf **Bearbeiten**.
    
    Der Fokus wechselt zum Skeleton-Ereignishandler für das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) im Code-Editor Visual Studio 2012. 
    
    > [!NOTE]
    > Das Kontrollkästchen zum Zusammenführen von **Formularen aktivieren** ist nicht verfügbar, wenn die Kompatibilitätseinstellung für die Formularvorlage auf **InfoPath Forms Services** festgelegt ist. Dies liegt daran, dass das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) in der Geschäftslogik von Formularvorlagen, die in Dokumentbibliotheken auf Microsoft SharePoint Server 2010 mit InfoPath Forms Services veröffentlicht wurden, nicht unterstützt wird. Um einen Ereignishandler für das [Merge-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) zu erstellen, müssen Sie die Kompatibilitätseinstellung im InfoPath-Designer in das **InfoPath-Editor-Formular** ändern. Klicken Sie dazu auf die Registerkarte **"Datei",** auf **"Formularoptionen",** auf **"Kompatibilität",** und legen Sie dann den **Formulartyp** auf das **InfoPath-Editor-Formular** fest. 
  
## <a name="see-also"></a>Siehe auch



[Exemplarische Vorgehensweise: Erstellen Sie eine einfache Formularvorlage mit Code](walkthrough-creating-a-basic-form-template-with-code.md)

