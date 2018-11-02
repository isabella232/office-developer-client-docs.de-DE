---
title: Mit der Methode DBEngine.OpenDatabase (DAO)
TOCTitle: OpenDatabase Method
ms:assetid: 49fca321-5955-3e69-64ea-da191536eadb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193474(v=office.15)
ms:contentKeyID: 48544654
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052979
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 23357443eeb479a6bdba2a3cc994de226290118a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922622"
---
# <a name="dbengineopendatabase-method-dao"></a><span data-ttu-id="e2878-102">Mit der Methode DBEngine.OpenDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="e2878-102">DBEngine.OpenDatabase method (DAO)</span></span>


<span data-ttu-id="e2878-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2878-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2878-104">Öffnet eine angegebene Datenbank und gibt einen Verweis auf das **[Database](database-object-dao.md)** -Objekt zurück, das sie darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2878-104">Opens a specified database and returns a reference to the **[Database](database-object-dao.md)** object that represents it.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2878-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2878-105">Syntax</span></span>

<span data-ttu-id="e2878-106">*Ausdruck* . OpenDatabase (***Name***, ***Optionen***, ***ReadOnly***, ***Verbinden***)</span><span class="sxs-lookup"><span data-stu-id="e2878-106">*expression* .OpenDatabase(***Name***, ***Options***, ***ReadOnly***, ***Connect***)</span></span>

<span data-ttu-id="e2878-107">*Ausdruck* Eine Variable, die ein **DBEngine** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2878-107">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="e2878-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2878-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2878-109">Name</span><span class="sxs-lookup"><span data-stu-id="e2878-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e2878-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="e2878-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="e2878-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e2878-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="e2878-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2878-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2878-113">Name</span><span class="sxs-lookup"><span data-stu-id="e2878-113">Name</span></span></p></td>
<td><p><span data-ttu-id="e2878-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e2878-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e2878-115"><strong>Zeichenfolge</strong></span><span class="sxs-lookup"><span data-stu-id="e2878-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e2878-p101">der Name einer vorhandenen Microsoft Access-Datenbankdatei oder der Datenquellenname (Data Source Name, DSN) einer ODBC-Datenquelle. Weitere Informationen zum Festlegen dieses Wertes finden Sie in der <strong><a href="connection-name-property-dao.md">Name</a></strong> -Eigenschaft.  </span><span class="sxs-lookup"><span data-stu-id="e2878-p101">the name of an existing Microsoft Access database file, or the data source name (DSN) of an ODBC data source. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for more information about setting this value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2878-118">Options</span><span class="sxs-lookup"><span data-stu-id="e2878-118">Options</span></span></p></td>
<td><p><span data-ttu-id="e2878-119">Optional</span><span class="sxs-lookup"><span data-stu-id="e2878-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="e2878-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e2878-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e2878-121">Legt entsprechend der Angaben unter den Hinweisen verschiedene Optionen für die Datenbank fest.</span><span class="sxs-lookup"><span data-stu-id="e2878-121">Sets various options for the database, as specified in Remarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2878-122">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="e2878-122">ReadOnly</span></span></p></td>
<td><p><span data-ttu-id="e2878-123">Optional</span><span class="sxs-lookup"><span data-stu-id="e2878-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="e2878-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e2878-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e2878-125"><strong>True</strong>, wenn Sie eine Datenbank nur mit Lesezugriff öffnen möchten, oder <strong>False</strong> (Standard), wenn Sie die Datenbank mit Lese-/Schreibzugriff öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="e2878-125"><strong>True</strong> if you want to open the database with read-only access, or <strong>False</strong> (default) if you want to open the database with read/write access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2878-126">Verbinden</span><span class="sxs-lookup"><span data-stu-id="e2878-126">Connect</span></span></p></td>
<td><p><span data-ttu-id="e2878-127">Optional</span><span class="sxs-lookup"><span data-stu-id="e2878-127">Optional</span></span></p></td>
<td><p><span data-ttu-id="e2878-128"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e2878-128"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e2878-129">Gibt verschiedene Verbindungsinformationen an, einschließlich der Kenntwörter.</span><span class="sxs-lookup"><span data-stu-id="e2878-129">Specifies various connection information, including passwords.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="e2878-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2878-130">Return value</span></span>

<span data-ttu-id="e2878-131">Datenbank</span><span class="sxs-lookup"><span data-stu-id="e2878-131">Database</span></span>

## <a name="remarks"></a><span data-ttu-id="e2878-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2878-132">Remarks</span></span>

<span data-ttu-id="e2878-133">Sie können für das options-Argument folgende Werte verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2878-133">You can use the following values for the options argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2878-134">Einstellung</span><span class="sxs-lookup"><span data-stu-id="e2878-134">Setting</span></span></p></th>
<th><p><span data-ttu-id="e2878-135">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e2878-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2878-136"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="e2878-136"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="e2878-137">Öffnet die Datenbank im Exklusivmodus.</span><span class="sxs-lookup"><span data-stu-id="e2878-137">Opens the database in exclusive mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2878-138"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="e2878-138"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="e2878-139">(Standard) Öffnet die Datenbank im Freigabemodus.</span><span class="sxs-lookup"><span data-stu-id="e2878-139">(Default) Opens the database in shared mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e2878-140">Wenn Sie eine Datenbank öffnen, wird sie automatisch zur **Databases** -Sammlung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e2878-140">When you open a database, it is automatically added to the **Databases** collection.</span></span>

<span data-ttu-id="e2878-141">Einige Aspekte sollten bei Verwenden von Dbname:</span><span class="sxs-lookup"><span data-stu-id="e2878-141">Some considerations apply when you use dbname:</span></span>

  - <span data-ttu-id="e2878-142">Wenn er sich auf eine Datenbank bezieht, die bereits für den Zugriff durch einen anderen Benutzer geöffnet wurde, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e2878-142">If it refers to a database that is already open for access by another user, an error occurs.</span></span>

  - <span data-ttu-id="e2878-143">Wenn er sich nicht auf eine vorhandene Datenbank oder einen gültigen ODBC-Datenquellennamen bezieht, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e2878-143">If it doesn't refer to an existing database or valid ODBC data source name, an error occurs.</span></span>

  - <span data-ttu-id="e2878-144">Ist eine leere Zeichenfolge ("") und "ODBC;" ist *eine Verbindung herstellen* , wird ein Dialogfeld mit allen registrierten ODBC-Datenquellennamen angezeigt, damit der Benutzer eine Datenbank auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="e2878-144">If it's a zero-length string ("") and *connect* is "ODBC;" , a dialog box listing all registered ODBC data source names is displayed so the user can select a database.</span></span>

<span data-ttu-id="e2878-145">Um eine Datenbank zu schließen und so das **Database** -Objekt aus der **Databases** -Auflistung zu entfernen, verwenden Sie für das Objekt die **[Close](connection-close-method-dao.md)** -Methode.</span><span class="sxs-lookup"><span data-stu-id="e2878-145">To close a database, and thus remove the **Database** object from the **Databases** collection, use the **[Close](connection-close-method-dao.md)** method on the object.</span></span>


> [!NOTE]
> <span data-ttu-id="e2878-146">[!HINWEIS] Wenn Sie auf eine ODBC-Datenquelle zugreifen, die mit einem Microsoft Access-Datenbankmodul verbunden ist, können Sie die Leistung der Anwendung verbessern, indem Sie ein **Database** -Objekt öffnen, das mit der ODBC-Datenquelle verbunden ist, anstatt einzelne [TableDef](tabledef-object-dao.md) -Objekte mit bestimmten Tabellen in der ODBC-Datenquelle zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e2878-146">When you access a Microsoft Access database engine-connected ODBC data source, you can improve your application's performance by opening a **Database** object connected to the ODBC data source, rather than by linking individual [TableDef](tabledef-object-dao.md) objects to specific tables in the ODBC data source.</span></span>


