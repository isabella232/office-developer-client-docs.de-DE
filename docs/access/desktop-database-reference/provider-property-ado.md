---
title: Provider-Eigenschaft (ADO)
TOCTitle: Provider property (ADO)
ms:assetid: 1b795f51-93d7-431c-b1fe-0db95f69a56a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248953(v=office.15)
ms:contentKeyID: 48543543
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: e63ec7813a1bc446502900de75369c9c42afd709
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565079"
---
# <a name="provider-property-ado"></a>Provider-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt den Namen des Anbieters für ein [Connection](connection-object-ado.md)-Objekt an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Legt einen **String**-Wert fest, der den Namen des Anbieters angibt, oder gibt den Wert zurück.

## <a name="remarks"></a>HinwBemerkungeneise

Use the **Provider** property to set or return the name of the provider for a connection. Diese Eigenschaft kann auch durch den Inhalt der [ConnectionString-Eigenschaft](connectionstring-property-ado.md) oder das *ConnectionString-Argument* der [Open-Methode](open-method-ado-connection.md) festgelegt werden. Das Angeben eines Anbieters an mehreren Stellen beim Aufrufen der **Open-Methode** kann jedoch zu unvorhersehbaren Ergebnissen führen. Wenn kein Anbieter angegeben ist, wird die Eigenschaft standardmäßig auf MSDASQL ([Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)) festgelegt.

Die **Provider**-Eigenschaft ist nicht schreibgeschützt, wenn die Verbindung geschlossen ist, und schreibgeschützt, wenn sie geöffnet ist. Die Einstellung wird erst wirksam, wenn Sie das **Connection**-Objekt öffnen oder auf die [Properties](properties-collection-ado.md)-Auflistung des **Connection**-Objekts zugreifen. Ist die Einstellung nicht gültig, tritt ein Fehler auf.

