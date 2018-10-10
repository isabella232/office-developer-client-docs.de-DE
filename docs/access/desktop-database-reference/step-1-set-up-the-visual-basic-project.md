---
title: 'Schritt 1: Einrichten des Visual Basic-Projekts'
TOCTitle: 'Step 1: Set Up the Visual Basic Project'
ms:assetid: 1b8195c9-60c8-18a2-3fa2-ffdeed370748
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248954(v=office.15)
ms:contentKeyID: 48543544
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f608d0dadb44a6ddea7a60123d2d6950bc9627cb
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473514"
---
# <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="210c3-102">Schritt 1: Einrichten des Visual Basic-Projekts</span><span class="sxs-lookup"><span data-stu-id="210c3-102">Step 1: Set Up the Visual Basic Project</span></span>


<span data-ttu-id="210c3-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="210c3-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-1-set-up-the-visual-basic-project"></a><span data-ttu-id="210c3-104">Schritt 1: Einrichten des Visual Basic-Projekts</span><span class="sxs-lookup"><span data-stu-id="210c3-104">Step 1: Set Up the Visual Basic Project</span></span>

<span data-ttu-id="210c3-105">Dieses Szenario geht davon aus, dass Sie Microsoft Visual Basic 6.0 oder höher, ADO 2.5 oder höher und den Microsoft OLE DB-Anbieter für Internet Publishing auf dem System installiert haben.</span><span class="sxs-lookup"><span data-stu-id="210c3-105">In this scenario, it is assumed that you have Microsoft Visual Basic 6.0 or later, ADO 2.5 or later, and the Microsoft OLE DB Provider for Internet Publishing installed on your system.</span></span>

<span data-ttu-id="210c3-106">**So erstellen Sie ein ADO-Projekt**</span><span class="sxs-lookup"><span data-stu-id="210c3-106">**To create an ADO project**</span></span>

1.  <span data-ttu-id="210c3-107">Erstellen Sie in Microsoft Visual Basic ein neues Standard EXE-Projekt.</span><span class="sxs-lookup"><span data-stu-id="210c3-107">In Microsoft Visual Basic, create a new Standard EXE project.</span></span>

2.  <span data-ttu-id="210c3-108">Klicken Sie im Menü **Project** auf **References**.</span><span class="sxs-lookup"><span data-stu-id="210c3-108">From the **Project** menu, choose **References**.</span></span>

3.  <span data-ttu-id="210c3-109">Wählen Sie **Microsoft ActiveX Data Objects 2.5 Library** aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="210c3-109">Select **"Microsoft ActiveX Data Objects 2.5 Library**" and click **OK**.</span></span>

<span data-ttu-id="210c3-110">**So fügen Sie Steuerelemente im Hauptformular ein**</span><span class="sxs-lookup"><span data-stu-id="210c3-110">**To insert controls on the main form**</span></span>

1.  <span data-ttu-id="210c3-p101">Fügen Sie Form1 ein ListBox-Steuerelement hinzu. Legen Sie seine Name-Eigenschaft auf IstMain fest.</span><span class="sxs-lookup"><span data-stu-id="210c3-p101">Add a ListBox control to Form1. Set its **Name** property to lstMain.</span></span>

2.  <span data-ttu-id="210c3-p102">Fügen Sie Form1 ein weiteres ListBox-Steuerelement hinzu. Legen Sie seine Name-Eigenschaft auf IstDetails fest.</span><span class="sxs-lookup"><span data-stu-id="210c3-p102">Add another ListBox control to Form1. Set its **Name** property to lstDetails.</span></span>

3.  <span data-ttu-id="210c3-p103">Fügen Sie Form1 ein TextBox-Steuerelement hinzu. Legen Sie seine Name-Eigenschaft auf IstDetails fest.</span><span class="sxs-lookup"><span data-stu-id="210c3-p103">Add a TextBox control to Form1. Set its **Name** property to txtDetails.</span></span>

