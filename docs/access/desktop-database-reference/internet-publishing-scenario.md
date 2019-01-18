---
title: Szenario für Veröffentlichungen im Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0f28b14f3eaf6792a74ef0967d698d5a3914955a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708508"
---
# <a name="internet-publishing-scenario"></a>Szenario für Veröffentlichungen im Internet

**Betrifft**: Access 2013, Office 2013

Mit diesem Code wird die Verwendung von ADO (ActiveX Data Objects) mit dem Microsoft OLE DB-Anbieter für Internet Publishing veranschaulicht. In diesem Szenario erstellen Sie eine Visual Basic-Anwendung, von der mithilfe der Objekte **Recordset**, **Record** und **Stream** die Inhalte von Ressourcen angezeigt werden, die mit dem Internet Publishing-Anbieter veröffentlicht wurden.

Für die Erstellung dieses Szenarios sind die folgenden Schritte erforderlich: 

1. Richten Sie das Visual Basic-Projekt.
2. Initialisieren Sie das Listenfeld Main.
3. Füllen Sie die Listenfelds "Fields" auf.
4. Füllen Sie das Textfeld "Details" auf.

## <a name="step-1-set-up-the-visual-basic-project"></a>Schritt 1: Einrichten des Visual Basic-Projekts

Dieses Szenario geht davon aus, dass Sie Microsoft Visual Basic 6.0 oder höher, ADO 2.5 oder höher und den Microsoft OLE DB-Anbieter für Internet Publishing auf dem System installiert haben.

### <a name="create-an-ado-project"></a>Erstellen Sie ein ADO-Projekt

1.  Erstellen Sie in Microsoft Visual Basic ein neues Standard EXE-Projekt.

2.  Klicken Sie im Menü **Project** auf **References**.

3.  Wählen Sie **Microsoft ActiveX Data Objects 2.5 Library**aus, und klicken Sie dann auf **OK**.

### <a name="insert-controls-on-the-main-form"></a>Fügen Sie Steuerelemente im Hauptformular

1.  Fügen Sie ein ListBox-Steuerelement zu Form1 hinzu. Legen Sie die **Name** -Eigenschaft auf **IstMain**.

2.  Fügen Sie ein anderes ListBox-Steuerelement zu Form1 hinzu. Legen Sie die **Name** -Eigenschaft auf **LstDetails**.

3.  Fügen Sie ein TextBox-Steuerelement zu Form1 hinzu. Legen Sie die **Name** -Eigenschaft auf **TxtDetails**.

## <a name="step-2-initialize-the-main-list-box"></a>Schritt 2: Initialisieren des Main-Listenfelds

### <a name="declare-global-record-and-recordset-objects"></a>Deklarieren Sie globale Objekte Record und Recordset

- Fügen Sie den folgenden Code in (General) (Declarations) für Form1 ein:

    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Dieser Code deklariert globale Objektverweise für die Objekte **Record** und **Recordset**, die später in diesem Szenario verwendet werden.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Verbinden mit einer URL und Auffüllen von IstMain

- Fügen Sie im Form Load-Ereignishandler für Form1 den folgenden Code ein:
    
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
    
   Dieser Code instanziiert die globalen Objekte **Record** und **Recordset**. Der **Eintrag** `grec` mit einer URL angegeben als **ActiveConnection**geöffnet wird. Wenn die URL vorhanden ist, wird sie geöffnet. Wenn er nicht bereits vorhanden ist, wird sie erstellt. 
   
   Notiz, die Sie ersetzen soll `https://servername/foldername/` durch eine gültige URL aus der Umgebung. 
   
   Das **Recordset-Objekt** `grs` wird geöffnet, auf die untergeordneten Elemente des **Datensatzes** `grec`. Die IstMain wird dann mit den Dateinamen der URL veröffentlichten Ressourcen aufgefüllt.

## <a name="step-3-populate-the-fields-list-box"></a>Schritt 3: Füllen Sie Listenfelds "Fields auf"

- Fügen Sie im Click-Ereignishandler von IstMain den folgenden Code ein:

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

   Dieser Code deklariert und instanziiert die lokalen **Record** und **Recordset** -Objekte `rec` und `rs`fest.

   Die Zeile, die in LstMain ausgewählten Ressource entspricht, erfolgt die aktuelle Zeile des `grs`. Das Listenfeld **Details** wird anschließend gelöscht und `rec` wird geöffnet, mit der aktuellen Zeile des `grs` als Quelle.

   Wenn die Ressource einen Auflistungsdatensatz handelt (wie durch **RecordType**angegeben), das lokale **Recordset** `rs` wird geöffnet, auf die untergeordneten Elemente des `rec`. wird mit den Werten aus den Zeilen LstDetails gefüllt `rs`.

   Wenn die Ressource ein einfacher Datensatz, `recFields` aufgerufen wird. Weitere Informationen zu `recFields`, finden Sie im nächsten Schritt.

   Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.

## <a name="step-4-populate-the-details-text-box"></a>Schritt 4: Füllen Sie Textfelds "Details auf"

- Erstellen Sie eine neue Unterroutine mit dem Namen `recFields` , und fügen Sie den folgenden Code:

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

   Dieser Code füllt LstDetails mit den Feldern und Werten des einfachen Datensatzes an `recFields`. Wenn die Ressource eine Textdatei ist, wird von der Ressourceneintrag **ein Stream** geöffnet. Der Code bestimmt, ob der Zeichensatz ASCII ist, und den Inhalt des **Streams** in kopiert `txtDetails`.

