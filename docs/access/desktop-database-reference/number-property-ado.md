---
title: Number-Eigenschaft (ADO)
TOCTitle: Number Property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4e9b048643b1892197f610ef6d53e6ba46b170d8
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472643"
---
# <a name="number-property-ado"></a>Number-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt die Nummer an, durch die ein [Error](error-object-ado.md)-Objekt eindeutig identifiziert wird.

## <a name="return-value"></a>Rückgabewert

Gibt einen **Long** -Wert zurück, der einer der [ErrorValueEnum](errorvalueenum.md)-Konstanten entsprechen kann.

## <a name="remarks"></a>Hinweise

Ermitteln Sie mit der **Number** -Eigenschaft, welcher Fehler aufgetreten ist. Der Wert der Eigenschaft ist eine eindeutige Zahl, die der Fehlerbedingung entspricht.

Die [Errors](errors-collection-ado.md) -Auflistung gibt ein HRESULT im Hexadezimal-Format (beispielsweise 0 x 80004005) oder long-Wert (beispielsweise 2147467259) zurück. Diese HRESULT-Werte können von zugrunde liegenden Komponenten wie OLE DB oder direkt von OLE ausgelöst werden. Weitere Informationen zu diesen Nummern finden Sie in Kapitel 16 von der *OLE DB-Programmierreferenz.*

