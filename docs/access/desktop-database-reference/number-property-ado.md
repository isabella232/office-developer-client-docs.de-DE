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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707471"
---
# <a name="number-property-ado"></a>Number-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013

Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.

## <a name="remarks"></a>Hinweise

Ermitteln Sie mit der **Number** -Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.

Die [Errors](errors-collection-ado.md) -Auflistung gibt ein HRESULT im Hexadezimal-Format (beispielsweise 0 x 80004005) oder long-Wert (beispielsweise 2147467259) zurück. Diese HRESULT-Werte können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden. Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 von der *OLE DB-Programmierreferenz.*

