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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301134"
---
# <a name="provider-property-ado"></a>Provider-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String**-Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>Bemerkungen

Use the **Provider** property to set or return the name of the provider for a connection. Diese Eigenschaft kann auch durch den Inhalt der [ConnectionString](connectionstring-property-ado.md) -Eigenschaft oder des *ConnectionString* -Arguments der [Open](open-method-ado-connection.md) -Methode festgelegt werden. die Angabe eines Anbieters an mehreren Stellen beim Aufrufen der **Open** -Methode kann jedoch zu unvorhersehbaren Ergebnissen führen. Wenn kein Anbieter angegeben wird, wird die Eigenschaft standardmäßig auf MSDASQL ([Microsoft OLE DB-Anbieter für ODBC](microsoft-ole-db-provider-for-odbc.md)) festgelegt.

Die **Provider**-Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection**-Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.

