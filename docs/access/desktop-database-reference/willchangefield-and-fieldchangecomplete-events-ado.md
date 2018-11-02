---
title: WillChangeField- und FieldChangeComplete-Ereignisse (ADO)
TOCTitle: WillChangeField and FieldChangeComplete events (ADO)
ms:assetid: bc4455a6-2925-33dc-d04f-8ea570e5e370
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249904(v=office.15)
ms:contentKeyID: 48547407
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2967b6670ad96752e7ce47d82227fad70335e1f6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927403"
---
# <a name="willchangefield-and-fieldchangecomplete-events-ado"></a><span data-ttu-id="35e2c-102">WillChangeField- und FieldChangeComplete-Ereignisse (ADO)</span><span class="sxs-lookup"><span data-stu-id="35e2c-102">WillChangeField and FieldChangeComplete events (ADO)</span></span>


<span data-ttu-id="35e2c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="35e2c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="35e2c-p101">Das **WillChangeField** -Ereignis wird aufgerufen, bevor der Wert eines oder mehrerer [Field](field-object-ado.md)-Objekte im [Recordset](recordset-object-ado.md)-Objekt durch einen ausstehenden Vorgang geändert wird. Das **FieldChangeComplete** -Ereignis wird aufgerufen, nachdem der Wert eines oder mehrerer **Field** -Objekte geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="35e2c-p101">The **WillChangeField** event is called before a pending operation changes the value of one or more [Field](field-object-ado.md) objects in the [Recordset](recordset-object-ado.md). The **FieldChangeComplete** event is called after the value of one or more **Field** objects has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="35e2c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="35e2c-106">Syntax</span></span>

<span data-ttu-id="35e2c-107">WillChangeField-*cFields*, *Felder*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="35e2c-107">WillChangeField*cFields*, *Fields*, *adStatus*, *pRecordset*</span></span>

<span data-ttu-id="35e2c-108">FieldChangeComplete*cFields*, *Felder*, *pError*, *AdStatus*, *pCommand*</span><span class="sxs-lookup"><span data-stu-id="35e2c-108">FieldChangeComplete*cFields*, *Fields*, *pError*, *adStatus*, *pRecordset*</span></span>

## <a name="parameters"></a><span data-ttu-id="35e2c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="35e2c-109">Parameters</span></span>

  - <span data-ttu-id="35e2c-110">*cFields*</span><span class="sxs-lookup"><span data-stu-id="35e2c-110">*cFields*</span></span>

  - <span data-ttu-id="35e2c-111">Ein **Long**-Wert, der die Anzahl der **Field**-Objekte von *Fields* angibt.</span><span class="sxs-lookup"><span data-stu-id="35e2c-111">A **Long** that indicates the number of **Field** objects in *Fields*.</span></span>

  - <span data-ttu-id="35e2c-112">*Fields*</span><span class="sxs-lookup"><span data-stu-id="35e2c-112">*Fields*</span></span>

  - <span data-ttu-id="35e2c-113">Für **WillChangeField**ist der Parameter *Felder* Arrays von **Varianten** , die mit den ursprünglichen Werten **Field** -Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="35e2c-113">For **WillChangeField**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the original values.</span></span>  
      
    <span data-ttu-id="35e2c-114">Für **FieldChangeComplete**ist der Parameter *Felder* Arrays von **Varianten** , die mit den geänderten Werten **Field** -Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="35e2c-114">For **FieldChangeComplete**, the *Fields* parameter is an array of **Variants** that contains **Field** objects with the changed values.</span></span>

  - <span data-ttu-id="35e2c-115">*pError*</span><span class="sxs-lookup"><span data-stu-id="35e2c-115">*pError*</span></span>

  - <span data-ttu-id="35e2c-p102">Ein [Error](error-object-ado.md)-Objekt. Es beschreibt den Fehler, der auftritt, wenn der *adStatus* -Wert **adStatusErrorsOccurred** lautet. Andernfalls wird er nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="35e2c-p102">An [Error](error-object-ado.md) object. It describes the error that occurred if the value of *adStatus* is **adStatusErrorsOccurred**; otherwise it is not set.</span></span>

  - <span data-ttu-id="35e2c-118">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="35e2c-118">*adStatus*</span></span>

  - [<span data-ttu-id="35e2c-119">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="35e2c-119">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="35e2c-p103">Wird **WillChangeField** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Der Parameter wird auf **adStatusCantDeny** festgelegt, wenn dieses Ereignis den Abbruch des ausstehenden Vorgangs nicht anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="35e2c-p103">When **WillChangeField** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful. It is set to **adStatusCantDeny** if this event cannot request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="35e2c-122">Wird **FieldChangeComplete** aufgerufen, wird dieser Parameter auf **adStatusOK** festgelegt, wenn der das Ereignis verursachende Vorgang erfolgreich war. Er wird auf **adStatusErrorsOccurred** festgelegt, wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="35e2c-122">When **FieldChangeComplete** is called, this parameter is set to **adStatusOK** if the operation that caused the event was successful, or to **adStatusErrorsOccurred** if the operation failed.</span></span>
    
    <span data-ttu-id="35e2c-123">Legen Sie diesen Parameter vor der Rückgabe von **WillChangeField** auf **AdStatusCancel** fest, um den Abbruch des ausstehenden Vorgangs anzufordern.</span><span class="sxs-lookup"><span data-stu-id="35e2c-123">Before **WillChangeField** returns, set this parameter to **adStatusCancel** to request cancellation of the pending operation.</span></span>
    
    <span data-ttu-id="35e2c-124">Legen Sie diesen Parameter vor der Rückgabe von **FieldChangeComplete** auf **AdStatusUnwantedEvent** fest, um nachfolgende Benachrichtigungen zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="35e2c-124">Before **FieldChangeComplete** returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications.</span></span>

  - <span data-ttu-id="35e2c-125">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="35e2c-125">*pRecordset*</span></span>

  - <span data-ttu-id="35e2c-p104">Ein **Recordset**-Objekt. Das **Recordset** -Objekt, für das dieses Ereignis eingetreten ist.</span><span class="sxs-lookup"><span data-stu-id="35e2c-p104">A **Recordset** object. The **Recordset** for which this event occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="35e2c-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="35e2c-128">Remarks</span></span>

<span data-ttu-id="35e2c-129">Ein **WillChangeField** - oder ein **FieldChangeComplete** -Ereignis kann eintreten, wenn die [Value](value-property-ado.md)-Eigenschaft festgelegt und die [Update](update-method-ado.md)-Methode mit Feld- und Wertarrayparametern aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="35e2c-129">A **WillChangeField** or **FieldChangeComplete** event may occur when setting the [Value](value-property-ado.md) property and calling the [Update](update-method-ado.md) method with field and value array parameters.</span></span>

