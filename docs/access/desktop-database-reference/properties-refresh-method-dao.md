---
title: Properties. Refresh-Methode (DAO)
TOCTitle: Refresh Method
ms:assetid: 71ba18fb-55a5-6a5f-3631-1c81c20f3369
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195805(v=office.15)
ms:contentKeyID: 48545593
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9d6b248bc4b8d9c1a9e01db0231bf58b16c36dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301197"
---
# <a name="propertiesrefresh-method-dao"></a><span data-ttu-id="a09d8-102">Properties. Refresh-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="a09d8-102">Properties.Refresh method (DAO)</span></span>


<span data-ttu-id="a09d8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a09d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a09d8-104">Aktualisiert die Objekte in der angegebenen Auflistung, um das aktuelle Schema der Datenbank wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="a09d8-104">Updates the objects in the specified colletion to reflect the database's current schema.</span></span>

## <a name="syntax"></a><span data-ttu-id="a09d8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a09d8-105">Syntax</span></span>

<span data-ttu-id="a09d8-106">*Ausdruck* . Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="a09d8-106">*expression* .Refresh</span></span>

<span data-ttu-id="a09d8-107">*Ausdruck* Eine Variable, die ein **Properties** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a09d8-107">*expression* A variable that represents a **Properties** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a09d8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a09d8-108">Remarks</span></span>

<span data-ttu-id="a09d8-p101">Verwenden Sie die **Refresh**-Methode in Mehrbenutzerumgebungen, in denen andere Benutzer auf die Datenbank zugreifen können. Außerdem bietet sich diese Methode für Auflistungen an, die indirekt von Änderungen an der Datenbank betroffen sind. Wenn Sie beispielsweise eine **Users**-Auflistung ändern, müssen Sie evtl. vor dem Verwenden der **Groups**-Auflistung eine **Groups**-Auflistung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a09d8-p101">Use the **Refresh** method in multiuser environments in which other users may change the database. You may also need to use it on any collections that are indirectly affected by changes to the database. For example, if you change a **Users** collection, you may need to refresh a **Groups** collection before using the **Groups** collection.</span></span>

<span data-ttu-id="a09d8-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span><span class="sxs-lookup"><span data-stu-id="a09d8-p102">A collection is filled with objects the first time it's referred to and won't automatically reflect subsequent changes other users make. If it's likely that another user has changed a collection, use the Refresh method on the collection immediately before carrying out any task in your application that assumes the presence or absence of a particular object in the collection. This will ensure that the collection is as up-to-date as possible. On the other hand, using Refresh can unnecessarily slow performance.</span></span>

