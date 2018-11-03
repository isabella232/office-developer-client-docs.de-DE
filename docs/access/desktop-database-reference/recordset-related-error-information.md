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
# <a name="recordset-related-error-information"></a>Recordsetbezogene Fehlerinformationen

**Betrifft**: Access 2013, Office 2013

Während der Batchverarbeitung stellt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu den einzelnen Datensätzen im **Recordset** -Objekt bereit. Vor einer Batchaktualisierung zeigt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu Datensätzen an, die hinzugefügt, geändert und gelöscht werden sollen. 

Nach dem Aufruf von **UpdateBatch** gibt die **Status** -Eigenschaft an, ob der Vorgang erfolgreich ausgeführt wurde. Beim Navigieren in den Datensätzen im **Recordset** -Objekt wird der Wert der **Status** -Eigenschaft geändert, um den Status des aktuellen Datensatzes zu beschreiben.

