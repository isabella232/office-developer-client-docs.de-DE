---
title: Microsoft OLE DB-Anbieter für Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e473176ae6a34d04fc316a8d5075e414f6c8e98
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868147"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a><span data-ttu-id="4bf11-102">Microsoft OLE DB-Anbieter für Oracle</span><span class="sxs-lookup"><span data-stu-id="4bf11-102">Microsoft OLE DB Provider for Oracle</span></span>

<span data-ttu-id="4bf11-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bf11-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bf11-104">Der Microsoft OLE DB-Anbieter für Oracle ermöglicht ADO den Zugriff auf Oracle-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="4bf11-104">The Microsoft OLE DB Provider for Oracle allows ADO to access Oracle databases.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="4bf11-105">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="4bf11-105">Connection String Parameters</span></span>

<span data-ttu-id="4bf11-106">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider* -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="4bf11-106">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAORA 
```

<span data-ttu-id="4bf11-107">Beim Lesen der [Provider](provider-property-ado.md)-Eigenschaft wird diese Zeichenfolge ebenfalls zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bf11-107">Reading the [Provider](provider-property-ado.md) property will return this string as well.</span></span>

<span data-ttu-id="4bf11-p101">Wenn eine JOIN-Abfrage mit einem dynamischen oder einem Keyset-Cursor in einer Oracle-Datenbank ausgeführt wird, tritt ein Fehler auf. Oracle unterstützt nur schreibgeschützte statische Cursor.</span><span class="sxs-lookup"><span data-stu-id="4bf11-p101">If a join query with a keyset or dynamic cursor is executed in an Oracle database, an error occurs. Oracle only supports a static read-only cursor.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="4bf11-110">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4bf11-110">Typical Connection String</span></span>

<span data-ttu-id="4bf11-111">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="4bf11-111">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
```

<span data-ttu-id="4bf11-112">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="4bf11-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bf11-113">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="4bf11-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="4bf11-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bf11-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bf11-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-116">Gibt den OLE DB-Anbieter für Oracle an.</span><span class="sxs-lookup"><span data-stu-id="4bf11-116">Specifies the OLE DB Provider for Oracle.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf11-117"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-117"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-118">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="4bf11-118">Specifies the name of a server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf11-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-120">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="4bf11-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf11-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-122">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="4bf11-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a><span data-ttu-id="4bf11-123">Anbieterspezifische Verbindungsparameter</span><span class="sxs-lookup"><span data-stu-id="4bf11-123">Provider-Specific Connection Parameters</span></span>

<span data-ttu-id="4bf11-p102">Der Anbieter unterstützt neben den von ADO definierten verschiedene anbieterspezifische Verbindungsparameter. Wie die ADO-Verbindungseigenschaften können diese anbieterspezifischen Eigenschaften über die [Properties](properties-collection-ado.md)-Auflistung eines [Connection](connection-object-ado.md)-Objekts oder als Teil der **ConnectionString** -Eigenschaft festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="4bf11-p102">The provider supports several provider-specific connection parameters in addition to those defined by ADO. As with the ADO connection properties, these provider-specific properties can be set via the [Properties](properties-collection-ado.md) collection of a [Connection](connection-object-ado.md) or as part of the **ConnectionString**.</span></span>

<span data-ttu-id="4bf11-p103">Diese Parameter sind in OLE DB Programmer's Reference ausführlich beschrieben. (Im "ADO Dynamic Property Index" finden Sie Querverweise zwischen diesen Parameternamen und den entsprechenden OLE DB-Eigenschaften.)</span><span class="sxs-lookup"><span data-stu-id="4bf11-p103">These parameters are fully described in the OLE DB Programmer's Reference. (The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between these parameter names and the corresponding OLE DB properties.)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bf11-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bf11-128">Parameter</span></span></p></th>
<th><p><span data-ttu-id="4bf11-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4bf11-129">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bf11-130"><strong>Window Handle</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-130"><strong>Window Handle</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-131">Gibt den Fensterhandle an, der verwendet werden soll, um nach zusätzlichen Informationen anzufragen.</span><span class="sxs-lookup"><span data-stu-id="4bf11-131">Indicates the window handle to use to prompt for additional information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf11-132"><strong>Locale Identifier</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-132"><strong>Locale Identifier</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-p104">Gibt eine eindeutige 32-Bit-Zahl (z. B. 1033) an, mit der Einstellungen für die Sprache des Benutzers festgelegt werden. Diese Einstellungen geben an, wie Datum und Uhrzeit formatiert, Elemente alphabetisch sortiert, Zeichenfolgen verglichen werden usw.</span><span class="sxs-lookup"><span data-stu-id="4bf11-p104">Indicates a unique 32-bit number (for example, 1033) that specifies preferences related to the user's language. These preferences indicate how dates and times are formatted, items are sorted alphabetically, strings are compared, and so on.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf11-135"><strong>OLE DB Services</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-135"><strong>OLE DB Services</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-136">Gibt eine Bitmaske an, die angibt, welche OLE DB-Dienste aktiviert oder deaktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4bf11-136">Indicates a bitmask that specifies OLE DB services to enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf11-137"><strong>Prompt</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-137"><strong>Prompt</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-138">Gibt an, ob für den Benutzer eine Eingabeaufforderung angezeigt wird, während eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4bf11-138">Indicates whether to prompt the user while a connection is being established.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf11-139"><strong>Extended Properties</strong></span><span class="sxs-lookup"><span data-stu-id="4bf11-139"><strong>Extended Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="4bf11-p105">Eine Zeichenfolge mit anbieterspezifischen erweiterten Verbindungsinformationen. Verwenden Sie diese Eigenschaft nur für anbieterspezifische Verbindungsinformationen, die nicht über den Eigenschaftenmechanismus beschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="4bf11-p105">A string containing provider-specific, extended connection information. Use this property only for provider-specific connection information that cannot be described through the property mechanism.</span></span></p></td>
</tr>
</tbody>
</table>

