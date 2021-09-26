---
title: Verwenden von CacheSize (Access-Desktopdatenbankreferenz)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 562ccc380c69ba1974405e5d7e4f64a1583f1a4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631643"
---
# <a name="using-cachesize"></a>Verwenden der CacheSize

**Gilt für**: Access 2013, Office 2013

Verwenden Sie die **CacheSize** -Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 aufweist, wird zunächst das **Recordset** -Objekt geöffnet. Anschließend ruft der Anbieter die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Abarbeiten des **Recordset** -Objekts gibt der Anbieter die Daten vom lokalen Arbeitsspeicherpuffer zurück. Sobald Sie den letzten Datensatz im Cache verarbeitet haben, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.

> [!NOTE]
> [!HINWEIS] **CacheSize** basiert auf der anbieterspezifischen Eigenschaft **Maximale Anzahl geöffneter Zeilen** (in der **Properties** -Auflistung des **Recordset** -Objekts). **CacheSize** kann nicht auf einen höheren Wert als **Maximale Anzahl geöffneter Zeilen** festgelegt werden. Legen Sie **Maximale Anzahl geöffneter Zeilen** fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.

Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgenden Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.

Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.

Die Einstellung 0 für **CacheSize** ist nicht zulässig. In diesem Fall würde ein Fehler gemeldet.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.

Wenn **CacheSize** auf einen Wert größer als 1 festgelegt ist, können die Navigationsmethoden ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext und MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) zu einer Navigation zu einem gelöschten Datensatz führen, wenn der Löschvorgang erfolgt, nachdem die Datensätze abgerufen wurden. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to 1 eliminates this issue because deleted rows cannot be fetched.

