---
title: Aktualisieren von Daten (Access PC-Datenbank-Referenz)
TOCTitle: Updating Data
ms:assetid: 02e82066-77c8-cbb2-db28-98e2fc94404c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248794(v=office.15)
ms:contentKeyID: 48542970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70ca34183d135c6907a185984b02b394776bfda4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944221"
---
# <a name="updating-data"></a><span data-ttu-id="39c0e-102">Aktualisieren von Daten</span><span class="sxs-lookup"><span data-stu-id="39c0e-102">Updating data</span></span>


<span data-ttu-id="39c0e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="39c0e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="39c0e-104">Aktualisierungsverhalten und Funktionalität sind größtenteils vom Aktualisierungsmodus (Sperrtyp), Cursortyp und Cursorplatzierung abhängig.</span><span class="sxs-lookup"><span data-stu-id="39c0e-104">Update behavior and functionality is largely dependent upon update mode (lock type), cursor type, and cursor location.</span></span>

<span data-ttu-id="39c0e-p101">Verwenden Sie die **Update** -Methode, um Änderungen am aktuellen Datensatz eines **Recordset** -Objekts seit dem Aufrufen der **AddNew** -Methode oder seit dem Ändern von Feldwerten in einem vorhandenen Datensatz zu speichern. Das **Recordset** -Objekt muss Aktualisierungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="39c0e-p101">Use the **Update** method to save any changes you have made to the current record of a **Recordset** object since calling the **AddNew** method or since changing any field values in an existing record. The **Recordset** object must support updates.</span></span>

<span data-ttu-id="39c0e-p102">Wenn das **Recordset** -Objekt die Batchaktualisierung unterstützt, können Sie mehrere Änderungen an mindestens einem Datensatz bis zum Aufrufen der **UpdateBatch** -Methode lokal speichern. Falls Sie den aktuellen Datensatz bearbeiten oder einen neuen Datensatz hinzufügen, wenn Sie die **UpdateBatch** -Methode aufrufen, ruft ADO automatisch die **Update** -Methode auf, um ausstehende Änderungen am aktuellen Datensatz zu speichern, bevor die Batchänderungen an den Anbieter übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="39c0e-p102">If the **Recordset** object supports batch updating, you can cache multiple changes to one or more records locally until you call the **UpdateBatch** method. If you are editing the current record or adding a new record when you call the **UpdateBatch** method, ADO will automatically call the **Update** method to save any pending changes to the current record before transmitting the batched changes to the provider.</span></span>

<span data-ttu-id="39c0e-109">Der aktuelle Datensatz bleibt aktuell, nachdem Sie die Methode **Update** oder **UpdateBatch** aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="39c0e-109">The current record remains current after you call the **Update** or **UpdateBatch** methods.</span></span>

<span data-ttu-id="39c0e-110">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="39c0e-110">This section includes the following topics:</span></span>

- [<span data-ttu-id="39c0e-111">Sofortiger Aktualisierungsmodus</span><span class="sxs-lookup"><span data-stu-id="39c0e-111">Immediate mode</span></span>](immediate-mode.md)
- [<span data-ttu-id="39c0e-112">Die Verarbeitung von Transaktionen</span><span class="sxs-lookup"><span data-stu-id="39c0e-112">Transaction processing</span></span>](transaction-processing.md)
- [<span data-ttu-id="39c0e-113">Batch-Modus (ADO)</span><span class="sxs-lookup"><span data-stu-id="39c0e-113">Batch mode (ADO)</span></span>](batch-mode.md)

