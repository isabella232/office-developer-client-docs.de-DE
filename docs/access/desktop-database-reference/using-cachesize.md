---
title: Verwenden der CacheSize (Access PC-Datenbank-Referenz)
TOCTitle: Using CacheSize
ms:assetid: b1677a9f-f22f-9456-0d2a-1ef7cf81bbdf
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249846(v=office.15)
ms:contentKeyID: 48547148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edf413cbfac35aa20b09508c3af5069f18d5076e
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997434"
---
# <a name="using-cachesize"></a>Verwenden der CacheSize

**Betrifft**: Access 2013, Office 2013

Verwenden Sie die **CacheSize** -Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 aufweist, wird zunächst das **Recordset** -Objekt geöffnet. Anschließend ruft der Anbieter die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Abarbeiten des **Recordset** -Objekts gibt der Anbieter die Daten vom lokalen Arbeitsspeicherpuffer zurück. Sobald Sie den letzten Datensatz im Cache verarbeitet haben, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.

> [!NOTE]
> [!HINWEIS] **CacheSize** basiert auf der anbieterspezifischen Eigenschaft **Maximale Anzahl geöffneter Zeilen** (in der **Properties** -Auflistung des **Recordset** -Objekts). **CacheSize** kann nicht auf einen höheren Wert als **Maximale Anzahl geöffneter Zeilen** festgelegt werden. Legen Sie **Maximale Anzahl geöffneter Zeilen** fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.

Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgenden Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.

Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.

Die Einstellung 0 für **CacheSize** ist nicht zulässig. In diesem Fall würde ein Fehler gemeldet.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.

Wenn CacheSize auf einen Wert größer 1 festgelegt wird, können die Navigationsmethoden (Move, MoveFirst, MoveLast, MoveNext und MovePrevious) dazu führen, dass zu einem gelöschten Datensatz navigiert wird, falls der Löschvorgang nach dem Abrufen der Datensätze erfolgt. Nach dem Abrufen werden nachfolgende Löschvorgänge erst im Datencache übernommen, wenn Sie versuchen auf einen Datenwert in einer gelöschten Zeile zuzugreifen. Wenn Sie allerdings CacheSize auf 1 festlegen, wird dieses Problem beseitigt, weil gelöschte Zeilen nicht abgerufen werden können.

