---
title: Szenario für Veröffentlichungen im Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f481c4bc5cf11f9345458b3859c099b40a79885
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026449"
---
# <a name="internet-publishing-scenario"></a><span data-ttu-id="3b1ef-102">Szenario für Veröffentlichungen im Internet</span><span class="sxs-lookup"><span data-stu-id="3b1ef-102">Internet publishing scenario</span></span>

<span data-ttu-id="3b1ef-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3b1ef-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3b1ef-p101">Mit diesem Code wird die Verwendung von ADO (ActiveX Data Objects) mit dem Microsoft OLE DB-Anbieter für Internet Publishing veranschaulicht. In diesem Szenario erstellen Sie eine Visual Basic-Anwendung, von der mithilfe der Objekte **Recordset**, **Record** und **Stream** die Inhalte von Ressourcen angezeigt werden, die mit dem Internet Publishing-Anbieter veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-p101">This code example demonstrates how to use ADO with the Microsoft OLE DB Provider for Internet Publishing. In this scenario, you will create a Visual Basic application that uses **Recordset**, **Record**, and **Stream** objects to display the contents of resources published with the Internet Publishing Provider.</span></span>

<span data-ttu-id="3b1ef-106">Für die Erstellung dieses Szenarios sind die folgenden Schritte erforderlich:</span><span class="sxs-lookup"><span data-stu-id="3b1ef-106">The following steps are necessary to create this scenario:</span></span> 

1. <span data-ttu-id="3b1ef-107">Richten Sie das Visual Basic-Projekt.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-107">Set up the Visual Basic project.</span></span>
2. <span data-ttu-id="3b1ef-108">Initialisieren Sie das Listenfeld Main.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-108">Initialize the Main list box.</span></span>
3. <span data-ttu-id="3b1ef-109">Füllen Sie die Listenfelds "Fields" auf.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-109">Populate the Fields list box.</span></span>
4. <span data-ttu-id="3b1ef-110">Füllen Sie das Textfeld "Details" auf.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-110">Populate the Details text box.</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="3b1ef-111">Schritt 1: Einrichten des Visual Basic-Projekts</span><span class="sxs-lookup"><span data-stu-id="3b1ef-111">Step 1: Set up the Visual Basic project</span></span>

<span data-ttu-id="3b1ef-112">Dieses Szenario geht davon aus, dass Sie Microsoft Visual Basic 6.0 oder höher, ADO 2.5 oder höher und den Microsoft OLE DB-Anbieter für Internet Publishing auf dem System installiert haben.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-112">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

### <a name="create-an-ado-project"></a><span data-ttu-id="3b1ef-113">Erstellen Sie ein ADO-Projekt</span><span class="sxs-lookup"><span data-stu-id="3b1ef-113">Create an ADO project</span></span>

1.  <span data-ttu-id="3b1ef-114">Erstellen Sie in Microsoft Visual Basic ein neues Standard EXE-Projekt.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-114">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="3b1ef-115">Klicken Sie im Menü **Project** auf **References**.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-115">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="3b1ef-116">Wählen Sie **Microsoft ActiveX Data Objects 2.5 Library**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-116">Select **Microsoft ActiveX Data Objects 2.5 Library**, and then click **OK**.</span></span>

### <a name="insert-controls-on-the-main-form"></a><span data-ttu-id="3b1ef-117">Fügen Sie Steuerelemente im Hauptformular</span><span class="sxs-lookup"><span data-stu-id="3b1ef-117">Insert controls on the main form</span></span>

1.  <span data-ttu-id="3b1ef-118">Fügen Sie ein ListBox-Steuerelement zu Form1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-118">Add a ListBox control to Form1.</span></span> <span data-ttu-id="3b1ef-119">Legen Sie die **Name** -Eigenschaft auf **IstMain**.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-119">Set its **Name** property to **lstMain**.</span></span>

2.  <span data-ttu-id="3b1ef-120">Fügen Sie ein anderes ListBox-Steuerelement zu Form1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-120">Add another ListBox control to Form1.</span></span> <span data-ttu-id="3b1ef-121">Legen Sie die **Name** -Eigenschaft auf **LstDetails**.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-121">Set its **Name** property to **lstDetails**.</span></span>

3.  <span data-ttu-id="3b1ef-122">Fügen Sie ein TextBox-Steuerelement zu Form1 hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-122">Add a TextBox control to Form1.</span></span> <span data-ttu-id="3b1ef-123">Legen Sie die **Name** -Eigenschaft auf **TxtDetails**.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-123">Set its **Name** property to **txtDetails**.</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="3b1ef-124">Schritt 2: Initialisieren des Main-Listenfelds</span><span class="sxs-lookup"><span data-stu-id="3b1ef-124">Step 2: Initialize the Main list box</span></span>

### <a name="declare-global-record-and-recordset-objects"></a><span data-ttu-id="3b1ef-125">Deklarieren Sie globale Objekte Record und Recordset</span><span class="sxs-lookup"><span data-stu-id="3b1ef-125">Declare global Record and Recordset objects</span></span>

- <span data-ttu-id="3b1ef-126">Fügen Sie den folgenden Code in (General) (Declarations) für Form1 ein:
</span><span class="sxs-lookup"><span data-stu-id="3b1ef-126">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   <span data-ttu-id="3b1ef-127">Dieser Code deklariert globale Objektverweise für die Objekte **Record** und **Recordset**, die später in diesem Szenario verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-127">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

### <a name="connect-to-a-url-and-populate-lstmain"></a><span data-ttu-id="3b1ef-128">Verbinden mit einer URL und Auffüllen von IstMain</span><span class="sxs-lookup"><span data-stu-id="3b1ef-128">Connect to a URL and populate lstMain</span></span>

- <span data-ttu-id="3b1ef-129">Fügen Sie im Form Load-Ereignishandler für Form1 den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="3b1ef-129">Insert the following code into the Form Load event handler for Form1:</span></span>
    
   ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
   ```
    
   <span data-ttu-id="3b1ef-130">Dieser Code instanziiert die globalen Objekte **Record** und **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-130">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="3b1ef-131">Der **Eintrag** `grec` mit einer URL angegeben als **ActiveConnection**geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-131">The **Record** `grec` is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="3b1ef-132">Wenn die URL vorhanden ist, wird sie geöffnet. Wenn er nicht bereits vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-132">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> 
   
   <span data-ttu-id="3b1ef-133">Notiz, die Sie ersetzen soll `https://servername/foldername/` durch eine gültige URL aus der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-133">Note that you should replace `https://servername/foldername/` with a valid URL from your environment.</span></span> 
   
   <span data-ttu-id="3b1ef-134">Das **Recordset-Objekt** `grs` wird geöffnet, auf die untergeordneten Elemente des **Datensatzes** `grec`.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-134">The **Recordset** `grs` is opened on the children of the **Record** `grec`.</span></span> <span data-ttu-id="3b1ef-135">Die IstMain wird dann mit den Dateinamen der URL veröffentlichten Ressourcen aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-135">The lstMain is then populated with the file names of the resources published to the URL.</span></span>

## <a name="step-3-populate-the-fields-list-box"></a><span data-ttu-id="3b1ef-136">Schritt 3: Füllen Sie Listenfelds "Fields auf"</span><span class="sxs-lookup"><span data-stu-id="3b1ef-136">Step 3: Populate the Fields list box</span></span>

- <span data-ttu-id="3b1ef-137">Fügen Sie im Click-Ereignishandler von IstMain den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="3b1ef-137">Insert the following code into the Click event handler of lstMain:</span></span>

   ```vb 
    
    Private Sub lstMain_Click() 
        Dim rec As Record 
        Dim rs As Recordset 
        Set rec = New Record 
        Set rs = New Recordset 
        grs.MoveFirst 
        grs.Move lstMain.ListIndex 
        lstDetails.Clear 
        rec.Open grs 
        Select Case rec.RecordType 
            Case adCollectionRecord: 
                Set rs = rec.GetChildren 
                While Not rs.EOF 
                    lstDetails.AddItem rs(0) 
                    rs.MoveNext 
                Wend 
            Case adSimpleRecord: 
                recFields rec, lstDetails, txtDetails 
                
            Case adStructDoc: 
        End Select 
        
    End Sub 
   ```

   <span data-ttu-id="3b1ef-138">Dieser Code deklariert und instanziiert die lokalen **Record** und **Recordset** -Objekte `rec` und `rs`fest.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-138">This code declares and instantiates local **Record** and **Recordset** objects `rec` and `rs`respectively.</span></span>

   <span data-ttu-id="3b1ef-139">Die Zeile, die in LstMain ausgewählten Ressource entspricht, erfolgt die aktuelle Zeile des `grs`.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-139">The row corresponding to the resource selected in lstMain is made the current row of `grs`.</span></span> <span data-ttu-id="3b1ef-140">Das Listenfeld **Details** wird anschließend gelöscht und `rec` wird geöffnet, mit der aktuellen Zeile des `grs` als Quelle.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-140">The **Details** list box is then cleared and `rec` is opened with the current row of `grs` as the source.</span></span>

   <span data-ttu-id="3b1ef-141">Wenn die Ressource einen Auflistungsdatensatz handelt (wie durch **RecordType**angegeben), das lokale **Recordset** `rs` wird geöffnet, auf die untergeordneten Elemente des `rec`.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-141">If the resource is a collection record (as specified by **RecordType**), the local **Recordset** `rs` is opened on the children of `rec`.</span></span> <span data-ttu-id="3b1ef-142">wird mit den Werten aus den Zeilen LstDetails gefüllt `rs`.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-142">lstDetails is then filled with the values from the rows of `rs`.</span></span>

   <span data-ttu-id="3b1ef-143">Wenn die Ressource ein einfacher Datensatz, `recFields` aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-143">If the resource is a simple record, `recFields` is called.</span></span> <span data-ttu-id="3b1ef-144">Weitere Informationen zu `recFields`, finden Sie im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-144">For more information about `recFields`, see the next step.</span></span>

   <span data-ttu-id="3b1ef-145">Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-145">No code is implemented if the resource is a structured document.</span></span>

## <a name="step-4-populate-the-details-text-box"></a><span data-ttu-id="3b1ef-146">Schritt 4: Füllen Sie Textfelds "Details auf"</span><span class="sxs-lookup"><span data-stu-id="3b1ef-146">Step 4: Populate the Details text box</span></span>

- <span data-ttu-id="3b1ef-147">Erstellen Sie eine neue Unterroutine mit dem Namen `recFields` , und fügen Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="3b1ef-147">Create a new subroutine named `recFields` and insert the following code:</span></span>

   ```vb 
    
    Sub recFields(r As Record, l As ListBox, t As TextBox) 
        Dim f As Field 
        Dim s As Stream 
        Set s = New Stream 
        Dim str As String 
        
        For Each f In r.Fields 
            l.AddItem f.Name & ": " & f.Value 
        Next 
        t.Text = "" 
        If r!RESOURCE_CONTENTCLASS = "text/plain" Then 
            s.Open r, adModeRead, adOpenStreamFromRecord 
            str = s.ReadText(1) 
            s.Position = 0 
            If Asc(Mid(str, 1, 1)) = 63 Then '//63 = "?" 
                s.Charset = "ascii" 
                s.Type = adTypeText 
            End If 
            t.Text = s.ReadText(adReadAll) 
        End If 
    End Sub 
   ```

   <span data-ttu-id="3b1ef-148">Dieser Code füllt LstDetails mit den Feldern und Werten des einfachen Datensatzes an `recFields`.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-148">This code populates lstDetails with the fields and values of the simple record passed to `recFields`.</span></span> <span data-ttu-id="3b1ef-149">Wenn die Ressource eine Textdatei ist, wird von der Ressourceneintrag **ein Stream** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-149">If the resource is a text file, a text **Stream** is opened from the resource record.</span></span> <span data-ttu-id="3b1ef-150">Der Code bestimmt, ob der Zeichensatz ASCII ist, und den Inhalt des **Streams** in kopiert `txtDetails`.</span><span class="sxs-lookup"><span data-stu-id="3b1ef-150">The code determines if the character set is ASCII, and copies the **Stream** contents into `txtDetails`.</span></span>

