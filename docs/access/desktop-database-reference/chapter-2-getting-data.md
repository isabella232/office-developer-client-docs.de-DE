---
title: 'Kapitel 2: Abrufen von Daten'
TOCTitle: 'Chapter 2: Getting Data'
ms:assetid: 72d097e1-9284-cc27-fd48-e6bbb6a2a543
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249465(v=office.15)
ms:contentKeyID: 48545619
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4d3df907e1dbe220caab58541b7c3eba605ef2f3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474624"
---
# <a name="chapter-2-getting-data"></a><span data-ttu-id="b0992-102">Kapitel 2: Abrufen von Daten</span><span class="sxs-lookup"><span data-stu-id="b0992-102">Chapter 2: Getting Data</span></span>


<span data-ttu-id="b0992-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0992-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b0992-p101">Im vorangegangenen Kapitel wurden vier wichtige Vorgänge zum Erstellen einer ADO-Anwendung vorgestellt: Abrufen von Daten, Überprüfen von Daten, Bearbeiten von Daten sowie Aktualisieren von Daten. Dieses Kapitel befasst sich mit den Konzepten im Zusammenhang mit dem ersten Vorgang, also dem Abrufen von Daten.</span><span class="sxs-lookup"><span data-stu-id="b0992-p101">The preceding chapter introduced four primary operations involved in creating an ADO application: getting data, examining data, editing data, and updating data. This chapter will focus on the details of the concepts relevant to the first operation: getting data.</span></span>

<span data-ttu-id="b0992-p102">Mehrere ADO-Objekte können bei diesem Vorgang eine Rolle spielen. Zunächst stellen Sie mithilfe eines **Connection** -Objekts von ADO (das manchmal impliziert erstellt wird) eine Verbindung mit der Datenquelle her. Danach übergeben Sie mit einem **Command** -Objekt von ADO (das auch implizit erstellt werden kann) Anweisungen an die Datenquelle, welche Schritte ausgeführt werden sollen. Das Ergebnis des Übergebens eines Befehls an eine Datenquelle und das Empfangen der Antwort wird gewöhnlich in einem **Recordset** -Objekt von ADO dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b0992-p102">Several ADO objects can play a role in this operation. First you connect to the data source using an ADO **Connection** object (which at times will be created implicitly). Then you pass instructions to the data source about what you want to do using an ADO **Command** object (which also can be created implicitly). The result of passing a command to a data source and receiving its response usually will be represented in an ADO **Recordset** object.</span></span>

<span data-ttu-id="b0992-110">Ihre Anwendung muss zum Abrufen von Daten in Verbindung mit einer Datenquelle, wie ein DBMS, einem Dateispeicher oder einer durch Trennzeichen getrennten Textdatei.</span><span class="sxs-lookup"><span data-stu-id="b0992-110">To get data, your application must be in communication with a data source, such as a DBMS, a file store, or a comma-delimited text file.</span></span> <span data-ttu-id="b0992-111">Diese Kommunikation stellt eine *Verbindung* – die erforderliche Umgebung für den Austausch von Daten.</span><span class="sxs-lookup"><span data-stu-id="b0992-111">This communication represents a *connection* — the environment necessary for exchanging data.</span></span>

<span data-ttu-id="b0992-p104">Das ADO-Objektmodell stellt das Konzept einer Verbindung mit dem **Connection** -Objekt dar, also die Grundlage, auf der ein Großteil der ADO-Funktionalität basiert. Ein **Connection** -Objekt hat folgenden Zweck:</span><span class="sxs-lookup"><span data-stu-id="b0992-p104">The ADO object model represents the concept of a connection with the **Connection** object — the foundation upon which much ADO functionality is built. The purpose of a **Connection** object is to:</span></span>

  - <span data-ttu-id="b0992-114">Definieren der Informationen, die ADO zum Kommunizieren mit Datenquellen und zum Erstellen von Sitzungen benötigt.</span><span class="sxs-lookup"><span data-stu-id="b0992-114">Define the information ADO needs to communicate with data sources and create sessions.</span></span>

  - <span data-ttu-id="b0992-115">Definieren der Transaktionsfunktionen der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b0992-115">Define the transactional capabilities of the session.</span></span>

  - <span data-ttu-id="b0992-116">Ermöglichen des Erstellens und Ausführens von Befehlen für die Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="b0992-116">Allow you to create and execute commands against the data source.</span></span>

  - <span data-ttu-id="b0992-p105">Bereitstellen von Informationen zum Entwurf der zugrunde liegenden Datenquelle in Form von Schemarowsets. Weitere Informationen zu Schemarowsets finden Sie unter [OpenSchema-Methode](openschema-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="b0992-p105">Provide information about the design of the underlying data source in the form of schema rowsets. For more information about schema rowsets, see [OpenSchema Method](openschema-method-ado.md).</span></span>

