---
title: Attributes-Eigenschaft (ADO)
TOCTitle: Attributes Property (ADO)
ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15)
ms:contentKeyID: 48544716
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231117
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 9fa17593a5606d288e519969ff63f10a1df229ba
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473242"
---
# <a name="attributes-property-ado"></a><span data-ttu-id="39247-102">Attributes-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="39247-102">Attributes Property (ADO)</span></span>


<span data-ttu-id="39247-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="39247-103">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="39247-104">Attributes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="39247-104">Attributes Property</span></span>

<span data-ttu-id="39247-105">Gibt mindestens ein Merkmal eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="39247-105">Indicates one or more characteristics of an object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="39247-106">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="39247-106">Settings and Return Values</span></span>

<span data-ttu-id="39247-107">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39247-107">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="39247-p101">Für ein Connection-Objekt weist die Attributes-Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem XactAttributeEnum-Wert sein. Der Standard ist 0.</span><span class="sxs-lookup"><span data-stu-id="39247-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="39247-p102">Für ein [Parameter](parameter-object-ado.md)-Objekt weist die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem [ParameterAttributesEnum](parameterattributesenum.md)-Wert sein. Der Standard ist **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="39247-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="39247-p103">Für ein [Field](field-object-ado.md)-Objekt kann die **Attributes** -Eigenschaft die Summe von mindestens einem [FieldAttributeEnum](fieldattributeenum.md)-Wert sein. Sie ist normalerweise schreibgeschützt. Für neue **Field** -Objekte, die an die [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, weist jedoch die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt angegeben wurde und das neue **Field** -Objekt vom Datenprovider durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="39247-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="39247-114">Für ein [Property](property-object-ado.md)-Objekt ist die **Attributes** -Eigenschaft schreibgeschützt, und ihr Wert kann die Summe von mindestens einem [PropertyAttributesEnum](propertyattributesenum.md)-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="39247-114">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="39247-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="39247-115">Remarks</span></span>

<span data-ttu-id="39247-116">Mithilfe der **Attributes** -Eigenschaft können Sie Merkmale von **Connection** -Objekten, **Parameter** -Objekten, [Field](field-object-ado.md)-Objekten oder [Property](property-object-ado.md)-Objekten festlegen oder zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="39247-116">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="39247-p104">Wenn Sie mehrere Attribute festlegen, können Sie die entsprechenden Konstanten addieren. Ein Fehler wird erzeugt, wenn Sie als Eigenschaftswert eine Summe festlegen, die inkompatible Konstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="39247-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="39247-119">**Remote Data Service-Verwendung** Diese Eigenschaft ist nicht verfügbar für ein clientseitiges **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="39247-119">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

