---
title: PermissionEnum Enumeration (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3583737eebc881ed5462fe76b6e4a37ad25a8f3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875224"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="dfda0-102">PermissionEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="dfda0-102">PermissionEnum Enumeration (DAO)</span></span>


<span data-ttu-id="dfda0-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dfda0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dfda0-104">Hiermit geben Sie zusammen mit der **Permissions**-Eigenschaft den Berechtigungstyp an.</span><span class="sxs-lookup"><span data-stu-id="dfda0-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dfda0-105">Name</span><span class="sxs-lookup"><span data-stu-id="dfda0-105">Name</span></span></p></th>
<th><p><span data-ttu-id="dfda0-106">Wert</span><span class="sxs-lookup"><span data-stu-id="dfda0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dfda0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfda0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="dfda0-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="dfda0-109">1</span><span class="sxs-lookup"><span data-stu-id="dfda0-109">1</span></span></p></td>
<td><p><span data-ttu-id="dfda0-110">Der Benutzer kann neue Dokumente erstellen (nicht für Dokumentobjekte gültig).</span><span class="sxs-lookup"><span data-stu-id="dfda0-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="dfda0-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="dfda0-112">8</span><span class="sxs-lookup"><span data-stu-id="dfda0-112">8</span></span></p></td>
<td><p><span data-ttu-id="dfda0-113">Der Benutzer kann eine Datenbank replizieren und das Datenbankkennwort ändern (nicht für Dokumentobjekte gültig).</span><span class="sxs-lookup"><span data-stu-id="dfda0-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="dfda0-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="dfda0-115">1</span><span class="sxs-lookup"><span data-stu-id="dfda0-115">1</span></span></p></td>
<td><p><span data-ttu-id="dfda0-p101">Der Benutzer kann neue Datenbanken erstellen. Diese Option ist nur im Datenbankencontainer in der Arbeitsgruppen-Informationsdatei (Systen.mdw) gültig. Diese Konstante ist nicht für Dokumentobjekte gültig.</span><span class="sxs-lookup"><span data-stu-id="dfda0-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="dfda0-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="dfda0-120">4</span><span class="sxs-lookup"><span data-stu-id="dfda0-120">4</span></span></p></td>
<td><p><span data-ttu-id="dfda0-121">Der Benutzer hat exklusiven Zugriff auf die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="dfda0-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="dfda0-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="dfda0-123">2</span><span class="sxs-lookup"><span data-stu-id="dfda0-123">2</span></span></p></td>
<td><p><span data-ttu-id="dfda0-124">Der Benutzer kann die Datenbank öffnen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="dfda0-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="dfda0-126">65536</span><span class="sxs-lookup"><span data-stu-id="dfda0-126">65536</span></span></p></td>
<td><p><span data-ttu-id="dfda0-127">Der Benutzer kann das Objekt löschen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="dfda0-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="dfda0-129">128</span><span class="sxs-lookup"><span data-stu-id="dfda0-129">128</span></span></p></td>
<td><p><span data-ttu-id="dfda0-130">Der Benutzer kann Datensätze löschen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="dfda0-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="dfda0-132">1048575</span><span class="sxs-lookup"><span data-stu-id="dfda0-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="dfda0-133">Der Benutzer hat Vollzugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="dfda0-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="dfda0-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="dfda0-135">32</span><span class="sxs-lookup"><span data-stu-id="dfda0-135">32</span></span></p></td>
<td><p><span data-ttu-id="dfda0-136">Der Benutzer kann Datensätze hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="dfda0-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="dfda0-138">0</span><span class="sxs-lookup"><span data-stu-id="dfda0-138">0</span></span></p></td>
<td><p><span data-ttu-id="dfda0-139">Der Benutzer hat keinen Zugriff auf das Objekt (nicht für Dokumentobjekte gültig).</span><span class="sxs-lookup"><span data-stu-id="dfda0-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="dfda0-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="dfda0-141">4</span><span class="sxs-lookup"><span data-stu-id="dfda0-141">4</span></span></p></td>
<td><p><span data-ttu-id="dfda0-142">Der Benutzer kann die Tabellendefinition lesen, einschließlich Spalten- und Indexinformationen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="dfda0-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="dfda0-144">131072</span><span class="sxs-lookup"><span data-stu-id="dfda0-144">131072</span></span></p></td>
<td><p><span data-ttu-id="dfda0-145">Der Benutzer kann die sicherheitsbezogenen Informationen des Objekts lesen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="dfda0-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="dfda0-147">64</span><span class="sxs-lookup"><span data-stu-id="dfda0-147">64</span></span></p></td>
<td><p><span data-ttu-id="dfda0-148">Der Benutzer kann Datensätze ändern.</span><span class="sxs-lookup"><span data-stu-id="dfda0-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="dfda0-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="dfda0-150">20</span><span class="sxs-lookup"><span data-stu-id="dfda0-150">20</span></span></p></td>
<td><p><span data-ttu-id="dfda0-151">Der Benutzer kann Daten vom Dokumentobjekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-152">über dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="dfda0-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="dfda0-153">65548</span><span class="sxs-lookup"><span data-stu-id="dfda0-153">65548</span></span></p></td>
<td><p><span data-ttu-id="dfda0-154">Der Benutzer kann die Tabellendefinition ändern oder löschen, einschließlich Spalten- und Indexinformationen.</span><span class="sxs-lookup"><span data-stu-id="dfda0-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dfda0-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="dfda0-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="dfda0-156">524288</span><span class="sxs-lookup"><span data-stu-id="dfda0-156">524288</span></span></p></td>
<td><p><span data-ttu-id="dfda0-157">Der Benutzer kann die Einstellung für die Owner-Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="dfda0-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dfda0-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="dfda0-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="dfda0-159">262144</span><span class="sxs-lookup"><span data-stu-id="dfda0-159">262144</span></span></p></td>
<td><p><span data-ttu-id="dfda0-160">Der Benutzer kann Zugriffsberechtigungen ändern.</span><span class="sxs-lookup"><span data-stu-id="dfda0-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

