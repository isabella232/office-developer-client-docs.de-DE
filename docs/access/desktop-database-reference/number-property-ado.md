---
title: Number-Eigenschaft (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288574"
---
# <a name="number-property-ado"></a>Number-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013

Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long**-Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.

## <a name="remarks"></a>Bemerkungen

Ermitteln Sie mit der **Number**-Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.

Die [Errors](errors-collection-ado.md)-Auflistung gibt ein HRESULT im Hexadezimalformat (z. B. 0x80004005) oder einen Long-Wert (beispielsweise 2147467259) zurück. Diese HRESULTs können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden. Weitere Informationen zu diesen Zahlen finden Sie in Kapitel 16 von *OLE DB Programmer's Reference*.

