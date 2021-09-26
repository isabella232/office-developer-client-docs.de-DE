---
title: Vorwärtscursor
TOCTitle: Forward-only cursors
ms:assetid: 27541bac-077b-bfe6-d9d8-713e4a945125
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249035(v=office.15)
ms:contentKeyID: 48543834
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 646be880b9e6dab22c8918603d2153f85d138ec7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612086"
---
# <a name="forward-only-cursors"></a>Vorwärtscursor

**Gilt für**: Access 2013, Office 2013

Der typische Standardcursortyp, der so genannte Vorwärtscursor (oder Cursor ohne Bildlauf), kann im Resultset nur vorwärts navigieren. Der Bildlauf (die Möglichkeit, im Resultset vorwärts und rückwärts zu navigieren) wird von diesem Cursortyp nicht unterstützt. Es können vielmehr nur Zeilen vom Anfang bis zum Ende des Resultsets abgerufen werden. Bei einigen Vorwärtscursorn (z. B. bei der SQL Server-Cursorbibliothek), werden alle Einfügungs-, Aktualisierungs- und Löschanweisungen des aktuellen Benutzers (oder anderer Benutzer), die Zeilen im Resultset betreffen, beim Abrufen der Zeilen angezeigt. Für den Cursor ist kein Bildlauf rückwärts möglich, weshalb Änderungen, die nach dem Abrufen von Zeilen in der Datenbank an diesen vorgenommen werden, mit diesem Cursor nicht angezeigt werden.

Nachdem die Daten für die aktuelle Zeile verarbeitet wurden, gibt der Vorwärtscursor die Ressourcen frei, mit denen diese Daten gespeichert wurden. Vorwärtscursor sind standardmäßig dynamisch, weshalb alle Änderungen beim Verarbeiten der aktuellen Zeile erkannt werden. Dadurch kann der Cursor schneller geöffnet werden, und im Resultset können Aktualisierungen an den zugrunde liegenden Tabellen angezeigt werden.

Der Bildlauf rückwärts wird zwar von Vorwärtscursorn nicht unterstützt, aber die Anwendung kann wieder an den Anfang des Resultsets zurückgesetzt werden, indem der Cursor geschlossen und erneut geöffnet wird. Dies ist eine effiziente Arbeitsweise für kleine Datenmengen. Als Alternative könnte die Anwendung das Resultset einmal lesen, die Daten lokal zwischenspeichern und dann den lokalen Datencache durchsuchen.

Wenn für die Anwendung kein Bildlauf im Resultset erforderlich ist, ist der Vorwärtscursor optimal geeignet, um Daten schnell und mit dem geringsten Arbeitsaufwand abzurufen. Verwenden Sie **adOpenForwardOnly** für **CursorTypeEnum**, um anzugeben, dass Sie einen Vorwärtscursor in ADO verwenden möchten.

