---
title: Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell
manager: soliver
ms.date: 01/20/2015
ms.audience: Developer
keywords:
- OnAfterImport-Ereignis [InfoPath 2007], OnAfterChange-Ereignis [InfoPath 2007], OnBeforeChange-Ereignis [InfoPath 2007], OnSubmitRequest-Ereignis [InfoPath 2007], OnVersionUpgrade-Ereignis [InfoPath 2007], InfoPath 2003-kompatible Formularvorlagen, Ereignishandler, OnLaden-Ereignis [InfoPath 2007], Ereignishandler [InfoPath 2007], hinzufügen mit InfoPath 2003-Objektmodell, OnValidate-Ereignis [InfoPath 2007], OnContextChange-Ereignis [InfoPath 2007], OnSaveRequest-Ereignis [InfoPath 2007], OnClick-Ereignis [InfoPath 2007], OnSwitchView-Ereignis [InfoPath 2007], onSign-Ereignis [InfoPath 2007], OnMergeRequest-Ereignis [InfoPath 2007]
localization_priority: Normal
ms.assetid: 0520df55-2d91-4cc5-be31-82144a2db4f6
description: Die Menübefehle zum Hinzufügen von Ereignishandlerfunktionen in einem Formularvorlagenprojekt, das mit dem InfoPath 2003-Objektmodell kompatibel ist, sind im Prinzip mit den Befehlen für andere Typen von Formularvorlagen identisch.
ms.openlocfilehash: 8533b6bc11dccdad9d0f05de35406ad3cf68eacd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303668"
---
# <a name="add-an-event-handler-using-the-infopath-object-model"></a><span data-ttu-id="14559-104">Hinzufügen eines Ereignishandlers mit dem InfoPath-Objektmodell</span><span class="sxs-lookup"><span data-stu-id="14559-104">Add an event handler using the InfoPath object model</span></span>

<span data-ttu-id="14559-105">Die Menübefehle zum Hinzufügen von Ereignishandlerfunktionen in einem Formularvorlagenprojekt, das mit dem InfoPath 2003-Objektmodell kompatibel ist, sind im Prinzip mit den Befehlen für andere Typen von Formularvorlagen identisch.</span><span class="sxs-lookup"><span data-stu-id="14559-105">The menu commands for adding event handler functions in a form template project that is compatible with the InfoPath 2003 object model are essentially the same as those for other types of form templates.</span></span> <span data-ttu-id="14559-106">Wenn Sie beispielsweise einen onLaden- \*\*\*\* Ereignishandler hinzufügen möchten, während die Formularvorlage im InfoPath-Designer geöffnet ist, klicken Sie auf der Registerkarte **Entwickler** auf den Befehl **beim Laden** . Der Fokus wechselt automatisch in den Code-Editor von \*\*\*\* Visual Studio 2012 in den Formularcode für den onlade-Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="14559-106">For example, in order to add an **OnLoad** event handler, with the form template open in the InfoPath designer, click the **On Load Event** command on the **Developer** tab. The focus automatically switches to the form code for the **OnLoad** event handler in the Visual Studio 2012 code editor.</span></span> 
  
<span data-ttu-id="14559-107">In mit InfoPath 2003 kompatiblen Projekten, die auf Formularvorlagen mit verwaltetem Code basieren, werden die Klasse mit den Ereignishandlerfunktionen sowie die Ereignishandler selbst durch InfoPath-spezifische Attribute im Codemodul identifiziert.</span><span class="sxs-lookup"><span data-stu-id="14559-107">In managed-code form template projects compatible with InfoPath 2003, the class that contains event handler functions and the event handlers themselves are identified by attributes specific to InfoPath in the code module.</span></span>

## <a name="adding-event-handlers"></a><span data-ttu-id="14559-108">Hinzufügen von Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="14559-108">Adding event handlers</span></span>

<span data-ttu-id="14559-109">Bei allen folgenden Verfahren wird davon ausgegangen, dass ein Formularvorlagenprojekt in Microsoft InfoPath mit Visual Studio 2012 geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="14559-109">All of the following procedures assume that you have a form template project open in Microsoft InfoPath with Visual Studio 2012.</span></span>
  
### <a name="add-an-event-handler-for-the-onclick-event-of-a-command-button"></a><span data-ttu-id="14559-110">Hinzufügen eines Ereignishandlers für das OnClick-Ereignis einer Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="14559-110">Add an event handler for the OnClick event of a command button</span></span>

1. <span data-ttu-id="14559-111">Klicken Sie im Bereich **Steuerelemente** auf **Schaltfläche**, um dem Formular eine Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="14559-111">In the **Controls** pane, click **Button** to add a button to the form.</span></span> 
    
2. <span data-ttu-id="14559-112">Klicken Sie auf der Registerkarte **Eigenschaften** auf **Benutzerdefinierter Code**.</span><span class="sxs-lookup"><span data-stu-id="14559-112">On the **Properties** tab, click **Custom Code**.</span></span>
    
   <span data-ttu-id="14559-113">Der Fokus wechselt zum Stub für den Ereignishandler für das [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) -Ereignis im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="14559-113">The focus switches to the stub for the event handler for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onbeforechange-onvalidate-or-onafterchange-event-of-a-field-or-group"></a><span data-ttu-id="14559-114">Hinzufügen eines Ereignishandlers für die Ereignisse "OnBeforeChange", "OnValidate" oder "OnAfterChange" eines Feldes oder einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="14559-114">Add an event handler for the OnBeforeChange, OnValidate, or OnAfterChange event of a field or group</span></span>

1. <span data-ttu-id="14559-115">Klicken Sie mit der rechten Maustaste auf ein an das Feld oder die Gruppe gebundenes Dateneingabe-Steuerelement, wie z. B. ein Steuerelement vom Typ **Textfeld**.</span><span class="sxs-lookup"><span data-stu-id="14559-115">Right-click a data-entry control bound to the field or group, such as a **Text Box** control.</span></span> 
    
2. <span data-ttu-id="14559-116">Zeigen Sie auf **Programmierung**, und klicken Sie dann auf einen der Befehle, z. B. **On Validate-Ereignis**.</span><span class="sxs-lookup"><span data-stu-id="14559-116">Point to **Programming**, and then click one of the commands, such as **On Validate Event**.</span></span>
    
   <span data-ttu-id="14559-117">Der Fokus wechselt zum Stub für den Ereignishandler für eines der folgenden Ereignisse im Code-Editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), OnValidate [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx)oder [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span><span class="sxs-lookup"><span data-stu-id="14559-117">The focus switches to the stub for the event handler for one of the following events in the code editor: [OnBeforeChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnBeforeChange.aspx), [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx), or [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onload-onswitchview-oncontextchange-or-onsign-event-of-a-form"></a><span data-ttu-id="14559-118">Hinzufügen eines Ereignishandlers für die Ereignisse "OnLoad", "OnSwitchView", "OnContextChange" oder "OnSign" eines Formulars</span><span class="sxs-lookup"><span data-stu-id="14559-118">Add an event handler for the OnLoad, OnSwitchView, OnContextChange, or OnSign event of a form</span></span>

- <span data-ttu-id="14559-119">Zeigen Sie im Menü **Extras** auf **Programmierung**, und klicken Sie dann auf das Formularereignis, für das ein Ereignishandler hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="14559-119">On the **Tools** menu, point to **Programming**, and then click the form event that you want to write an event handler for.</span></span>
    
    <span data-ttu-id="14559-120">Der Fokus wechselt zum Stub für den Ereignishandler für einen der folgenden im Code-Editor: onLaden [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx)oder OnSign. [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx)</span><span class="sxs-lookup"><span data-stu-id="14559-120">The focus switches to the stub for the event handler for one of the following in the code editor: [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx), [OnSwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSwitchView.aspx), [OnContextChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnContextChange.aspx), or [OnSign](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSign.aspx).</span></span> 
    
### <a name="add-an-event-handler-for-the-onsubmitrequest-event-of-a-form"></a><span data-ttu-id="14559-121">Hinzufügen eines Ereignishandlers für das OnSubmitRequest-Ereignis eines Formulars</span><span class="sxs-lookup"><span data-stu-id="14559-121">Add an event handler for the OnSubmitRequest event of a form</span></span>

1. <span data-ttu-id="14559-122">Klicken Sie auf der Registerkarte **Daten** auf **Absendeoptionen**.</span><span class="sxs-lookup"><span data-stu-id="14559-122">On the **Data** tab, click **Submit Options**.</span></span>
    
2. <span data-ttu-id="14559-123">Aktivieren Sie das Kontrollkästchen **Übermitteln dieses Formulars durch Benutzer zulassen**, und klicken Sie dann auf **Benutzerdefinierte Aktion mithilfe von Code ausführen**.</span><span class="sxs-lookup"><span data-stu-id="14559-123">Select the **Allow users to submit this form** check box, and then click **Perform custom action using Code**.</span></span>
    
3. <span data-ttu-id="14559-124">Klicken Sie auf **Code bearbeiten** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="14559-124">Click **Edit Code**, and then click **OK**.</span></span>
    
   <span data-ttu-id="14559-125">Der Fokus wechselt zum Stub für den Ereignishandler für das [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) -Ereignis im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="14559-125">The focus switches to the stub for the event handler for the [OnSubmitRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSubmitRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onsaverequest-event-of-a-form"></a><span data-ttu-id="14559-126">Hinzufügen eines Ereignishandlers für das OnSaveRequest-Ereignis eines Formulars</span><span class="sxs-lookup"><span data-stu-id="14559-126">Add an event handler for the OnSaveRequest event of a form</span></span>

1. <span data-ttu-id="14559-127">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="14559-127">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="14559-128">Klicken Sie in der Kategorie **Speichern** auf **Speichern erfolgt mittels benutzerdefiniertem Code**, dann auf **Bearbeiten** und anschließen auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="14559-128">In the **Save** category, click **Save using custom code**, click **Edit**, and then click **OK**.</span></span>
    
   <span data-ttu-id="14559-129">Der Fokus wechselt zum Stub für den Ereignishandler für das [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) -Ereignis im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="14559-129">The focus switches to the stub for the event handler for the [OnSaveRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnSaveRequest.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onversionupgrade-event-of-a-form"></a><span data-ttu-id="14559-130">Hinzufügen eines Ereignishandlers für das OnVersionUpgrade-Ereignis eines Formulars</span><span class="sxs-lookup"><span data-stu-id="14559-130">Add an event handler for the OnVersionUpgrade event of a form</span></span>

1. <span data-ttu-id="14559-131">Klicken Sie auf die Registerkarte **Datei**, und klicken Sie dann auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="14559-131">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="14559-132">Wählen Sie in der Kategorie **Versionsverwaltung** in der Liste **Vorhandene Formulare aktualisieren** den Eintrag **Benutzerdefiniertes Ereignis verwenden**, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="14559-132">In the **Versioning** category, select **Use custom event** from the **Update existing forms** list, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="14559-133">Der Fokus wechselt zum Stub für den Ereignishandler für das [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) -Ereignis im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="14559-133">The focus switches to the stub for the event handler for the [OnVersionUpgrade](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnVersionUpgrade.aspx) event in the code editor.</span></span> 
    
### <a name="add-an-event-handler-for-the-onmergerequest-event-of-a-form"></a><span data-ttu-id="14559-134">Hinzufügen eines Ereignishandlers für das OnMergeRequest-Ereignis eines Formulars</span><span class="sxs-lookup"><span data-stu-id="14559-134">Add an event handler for the OnMergeRequest event of a form</span></span>

1. <span data-ttu-id="14559-135">Klicken Sie auf die Registerkarte **Datei** und dann auf **Formularoptionen**.</span><span class="sxs-lookup"><span data-stu-id="14559-135">Click the **File** tab, and then click **Form Options**.</span></span>
    
2. <span data-ttu-id="14559-136">Aktivieren Sie in der Kategorie **Erweitert** die Kontrollkästchen **Zusammenführen von Formularen aktivieren** und **Mithilfe von benutzerdefiniertem Code zusammenführen**, klicken Sie auf **Bearbeiten**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="14559-136">In the **Advanced** category, select the **Enable Form merging** and the **Merge using custom code** check boxes, click **Edit**, and then click **OK**.</span></span>
    
    <span data-ttu-id="14559-137">Der Fokus wechselt zum Stub für den Ereignishandler für das [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) -Ereignis im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="14559-137">The focus switches to the stub for the event handler for the [OnMergeRequest](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnMergeRequest.aspx) event in the code editor.</span></span> 
    
## <a name="adding-an-event-handler-for-the-onafterimport-event"></a><span data-ttu-id="14559-138">Hinzufügen eines Ereignishandlers für das OnAfterImport-Ereignis</span><span class="sxs-lookup"><span data-stu-id="14559-138">Adding an event handler for the OnAfterImport event</span></span>

<span data-ttu-id="14559-139">Um Ereignishandler für das [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) -Ereignis hinzuzufügen, müssen Sie den Formularcode für die Formularvorlage mit verwaltetem Code öffnen und die Ereignishandlerfunktion manuell hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14559-139">To add event handlers for the [OnAfterImport](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnAfterImport.aspx) event, you must open the form code for your managed-code form template and add the event handler function manually.</span></span> <span data-ttu-id="14559-140">Informationen zum Erstellen eines Ereignishandlers für dieses Ereignis finden Sie, wenn Sie auf die Verknüpfung für das **OnAfterImport**-Ereignis klicken.</span><span class="sxs-lookup"><span data-stu-id="14559-140">For information on how to write an event handler for this event, click the link for the **OnAfterImport** event.</span></span> 
  
## <a name="adding-an-event-handler-for-a-secondary-data-source"></a><span data-ttu-id="14559-141">Hinzufügen eines Ereignishandlers für eine sekundäre Datenquelle</span><span class="sxs-lookup"><span data-stu-id="14559-141">Adding an event handler for a secondary data source</span></span>

<span data-ttu-id="14559-p103">Im folgenden Beispiel wird gezeigt, wie ein Ereignishandler für eine sekundäre Datenquelle hinzugefügt wird. Bei diesem Beispiel wird von einer sekundären Datenquelle in der Ressourcendatei "books.xml" ausgegangen, die folgendes Schema aufweist:</span><span class="sxs-lookup"><span data-stu-id="14559-p103">The following example shows how to add an event handler for a secondary data source. The example assumes a secondary data source from a resource file named books.xml, which has the following schema:</span></span>
  
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

<span data-ttu-id="14559-144">Die Ansicht des Formulars wird aus dieser Datenquelle erstellt.</span><span class="sxs-lookup"><span data-stu-id="14559-144">The form's view is built from this data source.</span></span> <span data-ttu-id="14559-145">Der Formularcode erstellt eine Hashtabelle, die auf den Autoren und der Anzahl von deren Büchern basiert.</span><span class="sxs-lookup"><span data-stu-id="14559-145">The form code creates a hash table based on the authors and the number of books they have written.</span></span> <span data-ttu-id="14559-146">Sie können einen Eintrag aus der in der Ansicht gezeigten Tabelle aktualisieren; dann aktualisiert der **OnAfterChange**-Ereignishandler die Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="14559-146">You can update an entry from the table shown in the view and the **OnAfterChange** event handler updates the hash table.</span></span> <span data-ttu-id="14559-147">Beachten Sie, dass die [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) -Eigenschaft des **InfoPathEventHandler** -Attributs (das von der [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) -Klasse implementiert wird) verwendet wird, um auf die sekundäre Datenquelle zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="14559-147">Note that the [DataObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.DataObject.aspx) property of the **InfoPathEventHandler** attribute (which is implemented by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is used to reference the secondary data source.</span></span> 
  
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

## <a name="how-the-class-that-contains-event-handlers-is-identified"></a><span data-ttu-id="14559-148">Wie die Klasse, die Ereignishandler enthält, identifiziert wird</span><span class="sxs-lookup"><span data-stu-id="14559-148">How the class that contains event handlers is identified</span></span>

<span data-ttu-id="14559-149">Wenn Sie ein neues InfoPath-Formularvorlagenprojekt erstellen, das mit dem InfoPath 2003-Objektmodell mit verwaltetem Code kompatibel ist, wird ein **System.ComponentModel.Description**-Attribut auf Assemblyebene am Anfang des Formularcodemoduls auf die Klasse angewendet, um die Klasse zu identifizieren, die alle Ereignishandler für die Formularvorlage enthält.</span><span class="sxs-lookup"><span data-stu-id="14559-149">When you create a new InfoPath form template project that is compatible with the InfoPath 2003 managed code object model, an assembly-level **System.ComponentModel.Description** attribute is applied to the class at the beginning of the form code module to identify the class that contains all event handlers for the form template.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="14559-150">Ändern Sie das **System.ComponentModel.Description**-Attribut in dieser Klasse nicht.</span><span class="sxs-lookup"><span data-stu-id="14559-150">Do not modify the **System.ComponentModel.Description** attribute in this class.</span></span> <span data-ttu-id="14559-151">Bei einer Änderung kann von der Formularvorlage die Position der Ereignishandler nicht identifiziert werden, und die Ereignishandler werden nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14559-151">If you do so, your form template will not be able to identify where event handlers are located, and the event handlers will fail to run.</span></span> 
  
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

## <a name="how-event-handlers-are-identified"></a><span data-ttu-id="14559-152">Identifizierung von Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="14559-152">How event handlers are identified</span></span>

<span data-ttu-id="14559-153">Wenn Sie einen neuen Ereignishandler über Menübefehle oder Schaltflächen auf der InfoPath-Benutzeroberfläche im Entwurfsmodus hinzufügen, wird der Stub für die Ereignishandlerfunktion in das Formular geschrieben.</span><span class="sxs-lookup"><span data-stu-id="14559-153">When you add a new event handler using menu commands or buttons in the InfoPath design mode user interface, the stub for the event handler function is written into the form.</span></span> <span data-ttu-id="14559-154">Das folgende Beispiel zeigt den Stub-Ereignishandler, der [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) für ein OnValidate-Element erstellt wurde, das für ein Feld mit dem Namen "Total" hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="14559-154">The following example shows the stub event handler created for an [OnValidate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnValidate.aspx) added for a field named 'total'.</span></span> 
  
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

<span data-ttu-id="14559-155">Anschließend können Sie Code hinzufügen, mit dem Member des InfoPath-Objektmodells mithilfe der privaten zwischengespeicherten Member `thisXDocument` der `thisApplication` Variablen or aufgerufen werden, oder mithilfe der Elemente, `e` auf die über das vom Ereignishandler empfangene **EventArgs** -Objekt zugegriffen wird:</span><span class="sxs-lookup"><span data-stu-id="14559-155">You can then add code that invokes members of the InfoPath object model using the private cached members of the  `thisXDocument` or  `thisApplication` variables, or by using the members accessed from the  `e` **EventArgs** object received by the event handler:</span></span> 
  
```cs
thisXDocument.UI.Alert.(e.Site.text);

```

```vb
thisXDocument.UI.Alert.(e.Site.text)

```

<span data-ttu-id="14559-156">Das **InfoPathEventHandler** -Attribut (wie von der [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) -Klasse definiert) ist das benutzerdefinierte Attribut für Funktionen, die als Ereignishandler verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14559-156">The **InfoPathEventHandler** attribute (as defined by the [InfoPathEventHandlerAttribute](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.aspx) class) is the custom attribute for functions that will be used as event handlers.</span></span> 
  
<span data-ttu-id="14559-157">Wenn das Ereignis dies erfordert, gibt der Parameter **MatchPath** (wie durch die [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) -Eigenschaft der **InfoPathEventHandlerAttribute** -Klasse definiert) einen XPath-Ausdruck an, der die Ereignisquelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="14559-157">When required by the event, the **MatchPath** parameter (as defined by the [MatchPath](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.MatchPath.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies an XPath expression that identifies the event source.</span></span> <span data-ttu-id="14559-158">Der **eventType** -Parameter (gemäß Definition durch [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) die EventType-Eigenschaft der **InfoPathEventHandlerAttribute** -Klasse) gibt den Typ des Ereignisses an.</span><span class="sxs-lookup"><span data-stu-id="14559-158">The **EventType** parameter (as defined by the [EventType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.InfoPathEventHandlerAttribute.EventType.aspx) property of the **InfoPathEventHandlerAttribute** class) specifies the type of event.</span></span> <span data-ttu-id="14559-159">Die Werte dieser Parameter sollten nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="14559-159">You should not change the values of these parameters.</span></span> <span data-ttu-id="14559-160">Wenn die Werte geändert werden, wird die Kompilierung des Ereignishandlers möglicherweise nicht richtig abgeschlossen, oder eine Ereignisbenachrichtigung wird nicht wie erwartet ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14559-160">If the values of these parameters are changed, the event handler may not compile correctly, or event notification will not occur as expected.</span></span> 
  
## <a name="obfuscating-code-in-event-handlers"></a><span data-ttu-id="14559-161">VerSchleiern von Code in Ereignishandlern</span><span class="sxs-lookup"><span data-stu-id="14559-161">Obfuscating code in event handlers</span></span>

<span data-ttu-id="14559-162">Wenn Sie ein verschleiern-Dienstprogramm für die Assembly ausführen, die beim Kompilieren einer Formularvorlage mit verwaltetem \*\* Code (ProjectName. dll) generiert wird, kann InfoPath die Assembly nicht laden, wenn ein Benutzer das Formular öffnet.</span><span class="sxs-lookup"><span data-stu-id="14559-162">If you run an obfuscator utility on the assembly that is generated when a managed-code form template is compiled ( *projectname*  .dll), InfoPath will not be able to load the assembly when a user opens the form.</span></span> <span data-ttu-id="14559-163">Falls Sie den Code für Ereignishandler oder anderen Formularcode verbergen möchten, müssen Sie den zu verbergenden Code in eine separate Assembly stellen, im Projekt auf diese Assembly verweisen und dann Member der referenzierten Assembly aus "FormCode.cs" oder "FormCode.vb" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="14559-163">If you want to obfuscate the code for your event handlers or other form code, you must put the code that you want to obfuscate in a separate assembly, and reference that assembly in your project, and then call members of the referenced assembly from FormCode.cs or FormCode.vb.</span></span> <span data-ttu-id="14559-164">Es ist wichtig, dass Sie das Hilfsprogramm zum Verbergen nur für die referenzierte Assembly ausführen.</span><span class="sxs-lookup"><span data-stu-id="14559-164">It is important that you run the obfuscator utility only on the referenced assembly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="14559-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14559-165">See also</span></span>

- [<span data-ttu-id="14559-166">Reagieren auf Formularereignisse mit dem InfoPath-Objektmodell 2003</span><span class="sxs-lookup"><span data-stu-id="14559-166">Respond to Form Events Using the InfoPath 2003 Object Model</span></span>](how-to-respond-to-form-events-using-the-infopath-2003-object-model.md)

