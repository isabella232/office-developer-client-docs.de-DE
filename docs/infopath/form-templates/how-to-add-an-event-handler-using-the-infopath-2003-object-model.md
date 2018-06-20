---
title: Hinzufügen eines ereignishandlers mit dem InfoPath-Objektmodell
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- OnAfterImport-Ereignis [Infopath 2007], OnAfterChange-Ereignis [InfoPath 2007], OnBeforeChange-Ereignis [InfoPath 2007], OnSubmitRequest-Ereignis [InfoPath 2007], OnVersionUpgrade-Ereignis [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, Ereignishandler, OnLoad-Ereignis [InfoPath 2007], [InfoPath 2007] Ereignishandler hinzufügen mithilfe des InfoPath 2003-Objektmodells OnValidate-Ereignis [InfoPath 2007], OnContextChange-Ereignis [InfoPath 2007], OnSaveRequest-Ereignis [InfoPath 2007], OnClick-Ereignis [InfoPath 2007] OnSwitchView-Ereignis [InfoPath 2007], OnSign-Ereignis [InfoPath 2007], OnMergeRequest-Ereignis [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Die Befehle für das Hinzufügen von Ereignishandler-Funktionen in ein Formularvorlagenprojekt, die mit dem InfoPath 2003-Objektmodell kompatibel ist, sind im Wesentlichen die gleichen, die für andere Arten von Formularvorlagen.
ms.openlocfilehash: 9f037c59180b9c8d858ec73d79ef892974efe483
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790749"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Hinzufügen eines ereignishandlers mit dem InfoPath-Objektmodell

Die Befehle für das Hinzufügen von Ereignishandler-Funktionen in ein Formularvorlagenprojekt, die mit dem InfoPath 2003-Objektmodell kompatibel ist, sind im Wesentlichen die gleichen, die für andere Arten von Formularvorlagen. Klicken Sie auf den Befehl **On Load-Ereignis** auf der Registerkarte **Entwicklertools** beispielsweise zum Hinzufügen eines **OnLoad** -ereignishandlers mit der Formularvorlage im InfoPath-Designer geöffnet. Der Fokus wechselt automatisch zum Formularcode für das **OnLoad** -Ereignishandler im Code-Editor von Visual Studio 2012. 
  
In mit InfoPath 2003 kompatiblen Projekten, die auf Formularvorlagen mit verwaltetem Code basieren, werden die Klasse mit den Ereignishandlerfunktionen sowie die Ereignishandler selbst durch InfoPath-spezifische Attribute im Codemodul identifiziert.

## <a name="adding-event-handlers"></a>Hinzufügen von Ereignishandlern

Alle der folgenden Verfahren wird davon ausgegangen, dass Sie ein Formularvorlagenprojekt in Microsoft InfoPath mit Visual Studio 2012 geöffnet haben.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Hinzufügen eines Ereignishandlers für das OnClick-Ereignis einer Befehlsschaltfläche

1. Klicken Sie im Bereich **Steuerelemente** auf **Schaltfläche** , um das Formular eine Schaltfläche hinzufügen. 
    
2. Klicken Sie auf der Registerkarte **Eigenschaften** auf **Benutzerdefinierter Code**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für das [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) -Ereignis im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "OnBeforeChange", "OnValidate" oder "OnAfterChange" eines Feldes oder einer Gruppe

1. Mit der rechten Maustaste in ein Steuerelement zur Eingabe von Daten an das Feld oder Gruppe, wie ein **Textfeld** -Steuerelement gebunden. 
    
2. Zeigen Sie auf **Programmierung**, und klicken Sie dann auf einen der Befehle, wie beispielsweise **On Validate-Ereignis**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für eins der folgenden Ereignisse im Code-Editor: [Ereignisse "OnBeforeChange"](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), ["OnValidate"](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)oder ["OnAfterChange"](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "OnLoad", "OnSwitchView", "OnContextChange" oder "OnSign" eines Formulars

- Klicken Sie im Menü **Extras** auf **Programmierung**zeigen Sie, und klicken Sie dann auf das Formularereignis, dem Sie für einen Ereignishandler schreiben möchten.
    
    Der Fokus wechselt zum Stub für den Ereignishandler für eins der folgenden im Code-Editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx)"," [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx)"," [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)"oder" [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx). 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnSubmitRequest-Ereignis eines Formulars

1. Klicken Sie auf der Registerkarte **Daten** auf **Absendeoptionen**.
    
2. Aktivieren Sie das Kontrollkästchen **Übermitteln dieses Formulars durch Benutzer zulassen** , und klicken Sie dann auf **benutzerdefinierte Aktion mithilfe von Code ausführen**.
    
3. Klicken Sie auf **Code bearbeiten**, und klicken Sie dann auf **OK**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für das [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) -Ereignis im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnSaveRequest-Ereignis eines Formulars

1. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Formularoptionen**.
    
2. Klicken Sie auf **Speichern erfolgt mittels benutzerdefinierten Code**in der Kategorie **Speichern** , klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für das [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) -Ereignis im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnVersionUpgrade-Ereignis eines Formulars

1. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Formularoptionen**.
    
2. Wählen Sie in der Kategorie **Versionsverwaltung** aus der Liste **vorhandene Formulare aktualisieren** **benutzerdefiniertes Ereignis verwenden** aus, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.
    
    Der Fokus wechselt zum Stub für den Ereignishandler für das [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) -Ereignis im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnMergeRequest-Ereignis eines Formulars

1. Klicken Sie auf der Registerkarte **Datei** , und klicken Sie dann auf **Formularoptionen**.
    
2. Wählen Sie in der Kategorie **Erweitert** das **Zusammenführen von Formularen aktivieren** und die Kontrollkästchen **Mithilfe benutzerdefiniertem Code Zusammenführen** , klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.
    
    Der Fokus wechselt zum Stub für den Ereignishandler für das [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) -Ereignis im Code-Editor. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Hinzufügen eines ereignishandlers für das OnAfterImport-Ereignis

Um Ereignishandler für das [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) -Ereignis hinzuzufügen, müssen Sie für die Formularvorlage mit verwaltetem Code Formularcode zu öffnen und die Ereignishandlerfunktion manuell hinzufügen. Informationen zum einen Ereignishandler für dieses Ereignis schreiben klicken Sie auf den Link für das **OnAfterImport** -Ereignis. 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Hinzufügen eines ereignishandlers für eine sekundäre Datenquelle

Im folgenden Beispiel wird gezeigt, wie ein Ereignishandler für eine sekundäre Datenquelle hinzugefügt wird. Bei diesem Beispiel wird von einer sekundären Datenquelle in der Ressourcendatei "books.xml" ausgegangen, die folgendes Schema aufweist:
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <xsd:element name="catalog">
        <xsd:complexType>
            <xsd:sequence>
                <xsd:element ref="book" minOccurs="0" maxOccurs="unbounded"></xsd:element>
            </xsd:sequence>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="genre" type="xsd:string"></xsd:element>
    <xsd:element name="author" type="xsd:string"></xsd:element>
    <xsd:element name="book">
        <xsd:complexType>
            <xsd:all>
                <xsd:element ref="author" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="title" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="genre" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="price" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="publish_date" minOccurs="0" maxOccurs="1"></xsd:element>
                <xsd:element ref="description" minOccurs="0" maxOccurs="1"></xsd:element>
            </xsd:all>
            <xsd:attribute ref="id"></xsd:attribute>
        </xsd:complexType>
    </xsd:element>
    <xsd:element name="price" type="xsd:string"></xsd:element>
    <xsd:element name="title" type="xsd:string"></xsd:element>
    <xsd:element name="publish_date" type="xsd:string"></xsd:element>
    <xsd:element name="description" type="xsd:string"></xsd:element>
    <xsd:attribute name="id" type="xsd:string"></xsd:attribute>
</xsd:schema>

```

<br/>

Der Ansicht des Formulars wird aus der Datenquelle erstellt. Der Formularcode erstellt eine Hashtabelle basierend auf den Autoren und die Anzahl der Bücher verfassten. Sie können einen Eintrag aus der Tabelle in der Ansicht angezeigten aktualisieren und der **OnAfterChange** -Ereignishandler die Hashtabelle aktualisiert. Beachten Sie, dass die [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) -Eigenschaft des **InfoPathEventHandler** -Attribut (das von der [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) -Klasse implementiert wird) verwendet wird, um auf die sekundäre Datenquelle zu verweisen. 
  
```cs
namespace AuxDom
{
    // InfoPathNamespace attribute goes here.
    public class AuxDom
    {
        private XDocument thisXDocument;
        private Application thisApplication;
        private Hashtable authors;
        public void _Startup(Application app, XDocument doc)
        {
            thisXDocument = doc;
            thisApplication = app;
            authors = new Hashtable();
        }
        public void _Shutdown()
        {
            authors.Clear();
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(EventType=InfoPathEventType.OnLoad)]
        public void OnLoad(DocReturnEvent e)
        {
            IXMLDOMDocument books = thisXDocument.GetDOM("books");
            DOMNodeList externalAuthors = books.selectNodes("/catalog/book/author");
            foreach (IXMLDOMNode authorNode in externalAuthors)
            {
                AddBookFromAuthor(authorNode.text);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="/catalog/book/author", EventType=InfoPathEventType.OnAfterChange, DataObject="books")]
        public void books__author_OnAfterChange(DataDOMEvent e)
        {
            if (e.IsUndoRedo)
            {
                // An undo or redo operation has occurred and the DOM 
                // is read-only.
                return;
            }
            
            if (e.Source.text != e.NewValue.ToString())
            {
                RemoveBookFromAuthor(e.OldValue.ToString());
                AddBookFromAuthor(e.NewValue.ToString());
            }
        }
        private void AddBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] + 1;
            }
            else
            {
                authors.Add(authorName, 1);
            }
        }
        private void RemoveBookFromAuthor(string authorName)
        {
            if (authors.Contains(authorName))
            {
                authors[authorName] = (int)authors[authorName] - 1;
            }
            if ((int)authors[authorName] == 0)
            {
                authors.Remove(authorName);
            }
        }
        // The following function handler is created by Microsoft
        // Office InfoPath. Do not modify the type or number of
        // arguments. 
        [InfoPathEventHandler(MatchPath="ShowAuthors", EventType=InfoPathEventType.OnClick)]
        public void ShowAuthors_OnClick(DocActionEvent e)
        {
            // Write your code here.
            StringBuilder report = new StringBuilder();
            foreach (string authorName in authors.Keys)
            {
                report.Append(authorName + ",\t\t\t");
                report.Append(authors[authorName] + "\n");
            }
            thisXDocument.UI.Alert(report.ToString());
        }
    }
}

```

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Wie wird die Klasse enthält Ereignishandler identifiziert.

Wenn Sie ein neues InfoPath-Formularvorlagenprojekt erstellen, die mit dem InfoPath 2003 verwaltetem Code-Objektmodell ein Assembly-Ebene **System.ComponentModel.Description** Attribut kompatibel ist wird der Klasse am Anfang des formularcodemoduls zu angewendet Identifizieren Sie die Klasse, die alle Ereignishandler für die Formularvorlage enthält. 
  
> [!IMPORTANT]
> Ändern Sie das Attribut **System.ComponentModel.Description** in dieser Klasse nicht. Wenn Sie dies tun, wird die Formularvorlage werden nicht identifiziert, auf dem Ereignishandler befinden, und die Ereignishandler werden nicht ausgeführt. 
  
```cs
using System;
using Microsoft.Office.Interop.InfoPath.SemiTrust;
// Office integration attribute. Identifies the startup class for the // form. Do not modify.
[assembly: System.ComponentModel.DescriptionAttribute(    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")]
```

```vb
Imports System
Imports Microsoft.Office.Interop.InfoPath.SemiTrust
' Office integration attribute. Identifies the startup class for the form. Do not modify.
<Assembly: System.ComponentModel.DescriptionAttribute( _    "InfoPathStartupClass, Version=1.0, Class=Template1.FormCode")>
```

## <a name="how-event-handlers-are-identified"></a>Wie Ereignishandler identifiziert werden

Wenn Sie einen neuen Ereignishandler mit Schaltflächen oder Menübefehle in der Benutzeroberfläche im Entwurfsmodus InfoPath hinzufügen, wird in das Formular Stub für den Ereignishandlerfunktion geschrieben. Das folgende Beispiel zeigt, dass der Stub-Ereignishandler für ein [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) erstellt für ein Feld namens "total" hinzugefügt. 
  
```cs
[InfoPathEventHandler(MatchPath="/invoice/total", EventType=InfoPathEventType.OnValidate)]
public void total_OnValidate(DataDOMEvent e)
{
    // Write your code here.
}

```

```vb
<InfoPathEventHandler(MatchPath:="/invoice/total",EventType:= OnValidate)> Public Sub total_OnValidate(ByVal e As EventArgs)
    ' Write your code here.
End Sub

```

Anschließend können Sie Code, die Mitglieder des InfoPath-Objektmodells mit der privaten zwischengespeicherte Elemente von aufruft Hinzufügen der `thisXDocument` oder `thisApplication` Variablen, oder indem Sie die Elemente aus zugegriffen der `e` **EventArgs** -Objekt von der Ereignishandler empfangen: 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

Das **InfoPathEventHandler** -Attribut (gemäß der von der [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) -Klasse) ist das benutzerdefinierte Attribut für Funktionen, die als Ereignishandler verwendet werden. 
  
Wenn das Ereignis erforderlich, gibt die **MatchPath** -Parameters (wie von der [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) -Eigenschaft der **InfoPathEventHandlerAttribute** -Klasse definiert) einen XPath-Ausdruck, der die Ereignisquelle identifiziert. Der Parameter **EventType** (wie von der [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) -Eigenschaft der **InfoPathEventHandlerAttribute** -Klasse definiert) gibt den Typ des Ereignisses an. Sie sollten die Werte dieser Parameter nicht ändern. Wenn die Werte dieser Parameter geändert werden, der Ereignishandler möglicherweise nicht ordnungsgemäß kompiliert oder ereignisbenachrichtigung nicht wie erwartet ausgeführt. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Verbergen von Code in Ereignishandlern

Wenn Sie eine beim Verbergen Dienstprogramm ausführen, klicken Sie auf die Assembly, die generiert wird, wenn eine Formularvorlage mit verwaltetem Code wird kompiliert ( *Projektname* .dll), InfoPath werden nicht die Assembly zu laden, wenn ein Benutzer das Formular wird geöffnet. Wenn Sie den Code für die Ereignishandler oder anderen Formularcode zu verbergen möchten, müssen Sie fügen Sie den Code, die Sie in einer separaten Assembly verschleiern und auf diese Assembly in Ihrem Projekt verweisen möchten, und rufen Sie Mitglieder der referenzierten Assembly "FormCode.cs" oder "FormCode.vb". Es ist wichtig, dass Sie nur auf die Assembly verwiesen wird das Dienstprogramm beim Verbergen ausgeführt werden. 
  
## <a name="see-also"></a>Siehe auch

- [Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

