---
title: TableDefs. Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6050e2d0b97421bda7a2914f068db4019459ee7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306314"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="51358-102">TableDefs. Refresh-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="51358-102">TableDefs.Refresh method (DAO)</span></span>


<span data-ttu-id="51358-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51358-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51358-104">Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="51358-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="51358-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="51358-105">Syntax</span></span>

<span data-ttu-id="51358-106">*Ausdruck* . Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="51358-106">*expression* .Refresh</span></span>

<span data-ttu-id="51358-107">*Ausdruck* Eine Variable, die ein **Tabledefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="51358-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="51358-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51358-108">Remarks</span></span>

<span data-ttu-id="51358-p101">Verwenden Sie die **OrdinalPosition**-Eigenschaft der einzelnen **Field**-Objekte, um die Position zu bestimmen, die das Microsoft Access-Datenbankmodul für **Field**-Objekte in der **Fields**-Auflistung eines **QueryDef**-, **Recordset**- oder **TableDef**-Objekts verwendet. Eine Änderung der **OrdinalPosition**-Eigenschaft eines **Field**-Objekts führt möglicherweise erst beim Anwenden der **Refresh**-Methode zu einer geänderten Reihenfolge der **Field**-Objekte.</span><span class="sxs-lookup"><span data-stu-id="51358-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="51358-p102">Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="51358-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="51358-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span><span class="sxs-lookup"><span data-stu-id="51358-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

