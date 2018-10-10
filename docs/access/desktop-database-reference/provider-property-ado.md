---
title: Provider-Eigenschaft (ADO)
TOCTitle: Provider Property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 890f80534ff47c4dea67b34f345bce0f90328c60
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472623"
---
# <a name="provider-property-ado"></a>Provider-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String** -Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Hinweise

Verwenden Sie die Provider-Eigenschaft, um den Namen des Anbieters für eine Verbindung festzulegen oder zurückzugeben. Diese Eigenschaft kann mit dem Inhalt der ConnectionString-Eigenschaft oder dem Argument ConnectionString der Open-Methode festgelegt werden. Wenn Sie jedoch einen Anbieter an mehreren Stellen angeben und die Open-Methode aufrufen, kann das zu unerwarteten Ergebnissen führen. Wird kein Anbieter angegeben, gilt der Standardwert MSDASQL für diese Eigenschaft (Microsoft OLE DB-Anbieter für ODBC).

Die **Provider** -Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection** -Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection** -Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.

