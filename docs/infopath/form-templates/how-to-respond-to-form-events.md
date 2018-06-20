---
title: Reagieren auf Formularereignisse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Reihenfolge von Ereignissen [Infopath 207], [InfoPath 2007], Ereignisse reagieren, Reihenfolge von Ereignissen [InfoPath 2007] InfoPath 2007, reagieren auf Ereignisse, EventArgs-Klassen [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Zum Arbeiten mit Ereignissen in InfoPath fügen Sie Ereignishandler hinzu, während Sie mit einer Formularvorlage im Entwurfsmodus arbeiten.
ms.openlocfilehash: 7968837fe0ed524104111bc3f2960860af51c75a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790778"
---
# <a name="respond-to-form-events"></a>Reagieren auf Formularereignisse

Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Zum Arbeiten mit Ereignissen in InfoPath fügen Sie Ereignishandler hinzu, während Sie mit einer Formularvorlage im Entwurfsmodus arbeiten.
  
InfoPath-Ereignishandler sollte immer im Entwurfsmodus erstellt werden, da InfoPath die korrekte Deklaration für Auffangen von das Ereignis an die **InternalStartup** -Methode fügt automatisch und den Ereignishandler Codeskelett in Datei () eines Formulars Code fügt "FormCode.cs" oder "FormCode.vb"). Nachdem Sie einen Ereignishandler erstellt haben, sollten Sie nicht die Deklaration in der Formularcodedatei ändern. 
  
Informationen zum Erstellen von InfoPath-Ereignishandler finden Sie unter [Hinzufügen eines Ereignishandlers](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Übersicht über die Ereignisklassen

Das InfoPath-Objektmodell des [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespace implementiert drei Klassen, die die 12 Ereignisse implementiert werden, die ausgelöst und vom Formularvorlagen-Geschäftslogik verarbeitet werden können. Die folgende Tabelle enthält alle InfoPath-Ereignisobjekte, die Ereignisse, denen sie zugeordnet sind sowie eine Beschreibung der Funktionen, die sie bereitstellen. 
  
|**Name**|**Ereignisse**|**Beschreibung**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Geklickt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |Die **ButtonEvent** -Klasse implementiert das **Clicked** -Ereignis, das ausgelöst wird, wenn ein **Button** -Steuerelement in einem Formular geklickt wird.  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Laden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Anmelden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Senden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |Die **FormEvents** -Klasse implementiert die Ereignisse, die in eine InfoPath-Formularvorlage selbst spezifisch sind:  <br/> **ContextChanged** <br/> Tritt nach der Änderung des Kontextknotens ein.  <br/> **Laden** <br/> Tritt ein, nachdem die Formularvorlage geladen, jedoch bevor eine Ansicht initialisiert wurde.  <br/> **Merge** <br/> Tritt auf, wenn der Befehl **Formulare zusammenführen** von der Benutzeroberfläche aufgerufen oder InfoPath mit gestartet wird die `/aggregate` Befehlszeilenoption.  <br/> **Save** <br/> Tritt auf, wenn die Befehle **Speichern** oder **Speichern unter** von der Benutzeroberfläche verwendet werden, oder wenn die [Speichern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) und die [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) -Methoden der [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) -Klasse verwendet werden.  <br/> **Anmelden** <br/> Tritt auf, nachdem eine Gruppe signierter Daten über das Dialogfeld **Digitale Signaturen** Signieren ausgewählt wurde.  <br/> **Senden** <br/> Tritt auf, wenn der Befehl **Absenden** von der Benutzeroberfläche verwendet wird, oder die [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) -Methode der **XmlForm** -Klasse verwendet wird.  <br/> **VersionUpgrade** <br/> Tritt ein, wenn die Versionsnummer des Formulars, das geöffnet wird, älter ist als die Versionsnummer der Formularvorlage, auf der das Formular basiert.  <br/> **ViewSwitched** <br/> Tritt ein, nachdem eine Ansicht eines Formulars erfolgreich gewechselt wurde.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Geändert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Ändern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Validieren](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Implementiert die durch Änderungen an den Daten des einer Formularinstanz zugrunde liegenden XML-Dokuments ausgelösten Ereignisse.  <br/> **Geändert** <br/> Tritt auf, nachdem Änderungen an einem Formular zugrunde liegenden XML-Dokument angenommen wurden und nachdem das **Validating** -Ereignis eingetreten ist.  <br/> **Ändern** <br/> Tritt ein, nachdem Änderungen an einem Formular zugrunde liegenden XML-Dokument vorgenommen wurden, jedoch bevor diese angenommen wurden.  <br/> **Validieren** <br/> Tritt auf, nachdem Änderungen an einem Formular zugrunde liegenden XML-Dokument angenommen wurden, jedoch bevor das **Changed** -Ereignis eingetreten ist.  <br/> Die **XmlEvent** -Klasse implementiert auch die [RaiseUndoRedoForChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) -Eigenschaft, die abruft oder festlegt, ob das **Changed** -Ereignis ausgelöst wird, wenn ein Vorgang zum Rückgängigmachen oder Wiederholen eintritt.  <br/> |
   
> [!NOTE]
>  Das **Changed** und **Changing** Ereignisse ausgelöst werden, nur einmal bei einer in einem Feld nicht leer, klicken Sie im Formular Änderung die vergleichbare Ereignisse in InfoPath 2003 und dem InfoPath 2003-kompatible Objektmodell durch die [vorgesehen Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) und [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) ) Feuer zweimal auf Änderungen an ein Feld nicht leer: einmal, wenn der alte Wert gelöscht wird, und erneut bei der neue Wert eingefügt wird. 
  
## <a name="overview-of-the-eventargs-classes"></a>Übersicht über die EventArgs-Klassen

Für jedes 12 Ereignisse ein **EventArgs** -Objekt, das das Ereignis, das an den Ereignishandler für das Ereignis anzugebende Zustandsinformationen übergeben werden zugeordnet und in den Ereignisdetails verwendet Ereignishandlercode andere Funktionen, die werden können. Die folgende Tabelle enthält die InfoPath-Ereignisse mit ihren zugeordneten **EventArgs** -Objekten und eine kurze Beschreibung der Funktionalität, die von den Eigenschaften und Methoden des Objekts bereitgestellt. Ausführliche Informationen dazu, die bestimmte Eigenschaften und Methoden des Objekts klicken Sie auf den Namen des **EventArgs** -Objekts in der Tabelle, und klicken Sie dann auf den Link Mitglieder im Thema. 
  
|Document.SelectionChanged **-Ereignis**|**EventsArgs-Klasse**|**Beschreibung**|
|:-----|:-----|:-----|
|**Geklickt** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Ruft die Steuerelement-ID ab.  <br/> Abrufen eines **XPathNavigator** -Objekts Positionierung im innersten XML-Knoten des dem Formular zugrunde liegenden XML-Dokument, das **das Steuerelement** enthält.  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Ruft den Typ der Kontextänderung ab, die beim Eintreten des Ereignisses ausgeführt wurde.   <br/> Ruft einen Wert ab, der angibt, ob das Kontextänderungsereignis als Reaktion auf einen Vorgang zum Rückgängigmachen oder Wiederholen ausgeführt wurde.   <br/> Ruft einen Verweis auf ein **XPathNavigator** am Kontextknoten, der das Ereignis ausgelöst hat.  <br/> |
|**Laden** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Gibt die Ansicht an, in der das Formular nach dem Laden geöffnet werden soll.  <br/> Ruft einen Verweis auf das **XmlFormCancelEventArgs** -Objekt ab.  <br/> Ruft ein **IDictionary-Objekt zu** , die eine enthalten Eingabeparameter mithilfe der `/InputParameters` -Befehlszeilenoption oder mit angegebene Parameter in einem URL Abfragen zum Öffnen des Formulars.  <br/> |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Ruft einen Verweis auf das **XmlFormCancelEventArgs** -Objekt ab.  <br/> Ruft die Anzahl der Formulare ab, die bei einem Zusammenführungsvorgang zusammengeführt werden.   <br/> Ruft den nullbasierten Index des Formulars ab, das zurzeit zusammengeführt wird.  <br/> Dient zum Abrufen oder Festlegen eines Werts, das mit der **Cancel** -Eigenschaft verwendet wird, um zu bestimmen, ob nur das aktuelle Formular oder der gesamte Zusammenführungsvorgang abgebrochen.  <br/> Dient zum Abrufen eines **XPathNavigator** -Objekts am Stammknoten des zugrunde liegenden XML-Dokuments des Formulars, das momentan zusammengeführt wird.  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Führt den vom Benutzer angeforderten Speichervorgang aus.  <br/> Ruft einen Verweis auf das **SaveCancelEventArgs** -Objekt, das zum Abbrechen des Ereignisses verwendet werden kann.  <br/> Ruft den Dateinamen ab, der im Ereignishandler für das Ereignis verwendet werden soll.  <br/> Ruft ab, ob der Speichervorgang als Speichern- oder als Speichern-unter-Vorgang ausgeführt wird.   <br/> |
|**Anmelden** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Ruft ab oder legt fest, ob das Dialogfeld **Digitale Signaturen** angezeigt werden soll.  <br/> Ruft die Gruppe signierbarer Daten ab, die das Ereignis ausgelöst hat.  <br/> |
|**Senden** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Ruft einen Verweis auf das **XmlFormCancelEventArgs** -Objekt zum Abbrechen des Ereignisses ab.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Ruft einen Verweis auf das **XmlFormCancelEventArgs** -Objekt zum Abbrechen des Ereignisses ab.  <br/> Ruft die Versionsnummer des Formulardokuments ab, für das ein Upgrade ausgeführt wird.  <br/> Ruft die Versionsnummer der Formularvorlage ab, die mit dem Formular verknüpft ist, für das ein Upgrade ausgeführt wird.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |Die **ViewSwitchedEventArgs** -Klasse stellt Eigenschaften und Methoden für das Ereignis als die von **System.Object**geerbten keine bereit.  <br/> |
|**Geändert** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Ruft ein **XPathExpression** -Objekt, einen XPath-Ausdruck enthält, der den Knoten zurückgibt, der zurzeit geändert wird.  <br/> Ruft den neuen Wert für den Knoten ab, der geändert wird.   <br/> Ruft ein **XPathNavigator** -Objekt verweist auf den Knoten, der das übergeordnete Objekt des gelöschten Knoten übergeordnet ist.  <br/> Ruft den ursprünglichen Wert des Knotens ab, der geändert wird.  <br/> Ruft eine [XmlOperation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) -Enumeration, die den Typ des Vorgangs angibt, der beim Ändern des Knotens aufgetreten.  <br/> Ruft ein **XPathNavigator** -Objekt, zeigen Sie auf den Knoten, der geändert wird.  <br/> Ruft einen Wert ab, der angibt, ob der zu ändernde Knoten Teil eines Vorgangs zum Rückgängigmachen oder Wiederholen ist.  <br/> |
|**Ändern** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Ruft ein **XmlFormCancelEventArgs** -Objekt mit dem Ereignis verknüpft ist.  <br/> Erbt die gesamte die oben aufgeführte Funktionalität für das **XmlEventArgs** -Objekt.  <br/> |
|**Validieren** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Erstellt ein [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) -Objekt, das benutzerdefinierte Fehlerinformationen mit den angegebenen Werten enthält, und fügt es der [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) -Objekt des Formulars hinzu.  <br/> Erbt die gesamte die oben aufgeführte Funktionalität für das **XmlEventArgs** -Objekt.  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Verwenden der EventArgs-Objekte

Wenn Sie einen Ereignishandler erstellen, erstellt InfoPath Deklaration der Ereignishandler im Formularcode für das Projekt. In der Deklaration der Ereignishandler verwendet InfoPath **e** als den Namen des Parameters, der an den Ereignishandler übergeben wird. Dieser Parameter enthält das **EventArgs** -Objekt, das der Ereignishandler zum Bereitstellen von Statusinformationen und andere Funktionen beim Eintreten des Ereignisses zugeordnet ist. 
  
Wenn Sie einen Ereignishandler für das **Loading** -Ereignis (durch Klicken auf **Loading-Ereignis** im Menü auf der Registerkarte **Entwicklertools** ) im Entwurfsmodus erstellen, wird InfoPath beispielsweise die Deklaration für den Ereignishandler, der die [LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) empfängt. Objekt, das der Formularcodedatei, und klicken Sie dann im Code-Editor öffnet, sodass Sie die folgende Deklaration der Ereignis-Handler Code hinzufügen können. 
  
```cs
public void FormEvents_Loading(object sender, LoadingEventArgs e)
{
   // Write your code here.
}
```

```vb
Public Sub FormEvents_Loading(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Write your code here.
End Sub
```

Wenn Sie Code für einen Ereignishandler schreiben, können Sie die Eigenschaften und Methoden implementiert, durch die **EventArgs** -Objekt, das über den **e** -Parameter übergeben wird. Beispielsweise wird in den folgenden **Changing** -Ereignishandler die [NewValue](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) -Eigenschaft des [XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) -Objekts (die von der [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) -Klasse geerbt wird) verwendet, um den Wert des Felds überprüfen, die gerade geändert wurde. Wenn der Benutzer das Feld geändert und leer gelassen, die [Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) -Eigenschaft der [XmlFormCancelEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) -Klasse erfolgt mithilfe der [CancelableArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) -Eigenschaft des **XmlChangingEventArgs** -Objekts für den Benutzer anzuzeigen und die **XmlFormCancelEventArgs.Cancel** -Eigenschaft ist auf **true**festgelegt, das Ereignis abzubrechen und Rollback für der Benutzer vorgenommenen Änderungen.
  
```cs
public void field1_Changing(object sender, LoadingEventArgs e)
{
   // Determine whether there is a new value.
   if (e.NewValue == "")
   {
      // The value is blank, so display an error message
      // and roll back the changes.
      e.CancelableArgs.Message = 
         "You must supply a value for this field.";
      e.CancelableArgs.Cancel = true;
      return;
   }
}
```

```vb
Public Sub field1_Changing(ByVal sender As Object, _
   ByVal e As LoadingEventArgs)
   ' Determine whether there is a new value.
   If (e.NewValue = "") Then
      ' The value is blank, so display an error message 
      ' and roll back the changes.
      e.CancelableArgs.Message = _
         "You must supply a value for this field."
      e.CancelableArgs.Cancel = True
      Return
   End If
End Sub
```


