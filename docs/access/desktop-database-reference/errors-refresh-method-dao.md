---
title: Errors.Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: dc352c5f-09d0-bfb3-b24a-4c3454dbf5aa
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835359(v=office.15)
ms:contentKeyID: 48548127
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c01dc4400593853daa4f2f82597d20032c3517dc
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924575"
---
# <a name="errorsrefresh-method-dao"></a><span data-ttu-id="99199-102">Errors.Refresh-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="99199-102">Errors.Refresh method (DAO)</span></span>


<span data-ttu-id="99199-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="99199-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="99199-104">Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="99199-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="99199-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99199-105">Syntax</span></span>

<span data-ttu-id="99199-106">*Ausdruck* . Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="99199-106">*expression* .Refresh</span></span>

<span data-ttu-id="99199-107">*Ausdruck* Eine Variable, die ein **Errors** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="99199-107">*expression* A variable that represents an **Errors** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="99199-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99199-108">Remarks</span></span>

<span data-ttu-id="99199-p101">Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="99199-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="99199-p102">Eine Sammlung ist mit Objekten gefüllt, wenn das erste Mal darauf verwiesen wird. Nachfolgende Änderungen durch andere Benutzer werden nicht automatisch angezeigt. Wenn es wahrscheinlich ist, dass ein anderer Benutzer eine Auflistung geändert hat, wenden Sie sofort die Refresh-Methode auf die Auflistung an, bevor Sie eine Aufgabe in der Anwendung ausführen, die voraussetzt, dass ein bestimmtes Objekt in der Auflistung vorhanden ist bzw. fehlt. So ist sichergestellt, dass die Auflistung möglichst aktuell ist. Andererseits kann die Refresh-Methode die Leistung unnötigerweise beeinträchtigen.
</span><span class="sxs-lookup"><span data-stu-id="99199-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

