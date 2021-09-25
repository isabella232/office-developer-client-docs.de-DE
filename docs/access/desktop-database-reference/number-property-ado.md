---
title: Number-Eigenschaft (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6707072a61f6be3538e8c0365383584802858981
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597170"
---
# <a name="number-property-ado"></a>Number-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long**-Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.

## <a name="remarks"></a>HinwBemerkungeneise

Ermitteln Sie mit der **Number**-Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.

Die [Errors](errors-collection-ado.md)-Auflistung gibt ein HRESULT im Hexadezimalformat (z. B. 0x80004005) oder einen Long-Wert (beispielsweise 2147467259) zurück. Diese HRESULTs können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden. Weitere Informationen zu diesen Zahlen finden Sie in Kapitel 16 von *OLE DB Programmer's Reference*.

