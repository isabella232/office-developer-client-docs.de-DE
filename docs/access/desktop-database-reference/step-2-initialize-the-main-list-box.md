---
title: 'Schritt 2: Initialisieren des Hauptlistenfelds'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475071"
---
# <a name="step-2-initialize-the-main-list-box"></a>Schritt 2: Initialisieren des Hauptlistenfelds


**Betrifft**: Access 2013 | Office 2013

## <a name="step-2-initialize-the-main-list-box"></a>Schritt 2: Initialisieren des Hauptlistenfelds

**So deklarieren Sie globale Objekte Record und Recordset**

  - Fügen Sie den folgenden Code in (General) (Declarations) für Form1 ein:

    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    Dieser Code deklariert globale Objektverweise für die Objekte **Record** und **Recordset**, die später in diesem Szenario verwendet werden.

**Herstellen einer Verbindung mit einer URL und Auffüllen von IstMain**

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
    
    Dieser Code instanziiert die globalen Objekte **Record** und **Recordset**. Der **Datensatz**, Grec, wird mit einer URL angegeben als **ActiveConnection**geöffnet. Wenn die URL vorhanden ist, wird sie geöffnet. Wenn er nicht bereits vorhanden ist, wird sie erstellt. Notiz, die Sie ersetzen soll "https://servername/foldername/" durch eine gültige URL aus der Umgebung. Öffnen des **Recordset-Objekts**, Grs, ist für die untergeordneten Elemente des **Datensatzes**, Grec. Dann wird mit den Dateinamen der Ressourcen auf die URL veröffentlicht IstMain aufgefüllt.

