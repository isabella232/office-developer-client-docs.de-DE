---
title: CreateParameter-Methode (ADO)
TOCTitle: CreateParameter method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fa060811f60379e720e06be9f94e9403477c7869
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295394"
---
# <a name="createparameter-method-ado"></a>CreateParameter-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Erstellt ein neues [Parameter](parameter-object-ado.md)-Objekt mit den angegebenen Eigenschaften.

## <a name="syntax"></a>Syntax

**Festgelegt** *Parameter*  =  *Befehl*aus. CreateParameter (*Name*, *Typ*, *Richtung*, *Größe*, *Wert*)

## <a name="return-value"></a>Rückgabewert

Gibt ein **Parameter**-Objekt zurück.

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Name* |Optional. Ein **String** -Wert, der den Namen des **Parameter** -Objekts enthält.|
|*Type* |Optional. Ein [DataTypeEnum](datatypeenum.md)-Wert, der den Datentyp des **Parameter** -Objekts angibt.|
|*Direction* |Optional. Ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert, der den Typ des **Parameter** -Objekts angibt.|
|*Size* |Optional. Ein **Long** -Wert, der die maximale Länge des Parameterwerts in Zeichen oder Bytes angibt.|
|*Wert* |Optional. Ein **Variant** -Wert, der den Wert für das **Parameter** -Objekt angibt.|

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die **CreateParameter** -Methode, um ein neues **Parameter** -Objekt mit einem angegebenen Namen, Typ, einer angegebenen Lesefolge und Größe sowie einem angegeben Wert zu erstellen. In Argumenten übergebene Werte werden in die entsprechenden **Parameter** -Eigenschaften geschrieben.

Diese Methode fügt das **Parameter** -Objekt nicht automatisch der **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts hinzu. Dadurch können Sie zusätzliche Eigenschaften festlegen, deren Werte ADO validiert, wenn Sie das **Parameter** -Objekt der Auflistung anfügen.

Wenn Sie im Argument *Type* einen Datentyp mit variabler Länge festlegen, müssen Sie ein Argument *Size* übergeben oder die [Size](size-property-ado.md)-Eigenschaft des **Parameter**-Objekts festlegen, bevor Sie der **Parameters**-Auflistung das Argument anfügen. Andernfalls tritt ein Fehler auf.

Wenn Sie im Argument *Type* einen numerischen Datentyp (**adNumeric** oder **adDecimal**) angeben, müssen Sie auch die Eigenschaften [NumericScale](numericscale-property-ado.md) und [Precision](precision-property-ado.md) festlegen.

