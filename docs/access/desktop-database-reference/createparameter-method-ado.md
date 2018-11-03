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
ms.openlocfilehash: 88a5d62cc94aa707c2e90467d74dc07d80a0af02
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928943"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="3868d-102">CreateParameter-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="3868d-102">CreateParameter method (ADO)</span></span>


<span data-ttu-id="3868d-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3868d-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="3868d-104">Erstellt ein neues [Parameter](parameter-object-ado.md)-Objekt mit den angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3868d-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3868d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3868d-105">Syntax</span></span>

<span data-ttu-id="3868d-106">**Festlegen** *Parameter*  =  *Befehl*. "CreateParameter" (*Name*, *Typ*, *Richtung*, *Größe*, *Wert*)</span><span class="sxs-lookup"><span data-stu-id="3868d-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

## <a name="return-value"></a><span data-ttu-id="3868d-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3868d-107">Return value</span></span>

<span data-ttu-id="3868d-108">Gibt ein **Parameter** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3868d-108">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="3868d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3868d-109">Parameters</span></span>

  - <span data-ttu-id="3868d-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="3868d-110">*Name*</span></span>

  - <span data-ttu-id="3868d-p101">Optional. Ein **String** -Wert, der den Namen des **Parameter** -Objekts enthält.</span><span class="sxs-lookup"><span data-stu-id="3868d-p101">Optional. A **String** value that contains the name of the **Parameter** object.</span></span>

  - <span data-ttu-id="3868d-113">*Type*</span><span class="sxs-lookup"><span data-stu-id="3868d-113">*Type*</span></span>

  - <span data-ttu-id="3868d-p102">Optional. Ein [DataTypeEnum](datatypeenum.md)-Wert, der den Datentyp des **Parameter** -Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="3868d-p102">Optional. A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="3868d-116">*Direction*</span><span class="sxs-lookup"><span data-stu-id="3868d-116">*Direction*</span></span>

  - <span data-ttu-id="3868d-p103">Optional. Ein [ParameterDirectionEnum](parameterdirectionenum.md)-Wert, der den Typ des **Parameter** -Objekts angibt.</span><span class="sxs-lookup"><span data-stu-id="3868d-p103">Optional. A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>

  - <span data-ttu-id="3868d-119">*Size*</span><span class="sxs-lookup"><span data-stu-id="3868d-119">*Size*</span></span>

  - <span data-ttu-id="3868d-p104">Optional. Ein **Long** -Wert, der die maximale Länge des Parameterwerts in Zeichen oder Bytes angibt.</span><span class="sxs-lookup"><span data-stu-id="3868d-p104">Optional. A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>

  - <span data-ttu-id="3868d-122">*Wert*</span><span class="sxs-lookup"><span data-stu-id="3868d-122">*Value*</span></span>

  - <span data-ttu-id="3868d-p105">Optional. Ein **Variant** -Wert, der den Wert für das **Parameter** -Objekt angibt.</span><span class="sxs-lookup"><span data-stu-id="3868d-p105">Optional. A **Variant** that specifies the value for the **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3868d-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3868d-125">Remarks</span></span>

<span data-ttu-id="3868d-p106">Verwenden Sie die **CreateParameter** -Methode, um ein neues **Parameter** -Objekt mit einem angegebenen Namen, Typ, einer angegebenen Lesefolge und Größe sowie einem angegeben Wert zu erstellen. In Argumenten übergebene Werte werden in die entsprechenden **Parameter** -Eigenschaften geschrieben.</span><span class="sxs-lookup"><span data-stu-id="3868d-p106">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value. Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="3868d-p107">Diese Methode fügt das **Parameter** -Objekt nicht automatisch der **Parameters** -Auflistung eines [Command](command-object-ado.md)-Objekts hinzu. Dadurch können Sie zusätzliche Eigenschaften festlegen, deren Werte ADO validiert, wenn Sie das **Parameter** -Objekt der Auflistung anfügen.</span><span class="sxs-lookup"><span data-stu-id="3868d-p107">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="3868d-130">Wenn Sie einen Datentyp variabler Länge im *Argument* angeben, müssen Sie eine *Größe* -Argument übergeben oder die [Size](size-property-ado.md) -Eigenschaft des **Parameter** -Objekts festlegen, bevor er an der **Parameters** -Auflistung angefügt; andernfalls, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="3868d-130">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="3868d-131">Wenn Sie im Argument *Type* einen numerischen Datentyp (**adNumeric** oder **adDecimal**) angeben, müssen Sie auch die Eigenschaften [NumericScale](numericscale-property-ado.md) und [Precision](precision-property-ado.md) festlegen.</span><span class="sxs-lookup"><span data-stu-id="3868d-131">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>

