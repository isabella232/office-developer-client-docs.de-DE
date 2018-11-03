---
title: Datensätze und vom Anbieter bereitgestellte Felder
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a2de9f48b9f35afb208006118add97c9b29c4885
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944522"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="85eea-102">Datensätze und vom Anbieter bereitgestellte Felder</span><span class="sxs-lookup"><span data-stu-id="85eea-102">Records and provider-supplied fields</span></span>

<span data-ttu-id="85eea-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="85eea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85eea-104">Wenn ein [Record](record-object-ado.md)-Objekt geöffnet wird, kann die Quelle die aktuelle Zeile eines geöffneten [Recordsets](recordset-object-ado.md), eine absolute URL oder eine relative URL in Verbindung mit einem geöffneten [Connection](connection-object-ado.md)-Objekt sein.</span><span class="sxs-lookup"><span data-stu-id="85eea-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="85eea-105">Wenn das **Record** -Objekt aus einem **Recordset** -Objekt geöffnet wird, enthält die **Fields**-Auflistung des [Record](fields-collection-ado.md) -Objekts alle Felder aus dem **Recordset** sowie alle durch den zugrunde liegenden Anbieter hinzugefügten Felder.</span><span class="sxs-lookup"><span data-stu-id="85eea-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="85eea-p101">Durch den Anbieter können zusätzliche Felder eingefügt werden, die als ergänzende Merkmale des **Record** -Objekts dienen. Daher verfügt ein **Record** -Objekt möglicherweise über eindeutige Felder, die im gesamten **Recordset** -Objekt oder in einem aus einer anderen Zeile des **Recordset** -Objekts abgeleiteten **Record** -Objekt nicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="85eea-p101">The provider may insert additional fields that serve as supplementary characteristics of the **Record**. As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="85eea-p102">Beispielsweise können alle Zeilen eines von einer E-Mail-Datenquelle abgeleiteten Recordset-Objekts die Spalten Von, An und Betreff enthalten. Ein von diesem Recordset-Objekt abgeleitetes Record-Objekt hat die gleichen Felder. Das Record-Objekt kann jedoch auch andere für die jeweilige Nachricht eindeutige Felder enthalten, die durch dieses Record-Objekt dargestellt werden, z. B. Anlage und CC (Kopie).</span><span class="sxs-lookup"><span data-stu-id="85eea-p102">For example, all rows of a **Recordset** derived from an e-mail data source might have columns such as From, To, and Subject. A **Record** derived from that **Recordset** will have the same fields. However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="85eea-111">Obwohl das **Record** -Objekt und die aktuelle Zeile des **Recordset** -Objekts die gleichen Felder enthalten, unterscheiden sie sich, da die Objekte **Record** und **Recordset** über verschiedene Methoden und Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="85eea-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="85eea-p103">Ein sowohl in **Record** als auch in **Recordset** enthaltenes Feld kann für jedes der Objekte geändert werden. Das Feld kann jedoch nicht für das **Record** -Objekt gelöscht werden, da vom zugrunde liegenden Anbieter möglicherweise das Festlegen des Felds auf Null unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="85eea-p103">A field held in common by the **Record** and **Recordset** can be modified on either object. However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="85eea-p104">Nach dem Öffnen des **Record** -Objekts können Sie programmatisch Felder hinzufügen. Sie können auch hinzugefügte Felder löschen, Sie können jedoch keine Felder aus dem ursprünglichen **Recordset** -Objekt löschen.</span><span class="sxs-lookup"><span data-stu-id="85eea-p104">After the **Record** is opened, you can programmatically add fields. You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="85eea-p105">Sie können das **Record** -Objekt auch direkt über eine URL öffnen. In diesem Fall hängen die dem **Record** -Objekt hinzugefügten Felder vom zugrunde liegenden Anbieter ab. Zurzeit wird durch die meisten Anbieter ein Satz Felder hinzugefügt, in denen die Entität beschrieben wird, die durch das **Record** -Objekt dargestellt wird. Wenn die Entität aus einem Bytedatenstrom besteht, z. B. aus einer einfachen Datei, kann ein [Stream](stream-object-ado.md)-Objekt normalerweise aus dem **Record** -Objekt geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="85eea-p105">You may also open the **Record** object directly from a URL. In this case, the fields added to the **Record** depend on the underlying provider. Currently, most providers add a set of fields that describe the entity represented by the **Record**. If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="85eea-120">Spezielle Felder für Dokumentquellenanbieter</span><span class="sxs-lookup"><span data-stu-id="85eea-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="85eea-p106">Mit einer speziellen Anbieterklasse, den *Dokumentquellenanbietern*, werden Ordner und Dokumente verwaltet. Wenn durch ein **Record**-Objekt ein Dokument dargestellt oder durch ein **Recordset**-Objekt ein Dokumentordner dargestellt wird, werden diese Objekte vom Dokumentquellenanbieter mit einem eindeutigen Satz Felder aufgefüllt, in dem die Merkmale des Dokuments anstelle des eigentlichen Dokuments selbst beschrieben sind. Normalerweise enthält ein Feld einen Verweis auf das **Stream**-Objekt, durch das das Dokument dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="85eea-p106">A special class of providers, called *document source providers*, manages folders and documents. When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself. Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="85eea-124">Diese Felder stellen einen Ressourcen **datensatz** oder ein **Recordset** dar und werden in [Anhang A: Anbieter](appendix-a-providers.md) für die Anbieter aufgelistet, von denen sie unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="85eea-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="85eea-p107">Die **Fields** -Auflistung des **Record** - oder **Recordset** -Objekts einer Ressource wird von zwei Konstanten indiziert, um ein Paar häufig verwendeter Felder abzurufen. Durch die **Value**-Eigenschaft des [Field](value-property-ado.md) -Objekts wird der gewünschte Inhalt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p107">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields. The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="85eea-p108">Das Feld, auf das mit der **adDefaultStream** -Konstante zugegriffen wird, enthält einen dem **Record** - oder **Recordset** -Objekt zugeordneten Standarddatenstrom. Dem Objekt wird vom Anbieter ein Standarddatenstrom zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="85eea-p108">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object. The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="85eea-129">Das Feld, auf das mit der **adRecordURL** -Konstante zugegriffen wird, enthält die absolute URL, durch die das Dokument identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="85eea-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="85eea-p109">Die [Properties](properties-collection-ado.md)-Auflistung der Objekte **Record** und **Field** wird von einem Dokumentquellenanbieter nicht unterstützt. Der Inhalt der **Properties** -Auflistung entspricht für solche Objekte Null.</span><span class="sxs-lookup"><span data-stu-id="85eea-p109">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects. The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="85eea-p110">Von einem Dokumentquellenanbieter kann eine anbieterspezifische Eigenschaft wie z. B **Datasource Type** hinzugefügt werden, um zu identifizieren, ob es sich um einen Dokumentquellenanbieter handelt. Weitere Informationen zum Ermitteln des Anbietertyps finden Sie in der Anbieterdokumentation.</span><span class="sxs-lookup"><span data-stu-id="85eea-p110">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider. For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="85eea-134">Spalten von Ressourcenrecordsets</span><span class="sxs-lookup"><span data-stu-id="85eea-134">Resource Recordset Columns</span></span>

<span data-ttu-id="85eea-135">Ein *Ressourcenrecordset* besteht aus den folgenden Spalten.</span><span class="sxs-lookup"><span data-stu-id="85eea-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="85eea-136">Spaltenname</span><span class="sxs-lookup"><span data-stu-id="85eea-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="85eea-137">Typ</span><span class="sxs-lookup"><span data-stu-id="85eea-137">Type</span></span></p></th>
<th><p><span data-ttu-id="85eea-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85eea-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85eea-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="85eea-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="85eea-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-p111">Schreibgeschützt. Die URL der Ressource wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p111">Read-only. Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="85eea-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="85eea-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-p112">Schreibgeschützt. Die absolute URL des übergeordneten Datensatzes wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p112">Read-only. Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="85eea-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="85eea-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-p113">Schreibgeschützt. Die absolute URL der Ressource, die der Verkettung von PARENTNAME und PARSENAME entspricht, wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p113">Read-only. Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="85eea-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="85eea-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="85eea-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="85eea-p114">True, wenn die Ressource ausgeblendet ist. Es werden nur Zeilen zurückgegeben, wenn durch den Befehl, durch den das Rowset erstellt wird, explizit Zeilen ausgewählt werden, bei denen RESOURCE_ISHIDDEN True entspricht.</span><span class="sxs-lookup"><span data-stu-id="85eea-p114">True if the resource is hidden. No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="85eea-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="85eea-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="85eea-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="85eea-p115">True, wenn die Ressource schreibgeschützt ist. Es wird versucht, diese Ressource mit DBBINDFLAG_WRITE zu öffnen, bei DB_E_READONLY schlägt der Vorgang fehl. Diese Eigenschaft kann auch dann bearbeitet werden, wenn die Ressource nur zum Lesen geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="85eea-p115">True if the resource is read-only. Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY. This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="85eea-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="85eea-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-162">Gibt die wahrscheinlich Verwendung des Dokuments an – beispielsweise ein Anwalt des kurze.</span><span class="sxs-lookup"><span data-stu-id="85eea-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="85eea-163">Dies kann zum Erstellen des Dokuments verwendeten Office-Vorlage entsprechen.&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="85eea-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="85eea-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="85eea-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-166">Gibt den MIME-Typ des Dokuments, der das Format angibt, wie &quot;Text/html&quot;. "</span><span class="sxs-lookup"><span data-stu-id="85eea-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="85eea-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="85eea-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-169">Die Sprache, in der der Inhalt gespeichert wird, wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="85eea-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="85eea-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="85eea-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="85eea-p117">Schreibgeschützt. Es wird eine FILETIME-Struktur angegeben, die die Uhrzeit der Erstellung der Ressource enthält. Die Uhrzeit wird im UTC-Format (Coordinated Universal Time, koordinierte Weltzeit) angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p117">Read-only. Indicates a FILETIME structure containing the time the resource was created. The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="85eea-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="85eea-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="85eea-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="85eea-p118">Schreibgeschützt. Es wird eine FILETIME-Struktur angegeben, die die Uhrzeit des letzten Zugriffs auf die Ressource enthält. Die Uhrzeit wird im UTC-Format angegeben. Die FILETIME-Elemente sind Null, wenn dieses Zeitelement vom Anbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="85eea-p118">Read-only. Indicates a FILETIME structure containing the time that the resource was last accessed. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="85eea-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="85eea-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="85eea-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="85eea-p119">Schreibgeschützt. Es wird eine FILETIME-Struktur angegeben, die die Uhrzeit des letzten Schreibvorgangs für die Ressource enthält. Die Uhrzeit wird im UTC-Format angegeben. Die FILETIME-Elemente sind Null, wenn dieses Zeitelement vom Anbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="85eea-p119">Read-only. Indicates a FILETIME structure containing the time that the resource was last written. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="85eea-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="85eea-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="85eea-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="85eea-p120">Schreibgeschützt. Die Größe des Standarddatenstroms der Ressource wird in Byte angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p120">Read-only. Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="85eea-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="85eea-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="85eea-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="85eea-p121">Schreibgeschützt. True, wenn die Ressource eine Auflistung, z. B. ein Verzeichnis, ist. False, wenn die Ressource eine einfache Datei ist.</span><span class="sxs-lookup"><span data-stu-id="85eea-p121">Read-only. True if the resource is a collection, such as a directory. False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="85eea-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="85eea-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="85eea-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="85eea-p122">True, wenn die Ressource ein strukturiertes Dokument ist. False, wenn die Ressource kein strukturiertes Dokument ist. Sie kann eine Auflistung oder eine einfache Datei sein.</span><span class="sxs-lookup"><span data-stu-id="85eea-p122">True if the resource is a structured document. False if the resource is not a structured document. It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="85eea-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="85eea-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-p123">Schreibgeschützt. Es wird angegeben, dass diese Ressource eine URL zum einfachen Standarddokument eines Ordners oder eines strukturierten Dokuments enthält. Wird verwendet, wenn der Standarddatenstrom von einer Ressource angefordert wird. Diese Eigenschaft ist für eine einfache Datei leer.</span><span class="sxs-lookup"><span data-stu-id="85eea-p123">Read-only. Indicates that this resource contains a URL to the default simple document of a folder or a structured document. Used when the default stream is requested from a resource. This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="85eea-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="85eea-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="85eea-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="85eea-p124">Schreibgeschützt. Optional. Das Kapitel des Rowsets, das die untergeordneten Elemente der Ressource enthält, wird angegeben. (Vom <em>OLE DB-Anbieter für Internet Publishing</em> wird diese Spalte nicht verwendet.)</span><span class="sxs-lookup"><span data-stu-id="85eea-p124">Read-only. Optional. Indicates the chapter of the rowset containing the children of the resource. (The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85eea-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="85eea-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="85eea-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="85eea-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="85eea-p125">Schreibgeschützt. Der Anzeigename der Ressource wird angegeben.</span><span class="sxs-lookup"><span data-stu-id="85eea-p125">Read-only. Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85eea-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="85eea-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="85eea-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="85eea-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="85eea-p126">Schreibgeschützt. True, wenn die Ressource der Stamm einer Auflistung oder eines strukturierten Dokuments ist.</span><span class="sxs-lookup"><span data-stu-id="85eea-p126">Read-only. True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>

