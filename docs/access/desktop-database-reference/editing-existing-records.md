---
title: Bearbeiten vorhandener Datensätze
TOCTitle: Editing existing records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 575bafdc630e3fa97afa72b54e8f977b758d118d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615571"
---
# <a name="editing-existing-records"></a>Bearbeiten vorhandener Datensätze


**Gilt für**: Access 2013, Office 2013

Zum Bearbeiten vorhandener Datensätze wechseln Sie zu der Zeile, die Sie bearbeiten möchten, und ändern Sie die **Value** -Eigenschaft der Felder, die Sie bearbeiten möchten. Weitere Informationen zur **Value** -Eigenschaft des **Field** -Objekts finden Sie in [Kapitel 3: Untersuchen von Daten](chapter-3-examining-data.md). In Abhängigkeit vom Cursortyp verwenden Sie **Update** oder **UpdateBatch**, um Änderungen an die Datenquelle zurückzusenden. Weitere Informationen finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

Gewöhnlich ist es effizienter, eine gespeicherte Prozedur mit einem Befehlsobjekt zu verwenden, um Aktualisierungen vorzunehmen sowie um andere Vorgänge auszuführen, da für eine gespeicherte Prozedur kein Cursor erstellt werden muss. Weitere Informationen zu Cursorn finden Sie in [Kapitel 8: Grundlegendes zu Cursorn und Sperren](chapter-8-understanding-cursors-and-locks.md).

