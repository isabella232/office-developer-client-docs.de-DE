---
title: 'HelloData: Eine einfache ADO-Anwendung'
TOCTitle: 'HelloData: A Simple ADO Application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9e70d611f351cf3ff073a1ad91e359a08e026295
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863297"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="a4e06-102">HelloData: Eine einfache ADO-Anwendung</span><span class="sxs-lookup"><span data-stu-id="a4e06-102">HelloData: A Simple ADO Application</span></span>


<span data-ttu-id="a4e06-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a4e06-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a4e06-p101">Als Grundlage für eine Erläuterung der ADO-Bibliothek wird im Folgenden eine einfache ADO-Anwendung mit dem Namen HelloData vorgestellt. HelloData durchläuft die vier wichtigsten ADO-Vorgänge (Abrufen, Überprüfen, Bearbeiten und Aktualisieren von Daten). In dem Beispiel wird eine minimale Fehlerbehandlung ausgeführt, um die ADO-Grundlagen darzustellen und Code-Durcheinander zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="a4e06-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="a4e06-107">Die Anwendung fragt die Northwind-Beispieldatenbank ab, die mit Microsoft SQL Server 2000 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="a4e06-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="a4e06-108">**Ausführen von HelloData**</span><span class="sxs-lookup"><span data-stu-id="a4e06-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="a4e06-109">Erstellen Sie ein neues ausführbares Visual Basic-Standardprojekt, das auf die ADO 2.5-Bibliothek verweist.</span><span class="sxs-lookup"><span data-stu-id="a4e06-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="a4e06-110">Erstellen Sie oben auf dem Formular vier Befehlsschaltflächen, indem Sie die Eigenschaften **Name** und **Caption** auf die Werte der folgenden Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="a4e06-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="a4e06-111">Fügen Sie unterhalb der Schaltflächen ein **DataGrid-Steuerelement von Microsoft** (Msdatgrd.ocx).</span><span class="sxs-lookup"><span data-stu-id="a4e06-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="a4e06-112">Die Datei Msdatgrd.ocx im Lieferumfang von Visual Basic und befindet sich Ihrer \\Windows\\system32 oder \\Winnt\\Ordner System32.</span><span class="sxs-lookup"><span data-stu-id="a4e06-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="a4e06-113">Um Ihre Visual Basic-Bereich Toolbox DataGrid-Steuerelement hinzuzufügen, wählen Sie im Menü **Projekt** **Komponenten...** aus.</span><span class="sxs-lookup"><span data-stu-id="a4e06-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="a4e06-114">Aktivieren Sie das Kontrollkästchen neben "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)", und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a4e06-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="a4e06-115">Um das Steuerelement dem Projekt hinzuzufügen, ziehen Sie das DataGrid-Steuerelement aus der Toolbox auf das Visual Basic-Formular.</span><span class="sxs-lookup"><span data-stu-id="a4e06-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="a4e06-p103">Erstellen Sie ein **TextBox** -Objekt auf dem Formular unterhalb des Rasters, und legen Sie seine Eigenschaften auf die in der folgenden Tabelle angegebenen Werte fest. Das Formular sollte bei seiner Fertigstellung ähnlich der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="a4e06-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="a4e06-118">Schließlich, kopieren Sie den Code in [HelloData-Code](hellodata-code.md) , und fügen Sie ihn in das Code-Editor-Fenster des Formulars.</span><span class="sxs-lookup"><span data-stu-id="a4e06-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="a4e06-119">Drücken Sie **F5**, um den Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a4e06-119">Press **F5** to run the code.</span></span>


> [!NOTE]
> <P><span data-ttu-id="a4e06-p105">[!HINWEIS] Im folgenden Beispiel und im gesamten Handbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Außerdem sollten Sie den Wert "MyServer" durch den Namen Ihres Servers ersetzen.</span><span class="sxs-lookup"><span data-stu-id="a4e06-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span></P>



<span data-ttu-id="a4e06-123">Eine ausführliche Beschreibung des Codes finden Sie unter [Informationen zu HelloData](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="a4e06-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a4e06-124">Control Type</span><span class="sxs-lookup"><span data-stu-id="a4e06-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="a4e06-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="a4e06-125">Property</span></span></p></th>
<th><p><span data-ttu-id="a4e06-126">Wert</span><span class="sxs-lookup"><span data-stu-id="a4e06-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a4e06-127">Formular</span><span class="sxs-lookup"><span data-stu-id="a4e06-127">Form</span></span></p></td>
<td><p><span data-ttu-id="a4e06-128">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-128">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-129">Form1</span><span class="sxs-lookup"><span data-stu-id="a4e06-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-130">Height</span><span class="sxs-lookup"><span data-stu-id="a4e06-130">Height</span></span></p></td>
<td><p><span data-ttu-id="a4e06-131">6500</span><span class="sxs-lookup"><span data-stu-id="a4e06-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-132">Width</span><span class="sxs-lookup"><span data-stu-id="a4e06-132">Width</span></span></p></td>
<td><p><span data-ttu-id="a4e06-133">6500</span><span class="sxs-lookup"><span data-stu-id="a4e06-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a4e06-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="a4e06-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="a4e06-135">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-135">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="a4e06-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4e06-137">TextBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="a4e06-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="a4e06-138">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-138">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="a4e06-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="a4e06-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="a4e06-141">true</span><span class="sxs-lookup"><span data-stu-id="a4e06-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4e06-142">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="a4e06-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="a4e06-143">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-143">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="a4e06-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-145">Caption</span><span class="sxs-lookup"><span data-stu-id="a4e06-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="a4e06-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="a4e06-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4e06-147">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="a4e06-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="a4e06-148">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-148">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="a4e06-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-150">Caption</span><span class="sxs-lookup"><span data-stu-id="a4e06-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="a4e06-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="a4e06-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4e06-152">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="a4e06-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="a4e06-153">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-153">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="a4e06-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-155">Caption</span><span class="sxs-lookup"><span data-stu-id="a4e06-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="a4e06-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="a4e06-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a4e06-157">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="a4e06-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="a4e06-158">Name</span><span class="sxs-lookup"><span data-stu-id="a4e06-158">Name</span></span></p></td>
<td><p><span data-ttu-id="a4e06-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="a4e06-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="a4e06-160">Caption</span><span class="sxs-lookup"><span data-stu-id="a4e06-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="a4e06-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="a4e06-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



