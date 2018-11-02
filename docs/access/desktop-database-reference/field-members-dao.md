---
title: Elemente des (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 497c0375496310c27c134792e01bd17e5533a452
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922202"
---
# <a name="field-members-dao"></a><span data-ttu-id="a1817-102">Elemente des (DAO)</span><span class="sxs-lookup"><span data-stu-id="a1817-102">Field members (DAO)</span></span>


<span data-ttu-id="a1817-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1817-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a1817-104">Ein Field-Objekt stellt Daten mit einem gemeinsamen Datentyp in einer Spalte und einer typischen Gruppe von Eigenschaften dar.</span><span class="sxs-lookup"><span data-stu-id="a1817-104">A Field object represents a column of data with a common data type and a common set of properties.</span></span>

## <a name="methods"></a><span data-ttu-id="a1817-105">Methoden</span><span class="sxs-lookup"><span data-stu-id="a1817-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1817-106">Name</span><span class="sxs-lookup"><span data-stu-id="a1817-106">Name</span></span></p></th>
<th><p><span data-ttu-id="a1817-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1817-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1817-108"><strong><a href="field-appendchunk-method-dao.md">Methoden "AppendChunk"</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-108"><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-109">Fügt Daten aus einem Zeichenfolgenausdruck an ein Field-Objekt vom Typ Memo oder Long Binary in einem Recordset an.</span><span class="sxs-lookup"><span data-stu-id="a1817-109">Appends data from a string expression to a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in a <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-110"><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-111">Erstellt ein neues, benutzerdefiniertes <strong><a href="property-object-dao.md">Property</a></strong> -Objekt (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-111">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-112"><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-113">Gibt den gesamten Inhalt oder einen Teil des Inhalts eines <strong><strong>Field</strong></strong> -Objekts vom Typ <a href="field-object-dao.md">Memo</a> oder <strong>Long Binary</strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="a1817-113">Returns all or a portion of the contents of a <strong>Memo</strong> or <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="a1817-114">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="a1817-114">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a1817-115">Name</span><span class="sxs-lookup"><span data-stu-id="a1817-115">Name</span></span></p></th>
<th><p><span data-ttu-id="a1817-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1817-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a1817-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-117"><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-118">Legt fest oder gibt einen Wert, der angibt, ob eine leere Zeichenfolge (&quot;&quot;) ist eine gültige Einstellung für die <strong><a href="field-value-property-dao.md">Value</a></strong> -Eigenschaft des <strong><a href="field-object-dao.md">Field</a></strong> -Objekts mit einem Text- oder Memo-Datentyp (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-118">Sets or returns a value that indicates whether a zero-length string (&quot;&quot;) is a valid setting for the <strong><a href="field-value-property-dao.md">Value</a></strong> property of the <strong><a href="field-object-dao.md">Field</a></strong> object with a Text or Memo data type (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-119"><strong><a href="field-attributes-property-dao.md">Attribute</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-119"><strong><a href="field-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p101">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der ein oder mehrere Merkmale eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts angibt. <strong>Long</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a1817-p101">Sets or returns a value that indicates one or more characteristics of a <strong><a href="field-object-dao.md">Field</a></strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-122"><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p102">Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter <strong>Long</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="a1817-p102">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-125"><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-126">Gibt einen Wert zurück, der angibt, ob die Daten eines durch ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt dargestellten Felds aktualisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="a1817-126">Returns a value that indicates whether the data in the field represented by a <strong><a href="field-object-dao.md">Field</a></strong> object is updatable.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-127"><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p103">Legt den Standardwert eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts fest oder gibt den Wert zurück. Bei einem <strong>Field</strong>-Objekt, das der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung noch nicht angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-p103">Sets or returns the default value of a <strong><a href="field-object-dao.md">Field</a></strong> object. For a <strong>Field</strong> object not yet appended to the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection, this property is read/write (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-130"><strong><a href="field-fieldsize-property-dao.md">Feldgröße</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-130"><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-131">Gibt die Anzahl von Bytes in der Datenbank (nicht im Arbeitsspeicher) verwendete eines Objekts vom Typ Memo oder Long Binary- <strong><a href="field-object-dao.md">Feld</a></strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1817-131">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-132"><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-133">Mit dieser Eigenschaft wird ein Wert festgelegt oder zurückgegeben, der den Namen des <strong><a href="field-object-dao.md">Field</a></strong> -Objekts in einer Fremdtabelle angibt, das einem Feld in einer Primärtabelle für eine Beziehung entspricht (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-133">Sets or returns a value that specifies the name of the <strong><a href="field-object-dao.md">Field</a></strong> object in a foreign table that corresponds to a field in a primary table for a relationship (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-134"><strong><a href="field-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p104">Gibt den Namen des angegebenen Objekts zurück oder legt diesen fest. <strong>String</strong>-Wert mit Lese-/Schreibzugriff, wenn das Objekt noch keiner Auflistung angefügt wurde. Schreibgeschützter <strong>String</strong>-Wert, wenn das Objekt einer Auflistung angefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="a1817-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-138"><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p105">Legt die relative Position eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts innerhalb einer <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung fest oder gibt die relative Position zurück.</span><span class="sxs-lookup"><span data-stu-id="a1817-p105">Sets or returns the relative position of a <strong><a href="field-object-dao.md">Field</a></strong> object within a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection. .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-141"><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="a1817-p106">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1817-p106">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="a1817-144">Gibt den Wert eines <strong>Field</strong>-Objekts in der Datenbank zurück, das vorhanden war, als die letzte Batchaktualisierung begann (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-144">Returns the value of a <strong>Field</strong> in the database that existed when the last batch update began (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-145"><strong><a href="field-properties-property-dao.md">Eigenschaften</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-145"><strong><a href="field-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p107">Gibt die <strong><a href="properties-collection-dao.md">Properties</a></strong> -Auflistung des angegebenen Objekts zurück. Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a1817-p107">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-148"><strong><a href="field-required-property-dao.md">Erforderlich</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-148"><strong><a href="field-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-149">Gibt einen Wert zurück, der angibt, ob ein <strong><a href="field-object-dao.md">Field</a></strong> -Objekt einen Nicht-Null-Wert erfordert, oder legt den betreffenden Wert fest.</span><span class="sxs-lookup"><span data-stu-id="a1817-149">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-150"><strong><a href="field-fieldsize-property-dao.md">Größe</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-150"><strong><a href="field-fieldsize-property-dao.md">Size</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-151">Gibt die Anzahl von Bytes in der Datenbank (nicht im Arbeitsspeicher) verwendete eines Objekts vom Typ Memo oder Long Binary- <strong><a href="field-object-dao.md">Feld</a></strong> in der <strong><a href="fields-collection-dao.md">Fields</a></strong> -Auflistung eines <strong><a href="recordset-object-dao.md">Recordset</a></strong> -Objekts.</span><span class="sxs-lookup"><span data-stu-id="a1817-151">Returns the number of bytes used in the database (rather than in memory) of a Memo or Long Binary <strong><a href="field-object-dao.md">Field</a></strong> object in the <strong><a href="fields-collection-dao.md">Fields</a></strong> collection of a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-152"><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p108">Gibt einen Wert zurück, der den Namen des Felds angibt, das die ursprüngliche Quelle der Daten für ein <strong>Field</strong>-Objekt ist. Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="a1817-p108">Returns a value that indicates the name of the field that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-155"><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p109">Gibt einen Wert zurück, der den Namen einer Tabelle enthält, bei der es sich um die ursprüngliche Datenquelle für ein <strong>Field</strong>-Objekt handelt. Schreibgeschützter <strong>String</strong>-Wert.</span><span class="sxs-lookup"><span data-stu-id="a1817-p109">Returns a value that indicates the name of the table that is the original source of the data for a <strong>Field</strong> object. Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-158"><strong><a href="field-type-property-dao.md">Typ</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-158"><strong><a href="field-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p110">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="a1817-p110">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-161"><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-162">Legt einen Wert fest, der angibt, ob der Wert eines <strong><a href="field-object-dao.md">Field</a></strong> -Objekts sofort der Gültigkeitsprüfung unterzogen wird, wenn die <strong><a href="field-value-property-dao.md">Value</a></strong> -Eigenschaft des Objekts festgelegt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-162">Sets or returns a value that specifies whether or not the value of a <strong><a href="field-object-dao.md">Field</a></strong> object is immediately validated when the object's <strong><a href="field-value-property-dao.md">Value</a></strong> property is set (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-163"><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p111">Legt einen Wert fest, der die Daten in einem Feld überprüft, wenn es geändert oder einer Tabelle hinzugefügt wird, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a1817-p111">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-166"><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p112">Legt einen Wert fest, der den Text der Nachricht angibt, die von der Anwendung angezeigt wird, wenn der Wert eines <strong>Field</strong>-Objekts die von der <strong>ValidationRule</strong>-Eigenschaft festgelegte Gültigkeitsregel nicht unterstützt, oder gibt den betreffenden Wert zurück (nur Microsoft Access-Arbeitsbereiche). <strong>String</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a1817-p112">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only). Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a1817-169"><strong><a href="field-value-property-dao.md">Wert</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-169"><strong><a href="field-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a1817-p113">Legt den Wert eines Objekts fest oder gibt ihn zurück. <strong>Variant</strong>-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a1817-p113">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a1817-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span><span class="sxs-lookup"><span data-stu-id="a1817-172"><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="a1817-p114">[!HINWEIS] ODBCDirect-Arbeitsbereiche werden in Microsoft Access 2013 nicht unterstützt. Verwenden Sie ADO, wenn Sie auf externe Datenquellen zugreifen möchten, ohne das Microsoft Access-Datenbankmodul zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a1817-p114">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="a1817-175">Gibt einen Wert zurück, der aktuell in der Datenbank vorhanden und neuer ist als die <strong>OriginalValue</strong>-Eigenschaft, wie von einem Konflikt der Batchaktualisierung festgestellt wurde (nur ODBCDirect-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="a1817-175">Returns a value currently in the database that is newer than the <strong>OriginalValue</strong> property as determined by a batch update conflict (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

