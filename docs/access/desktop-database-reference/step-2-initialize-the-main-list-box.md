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
# <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="363fb-102">Schritt 2: Initialisieren des Hauptlistenfelds</span><span class="sxs-lookup"><span data-stu-id="363fb-102">Step 2: Initialize the Main List Box</span></span>


<span data-ttu-id="363fb-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="363fb-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="363fb-104">Schritt 2: Initialisieren des Hauptlistenfelds</span><span class="sxs-lookup"><span data-stu-id="363fb-104">Step 2: Initialize the Main List Box</span></span>

<span data-ttu-id="363fb-105">**So deklarieren Sie globale Objekte Record und Recordset**</span><span class="sxs-lookup"><span data-stu-id="363fb-105">**To declare global Record and Recordset objects**</span></span>

  - <span data-ttu-id="363fb-106">Fügen Sie den folgenden Code in (General) (Declarations) für Form1 ein:
</span><span class="sxs-lookup"><span data-stu-id="363fb-106">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    <span data-ttu-id="363fb-107">Dieser Code deklariert globale Objektverweise für die Objekte **Record** und **Recordset**, die später in diesem Szenario verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="363fb-107">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

<span data-ttu-id="363fb-108">**Herstellen einer Verbindung mit einer URL und Auffüllen von IstMain**</span><span class="sxs-lookup"><span data-stu-id="363fb-108">**To connect to a URL and populate lstMain**</span></span>

  - <span data-ttu-id="363fb-109">Fügen Sie im Form Load-Ereignishandler für Form1 den folgenden Code ein:</span><span class="sxs-lookup"><span data-stu-id="363fb-109">Insert the following code into the Form Load event handler for Form1:</span></span>
    
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
    
    <span data-ttu-id="363fb-110">Dieser Code instanziiert die globalen Objekte **Record** und **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="363fb-110">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="363fb-111">Der **Datensatz**, Grec, wird mit einer URL angegeben als **ActiveConnection**geöffnet.</span><span class="sxs-lookup"><span data-stu-id="363fb-111">The **Record**, grec, is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="363fb-112">Wenn die URL vorhanden ist, wird sie geöffnet. Wenn er nicht bereits vorhanden ist, wird sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="363fb-112">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> <span data-ttu-id="363fb-113">Notiz, die Sie ersetzen soll "https://servername/foldername/" durch eine gültige URL aus der Umgebung.</span><span class="sxs-lookup"><span data-stu-id="363fb-113">Note that you should replace "https://servername/foldername/" with a valid URL from your environment.</span></span> <span data-ttu-id="363fb-114">Öffnen des **Recordset-Objekts**, Grs, ist für die untergeordneten Elemente des **Datensatzes**, Grec.</span><span class="sxs-lookup"><span data-stu-id="363fb-114">The **Recordset**, grs, is opened on the children of the **Record**, grec.</span></span> <span data-ttu-id="363fb-115">Dann wird mit den Dateinamen der Ressourcen auf die URL veröffentlicht IstMain aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="363fb-115">Then lstMain is populated with the file names of the resources published to the URL.</span></span>

