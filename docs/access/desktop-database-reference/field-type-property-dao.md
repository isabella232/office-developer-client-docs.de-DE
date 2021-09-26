---
title: Field.Type-Eigenschaft (DAO)
TOCTitle: Type Property
description: Typ-Eigenschaft
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 082f6b34965ae90c99efd8d8cf3ac34d2cfc5dfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581294"
---
# <a name="fieldtype-property-dao"></a>Field.Type-Eigenschaft (DAO)


**Gilt für**: Access 2013, Office 2013

Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück. Lesen/Schreiben **Ganzzahl**.

## <a name="syntax"></a>Syntax

*expression* .Type

*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.

## <a name="remarks"></a>Bemerkungen

Der Einstellungs- oder Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Für ein **Field** -Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt an eine Auflistung oder ein anderes Objekt angefügt wird; anschließend ist sie schreibgeschützt.

Die möglichen Einstellungs- und Rückgabewerte für ein **Field** -Objekt werden in der folgenden Tabelle beschrieben.

|**Konstante**|**Wert**|**Beschreibung**|
|:----------|:----------|:----------|
|**dbBigInt**|16|Große Ganzzahl|
|**dbBinary**|9|Binär|
|**dbBoolean**|1|Boolesch|
|**dbByte**|2|Byte|
|**dbChar**|18|Char|
|**dbCurrency**|5|Währung|
|**dbDate**|8|Datum/Uhrzeit|
|**dbDecimal**|20|Decimal|
|**dbDouble**|7|Gleitkommawert mit doppelter Genauigkeit|
|**dbFloat**|21|Gleitkommazahl|
|**dbGUID**|15|GUID|
|**dbInteger**|3|Ganze Zahl|
|**dbLong**|4|Long|
|**dbLongBinary**|11|Langer Binärwert (OLE-Objekt)|
|**dbMemo**|12|Memo|
|**dbNumeric**|19|Numeric|
|**dbSingle**|6|Single|
|**dbText**|10|Text|
|**dbTime**|22|Time|
|**dbTimeStamp**|23|Zeitstempel|
|**dbVarBinary**|17|VarBinary|

Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.
