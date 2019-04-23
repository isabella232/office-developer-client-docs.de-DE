---
title: PermissionEnum-Aufzählung (DAO)
TOCTitle: PermissionEnum Enumeration
ms:assetid: dcce9940-f8a7-e915-1b69-05c341bea8cd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835373(v=office.15)
ms:contentKeyID: 48548147
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8d4f6741bd6203dbdeffb364650b5e3550ea8b1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287710"
---
# <a name="permissionenum-enumeration-dao"></a><span data-ttu-id="acd4c-102">PermissionEnum-Aufzählung (DAO)</span><span class="sxs-lookup"><span data-stu-id="acd4c-102">PermissionEnum enumeration (DAO)</span></span>


<span data-ttu-id="acd4c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="acd4c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="acd4c-104">Hiermit geben Sie zusammen mit der **Permissions**-Eigenschaft den Berechtigungstyp an.</span><span class="sxs-lookup"><span data-stu-id="acd4c-104">Used with the **Permissions** property to specify the type of permissions.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="acd4c-105">Name</span><span class="sxs-lookup"><span data-stu-id="acd4c-105">Name</span></span></p></th>
<th><p><span data-ttu-id="acd4c-106">Wert</span><span class="sxs-lookup"><span data-stu-id="acd4c-106">Value</span></span></p></th>
<th><p><span data-ttu-id="acd4c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="acd4c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-108">dbSecCreate</span><span class="sxs-lookup"><span data-stu-id="acd4c-108">dbSecCreate</span></span></p></td>
<td><p><span data-ttu-id="acd4c-109">1</span><span class="sxs-lookup"><span data-stu-id="acd4c-109">1</span></span></p></td>
<td><p><span data-ttu-id="acd4c-110">Der Benutzer kann neue Dokumente erstellen (nicht für Dokumentobjekte gültig).</span><span class="sxs-lookup"><span data-stu-id="acd4c-110">The user can create new documents (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-111">dbSecDBAdmin</span><span class="sxs-lookup"><span data-stu-id="acd4c-111">dbSecDBAdmin</span></span></p></td>
<td><p><span data-ttu-id="acd4c-112">8</span><span class="sxs-lookup"><span data-stu-id="acd4c-112">8</span></span></p></td>
<td><p><span data-ttu-id="acd4c-113">Der Benutzer kann eine Datenbank replizieren und das Datenbankkennwort ändern (nicht für Dokumentobjekte gültig).</span><span class="sxs-lookup"><span data-stu-id="acd4c-113">The user can replicate a database and change the database password (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-114">dbSecDBCreate</span><span class="sxs-lookup"><span data-stu-id="acd4c-114">dbSecDBCreate</span></span></p></td>
<td><p><span data-ttu-id="acd4c-115">1</span><span class="sxs-lookup"><span data-stu-id="acd4c-115">1</span></span></p></td>
<td><p><span data-ttu-id="acd4c-p101">Der Benutzer kann neue Datenbanken erstellen. Diese Option ist nur im Datenbankencontainer in der Arbeitsgruppen-Informationsdatei (Systen.mdw) gültig. Diese Konstante ist nicht für Dokumentobjekte gültig.</span><span class="sxs-lookup"><span data-stu-id="acd4c-p101">The user can create new databases. This option is valid only on the Databases container in the workgroup information file (Systen.mdw). This constant is not valid for Document objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-119">dbSecDBExclusive</span><span class="sxs-lookup"><span data-stu-id="acd4c-119">dbSecDBExclusive</span></span></p></td>
<td><p><span data-ttu-id="acd4c-120">4</span><span class="sxs-lookup"><span data-stu-id="acd4c-120">4</span></span></p></td>
<td><p><span data-ttu-id="acd4c-121">Der Benutzer hat exklusiven Zugriff auf die Datenbank.</span><span class="sxs-lookup"><span data-stu-id="acd4c-121">The user has exclusive access to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-122">dbSecDBOpen</span><span class="sxs-lookup"><span data-stu-id="acd4c-122">dbSecDBOpen</span></span></p></td>
<td><p><span data-ttu-id="acd4c-123">2</span><span class="sxs-lookup"><span data-stu-id="acd4c-123">2</span></span></p></td>
<td><p><span data-ttu-id="acd4c-124">Der Benutzer kann die Datenbank öffnen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-124">The user can open the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-125">dbSecDelete</span><span class="sxs-lookup"><span data-stu-id="acd4c-125">dbSecDelete</span></span></p></td>
<td><p><span data-ttu-id="acd4c-126">65536</span><span class="sxs-lookup"><span data-stu-id="acd4c-126">65536</span></span></p></td>
<td><p><span data-ttu-id="acd4c-127">Der Benutzer kann das Objekt löschen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-127">The user can delete the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-128">dbSecDeleteData</span><span class="sxs-lookup"><span data-stu-id="acd4c-128">dbSecDeleteData</span></span></p></td>
<td><p><span data-ttu-id="acd4c-129">128</span><span class="sxs-lookup"><span data-stu-id="acd4c-129">128</span></span></p></td>
<td><p><span data-ttu-id="acd4c-130">Der Benutzer kann Datensätze löschen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-130">The user can delete records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-131">dbSecFullAccess</span><span class="sxs-lookup"><span data-stu-id="acd4c-131">dbSecFullAccess</span></span></p></td>
<td><p><span data-ttu-id="acd4c-132">1048575</span><span class="sxs-lookup"><span data-stu-id="acd4c-132">1048575</span></span></p></td>
<td><p><span data-ttu-id="acd4c-133">Der Benutzer hat Vollzugriff auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="acd4c-133">The user has full access to the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-134">dbSecInsertData</span><span class="sxs-lookup"><span data-stu-id="acd4c-134">dbSecInsertData</span></span></p></td>
<td><p><span data-ttu-id="acd4c-135">32</span><span class="sxs-lookup"><span data-stu-id="acd4c-135">32</span></span></p></td>
<td><p><span data-ttu-id="acd4c-136">Der Benutzer kann Datensätze hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-136">The user can add records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-137">dbSecNoAccess</span><span class="sxs-lookup"><span data-stu-id="acd4c-137">dbSecNoAccess</span></span></p></td>
<td><p><span data-ttu-id="acd4c-138">0</span><span class="sxs-lookup"><span data-stu-id="acd4c-138">0</span></span></p></td>
<td><p><span data-ttu-id="acd4c-139">Der Benutzer hat keinen Zugriff auf das Objekt (nicht für Dokumentobjekte gültig).</span><span class="sxs-lookup"><span data-stu-id="acd4c-139">The user does not have access to the object (not valid for Document objects).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-140">dbSecReadDef</span><span class="sxs-lookup"><span data-stu-id="acd4c-140">dbSecReadDef</span></span></p></td>
<td><p><span data-ttu-id="acd4c-141">4</span><span class="sxs-lookup"><span data-stu-id="acd4c-141">4</span></span></p></td>
<td><p><span data-ttu-id="acd4c-142">Der Benutzer kann die Tabellendefinition lesen, einschließlich Spalten- und Indexinformationen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-142">The user can read the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-143">dbSecReadSec</span><span class="sxs-lookup"><span data-stu-id="acd4c-143">dbSecReadSec</span></span></p></td>
<td><p><span data-ttu-id="acd4c-144">131072</span><span class="sxs-lookup"><span data-stu-id="acd4c-144">131072</span></span></p></td>
<td><p><span data-ttu-id="acd4c-145">Der Benutzer kann die sicherheitsbezogenen Informationen des Objekts lesen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-145">The user can read the object's security-related information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-146">dbSecReplaceData</span><span class="sxs-lookup"><span data-stu-id="acd4c-146">dbSecReplaceData</span></span></p></td>
<td><p><span data-ttu-id="acd4c-147">64</span><span class="sxs-lookup"><span data-stu-id="acd4c-147">64</span></span></p></td>
<td><p><span data-ttu-id="acd4c-148">Der Benutzer kann Datensätze ändern.</span><span class="sxs-lookup"><span data-stu-id="acd4c-148">The user can modify records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-149">dbSecRetrieveData</span><span class="sxs-lookup"><span data-stu-id="acd4c-149">dbSecRetrieveData</span></span></p></td>
<td><p><span data-ttu-id="acd4c-150">20</span><span class="sxs-lookup"><span data-stu-id="acd4c-150">20</span></span></p></td>
<td><p><span data-ttu-id="acd4c-151">Der Benutzer kann Daten vom Dokumentobjekt abrufen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-151">The user can retrieve data from the Document object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-152">dbSecWriteDef</span><span class="sxs-lookup"><span data-stu-id="acd4c-152">dbSecWriteDef</span></span></p></td>
<td><p><span data-ttu-id="acd4c-153">65548</span><span class="sxs-lookup"><span data-stu-id="acd4c-153">65548</span></span></p></td>
<td><p><span data-ttu-id="acd4c-154">Der Benutzer kann die Tabellendefinition ändern oder löschen, einschließlich Spalten- und Indexinformationen.</span><span class="sxs-lookup"><span data-stu-id="acd4c-154">The user can modify or delete the table definition, including column and index information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="acd4c-155">dbSecWriteOwner</span><span class="sxs-lookup"><span data-stu-id="acd4c-155">dbSecWriteOwner</span></span></p></td>
<td><p><span data-ttu-id="acd4c-156">524288</span><span class="sxs-lookup"><span data-stu-id="acd4c-156">524288</span></span></p></td>
<td><p><span data-ttu-id="acd4c-157">Der Benutzer kann die Einstellung für die Owner-Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="acd4c-157">The user can change the Owner property setting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="acd4c-158">dbSecWriteSec</span><span class="sxs-lookup"><span data-stu-id="acd4c-158">dbSecWriteSec</span></span></p></td>
<td><p><span data-ttu-id="acd4c-159">262144</span><span class="sxs-lookup"><span data-stu-id="acd4c-159">262144</span></span></p></td>
<td><p><span data-ttu-id="acd4c-160">Der Benutzer kann Zugriffsberechtigungen ändern.</span><span class="sxs-lookup"><span data-stu-id="acd4c-160">The user can alter access permissions.</span></span></p></td>
</tr>
</tbody>
</table>

