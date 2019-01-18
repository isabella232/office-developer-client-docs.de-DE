---
title: Was ist ein Cursor?  (Access PC-Datenbank-Referenz)
TOCTitle: What is a Cursor?
ms:assetid: cc70d941-05e0-9b14-1c5d-6b1a5802f546
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250013(v=office.15)
ms:contentKeyID: 48547738
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2023b39620f80e6f770153e381c74d5285d027c6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718938"
---
# <a name="what-is-a-cursor"></a><span data-ttu-id="5d5b9-103">Was ist ein Cursor?</span><span class="sxs-lookup"><span data-stu-id="5d5b9-103">What is a cursor?</span></span>


<span data-ttu-id="5d5b9-104">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d5b9-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d5b9-p102">Vorgänge in einer relationalen Datenbank fungieren auf einem vollständigen Zeilensatz. Der Zeilensatz, der von einer SELECT-Anweisung zurückgegeben wird, besteht aus allen Zeilen, die den Bedingungen in der WHERE-Klausel der Anweisung entsprechen. Dieser vollständige Zeilensatz, der von der Anweisung zurückgegeben wird, wird als Resultset bezeichnet. Anwendungen, insbesondere interaktive Anwendungen und Onlineanwendungen, können nicht immer effizient mit dem gesamten Resultset als eine Einheit arbeiten. Diese Anwendungen benötigen einen Mechanismus, um jeweils mit einer Zeile oder einem kleinen Zeilenblock zu arbeiten. Cursor sind eine Erweiterung für Resultsets, die diesen Mechanismus anbieten.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p102">Operations in a relational database act on a complete set of rows. The set of rows returned by a SELECT statement consists of all the rows that satisfy the conditions in the WHERE clause of the statement. This complete set of rows returned by the statement is known as the result set. Applications, especially those that are interactive and online, cannot always work effectively with the entire result set as a unit. These applications need a mechanism to work with one row or a small block of rows at a time. Cursors are an extension to result sets that provide that mechanism.</span></span>

<span data-ttu-id="5d5b9-p103">Ein Cursor wird von einer Cursorbibliothek implementiert. Eine Cursorbibliothek ist Software, die häufig als Teil eines Datenbanksystems oder einer Datenzugriffs-API implementiert wird und zum Verwalten der Attribute von Daten, die von einer Datenquelle (ein Resultset) zurückgegeben werden, verwendet wird. Zu diesen Attributen zählen Parallelitätsverwaltung, Position im Resultset, Anzahl der zurückgegebenen Zeilen sowie, ob die Navigation vorwärts und/oder rückwärts im Resultset möglich ist (Bildlauffähigkeit).</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p103">A cursor is implemented by a cursor library. A cursor library is software, often implemented as a part of a database system or a data access API, that is used to manage attributes of data returned from a data source (a result set). These attributes include concurrency management, position in the result set, number of rows returned, and whether or not you can move forward and/or backward through the result set (scrollability).</span></span>

<span data-ttu-id="5d5b9-p104">Ein Cursor verfolgt die Position im Resultset und ermöglicht die zeilenweise Ausführung mehrerer Vorgänge für ein Resultset, wobei zur ursprünglichen Tabelle zurückgekehrt wird, oder auch nicht. Cursor geben also ein Resultset basierend auf Tabellen innerhalb der Datenbanken zurück. Der Cursor heißt so, weil er die aktuelle Position im Resultset angibt, so wie der Cursor auf einem Computerbildschirm die aktuelle Position anzeigt.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p104">A cursor keeps track of the position in the result set, and allows you to perform multiple operations row by row against a result set, with or without returning to the original table. In other words, cursors conceptually return a result set based on tables within the databases. The cursor is so named because it indicates the current position in the result set, just as the cursor on a computer screen indicates current position.</span></span>

<span data-ttu-id="5d5b9-117">Sie sollten sich unbedingt mit dem Cursorkonzept vertraut machen, bevor Sie sich mit den Einzelheiten ihrer Verwendung in ADO beschäftigen.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-117">It is important to become familiar with the concept of cursors before moving on to learn the specifics of their usage in ADO.</span></span>

<span data-ttu-id="5d5b9-118">Cursor ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5d5b9-118">Using cursors, you can:</span></span>

  - <span data-ttu-id="5d5b9-119">Angeben der Position in bestimmten Zeilen im Resultset.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-119">Specify positioning at specific rows in the result set.</span></span>

  - <span data-ttu-id="5d5b9-120">Abrufen einer Zeile oder eines Zeilenblocks basierend auf der aktuellen Resultsetposition.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-120">Retrieve one row or a block of rows based on the current result set position.</span></span>

  - <span data-ttu-id="5d5b9-121">Ändern von Daten in den Zeilen an der aktuellen Position im Resultset.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-121">Modify data in the rows at the current position in the result set.</span></span>

  - <span data-ttu-id="5d5b9-122">Definieren unterschiedlicher Ebenen der Empfindlichkeit gegenüber Datenänderungen durch andere Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-122">Define different levels of sensitivity to data changes made by other users.</span></span>

<span data-ttu-id="5d5b9-p105">Angenommen, eine Anwendung zeigt einem potenziellen Käufer eine Liste verfügbarer Produkte an. Der Käufer führt einen Bildlauf in der Liste aus, um Produktdetails und Kosten anzuzeigen, und wählt schließlich ein Produkt für den Kauf aus. Für den Rest der Liste werden zusätzliche Bildlauf- und Auswahlschritte ausgeführt. Was den Käufer betrifft, werden die Produkte einzeln angezeigt, aber die Anwendung verwendet einen bildlauffähigen Cursor, um das Resultset nach oben und unten zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p105">For example, consider an application that displays a list of available products to a potential buyer. The buyer scrolls through the list to see product details and cost, and finally selects a product for purchase. Additional scrolling and selection occurs for the remainder of the list. As far as the buyer is concerned, the products appear one at a time, but the application uses a scrollable cursor to browse up and down through the result set.</span></span>

<span data-ttu-id="5d5b9-127">Sie können Cursor auf verschiedene Weise verwenden:</span><span class="sxs-lookup"><span data-stu-id="5d5b9-127">You can use cursors in a variety of ways:</span></span>

  - <span data-ttu-id="5d5b9-128">Ohne Zeilen.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-128">With no rows at all.</span></span>

  - <span data-ttu-id="5d5b9-129">Mit einigen oder allen Zeilen in einer einzelnen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-129">With some or all of the rows in a single table.</span></span>

  - <span data-ttu-id="5d5b9-130">Mit einigen oder allen Zeilen aus logisch verknüpften Tabellen.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-130">With some or all of the rows from logically joined tables.</span></span>

  - <span data-ttu-id="5d5b9-131">Als schreibgeschützt oder aktualisierbar auf Cursor- oder Feldebene.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-131">As read-only or updateable at the cursor or field level.</span></span>

  - <span data-ttu-id="5d5b9-132">Als Vorwärtscursor oder voll bildlauffähigen Cursor.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-132">As forward-only or fully scrollable.</span></span>

  - <span data-ttu-id="5d5b9-133">Mit dem Cursorkeyset auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-133">With the cursor keyset located on the server.</span></span>

  - <span data-ttu-id="5d5b9-134">Empfindlich für Änderungen an zugrunde liegenden Tabellen durch andere Anwendungen (z. B. Mitgliedschaft, Sortierung, Einfügungen, Aktualisierungen und Löschvorgänge).</span><span class="sxs-lookup"><span data-stu-id="5d5b9-134">Sensitive to underlying table changes caused by other applications (such as membership, sort, inserts, updates, and deletes).</span></span>

  - <span data-ttu-id="5d5b9-135">Auf dem Server oder auf dem Client vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-135">Existing on either the server or the client.</span></span>

<span data-ttu-id="5d5b9-p106">Mit schreibgeschützten Cursorn können Benutzer das Resultset durchsuchen, und Cursor mit Lese-/Schreibzugriff können einzelne Zeilenaktualisierungen implementieren. Komplexe Cursor können mit Keysets definiert werden, die auf Basistabellenzeilen zurückverweisen. Manche Cursor sind für die Vorwärtsnavigation schreibgeschützt, während andere Cursor rückwärts und vorwärts navigieren können und eine dynamische Aktualisierung des Resultsets basierend auf Änderungen durch andere Anwendungen an der Datenbank ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p106">Read-only cursors help users browse through the result set, and read/write cursors can implement individual row updates. Complex cursors can be defined with keysets that point back to base table rows. While some cursors are read-only in a forward direction, others can move back and forth and provide a dynamic refresh of the result set based on changes that other applications are making to the database.</span></span>

<span data-ttu-id="5d5b9-p107">Nicht alle Anwendungen müssen Cursor verwenden, um auf Daten zuzugreifen oder diese zu aktualisieren. Manche Abfragen erfordern keine direkte Zeilenaktualisierung mithilfe eines Cursors. Cursor sollten eines der letzten Verfahren sein, die Sie zum Abrufen von Daten auswählen - und in diesem Fall sollten Sie den Cursor mit dem geringsten Aufwand auswählen. Wenn Sie ein Resultset mithilfe einer gespeicherten Prozedur erstellen, kann das Resultset nicht mit Cursorbearbeitungs- oder Cursoraktualisierungsmethoden aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p107">Not all applications need to use cursors to access or update data. Some queries simply do not require direct row updating by using a cursor. Cursors should be one of the last techniques you choose to retrieve data — and then you should choose the lowest impact cursor possible. When you create a result set by using a stored procedure, the result set is not updateable using cursor edit or update methods.</span></span>

## <a name="concurrency"></a><span data-ttu-id="5d5b9-143">Parallelität</span><span class="sxs-lookup"><span data-stu-id="5d5b9-143">Concurrency</span></span>

<span data-ttu-id="5d5b9-p108">Bei manchen Mehrbenutzeranwendungen müssen die dem Endbenutzer angezeigten Daten unbedingt möglichst aktuell sein. Ein klassisches Beispiel für ein solches System ist ein Flugreservierungssystem, bei dem sich möglicherweise viele Benutzer um den gleichen Platz für einen bestimmten Flug schlagen (und damit einen einzelnen Datensatz). In diesem Fall muss der Anwendungsentwurf gleichzeitige Vorgänge für einen einzelnen Datensatz ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p108">In some multi-user applications it is vitally important for the data presented to the end user to be as current as possible. A classic example of such a system is an airline reservation system, where many users might be contending for the same seat on a given flight (and thus, a single record). In a case like this, the application design must handle concurrent operations on a single record.</span></span>

<span data-ttu-id="5d5b9-p109">Bei anderen Anwendungen ist die Parallelität nicht so wichtig. In diesen Fällen ist der Aufwand, die Daten ständig auf dem aktuellen Stand zu halten, nicht gerechtfertigt.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p109">In other applications, concurrency is not as important. In such cases, the expense involved in keeping the data current at all times cannot be justified.</span></span>

## <a name="position"></a><span data-ttu-id="5d5b9-149">Position</span><span class="sxs-lookup"><span data-stu-id="5d5b9-149">Position</span></span>

<span data-ttu-id="5d5b9-p110">Ein Cursor verfolgt auch die aktuelle Position in einem Resultset. Stellen Sie sich die Cursorposition als Zeiger auf den aktuellen Datensatz vor, ähnlich wie ein Arrayindex auf den Wert an eben dieser Position im Array zeigt.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-p110">A cursor also keeps track of the current position in a result set. Think of the cursor position as a pointer to the current record, similar to the way an array index points to the value at that particular location in the array.</span></span>

## <a name="scrollability"></a><span data-ttu-id="5d5b9-152">Bildlauffähigkeit</span><span class="sxs-lookup"><span data-stu-id="5d5b9-152">Scrollability</span></span>

<span data-ttu-id="5d5b9-153">Der Typ des Cursors, die von der Anwendung verwendete wirkt sich auch die Möglichkeit, die die Zeilen in einem Resultset vorwärts- und Rückwärtssuche durchlaufen; Dies wird manchmal als Scrollfähigkeit bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-153">The type of cursor employed by your application also affects the ability to move forward and backward through the rows in a result set; this is sometimes called scrollability.</span></span> <span data-ttu-id="5d5b9-154">Die Möglichkeit zum Vorwärts- *und* Rückwärtsblättern durch ein Resultset Verschieben der Komplexität des Cursors hinzugefügt und ist deshalb teurer implementieren.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-154">The ability to move forward *and* backward through a result set adds to the complexity of the cursor, and is therefore more expensive to implement.</span></span> <span data-ttu-id="5d5b9-155">Aus diesem Grund sollten Sie einen Cursor mit dieser Funktionalität nur bei Bedarf erhalten.</span><span class="sxs-lookup"><span data-stu-id="5d5b9-155">For this reason, you should ask for a cursor with this functionality only when necessary.</span></span>

