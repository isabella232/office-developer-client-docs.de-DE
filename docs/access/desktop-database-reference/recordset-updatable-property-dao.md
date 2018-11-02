---
title: Recordset.Updatable-Eigenschaft (DAO)
TOCTitle: Updatable Property
ms:assetid: 2d4bdcef-1b10-b542-ce0f-6172c271131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192110(v=office.15)
ms:contentKeyID: 48543968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a7f5d803c64504c598a96c244db3fcf75bf0dd5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919262"
---
# <a name="recordsetupdatable-property-dao"></a><span data-ttu-id="ed555-102">Recordset.Updatable-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="ed555-102">Recordset.Updatable property (DAO)</span></span>


<span data-ttu-id="ed555-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ed555-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ed555-p101">Gibt einen Wert zurück, der anzeigt, ob ein DAO-Objekt geändert werden kann. Schreibgeschützter **Boolean**-Wert.</span><span class="sxs-lookup"><span data-stu-id="ed555-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed555-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed555-106">Syntax</span></span>

<span data-ttu-id="ed555-107">*Ausdruck* . Aktualisierbar</span><span class="sxs-lookup"><span data-stu-id="ed555-107">*expression* .Updatable</span></span>

<span data-ttu-id="ed555-108">*Ausdruck* Eine Variable, die ein **Recordset** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="ed555-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed555-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ed555-109">Remarks</span></span>

<span data-ttu-id="ed555-110">Recordset-Objekte vom Typ Momentaufnahme und vorwärtsgerichtet geben immer False zurück.</span><span class="sxs-lookup"><span data-stu-id="ed555-110">Snapshot- and forward-only–type Recordset objects always return **False**.</span></span>

<span data-ttu-id="ed555-p102">Zahlreiche Typen von Objekten können Felder enthalten, die nicht aktualisiert werden können. Sie können z. B. ein Recordset-Objekt vom Typ Dynaset erstellen, in dem nur bestimmte Felder geändert werden können. Diese Felder können feste Daten enthalten oder auch Werte, die automatisch erhöht werden. Das Dynaset kann auch das Ergebnis einer Abfrage sein, in der aktualisierbare und nicht-aktualisierbare Tabellen kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="ed555-p102">Many types of objects can contain fields that can't be updated. For example, you can create a dynaset-type **Recordset** object in which only some fields can be changed. These fields can be fixed or contain data that increments automatically, or the dynaset can result from a query that combines updatable and nonupdatable tables.</span></span>

<span data-ttu-id="ed555-p103">Wenn das Objekt nur schreibgeschützte Felder enthält, ist der Wert der **Updatable**-Eigenschaft **False**. Wenn mindestens ein Feld aktualisierbar ist, ist der Wert der Eigenschaft **True**. Sie können nur die aktualisierbaren Felder bearbeiten. Wenn Sie versuchen, einem schreibgeschützten Feld einen neuen Wert zuzuweisen, tritt ein auffangbarer Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="ed555-p103">If the object contains only read-only fields, the value of the **Updatable** property is **False**. When one or more fields are updatable, the property's value is **True**. You can edit only the updatable fields. A trappable error occurs if you try to assign a new value to a read-only field.</span></span>

<span data-ttu-id="ed555-118">Da ein aktualisierbares Objekt schreibgeschützte Felder enthalten kann, müssen Sie die **DataUpdatable**-Eigenschaft der einzelnen Felder der **Fields**-Auflistung eines **Recordset**-Objekts überprüfen, bevor Sie einen Datensatz bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ed555-118">Because an updatable object can contain read-only fields, check the **DataUpdatable** property of each field in the **Fields** collection of a **Recordset** object before you edit a record.</span></span>

