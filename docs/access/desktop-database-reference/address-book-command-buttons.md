---
title: Befehlsschaltflächen des Adressbuchs
TOCTitle: Address Book Command Buttons
ms:assetid: bcea6f53-3e36-b067-03c2-b157ed02d41d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249908(v=office.15)
ms:contentKeyID: 48547422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15a79db455032ddf2eb9fa0d9555d8f7a4959313
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475846"
---
# <a name="address-book-command-buttons"></a><span data-ttu-id="77e7a-102">Befehlsschaltflächen des Adressbuchs</span><span class="sxs-lookup"><span data-stu-id="77e7a-102">Address Book Command Buttons</span></span>


<span data-ttu-id="77e7a-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="77e7a-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="77e7a-104">Die Adressbuchanwendung bietet die folgenden Befehlsschaltflächen:</span><span class="sxs-lookup"><span data-stu-id="77e7a-104">The Address Book application includes the following command buttons:</span></span>

  - <span data-ttu-id="77e7a-105">Eine Schaltfläche Find, um eine Abfrage an die Datenbank abzusenden.</span><span class="sxs-lookup"><span data-stu-id="77e7a-105">A Find button to submit a query to the database.</span></span>

  - <span data-ttu-id="77e7a-106">Eine Schaltfläche **Clear**, um die Inhalte aus den Textfelder zu löschen, bevor eine neue Suche gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="77e7a-106">A **Clear** button to clear the text boxes before starting a new search.</span></span>

  - <span data-ttu-id="77e7a-107">Eine Schaltfläche Update Profile, um die Änderungen an einem Mitarbeiterdatensatz zu ändern.</span><span class="sxs-lookup"><span data-stu-id="77e7a-107">An Update Profile button to save changes to an employee record.</span></span>

  - <span data-ttu-id="77e7a-108">Eine Schaltfläche Cancel Changes, um Änderungen zu verwerfen.</span><span class="sxs-lookup"><span data-stu-id="77e7a-108">A Cancel Changes button to discard changes.</span></span>

## <a name="find-button"></a><span data-ttu-id="77e7a-109">Find (Schaltfläche)</span><span class="sxs-lookup"><span data-stu-id="77e7a-109">Find Button</span></span>

<span data-ttu-id="77e7a-110">Durch Klicken auf die Schaltfläche **Suchen** VBScript suchen aktiviert\_OnClick Sub-Prozedur, die die SQL-Abfrage erstellt und gesendet.</span><span class="sxs-lookup"><span data-stu-id="77e7a-110">Clicking the **Find** button activates the VBScript Find\_OnClick Sub procedure, which builds and sends the SQL query.</span></span> <span data-ttu-id="77e7a-111">Auf diese Schaltfläche klicken, wird das Datenraster aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="77e7a-111">Clicking this button populates the data grid.</span></span>

## <a name="building-the-sql-query"></a><span data-ttu-id="77e7a-112">Erstellen der SQL-Abfrage</span><span class="sxs-lookup"><span data-stu-id="77e7a-112">Building the SQL Query</span></span>

<span data-ttu-id="77e7a-113">Der erste Teil der Suche\_OnClick Sub-Prozedur erstellt die SQL-Abfrage einem Begriff zu einem Zeitpunkt durch Anfügen von Zeichenfolgen, die an eine globale SQL SELECT-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="77e7a-113">The first part of the Find\_OnClick Sub procedure builds the SQL query, one phrase at a time, by appending text strings to a global SQL SELECT statement.</span></span> <span data-ttu-id="77e7a-114">Zunächst wird die Variable auf einer SQL SELECT-Anweisung, die alle Zeilen der Daten aus der Datenquellentabelle anfordert.</span><span class="sxs-lookup"><span data-stu-id="77e7a-114">It begins by setting the variable to a SQL SELECT statement that requests all rows of data from the data source table.</span></span> <span data-ttu-id="77e7a-115">Im nächsten Schritt überprüft der Unterprozedur jede der vier input Felder auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="77e7a-115">Next, the Sub procedure scans each of the four input boxes on the page.</span></span>

<span data-ttu-id="77e7a-116">Da das Programm das Wort im Erstellen der SQL-Anweisungen verwendet, stellen die Abfragen Suchvorgänge nach Teilzeichenfolgen dar und nicht als nach genauen Übereinstimmungen.</span><span class="sxs-lookup"><span data-stu-id="77e7a-116">Because the program uses the word in building the SQL statements, the queries are substring searches rather than exact matches.</span></span>

<span data-ttu-id="77e7a-117">Wenn das Feld **Nachname** den Eintrag "Berge" enthalten, und das Feld **Titel** den Eintrag "Programmmanager" enthalten, würde beispielsweise die SQL-Anweisung (Wert) lauten:</span><span class="sxs-lookup"><span data-stu-id="77e7a-117">For example, if the **Last Name** box contained the entry "Berge" and the **Title** box contained the entry "Program Manager", the SQL statement (value of ) would read:</span></span>

```vb 
 
Select FirstName, LastName, Title, Email, Building, Room, Phone from Employee where lastname like 'Berge%' and title like 'Program Manager%' 
```

<span data-ttu-id="77e7a-118">War die Abfrage erfolgreich, werden alle Personen, deren Nachnamen den Text Berge (z. B. Berge und Berger) und deren Positionsbezeichnung die Wörter Program Manager (z. B. Program Manager, Advanced Technologies) enthalten, im HTML-Datenraster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77e7a-118">If the query was successful, all persons with a last name containing the text "Berge" (such as Berge and Berger) and with a title containing the words "Program Manager" (for example, Program Manager, Advanced Technologies) are displayed in the HTML data grid.</span></span>

## <a name="preparing-and-sending-the-query"></a><span data-ttu-id="77e7a-119">Vorbereiten und Senden der Abfrage</span><span class="sxs-lookup"><span data-stu-id="77e7a-119">Preparing and Sending the Query</span></span>

<span data-ttu-id="77e7a-120">Den letzten Teil der Suche\_OnClick Sub-Prozedur besteht aus zwei Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="77e7a-120">The last part of the Find\_OnClick Sub procedure consists of two statements.</span></span> <span data-ttu-id="77e7a-121">Der ersten Anweisung wird die SQL-Eigenschaft des RDS.DataControl-Objekt ist gleich der dynamisch erstellte SQL-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="77e7a-121">The first statement assigns the SQL property of the RDS.DataControl object equal to the dynamically built SQL query.</span></span> <span data-ttu-id="77e7a-122">Die zweite Anweisung bewirkt, dass die **RDS.DataControl** -Objekts (), um die Datenbank Abfragen, und klicken Sie dann die Ergebnisse der Abfrage im Raster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="77e7a-122">The second statement causes the **RDS.DataControl** object () to query the database, and then display the new results of the query in the grid.</span></span>

```vb 
 
Sub Find_OnClick 
 '... 
 DC1.SQL = myQuery 
 DC1.Refresh 
End Sub 
```

## <a name="update-profile-button"></a><span data-ttu-id="77e7a-123">Update Profile (Schaltfläche)</span><span class="sxs-lookup"><span data-stu-id="77e7a-123">Update Profile Button</span></span>

<span data-ttu-id="77e7a-124">Durch Klicken auf die Schaltfläche **Update Profile** aktiviert das VBScript Update\_OnClick-Unterprozedur Update_OnClick RDS. DataControl-Objekt () SubmitChanges und Refresh-Methode.</span><span class="sxs-lookup"><span data-stu-id="77e7a-124">Clicking the **Update Profile** button activates the VBScript Update\_OnClick Sub procedure, which executes the RDS.DataControl object's () SubmitChanges and Refresh methods.</span></span>

```vb 
 
Sub Update_OnClick 
 DC1.SubmitChanges 
 DC1.Refresh 
End Sub 
```

<span data-ttu-id="77e7a-125">Wenn DC1. SubmitChanges ausgeführt wird, Remote Data Service die Aktualisierungsinformationen verpackt und sendet ihn an den Server via HTTP.</span><span class="sxs-lookup"><span data-stu-id="77e7a-125">When DC1.SubmitChanges executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="77e7a-126">Das Update ist nichts. Wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird die Änderungen vorgenommen, und eine Statusnachricht wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77e7a-126">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="77e7a-127">ausgeführt wird, Remote Data Service die Aktualisierungsinformationen verpackt und sendet ihn an den Server via HTTP.</span><span class="sxs-lookup"><span data-stu-id="77e7a-127">executes, the Remote Data Service packages all the update information and sends it to the server via HTTP.</span></span> <span data-ttu-id="77e7a-128">Das Update ist nichts. Wenn ein Teil der Aktualisierung nicht erfolgreich ist, wird die Änderungen vorgenommen, und eine Statusnachricht wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77e7a-128">The update is all-or-nothing; if a part of the update is unsuccessful, none of the changes is made, and a status message is returned.</span></span> <span data-ttu-id="77e7a-129">DC1. Aktualisieren nach **SubmitChanges** mit Remote Data Service nicht erforderlich, aber es werden aktuelle Daten sichergestellt.</span><span class="sxs-lookup"><span data-stu-id="77e7a-129">DC1.Refresh isn't necessary after **SubmitChanges** with Remote Data Service, but it ensures fresh data.</span></span>

## <a name="cancel-changes-button"></a><span data-ttu-id="77e7a-130">Cancel Changes (Schaltfläche)</span><span class="sxs-lookup"><span data-stu-id="77e7a-130">Cancel Changes Button</span></span>

<span data-ttu-id="77e7a-131">Durch Klicken auf **Cancel Changes** wird die VBScript-Abbrechen aktiviert\_OnClick-Unterprozedur Update_OnClick RDS. DataControl Objekt (CancelUpdate-Methode.</span><span class="sxs-lookup"><span data-stu-id="77e7a-131">Clicking **Cancel Changes** activates the VBScript Cancel\_OnClick Sub procedure, which executes the RDS.DataControl object's ( CancelUpdate method.</span></span>

```vb 
 
Sub Cancel_OnClick 
 DC1.CancelUpdate 
End Sub 
```

<span data-ttu-id="77e7a-p105">Wenn ausgeführt wird, es verwirft alle Änderungen, die ein Benutzer an einem Mitarbeiterdatensatz auf das Datenraster seit der letzten Abfrage oder Aktualisierung vorgenommen hat. Die ursprünglichen Werte werden wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="77e7a-p105">When executes, it discards any edits that a user has made to an employee record on the data grid since the last query or update. It restores the original values.</span></span>

