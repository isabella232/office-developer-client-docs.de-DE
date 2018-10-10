---
title: AddNew-Methode (ADO)
TOCTitle: AddNew Method (ADO)
ms:assetid: bae09be0-5707-4f38-9c74-0acd0f29dbac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249899(v=office.15)
ms:contentKeyID: 48547384
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b84e6651093d932a17ff20097841bf84bac00c66
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475627"
---
# <a name="addnew-method-ado"></a><span data-ttu-id="0f8ef-102">AddNew-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="0f8ef-102">AddNew Method (ADO)</span></span>


<span data-ttu-id="0f8ef-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f8ef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0f8ef-104">Es wird ein neuer Datensatz für ein aktualisierbares [Recordset](recordset-object-ado.md)-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-104">Creates a new record for an updatable [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8ef-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f8ef-105">Syntax</span></span>

<span data-ttu-id="0f8ef-106">*Recordset-Objekt*. AddNew *FieldList*, *Werte*</span><span class="sxs-lookup"><span data-stu-id="0f8ef-106">*recordset*.AddNew *FieldList*, *Values*</span></span>

## <a name="parameters"></a><span data-ttu-id="0f8ef-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f8ef-107">Parameters</span></span>

  - <span data-ttu-id="0f8ef-108">*recordset*</span><span class="sxs-lookup"><span data-stu-id="0f8ef-108">*recordset*</span></span>

  - <span data-ttu-id="0f8ef-109">Ein **Recordset** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-109">A **Recordset** object.</span></span>

  - <span data-ttu-id="0f8ef-110">*Feldliste*</span><span class="sxs-lookup"><span data-stu-id="0f8ef-110">*FieldList*</span></span>

  - <span data-ttu-id="0f8ef-p101">Optional. Ein einzelner Name oder ein Array aus Namen oder Positionen der Felder im neuen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-p101">Optional. A single name, or an array of names or ordinal positions of the fields in the new record.</span></span>

  - <span data-ttu-id="0f8ef-113">*Values*</span><span class="sxs-lookup"><span data-stu-id="0f8ef-113">*Values*</span></span>

  - <span data-ttu-id="0f8ef-114">Optional.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-114">Optional.</span></span> <span data-ttu-id="0f8ef-115">Ein einzelner Wert oder ein Array aus Werten für die Felder im neuen Datensatz.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-115">A single value, or an array of values for the fields in the new record.</span></span> <span data-ttu-id="0f8ef-116">Wenn *Fieldlist* ein Array ist, muss *Werte* auch ein Array mit der gleichen Anzahl von Elementen sein; andernfalls, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-116">If *Fieldlist* is an array, *Values* must also be an array with the same number of members; otherwise, an error occurs.</span></span> <span data-ttu-id="0f8ef-117">Die Reihenfolge der Feldnamen muss mit der Reihenfolge der Feldwerte in den einzelnen Arrays übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-117">The order of field names must match the order of field values in each array.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f8ef-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f8ef-118">Remarks</span></span>

<span data-ttu-id="0f8ef-p103">Verwenden Sie die **AddNew** -Methode zum Erstellen und Initialisieren eines neuen Datensatzes. Verwenden Sie die [Supports](supports-method-ado.md)-Methode mit **adAddNew** (ein [CursorOptionEnum](cursoroptionenum.md)-Wert), um zu überprüfen, ob Sie dem aktuellen **Recordset** -Objekt Datensätze hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-p103">Use the **AddNew** method to create and initialize a new record. Use the [Supports](supports-method-ado.md) method with **adAddNew** (a [CursorOptionEnum](cursoroptionenum.md) value) to verify whether you can add records to the current **Recordset** object.</span></span>

<span data-ttu-id="0f8ef-p104">Nach dem Aufrufen der AddNew-Methode wird der neue Datensatz zum aktuellen Datensatz und bleibt aktuell, wenn Sie die Update-Methode aufrufen. Da der neue Datensatz dem Recordset-Objekt angefügt wird, wird durch einen Aufruf von MoveNext nach der Aktualisierung an das Ende des Recordset-Objekts gewechselt, sodass EOF True entspricht. Wenn vom Recordset-Objekt keine Lesezeichen unterstützt werden, können Sie möglicherweise nicht auf den neuen Datensatz zugreifen, wenn Sie zu einem anderen Datensatz wechseln. Abhängig vom Cursortyp müssen Sie möglicherweise die Requery-Methode aufrufen, um den Zugriff auf den neuen Datensatz zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-p104">After you call the **AddNew** method, the new record becomes the current record and remains current after you call the [Update](update-method-ado.md) method. Since the new record is appended to the **Recordset**, a call to **MoveNext** following the Update will move past the end of the **Recordset**, making **EOF** True. If the **Recordset** object does not support bookmarks, you may not be able to access the new record once you move to another record. Depending on your cursor type, you may need to call the [Requery](requery-method-ado.md) method to make the new record accessible.</span></span>

<span data-ttu-id="0f8ef-125">Wenn Sie **AddNew** beim Bearbeiten des aktuellen Datensatzes oder beim Hinzufügen eines neuen Datensatzes aufrufen, wird von ADO die **Update** -Methode aufgerufen, um alle Änderungen zu speichern und dann den neuen Datensatz zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-125">If you call **AddNew** while editing the current record or while adding a new record, ADO calls the **Update** method to save any changes and then creates the new record.</span></span>

<span data-ttu-id="0f8ef-126">Das Verhalten der **AddNew** -Methode hängt vom Aktualisierungsmodus des **Recordset** -Objekts und gibt an, ob Sie die Argumente *Fieldlist* und *Values* übergeben.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-126">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *Fieldlist* and *Values* arguments.</span></span>

<span data-ttu-id="0f8ef-p105">Im *unmittelbaren Aktualisierungsmodus* (in dem Änderungen durch den Anbieter in die zugrunde liegende Datenquelle geschrieben werden, wenn Sie die **Update**-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die [EditMode](editmode-property-ado.md)-Eigenschaft auf **adEditAdd** festgelegt (ein [EditModeEnum](editmodeenum.md)-Wert). Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz in der Datenbank bereitgestellt und die **EditMode**-Eigenschaft auf **adEditNone** festgelegt (ein **EditModeEnum**-Wert). Wenn Sie die Argumente *Fieldlist* und *Values*übergeben, wird der neue Datensatz von ADO sofort in der Datenbank bereitgestellt (ein Aufruf von **Update** ist nicht notwendig); der Wert der **EditMode**-Eigenschaft wird nicht geändert (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="0f8ef-p105">In *immediate update mode* (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the [EditMode](editmode-property-ado.md) property to **adEditAdd** (an [EditModeEnum](editmodeenum.md) value). The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone** (an **EditModeEnum** value). If you pass the *Fieldlist* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="0f8ef-131">Im *Batchaktualisierungsmodus* (in dem der Anbieter mehrere Änderungen zwischenspeichert und schreibt sie in der zugrunde liegenden Datenquelle nur, wenn Sie die [UpdateBatch](updatebatch-method-ado.md) -Methode aufrufen), durch Aufrufen der **AddNew** -Methode ohne Argumente **EditMode** wird **AdEditAdd**-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-131">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="0f8ef-132">Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-132">The provider caches any field value changes locally.</span></span> <span data-ttu-id="0f8ef-133">Aufrufen der **Update** -Methode fügt den neuen Datensatz zum aktuellen **Recordset-Objekt** und die **EditMode** -Eigenschaft auf **adEditNone festgelegt**, aber der Anbieter nicht die Änderungen an der zugrunde liegenden Datenbank gebucht wird erst nach dem Aufruf der \*\*UpdateBatch \*\*Methode.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-133">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="0f8ef-134">Wenn Sie die Argumente *Fieldlist* und *Values* übergeben, sendet ADO den neuen Datensatz an den Anbieter für die Speicherung in einem Cache. Sie müssen die **UpdateBatch** -Methode, um den neuen Datensatz in der zugrunde liegenden Datenbank buchen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0f8ef-134">If you pass the *Fieldlist* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span>

