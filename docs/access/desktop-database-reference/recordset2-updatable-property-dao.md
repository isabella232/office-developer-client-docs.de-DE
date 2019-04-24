---
title: Recordset2. aktualisierbare Eigenschaft (DAO)
TOCTitle: Updatable Property
ms:assetid: ad8184b6-ffe3-dde6-ddee-4b23cdaa9c59
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821726(v=office.15)
ms:contentKeyID: 48547041
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b6e6f2a20b4779259b80eff1fc152abe3698217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309324"
---
# <a name="recordset2updatable-property-dao"></a><span data-ttu-id="4ecc9-102">Recordset2. aktualisierbare Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4ecc9-102">Recordset2.Updatable property (DAO)</span></span>


<span data-ttu-id="4ecc9-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ecc9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4ecc9-104">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="4ecc9-105">Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecc9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ecc9-106">Syntax</span></span>

<span data-ttu-id="4ecc9-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="4ecc9-107">*expression* .Updatable</span></span>

<span data-ttu-id="4ecc9-108">*Ausdruck* Eine Variable, die ein **Recordset2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ecc9-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4ecc9-109">Remarks</span></span>

<span data-ttu-id="4ecc9-110">Snapshot-und Forward-only-Recordset-Objekte geben immer **false**zurück.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="4ecc9-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="4ecc9-p103">Wenn das Objekt nur schreibgeschützte Felder enthält, ist der Wert der **Updatable**-Eigenschaft **False**. Wenn mindestens ein Feld aktualisierbar ist, ist der Wert der Eigenschaft **True**. Sie können nur die aktualisierbaren Felder bearbeiten. Wenn Sie versuchen, einem schreibgeschützten Feld einen neuen Wert zuzuweisen, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="4ecc9-118">Da ein aktualisierbares Objekt schreibgeschützte Felder enthalten kann, müssen Sie die **DataUpdatable**-Eigenschaft der einzelnen Felder der **Fields**-Auflistung eines **Recordset**-Objekts überprüfen, bevor Sie einen Datensatz bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="4ecc9-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

