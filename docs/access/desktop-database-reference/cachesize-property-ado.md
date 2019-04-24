---
title: CacheSize-Eigenschaft (ADO)
TOCTitle: CacheSize property (ADO)
ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15)
ms:contentKeyID: 48544491
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 725c2f81b3f3bce05a3007c50705e9cf35f7008f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296745"
---
# <a name="cachesize-property-ado"></a>CacheSize-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Anzahl von Datensätzen aus einem [Recordset](recordset-object-ado.md)-Objekt an, die lokal im Arbeitsspeicher zwischengespeichert werden.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Sets or returns a **Long** value that must be greater than 0. Default is 1.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **CacheSize**-Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 hat, ruft der Anbieter, nachdem er zunächst das **Recordset**-Objekt geöffnet hat, die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Durchlaufen des **Recordset**-Objekts gibt der Anbieter die Daten aus dem lokalen Arbeitsspeicherpuffer zurück. Sobald Sie hinter den letzten Datensatz im Cache gelangt sind, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.

> [!NOTE]
> [!HINWEIS] **CacheSize** basiert auf der anbieterspezifischen Eigenschaft **Maximale Anzahl geöffneter Zeilen** (in der **Properties** -Auflistung des **Recordset** -Objekts). **CacheSize** kann nicht auf einen höheren Wert als **Maximale Anzahl geöffneter Zeilen** festgelegt werden. Legen Sie **Maximale Anzahl geöffneter Zeilen** fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.

Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgendem Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.

Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.

A **CacheSize** setting of zero is not allowed and returns an error.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.

Wenn **CacheSize** auf einen Wert größer als 1 festgelegt ist, können die Navigationsmethoden ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext und MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) zu einer Navigation zu einem gelöschten Datensatz führen, wenn nach dem Abrufen der Datensätze ein Löschvorgang erfolgt. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.

