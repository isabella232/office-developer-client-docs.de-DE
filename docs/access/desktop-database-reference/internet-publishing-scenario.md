---
title: Szenario für Veröffentlichungen im Internet
TOCTitle: Internet publishing scenario
ms:assetid: 25a3fa8b-86ec-9e72-5e62-bf0d849479b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249024(v=office.15)
ms:contentKeyID: 48543790
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 9a2216d41bd9d55e8b56816301350906fc2654a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594111"
---
# <a name="internet-publishing-scenario"></a>Szenario für Veröffentlichungen im Internet

**Gilt für**: Access 2013, Office 2013

Mit diesem Code wird die Verwendung von ADO (ActiveX Data Objects) mit dem Microsoft OLE DB-Anbieter für Internet Publishing veranschaulicht. In diesem Szenario erstellen Sie eine Visual Basic-Anwendung, von der mithilfe der Objekte **Recordset**, **Record** und **Stream** die Inhalte von Ressourcen angezeigt werden, die mit dem Internet Publishing-Anbieter veröffentlicht wurden.

Für die Erstellung dieses Szenarios sind die folgenden Schritte erforderlich: 

1. Richten Sie das Visual Basic Projekt ein.
2. Initialisieren Sie das Hauptlistenfeld.
3. Füllen Sie das Listenfeld Felder auf.
4. Füllen Sie das Textfeld Details auf.

## <a name="step-1-set-up-the-visual-basic-project"></a>Schritt 1: Einrichten des Visual Basic Projekts

Dieses Szenario geht davon aus, dass Sie Microsoft Visual Basic 6.0 oder höher, ADO 2.5 oder höher und den Microsoft OLE DB-Anbieter für Internet Publishing auf dem System installiert haben.

### <a name="create-an-ado-project"></a>Erstellen eines ADO-Projekts

1.  Erstellen Sie in Microsoft Visual Basic ein neues Standard EXE-Projekt.

2.  Klicken Sie im Menü **Project** auf **References**.

3.  Wählen Sie **Microsoft ActiveX Data Objects 2.5 Library** aus, und klicken Sie dann auf **OK.**

### <a name="insert-controls-on-the-main-form"></a>Einfügen von Steuerelementen im Hauptformular

1.  Add a ListBox control to Form1. Legen Sie die **Name-Eigenschaft** auf **"lstMain"** fest.

2.  Add another ListBox control to Form1. Legen Sie die **Name-Eigenschaft** auf **"lstDetails"** fest.

3.  Add a TextBox control to Form1. Legen Sie die **Name-Eigenschaft** auf **txtDetails** fest.

## <a name="step-2-initialize-the-main-list-box"></a>Schritt 2: Initialisieren des Hauptlistenfelds

### <a name="declare-global-record-and-recordset-objects"></a>Deklarieren von globalen Record- und Recordset-Objekten

- Insert the following code into the (General) (Declarations) for Form1:
    
   ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
   ```
    
   Dieser Code deklariert globale Objektverweise für die Objekte **Record** und **Recordset**, die später in diesem Szenario verwendet werden.

### <a name="connect-to-a-url-and-populate-lstmain"></a>Verbinden zu einer URL und Auffüllen von lstMain

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
    
   Dieser Code instanziiert die globalen Objekte **Record** und **Recordset**. The **Record** `grec` is opened with a URL specified as the **ActiveConnection**. Wenn die URL vorhanden ist, wird sie geöffnet. wenn es noch nicht vorhanden ist, wird es erstellt. 
   
   Beachten Sie, dass Sie eine gültige URL aus Ihrer Umgebung ersetzen `https://servername/foldername/` sollten. 
   
   Das **Recordset** `grs` wird für die untergeordneten Elemente des **Datensatzes** `grec` geöffnet. Das lstMain wird dann mit den Dateinamen der Ressourcen aufgefüllt, die unter der URL veröffentlicht wurden.

## <a name="step-3-populate-the-fields-list-box"></a>Schritt 3: Auffüllen des Listenfelds "Felder"

- Insert the following code into the Click event handler of lstMain:

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

   Dieser Code deklariert bzw. instanziiert lokale **Record-** und **Recordset-Objekte.** `rec` `rs`

   Die Zeile, die der in lstMain ausgewählten Ressource entspricht, wird zur aktuellen Zeile von `grs` . Das **Listenfeld Details** wird gelöscht und `rec` mit der aktuellen Zeile als Quelle `grs` geöffnet.

   Wenn es sich bei der Ressource um einen Auflistungsdatensatz handelt (wie durch **RecordType** angegeben), wird das lokale **Recordset** `rs` für die untergeordneten Elemente von `rec` geöffnet. lstDetails wird dann mit den Werten aus den Zeilen von `rs` gefüllt.

   Wenn die Ressource ein einfacher Datensatz `recFields` ist, wird aufgerufen. Weitere Informationen `recFields` finden Sie im nächsten Schritt.

   Ist die Ressource ein strukturiertes Dokument, wird kein Code implementiert.

## <a name="step-4-populate-the-details-text-box"></a>Schritt 4: Auffüllen des Textfelds "Details"

- Erstellen Sie eine neue Unterroutine mit dem `recFields` Namen, und fügen Sie den folgenden Code ein:

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

   Dieser Code füllt lstDetails mit den Feldern und Werten des einfachen Datensatzes auf, der an übergeben `recFields` wird. If the resource is a text file, a text **Stream** is opened from the resource record. Der Code bestimmt, ob der Zeichensatz ASCII ist, und kopiert den **Stream-Inhalt** in `txtDetails` .

