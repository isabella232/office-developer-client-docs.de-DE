---
title: Recordsetbezogene Fehlerinformationen
TOCTitle: Recordset-related error information
ms:assetid: 388308c7-e121-bd12-228a-312c897b8c55
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249136(v=office.15)
ms:contentKeyID: 48544222
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5b0dc56ba591263cd834e26ca4e89a371f272d5a
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946468"
---
# <a name="recordset-related-error-information"></a><span data-ttu-id="a17c9-102">Recordsetbezogene Fehlerinformationen</span><span class="sxs-lookup"><span data-stu-id="a17c9-102">Recordset-related error information</span></span>

<span data-ttu-id="a17c9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a17c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a17c9-104">Während der Batchverarbeitung stellt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu den einzelnen Datensätzen im **Recordset** -Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="a17c9-104">During batch processing, the **Status** property of the **Recordset** object provides information about the individual records in the **Recordset**.</span></span> <span data-ttu-id="a17c9-105">Vor einer Batchaktualisierung zeigt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu Datensätzen an, die hinzugefügt, geändert und gelöscht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a17c9-105">Before a batch update takes place, the **Status** property of the **Recordset** reflects information about records to be added, changed and deleted.</span></span> 

<span data-ttu-id="a17c9-106">Nach dem Aufruf von **UpdateBatch** gibt die **Status** -Eigenschaft an, ob der Vorgang erfolgreich ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="a17c9-106">After **UpdateBatch** has been called, the **Status** property indicates the success or failure of the operation.</span></span> <span data-ttu-id="a17c9-107">Beim Navigieren in den Datensätzen im **Recordset** -Objekt wird der Wert der **Status** -Eigenschaft geändert, um den Status des aktuellen Datensatzes zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="a17c9-107">As you move from record to record in the **Recordset,** the value of the **Status** property changes to describe the status of the current record.</span></span>

