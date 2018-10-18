---
title: CreateParameter-Methode (ADO)
TOCTitle: CreateParameter Method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 00a2c5e2eb8613434b80c80e2a51cbf5d1deb644
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605485"
---
# <a name="createparameter-method-ado"></a>CreateParameter-Methode (ADO)


**Betrifft**: Access 2013 | Office 2013


Erstellt ein neues [Parameter](parameter-object-ado.md)-Objekt mit den angegebenen Eigenschaften.

## <a name="syntax"></a>Syntax

**Festlegen** *Parameter*  =  *Befehl*. "CreateParameter" (*Name*, *Typ*, *Richtung*, *Größe*, *Wert*)

<<<<<<< Kopf
## <a name="return-value"></a>Rückgabewert
=======
## <a name="return-value"></a>Rückgabewert
>>>>>>> master

Gibt ein **Parameter** -Objekt zurück.

## <a name="parameters"></a>Parameter

  - *Name*

  - Optional. Ein **String** -Wert, der den Namen des **Parameter** -Objekts enthält.

  - *Type*

  - Optional. Ein [DataTypeEnum](datatypeenum.md)-Wert, der den Datentyp des **Parameter** -Objekts angibt.

  - *Direction*

  - Optional. Ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert, der den Typ des **Parameter** -Objekts angibt.

  - *Size*

  - Optional. Ein **Long** -Wert, der die maximale Länge des Parameterwerts in Zeichen oder Bytes angibt.

  - *Wert*

  - Optional. Ein **Variant** -Wert, der den Wert für das **Parameter** -Objekt angibt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CreateParameter** -Methode, um ein neues **Parameter** -Objekt mit einem angegebenen Namen, Typ, einer angegebenen Lesefolge und Größe sowie einem angegeben Wert zu erstellen. In Argumenten übergebene Werte werden in die entsprechenden **Parameter** -Eigenschaften geschrieben.

Diese Methode fügt das **Parameter** -Objekt nicht automatisch der **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts hinzu. Dadurch können Sie zusätzliche Eigenschaften festlegen, deren Werte ADO validiert, wenn Sie das **Parameter** -Objekt der Auflistung anfügen.

Wenn Sie einen Datentyp variabler Länge im *Argument* angeben, müssen Sie eine *Größe* -Argument übergeben oder die [Size](size-property-ado.md) -Eigenschaft des **Parameter** -Objekts festlegen, bevor er an der **Parameters** -Auflistung angefügt; andernfalls, tritt ein Fehler auf.

Wenn Sie im Argument *Type* einen numerischen Datentyp (**adNumeric** oder **adDecimal**) angeben, müssen Sie auch die Eigenschaften [NumericScale](numericscale-property-ado.md) und [Precision](precision-property-ado.md) festlegen.

