---
title: Verwendungsmöglichkeiten von ADO
TOCTitle: What You Can Do With ADO
ms:assetid: 98246cb0-aec6-6a77-c953-85895ad83a5d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249681(v=office.15)
ms:contentKeyID: 48546483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d944d70e7aba054abb7e6f02933b1311bb90ee17
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473050"
---
# <a name="what-you-can-do-with-ado"></a><span data-ttu-id="07475-102">Verwendungsmöglichkeiten von ADO</span><span class="sxs-lookup"><span data-stu-id="07475-102">What You Can Do With ADO</span></span>


<span data-ttu-id="07475-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="07475-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="07475-p101">ADO bietet Entwicklern ein leistungsfähiges, logisches Objektmodell, mit dem sie programmgesteuert eine Reihe von Datenquellen über OLE DB-Systemschnittstellen öffnen, bearbeiten und aktualisieren können. Das Abfragen einer Tabelle oder von Tabellen in einer relationalen Datenbank, das Abrufen und Anzeigen der Ergebnisse in einer Anwendung sowie vielleicht das Ändern der Daten und das Speichern dieser Änderungen durch Benutzer sind die häufigsten Verwendungsmöglichkeiten von ADO. Darüber hinaus ermöglicht ADO die folgenden programmgesteuerten Schritte:</span><span class="sxs-lookup"><span data-stu-id="07475-p101">ADO is designed to provide developers with a powerful, logical object model for programmatically accessing, editing, and updating a wide variety of data sources through OLE DB system interfaces. The most common usage of ADO is to query a table or tables in a relational database, retrieve and display the results in an application, and perhaps allow users to make and save changes to the data. Other things that can be done programmatically with ADO include:</span></span>

  - <span data-ttu-id="07475-107">Abfragen einer Datenbank mithilfe von SQL und Anzeigen der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="07475-107">Querying a database using SQL and displaying the results.</span></span>

  - <span data-ttu-id="07475-108">Zugreifen über das Internet auf Informationen in einem Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="07475-108">Accessing information in a file store over the Internet.</span></span>

  - <span data-ttu-id="07475-109">Bearbeiten von Nachrichten und Ordnern in einem E-Mail-System.</span><span class="sxs-lookup"><span data-stu-id="07475-109">Manipulating messages and folders in an e-mail system.</span></span>

  - <span data-ttu-id="07475-110">Speichern von Daten aus einer Datenbank in einer XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="07475-110">Saving data from a database into an XML file.</span></span>

  - <span data-ttu-id="07475-111">Überprüfen und Ändern von Daten in Datenbanktabellen durch Benutzer.</span><span class="sxs-lookup"><span data-stu-id="07475-111">Allowing a user to review and make changes to data in database tables.</span></span>

  - <span data-ttu-id="07475-112">Erstellen und Wiederverwenden parametrisierter Datenbankbefehle.</span><span class="sxs-lookup"><span data-stu-id="07475-112">Creating and reusing parameterized database commands.</span></span>

  - <span data-ttu-id="07475-113">Ausführen von gespeicherten Prozeduren.</span><span class="sxs-lookup"><span data-stu-id="07475-113">Executing stored procedures.</span></span>

  - <span data-ttu-id="07475-114">Dynamisches Erstellen einer flexiblen Struktur, die als **Recordset** bezeichnet wird, um Daten zu speichern und zu bearbeiten und in diesen zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="07475-114">Dynamically creating a flexible structure, called a **Recordset**, to hold, navigate, and manipulate data.</span></span>

  - <span data-ttu-id="07475-115">Ausführen transaktionaler Datenbankvorgänge.</span><span class="sxs-lookup"><span data-stu-id="07475-115">Performing transactional database operations.</span></span>

  - <span data-ttu-id="07475-116">Filtern und Sortieren lokaler Kopien der Datenbankinformationen auf Grundlage von Laufzeitkriterien.</span><span class="sxs-lookup"><span data-stu-id="07475-116">Filtering and sorting local copies of database information based on run-time criteria.</span></span>

  - <span data-ttu-id="07475-117">Erstellen und Bearbeiten hierarchischer Ergebnisse in Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="07475-117">Creating and manipulating hierarchical results from databases.</span></span>

  - <span data-ttu-id="07475-118">Binden von Datenbankfeldern an Komponenten, die Daten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="07475-118">Binding database fields to data-aware components.</span></span>

  - <span data-ttu-id="07475-119">Erstellen getrennter **Recordset** -Remoteobjekte.</span><span class="sxs-lookup"><span data-stu-id="07475-119">Creating remote, disconnected **Recordsets**.</span></span>

<span data-ttu-id="07475-p102">ADO muss zahlreiche Optionen und Einstellungen verfügbar machen, um diese Flexibilität zu bieten. Deshalb spielt es eine wichtige Rolle, dass Sie methodisch vorgehen, um sich mit den Verwendungsmöglichkeiten von ADO in einer Anwendung vertraut zu machen. Jedes Lernziel sollte dabei in überschaubare Einheiten aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="07475-p102">ADO must expose a wide variety of options and settings in order to provide such flexibility. Therefore it's important to take a methodical approach to learning how to use ADO in an application, breaking down each of your goals into manageable pieces.</span></span>

<span data-ttu-id="07475-p103">In den meisten ADO-Programmen sind vier wichtige Vorgänge beteiligt: Abrufen von Daten, Überprüfen von Daten, Bearbeiten von Daten sowie Aktualisieren von Daten. In den nächsten vier Kapiteln werden diese Vorgänge ausführlicher behandelt.</span><span class="sxs-lookup"><span data-stu-id="07475-p103">Four primary operations are involved in most ADO programs: getting data, examining data, editing data, and updating data. The next four chapters examine each of these operations in more detail.</span></span>

<span data-ttu-id="07475-p104">Bevor Sie fortfahren, sollten Sie sich mit den Objekten im ADO-Objektmodell vertraut machen. Lesen Sie anschließend das Thema [HelloData: Eine einfache ADO-Anwendung](hellodata-a-simple-ado-application.md). Diese Anwendung ist in Visual Basic geschrieben und führt alle vier wichtigen ADO-Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="07475-p104">Before proceeding, familiarize yourself with the objects in the ADO Object Model. Then review [HelloData: A Simple ADO Application](hellodata-a-simple-ado-application.md). This application is written in Visual Basic and performs each of the four primary ADO operations.</span></span>

