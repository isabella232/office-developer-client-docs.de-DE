---
<span data-ttu-id="50f05-101"><<<<<<< HEAD-Titel: Attributes-Eigenschaft (ADO) TOCTitle: Attributes-Eigenschaft (ADO) === Titel: Attributes-Eigenschaft (ADO) TOCTitle: Attributes-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="50f05-101"><<<<<<< HEAD title: Attributes Property (ADO) TOCTitle: Attributes Property (ADO) ======= title: Attributes property (ADO) TOCTitle: Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="50f05-102">Master Ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) Ms:contentKeyID: 48544716 ms.date: 09/18/2015 Mtps_version: Office. 15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="50f05-102">master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="50f05-103">ado210.chm1231117 f1_categories:</span><span class="sxs-lookup"><span data-stu-id="50f05-103">ado210.chm1231117 f1_categories:</span></span>
- <span data-ttu-id="50f05-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="50f05-104">Office.Version=v15</span></span>
---

<span data-ttu-id="50f05-105"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="50f05-105"><<<<<<< HEAD</span></span>
# <a name="attributes-property-ado"></a><span data-ttu-id="50f05-106">Attributes-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="50f05-106">Attributes Property (ADO)</span></span>
=======
# <a name="attributes-property-ado"></a><span data-ttu-id="50f05-107">Attributes-Eigenschaft (ADO)</span><span class="sxs-lookup"><span data-stu-id="50f05-107">Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="50f05-108">master</span><span class="sxs-lookup"><span data-stu-id="50f05-108">master</span></span>


<span data-ttu-id="50f05-109">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="50f05-109">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="50f05-110">Attributes-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="50f05-110">Attributes Property</span></span>

<span data-ttu-id="50f05-111">Gibt mindestens ein Merkmal eines Objekts an.</span><span class="sxs-lookup"><span data-stu-id="50f05-111">Indicates one or more characteristics of an object.</span></span>

<span data-ttu-id="50f05-112"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="50f05-112"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="50f05-113">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="50f05-113">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="50f05-114">Einstellungen und Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="50f05-114">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="50f05-115">master</span><span class="sxs-lookup"><span data-stu-id="50f05-115">master</span></span>

<span data-ttu-id="50f05-116">Mit dieser Eigenschaft wird ein Wert vom Datentyp **Long** festgelegt oder zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50f05-116">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="50f05-p101">Für ein Connection-Objekt weist die Attributes-Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem XactAttributeEnum-Wert sein. Der Standard ist 0.</span><span class="sxs-lookup"><span data-stu-id="50f05-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="50f05-p102">Für ein [Parameter](parameter-object-ado.md)-Objekt weist die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, und ihr Wert kann die Summe von mindestens einem [ParameterAttributesEnum](parameterattributesenum.md)-Wert sein. Der Standard ist **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="50f05-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="50f05-p103">Für ein [Field](field-object-ado.md)-Objekt kann die **Attributes** -Eigenschaft die Summe von mindestens einem [FieldAttributeEnum](fieldattributeenum.md)-Wert sein. Sie ist normalerweise schreibgeschützt. Für neue **Field** -Objekte, die an die [Fields](fields-collection-ado.md)-Auflistung eines [Record](record-object-ado.md)-Objekts angefügt wurden, weist jedoch die **Attributes** -Eigenschaft Lese-/Schreibzugriff auf, nachdem die [Value](value-property-ado.md)-Eigenschaft für das **Field** -Objekt angegeben wurde und das neue **Field** -Objekt vom Datenprovider durch Aufrufen der [Update](update-method-ado.md)-Methode der **Fields** -Auflistung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="50f05-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="50f05-123">Für ein [Property](property-object-ado.md)-Objekt ist die **Attributes** -Eigenschaft schreibgeschützt, und ihr Wert kann die Summe von mindestens einem [PropertyAttributesEnum](propertyattributesenum.md)-Wert sein.</span><span class="sxs-lookup"><span data-stu-id="50f05-123">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="50f05-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50f05-124">Remarks</span></span>

<span data-ttu-id="50f05-125">Mithilfe der **Attributes** -Eigenschaft können Sie Merkmale von **Connection** -Objekten, **Parameter** -Objekten, [Field](field-object-ado.md)-Objekten oder [Property](property-object-ado.md)-Objekten festlegen oder zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="50f05-125">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="50f05-p104">Wenn Sie mehrere Attribute festlegen, können Sie die entsprechenden Konstanten addieren. Ein Fehler wird erzeugt, wenn Sie als Eigenschaftswert eine Summe festlegen, die inkompatible Konstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="50f05-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="50f05-128">**Remote Data Service-Verwendung** Diese Eigenschaft ist nicht verfügbar für ein clientseitiges **Connection** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="50f05-128">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

