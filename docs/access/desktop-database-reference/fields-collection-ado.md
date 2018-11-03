---
title: Fields-Auflistung (ADO)
TOCTitle: Fields collection (ADO)
ms:assetid: 029aa738-8726-54a6-1813-b152813948bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248791(v=office.15)
ms:contentKeyID: 48542962
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39c801e223eba83a8de6aa7dacda6d8296e77588
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936973"
---
# <a name="fields-collection-ado"></a>Fields-Auflistung (ADO)


**Betrifft**: Access 2013, Office 2013

Enthält alle [Field](field-object-ado.md)-Objekte eines [Recordset](recordset-object-ado.md)- oder [Record](record-object-ado.md)-Objekts.

## <a name="remarks"></a>Hinweise

Ein **Recordset** -Objekt besitzt eine **Fields** -Auflistung, die aus **Field** -Objekten besteht. Jedes **Field** -Objekt entspricht einer Spalte im **Recordset** -Objekt. Sie können die **Fields** -Auflistung auffüllen, bevor Sie das **Recordset** -Objekt öffnen, indem Sie die [Refresh](refresh-method-ado.md)-Methode der Auflistung aufrufen.

> [!NOTE]
> [!HINWEIS] Eine detaillierte Beschreibung der Verwendung der **Field** -Objekte finden Sie in der Beschreibung des **Field** -Objekts.

Die **Fields** -Auflistung verfügt über die [Append](append-method-ado.md)-Methode, die ein **Field** -Objekt provisorisch erstellt und der Auflistung hinzufügt, sowie die **Update** -Methode, die Hinzufügungen und Löschungen fertig stellt.

Ein **Record** -Objekt hat zwei spezielle Felder, die mit [FieldEnum](fieldenum.md)-Konstanten indiziert werden können. Eine Konstante greift auf ein Feld zu, das den Standarddatenstrom für das **Record** -Objekt erstellt. Die andere Konstante greift auf ein Feld zu, das die absolute URL-Zeichenfolge für das **Record** -Objekt enthält.

Bestimmte Anbieter (z. B. der [Microsoft OLE DB Provider für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)) füllen die **Fields** -Auflistung mit einer Teilmenge der verfügbaren Felder für das **Record** - oder **Recordset** -Objekt auf. Andere Felder werden der Auflistung erst dann hinzugefügt, wenn im Code namentlich auf sie verwiesen wird oder sie indiziert werden.

Wenn Sie versuchen, auf ein nicht vorhandenes Feld namentlich zu verweisen, wird ein neues **Field** -Objekt an die **Fields** -Auflistung angehängt. Die [Status](status-property-ado-field.md)-Eigenschaft des Objekts hat den Wert **adFieldPendingInsert**. Wenn Sie [Update](update-method-ado.md) aufrufen, erstellt ADO ein neues Feld in der Datenquelle, sofern dies vom Anbieter zugelassen wird.

