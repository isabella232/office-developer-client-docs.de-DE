---
title: Reagieren auf Formularereignisse
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- Reihenfolge der Ereignisse [infopath 207],events [InfoPath 2007], responding,events [InfoPath 2007], order,InfoPath 2007, reponding to events,EventArgs classes [InfoPath 2007]
localization_priority: Normal
ms.assetid: 754db64b-179f-4385-8dd9-c20c9407b186
description: Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Zum Arbeiten mit Ereignissen in InfoPath fügen Sie Ereignishandler hinzu, während Sie mit einer Formularvorlage im Entwurfsmodus arbeiten.
ms.openlocfilehash: 0db3209dfe005f2a87ad65f3fc89b1714ec7d95c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407683"
---
# <a name="respond-to-form-events"></a>Reagieren auf Formularereignisse

Sie können Code schreiben, um auf unterschiedliche Ereignisse zu reagieren, die auftreten können, wenn ein Benutzer ein Formular ausfüllt. Zum Arbeiten mit Ereignissen in InfoPath fügen Sie Ereignishandler hinzu, während Sie mit einer Formularvorlage im Entwurfsmodus arbeiten.
  
InfoPath-Ereignishandler sollten immer im Entwurfsmodus erstellt werden, da InfoPath automatisch die richtige Deklaration zum Runtersetzen des Ereignisses der **InternalStartup**-Methode hinzufügt und die Codevorlage des Ereignishandlers in die Codedatei ("FormCode.cs" oder "FormCode.vb") eines Formulars einfügt. Nachdem Sie einen Ereignishandler erstellt haben, sollten Sie die zugehörige Deklaration in der Codedatei des Formulars nicht mehr ändern. 
  
Informationen zum Erstellen der InfoPath-Ereignishandler finden Sie unter [Add an Event Handler](how-to-add-an-event-handler.md).
  
## <a name="overview-of-the-event-classes"></a>Übersicht über die Ereignisklassen

Das vom [Microsoft.Office bereitgestellte InfoPath-Office. InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) implementiert drei Klassen, die die 12 Ereignisse implementieren, die von der Geschäftslogik der Formularvorlage ausgelöst und verarbeitet werden können. In der folgenden Tabelle sind alle InfoPath-Ereignisobjekte, die Ereignisse, denen sie zugeordnet sind, sowie eine Beschreibung der durch sie bereitgestellten Funktionalität aufgeführt. 
  
|**Name**|**Ereignisse**|**Beschreibung**|
|:-----|:-----|:-----|
|[ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) <br/> |[Geklickt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) <br/> |Die **ButtonEvent**-Klasse implementiert das **Clicked**-Ereignis, das ausgelöst wird, wenn Sie in einem Formular auf ein Steuerelement vom Typ **Schaltfläche** klicken.  <br/> |
|[FormEvents](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.aspx) <br/> |[ContextChanged](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ContextChanged.aspx) <br/> [Ladevorgang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) <br/> [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) <br/> [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Save.aspx) <br/> [Sign](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Sign.aspx) <br/> [Senden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Submit.aspx) <br/> [VersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.VersionUpgrade.aspx) <br/> [ViewSwitched](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.ViewSwitched.aspx) <br/> |Die **FormEvents**-Klasse implementiert die Ereignisse, die für die InfoPath-Formularvorlage selbst spezifisch sind:  <br/> **ContextChanged** <br/> Tritt nach der Änderung des Kontextknotens ein.  <br/> **Ladevorgang** <br/> Tritt ein, nachdem die Formularvorlage geladen, jedoch bevor eine Ansicht initialisiert wurde.  <br/> **Merge** <br/> Tritt auf, wenn der **Befehl Formulare** zusammenführen über die Benutzeroberfläche aufgerufen wird oder InfoPath mit der  `/aggregate` Befehlszeilenschaltlinie gestartet wird.  <br/> **Save** <br/> Tritt auf,  wenn die Befehle **Speichern** oder Speichern unter über die Benutzeroberfläche verwendet werden oder wenn die [Save-](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) und [SaveAs-Methoden](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) der [XmlForm-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) verwendet werden.  <br/> **Sign** <br/> Tritt ein, nachdem eine Gruppe signierter Daten im Dialogfeld **Digitale Signaturen** zum Signieren ausgewählt wurde.  <br/> **Senden** <br/> Tritt auf, wenn der **Befehl Submit** über die Benutzeroberfläche verwendet wird oder die [Submit-Methode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) der **XmlForm-Klasse** verwendet wird.  <br/> **VersionUpgrade** <br/> Tritt ein, wenn die Versionsnummer des Formulars, das geöffnet wird, älter ist als die Versionsnummer der Formularvorlage, auf der das Formular basiert.  <br/> **ViewSwitched** <br/> Tritt ein, nachdem eine Ansicht eines Formulars erfolgreich gewechselt wurde.  <br/> |
|[XmlEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.aspx) <br/> |[Geändert](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) <br/> [Ändern](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changing.aspx) <br/> [Überprüfen](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Validating.aspx) <br/> |Implementiert die durch Änderungen an den Daten des einer Formularinstanz zugrunde liegenden XML-Dokuments ausgelösten Ereignisse.  <br/> **Geändert** <br/> Tritt ein, nachdem Änderungen an dem einem Formular zugrunde liegenden XML-Dokument angenommen wurden und nachdem das **Validating**-Ereignis eingetreten ist.  <br/> **Ändern** <br/> Tritt ein, nachdem Änderungen an einem Formular zugrunde liegenden XML-Dokument vorgenommen wurden, jedoch bevor diese angenommen wurden.  <br/> **Überprüfen** <br/> Tritt ein, nachdem Änderungen an dem einem Formular zugrunde liegenden XML-Dokument angenommen wurden, jedoch bevor das **Changed**-Ereignis eingetreten ist.  <br/> Die **XmlEvent-Klasse** implementiert auch die [RaiseUndoRedoForChanged-Eigenschaft,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.RaiseUndoRedoForChanged.aspx) die ruft ab oder legt fest, ob das **Changed-Ereignis** ausgelöst wird, wenn ein Rückgängig- oder Wiederherstellungsvorgang auftritt.  <br/> |
   
> [!NOTE]
>  Die  Ereignisse Changed und **Changing** werden nur einmal ausgelöst, wenn eine Änderung in einem nicht leeren Feld im Formular vorgenommen wird, während die vergleichbaren Ereignisse in InfoPath 2003 und das InfoPath 2003-kompatible Objektmodell, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) ( [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx) und [OnAfterChange)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) bereitgestellt wird, zweimal bei Änderungen an einem nicht leeren Feld ausgelöst werden: einmal, wenn der alte Wert gelöscht wird, und erneut, wenn der neue Wert eingefügt wird. 
  
## <a name="overview-of-the-eventargs-classes"></a>Übersicht über die EventArgs-Klassen

Jedem der 12 Ereignisse ist ein **EventArgs**-Objekt zugeordnet, das an den Ereignishandler für das Ereignis übergeben wird, um Statusinformationen und andere Funktionalität bereitzustellen, die im Ereignishandlercode verwendet werden können. Die folgende Tabelle listet die InfoPath-Ereignisse mit den ihnen zugeordneten **EventArgs**-Objekten und einer kurzen Beschreibung der durch die Eigenschaften und Methoden des Objekts bereitgestellten Funktionalität auf. Details zu den speziellen Eigenschaften und Methoden des Objekts erhalten Sie, indem Sie auf den Namen des **EventArgs**-Objekts in der Tabelle und dann auf den Hyperlink zu den Membern im Thema klicken. 
  
|**Event**|**EventsArgs-Klasse**|**Beschreibung**|
|:-----|:-----|:-----|
|**Geklickt** <br/> |[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Ruft die Steuerelement-ID ab.  <br/> Ruft ein **XPathNavigator**-Objekt ab, mit Positionierung im innersten XML-Knoten des dem Formular zugrunde liegenden XML-Dokuments, in dem das Steuerelement **Schaltfläche** enthalten ist.  <br/> |
|**ContextChanged** <br/> |[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Ruft den Typ der Kontextänderung ab, die beim Eintreten des Ereignisses ausgeführt wurde.  <br/> Ruft einen Wert ab, der angibt, ob das Kontextänderungsereignis als Reaktion auf einen Vorgang zum Rückgängigmachen oder Wiederholen ausgeführt wurde.   <br/> Ruft einen Verweis auf **XPathNavigator** am Kontextknoten ab, der das Ereignis ausgelöst hat.   <br/> |
|**Ladevorgang** <br/> |[LoadingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) <br/> |Gibt die Ansicht an, in der das Formular nach dem Laden geöffnet werden soll.  <br/> Ruft einen Verweis auf das **XmlFormCancelEventArgs**-Objekt ab.  <br/> Ruft einen **IDictionary-Wert ab,** der alle Eingabeparameter enthält, die mit der Befehlszeilenoption angegeben oder mithilfe von Abfrageparametern in einer URL angegeben werden, um  `/InputParameters` das Formular zu öffnen.  <br/> |
|**Merge** <br/> |[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Ruft einen Verweis auf das **XmlFormCancelEventArgs**-Objekt ab.  <br/> Ruft die Anzahl der Formulare ab, die bei einem Zusammenführungsvorgang zusammengeführt werden.  <br/> Ruft den nullbasierten Index des Formulars ab, das zurzeit zusammengeführt wird.  <br/> Ruft einen mit der **Cancel**-Eigenschaft verwendeten Wert ab oder legt diesen fest, um zu bestimmen, ob nur das aktuelle Formular oder der gesamte Zusammenführungsvorgang abgebrochen werden soll.   <br/> Ruft ein **XPathNavigator**-Objekt auf, welches am Stammknoten des zugrunde liegenden XML-Dokuments des momentan zusammengeführten Formulars positioniert ist.  <br/> |
|**Save** <br/> |[SaveEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SaveEventArgs.aspx) <br/> |Führt den vom Benutzer angeforderten Speichervorgang aus.  <br/> Ruft einen Verweis auf das **SaveCancelEventArgs**-Objekt ab, das zum Abbrechen des Ereignisses verwendet werden kann.  <br/> Ruft den Dateinamen ab, der im Ereignishandler für das Ereignis verwendet werden soll.  <br/> Ruft ab, ob der Speichervorgang als Speichern- oder als Speichern-unter-Vorgang ausgeführt wird.   <br/> |
|**Sign** <br/> |[SignEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignEventArgs.aspx) <br/> |Ruft ab oder legt fest, ob das Dialogfeld **Digitale Signaturen** angezeigt wird.  <br/> Ruft die Gruppe signierbarer Daten ab, die das Ereignis ausgelöst hat.  <br/> |
|**Senden** <br/> |[SubmitEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SubmitEventArgs.aspx) <br/> |Ruft einen Verweis auf das **XmlFormCancelEventArgs**-Objekt zum Abbrechen des Ereignisses ab.  <br/> |
|**VersionUpgrade** <br/> |[VersionUpgradeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.VersionUpgradeEventArgs.aspx) <br/> |Ruft einen Verweis auf das **XmlFormCancelEventArgs**-Objekt zum Abbrechen des Ereignisses ab.  <br/> Ruft die Versionsnummer des Formulardokuments ab, für das ein Upgrade ausgeführt wird.  <br/> Ruft die Versionsnummer der Formularvorlage ab, die mit dem Formular verknüpft ist, für das ein Upgrade ausgeführt wird.  <br/> |
|**ViewSwitched** <br/> |[ViewSwitchedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewSwitchedEventArgs.aspx) <br/> |Die **ViewSwitchedEventArgs**-Klasse stellt keine anderen als die von **System.Object** geerbten Eigenschaften und Methoden für das Ereignis bereit.  <br/> |
|**Geändert** <br/> |[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Ruft ein **XPathExpression**-Objekt ab, das einen XPath-Ausdruck enthält, der den Knoten zurückgibt, der zurzeit geändert wird.  <br/> Ruft den neuen Wert für den Knoten ab, der geändert wird.  <br/> Ruft ein **XPathNavigator**-Objekt ab, das auf den Knoten zeigt, der dem gelöschten Knoten übergeordnet ist.  <br/> Ruft den ursprünglichen Wert des Knotens ab, der geändert wird.  <br/> Ruft eine [XmlOperation-Enumeration](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlOperation.aspx) ab, die den Typ des Vorgangs angibt, der beim Ändern des Knotens aufgetreten ist.  <br/> Ruft ein **XPathNavigator**-Objekt ab, das auf den Knoten zeigt, der geändert wird.  <br/> Ruft einen Wert ab, der angibt, ob der zu ändernde Knoten Teil eines Vorgangs zum Rückgängigmachen oder Wiederholen ist.  <br/> |
|**Ändern** <br/> |[XmlChangingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) <br/> |Ruft ein **XmlFormCancelEventArgs**-Objekt ab, das dem Ereignis zugeordnet ist.  <br/> Erbt die gesamte oben aufgeführte Funktionalität für das **XmlEventArgs**-Objekt.  <br/> |
|**Überprüfen** <br/> |[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Erstellt ein [FormError-Objekt,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) das benutzerdefinierte Fehlerinformationen mit den angegebenen Werten enthält, und fügt es dem [FormErrorCollection-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) des Formulars hinzu.  <br/> Erbt die gesamte oben aufgeführte Funktionalität für das **XmlEventArgs**-Objekt.  <br/> |
   
## <a name="using-the-eventargs-objects"></a>Verwenden der EventArgs-Objekte

Beim Erstellen eines Ereignishandlers wird von InfoPath dessen Deklaration im Formularcode des Projekts erstellt. In der Deklaration des Ereignishandlers wird von InfoPath **e** als Name des Parameters verwendet, der an den Ereignishandler übergeben wird. Dieser Parameter enthält das **EventArgs**-Objekt, das dem Ereignishandler zugeordnet ist, um Statusinformationen und andere Funktionalität bereitzustellen, wenn das Ereignis eintritt.  
  
Wenn Sie z. B. einen Ereignishandler für das **Loading-Ereignis** im  Entwurfsmodus erstellen (indem Sie auf der Registerkarte Entwickler auf das Menü Ereignis laden klicken), fügt InfoPath die Deklaration für den Ereignishandler hinzu, der das  [LoadingEventArgs-Objekt](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.LoadingEventArgs.aspx) empfängt, zur Formularcodedatei und öffnet dann den Code-Editor, damit Sie den Code der folgenden Ereignishandlerdeklaration hinzufügen können. 
  
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

Beim Schreiben von Code für einen Ereignishandler können Sie die Eigenschaften und Methoden verwenden, die vom **EventArgs**-Objekt implementiert werden, das durch den **e**-Parameter übergeben wird. Im folgenden **Changing-Ereignishandler** wird beispielsweise die [NewValue-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.NewValue.aspx) des [XmlChangingEventArgs-Objekts](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.aspx) (das von der [XmlEventArgs-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) geerbt wird) verwendet, um den Wert des Felds zu überprüfen, das gerade geändert wurde. Wenn der Benutzer das Feld geändert und leer gelassen hat, wird auf die [Message-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.Message.aspx) der [XmlFormCancelEventArgs-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCancelEventArgs.aspx) mithilfe der [CancelableArgs-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlChangingEventArgs.CancelableArgs.aspx) des **XmlChangingEventArgs-Objekts** zugegriffen, um dem Benutzer einen Fehler angezeigt zu haben, und die **XmlFormCancelEventArgs.Cancel-Eigenschaft** ist auf **true** festgelegt, um das Ereignis abbricht und ein Rollback der vom Benutzer vorgenommenen Änderungen vorzunehmen.
  
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


