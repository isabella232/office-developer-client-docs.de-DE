---
title: Relations.Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: d71cecf2-da90-5f62-9e51-f994e660ad34
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835058(v=office.15)
ms:contentKeyID: 48547997
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edd018039ce6f612994c06da1036318586924883
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928376"
---
# <a name="relationsrefresh-method-dao"></a><span data-ttu-id="b8fc3-102">Relations.Refresh-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="b8fc3-102">Relations.Refresh method (DAO)</span></span>


<span data-ttu-id="b8fc3-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8fc3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8fc3-104">Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8fc3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8fc3-105">Syntax</span></span>

<span data-ttu-id="b8fc3-106">*Ausdruck* . Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b8fc3-106">*expression* .Refresh</span></span>

<span data-ttu-id="b8fc3-107">*Ausdruck* Eine Variable, die ein **Relations** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-107">*expression* A variable that represents a **Relations** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8fc3-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8fc3-108">Remarks</span></span>

<span data-ttu-id="b8fc3-p101">Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="b8fc3-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="b8fc3-p102">Eine Sammlung ist mit Objekten gefüllt, wenn das erste Mal darauf verwiesen wird. Nachfolgende Änderungen durch andere Benutzer werden nicht automatisch angezeigt. Wenn es wahrscheinlich ist, dass ein anderer Benutzer eine Auflistung geändert hat, wenden Sie sofort die Refresh-Methode auf die Auflistung an, bevor Sie eine Aufgabe in der Anwendung ausführen, die voraussetzt, dass ein bestimmtes Objekt in der Auflistung vorhanden ist bzw. fehlt. So ist sichergestellt, dass die Auflistung möglichst aktuell ist. Andererseits kann die Refresh-Methode die Leistung unnötigerweise beeinträchtigen.
</span><span class="sxs-lookup"><span data-stu-id="b8fc3-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

