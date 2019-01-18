---
title: GetChildren-Methode (ADO)
TOCTitle: GetChildren method (ADO)
ms:assetid: 998cf640-ffc7-51e1-4d1e-4797f7cdea4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249687(v=office.15)
ms:contentKeyID: 48546515
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4ca8c113a377543ea8624972adb5958612a3fc72
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722025"
---
# <a name="getchildren-method-ado"></a>GetChildren-Methode (ADO)


**Betrifft**: Access 2013, Office 2013


Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, dessen Zeilen die untergeordneten Elemente einer Auflistung eines [Record](record-object-ado.md) darstellen.

## <a name="syntax"></a>Syntax

**Festlegen** *Recordset-Objekt*  =  *Datensatz*. GetChildren

## <a name="return-value"></a>Rückgabewert

Ein **Recordset** -Objekt, bei dem jede Zeile ein untergeordnetes Element des aktuellen **Record** -Objekts darstellt. Das untergeordnete Element eines **Record**, der ein Verzeichnis darstellt, sind beispielsweise die Dateien und Unterverzeichnisse innerhalb des übergeordneten Verzeichnisses.

## <a name="remarks"></a>Hinweise

Der Anbieter bestimmt, welche Spalten im zurückgegebenen **Recordset** -Objekt vorhanden sind. Ein Anbieter für Dokumentquellen gibt beispielsweise immer ein **Recordset** -Ressourcenobjekt zurück.

