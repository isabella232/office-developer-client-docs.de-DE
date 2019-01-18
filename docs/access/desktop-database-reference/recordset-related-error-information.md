---
title: Recordset-bezogene Fehlerinformationen
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 12a67657d5543aac22a49690256b0410a2b901bd
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708900"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="ec8a8-102">Recordset-bezogene Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="ec8a8-102">Recordset-related error information</span></span>

<span data-ttu-id="ec8a8-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec8a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec8a8-104">Während der Batchverarbeitung stellt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu den einzelnen Datensätzen im **Recordset** -Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="ec8a8-105">Vor einer Batchaktualisierung zeigt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu Datensätzen an, die hinzugefügt, geändert und gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="ec8a8-106">Nach dem Aufruf von **UpdateBatch** gibt die **Status** -Eigenschaft an, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="ec8a8-107">Beim Navigieren in den Datensätzen im **Recordset** -Objekt wird der Wert der **Status** -Eigenschaft geändert, um den Status des aktuellen Datensatzes zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ec8a8-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

