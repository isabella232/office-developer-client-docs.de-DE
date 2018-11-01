---
title: Bearbeiten vorhandener Datensätze
TOCTitle: Editing Existing Records
ms:assetid: 86b961e0-e0a5-85a2-1138-7ab2e696ec11
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249585(v=office.15)
ms:contentKeyID: 48546089
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c500f89b0f16062e43ace45f55eab9a593d071a2
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884233"
---
# <a name="editing-existing-records"></a>Bearbeiten vorhandener Datensätze


**Betrifft**: Access 2013, Office 2013

Zum Bearbeiten vorhandener Datensätze wechseln Sie zu der Zeile, die Sie bearbeiten möchten, und ändern Sie die **Value** -Eigenschaft der Felder, die Sie bearbeiten möchten. Weitere Informationen zur **Value** -Eigenschaft des **Field** -Objekts finden Sie in [Kapitel 3: Untersuchen von Daten](chapter-3-examining-data.md). In Abhängigkeit vom Cursortyp verwenden Sie **Update** oder **UpdateBatch**, um Änderungen an die Datenquelle zurückzusenden. Weitere Informationen finden Sie in [Kapitel 5: Aktualisieren und Speichern von Daten](chapter-5-updating-and-persisting-data.md).

Gewöhnlich ist es effizienter, eine gespeicherte Prozedur mit einem Befehlsobjekt zu verwenden, um Aktualisierungen vorzunehmen sowie um andere Vorgänge auszuführen, da für eine gespeicherte Prozedur kein Cursor erstellt werden muss. Weitere Informationen zu Cursorn finden Sie in [Kapitel 8: Grundlegendes zu Cursorn und Sperren](chapter-8-understanding-cursors-and-locks.md).

