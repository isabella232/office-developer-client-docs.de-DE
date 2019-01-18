---
title: Provider-Eigenschaft (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e640fb6131919cbdf88fbbf8229c62d0e2e4e13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719554"
---
# <a name="provider-property-ado"></a>Provider-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String** -Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die Provider-Eigenschaft, um den Namen des Anbieters für eine Verbindung festzulegen oder zurückzugeben. Diese Eigenschaft kann mit dem Inhalt der ConnectionString-Eigenschaft oder dem Argument ConnectionString der Open-Methode festgelegt werden. Wenn Sie jedoch einen Anbieter an mehreren Stellen angeben und die Open-Methode aufrufen, kann das zu unerwarteten Ergebnissen führen. Wird kein Anbieter angegeben, gilt der Standardwert MSDASQL für diese Eigenschaft (Microsoft OLE DB-Anbieter für ODBC).

Die **Provider** -Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection** -Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.

