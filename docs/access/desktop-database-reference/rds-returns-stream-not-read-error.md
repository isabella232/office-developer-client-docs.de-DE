---
title: Zurückgeben des Fehlers "Stream Not Read" durch RDS
TOCTitle: RDS Returns "Stream Not Read" Error
ms:assetid: 325f7b9d-8e71-bc2c-94e3-b4b4a1a2dc58
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249097(v=office.15)
ms:contentKeyID: 48544075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 312d6f7e29a7573237bf8e4ddab17b9f8796cc4b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870016"
---
# <a name="rds-returns-stream-not-read-error"></a>RDS-gibt \"Stream Not Read\" Fehler


**Betrifft**: Access 2013, Office 2013

"The Stream object could not be read because it is empty, or the current position is at the end of the Stream. For non-empty Streams, set the current position with the Position property. To determine if a Stream is empty, check the Size property." (Das Stream-Objekt konnte nicht gelesen werden, da es leer ist oder weil sich die aktuelle Position am Ende des Streams befindet. Legen Sie bei nicht leeren Streams die aktuelle Position mithilfe der Position-Eigenschaft fest. Überprüfen Sie die Size-Eigenschaft, um festzustellen, ob der Stream leer ist.)

Wenn die obige Fehlermeldung angezeigt wird, wurde möglicherweise versucht, eine parametrisierte hierarchische Abfrage über HTTP zu verwenden. RDS lässt keine parametrisierten Hierarchien über Remoteverbindungen zu.

