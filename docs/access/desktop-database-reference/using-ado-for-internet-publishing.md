---
title: Verwenden von ADO für Internet Publishing
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3a9c6b8dc7a6dc88ac6baf8d05e1baf4a0e048b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868553"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="30a87-102">Verwenden von ADO für Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="30a87-102">Using ADO for Internet Publishing</span></span>


<span data-ttu-id="30a87-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30a87-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="30a87-p101">In [Der OLE DB-Anbieter für Internet Publishing](the-ole-db-provider-for-internet-publishing.md) wird ein konkretes Beispiel für das Zugreifen auf heterogene Daten mit ADO gezeigt. Während sich die Beispiele in diesem Abschnitt speziell auf das Verwenden des Internet Publishing-Anbieters beziehen, sollten die veranschaulichten Prinzipien mit denen für die Verwendung von ADO mit anderen Anbietern für heterogene Daten, z. B. einem Anbieter für einen E-Mail-Speicher, vergleichbar sein.</span><span class="sxs-lookup"><span data-stu-id="30a87-p101">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO. While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an e-mail store.</span></span>

## <a name="urls"></a><span data-ttu-id="30a87-106">URLs</span><span class="sxs-lookup"><span data-stu-id="30a87-106">URLs</span></span>

<span data-ttu-id="30a87-p102">URLs (Uniform Resource Locators) können als Alternative zu Verbindungszeichenfolgen und Befehlstext verwendet werden, um Datenquellen und Speicherorte von Dateien und Verzeichnissen anzugeben. Sie können URLs mit den vorhandenen Objekten [Connection](connection-object-ado.md) und **Recordset** sowie mit den Objekten **Record** und **Stream** verwenden.</span><span class="sxs-lookup"><span data-stu-id="30a87-p102">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories. You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="30a87-109">Weitere Informationen zum Verwenden von URLs finden Sie unter [Absolute und relative URLs](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="30a87-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="30a87-110">Record-Felder</span><span class="sxs-lookup"><span data-stu-id="30a87-110">Record Fields</span></span>

<span data-ttu-id="30a87-p103">Der entscheidende Unterschied zwischen heterogenen Daten und homogenen Daten besteht darin, dass für erstere jede Zeile mit Daten bzw. jeder **Datensatz** einen unterschiedlichen Satz Spalten bzw. **Felder** enthalten kann. Bei homogenen Daten enthält jede Zeile den gleichen Satz Spalten. Weitere Informationen zu den spezifischen Feldern für den Internet Publishing-Anbieter finden Sie unter [Datensätze und vom Anbieter bereitgestellte Felder](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="30a87-p103">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="30a87-114">Anfügen neuer Felder</span><span class="sxs-lookup"><span data-stu-id="30a87-114">Appending New Fields</span></span>

<span data-ttu-id="30a87-115">Mehrere ADO-Objekte wurden verbessert, um mit den Objekten **Record** und **Stream** zusammenzuarbeiten.</span><span class="sxs-lookup"><span data-stu-id="30a87-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="30a87-116">Mit der [Append](fields-collection-ado.md)-Methode der [Fields](append-method-ado.md)-Auflistung, durch die ein [Field](field-object-ado.md)-Objekt erstellt und der Auflistung hinzugefügt wird, kann auch der Wert von **Field** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="30a87-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="30a87-117">Durch die [Update](update-method-ado.md)-Methode wird die Hinzufügung oder Löschung von Feldern in der Auflistung fertig gestellt.</span><span class="sxs-lookup"><span data-stu-id="30a87-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="30a87-118">Als Abkürzung und Alternative zur **Append** -Methode können Sie Felder erstellen, indem Sie einfach einem nicht definierten oder vorher gelöschten Feld einen Wert zuweisen.</span><span class="sxs-lookup"><span data-stu-id="30a87-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="30a87-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a87-119">See also</span></span>

- [<span data-ttu-id="30a87-120">Internet Publishing-Szenario Themen</span><span class="sxs-lookup"><span data-stu-id="30a87-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)