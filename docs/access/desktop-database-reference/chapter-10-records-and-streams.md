---
title: 'Kapitel 10: Datensätze und Datenströme'
TOCTitle: 'Chapter 10: Records and Streams'
ms:assetid: 74862096-2273-3b61-f89c-06554ccf42cd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249477(v=office.15)
ms:contentKeyID: 48545663
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92d0eafcb1930e7aa7014e3b120b34e2a8d64231
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864086"
---
# <a name="chapter-10-records-and-streams"></a><span data-ttu-id="d7cb7-102">Kapitel 10: Datensätze und Datenströme</span><span class="sxs-lookup"><span data-stu-id="d7cb7-102">Chapter 10: Records and Streams</span></span>


<span data-ttu-id="d7cb7-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7cb7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d7cb7-p101">Zurzeit wird durch ADO das [Recordset](recordset-object-ado.md)-Objekt als primäre Methode für das Zugreifen auf Informationen in Datenquellen, z. B. in relationalen Datenbanken, bereitgestellt. Von manchen Anbietern werden jedoch die Objekte [Record](record-object-ado.md) und [Stream](stream-object-ado.md) als alternative oder ergänzende Objekte, mit denen Daten von Anbietern geändert werden können, bereitgestellt. Einzelheiten zum Verhalten von **Record** finden Sie in der Dokumentation des Anbieters.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p101">ADO currently provides the[Recordset](recordset-object-ado.md) object as the primary means of accessing information in data sources, such as relational databases. However, some providers support the [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects as alternative or complementary objects with which data from providers can be manipulated. For specifics on **Record** behavior, see your provider's documentation.</span></span>

## <a name="records"></a><span data-ttu-id="d7cb7-107">Datensätze</span><span class="sxs-lookup"><span data-stu-id="d7cb7-107">Records</span></span>

<span data-ttu-id="d7cb7-p102">**Record**-Objekte fungieren im Wesentlichen als einzeilige **Datensätze**. **Datensätze** verfügen jedoch im Vergleich zu **Recordsets** über eine eingeschränkte Funktionalität und unterschiedliche Eigenschaften und Methoden. Die Quelle für die Daten in einem **Record**-Objekt kann ein Befehl sein, durch den eine Zeile mit Daten vom Anbieter zurückgegeben wird. Das Verwenden von **Record**-Objekten anstelle von **Recordset**-Objekten zum Empfangen der Ergebnisse aus einer Abfrage, durch die eine Zeile mit Daten zurückgegeben wird, eliminiert den Aufwand für das Instanziieren des komplexeren **Recordset**-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p102">**Record** objects essentially function as one-row **Recordset**s. However, **Records** have limited functionality compared to **Recordsets** and they have different properties and methods.The source for the data in a **Record** object can be a command which returns one row of data from the provider. Using **Record** objects rather than **Recordset** objects to receive the results from a query that returns one row of data eliminates the overhead of instantiating the more complex **Recordset** object.</span></span>

<span data-ttu-id="d7cb7-p103">**Record** -Objekte können zu einem anderen Zweck dienen, insbesondere bei anderen Anbietern als herkömmlichen relationalen Datenbanken für Datenquellen, z. B. dem [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Ein großer Teil der zu verarbeitenden Informationen ist nicht als Tabellen in Datenbanken, sondern als Nachrichten in elektronischen Mailsystemen und Dateien in modernen Dateisystemen vorhanden. Die Objekte **Record** und **Stream** ermöglichen den Zugriff auf Informationen, die in anderen Quellen als in relationalen Datenbanken gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p103">**Record** objects can serve another purpose, particularly with providers for data sources other than traditional relational databases, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Much of the information that must be processed exists, not as tables in databases, but as messages in electronic mail systems and files in modern file systems. The **Record** and **Stream** objects facilitate access to information stored in sources other than relational databases.</span></span>

<span data-ttu-id="d7cb7-p104">Durch das **Record** -Objekt können Daten, z. B. Verzeichnisse und Dateien in einem Dateisystem oder Ordner und Nachrichten in einem E-Mail-System, dargestellt und verwaltet werden. Zu diesen Zwecken kann die Quelle für das **Record** -Objekt die aktuelle Zeile eines geöffneten **Recordset** -Objekts, eine absolute URL oder eine relative URL in Verbindung mit einem geöffneten [Connection](connection-object-ado.md)-Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p104">The **Record** object can represent and manage data such as directories and files in a file system or folders and messages in an e-mail system. For these purposes, the source for the **Record** can be the current row of an open **Recordset**, an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="d7cb7-p105">Normalerweise kann ein **Recordset** -Objekt verwendet werden, um einen Container oder einen übergeordneten Container in einer Hierarchie, z. B. einen Ordner oder ein Verzeichnis, darzustellen. Ein **Record** -Objekt kann verwendet werden, um bestimmte Informationen zu einem Knoten im übergeordneten Container, z. B. eine Datei oder ein Dokument, zurückzugeben. Der Hauptgrund für die Verwendung von **Record** -Objekten zum Darstellen dieses Informationstyps besteht darin, dass diese Datenquellen heterogen sind. Das heißt, dass jedes **Record** -Objekt verschiedene und unterschiedlich viele Felder enthalten kann. Herkömmliche **Recordset** -Objekte, die Zeilen aus einer Datenbank enthalten, sind homogen, d. h., jede Zeile enthält gleich viele Felder vom gleichen Typ.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p105">Typically, a **Recordset** can be used to represent a container or parent in a hierarchy such as a folder or directory. A **Record** can be used to return specific information about one node in the parent container, such as a file or document. The primary reason **Records** are used to represent this type of information is that these sources of data are heterogenous. This means that each **Record** may have a different set and number of fields. Traditional **Recordsets** containing rows from a database are homogenous, which means that each row has the same number and type of fields.</span></span>

<span data-ttu-id="d7cb7-121">Weitere Informationen zum Verwenden des **Record** -Objekts zum Verarbeiten dieser heterogenen Daten von Anbietern wie dem Internet Publishing-Anbieter finden Sie unter [Verwenden von ADO für Internet Publishing](using-ado-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d7cb7-121">For more information about using the **Record** object for processing this heterogeneous data from providers such as the Internet Publishing Provider, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

## <a name="streams"></a><span data-ttu-id="d7cb7-122">Datenströme</span><span class="sxs-lookup"><span data-stu-id="d7cb7-122">Streams</span></span>

<span data-ttu-id="d7cb7-p106">Durch das **Stream** -Objekt wird die Möglichkeit zum Lesen, Schreiben und Verwalten eines Bytedatenstroms bereitgestellt. Dieser Bytedatenstrom kann aus Text oder Binärdaten bestehen und ist in der Größe nur durch die Systemressourcen beschränkt. Normalerweise werden **Stream** -ADO-Objekte für die folgenden Zwecke verwendet:</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p106">The **Stream** object provides the means to read, write, and manage a stream of bytes. This byte stream may be text or binary and is limited in size only by system resources. Typically, ADO **Stream** objects are used for the following purposes:</span></span>

  - <span data-ttu-id="d7cb7-p107">Abrufen des Texts oder der Bytes, aus denen eine Datei oder Nachricht besteht, wird normalerweise mit Anbietern wie dem Microsoft OLE DB-Anbieter für Internet Publishing verwendet. Weitere Informationen zu dieser Verwendung von **Stream** -Objekten finden Sie unter [Verwenden von ADO für Internet Publishing](using-ado-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p107">To contain the text or bytes that comprise a file or message, typically used with providers such as the Microsoft OLE DB Provider for Internet Publishing. For more information about this use of **Stream** objects, see [Using ADO for Internet Publishing](using-ado-for-internet-publishing.md).</span></span>

<span data-ttu-id="d7cb7-128">Ein **Stream** -Objekt kann für Folgendes geöffnet werden:</span><span class="sxs-lookup"><span data-stu-id="d7cb7-128">A **Stream** object can be opened on:</span></span>

  - <span data-ttu-id="d7cb7-129">Eine einfache Datei, die mit einer URL angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-129">A simple file specified with a URL.</span></span>

  - <span data-ttu-id="d7cb7-130">Ein Feld eines **Record** oder **Recordset** -Objekts, das ein **Stream** -Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-130">A field of a **Record** or **Recordset** containing a **Stream** object.</span></span>

  - <span data-ttu-id="d7cb7-131">Den Standarddatenstrom eines **Record** - oder **Recordset** -Objekts, das ein Verzeichnis oder eine Verbunddatei darstellt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-131">The default stream of a **Record** or **Recordset** object representing a directory or compound file.</span></span>

  - <span data-ttu-id="d7cb7-132">Ein Ressourcenfeld, das die URL einer einfachen Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-132">A resource field containing the URL of a simple file.</span></span>

  - <span data-ttu-id="d7cb7-p108">Keine bestimmte Quelle. In diesem Fall wird ein **Stream** -Objekt im Arbeitsspeicher geöffnet. Es ist möglich, Daten in das Objekt zu schreiben und es in einem anderen **Stream** -Objekt oder einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-p108">No particular source at all. In this case, a **Stream** object is opened in memory. Data can be written to it and then saved in another **Stream** or file.</span></span>

  - <span data-ttu-id="d7cb7-136">Ein BLOB-Feld in einem **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7cb7-136">A BLOB field in a **Recordset**.</span></span>

<span data-ttu-id="d7cb7-137">In diesem Kapitel werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="d7cb7-137">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="d7cb7-138">Streams and Persistence</span><span class="sxs-lookup"><span data-stu-id="d7cb7-138">Streams and Persistence</span></span>](streams-and-persistence.md)

- [<span data-ttu-id="d7cb7-139">Records and Provider-Supplied Fields</span><span class="sxs-lookup"><span data-stu-id="d7cb7-139">Records and Provider-Supplied Fields</span></span>](records-and-provider-supplied-fields.md)

- [<span data-ttu-id="d7cb7-140">Absolute und relative URLs</span><span class="sxs-lookup"><span data-stu-id="d7cb7-140">Absolute and Relative URLs</span></span>](absolute-and-relative-urls.md)

- [<span data-ttu-id="d7cb7-141">Using ADO for Internet Publishing (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7cb7-141">Using ADO for Internet Publishing (ADO)</span></span>](using-ado-for-internet-publishing.md)