---
title: 'HelloData: Eine einfache ADO-Anwendung'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 359816f828191a8643941a21ac520ba7b3231e6b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998203"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="8ffe7-102">HelloData: Eine einfache ADO-Anwendung</span><span class="sxs-lookup"><span data-stu-id="8ffe7-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="8ffe7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ffe7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8ffe7-p101">Als Grundlage für eine Erläuterung der ADO-Bibliothek wird im Folgenden eine einfache ADO-Anwendung mit dem Namen HelloData vorgestellt. HelloData durchläuft die vier wichtigsten ADO-Vorgänge (Abrufen, Überprüfen, Bearbeiten und Aktualisieren von Daten). In dem Beispiel wird eine minimale Fehlerbehandlung ausgeführt, um die ADO-Grundlagen darzustellen und Code-Durcheinander zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="8ffe7-107">Die Anwendung fragt die Northwind-Beispieldatenbank ab, die mit Microsoft SQL Server 2000 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="8ffe7-108">**Ausführen von HelloData**</span><span class="sxs-lookup"><span data-stu-id="8ffe7-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="8ffe7-109">Erstellen Sie ein neues ausführbares Visual Basic-Standardprojekt, das auf die ADO 2.5-Bibliothek verweist.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="8ffe7-110">Erstellen Sie oben auf dem Formular vier Befehlsschaltflächen, indem Sie die Eigenschaften **Name** und **Caption** auf die Werte der folgenden Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="8ffe7-111">Fügen Sie unterhalb der Schaltflächen ein **DataGrid-Steuerelement von Microsoft** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="8ffe7-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="8ffe7-112">Die Datei Msdatgrd.ocx im Lieferumfang von Visual Basic und befindet sich Ihrer \\Windows\\system32 oder \\Winnt\\Ordner System32.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="8ffe7-113">Um Ihre Visual Basic-Bereich Toolbox DataGrid-Steuerelement hinzuzufügen, wählen Sie im Menü **Projekt** **Komponenten...** aus.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="8ffe7-114">Aktivieren Sie das Kontrollkästchen neben "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)", und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="8ffe7-115">Um das Steuerelement dem Projekt hinzuzufügen, ziehen Sie das DataGrid-Steuerelement aus der Toolbox auf das Visual Basic-Formular.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="8ffe7-p103">Erstellen Sie ein **TextBox** -Objekt auf dem Formular unterhalb des Rasters, und legen Sie seine Eigenschaften auf die in der folgenden Tabelle angegebenen Werte fest. Das Formular sollte bei seiner Fertigstellung ähnlich der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="8ffe7-118">Schließlich, kopieren Sie den Code in [HelloData-Code](hellodata-code.md) , und fügen Sie ihn in das Code-Editor-Fenster des Formulars.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="8ffe7-119">Drücken Sie **F5**, um den Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="8ffe7-p105">[!HINWEIS] Im folgenden Beispiel und im gesamten Handbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Außerdem sollten Sie den Wert "MyServer" durch den Namen Ihres Servers ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8ffe7-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="8ffe7-123">Eine ausführliche Beschreibung des Codes finden Sie unter [Informationen zu HelloData](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="8ffe7-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ffe7-124">Control Type</span><span class="sxs-lookup"><span data-stu-id="8ffe7-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="8ffe7-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8ffe7-125">Property</span></span></p></th>
<th><p><span data-ttu-id="8ffe7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8ffe7-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ffe7-127">Formular</span><span class="sxs-lookup"><span data-stu-id="8ffe7-127">Form</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-128">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-128">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-129">Form1</span><span class="sxs-lookup"><span data-stu-id="8ffe7-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-130">Height</span><span class="sxs-lookup"><span data-stu-id="8ffe7-130">Height</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-131">6500</span><span class="sxs-lookup"><span data-stu-id="8ffe7-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-132">Width</span><span class="sxs-lookup"><span data-stu-id="8ffe7-132">Width</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-133">6500</span><span class="sxs-lookup"><span data-stu-id="8ffe7-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ffe7-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="8ffe7-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-135">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-135">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="8ffe7-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ffe7-137">TextBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="8ffe7-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-138">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-138">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="8ffe7-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="8ffe7-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-141">true</span><span class="sxs-lookup"><span data-stu-id="8ffe7-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ffe7-142">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="8ffe7-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-143">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-143">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="8ffe7-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-145">Caption</span><span class="sxs-lookup"><span data-stu-id="8ffe7-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="8ffe7-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ffe7-147">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="8ffe7-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-148">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-148">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="8ffe7-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-150">Caption</span><span class="sxs-lookup"><span data-stu-id="8ffe7-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="8ffe7-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ffe7-152">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="8ffe7-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-153">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-153">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="8ffe7-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-155">Caption</span><span class="sxs-lookup"><span data-stu-id="8ffe7-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="8ffe7-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ffe7-157">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="8ffe7-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-158">Name</span><span class="sxs-lookup"><span data-stu-id="8ffe7-158">Name</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="8ffe7-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="8ffe7-160">Caption</span><span class="sxs-lookup"><span data-stu-id="8ffe7-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="8ffe7-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="8ffe7-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



