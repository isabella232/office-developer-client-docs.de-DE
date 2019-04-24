---
title: 'HelloData: Eine einfache ADO-Anwendung'
TOCTitle: 'HelloData: A simple ADO application'
ms:assetid: c271abeb-8865-81f9-db8e-47d3db87ad30
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249950(v=office.15)
ms:contentKeyID: 48547554
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3c7d9be9b91b3f847516eb3c22aa37e46c8a551d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292020"
---
# <a name="hellodata-a-simple-ado-application"></a><span data-ttu-id="2f613-102">HelloData: Eine einfache ADO-Anwendung</span><span class="sxs-lookup"><span data-stu-id="2f613-102">HelloData: A simple ADO application</span></span>

<span data-ttu-id="2f613-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f613-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2f613-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span><span class="sxs-lookup"><span data-stu-id="2f613-p101">To lay the groundwork for an exploration of the ADO library, consider a simple ADO application called "HelloData." HelloData steps through each of the four major ADO operations (getting, examining, editing, and updating data). In order to focus on the fundamentals of ADO and prevent code clutter, minimal error handling is done in the example.</span></span>

<span data-ttu-id="2f613-107">Die Anwendung fragt die Northwind-Beispieldatenbank ab, die mit Microsoft SQL Server 2000 ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="2f613-107">The application queries the Northwind sample database that is included with Microsoft SQL Server 2000.</span></span>

<span data-ttu-id="2f613-108">**Ausführen von HelloData**</span><span class="sxs-lookup"><span data-stu-id="2f613-108">**To run HelloData**</span></span>

1.  <span data-ttu-id="2f613-109">Erstellen Sie ein neues ausführbares Visual Basic-Standardprojekt, das auf die ADO 2.5-Bibliothek verweist.</span><span class="sxs-lookup"><span data-stu-id="2f613-109">Create a new Standard Executable Visual Basic Project that references the ADO 2.5 library.</span></span>

2.  <span data-ttu-id="2f613-110">Erstellen Sie oben auf dem Formular vier Befehlsschaltflächen, indem Sie die Eigenschaften **Name** und **Caption** auf die Werte der folgenden Tabelle festlegen.</span><span class="sxs-lookup"><span data-stu-id="2f613-110">Create four command buttons at the top of the form, setting the **Name** and **Caption** properties to the values shown in the table below.</span></span>

3.  <span data-ttu-id="2f613-111">Fügen Sie unterhalb der Schaltflächen ein **Microsoft DataGrid-Steuerelement** (msdatgrd. ocx) hinzu.</span><span class="sxs-lookup"><span data-stu-id="2f613-111">Below the buttons, add a **Microsoft DataGrid Control** (Msdatgrd.ocx).</span></span> <span data-ttu-id="2f613-112">Die Datei msdatgrd. ocx wird mit Visual Basic geliefert und befindet sich in \\Ihrem\\Windows System32 \\-\\oder winnt system32-Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="2f613-112">The Msdatgrd.ocx file comes with Visual Basic and is located in your \\windows\\system32 or \\winnt\\system32 directory.</span></span> <span data-ttu-id="2f613-113">Zum Hinzufügen des DataGrid-Steuerelements zum Visual Basic-Toolboxbereich wählen Sie im Menü **Projekt** die Option Components.. **.** aus.</span><span class="sxs-lookup"><span data-stu-id="2f613-113">To add the DataGrid control to your Visual Basic toolbox pane, select **Components...** from the **Project** menu.</span></span> <span data-ttu-id="2f613-114">Aktivieren Sie dann das Kontrollkästchen neben "Microsoft DataGrid-Steuerelement 6,0 (SP3) (OLEDB)", und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2f613-114">Then check the box next to "Microsoft DataGrid Control 6.0 (SP3) (OLEDB)" and click **OK**.</span></span> <span data-ttu-id="2f613-115">Um dem Projekt das Steuerelement hinzuzufügen, ziehen Sie das DataGrid-Steuerelement aus der Toolbox in das Visual Basic-Formular.</span><span class="sxs-lookup"><span data-stu-id="2f613-115">To add the control to the project, drag the DataGrid control from the Toolbox to the Visual Basic form.</span></span>

4.  <span data-ttu-id="2f613-p103">Erstellen Sie ein **TextBox** -Objekt auf dem Formular unterhalb des Rasters, und legen Sie seine Eigenschaften auf die in der folgenden Tabelle angegebenen Werte fest. Das Formular sollte bei seiner Fertigstellung ähnlich der folgenden Abbildung aussehen.</span><span class="sxs-lookup"><span data-stu-id="2f613-p103">Create a **TextBox** on the form below the grid and set its properties as shown in the table. The form should look similar to the following figure when you are finished.</span></span>

5.  <span data-ttu-id="2f613-118">Kopieren Sie schließlich den im HelloData- [Code](hellodata-code.md) aufgeführten Code, und fügen Sie ihn in das Code-Editor-Fenster des Formulars ein.</span><span class="sxs-lookup"><span data-stu-id="2f613-118">Finally, copy the code listed in [HelloData Code](hellodata-code.md) and paste it into the code editor window of the form.</span></span> <span data-ttu-id="2f613-119">Drücken Sie **F5**, um den Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2f613-119">Press **F5** to run the code.</span></span>

> [!NOTE]
> <span data-ttu-id="2f613-p105">[!HINWEIS] Im folgenden Beispiel und im gesamten Handbuch werden die Benutzer-ID "MyId" und das Kennwort "123aBc" zum Authentifizieren am Server verwendet. Sie sollten diese Werte durch gültige Anmeldeinformationen für Ihren Server ersetzen. Außerdem sollten Sie den Wert "MyServer" durch den Namen Ihres Servers ersetzen.</span><span class="sxs-lookup"><span data-stu-id="2f613-p105">In the following example, and throughout the guide, the user id "MyId" with a password of "123aBc" is used to authenticate against the server. You should substitute these values with valid logon credentials for your server. Also, substitute the "MyServer" value with the name of your server.</span></span>

<span data-ttu-id="2f613-123">Eine ausführliche Beschreibung des Codes finden Sie unter [HelloData Details](hellodata-details.md).</span><span class="sxs-lookup"><span data-stu-id="2f613-123">For a detailed description of the code, see [HelloData Details](hellodata-details.md).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f613-124">Control Type</span><span class="sxs-lookup"><span data-stu-id="2f613-124">Control Type</span></span></p></th>
<th><p><span data-ttu-id="2f613-125">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2f613-125">Property</span></span></p></th>
<th><p><span data-ttu-id="2f613-126">Wert</span><span class="sxs-lookup"><span data-stu-id="2f613-126">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f613-127">Formular</span><span class="sxs-lookup"><span data-stu-id="2f613-127">Form</span></span></p></td>
<td><p><span data-ttu-id="2f613-128">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-128">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-129">Form1</span><span class="sxs-lookup"><span data-stu-id="2f613-129">Form1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-130">Height</span><span class="sxs-lookup"><span data-stu-id="2f613-130">Height</span></span></p></td>
<td><p><span data-ttu-id="2f613-131">6500</span><span class="sxs-lookup"><span data-stu-id="2f613-131">6500</span></span></p></td>
</tr>
<tr class="odd">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-132">Width</span><span class="sxs-lookup"><span data-stu-id="2f613-132">Width</span></span></p></td>
<td><p><span data-ttu-id="2f613-133">6500</span><span class="sxs-lookup"><span data-stu-id="2f613-133">6500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f613-134">MS DataGrid</span><span class="sxs-lookup"><span data-stu-id="2f613-134">MS DataGrid</span></span></p></td>
<td><p><span data-ttu-id="2f613-135">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-135">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-136">grdDisplay1</span><span class="sxs-lookup"><span data-stu-id="2f613-136">grdDisplay1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f613-137">TextBox</span><span class="sxs-lookup"><span data-stu-id="2f613-137">TextBox</span></span></p></td>
<td><p><span data-ttu-id="2f613-138">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-138">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-139">txtDisplay1</span><span class="sxs-lookup"><span data-stu-id="2f613-139">txtDisplay1</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-140">Multiline</span><span class="sxs-lookup"><span data-stu-id="2f613-140">Multiline</span></span></p></td>
<td><p><span data-ttu-id="2f613-141">true</span><span class="sxs-lookup"><span data-stu-id="2f613-141">true</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f613-142">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="2f613-142">Command Button</span></span></p></td>
<td><p><span data-ttu-id="2f613-143">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-143">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-144">cmdGetData</span><span class="sxs-lookup"><span data-stu-id="2f613-144">cmdGetData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-145">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="2f613-145">Caption</span></span></p></td>
<td><p><span data-ttu-id="2f613-146">Get Data</span><span class="sxs-lookup"><span data-stu-id="2f613-146">Get Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f613-147">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="2f613-147">Command Button</span></span></p></td>
<td><p><span data-ttu-id="2f613-148">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-148">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-149">cmdExamineData</span><span class="sxs-lookup"><span data-stu-id="2f613-149">cmdExamineData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-150">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="2f613-150">Caption</span></span></p></td>
<td><p><span data-ttu-id="2f613-151">Examine Data</span><span class="sxs-lookup"><span data-stu-id="2f613-151">Examine Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f613-152">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="2f613-152">Command Button</span></span></p></td>
<td><p><span data-ttu-id="2f613-153">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-153">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-154">cmdEditData</span><span class="sxs-lookup"><span data-stu-id="2f613-154">cmdEditData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-155">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="2f613-155">Caption</span></span></p></td>
<td><p><span data-ttu-id="2f613-156">Edit Data</span><span class="sxs-lookup"><span data-stu-id="2f613-156">Edit Data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2f613-157">Befehlsschaltfläche</span><span class="sxs-lookup"><span data-stu-id="2f613-157">Command Button</span></span></p></td>
<td><p><span data-ttu-id="2f613-158">Name</span><span class="sxs-lookup"><span data-stu-id="2f613-158">Name</span></span></p></td>
<td><p><span data-ttu-id="2f613-159">cmdUpdateData</span><span class="sxs-lookup"><span data-stu-id="2f613-159">cmdUpdateData</span></span></p></td>
</tr>
<tr class="even">
<td><p><br />
</p></td>
<td><p><span data-ttu-id="2f613-160">Beschriftung</span><span class="sxs-lookup"><span data-stu-id="2f613-160">Caption</span></span></p></td>
<td><p><span data-ttu-id="2f613-161">Update Data</span><span class="sxs-lookup"><span data-stu-id="2f613-161">Update Data</span></span></p></td>
</tr>
</tbody>
</table>



