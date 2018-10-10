---
title: Append-Methode (ADO)
TOCTitle: Append Method (ADO)
ms:assetid: cca133af-2b95-877d-0488-0d99631623f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250014(v=office.15)
ms:contentKeyID: 48547742
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b47b7b0514b78a89425e47962c36b092e35677ea
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474852"
---
# <a name="append-method-ado"></a><span data-ttu-id="3e696-102">Append-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="3e696-102">Append Method (ADO)</span></span>


<span data-ttu-id="3e696-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3e696-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3e696-p101">Ein Objekt wird einer Auflistung angefügt. Bei einer [Fields](fields-collection-ado.md)-Auflistung wird möglicherweise ein neues [Field](field-object-ado.md)-Objekt erstellt, bevor es der Auflistung angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="3e696-p101">Appends an object to a collection. If the collection is [Fields](fields-collection-ado.md), a new [Field](field-object-ado.md) object may be created before it is appended to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e696-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e696-106">Syntax</span></span>

<span data-ttu-id="3e696-107">*Auflistung*. Fügen Sie *-Objekt*</span><span class="sxs-lookup"><span data-stu-id="3e696-107">*collection*.Append *object*</span></span>

<span data-ttu-id="3e696-108">*Felder*. *Name*, *Typ*, *DefinedSize*, *Attrib*, *FieldValue* Anfügen</span><span class="sxs-lookup"><span data-stu-id="3e696-108">*fields*.Append *Name*, *Type*, *DefinedSize*, *Attrib*, *FieldValue*</span></span>

## <a name="parameters"></a><span data-ttu-id="3e696-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e696-109">Parameters</span></span>

  - <span data-ttu-id="3e696-110">*collection*</span><span class="sxs-lookup"><span data-stu-id="3e696-110">*collection*</span></span>

  - <span data-ttu-id="3e696-111">Ein Collection-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3e696-111">A collection object.</span></span>

  - <span data-ttu-id="3e696-112">*fields*</span><span class="sxs-lookup"><span data-stu-id="3e696-112">*fields*</span></span>

  - <span data-ttu-id="3e696-113">Eine **Fields** -Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3e696-113">A **Fields** collection.</span></span>

  - <span data-ttu-id="3e696-114">*Objekt*</span><span class="sxs-lookup"><span data-stu-id="3e696-114">*object*</span></span>

  - <span data-ttu-id="3e696-115">Eine Objektvariable, durch die das anzufügende Objekt dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3e696-115">An object variable that represents the object to be appended.</span></span>

  - <span data-ttu-id="3e696-116">*Name*</span><span class="sxs-lookup"><span data-stu-id="3e696-116">*Name*</span></span>

  - <span data-ttu-id="3e696-117">Ein **String**-Wert, der den Namen des neuen **Field**-Objekts enthält und nicht mit dem Namen eines anderen Objekts in *fields* übereinstimmen darf.</span><span class="sxs-lookup"><span data-stu-id="3e696-117">A **String** value that contains the name of the new **Field** object, and must not be the same name as any other object in *fields*.</span></span>

  - <span data-ttu-id="3e696-118">*Type*</span><span class="sxs-lookup"><span data-stu-id="3e696-118">*Type*</span></span>

  - <span data-ttu-id="3e696-p102">Ein [DataTypeEnum](datatypeenum.md)-Wert, dessen Standardwert **adEmpty** ist und durch den der Datentyp des neuen Felds angegeben wird. Die folgenden Datentypen werden von ADO nicht unterstützt und sollten beim Anfügen neuer Felder an ein **Recordset** nicht verwendet werden: **adIDispatch**, **adIUnknown**, **adVariant**.</span><span class="sxs-lookup"><span data-stu-id="3e696-p102">A [DataTypeEnum](datatypeenum.md) value, whose default value is **adEmpty**, that specifies the data type of the new field. The following data types are not supported by ADO, and should not be used when appending new fields to a **Recordset**: **adIDispatch**, **adIUnknown**, **adVariant**.</span></span>

  - <span data-ttu-id="3e696-121">*DefinedSize*</span><span class="sxs-lookup"><span data-stu-id="3e696-121">*DefinedSize*</span></span>

  - <span data-ttu-id="3e696-p103">Optional. Ein Long-Wert, durch den die definierte Größe des neuen Felds in Zeichen oder Byte dargestellt wird. Der Standardwert für diesen Parameter wird von Type abgeleitet. Felder mit einem DefinedSize-Wert von mehr als 255 Bytes werden als Spalten mit variabler Länge behandelt. (Der Standardwert für DefinedSize ist nicht angegeben.)</span><span class="sxs-lookup"><span data-stu-id="3e696-p103">Optional. A **Long** value that represents the defined size, in characters or bytes, of the new field. The default value for this parameter is derived from *Type*. Fields with a DefinedSize greater than 255 bytes, and treated as variable length columns. (The default *DefinedSize* is unspecified.)</span></span>

  - <span data-ttu-id="3e696-127">*Attrib*</span><span class="sxs-lookup"><span data-stu-id="3e696-127">*Attrib*</span></span>

  - <span data-ttu-id="3e696-p104">Optional. Ein [FieldAttributeEnum](fieldattributeenum.md)-Wert, dessen Standardwert **adFldDefault** ist und durch den Attribute für das neue Feld angegeben werden. Wenn dieser Wert nicht angegeben ist, enthält das Feld von *Type* abgeleitete Werte.</span><span class="sxs-lookup"><span data-stu-id="3e696-p104">Optional. A [FieldAttributeEnum](fieldattributeenum.md) value, whose default value is **adFldDefault**, that specifies attributes for the new field. If this value is not specified, the field will contain attributes derived from *Type*.</span></span>

  - <span data-ttu-id="3e696-131">*FieldValue*</span><span class="sxs-lookup"><span data-stu-id="3e696-131">*FieldValue*</span></span>

  - <span data-ttu-id="3e696-p105">Optional. Ein **Variant** -Objekt, durch das der Wert für das neue Feld dargestellt wird. Wenn nichts angegeben ist, wird dem Feld ein Nullwert angefügt.</span><span class="sxs-lookup"><span data-stu-id="3e696-p105">Optional. A **Variant** that represents the value for the new field. If not specified, then the field is appended with a null value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e696-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e696-135">Remarks</span></span>

<span data-ttu-id="3e696-136">**Parameters-Auflistung**</span><span class="sxs-lookup"><span data-stu-id="3e696-136">**Parameters Collection**</span></span>

<span data-ttu-id="3e696-p106">Sie müssen die [Type](type-property-ado.md)-Eigenschaft eines [Parameter](parameter-object-ado.md)-Objekts festlegen, bevor Sie es der **Parameters** -Auflistung anfügen. Wenn Sie einen Datentyp mit variabler Länge auswählen, müssen Sie auch die [Size](size-property-ado.md)-Eigenschaft auf einen größeren Wert als Null festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e696-p106">You must set the [Type](type-property-ado.md) property of a [Parameter](parameter-object-ado.md) object before appending it to the **Parameters** collection. If you select a variable-length data type, you must also set the [Size](size-property-ado.md) property to a value greater than zero.</span></span>

<span data-ttu-id="3e696-p107">Indem Sie Parameter selbst beschreiben, minimieren Sie Aufrufe an den Anbieter und verbessern folglich die Leistung beim Verwenden gespeicherter Prozeduren oder parametrisierter Abfragen. Sie müssen jedoch die Eigenschaften der zur aufzurufenden gespeicherten Prozedur oder parametrisierten Abfrage zugeordneten Parameter kennen.</span><span class="sxs-lookup"><span data-stu-id="3e696-p107">Describing parameters yourself minimizes calls to the provider and consequently improves performance when using stored procedures or parameterized queries. However, you must know the properties of the parameters associated with the stored procedure or parameterized query that you want to call.</span></span>

<span data-ttu-id="3e696-p108">Verwenden Sie die [CreateParameter](createparameter-method-ado.md)-Methode, um **Parameter** -Objekte mit den entsprechenden Eigenschafteneinstellungen zu erstellen, und verwenden Sie die **Append** -Methode, um diese der [Parameters](parameters-collection-ado.md)-Auflistung hinzuzufügen. Auf diese Weise können Sie Parameterwerte festlegen und zurückgeben, ohne den Anbieter für die Parameterinformationen aufrufen zu müssen. Wenn Sie für einen Anbieter schreiben, von dem keine Parameterinformationen bereitgestellt werden, müssen Sie mit dieser Methode die **Parameters** -Auflistung manuell auffüllen, um überhaupt Parameter verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="3e696-p108">Use the [CreateParameter](createparameter-method-ado.md) method to create **Parameter** objects with the appropriate property settings and use the **Append** method to add them to the [Parameters](parameters-collection-ado.md) collection. This lets you set and return parameter values without having to call the provider for the parameter information. If you are writing to a provider that does not supply parameter information, you must use this method to manually populate the **Parameters** collection in order to use parameters at all.</span></span>

<span data-ttu-id="3e696-144">**Fields-Auflistung**</span><span class="sxs-lookup"><span data-stu-id="3e696-144">**Fields Collection**</span></span>

<span data-ttu-id="3e696-145">Der *FieldValue* -Parameter ist nur gültig, wenn ein **Field** -Objekt eines [Record](record-object-ado.md) -Objekts, um ein **Recordset** -Objekt nicht hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3e696-145">The *FieldValue* parameter is only valid when adding a **Field** object to a [Record](record-object-ado.md) object, not to a **Recordset** object.</span></span> <span data-ttu-id="3e696-146">Mit einem **Record** -Objekt können Sie gleichzeitig Felder anfügen und Werte bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3e696-146">With a **Record** object, you may append fields and provide values at the same time.</span></span> <span data-ttu-id="3e696-147">Bei einem **Recordset** -Objekt müssen Sie Felder erstellen, während das **Recordset** geschlossen ist, dann das **Recordset** öffnen und den Feldern Werte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="3e696-147">With a **Recordset** object, you must create fields while the **Recordset** is closed, then open the **Recordset** and assign values to the fields.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3e696-p110">Bei neuen <STRONG>Field</STRONG> -Objekten, die der <STRONG>Fields</STRONG>-Auflistung eines <STRONG>Record</STRONG>-Objekts angefügt wurden, muss die <A href="value-property-ado.md">Value</A> -Eigenschaft festgelegt werden, bevor andere <STRONG>Field</STRONG> -Eigenschaften angegeben werden. Zuerst müssen ein angegebener Wert für die <STRONG>Value</STRONG> -Eigenschaft zugewiesen und die <A href="update-method-ado.md">Update</A>-Methode für die <STRONG>Fields</STRONG> -Auflistung aufgerufen worden sein. Anschließend kann auf weitere Eigenschaften, wie z. B. <A href="type-property-ado.md">Type</A> oder <A href="attributes-property-ado.md">Attributes</A>, zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="3e696-p110">For new <STRONG>Field</STRONG> objects that have been appended to the <STRONG>Fields</STRONG> collection of a <STRONG>Record</STRONG> object, the <A href="value-property-ado.md">Value</A> property must be set before any other <STRONG>Field</STRONG> properties can be specified. First, a specific value for the <STRONG>Value</STRONG> property must have been assigned and <A href="update-method-ado.md">Update</A> on the <STRONG>Fields</STRONG> collection called. Then, other properties such as <A href="type-property-ado.md">Type</A> or <A href="attributes-property-ado.md">Attributes</A> can be accessed.</span></span></P>



<span data-ttu-id="3e696-p111">**Field**-Objekte der folgenden Datentypen (**DataTypeEnum**) können nicht der **Fields**-Auflistung angefügt werden und verursachen das Auftreten eines Fehlers: **adArray**, **adChapter**, **adEmpty**, **adPropVariant** und **adUserDefined**. Außerdem werden die folgenden Datentypen von ADO nicht unterstützt: **adIDispatch**, **adIUnknown** und **adIVariant**. Für diese Typen tritt beim Anfügen kein Fehler auf, aber die Verwendung kann zu unvorhersehbaren Ergebnissen, wie z. B. Speicherverlusten, führen.</span><span class="sxs-lookup"><span data-stu-id="3e696-p111">**Field** objects of the following data types (**DataTypeEnum**) cannot be appended to the **Fields** collection and will cause an error to occur: **adArray**, **adChapter**, **adEmpty**, **adPropVariant**, and **adUserDefined**. Also, the following data types are not supported by ADO: **adIDispatch**, **adIUnknown**, and **adIVariant**. For these types, no error will occur when appended, but usage can produce unpredictable results including memory leaks.</span></span>

<span data-ttu-id="3e696-154">**Recordset**</span><span class="sxs-lookup"><span data-stu-id="3e696-154">**Recordset**</span></span>

<span data-ttu-id="3e696-155">Wenn Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft nicht festlegen, bevor Sie die **Append** -Methode aufrufen, wird **CursorLocation** automatisch auf **adUseClient** (einen [CursorLocationEnum](cursorlocationenum.md)-Wert) festgelegt, wenn die [Open](recordset-object-ado.md)-Methode des [Recordset](open-method-ado-recordset.md)-Objekts aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3e696-155">If you do not set the [CursorLocation](cursorlocation-property-ado.md) property before calling the **Append** method, **CursorLocation** will be set to **adUseClient** (a [CursorLocationEnum](cursorlocationenum.md) value) automatically when the [Recordset](recordset-object-ado.md) object's [Open](open-method-ado-recordset.md) method is called.</span></span>

<span data-ttu-id="3e696-p112">Ein Laufzeitfehler tritt auf, wenn die **Append** -Methode für die **Fields** -Auflistung eines geöffneten **Recordsets** oder für ein **Recordset**, für das die [ActiveConnection](activeconnection-property-ado.md)-Eigenschaft festgelegt wurde, aufgerufen wird. Sie können nur Felder zu einem **Recordset** hinzufügen, das nicht geöffnet ist und noch nicht mit einer Datenquelle verbunden wurde. Dies ist normalerweise der Fall, wenn ein **Recordset** -Objekt mit der [CreateRecordset](createrecordset-method-rds.md)-Methode erstellt oder einer Objektvariablen zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3e696-p112">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset**, or on a **Recordset** where the [ActiveConnection](activeconnection-property-ado.md) property has been set. You can only append fields to a **Recordset** that is not open and has not yet been connected to a data source. This is typically the case when a **Recordset** object is fabricated with the [CreateRecordset](createrecordset-method-rds.md) method or assigned to an object variable.</span></span>

<span data-ttu-id="3e696-159">**Record**</span><span class="sxs-lookup"><span data-stu-id="3e696-159">**Record**</span></span>

<span data-ttu-id="3e696-p113">Es tritt kein Laufzeitfehler auf, wenn die **Append** -Methode für die **Fields** -Auflistung eines geöffneten **Record** -Objekts aufgerufen wird. Das neue Feld wird der **Fields** -Auflistung des **Record** -Objekts hinzugefügt. Wenn das **Record** -Objekt von einem **Recordset** abgeleitet wurde, wird das neue Feld nicht in der **Fields** -Auflistung des **Recordset** -Objekts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3e696-p113">A run-time error will not occur if the **Append** method is called on the **Fields** collection of an open **Record**. The new field will be added to the **Record** object's **Fields** collection. If the **Record** was derived from a **Recordset**, then the new field will not appear in the **Recordset** object's **Fields** collection.</span></span>

<span data-ttu-id="3e696-p114">Sie können ein nicht vorhandenes Feld erstellen und der **Fields** -Auflistung anfügen, indem Sie dem Feldobjekt einen Wert zuweisen, als sei es bereits in der Auflistung vorhanden. Durch die Zuweisung wird die automatische Erstellung und Anfügung des **Field** -Objekts ausgelöst, dann wird die Zuweisung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3e696-p114">A non-existent field can be created and appended to the **Fields** collection by assigning a value to the field object as if it already existed in the collection. The assignment will trigger the automatic creation and appending of the **Field** object, then the assignment will be completed.</span></span>

<span data-ttu-id="3e696-165">Rufen Sie nach dem Anfügen eines **Field** -Objekts an die **Fields** -Auflistung eines **Record** -Objekts die **Update** -Methode der **Fields** -Auflistung auf, um die Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3e696-165">After appending a **Field** to a **Record** object's **Fields** collection, call the **Update** method of the **Fields** collection to save the change.</span></span>

