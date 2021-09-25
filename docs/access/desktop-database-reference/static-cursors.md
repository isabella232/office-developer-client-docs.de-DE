---
title: Statische Cursor (Access-Desktopdatenbankreferenz)
TOCTitle: Static cursors
ms:assetid: 1acf7fc5-fb12-e59e-f480-dde378a29c53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248950(v=office.15)
ms:contentKeyID: 48543524
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b0953c631f1eba746d6f5ce8741e29f78525e219
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580776"
---
# <a name="static-cursors"></a>Statischer Cursor


**Gilt für**: Access 2013, Office 2013

Der statische Cursor zeigt das Resultset so wie beim ersten Öffnen des Cursors an. Je nach Implementierung sind statische Cursor entweder schreibgeschützt oder weisen Lese-/Schreibzugriff auf und ermöglichen den Bildlauf vorwärts und rückwärts. Änderungen an der Mitgliedschaft, der Reihenfolge oder den Werten des Resultsets nach dem Öffnen des Cursors werden gewöhnlich nicht vom Cursor erkannt. Statische Cursor erkennen möglicherweise eigene Aktualisier-, Lösch- und Einfügevorgänge, obwohl sie dies nicht müssen.

Andere Aktualisier-, Lösch- und Einfügevorgänge werden von statischen Cursorn niemals erkannt. Angenommen, ein statischer Cursor ruft eine Zeile ab, und eine andere Anwendung aktualisiert dann diese Zeile. Falls die Anwendung die Zeile erneut vom statischen Cursor abruft, sind die Werte unverändert, trotz der Änderungen durch die andere Anwendung. Alle Bildlaufarten werden unterstützt, aber Lesezeichen werden von Anbietern unterstützt, oder auch nicht.

Wenn Ihre Anwendung Datenänderungen nicht erkennen muss und ein Bildlauf erforderlich ist, ist der statische Cursor optimal geeignet. Verwenden Sie **adOpenStatic** für **CursorTypeEnum**, um anzuzeigen, dass Sie einen statischen Cursor in ADO verwenden möchten.

