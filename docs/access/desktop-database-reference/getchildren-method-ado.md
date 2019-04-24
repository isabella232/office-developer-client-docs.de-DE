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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292307"
---
# <a name="getchildren-method-ado"></a>GetChildren-Methode (ADO)


**Gilt für**: Access 2013, Office 2013


Gibt ein [Recordset](recordset-object-ado.md)-Objekt zurück, dessen Zeilen die untergeordneten Elemente einer Auflistung eines [Record](record-object-ado.md) darstellen.

## <a name="syntax"></a>Syntax

**Festgelegt** *Recordset*  =  *Record*. GetChildren

## <a name="return-value"></a>Rückgabewert

Ein **Recordset** -Objekt, bei dem jede Zeile ein untergeordnetes Element des aktuellen **Record** -Objekts darstellt. Das untergeordnete Element eines **Record**, der ein Verzeichnis darstellt, sind beispielsweise die Dateien und Unterverzeichnisse innerhalb des übergeordneten Verzeichnisses.

## <a name="remarks"></a>Bemerkungen

Der Anbieter bestimmt, welche Spalten im zurückgegebenen **Recordset**-Objekt vorhanden sind. Ein Anbieter für Dokumentquellen gibt beispielsweise immer ein **Recordset**-Ressourcenobjekt zurück.

