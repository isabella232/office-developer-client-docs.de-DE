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
ms.openlocfilehash: ea253515a673f0f941032e2920d84c7ebf68f1bf
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874818"
---
# <a name="attributes-property-ado"></a>Attributes-Eigenschaft (ADO)


**Betrifft**: Access 2013, Office 2013


## <a name="attributes-property"></a>Attributes-Eigenschaft

Gibt mindestens ein Merkmal eines Objekts an.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.

Für ein Connection-Objekt weist die Attributes-Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem XactAttributeEnum-Wert sein. Der Standard ist 0.

Für ein [Parameter](parameter-object-ado.md)-Objekt weist die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem [ParameterAttributesEnum](parameterattributesenum.md)-Wert sein. Der Standard ist **adParamSigned**.

Für ein [Field](field-object-ado.md)-Objekt kann die **Attributes** -Eigenschaft die Summe von mindestens einem [FieldAttributeEnum](fieldattributeenum.md)-Wert sein. Sie ist normalerweise schreibgeschützt. Für neue **Field** -Objekte, die an die [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, weist jedoch die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt angegeben wurde und das neue **Field** -Objekt vom Datenprovider durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung erfolgreich hinzugefügt wurde.

Für ein [Property](property-object-ado.md)-Objekt ist die **Attributes** -Eigenschaft schreibgeschützt, und ihr Wert kann die Summe von mindestens einem [PropertyAttributesEnum](propertyattributesenum.md)-Wert sein.

## <a name="remarks"></a>Hinweise

Mithilfe der **Attributes** -Eigenschaft können Sie Merkmale von **Connection** -Objekten, **Parameter** -Objekten, [Field](field-object-ado.md)-Objekten oder [Property](property-object-ado.md)-Objekten festlegen oder zurückgeben.

Wenn Sie mehrere Attribute festlegen, können Sie die entsprechenden Konstanten addieren. Ein Fehler wird erzeugt, wenn Sie als Eigenschaftswert eine Summe festlegen, die inkompatible Konstanten enthält.

**Remote Data Service-Verwendung** Diese Eigenschaft ist nicht verfügbar für ein clientseitiges **Connection** -Objekt.

