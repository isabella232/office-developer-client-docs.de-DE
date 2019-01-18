---
title: Was ist neu in ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713632"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="3888e-102">Neuigkeiten in ADO</span><span class="sxs-lookup"><span data-stu-id="3888e-102">What's new in ADO</span></span>

<span data-ttu-id="3888e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3888e-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="3888e-p101">Die folgenden neuen Features und die folgende erweiterte Dokumentation sind in der Version ADO 2.5 enthalten. In dieser Liste werden ADO, ADO MD und ADOX behandelt.</span><span class="sxs-lookup"><span data-stu-id="3888e-p101">The following new features and enhanced documentation are included in the ADO 2.5 release. This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="3888e-106">Neue features</span><span class="sxs-lookup"><span data-stu-id="3888e-106">New features</span></span>

- <span data-ttu-id="3888e-107">**[Datensätze und Datenströme](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="3888e-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="3888e-108">Diese Version von ADO enthält das [Record](record-object-ado.md) -Objekt, das dargestellt und Dinge wie Verzeichnisse und Dateien in einem Dateisystem oder Ordner und Nachrichten in einem e-Mail-System verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="3888e-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="3888e-109">Ein **Datensatz** kann auch eine Zeile in einem [Recordset-Objekt](recordset-object-ado.md)darstellen, auch wenn Objekte **Record** und **Recordset** über verschiedene Methoden und Eigenschaften haben.</span><span class="sxs-lookup"><span data-stu-id="3888e-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="3888e-110">Das neue [Stream](stream-object-ado.md)-Objekt ermöglicht das Lesen, Schreiben und Verwalten des binären Byte- oder Textdatenstroms, aus dem ein Datei- oder Nachrichtendatenstrom besteht.</span><span class="sxs-lookup"><span data-stu-id="3888e-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="3888e-111">**[URL-Verwendung](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="3888e-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="3888e-p103">In dieser Version wird außerdem die Verwendung von URLs (Uniform Resource Locators) als Alternative zu Verbindungszeichenfolgen und Befehlstext zum Benennen von Datenspeicherobjekten eingeführt. URLs können mit den vorhandenen Objekten [Connection](connection-object-ado.md) und **Recordset** sowie mit den neuen Objekten **Record** und **Stream** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3888e-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="3888e-p104">In dieser Version von ADO werden OLE DB-Anbieter unterstützt, von denen die eigenen URL-Schemas erkannt werden. Beispielsweise wird vom [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* durch den auf das Windows 2000-Dateisystem zugegriffen wird, das vorhandene HTTP-Schema erkannt.</span><span class="sxs-lookup"><span data-stu-id="3888e-p104">With this release, ADO supports OLE DB providers that recognize their own URL schemes. For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="3888e-116">**[Spezielle Felder für Dokumentquellenanbieter](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="3888e-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="3888e-117">Eine spezielle Klasse von Anbietern von Anbietern von *Quelle des Dokuments* aufgerufen werden Ordner und Dokumente verwaltet.</span><span class="sxs-lookup"><span data-stu-id="3888e-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="3888e-118">Wenn ein **Record** -Objekt ein Dokument stellt oder ein **Recordset** -Objekt einen Ordner von Dokumenten stellt, füllt der Dokumentquellenanbieter diese Objekte mit einem eindeutigen Satz von Feldern, die Merkmale des Dokuments beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3888e-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="3888e-119">Diese Felder bilden eine *Ressource* \*\*oder ein \*\*Recordset\*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="3888e-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="3888e-120">Neue Referenzthemen</span><span class="sxs-lookup"><span data-stu-id="3888e-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="3888e-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3888e-121">Properties</span></span>

<span data-ttu-id="3888e-122">Die folgenden neuen Eigenschaften sind in dieser Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="3888e-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3888e-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3888e-123">Property</span></span></p></th>
<th><p><span data-ttu-id="3888e-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3888e-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3888e-125"><a href="charset-property-ado.md">CharSet</a></span><span class="sxs-lookup"><span data-stu-id="3888e-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-126">Der Zeichensatz wird angegeben, in den der Inhalt eines <strong>Stream</strong>-Textobjekts übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3888e-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="3888e-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-128">Gibt an, ob sich die aktuelle Position am Ende des Datenstroms befindet.</span><span class="sxs-lookup"><span data-stu-id="3888e-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="3888e-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-130">Gibt das binäre Zeichen an, das als Zeilentrennzeichen in <strong>Stream</strong>-Textobjekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3888e-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="3888e-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-132">Zeigt die verfügbaren Berechtigungen zum Ändern von Daten in einem <strong>Connection</strong>-, <strong>Record</strong>- oder <strong>Stream</strong>-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3888e-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="3888e-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-134">Gibt die Zeichenfolge einer absoluten URL an, die auf das übergeordnete <strong>Record</strong>-Objekt des aktuellen <strong>Record</strong> -Objekts verweist.</span><span class="sxs-lookup"><span data-stu-id="3888e-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="3888e-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-136">Gibt die aktuelle Position in einem <strong>Stream</strong>-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3888e-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="3888e-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-138">Gibt den Typ des <strong>Record</strong>-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="3888e-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Größe</a></span><span class="sxs-lookup"><span data-stu-id="3888e-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-140">Die Größe des Datenstroms wird als Byteanzahl angegeben.</span><span class="sxs-lookup"><span data-stu-id="3888e-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="3888e-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-142">Die Entität wird angegeben, die durch das <strong>Record</strong>-Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3888e-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="3888e-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-144">Gibt für alle entsprechenden Objekte an, ob deren Status als geöffnet oder geschlossen gilt.</span><span class="sxs-lookup"><span data-stu-id="3888e-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="3888e-145">Gibt für alle entsprechenden Objekte, die eine asynchrone Methode ausführen, den aktuellen Status des Objekts an: Verbindungsherstellung (connecting), Ausführen (executing) oder Abrufen (retrieving).</span><span class="sxs-lookup"><span data-stu-id="3888e-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-146"><a href="type-property-ado-stream.md">Typ</a></span><span class="sxs-lookup"><span data-stu-id="3888e-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-147">Der Typ der im <strong>Stream</strong>-Objekt enthaltenen Daten (Binärdaten oder Textdaten) wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="3888e-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="3888e-148">Methoden</span><span class="sxs-lookup"><span data-stu-id="3888e-148">Methods</span></span>

<span data-ttu-id="3888e-149">Die folgenden neuen Methoden sind in dieser Version enthalten.</span><span class="sxs-lookup"><span data-stu-id="3888e-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3888e-150">Methode</span><span class="sxs-lookup"><span data-stu-id="3888e-150">Method</span></span></p></th>
<th><p><span data-ttu-id="3888e-151">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3888e-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3888e-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="3888e-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-153">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort kopiert.</span><span class="sxs-lookup"><span data-stu-id="3888e-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="3888e-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-155">Kopiert die angegebene Anzahl von Zeichen oder Bytes (abhängig vom <strong>Typ</strong>) im <strong>Stream</strong> - <strong>Objekt</strong> in ein anderes <strong>Stream</strong> -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3888e-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="3888e-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-157">Eine Datei oder ein Verzeichnis mit allen Unterverzeichnissen wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3888e-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-158"><a href="flush-method-ado.md">Leeren</a></span><span class="sxs-lookup"><span data-stu-id="3888e-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-159">Es wird erzwungen, dass der Inhalt des im ADO-Puffer verbleibenden <strong>Stream</strong>-Objekts in das zugrunde liegende Objekt übernommen wird, das dem <strong>Stream</strong>-Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3888e-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="3888e-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-161">Ein <strong>Recordset</strong>-Objekt wird zurückgegeben, dessen Zeilen die Daten und Unterverzeichnisse in dem durch dieses <strong>Record</strong>-Objekt dargestellten Verzeichnis darstellen.</span><span class="sxs-lookup"><span data-stu-id="3888e-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="3888e-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-163">Der Inhalt einer vorhandenen Datei wird in ein <strong>Stream</strong>-Objekt geladen.</span><span class="sxs-lookup"><span data-stu-id="3888e-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="3888e-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-165">Eine Datei oder ein Verzeichnis und sein Inhalt werden an einen anderen Speicherort verschoben.</span><span class="sxs-lookup"><span data-stu-id="3888e-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="3888e-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-167">Ein vorhandenes <strong>Record</strong>-Objekt wird geöffnet, oder eine neue Datei oder ein neues Verzeichnis wird erstellt.</span><span class="sxs-lookup"><span data-stu-id="3888e-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="3888e-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-169">Öffnet ein <strong>Stream</strong>-Objekt, um Datenströme von Binär- oder Textdaten zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3888e-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-170"><a href="read-method-ado.md">Lesen</a></span><span class="sxs-lookup"><span data-stu-id="3888e-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-171">Liest eine angegebene Anzahl von Bytes aus einem binären <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3888e-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="3888e-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-173">Liest eine angegebene Anzahl von Zeichen aus einem <strong>Stream</strong>-Textobjekt.</span><span class="sxs-lookup"><span data-stu-id="3888e-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="3888e-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-175">Speichert den binären Inhalt eines <strong>Stream</strong>-Objekts in eine Datei.</span><span class="sxs-lookup"><span data-stu-id="3888e-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="3888e-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-177">Legt die Position fest, bei der es sich um das Ende des Datenstroms handelt.</span><span class="sxs-lookup"><span data-stu-id="3888e-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="3888e-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-179">Beim Lesen eines <strong>Stream</strong>-Textobjekts wird eine gesamte Zeile übersprungen.</span><span class="sxs-lookup"><span data-stu-id="3888e-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3888e-180"><a href="write-method-ado.md">Write</a>-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3888e-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-181">Schreibt Binärdaten in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3888e-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3888e-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="3888e-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="3888e-183">Schreibt eine angegebene Textzeichenfolge in ein <strong>Stream</strong>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3888e-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="3888e-184">Neue und erweiterte Dokumentation</span><span class="sxs-lookup"><span data-stu-id="3888e-184">New and enhanced documentation</span></span>

- <span data-ttu-id="3888e-185">**[Code-Beispiele](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="3888e-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="3888e-186">In den Beispielen wurden erweitert um Codebeispiele in Microsoft Visual C++ und Microsoft Visual J++ geschriebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="3888e-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="3888e-187">Sie können diese Codebeispiele kopieren und in den Editor einfügen.</span><span class="sxs-lookup"><span data-stu-id="3888e-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="3888e-188">**[Anhang a: Anbieter](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="3888e-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="3888e-189">Es ist ein neues Thema enthalten, in dem die Verwendung von ADO mit dem [OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="3888e-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="3888e-190">**[Programmieren mit ADO](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="3888e-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="3888e-191">Dieser neue Abschnitt enthält Tipps und Tricks für das Verwenden von ADO mit verschiedenen Programmiersprachen.</span><span class="sxs-lookup"><span data-stu-id="3888e-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="3888e-192">Sie enthält die vorhandenen Syntaxindizes für die Visual C++-Erweiterungen für ADO und ADO/WFC-als auch neue Informationen speziell für Entwickler, die mit Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, oder Microsoft Visual J++.</span><span class="sxs-lookup"><span data-stu-id="3888e-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

