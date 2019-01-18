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
# <a name="recordset-related-error-information"></a>Recordset-bezogene Fehlerinformationen

**Betrifft**: Access 2013, Office 2013

Während der Batchverarbeitung stellt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu den einzelnen Datensätzen im **Recordset** -Objekt bereit. Vor einer Batchaktualisierung zeigt die **Status** -Eigenschaft des **Recordset** -Objekts Informationen zu Datensätzen an, die hinzugefügt, geändert und gelöscht werden sollen. 

Nach dem Aufruf von **UpdateBatch** gibt die **Status** -Eigenschaft an, ob der Vorgang erfolgreich ausgeführt wurde. Beim Navigieren in den Datensätzen im **Recordset** -Objekt wird der Wert der **Status** -Eigenschaft geändert, um den Status des aktuellen Datensatzes zu beschreiben.

