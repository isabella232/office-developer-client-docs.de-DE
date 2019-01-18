---
title: MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methode (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5631ce68a0479146e15ba74b41af5669d86175a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716033"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a>MoveFirst-, MoveLast-, MoveNext- und MovePrevious-Methode (RDS)

**Betrifft**: Access 2013, Office 2013

Wechselt zum ersten, letzten, nächsten oder vorherigen Datensatz in einem angegebenen [Recordset](recordset-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*DataControl*. Recordset-Objekt. { MoveFirst | MoveLast | MoveNext | MovePrevious}

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*DataControl* |Eine Objektvariable, die ein [RDS.DataControl](datacontrol-object-rds.md)-Objekt darstellt.|

## <a name="remarks"></a>Hinweise

Sie können die **Move** -Methoden verwenden, mit der **RDS. DataControl** Objekt, das durch die Datensätze in der datengebundene Steuerelemente auf einer Webseite zu navigieren. 

Angenommen Sie, dass Sie ein **Recordset** in einem Raster durch Bindung an ein **RDS. anzeigen DataControl** Objekt. Sie können dann ersten, letzten, weiter und vorherige Schaltflächen, mit denen Benutzer, um diese Move zum ersten, letzten, nächsten klicken, einschließen oder vorherigen Datensatz im **Recordset**angezeigt. Zu diesem Zweck Aufrufen der **Methoden MoveFirst**, **MoveLast**, **MoveNext**und **MovePrevious** -Methoden des der **RDS. DataControl** jeweils in den OnClick-Verfahren für die ersten, letzten, weiter und zurück-Tasten-Objekts. Der [Adressbuch-Beispiel](address-book-navigation-buttons.md) zeigt, wie dazu.

