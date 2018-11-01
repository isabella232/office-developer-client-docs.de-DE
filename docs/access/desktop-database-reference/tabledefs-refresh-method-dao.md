---
title: TableDefs.Refresh Method (DAO)
TOCTitle: Refresh Method
ms:assetid: f76c1a3f-1561-ce1f-a535-a5a2179ea739
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836915(v=office.15)
ms:contentKeyID: 48548765
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9820bf278277d3b7d021f56524fea869eebcdf41
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886067"
---
# <a name="tabledefsrefresh-method-dao"></a><span data-ttu-id="1045c-102">TableDefs.Refresh Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="1045c-102">TableDefs.Refresh Method (DAO)</span></span>


<span data-ttu-id="1045c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1045c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1045c-104">Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="1045c-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="1045c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1045c-105">Syntax</span></span>

<span data-ttu-id="1045c-106">*Ausdruck* . Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="1045c-106">*expression* .Refresh</span></span>

<span data-ttu-id="1045c-107">*Ausdruck* Eine Variable, die ein **TableDefs** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1045c-107">*expression* A variable that represents a **TableDefs** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1045c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1045c-108">Remarks</span></span>

<span data-ttu-id="1045c-p101">Verwenden Sie die **OrdinalPosition**-Eigenschaft der einzelnen **Field**-Objekte, um die Position zu bestimmen, die das Microsoft Access-Datenbankmodul für **Field**-Objekte in der **Fields**-Auflistung eines **QueryDef**-, **Recordset**- oder **TableDef**-Objekts verwendet. Eine Änderung der **OrdinalPosition**-Eigenschaft eines **Field**-Objekts führt möglicherweise erst beim Anwenden der **Refresh**-Methode zu einer geänderten Reihenfolge der **Field**-Objekte.</span><span class="sxs-lookup"><span data-stu-id="1045c-p101">To determine the position that the Microsoft Access database engine uses for **Field** objects in the **Fields** collection of a **QueryDef**, **Recordset**, or **TableDef** object, use the **OrdinalPosition** property of each **Field** object. Changing the **OrdinalPosition** property of a **Field** object may not change the order of the **Field** objects in the collection until you use the **Refresh** method</span></span>

<span data-ttu-id="1045c-p102">Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1045c-p102">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="1045c-p103">Eine Sammlung ist mit Objekten gefüllt, wenn das erste Mal darauf verwiesen wird. Nachfolgende Änderungen durch andere Benutzer werden nicht automatisch angezeigt. Wenn es wahrscheinlich ist, dass ein anderer Benutzer eine Auflistung geändert hat, wenden Sie sofort die Refresh-Methode auf die Auflistung an, bevor Sie eine Aufgabe in der Anwendung ausführen, die voraussetzt, dass ein bestimmtes Objekt in der Auflistung vorhanden ist bzw. fehlt. So ist sichergestellt, dass die Auflistung möglichst aktuell ist. Andererseits kann die Refresh-Methode die Leistung unnötigerweise beeinträchtigen.
</span><span class="sxs-lookup"><span data-stu-id="1045c-p103">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

