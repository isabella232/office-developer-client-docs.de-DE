---
title: 'Kapitel 12: RDS-Lernprogramm'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9455d7b2a9df98671f8ce6f9d8a939fcadc56f79
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936945"
---
# <a name="chapter-12-rds-tutorial"></a><span data-ttu-id="3d339-102">Kapitel 12: RDS-Lernprogramm</span><span class="sxs-lookup"><span data-stu-id="3d339-102">Chapter 12: RDS Tutorial</span></span>


<span data-ttu-id="3d339-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d339-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3d339-104">Dieses Lernprogramm zeigt, wie eine Datenquelle mit dem RDS-Programmiermodell abgefragt und aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="3d339-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="3d339-105">Zunächst werden die Schritte beschrieben, die für diese Aufgabe nötig sind.</span><span class="sxs-lookup"><span data-stu-id="3d339-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="3d339-106">Das Lernprogramm wird dann in Microsoft Visual Basic Scripting Edition und Microsoft Visual J++ mit ADO für Windows Foundation Classes (ADO/WFC) wiederholt.</span><span class="sxs-lookup"><span data-stu-id="3d339-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="3d339-107">Aus zwei Gründen enthält dieses Lernprogramm Code in verschiedenen Sprachen:</span><span class="sxs-lookup"><span data-stu-id="3d339-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="3d339-p102">Die Dokumentation für RDS setzt voraus, dass der Leser Visual Basic-Code verwendet. Dadurch eignet sich die Dokumentation besonders für Visual Basic-Programmierer, für Programmierer anderer Sprachen ist sie jedoch weniger praktisch.</span><span class="sxs-lookup"><span data-stu-id="3d339-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="3d339-110">Wenn Sie bei einem bestimmten Feature von RDS unsicher sind und gewisse Sprachkenntnisse in einer anderen Sprache haben, finden Sie vielleicht eine Lösung zu Ihrer Frage, indem Sie nach demselben Feature in einer anderen Sprache suchen.</span><span class="sxs-lookup"><span data-stu-id="3d339-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

## <a name="how-the-tutorial-is-presented"></a><span data-ttu-id="3d339-111">Wie des Lernprogramms</span><span class="sxs-lookup"><span data-stu-id="3d339-111">How the tutorial is presented</span></span>

<span data-ttu-id="3d339-p103">Dieses Lernprogramm basiert auf dem RDS-Programmiermodell. Die jeweiligen Schritte des Programmiermodells werden dabei einzeln vorgestellt. Darüber hinaus wird jeder Schritt durch einen Ausschnitt eines Visual Basic-Codes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3d339-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="3d339-p104">Das Codebeispiel wird ohne ausführliche Erläuterungen in weiteren Sprachen wiederholt. Jeder Schritt in einem Lernprogramm einer bestimmten Sprache ist mit dem entsprechenden Schritt im Programmiermodell und dem erläuternden Lernprogramm gekennzeichnet. Anhand der Schrittnummer finden Sie die Erläuterungen im Lernprogramm.</span><span class="sxs-lookup"><span data-stu-id="3d339-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="3d339-p105">Das RDS-Programmiermodell wird unten aufgeführt. Verwenden Sie es als Leitfaden, wenn Sie das Lernprogramm durchgehen.</span><span class="sxs-lookup"><span data-stu-id="3d339-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

## <a name="rds-programming-model-with-objects"></a><span data-ttu-id="3d339-120">RDS-Programmiermodell mit Objekten</span><span class="sxs-lookup"><span data-stu-id="3d339-120">RDS programming model with objects</span></span>

- <span data-ttu-id="3d339-121">Geben Sie das auf dem Server aufzurufende Programm an, und ermitteln Sie eine Möglichkeit (Proxy), vom Client darauf zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="3d339-121">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="3d339-p106">Aufrufen des Serverprogramms. Übergeben von Parametern an das Serverprogramm, die die Datenquelle und den auszugebenden Befehl identifizieren.</span><span class="sxs-lookup"><span data-stu-id="3d339-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="3d339-p107">Das Serverprogramm ruft ein [Recordset](recordset-object-ado.md)-Objekt aus der Datenquelle ab, in der Regel unter Verwendung von ADO. Das **Recordset** -Objekt kann optional auf dem Server verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="3d339-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="3d339-126">Das Serverprogramm gibt das endgültige **Recordset** -Objekt an die Clientanwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="3d339-126">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="3d339-127">Auf dem Client wird das **Recordset** -Objekt optional in eine Form gebracht, die leicht von visuellen Steuerelementen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3d339-127">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="3d339-128">Änderungen am **Recordset** -Objekt werden zurück an den Server gesendet und zur Aktualisierung der Datenquelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="3d339-128">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

<span data-ttu-id="3d339-129">Dies sind die Schritte in diesem Lernprogramm:</span><span class="sxs-lookup"><span data-stu-id="3d339-129">Following are the steps in this tutorial:</span></span>

- [<span data-ttu-id="3d339-130">Schritt 1: Angeben eines Serverprogramms</span><span class="sxs-lookup"><span data-stu-id="3d339-130">Step 1: Specify a server program</span></span>](step-1-specify-a-server-program-rds-tutorial.md)
- [<span data-ttu-id="3d339-131">Schritt 2: Aufrufen des Serverprogramms</span><span class="sxs-lookup"><span data-stu-id="3d339-131">Step 2: Invoke the server program</span></span>](step-2-invoke-the-server-program-rds-tutorial.md)
- [<span data-ttu-id="3d339-132">Schritt 3: Abrufen ein Recordset-Objekts den Server</span><span class="sxs-lookup"><span data-stu-id="3d339-132">Step 3: Server obtains a Recordset</span></span>](step-3-server-obtains-a-recordset-rds-tutorial.md)
- [<span data-ttu-id="3d339-133">Schritt 4: Server gibt das Recordset-Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3d339-133">Step 4: Server returns the Recordset</span></span>](step-4-server-returns-the-recordset-rds-tutorial.md)
- [<span data-ttu-id="3d339-134">Schritt 5: DataControl ist verwendbar vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="3d339-134">Step 5: DataControl is made usable</span></span>](step-5-datacontrol-is-made-usable-rds-tutorial.md)
- [<span data-ttu-id="3d339-135">Schritt 6: Änderungen werden an den Server gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d339-135">Step 6: Changes are sent to the server</span></span>](step-6-changes-are-sent-to-the-server-rds-tutorial.md)
- [<span data-ttu-id="3d339-136">RDS-Lernprogramm (VBScript)</span><span class="sxs-lookup"><span data-stu-id="3d339-136">RDS tutorial (VBScript)</span></span>](rds-tutorial-vbscript.md)
- [<span data-ttu-id="3d339-137">RDS-Lernprogramm (Visual J++)</span><span class="sxs-lookup"><span data-stu-id="3d339-137">RDS tutorial (Visual J++)</span></span>](rds-tutorial-visual-j.md)