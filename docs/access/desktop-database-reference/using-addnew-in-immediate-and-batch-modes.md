---
title: Verwenden der AddNew-Methode im sofortigen Aktualisierungsmodus und im Batchmodus
TOCTitle: Using AddNew in Immediate and Batch Modes
ms:assetid: 1dc32284-9514-083d-ce56-58abbafa7bb7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248970(v=office.15)
ms:contentKeyID: 48543602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 929c01032924182d8db1bd5b06b573fb5d0171ae
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701578"
---
# <a name="using-addnew-in-immediate-and-batch-modes"></a><span data-ttu-id="ae7b4-102">Verwenden von AddNew im Direktfenster und Batch-Modus</span><span class="sxs-lookup"><span data-stu-id="ae7b4-102">Using AddNew in Immediate and Batch modes</span></span>


<span data-ttu-id="ae7b4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae7b4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae7b4-104">Das Verhalten der **AddNew** -Methode hängt vom Aktualisierungsmodus des **Recordset** -Objekts und gibt an, ob Sie die Argumente *FieldList* und *Values* übergeben.</span><span class="sxs-lookup"><span data-stu-id="ae7b4-104">The behavior of the **AddNew** method depends on the updating mode of the **Recordset** object and whether you pass the *FieldList* and *Values* arguments.</span></span>

<span data-ttu-id="ae7b4-p101">Im sofortigen Aktualisierungsmodus (bei dem der Anbieter Änderungen in die zugrunde liegende Datenquelle schreibt, wenn Sie die **Update**-Methode aufrufen) wird durch Aufrufen der **AddNew**-Methode ohne Argumente die **EditMode**-Eigenschaft auf **adEditAdd** festgelegt. Änderungen der Werte von Feldern werden vom Anbieter lokal zwischengespeichert. Durch Aufrufen der **Update**-Methode wird der neue Datensatz in der Datenbank bereitgestellt, und die **EditMode**-Eigenschaft wird auf **adEditNone** zurückgesetzt. Wenn Sie die Argumente *FieldList* und *Values* übergeben, stellt ADO den neuen Datensatz sofort in der Datenbank bereit (der Aufruf von **Update** ist nicht erforderlich). Der Wert der **EditMode**-Eigenschaft wird nicht geändert (**adEditNone**).</span><span class="sxs-lookup"><span data-stu-id="ae7b4-p101">In immediate update mode (in which the provider writes changes to the underlying data source once you call the **Update** method), calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd.** The provider caches any field value changes locally. Calling the **Update** method posts the new record to the database and resets the **EditMode** property to **adEditNone**. If you pass the *FieldList* and *Values* arguments, ADO immediately posts the new record to the database (no **Update** call is necessary); the **EditMode** property value does not change (**adEditNone**).</span></span>

<span data-ttu-id="ae7b4-109">Aufrufen der **AddNew** -Methode ohne Argumente im Batchaktualisierungsmodus werden die **EditMode** -Eigenschaft auf **AdEditAdd**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ae7b4-109">In batch update mode, calling the **AddNew** method without arguments sets the **EditMode** property to **adEditAdd**.</span></span> <span data-ttu-id="ae7b4-110">Alle Änderungen von Feldwerten werden vom Anbieter lokal zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="ae7b4-110">The provider caches any field value changes locally.</span></span> <span data-ttu-id="ae7b4-111">Aufrufen der **Update** -Methode fügt den neuen Datensatz zum aktuellen **Recordset-Objekt** und die **EditMode** -Eigenschaft auf **adEditNone festgelegt**, aber der Anbieter nicht die Änderungen an der zugrunde liegenden Datenbank gebucht wird erst nach dem Aufruf der \*\*UpdateBatch \*\*Methode.</span><span class="sxs-lookup"><span data-stu-id="ae7b4-111">Calling the **Update** method adds the new record to the current **Recordset** and resets the **EditMode** property to **adEditNone**, but the provider does not post the changes to the underlying database until you call the **UpdateBatch** method.</span></span> <span data-ttu-id="ae7b4-112">Wenn Sie die Argumente *FieldList* und *Values* übergeben, sendet ADO den neuen Datensatz an den Anbieter für die Speicherung in einem Cache. Sie müssen die **UpdateBatch** -Methode, um den neuen Datensatz in der zugrunde liegenden Datenbank buchen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ae7b4-112">If you pass the *FieldList* and *Values* arguments, ADO sends the new record to the provider for storage in a cache; you need to call the **UpdateBatch** method to post the new record to the underlying database.</span></span> <span data-ttu-id="ae7b4-113">Weitere Informationen zu **Updates** und **UpdateBatch**, finden Sie unter [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).</span><span class="sxs-lookup"><span data-stu-id="ae7b4-113">For more information about **Update** and **UpdateBatch**, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).</span></span>

