---
title: Recordsetpositionierung
TOCTitle: Recordset positioning
ms:assetid: 1b8b08d5-a11c-ec6e-201c-1405171a1264
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248955(v=office.15)
ms:contentKeyID: 48543546
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bf4c442ecd7cbce740df69d60b5ec3e1e405a412
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997854"
---
# <a name="recordset-positioning"></a>Recordsetpositionierung

**Betrifft**: Access 2013, Office 2013

Verwenden Sie die **AbsolutePosition** -Eigenschaft, um basierend auf der Position im **Recordset** -Objekt zu einem Datensatz zu navigieren, oder um die Position des aktuellen Datensatzes zu bestimmen. Die entsprechende Funktionalität muss vom Anbieter unterstützt werden, damit diese Eigenschaft verfügbar ist.

**AbsolutePosition** ist 1-basiert und entspricht 1, wenn der aktuelle Datensatz der erste Datensatz im **Recordset** -Objekt ist. Wie bereits weiter oben erwähnt, können Sie die Gesamtanzahl der Datensätze im **Recordset** -Objekt mit der **RecordCount** -Eigenschaft abrufen.

Wenn Sie die **AbsolutePosition** -Eigenschaft festlegen, lädt ADO, selbst wenn Sie diese Eigenschaft auf einen Datensatz im aktuellen Cache festlegen, den Cache erneut mit einer neuen Datensatzgruppe, und zwar beginnend mit dem von Ihnen angegebenen Datensatz. Die **CacheSize** -Eigenschaft bestimmt die Größe dieser Gruppe.

> [!NOTE]
> [!HINWEIS] Sie sollten die **AbsolutePosition** -Eigenschaft nicht als Ersatz-Datensatznummer verwenden. Die Position eines Datensatzes wird geändert, wenn Sie einen vorausgehenden Datensatz löschen. Außerdem gibt es keine Gewähr, dass ein bestimmter Datensatz den gleichen Wert für **AbsolutePosition** aufweist, wenn das **Recordset** -Objekt erneut abgefragt oder geöffnet wird. Lesezeichen sind die empfohlene Methode, um zu einer bestimmten Position zurückzukehren, und sie sind die einzige Methode der Positionierung für alle Typen von **Recordset** -Objekten.


