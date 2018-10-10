---
title: Was ist neu in ActiveX Data Objects (ADO)
TOCTitle: What's New in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86d3c151ac77ab4138afcd84ee2a14d94dd07aef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473620"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="1f5d4-102">Neuigkeiten in ADO</span><span class="sxs-lookup"><span data-stu-id="1f5d4-102">What's New in ADO</span></span>


<span data-ttu-id="1f5d4-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f5d4-103">**Applies to**: Access 2013 | Office 2013</span></span> 
 

<span data-ttu-id="1f5d4-p101">Die folgenden neuen Features und die folgende erweiterte Dokumentation sind in der Version ADO 2.5 enthalten. In dieser Liste werden ADO, ADO MD und ADOX behandelt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-p101">The following new features and enhanced documentation are included in the ADO 2.5 release. This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="1f5d4-106">Neue Features</span><span class="sxs-lookup"><span data-stu-id="1f5d4-106">New Features</span></span>

<span data-ttu-id="1f5d4-107">**[Datensätze und Datenströme](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="1f5d4-107">**[Records and Streams](chapter-10-records-and-streams.md)**</span></span>

<span data-ttu-id="1f5d4-p102">In dieser Version von ADO wird das [Record](record-object-ado.md)-Objekt eingeführt, durch das z. B. Verzeichnisse und Dateien in einem Dateisystem oder Ordner und Nachrichten in einem E-Mail-System dargestellt und verwaltet werden können. Durch ein **Record** -Objekt kann auch eine Zeile in einem [Recordset](recordset-object-ado.md)-Objekt dargestellt werden, obwohl die Objekte **Record** und **Recordset** über unterschiedliche Methoden und Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-p102">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an e-mail system. A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="1f5d4-110">Das neue [Stream](stream-object-ado.md)-Objekt ermöglicht das Lesen, Schreiben und Verwalten des binären Byte- oder Textdatenstroms, aus dem ein Datei- oder Nachrichtendatenstrom besteht.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

<span data-ttu-id="1f5d4-111">**[URL-Verwendung](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="1f5d4-111">**[URL Usage](absolute-and-relative-urls.md)**</span></span>

<span data-ttu-id="1f5d4-p103">In dieser Version wird außerdem die Verwendung von URLs (Uniform Resource Locators) als Alternative zu Verbindungszeichenfolgen und Befehlstext zum Benennen von Datenspeicherobjekten eingeführt. URLs können mit den vorhandenen Objekten [Connection](connection-object-ado.md) und **Recordset** sowie mit den neuen Objekten **Record** und **Stream** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

<span data-ttu-id="1f5d4-p104">In dieser Version von ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* durch den auf das Windows 2000-Dateisystem zugegriffen wird, das vorhandene HTTP-Schema erkannt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-p104">With this release, ADO supports OLE DB providers that recognize their own URL schemes. For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

<span data-ttu-id="1f5d4-116">**[Spezielle Felder für Dokumentquellenanbieter](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="1f5d4-116">**[Special Fields for Document Source Providers](records-and-provider-supplied-fields.md)**</span></span>

<span data-ttu-id="1f5d4-117">Eine spezielle Klasse von Anbietern von Anbietern von *Quelle des Dokuments* aufgerufen werden Ordner und Dokumente verwaltet.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="1f5d4-118">Wenn ein **Record** -Objekt ein Dokument stellt oder ein **Recordset** -Objekt einen Ordner von Dokumenten stellt, füllt der Dokumentquellenanbieter diese Objekte mit einem eindeutigen Satz von Feldern, die Merkmale des Dokuments beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="1f5d4-119">Diese Felder bilden eine *Ressource* \*\*oder ein \*\*Recordset\*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="1f5d4-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="1f5d4-120">Neue Referenzthemen</span><span class="sxs-lookup"><span data-stu-id="1f5d4-120">New Reference Topics</span></span>

<span data-ttu-id="1f5d4-121">Die folgenden neuen Eigenschaften sind in dieser Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-121">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f5d4-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1f5d4-122">Property</span></span></p></th>
<th><p><span data-ttu-id="1f5d4-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f5d4-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-124"><a href="charset-property-ado.md">CharSet</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-124"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-125">Der Zeichensatz wird angegeben, in den der Inhalt eines <strong>Stream</strong>-Textobjekts übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-125">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-126"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-126"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-127">Gibt an, ob sich die aktuelle Position am Ende des Datenstroms befindet.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-127">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-128"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-128"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-129">Gibt das binäre Zeichen an, das als Zeilentrennzeichen in <strong>Stream</strong>-Textobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-129">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-130"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-130"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-131">Zeigt die verfügbaren Berechtigungen zum Ändern von Daten in einem <strong>Connection</strong>-, <strong>Record</strong>- oder <strong>Stream</strong>-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-131">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-132"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-132"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-133">Gibt die Zeichenfolge einer absoluten URL an, die auf das übergeordnete <strong>Record</strong>-Objekt des aktuellen <strong>Record</strong> -Objekts verweist.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-133">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-134"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-134"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-135">Gibt die aktuelle Position in einem <strong>Stream</strong>-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-135">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-136"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-136"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-137">Gibt den Typ des <strong>Record</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-137">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-138"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-138"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-139">Die Größe des Datenstroms wird als Byteanzahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-139">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-140"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-140"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-141">Die Entität wird angegeben, die durch das <strong>Record</strong>-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-141">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-142"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-142"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-143">Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-143">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="1f5d4-144">Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).</span><span class="sxs-lookup"><span data-stu-id="1f5d4-144">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-145"><a href="type-property-ado-stream.md">Typ</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-145"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-146">Der Typ der im <strong>Stream</strong>-Objekt enthaltenen Daten (Binärdaten oder Textdaten) wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-146">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1f5d4-147">Die folgenden neuen Methoden sind in dieser Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-147">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f5d4-148">Methode</span><span class="sxs-lookup"><span data-stu-id="1f5d4-148">Method</span></span></p></th>
<th><p><span data-ttu-id="1f5d4-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f5d4-149">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-150"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-150"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-151">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-151">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-152"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-152"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-153">Kopiert die angegebene Anzahl von Zeichen oder Bytes (abhängig vom <strong>Typ</strong>) im <strong>Stream</strong> - <strong>Objekt</strong> in ein anderes <strong>Stream</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-153">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-154"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-154"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-155">Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-155">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-156"><a href="flush-method-ado.md">Leeren</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-156"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-157">Es wird erzwungen, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts in das zugrunde liegende Objekt übernommen wird, das dem <strong>Stream</strong>-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-157">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-158"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-158"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-159">Ein <strong>Recordset</strong>-Objekt wird zurückgegeben, dessen Zeilen die Daten und Unterverzeichnisse in dem durch dieses <strong>Record</strong>-Objekt dargestellten Verzeichnis darstellen.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-159">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-160"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-160"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-161">Der Inhalt einer vorhandenen Datei wird in ein <strong>Stream</strong>-Objekt geladen.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-161">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-162"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-162"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-163">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-163">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-164"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-164"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-165">Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-165">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-166"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-166"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-167">Öffnet ein <strong>Stream</strong>-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-167">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-168"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-168"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-169">Liest eine angegebene Anzahl von Bytes aus einem binären <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-169">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-170"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-170"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-171">Liest eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-171">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-172"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-172"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-173">Speichert den binären Inhalt eines <strong>Stream</strong>-Objekts in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-173">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-174"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-174"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-175">Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-175">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-176"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-176"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-177">Beim Lesen eines <strong>Stream</strong>-Textobjekts wird eine gesamte Zeile übersprungen.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-177">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f5d4-178"><a href="write-method-ado.md">Schreiben</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-178"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-179">Schreibt Binärdaten in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-179">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f5d4-180"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="1f5d4-180"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="1f5d4-181">Schreibt eine angegebene Textzeichenfolge in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-181">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="1f5d4-182">Neue und erweiterte Dokumentation</span><span class="sxs-lookup"><span data-stu-id="1f5d4-182">New and Enhanced Documentation</span></span>

<span data-ttu-id="1f5d4-183">**[ADO-Codebeispiele](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="1f5d4-183">**[Code Example Topics](ado-code-examples.md)**</span></span>

<span data-ttu-id="1f5d4-p107">Die Beispiele wurden um in Microsoft Visual C++® und Microsoft Visual J++® geschriebene Codebeispiele erweitert. Sie können diese Codebeispiele kopieren und in den Editor einfügen.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-p107">The examples have been expanded to contain code examples written in Microsoft Visual C++® and Microsoft Visual J++®. You can copy and paste these code examples into your editor.</span></span>

<span data-ttu-id="1f5d4-186">**[Anhang A: Anbieter](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="1f5d4-186">**[Provider Topics](appendix-a-providers.md)**</span></span>

<span data-ttu-id="1f5d4-187">Es ist ein neues Thema enthalten, in dem die Verwendung von ADO mit dem [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-187">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

<span data-ttu-id="1f5d4-188">**[Programmieren mit ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="1f5d4-188">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

<span data-ttu-id="1f5d4-p108">Dieser neue Abschnitt enthält Tipps und Tricks für das Verwenden von ADO mit verschiedenen Programmiersprachen. Er enthält die vorhandenen Syntaxindizes für die Visual C++-Erweiterungen für ADO und ADO/WFC sowie neue Informationen speziell für Entwickler, die Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++ oder Microsoft Visual J++ verwenden.</span><span class="sxs-lookup"><span data-stu-id="1f5d4-p108">This new section contains tips and tricks for using ADO with various programming languages. It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

