---
title: Attributes-Eigenschaft (ADO)
TOCTitle: Attributes property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 0edebe425b025e3b3497640a7e436b5996493dae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558884"
---
# <a name="attributes-property-ado"></a>Attributes-Eigenschaft (ADO)


**Gilt für**: Access 2013, Office 2013


## <a name="attributes-property"></a>Attributes-Eigenschaft

Gibt mindestens ein Merkmal eines Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.

For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).

Für ein [Parameter](parameter-object-ado.md)-Objekt weist die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem [ParameterAttributesEnum](parameterattributesenum.md)-Wert sein. Der Standard ist **adParamSigned**.

Für ein [Field](field-object-ado.md)-Objekt kann die **Attributes** -Eigenschaft die Summe von mindestens einem [FieldAttributeEnum](fieldattributeenum.md)-Wert sein. Sie ist normalerweise schreibgeschützt. Für neue **Field** -Objekte, die an die [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, weist jedoch die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt angegeben wurde und das neue **Field** -Objekt vom Datenprovider durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung erfolgreich hinzugefügt wurde.

Für ein [Property](property-object-ado.md)-Objekt ist die **Attributes**-Eigenschaft schreibgeschützt, und ihr Wert kann die Summe von mindestens einem [PropertyAttributesEnum](propertyattributesenum.md)-Wert sein.

## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe der **Attributes**-Eigenschaft können Sie Merkmale von **Connection**-Objekten, **Parameter**-Objekten, [Field](field-object-ado.md)-Objekten oder [Property](property-object-ado.md)-Objekten festlegen oder zurückgeben.

Wenn Sie mehrere Attribute festlegen, können Sie die entsprechenden Konstanten addieren. Ein Fehler wird erzeugt, wenn Sie als Eigenschaftswert eine Summe festlegen, die inkompatible Konstanten enthält.

**Remote data service usage** Diese Eigenschaft ist für ein clientseitiges **Connection-Objekt** nicht verfügbar.

