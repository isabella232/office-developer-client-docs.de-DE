---
title: Hinzufügen eines Ereignishandlers mithilfe des InfoPath-Objektmodells
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- onafterimport event [infopath 2007],OnAfterChange event [InfoPath 2007],OnBeforeChange event [InfoPath 2007],OnSubmitRequest event [InfoPath 2007],OnVersionUpgrade event [InfoPath 2007],InfoPath 2003-compatible form templates, event handlers,OnLoad event [InfoPath 2007],event handlers [InfoPath 2007], adding using InfoPath 2003 object model,OnValidate event [InfoPath 2007],OnContextChange event [InfoPath 2007],OnSaveRequest event [InfoPath 2007],OnClick event [InfoPath 2007], OnSwitchView-Ereignis [InfoPath 2007],OnSign-Ereignis [InfoPath 2007],OnMergeRequest-Ereignis [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Die Menübefehle zum Hinzufügen von Ereignishandlerfunktionen in einem Formularvorlagenprojekt, das mit dem InfoPath 2003-Objektmodell kompatibel ist, sind im Prinzip mit den Befehlen für andere Typen von Formularvorlagen identisch.
ms.openlocfilehash: 742af7d5b4a1b1b1c3b90dea2da80f4d85d7fac9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592900"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a>Hinzufügen eines Ereignishandlers mithilfe des InfoPath-Objektmodells

Die Menübefehle zum Hinzufügen von Ereignishandlerfunktionen in einem Formularvorlagenprojekt, das mit dem InfoPath 2003-Objektmodell kompatibel ist, sind im Prinzip mit den Befehlen für andere Typen von Formularvorlagen identisch. Um z. B. einen **OnLoad-Ereignishandler** hinzuzufügen, wenn die Formularvorlage im InfoPath-Designer geöffnet ist, klicken Sie auf der Registerkarte **"Entwickler"** auf den Befehl **"On Load Event".** Der Fokus wechselt automatisch zum Formularcode für den **OnLoad-Ereignishandler** im Code-Editor Visual Studio 2012. 
  
In mit InfoPath 2003 kompatiblen Projekten, die auf Formularvorlagen mit verwaltetem Code basieren, werden die Klasse mit den Ereignishandlerfunktionen sowie die Ereignishandler selbst durch InfoPath-spezifische Attribute im Codemodul identifiziert.

## <a name="adding-event-handlers"></a>Hinzufügen von Ereignishandlern

Bei allen folgenden Verfahren wird davon ausgegangen, dass in Microsoft InfoPath mit Visual Studio 2012 ein Formularvorlagenprojekt geöffnet ist.
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a>Hinzufügen eines Ereignishandlers für das OnClick-Ereignis einer Befehlsschaltfläche

1. Klicken Sie im Bereich **Steuerelemente** auf **Schaltfläche**, um dem Formular eine Schaltfläche hinzuzufügen. 
    
2. Klicken Sie auf der Registerkarte **Eigenschaften** auf **Benutzerdefinierter Code**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für das [OnClick-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "OnBeforeChange", "OnValidate" oder "OnAfterChange" eines Feldes oder einer Gruppe

1. Klicken Sie mit der rechten Maustaste auf ein an das Feld oder die Gruppe gebundenes Dateneingabe-Steuerelement, wie z. B. ein Steuerelement vom Typ **Textfeld**. 
    
2. Zeigen Sie auf **Programmierung**, und klicken Sie dann auf einen der Befehle, z. B. **On Validate-Ereignis**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für eines der folgenden Ereignisse im Code-Editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)oder [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx). 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für die Ereignisse "OnLoad", "OnSwitchView", "OnContextChange" oder "OnSign" eines Formulars

- Zeigen Sie im Menü **Extras** auf **Programmierung**, und klicken Sie dann auf das Formularereignis, für das ein Ereignishandler hinzugefügt werden soll.
    
    Der Fokus wechselt zum Stub für den Ereignishandler für einen der folgenden Elemente im Code-Editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)oder [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx). 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnSubmitRequest-Ereignis eines Formulars

1. Klicken Sie auf der Registerkarte **Daten** auf **Absendeoptionen**.
    
2. Aktivieren Sie das Kontrollkästchen **Übermitteln dieses Formulars durch Benutzer zulassen**, und klicken Sie dann auf **Benutzerdefinierte Aktion mithilfe von Code ausführen**.
    
3. Klicken Sie auf **Code bearbeiten** und dann auf **OK**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für das [OnSubmitRequest-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnSaveRequest-Ereignis eines Formulars

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Formularoptionen**.
    
2. Klicken Sie in der Kategorie **Speichern** auf **Speichern erfolgt mittels benutzerdefiniertem Code**, dann auf **Bearbeiten** und anschließen auf **OK**.
    
   Der Fokus wechselt zum Stub für den Ereignishandler für das [OnSaveRequest-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnVersionUpgrade-Ereignis eines Formulars

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Formularoptionen**.
    
2. Wählen Sie in der Kategorie **Versionsverwaltung** in der Liste **Vorhandene Formulare aktualisieren** den Eintrag **Benutzerdefiniertes Ereignis verwenden**, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.
    
    Der Fokus wechselt zum Stub für den Ereignishandler für das [OnVersionUpgrade-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) im Code-Editor. 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a>Hinzufügen eines Ereignishandlers für das OnMergeRequest-Ereignis eines Formulars

1. Klicken Sie auf die Registerkarte **Datei** und dann auf **Formularoptionen**.
    
2. Aktivieren Sie in der Kategorie **Erweitert** die Kontrollkästchen **Zusammenführen von Formularen aktivieren** und **Mithilfe von benutzerdefiniertem Code zusammenführen**, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.
    
    Der Fokus wechselt zum Stub für den Ereignishandler für das [OnMergeRequest-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) im Code-Editor. 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a>Hinzufügen eines Ereignishandlers für das OnAfterImport-Ereignis

Zum Hinzufügen von Ereignishandlern für das [OnAfterImport-Ereignis](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) müssen Sie den Formularcode für die Formularvorlage mit verwaltetem Code öffnen und die Ereignishandlerfunktion manuell hinzufügen. Informationen zum Erstellen eines Ereignishandlers für dieses Ereignis finden Sie, wenn Sie auf die Verknüpfung für das **OnAfterImport**-Ereignis klicken. 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a>Hinzufügen eines Ereignishandlers für eine sekundäre Datenquelle

Im folgenden Beispiel wird gezeigt, wie ein Ereignishandler für eine sekundäre Datenquelle hinzugefügt wird. Bei diesem Beispiel wird von einer sekundären Datenquelle in der Ressourcendatei "books.xml" ausgegangen, die folgendes Schema aufweist:
  
```xml
<?xml version="1.0"?>
<xsd:schema xmlns:xsd="https://www.w3.org/2001/XMLSchema">
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

Die Ansicht des Formulars wird aus dieser Datenquelle erstellt. Der Formularcode erstellt eine Hashtabelle, die auf den Autoren und der Anzahl von deren Büchern basiert. Sie können einen Eintrag aus der in der Ansicht gezeigten Tabelle aktualisieren; dann aktualisiert der **OnAfterChange**-Ereignishandler die Hashtabelle. Beachten Sie, dass die [DataObject-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) des **InfoPathEventHandler-Attributs** (das von der [InfoPathEventHandlerAttribute-Klasse](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) implementiert wird) verwendet wird, um auf die sekundäre Datenquelle zu verweisen. 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a>Wie die Klasse identifiziert wird, die Ereignishandler enthält

Wenn Sie ein neues InfoPath-Formularvorlagenprojekt erstellen, das mit dem InfoPath 2003-Objektmodell mit verwaltetem Code kompatibel ist, wird ein **System.ComponentModel.Description**-Attribut auf Assemblyebene am Anfang des Formularcodemoduls auf die Klasse angewendet, um die Klasse zu identifizieren, die alle Ereignishandler für die Formularvorlage enthält. 
  
> [!IMPORTANT]
> Ändern Sie das **System.ComponentModel.Description**-Attribut in dieser Klasse nicht. Bei einer Änderung kann von der Formularvorlage die Position der Ereignishandler nicht identifiziert werden, und die Ereignishandler werden nicht ausgeführt. 
  
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

## <a name="how-event-handlers-are-identified"></a>Identifizieren von Ereignishandlern

Wenn Sie einen neuen Ereignishandler über Menübefehle oder Schaltflächen auf der InfoPath-Benutzeroberfläche im Entwurfsmodus hinzufügen, wird der Stub für die Ereignishandlerfunktion in das Formular geschrieben. Das folgende Beispiel zeigt den Stub-Ereignishandler, der für ein [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) erstellt wurde, das für ein Feld namens "total" hinzugefügt wurde. 
  
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

Sie können dann Code hinzufügen, der Elemente des InfoPath-Objektmodells mithilfe der privaten zwischengespeicherten Elemente der  `thisXDocument` oder  `thisApplication` Variablen aufruft, oder indem Sie die Member verwenden, auf die über das  `e` **EventArgs-Objekt** zugegriffen wird, das vom Ereignishandler empfangen wurde: 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

Das **InfoPathEventHandler-Attribut** (gemäß Definition durch die [InfoPathEventHandlerAttribute-Klasse)](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) ist das benutzerdefinierte Attribut für Funktionen, die als Ereignishandler verwendet werden. 
  
Wenn dies für das Ereignis erforderlich ist, gibt der **MatchPath-Parameter** (wie durch die [MatchPath-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) der **InfoPathEventHandlerAttribute-Klasse** definiert) einen XPath-Ausdruck an, der die Ereignisquelle identifiziert. Der **Parameter EventType** (gemäß Definition durch die [EventType-Eigenschaft](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) der **InfoPathEventHandlerAttribute-Klasse)** gibt den Ereignistyp an. Die Werte dieser Parameter sollten nicht geändert werden. Wenn die Werte geändert werden, wird die Kompilierung des Ereignishandlers möglicherweise nicht richtig abgeschlossen, oder eine Ereignisbenachrichtigung wird nicht wie erwartet ausgeführt. 
  
## <a name="obfuscating-code-in-event-handlers"></a>Verschleieren von Code in Ereignishandlern

Wenn Sie ein Verschleierungsprogramm für die Assembly ausführen, die generiert wird, wenn eine Formularvorlage mit verwaltetem Code kompiliert wird *(Projektname*  .dll), kann InfoPath die Assembly nicht laden, wenn ein Benutzer das Formular öffnet. Falls Sie den Code für Ereignishandler oder anderen Formularcode verbergen möchten, müssen Sie den zu verbergenden Code in eine separate Assembly stellen, im Projekt auf diese Assembly verweisen und dann Member der referenzierten Assembly aus "FormCode.cs" oder "FormCode.vb" aufrufen. Es ist wichtig, dass Sie das Hilfsprogramm zum Verbergen nur für die referenzierte Assembly ausführen. 
  
## <a name="see-also"></a>Siehe auch

- [Reagieren auf Formularereignisse mithilfe des InfoPath 2003-Objektmodells](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

